# Das Lage-Programm - ein multifunktionales Programm der linearen Algebra und Vektorrechnung auf dem TI nspire CAS

Bitte benutzt das Programm nur im Rahmen der MIT-Lizenz. Jede wirtschaftliche Nutzung des Programms ist ausdrücklich untersagt. Ich hafte NICHT für falsche Ergebnisse, die Nutzung ist auf eigene Gefahr (aber bisher sind bei mir in einem Jahr Nutzung alle Ergebnisse richtig gewesen). Bitte achtet auch darauf, dass in Arbeiten meist Lösungsansätze oder Rechenwege gefordert werden und das reine Ergebnis oft keine volle Punktzahl gibt. Nutzt das Programm am besten zum Überprüfen der eigenen Lösungen oder in Übungen.

# Allgemeines

Das Programm verfolgt die Idee eines Programmes für den TI nspire CAS, mit welchem man schnell Lagebeziehungen zwischen Punkten, Ebenen und Geraden in der linearen Algebra ermitteln kann. Dabei ist es nur notwendig die verschiedenen Elemente in das Programm einzugeben, um verschiedene Informationen zur Lage dieser zu erhalten. Das Lageprogramm benötigt als Eingaben immer 2 mit einem echten Komma getrennte Argumente. Also Lage(Argument1,Argument2)

Zum Lageprogramm zugehörig ist ein Dokument Hilfsprogramme. Ohne dieses funktioniert das Lageprogramm nicht! 

# Möglichkeiten

Hier sind alle möglichen Beziehungen, die das Lageprogramm verarbeiten kann:

Punkt-Punkt   
Punkt-Gerade  
Gerade-Gerade   
Gerade-Ebene  
Ebene-Ebene 

Dabei ist egal, welches Element zuerst eingeben werden muss. Das heißt, dass es egal ist, ob man beispielsweise zuerst die Gerade und dann die Ebene eingibt oder anders herum.

Für die Ebenen gibt es drei verschiedene Varianten, diese wären:

Normalenform und Hessesche Normalenform   
Parameterform   
Parameterfreie Form / Koordinatenform   

Die verschiedenen Eingaben der Ebenenformen sind in den folgenden Abschnitten nachzulesen.

# Eingabe

Im Nachfolgenden sollen die Eingabe der verschiedenen Elemente gezeigt werden:

#  Punkt

Die Eingabe eines Punktes erfolgt einfach über dessen Ortsvektor. Das heißt, ein Punkt P(x/y/z) wird in das Lageprogramm mit [x;y;z] oder [x,y,z] eingegeben. Welche dieser beiden Eingabemöglichkeiten genutzt wird, ist dabei egal. Möchte man beispielsweise den Abstand und die resultierende Gerade aus den Punkten P(1/2/3) und T(3/1/8) ermitteln, sieht die Eingabe wie folgt aus:

Lage([1,2,3],[3,1,8])

Die Ausgabe des Programmes sieht dann so aus:

