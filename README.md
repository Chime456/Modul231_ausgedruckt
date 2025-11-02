**Datentypen**
boolean, ganzzahlen (-5, 0, 42)
Dezimalzahlen(genaue Nachkommastellen)
Datum/Zeit
Gleitkommazahlen
Zeichenkette(String)
Objekt/Record ({Name:"", etc.})
Character(Char, 'A', '7')
Binärdaten(Bilder)
Null


**Struktur**
Array, Datensatz, Verketteliste, Stapelspeicher, Warteschlange, Vorrangwarteschlange, Graph, Baum, Heap, Hashtabelle


**ERM-Grundlagen**
- ENtität: Ein **Objekt** der gespeichert wird
- Attribut: **Eigenschaft** der Entität (Kategorieren der Entität)
- Beziehung: **verknüpfung** zwischen entitäten
- Kardinalität: Anzahl beteiligter | 1:1, 1:n, n:m
- PK: **eindeutige ID** einer Entität
- FK: Attribut in einer Entität, dass auf den PK einer anderen Entität **verweist**


**Redundanz**
- dopppelte einträge, mehrfach gleiche information erscheinen
- wiederholte attributen, unterschiedliche schreibweise oder werte
- speicherplatzverschwendung, änderung an einer stelle werden nicht automatisch übernommen


**Modellierung**

<img width="600" height="200" alt="image" src="https://github.com/user-attachments/assets/198b9fe2-c7e5-48c9-88d9-3ce648bee783" />


**logisches ERD**

was: ID, Attributen und FK


**physisches ERD**

was: kardinalitäten, FKs integrität
<img width="800" height="600" alt="image" src="https://github.com/user-attachments/assets/361c241d-05db-4399-9c56-8f13c7455a6f" />


**Normalformen**

1NF: Keine mehrfachen Werte, atomar -> so klein wie möglich trennen/ordnen, Spalten aufteilen

2NF: logische Gruppe, Tabellen nach Entitäten trennen, Ein Relationstyp (Tabelle) befindet sich genau dann in der zweiten Normalform (2NF), wenn er sich in der ersten Normalform (1NF) befindet und jedes Nichtschlüsselattribut von jedem Schlüsselkandidaten voll funktional abhängig ist.  
<img width="600" height="400" alt="image" src="https://github.com/user-attachments/assets/db354428-8129-4277-87f2-999a43a4a7c7" />

3NF: keine transitive Abhängigkeit (nochmal gruppieren), Attribute logisch weiter aufteilen, Ein Relationstyp befindet sich genau dann in der dritten Normalform (3NF), wenn er sich in der zweiten Normalform (2NF) befindet und kein Nichtschlüsselattribut transitiv von einem Kandidatenschlüssel abhängt.  
<img width="600" height="300" alt="image" src="https://github.com/user-attachments/assets/3f99e9ae-d720-4c4d-98a8-6e98fb39463c" />
