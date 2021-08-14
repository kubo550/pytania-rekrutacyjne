# Pytania na wiedzę

<details>
<summary> Opisz różnice pomiędzy zmiennymi definiowanymi z użyciem <code>var</code>, <code>let</code> oraz <code>const</code>.</summary>
<div style="background-color: rgba(214, 235, 202, 1);">
<ul >
<li> <code>const</code> i <code>let</code> są z nami od <b>ES6</b>. </li>
<li> 
Zmienne zadeklarowane przez <code>var</code> ulegają <b> hoistingowi </b> i działają w kontekscie funkcji.
do <code>let</code> i <code>const</code> nie można się odwołać przed <b>inicjalizacją</b> i działają w kontekście blokowym <i> np. pętla for </i>
<pre>
<code>
for (let i = 0; i < 5; i++) {
setTimeout(() => console.log(i), 1000)
}
</code></pre></li>
<li>Zmienne deklarowane za pomącą <code>const</code> nie mogą być redefiniowane
<pre>
<code>
 let score = 10;
 score = score + 1;
 const divEl = document.getElementById('div1');
 divEl = 10 // Error
</code>
</pre></li>
</ul>
</div>
</code>
</details>

<details>
<summary> Na czym polega hoisting i które elementy mu podlegają? </summary>
<ul style="background-color: rgba(214, 235, 202, 1);">
<li>Polega na <i>wynoszeniu</i> zmiennych i funkcji (zadeklarowanych za pomocą słowa <code>function</code>) na sam początek scope'u.</li>
<li>Zmienne deklarowane za pomocą  <code>const</code> i <code>let</code> też ulegają hoistingowi, lecz trafiają do <b>Temporal Dead Zone</b> <a href="https://www.freecodecamp.org/news/what-is-the-temporal-dead-zone/">(TDZ)</a></li>
</details>

<details>
<summary> Opisz różnice pomiędzy funkcją definiowaną z użyciem słowa kluczowego <code>function</code> a arrow function. </summary>
<ul style="background-color: rgba(214, 235, 202, 1);">
<li> Arrow function nie tworzy zakresu </li>
<li> Do funkcji zadeklarowanej słowem kluczowym <code>function</code> można odwoływać się i przed i po zadeklarowaniu</li>
</ul>
</details>

<details>
<summary> Jaka jest różnica pomiędzy metodami <code>map()</code> oraz <code>forEach()</code>. Do czego możemy wykorzystać te metody. </summary> 
<ul style="background-color: rgba(214, 235, 202, 1);">
<li>Metoda <code>map()</code> zwraca nową tablice </li>
<li>Metoda <code>forEach()</code> działa na oryginalnej tablicy. Więc nie powinno się zmieniać elementów tablicy tym sposobem (a zwłaszcza kiedy nie rozumie się różnicy)  </li>
</ul>
</details>

<details>
<summary> Jak działa metoda <code>reduce()</code>? Jakie argumenty przyjmuje ta metoda oraz przekazany do niej callback? </summary> 
<ul style="background-color: rgba(214, 235, 202, 1);">
<li>
    todo
</li>
</ul>
</details>

<details>
<summary> Wymień różnice pomiędzy <code>Cookies</code>, <code>Local Storage</code> i <code>Session Storage</code> </summary>
| x                      | Cookies               | Local Storage | Session Storage    |
| ---------------------- | --------------------- | ------------- | ------------------ |
| **Max rozmiar**        | 4kb                   | 10mb          | 5mb                |
| **HTML**               | HTML4 / HTML5         | HTML5         | HTML5              |
| **Dostępność**         | tylko dana domena     | każde okno    | to samo okno       |
| **Żywotność**          | do ustawienia         | nigdy         | do zamknięcia okna |
| **Lokalizacja**        | przeglądarka i server | przegladarka  | przegladarka       |
| **Wysyłany w request** | tak                   | nie           | nie                |
</details>

<details>
<summary> Opisz różnicę pomiędzy kompozycją a dziedziczeniem uwzględniając wady i zalety każdego z tych podejść. </summary> 
<ul style="background-color: rgba(214, 235, 202, 1);">
<li> <a href="https://www.youtube.com/watch?v=E_BRt_fqaeA"> youtube </li>
</ul>
</details>

<details>
<summary> Wymień kilka wzorców pozwalających na tworzenie obiektów. </summary> 
<ul style="background-color: rgba(214, 235, 202, 1);">
<li> Poprzez zwykle <code>const obj = {}</code>  </li>
<li> Za pomocą klas <code> const obj = new Obj() </code> </li>
<li> Używając fabryk <code>factory function</code>
    <pre>
    <code>
    const list = () => {
        const items = [];
        return {
            addItem = (item) => items.push(item),
            showItems = () => items
        } 
    }
    </code>
    </pre>
 </li>
</ul>
</details>

<details>
<summary> Na czym polega bąbelkowanie (ang. bubbling) oraz propagacja zdarzeń? </summary> 
<ul style="background-color: rgba(214, 235, 202, 1);">
<li> todo </li>
</ul>
</details>

<details>
<summary> W jaki sposób jednowątkowy język, jakim jest JS pozwala na wykonywanie asynchronicznych operacji? Czym jest event loop? </summary> 
<ul style="background-color: rgba(214, 235, 202, 1);">
<li> Aby nie blokować wykonywanego kodu wykorzystujemy <code>Promise</code> funkcja działa w tle i gdy się skończy wykona się callback</li>
<li>
    Można używać <code>.then()</code> albo <code>async await</code>
