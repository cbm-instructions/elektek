# Elektronik:
![Elektronik](https://user-images.githubusercontent.com/65849767/216325939-515f0abe-9433-4203-af4c-b0fb4cb4a53c.png)

## Bestandteile:
-A1: Arduino Uno
-M1: Gleichstrommotor
-Z1: Spannungsregler
-K1, K2: Kondensator
-L2: NeoPixel Ring 24 LED
-L1: NeoPixel Ring 16 LED
-L3: NeoPixel Ring 12 LED
-S1, S2, S3, S4: Kippschalter


## Funktion + Aufbau:
Wird der Motor in die richtige Richtung gedreht, bekommen wir eine positive Spannung, diese leiten wir von dem Motor auf die Platine mit Hilfe 2 Kabeln. Auf der Platine wird durch einen Kondensator die elektrische Ladung gespeichert, dadurch verlangsamen wir das Abfallen der elektrischen Ladung, sobald der Motor nicht mehr gedreht wird. Als Nächstes sorgt ein Spannungsregler dafür, dass die Spannung stabilisiert wird.  Durch das Stabilisieren pendelt die Spannung in dem Bereich von 4,8 bis 5,2 Volt, mit dem Typ Spannungsregler, den wir benutzt haben. Als Letztes auf der Platine sitzt ein weiterer Kondensator, der wieder die elektrische Ladung speichert und somit erreichen wir ein schönes Abfallen der Spannung, anstatt dass diese sofort auf 0 runterfällt. Von der Platine aus gehen wir mit der Plus-Seite aus auf einen analogen Input auf dem Arduino Uno Board und mit der Minus-Seite gehen wir zuerst einmal in eine Mehrfachklemme. Im Arduino wird nun ein Wert anhand der elektrischen Ladung erstellt, welchen wir auslesen und speichern. Diesen Wert benutzen wir in unterschiedlichen Formeln, um somit die Spannung, den Kalorienverbrauch und das Gramm CO2 zu ermitteln. Diese werden anhand der Lampen der NeoPixel LEDs sichtbar gemacht. An den 5 Volt Ausgang des Arduinos stecken wir ein Kabel, welches zum Haupt-Kippschalter führt. Von diesem geht es an die 3 separaten Kippschalter und von ihnen aus geht es an den Power Anschluss der NeoPixels. Der Haupt-Kippschalter sorgt dafür, dass alle LEDs keine Spannung mehr haben und ausgehen, wobei die 3 separaten Kippschalter jeweils für einen LED-Ring sorgen. Durch diese Funktion kann man bestimmen, ob einen die Werte einer bestimmten LED Ring nicht interessiert und man diesen nicht angezeigt bekommen möchte. Ein weiterer Anschluss der NeoPixels ist der digitale Input, diese schließen wir an die digitalen Anschlüsse des Arduinos. In unserem Fall sind es die Anschlüsse 3, 4 und 5. Durch diese können wir bestimmen, welchen LED Ring wir mit dem Arduino genau ansteuern möchten. Der letzte Anschluss der LED ́s ist der Ground diese stecken wir in die Mehrfachklemme, in der schon der Ground des Motors steckt. Zum Schluss muss nur noch die Mehrfachklemme mit den Grounds, mit einem Arduino Ground Anschluss angeschlossen werden, durch ein zusätzliches Kabel.
