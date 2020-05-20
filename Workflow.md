
# Unser Workflow
1. [Vorbereitung](#Vorbereitung) 
2. Branches im remote upstream repository
3. [Workflow für die eigene Arbeit](#own_workflow)\
	3.1 [Anfang der Sitzung](#own_workflow:start)\
	3.2 [Branches für Bearbeitungen erstellen](#own_workflow:branches)\
	3.3 [Commits](#own_workflow:commits)\
	3.4 [Eigenes remotes repository aktualisieren](#own_workflow:push_origin)
4. [Pull request für remote upstream repository, master branch](pullrequest_upstream)
	

## 1. Vorbereitung (einmalig) <a name="Vorbereitung">
1. In github das Original repository forken
2. Das Repository vom eigenen github account clonen
3. Das Repository auf das original Repository bei github (remote upstream repository) zeigen lassen 

## 2. Branches im remote upstream repository <a name="branches_upstream">
Wir nutzen den **github workflow**: Wir arbeiten nur an einem Masterstrang mit branches. 
Wir überlegen uns bei einem laufenden System zum **git workflow** zu wechseln: Wir eröffnen einen zweiten Developmentstrang, wenn wir ein laufendes System haben.
Der Masterstrang spiegelt dann alles wieder was gerade läuft. Der Developmentstrang wird zur Entwicklung genutzt. Das heißt wir mergen neue features in diesen.
https://medium.com/@patrickporto/4-branching-workflows-for-git-30d0aaee7bf

## <a name="own_workflow"> 3. Workflow für die eigene Arbeit </a>
### <a name="own_workflow:start"> 3.1  Anfang der Sitzung </a>
Bevor wir an unseren eigenen Arbeitspakten arbeiten holen wir uns immer erst die aktuelle Version aus dem Originalrepository. Dafür gibt es zwei Möglichkeiten.

a) Unser Master repository soll durch das original master repository ersetzt werden.
pull x aus y

b) Unser Master repository soll mit dem original master repository gemerged werden. (Sinnvoll wenn wir an unserem eigenen Masterrepository Änderungen vorgenommen haben, die noch nicht ins Oririnal Master repository gepullt wurde)

### <a name="own_workflow:branches"> 3. 2. Branches für Bearbeitungen erstellen </a>
Wenn wir etwas verändern oder neu hinzufügen wollene rstellen wir ein branch in dem wir arbeiten. Die Bezeichnung sollte was darüber aussagen was wir machen. Wir können aus auch auf bestimmte Schlüsselwörter einigen z.B.
text_xxx - Überarbeitung des Textes in einem Dokument
code_xxx - Wir überarbeiten den Code bzgl: Effektivität, Lesbarkeit etc.
comment_xxx - bessere Kommentierung des Codes
feature_xxx - Erstellung eines neues features
bugfix_xxx - Die Veränderung an einem Code

### <a name="own_workflow:commits"> 3.3 Commits </a>
Wir versuchen unsere commits thematisch zu ordnen und commiten nicht alles was wir bearbeitet haben aufeinmal.
Arbeiten wir in einer Sitzung an einem neuen feature und seiner Beschreibung in einer extra Readme Datei laden wir erst das eine in die staging area und commiten und dann die andere Änderung in die Staging area.
Wir versuchen gute commit messages mit Schlagwörtern z.B. `text`, `code`, `comment`, `feature`, `bugfix`. Innerhalb eines feature branches können wir ja auch einen bugfix der uns aufgefallen ist bevor wir das feature in den master brunch des remote upstream repositorie gemerged haben.

### <a name="own_workflow:push_origin"> 3.4 Eigenes remotes repository aktualisieren</a>

## <a name="own_workflow:pullrequest_upstream">  4. Pull request für remote upstream repository, master branch </a>
Wenn wir eine Entwicklung, Bearbeitung abgeschlossen haben gehen wir in folgenden Schritten vor:

1. Wir aktualisieren unser eigenes Masterrepository (siehe Punkt 1)
2. Wir mergen dieses in den branch an dem wir gerade arbeiten um festzustellen ob es Konflikte gibt
3. Wir pushen den branch in unser eigenes repository, hier in den gleichen branch, nicht ins master repository
4. Wir erstellen einen Pull request und kommentieren diesen im remote upstream repository
5. Eine Person muss den Code reviewen erst dann kann der pullrequest erlaubt werden

## Offene Fragen ohne Vorschlag
* Wie gehen wir mit pullrequests und branches des owners um?