</li>
<li> <code>async await</code> jest czytelniejsze i wykorzystuje 
<pre>
<code>
try {
    await doSomething();
} catch(error) {
    cnosole.error(error)
}
</code>
</pre>
</li>
</ul>
</details>

<details>
<summary> Czym jest `Symbol`? </summary> 
<ul style="background-color: rgba(214, 235, 202, 1);">
<li>todo </li>
</ul>
</details>

<details>
<summary> Na czym polega mechanizm koercji w języku JavaScript? </summary> 
<ul style="background-color: rgba(214, 235, 202, 1);">
<li>todo </li>
</ul>
</details>

<details>
<summary> Wymień różnice między `axios` a `fetch`. </summary> 
<ul style="background-color: rgba(214, 235, 202, 1);">
<li>todo </li>
</ul>
</details>

<details>
<summary> Co to jest domknięcie? Podać przykład kodu. </summary> 
<ul style="background-color: rgba(214, 235, 202, 1);">
<li> Closure jest wtedy, kiedy mamy dostęp do zmiennej poza jej obecnym zakresem</li>
<li> <pre> <code>
const points = () => {
    let score = 0;

    return {
        getScore:() => score,
        addScore: (scores) => score += scores
    }

}
</code> </pre> </li>

</ul>
</details>

<details>
<summary> Jaka jest różnica między `==` i `===`? </summary> 
<ul style="background-color: rgba(214, 235, 202, 1);">
<li> </li>
</ul>
</details>

<details>
<summary> W jaki sposób możemy zmienić kontekst wywołania funkcji? </summary> 
<ul style="background-color: rgba(214, 235, 202, 1);">
<li> bind(this) - zwraca funkcję z nowym kontekstem </li>
<li> call() - wywołuje funkcje z nowym kontekstem, od apply rózni się tym ze tu oarametry do funkcji przekazuje się po przecinku a nie w tablicy </li>
<li> appy() - wywołuje funkcje z nowym kontekstem, parametry funkcji są przekazywane w tablicy </li>
</ul>
</details>

<details>
<summary> Jakie znasz sposoby optymalizacji wydajności stron internetowych? </summary> 
<ul style="background-color: rgba(214, 235, 202, 1);">
<li> Używanie Server Side Rendering (Next.js, vuex) </li>
<li> Code spliting np. lazy load  - zmiejsza rozmiar początkowego bundle'a dzieki czemu strona ładuje się szybciej [todo link]() </li>
</ul>
</details>

<details>
<summary> Co to jest `use strict` </summary> 
<ul style="background-color: rgba(214, 235, 202, 1);">
<li> </li>
</ul>
</details>

<details>
<summary> Co to jest `ajax` </summary> 
<ul style="background-color: rgba(214, 235, 202, 1);">
<li> </li>
</ul>
</details>

<details>
<summary> Czym jest i do czego jest używana funkcja natychmiastowa (IIFE)? </summary> 
<ul style="background-color: rgba(214, 235, 202, 1);">
<li> </li>
</ul>
</details>

<details>
<summary> Co to jest `hoisting`? </summary> 
<ul style="background-color: rgba(214, 235, 202, 1);">
<li> </li>
</ul>
</details>

<details>
<summary> Wymień typy w JS (Prymitywne i Referencyjne) </summary> 
<ul style="background-color: rgba(214, 235, 202, 1);">
<li> </li>
</ul>
</details>

<details>
<summary> Czy w JS'ie występuje dziedziczenie? </summary> 
<ul style="background-color: rgba(214, 235, 202, 1);">
<li> tak np. <code> class App extends React.Component {} </code> </li>
</ul>
</details>

---

- Czym różni się `mongo db` od `mysql`
- Klasy kodów `HTTP` (200, 300, 400, 500)
- Metody `HTTP` (`PUT`, `GET`, `PATCH`, `POST`, `DELETE`) - różnica między `PUT` i `PATCH`
- Tworzenie sessji http, headers, token

- Gdzie dodać znacznik script? przed zamknięciem body, czy w nagłówku? // _przed zamknięciem body_
- Ile może być maksymalnie znaczników `nav`? // _1 (ułatwienie dla osob np niewidzących)_
- Jak przekazać z html do css jakieś stringi ? // `data-atrybut`
- Jak tworzyć i konfigurować tokeny w `axios`
- Jaka jest różnica w `sass` pomiędzy `placeholder` a `mixin`
- Sposoby optymalizacji kodu
- Konfiguracja webpacka

- czym się rózni deklaracja funkcji od przypisania jej do zmiennej
- czym są genric type (typescript);
- czym jest redux thunk
- opisz działanie reduxa
- czym się rózni object programing od functional programming

- Jak działa `jwt`
- róznice między `HTTP` a `HTTPS`
- git `merge` vs `rebase`
- czym jest `mock` - Mock to obiekt, którego używa się zamiast rzeczywistej implementacji w trakcie testów jednostkowych.
- do czego sluzy cron - cron jest opartym na czasie programem do harmonogramowania zadań w systemach operacyjnych z rodziny Unixa. Może zostać wykorzystany do uruchamiania zadań (programów, komend, skryptów) o określonych godzinach,
- do czego słuzy indeksowanie w bazie danych
- w jaki sposób wysyłasz zapytania do api // postman insomnia przeglądarka
