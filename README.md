## Fråga 1

Versionshantering betyder att man sparar olika versioner av sina filer under arbetets gång (frysta ögonblicksbilder), och inte bara "sparar över" (uppdaterar) filen/filerna gång på gång, vilket är fallet när du bara sparar via sparafunktionen i editorn. När du använder versionshantering så kan du alltså se vilka ändringar som gjorts, se ve,m som gjort ändringarna och när, gå tillbaks till en tidigare version, tex om något blivit fel, jämföra olika versioner med git diff...

## Fråga 2

Git status visar vilka filer som ändrats sedan senaste commit, dessa ändringar finns ännu bara på arbetsytan, dvs i din editor. När du sedan använder git add så väljer du vilka ändringar som skall skickas till nästa commit, du "lägger dem i kuvertet", staging alltså. Git commit i sin tur sparar, det som ligger i staging som en permanent punkt i historiken, vilken du kan gå tillbaka till vid ett senare tillfälle (se Fråga 1).
Om du ändrar i en fil oc kör git commit direkt utan att först kört git add så protesterar git, eftersom ändringen ännu bara finns på arbetsytan, och du inte med git add talat om vilka ändringar som skall tas med.

## Fråga 3

Mappen på den egna datorn är din lokala arbetsplats, det är här du skriver och ändrar i koden, Git lagrar också dina commits i projektets lokala historik. Repot på GitHub är en kopia av projektet som finns online, fungrrar som en plats där du kan lagra o dela projektet med andra. Git push skickar dina lokala commits till GitHub.
"Lådan hemma på datorn" är helt enkelt ditt lokala repo (som även är tillgängligt offline), där du arbetar med dina filer (se fråga 2), medans "glasmontern" är repot på GitHub, projektets onlineversion, där andra kan se och hämta de commits du pushat dit, Det funkar också som en samarbetsplats och en säkerhetskopia.
Om du försöker köra git push innan du stagat och commitat, så finns det inget att skicka eftersom ditt lokala repo och gitrepot båda har samma version av filen ifråga, du måste alltså köra git add och git commit först, så att ditt lokala repo inehåller den uppdaterade versionen - då funkar git push.
