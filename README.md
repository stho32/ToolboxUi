# ToolboxUi
An experiment for a different approach to UI

Datum: 17.06.2023
Verantwortlich: Stefan Hoffmann
Mentor: 

## Hintergrund / Problem

Ich habe mich mit der Art beschäftigt, wie im Toyota Production System Automatisierung verstanden wird. 
Der im "Toyota Way" beschriebene Weg ist weniger fixiert als die "gewöhnliche" Denkweise. 
Im Kern bleiben Menschen das wichtigste Element sowie ihre Fähigkeit zu ständiger Innovation.

Das bedeutet, dass die klassische Art Software zu entwickeln eigentlich recht ungeeignet ist.

> "... Was mich aber faszinierte, war, zu sehen, dass ein simpler Pick-and-Place-Roboter diese Aufgabe übernehmen konnte. Toyota 
> hatte ihn als kostengünstige Alternative entworfen und gebaut. Der Roboter entnahm die fertigen Teile mit einer »Hand« und 
> bestückte mit der anderen die nächste Maschine. — ..." 
>
> location: [4143](kindle://book?action=open&asin=B094S6WY3F&location=4143) 
> ^ref-36035
> 
> Das besondere an diesem Roboter ist, dass er eine ganz einfache Funktion erfüllt, die sich bei allen möglichen Änderungen am 
> Prozessablauf überall wieder einsetzen lässt. Das entspricht der Unix-Philosophie:
> 
> The Unix philosophy was captured by Doug McIlroy, one of the original Unix developers, in the following:
> 
> - Make each program do one thing well. To do a new job, build afresh rather than complicate old programs by adding new "features".
> 
> - Expect the output of every program to become the input to another, as yet unknown, program. Don't clutter output with extraneous information. Avoid stringently columnar or binary input formats. Don't insist on interactive input.
> 
> - Design and build software, even operating systems, to be tried early, ideally within weeks. Don't hesitate to throw away the clumsy parts and rebuild them.
> 
> - Use tools in preference to unskilled help to lighten a programming task, even if you have to detour to build the tools and expect to throw some of them out after you've finished using them.
>
> [Jeffrey K. Liker-Der Toyota Weg]

Bei der Prüfung der Clean Code Craver-Ziele stolperten wir über einen Gedanken: Was ist, wenn das Entwickeln von eigenen Tools zu viel Zeit in Anspruch nimmt. 

Dann sollten wir uns gut überlegen, wann wir in was für ein Tool investieren. 

Dieses Repository soll mit der Situation experimentieren. Die Idee ist es UIs eher zu sehen, wie den Roboter in dem Buch. Das bedeutet sehr kleine aber in sich schlüssige Tools die einen kombinierbaren Funktionsbereich ausmachen.

Vielleicht könnte man das als Grundlage für schnelle Support-Oberflächen o.ä. nutzen.

## Ausgangssituation

- Letzte Zeitmessungen zeigen, dass der Support-Aufwand in der Abteilung erneut gestiegen ist, ohne dass ausreichend Eindämmungsinnovation geleistet wurde.
- Die Folge ist noch weniger Zeit für Innovation. Ist also eine Abwärtsspirale.
- Tool-Entwicklung nimmt viel Zeit in Anspruch, wenn man es wie bisher als Entwicklung komplett neuer Software angeht.
	  
## Zielsituation

- Es gibt eine Reihe von Standard-Tools die sich sehr einfach konfigurieren und in Kombination schalten lassen, so dass statt Support-Werkzeuge zu entwickeln, wir sie in wirklichkeit kombinieren.

- Um den Erfolg zu messen müssten wir die Zeit, die es dauert die Tools zu entwickeln plus die Kombinationszeit über eine Testmenge erfassen.

- Ziel ist es ein Werkzeug z.B. für die Verwaltung von Zeiterfassungsdaten für die Abteilung innerhalb von 10 Minuten zusammenbasteln zu können.

## Ursachenanalyse

- Die Entwicklung von Tools dauert zu lange.
1. Warum?
- Wir beginnen die Entwicklung von Tools immer bei 0 und starten mit der "gewöhnlichen Anwendung der Programmiersprachen".
2. Warum?
- Wir denken wir schreiben Software, und nicht Funktionsabschnitte.
3. Warum?
- Wir planen nicht genug.
4. Warum?
- Bis vor einiger Zeit hatten wir noch nicht so viel Einblick in Planungsmethoden.
- Wir haben uns die Zeit für die Planung nicht genommen.
- Wir haben bei der Planung nicht auf größere wiederverwendbare Teilbereiche geachtet, die man mit etwas Konfiguration ausbauen könnte.
5. Warum?
- Uns war die Art der Automatisierung nicht präsent.
  
## Problemlösung / Gegenmaßnahmen / Maßnahmenplan

- [ ] Experiment mit Pipelines: Produktionslinie nachstellen mit Powershell (Kombinierbarkeit)
- [ ] Experiment Bessere "CRUD"-UI für Powershell
  - [ ] Experiment: Kann man eine bessere Tabellenanzeige für Powershell bauen, als "Out-GridView"?
  - [ ] Experiment: Kann man eine Record-Eingabe für Powershell bauen?

## Erfolgsmessung

- Die Zusammenstellung einer UI zur Erfassung von Zeiterfassungsdaten für die Abteilung (1 Benutzer, n Zeitarten, Eingabe eines Tagesberichtes mit Zeitabschnittsanzahlen pro Zeitart, Abrufmöglichkeit, Änderbarkeit, lokale Datenablage) dauert unter 10 Minuten.

## Standardisierung und Know-How-Transfer

- Wie verankern wir die Lösungen in unserer täglichen Arbeitsweise?