![TR_Punkte](https://github.com/Tom-Haustein/TI-nspire-Programm/blob/main/Bilder/TR_Punkte.JPG)

Zwischen einem Punkt und einer Geraden oder einer Ebene kann der Abstand ermittelt werden.

# Geraden

Geraden bestehen grundsätzlich aus Stützvektor, Parameter und Richtungvektor in der Form:

Die Eingabe des Stützvektors erfolgt ähnlich dem eines Punktes. Dazu wird ein Parameter mal den Richtungsvektor addiert. 
DABEI BESTEHT FREIE AUSWAHL DER VARIABLE DES PARAMETERS. Das heißt das alle Variablen von a bis z können als Paramtername genutzt werden. Gleiches gilt im übrigen für die Ebene in Parameterform. So entspricht beispielsweise die Gerade [1,2,5]+r*[2,6,1] exakt der Geraden [1,2,5]+s*[2,6,1] oder [1,2,5]+t*[2,6,1] (bei einer Geraden mit Stützvektor [1,2,5] und Richtungsvektor [2,6,1]). 
Eine mögliche Eingabe für die Lage zwischen zwei Geraden könnte also so aussehen:

Lage([1,2,4]+r[3,1,5],[3,1,9]+t*[2,5,1])

Die Ausgabe des Programmes sieht dann so aus:

![TR_Geraden](https://github.com/Tom-Haustein/TI-nspire-Programm/blob/main/Bilder/TR_Geraden.JPG)

Diese Art der Eingabe ist die einzige Möglichkeit der Eingabe für eine Gerade. So werden beispielsweise Geraden in Normalenform nicht vom Programm angenommen.

# Ebenen

Wie oben bereits erwähnt, gibt es drei mögliche Ebenenformen. Diese werde ich nun nacheinander durchgehen.

Parameterform
-
Eine Ebene in Parameterform besteht aus Stützvektor und 2 Spannvektoren, die jeweils mit einem eigenen Parameter multipliziert werden. Hier sieht man noch einmal, wie eine Ebene in Parameterform aussieht:

![Parameterform_Beispiel](https://github.com/Tom-Haustein/TI-nspire-Programm/blob/main/Bilder/Parameterform_Beispiel.png)

Die Eingabe ist sehr ähnlich, der einer Geraden, nur zusätzlich mit einem weiteren Spannvektor und dem dazugehörigen Parameter. Dementsprechend sieht die Eingabe an einem Beispiel wie folgt aus:

[2,1,4]+r*[6,4,3]+t*[9,1,4]

Auch hierbei besteht frei Parameterwahl, allerdings dürfen die Parameter von Spannvektor1 und Spannvektor2 nicht identisch sein. Das heißt folgende Ebene wäre NICHT gültig und würde zu einer Fehlermeldung führen:

[2,1,4]+r*[6,4,3]+r*[9,1,4]

Koordinatenform bzw. parameterfreie Form
-
Eine Ebene in Koordinatenform hat die Form a*x+b*y+c*z=d.* Genau diese Form kann auch so in das Lageprogramm eingegeben werden. Am Beispiel der Ebene 3x+7y-2z=10 und dem Punkt P(2/4/1) sieht die Eingabe dann wie folgt aus:

Lage([2,4,1],3x+7y-2z=10)

Das Ergebnis des Programmes sieht dann wie folgt aus:

![TR_Koordinatenebene](https://github.com/Tom-Haustein/TI-nspire-Programm/blob/main/Bilder/TR_Koordinatenebene.JPG)

Diese Form der Eingabe ist vermutlich die einfachste. Für den Fall, dass der Wert vor dem X-Wert gleich null oder einem der anderen Werte, so ist es egal, ob man die 0 mit dem X multipliziert oder diesen gleich ganz weglässt. Es gehen also 0*x+3*y+5*z=10* oder auch 3*y+5*z=10 als Eingabe. Somit geht auch z=0 als Ebenenform.

Normalenform
-
Die Normalenform einer Ebene besteht aus einem Stützvektor und einem Normalenvektor. Diese sieht wie folgt aus:

![Normalenform_allgemein](https://github.com/Tom-Haustein/TI-nspire-Programm/blob/main/Bilder/Normalenform_allgemein.jpg)

([p1,p1,p3] beschreibt den Stützvektor und [n1,n2,n3] den Normalenvektor, die skalarmultipliziert werden. Wird nun ein Punkt [x1,x2,x3] in die Gleichung eingesetzt und dieser erfüllt die Gleichung, so liegt er in der Ebene. Falls die Gleichung einen Widerspruch, beispielsweise 3=0, ergibt, so liegt er eingesetzte Punkt nicht in der Ebene)

In diesem Fall ist die Eingabe in das Lageprogramm allerdings nicht so einfach, da der Taschenrechner ohne ein eigenes Programm (dotP) kein Skalarprodukt rechnen kann. Deshalb musste ich mir hier etwas anderes überlegen.

Für die Eingabe einer Ebene in Normalenform muss als Argument in das Lageprogramm nf, was für Normalenform steht, eingegeben werden. Sobald nf eingegeben wurde, wird der Stütz- und Richtungsvektor abgefragt. Die Eingabe einer Normalenform sieht dann beispielsweise so aus, für die Lagebeziehung zwischen dieser Ebene und einer Gerade so aussieht:

Lage(nf,[1,2,3]+r*[4,5,6])

Ob das nf dabei an erster oder zweiter Stelle steht, ist dabei egal.
Die Antwort des Programmes auf die Eingabe sieht dann wie folgt aus:

![Abfrage_stützvektor](https://github.com/Tom-Haustein/TI-nspire-Programm/blob/main/Bilder/Abfrage_st%C3%BCtzvektor.JPG)

Unsere Ebene in Normalenform sieht nun beispielsweise so aus:

![Normalenform_beispiel](https://github.com/Tom-Haustein/TI-nspire-Programm/blob/main/Bilder/Normalenform_Beispiel.png)

Das heißt unser Stützvektor ist [3,1,-1] und der Normalenvektor [0,3,2]. Auf die Abfrage des Stützvektors wird also nun folgendes eingegeben:

![Stützvektor_Eingabe](https://github.com/Tom-Haustein/TI-nspire-Programm/blob/main/Bilder/St%C3%BCtzvektor_Eingabe.JPG)

Und auf die Abfrage des Normalenvektors wird nun aufgrund unseres Normalenvektors folgendes eingegeben:

![Normalenvektor_Eingabe](https://github.com/Tom-Haustein/TI-nspire-Programm/blob/main/Bilder/Normalvektor_Eingabe.JPG)

Und die Ausgabe des Programmes für unsere Lagebeziehung zwischen der Ebene in Normalenform und dem Punkt P ist:

![TR_Koordinatenebene](https://github.com/Tom-Haustein/TI-nspire-Programm/blob/main/Bilder/TR_Normalenebene.JPG)

Somit sind nun alle Eingabemöglichkeiten des Lageprogramms erklärt. Das Lageprogramm besitzt folgende Ausgaben in Abhängigkeit der eingegeben der möglichen Beziehungen:

Abstand   
Gerade zwischen zwei Punkten    
Schnittpunkt zweier Geraden   
Parallelität oder Windschiefe von Geraden zueinander    
Schnittwinkel zweier Geraden    
Schnittgerade zweier Ebenen   
Schnittwinkel zweier Ebenen   

# Funktionsweise
Dieser Teil beschäftigt sich nun nichtmehr mit der Eingabe sondern geht etwas auf die Funktionsweise ein. Allgemein umfasst das reine Lageprogramm rund 900 Programmzeilen. Das Dokument Hilfsprogramme umfasst noch einmal 4 Programme mit insgesamt fasst 800 Programmzeilen. 

Die Programme aus Hilfsprogramme beinhalten hauptsächlich Programme die Variablennamen aus Geraden oder Ebenen herausfinden. Im Lageprogramm selbst wird mehrmals auf diese Programme als Funktions verwiesen, sodass diese nicht mehrmals  in das Programm selbst kopiert werden müssen. Dadurch wird der Programmcode wesentlich kürzer und würde ansonsten mehrere Tausend Programmzeilen umfassen. 

Um den Programmcode des Lageprogramms einzusehen, muss das tns Dokument einfach in der CAS Software geöffnet werden. Um ehrlich zu sein, blicke ich im Programmcode selbst nicht mehr durch, da dieser so viele Möglichkeiten und Funktionen beinhaltet. Zudem habe ich mir das Programmieren in dieser Programmiersprache selbst beigebracht, weshalb der Code an vielen Stellen unstrukturiert und ineffektiv ist. Aber was soll man sagen, es funktioniert. 

Ich werde den Programmcode jetzt auch nicht noch einmal genau analysieren, da dies hier bei 900 Programmzeilen viel zu lang werden würde. 
Wer aber etwas an meinem Programmcode ändern möchte, sodass er effektiver und strukturierter bzw. neue Funktionen erhält, kann dies im Rahmen der MIT-Lizenz gerne tun. Ich würde mich darüber sehr freuen.

Ich hoffe das Programm hilft Einigen weiter ^^

