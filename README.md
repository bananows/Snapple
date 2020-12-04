<h1>Snapple</h1>
Projekt von Samed und Bjarne
Informatik 12bc
Herr Buhl



<h2>Inhaltsverzeichnis</h2> 

Spielprinzip

Snap!

<h2>Programmierung</h2>

<h2 id="spielprinzip">Spielprinzip</h2>
Unser Spiel Snapple ist ein Snakespiel. Das Ziel des Spiels ist es hierbei, eine möglichst lange Schlange zu werden und somit einen möglichst hohen Score zu erreichen. Um dies zu erreichen, muss unsere Schlange Äpfel einsammeln, welche bei unserem Spiel das Gesicht einer fiktiven Apfelfigur aus einem etwas älteren Youtube-Video haben. Die Schlange darf hierbei nicht sich selbst oder den Rand des Spielfeldes berühren. Falls dies doch passieren sollte, wird der Score wieder auf 0 gesetzt und man muss von vorne anfangen. Um unser Spiel etwas zeitgerechter zu gestalten, haben wir uns dafür entschieden, aktuelle Meme-Figuren mit in unser Projekt einzubauen. So haben wir zum Beispiel im Startscreen und im Endscreen ein Pepe-Emote eingebaut, welcher seinen Ursprung auf der Gaminglivestream-Plattform Twitch hat. Diese gibt es in verschiedensten Stilen, um sich mit anderen Menschen auch ohne Wörter verständigen zu können.

Snap!
Snap! ist eine auf kindertaugliche Programmiersprachen aufbauende erziehungsorientierte Programmiersprache. Sie ist für fortgeschrittenere Schüler und auch für durchaus erfahrene Erwachsene geeignet. Sie wurde von der Universität Berkley 2011 veröffentlicht. Zu den Entwicklern gehören Jens Möning und Brian Harvey. Snap! ist kompatibel mit Windows, macOS und Linux. Die Programmiersprache ist in 20 verschiedene Sprachen übersetzt und frei im Browser verfügbar.

Programmierung

Grundbewegung

<p align="center"><img src="https://github.com/bananows/Snapple/blob/master/Projektseite%20Images/Grundbewegung.png" width="600px">

Die linken Blöcke geben die Richtung mithilfe der Pfeiltasten an, in der sich die Schlange bewegen soll. Zudem geben wir mit den "if not"- Befehlen an, dass sich die Schlange auf der Stelle nicht um 180° drehen und somit in sich selbst reinbewegen kann.
Der "move 15 steps"-Befehl in dem rechten großen Block gibt an, dass sobald [space] gedrückt wurde und das Spiel somit gestartet wurde die Schlange sich zu jeder Zeit um 15 Schritte bewegt.

Spritefunktion

<p align="center"><img src="https://github.com/bananows/Snapple/blob/master/Projektseite%20Images/Sprite%20funktion.png" width="600px">
  
  Dieser Block dient dazu, dass wenn wir {space] drücken, die "trail"-Variable zur Liste hinzugefügt wird. Außerdem wird der Score auf 0 gesetzt und oben links während des Spiels angezeigt. Der "clear"-Befehl löscht alle Zeichnungen der vorherigen Runde. Anschließend werden alle laufenden Schleifen von davor ebensfalls beendet und auch andere Zeichnungen entfernt. Danach wird die Größe unserer Schlange definiert und es wird ein Startpunkt und eine Startrichtung festgesetzt. Der Befehl danach gibt an, dass die x- und y- Positionen der Schlange in die Liste gesetzt werden. Anschließend wird anhand der Liste gestempelt und die Schlange sozusagen angezeigt. Danach werden der "Eraser" und der "Apfel" in Funktion gerufen. Die "forever"-Schleife gibt an, dass wenn der Rand berührt wird oder die Schlange sich selbst berührt, das Spiel gestoppt wird bzw. der Endscreen erscheint. Außerdem wird angegeben, dass sobald ein Apfel von der Schlange berührt wird, ein Listeneintrag, also ein Block, zur Schlange hinzugefügt wird und dass der Score sich um +1 verändert.
  
  Eraser
  
  <p align="center"><img src="https://github.com/bananows/Snapple/blob/master/Images/Eraser.png" width="600px">
  
  Der Eraser ist der "Überstempler" unserer Schlange. Die Blockeinheiten unserer Schlange werden nicht gelöscht, sondern weiß überstempelt. Dies passiert, indem wir vorher einen "Eraser" zeichnen und ihm eine bestimmte rechteckige Form und eine weiße Farbe geben. Der Eraser ruft immer die letzten Listeneintrag ab und überstempelt diesen, indem er diesen mit seiner Position abgleicht und mit sich selbst ersetzt. Die Größe des Erasers gleicht der Größe eines Blocks unserer Schlange, damit präzise und genau überstempelt werden kann.
  
  Apfel
  
  <p align="center"><img src="https://github.com/bananows/Snapple/blob/master/Images/Apfel.png" width="600px">
  
  Unser zuvor bereits erwähnter Apfel wird mit dem oberen Block, sobald [space] gedrückt wird, an eine bestimmte Startkoordinate positioniert, damit der Apfel nicht zufällig in unserer Schlange spawnt. Der untere Block gibt die Größe unseres Apfels an sorgt dafür, dass dieser an einer zufälligen Postition spawnt, sobald er von der Schlange berührt und aus deren Code gebroadcastet wird. 
  
  Blinkende Schrift
  
  <p align="center"><img src="https://github.com/bananows/Snapple/blob/master/Images/Blinkende%20Schrift.png" width="600px">
  
  Bei unserem Endscreen soll der Schriftzug "Drücke [space] für Neustart" blinken, da es unserer Meinung nach anschaulicher ist und eine gewisse Dynamik mitbringt. Das funktioniert mithilfe einer Variable. Diese wird, wenn der Endscreen gebroadcastet wird, auf falsch gesetzt und dadurch das Blinken ausgelöst. Dieses wird solange wiederholt bis die Variable durch einen Druck auf [space] auf true gesetzt wird und die Schleife, die das Blinken verursacht, beendet wird. Das Blinken passert immer in 1er Sekunde Schritten. Dies passiert im unteren Block. 
Im oberen Block geben wir an, dass wenn [space] gedrückt wird, der Schriftzug sich hidet, also verschwindet. 
  
  
  
 
  
  






