# Optymalizacja kodu

---

### Ogólnie

- dołączanie **script** na samym koncu **body**
- słowo kluczowe `<script src="scripts.js" async ></script>` jeśli skrypt nie wpływa ani na **DOM** ani na **CSSOM** _(**CSS** **O**bject **M**odule manipulacja css za pomocą JS - dynamiczna zmiana stylów)_
- skrypt **inline** i zwykly **src** blokuje wykonywanie kodu
- usuwanie nieużywanego kodu
- cashowanie plikow js przy przejsciu na inne subdomeny
- umieszczanie plików statycznych na osobnej subdomenie i integracja z siecią CDN
- mimifikacja - optymalizacja kodowania i rozmiaru plików
  - usuwa **spacje**, **taby**, **znaki nowej lini** i **komentarze**
  - zmienia nazwy **funkcji** i **zmiennych** na jednoliterowe

#### Web Vitails

- LCP **L**argest **C**ontentful **P**aint - _(Ładowanie)_
- FID **F**irst **I**nput **D**elay _(Interakcja)_
- CLS **C**umulative **L**ayout **S**hift _(Stabilizacja wizualna)_ np. next, image
  - zamiast zmiany `width` i `height` używać `transform: scale()`.
  - do przesuwania zamiast `top` `left` `right` `bottom` używać `transform: translate()`

---

### JavaScript (React)

**Memoizacja** - zapisywanie wyniku kosztownych pod względem wydajnosci funkcji dla takich samych argumentów **_(React.memo, useCallback, useMemo)_**

- **Lazy Load** - Code spliting przy duzych komponentach typu chartjs czy leaflet map **_(React.lazy, Suspense i fallback)_**
- **Caschowanie** danych z zewnątrz, które wiemy że się nie zmienią np. **Redis** (React query (Pure Component)
- **SSR** - **S**erver **S**ide **R**endering i **SSG** - **S**tatic **G**eneration (90% przypadków) dla lepszego **SEO**
- Image optymalization np **Next.js**

---

#### podsumowanie

- kod powinien byc pozbawiony wszelkich białych znaków i nieużywanych funkcji (niech to robi prettier eslint i babel)
- Cashować wyniki pamięciochłonnych funkcji
- Używać ssr żeby roboty googla nie widziały tylko `<div id="app">`
- Jeśli szybkosc strony nie jest zła warto zająć się czym innym niż optymalizacja
