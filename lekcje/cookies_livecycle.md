# Cookies vs Local Storage vs Session Storage

Są wykorzystywane do zapisywania danych sesynjych takich jak stan zalogowania uzytkownika czy theme. Powinny poisadać mksymalnie **niezbędne minimum** o danym użytkowniku

---

| x                      | Cookies               | Local Storage | Session Storage    |
| ---------------------- | --------------------- | ------------- | ------------------ |
| **Max rozmiar**        | 4kb                   | 10mb          | 5mb                |
| **HTML**               | HTML4 / HTML5         | HTML5         | HTML5              |
| **Dostępność**         | tylko dana domena     | każde okno    | to samo okno       |
| **Żywotność**          | do ustawienia         | nigdy         | do zamknięcia okna |
| **Lokalizacja**        | przeglądarka i server | przegladarka  | przegladarka       |
| **Wysyłany w request** | tak                   | nie           | nie                |

---

# Cykl życia komponentu

### Montowanie (Mount)

- constructor(props)
- componentWillMount()
- render ()
- comopnentDidMount()

```
    useEffect(() => {
        // only once
    }, [])
```

### Aktualizacja (Update)

- componentWillReceiveProps(nextProps)
- shouldComponentUpdate(nextProps, nextState)

`React.memo`

- componentWillUpdate(nextProps, nextState)
- render
- componentDidUpdate(prevProps, prevState)

```
    useEffect(() => {

    }, [dependencies])
```

### Odmontowywanie

componentWillUnmount()

```
    useEffect(() => {

        return () => { // cleanup }
    }, [])
```

#### Łapanie błędów

- componentDidCatch(error, info)
