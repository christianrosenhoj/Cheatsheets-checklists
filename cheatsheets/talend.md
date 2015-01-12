#Talend

## Standaardverloop en opmerkingen 

- Altijd componenten instellen
- !! Opletten voor headers als je doc's inleest !! (zet 0 op 1 om eerste rij in te lezen als titels)
- Altijd schema aanpassen/controleren
- Altijd main toevoegen
- Runnen

## Extra's

- Bij tmap (editor) altijd slepen en dan tmap settings om type van joins te wijzigen
- Variabelen maak je in de contexts tab
- Als je je job build run dan altijd via `bash naam.sh` (anders soms permissie problemen)
- Voor parameters mee te geven run je `bash naam.sh --contect_param input==other`
- Voor schedule tasks run je `crontab -e` en je vult (in vim) in volgens formaat `1 2 3 4 5 /path/ args` waarbij de cijfers `min hours days month dayoftheweek` voorstellen


## Lijst die we gebruikt hebben in de oefening

| Type								| Betekenis
| :---                  			| :---
| tFileInputDelimited				|importeren van txt,csv,...
| tLogRow							|simple output per rij
| tFileInputJSON					|JSON file lezen
| tFileOutputJSON					|JSON wegschrijven
| tSQLiteOutput						|Wegschrijven naar sqlite db
| tFileInputExcel					|importeren excel
| tMap								|grouperen, mappen
| tJavaRow							|java code toepassen op rows
| tJavaFlex							|java met (start, main, end)
| tJava								|Java (runt maar 1 keer)
| metadata>excel (slepen)			|excel file gebruiken
| sqlite3 vbdatabank.db				|maken van vbdatabank.db
| .exit								|sqlite3 sluiten

