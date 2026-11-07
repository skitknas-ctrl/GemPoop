# GemPoop

Ett tvåtummarsspel för liggande skärm. Fyra apor står på en gammal packlår med baken
mot spelaren, och ur deras anus ploppar ädelstenar ut. Din uppgift är att vinkla
paddeln i botten så att varje sten studsar upp till grodan med samma färg.

![Skärmbild](design/skarmbild.png)

![Butiken mellan nivåerna](design/butik.png)

## Spelplanen

- Spelplanen är kvadratisk och fyller hela skärmens höjd.
- De nedersta 20 % är en svart yta med paddeln. Paddeln är 70 % av planens bredd och sitter fast i mitten.
- Ovanför den svarta ytan står packlåren, 55 % av höjden, byggd av gamla brädor.
- Fyra olika apor står på lådan: en schimpans, en orangutang, en gorilla och en babian.
  Deras anus sitter 8 % från överkanten, vid 20, 40, 60 och 80 % från vänster.
- På lådans kant sitter en blå groda vid 30 %, en gul vid 50 % och en grön vid 70 %.
- Ytorna till vänster och höger om spelplanen är fulla av fingeravtryck. Det är där tummarna styr.

## Så spelar du

- All text i spelet är på engelska.
- Lägg en tumme på varje fingeravtrycksyta. Paddeln lutar efter hur högt tummarna ligger
  i förhållande till varandra. Håller du vänster tumme högre lyfts paddelns vänstra ände.
- En ädelsten anas först i en apas anus och pressas sedan fram under en sekund innan den ploppar ut.
- Stenarna faller allt snabbare, studsar mot paddeln och bromsar in på vägen upp i en parabel.
- Kommer en sten inom räckhåll för grodan med samma färg skjuter grodan ut tungan och sväljer den.
- Stenar som landar på lådan tonar långsamt bort. Både de och stenar som faller förbi
  paddeln räknas som missade.
- Färgerna har olika slipform (blå romb, gul rund, grön smaragdslipning, röd trekant) så att
  de går att skilja åt även för den som är färgblind.

## Nivåer, poäng och butik

- Varje nivå har 20 ädelstenar. Nivå 1 ger 0,8 stenar per sekund, och varje ny nivå lägger till 0,2 (högst 3,5).
- Efter varje nivå dras de missade stenarna av från de fångade, och resultatet läggs till poängen.
- Hamnar poängen under noll är spelet slut.
- Mellan nivåerna kan poäng köpa längre tunga, en procent i taget och för varje groda för sig.
  Varje ny procent blir dyrare: 3, 4, 6, 8, 12, 16, 23 … poäng (högst 40 %).
- Från nivå 4 kommer ibland röda ädelstenar. Fångar en groda en röd sten klipps tungan av
  till ursprungslängden, och de köpta procenten försvinner. Röda stenar räknas aldrig som missade.
- Andelen röda stenar ökar för varje nivå: 8 % på nivå 4, sedan 5 procentenheter mer per nivå (högst 45 %).
- Bästa poäng och bästa nivå sparas i telefonen.

## Inställningar (kugghjulet)

- **Starting gem rate:** stenar per sekund på nivå 1 (0,5–2).
- **Base tongue reach:** tungornas ursprungslängd i procent av spelplanens bredd (5–20). Det är hit de röda stenarna klipper tillbaka tungan.
- **Show tongue reach:** en streckad ring runt varje groda.

Ändringar av takt och räckvidd gäller från nästa nytt spel.

## Teknik

- Själva spelet är `index.html`, utan beroenden. Det går att köra direkt i en webbläsare
  eller via GitHub Pages.
- Android-appen är ett tunt WebView-skal i liggande läge. Navigeringsknapparna är dolda
  under spelet (ett svep från kanten visar dem tillfälligt), och spelet hålls innanför statusfältet.
- GitHub Actions bygger en test-APK vid varje push till `main`. Den publiceras som
  senaste release: `releases/latest/download/gempoop-debug.apk`.
- `design/Main.dc.html` är originalskissen från Claude Design.
- Appen har inga annonser och ingen spårning, och den använder inget nätverk.
