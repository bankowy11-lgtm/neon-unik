# Neon Unik

Neonowa gra zręcznościowa na telefon: przesuwasz statek palcem, unikasz przeszkód, zbierasz gwiazdki (combo do x8) i bonusy (T = tarcza, S = spowolnienie). Za „blisko!” (minięcie przeszkody o włos) jest +5.

## Pliki

| Plik | Do czego |
|---|---|
| `index.html` | cała gra (HTML + CSS + JavaScript, rysowanie na `<canvas>`) |
| `manifest.webmanifest` | nazwa, ikona, kolory, pełny ekran — dzięki temu gra jest „aplikacją” (PWA) |
| `sw.js` | service worker — gra działa offline |
| `icon.svg` | ikona |

Uruchomienie lokalne: `python -m http.server 8794 -d neon-unik` i otwórz http://localhost:8794

## Droga do Google Play

1. **Hosting** – wrzuć folder na GitHub Pages (tak jak Italia Gusto). Gra ma wtedy adres https://… i można ją zainstalować z przeglądarki.
2. **Ikony PNG** – Google Play wymaga ikony 512×512 PNG (i 192×192 dla PWA). Do zrobienia z `icon.svg`.
3. **Paczka Androida (.aab)** – najprościej przez https://www.pwabuilder.com: wklejasz adres gry → „Package for stores” → Android. Dostajesz gotowy plik `.aab` (aplikacja typu TWA – pełnoekranowe okno Chrome z Twoją grą) oraz plik `assetlinks.json`, który trzeba wrzucić do `/.well-known/` na stronie (bez tego pokaże się pasek adresu).
   Alternatywa: **Capacitor** (`npx cap add android`) + Android Studio — więcej pracy, ale gra jest wtedy w paczce i działa bez internetu od pierwszego uruchomienia.
4. **Konto deweloperskie Google Play** – jednorazowo 25 USD, weryfikacja tożsamości.
5. **Testy zamknięte** – nowe konta prywatne muszą przed publikacją przeprowadzić test zamknięty: min. 12 testerów przez 14 dni.
6. **Karta sklepu** – opis, min. 2 zrzuty ekranu, grafika 1024×500, polityka prywatności (link — wystarczy prosta strona, że gra nie zbiera danych), ankieta klasyfikacji wiekowej, formularz „Bezpieczeństwo danych”.
7. **Publikacja** – przegląd Google trwa zwykle od kilku dni do tygodnia.
