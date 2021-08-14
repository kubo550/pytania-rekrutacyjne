# Zadanie praktyczne

- Napisz funkcję, która jako argument przyjmuje dowolną tablicę liczb, a następnie zwraca jej zduplokowaną wersję ([1, 2, 3] => [1, 2, 3, 1, 2, 3].

- Napisz funkcję, która sprawdzi, czy tablica jest posortowana. Jeśli jest posortowana zwróć `true`.
- Napisz funkcję, która przyjmuję dowolną liczbę naturalną i zwraca tablicę kolejnych liczb z ciągu Fibbonacciego mniejszych niż ta liczba.
- Napisz funkcję przyjmującą dowolną liczbę naturalną i zwracającą silnię tej liczby. Zadanie rozwiąż zarówno iteracyjnie, jak i rekurencyjnie.

# przykłady kodu

1. konwersja kodu

```javascript
console.log(false == "0"); // true
console.log(false === "0"); // false
```

2. floatingpoint

```javascript
console.log(0.1 + 0.2); // 0.300000000000004
console.log(0.1 + 0.2 === 0.3); //false
```

3. timeout i pętla

```javascript
for (var i = 0; i < 5; i++) {
  setTimeout(() => {
    console.log(i);
  }, 1000);
}
```

i jak naprawić

5 x 5, zmienić var na let / zastosować IIFE

4. setTimeout i stack

```javascript
console.log(1);
setTimeout(() => console.log(2), 0);
console.log(3); // 1, 3, 2
```

5. scope

```javascript
var global = 1;
(function fn(outer) {
  var local = "a";
  (function infn(inter) {
    var another = "c";
    console.log(global); // 1
    console.log(outer); // 2
    console.log(local); // a
    console.log(inter); // b
    console.log(another); // c
  })("b");
})(2);
```

6. this

```javascript
var obj = {
  foo: "1",
  fn: function () {
    const self = this;
    console.log(this.foo); // 1
    console.log(self.foo); // 1

    (function f() {
      console.log(this.foo); // Cannot read property 'foo' of undefined
      console.log(self.foo); // 1
    })();
  },
};
```

7. route

```javascript
app.get("/calculate/:price", (req, res) => {
  const grosze = Number(req.body.price);
  const zl = +(grosze / 100).toFixed(2);

  return res.status(200).json({ zl });
});
```

8. github api

```javascript
(async () => {
  const repos = await fetch("https://api.github.com/users/torvalds/repos");
  const reposJson = await repos.json();
  const data = reposJson
    .map(repo => `<p>${repo.name} - ${repo.stargazers_count}</p>`)
    .join("");

  document.getElementById("app").innerHTML = data;
})();
```
