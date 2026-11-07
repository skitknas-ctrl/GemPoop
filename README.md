# GemPoop

Ett tvåtummarsspel för liggande skärm. Fyra apor står på en gammal packlår med baken
mot spelaren, och ur deras anus ploppar ädelstenar ut. Din uppgift är att vinkla
paddeln i botten så att varje sten studsar upp till grodan med samma färg.

![Skärmbild](design/skarmbild.png)

## Spelplanen

- Spelplanen är kvadratisk och fyller hela skärmens höjd.
- De nedersta 20 % är en svart yta med paddeln. Paddeln är 70 % av planens bredd och sitter fast i mitten.
- Ovanför den svarta ytan står packlåren, 55 % av höjden, byggd av gamla brädor.
- Fyra olika apor står på lådan: en schimpans, en orangutang, en gorilla och en babian.
  Deras anus sitter 8 % från överkanten, vid 20, 40, 60 och 80 % från vänster.
- På lådans kant sitter en blå groda vid 30 %, en gul vid 50 % och en grön vid 70 %.
- Ytorna till vänster och höger om spelplanen är fulla av fingeravtryck. Det är där tummarna styr.

## Så spelar du

- Lägg en tumme på varje fingeravtrycksyta. Paddeln lutar efter hur högt tummarna ligger
  i förhållande till varandra. Håller du vänster tumme högre lyfts paddelns vänstra ände.
- Varje sekund (som standard) ploppar en ädelsten ut ur ett slumpvis valt anus, i en slumpvis vald färg.
- Stenarna faller allt snabbare, studsar mot paddeln och bromsar in på vägen upp i en parabel.
- Kommer en sten inom räckhåll för grodan med samma färg skjuter grodan ut tungan och sväljer den.
- Stenar som landar på lådan tonar långsamt bort. Både de och stenar som faller förbi
  paddeln räknas som missade.
- Färgerna har olika slipform (blå romb, gul rund, grön smaragdslipning) så att de går
  att skilja åt även för den som är färgblind.

## Inställningar (kugghjulet)

- **Frekvens:** 0,25–3 ädelstenar per sekund.
- **Tungans räckvidd:** 4–25 % av spelplanens bredd.
- **Visa räckvidd:** en streckad ring runt varje groda.

Inställningarna sparas i telefonen.

## Teknik

- Själva spelet är `index.html`, utan beroenden. Det går att köra direkt i en webbläsare
  eller via GitHub Pages.
- Android-appen är ett tunt WebView-skal i liggande läge. Spelet hålls innanför
  statusfältet och navigeringsfältet.
- GitHub Actions bygger en test-APK vid varje push till `main`. Den publiceras som
  senaste release: `releases/latest/download/gempoop-debug.apk`.
- `design/Main.dc.html` är originalskissen från Claude Design.
- Appen har inga annonser och ingen spårning, och den använder inget nätverk.
