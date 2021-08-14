# JS Bundle

Im mniejszy bundle tym lepiej dla czasu ładowania strony i SEO
Bundle może składać się z wielu plików js.

---

## Webpack

_ES 6_
`import Search from 'components';`
_Common JS_
`const Search = require('components/search');`

Webpack buduje bandle tworząc drzewo zależnośći począwszy od pliku wejsciowego.

Przetwarza kod naszej aplikacji wyszukując zależności pomiędzy modułami.
Umożliwia zarządzanie asetami np `.css` `.png` `.svg` czy fontami

- **Entry** - plik wejsciowy (od niego tworzone jest _drzewo zależności_)
- **Output** - plik w wktórym zostanie zapisany bandle
- **Loadery** - przetwarzają pojedyńcze pliki, aby mogły być dodane do drzewa zależności
- **Pluginy** - wykonują pomocnicze operacje np. **mimifikacja js** lub np przenoszenie kodu css do osobnych plików.

---

### Code Spliting

Wydziela elementy aplikacji do osobnych plików bandlowych

Pozwala doładowywać dane komponenty (i duze biblioteki) (zazwyczaj te rzadko uzywane przez uzytkowników, które dużo ważą np. jakies dane czy statystyki) dopiero wtedy, kiedy zajdzie taka potrzeba. Dzięki czemu początkowy bandle jest dużo mniejszy co jest dobre dla ładowania strony, zwłaszcza na użadzeniach mobilnych, (które są teraz częściej używane niż desktopy)

#### React Lazy

Działa na zasadzie **dinamic imports**

```
React.lazy(() => import Search from "components/Search");

const App = () => (
    <Suspense fallback={<div> </div>}>
        <Search />
    </Suspense>
)
```

#### Next Dynamic

```

const Puppy = dynamic(() => import("../components/Puppy"), {
  loading: () => <p>Loading...</p>
});

```
