# TimeBox - Girl's Day 2023

Zum Girl's Day 2023 programmieren und basteln wir unsere eigene Uhr - aus einer Holzbox,
dem Mikrocontroller ESP32 und einem (NeoPixel-)Ring mit 12 LEDs!

## Verkabeln
Der NeoPixel hat 3 Kontakte, die bereits verlötet sind: VCC, GND und IN.
Diese Steckbrücken müssen auf VCC -> 5V, GNC -> GND und IN auf euren ausgewählten GPIO (zB PIN #16) des ESPs gesteckt werden.

## Vorbereitungen
- Um den Mikrocontroller zu programmieren benötigen wir eine Entwicklungsumgebung und
  müssen diese zuerst installieren. Wir nutzen [Thonny](https://thonny.org/).
  Auf der Thonny-Webseite findet ihr unter <i><Instructions & downloads></i> Informationen zur Installation.
- Wenn nicht bereits geschehen, muss der Mikrocontroller lernen, dass wir mit der Programmiersprache
  [MicroPython](https://micropython.org) arbeiten wollen.
  Dazu müssen wir die MicroPython installieren.
  - Gehe dazu in Werkzeuge->Optionen...->Interpreter (Raspi: Extras->Optionen...->Interpreter) und klicke unten rechts auf
  MicroPython installieren oder aktualisieren. Ein Thonny-Neustart ist nach der Installation (des esptool) notwendig ;-)
  -  Anschließend nochmals zu Interpreter navigieren, wähle den richtigen Port aus und lade die Firmware (entweder von der [MicroPython-Seite](https://micropython.org/download/esp32) oder aus diesem Repo)
  mit dem Button installieren hoch.
  (Tipp Raspi: falls sich das esptool nicht installieren lässt, kannst du alternativ in einem Terminal per <i> pip3 install esptool </i> dieses manuell installieren)


## Programm dauerhaft hochladen
Um deine TimeBox auch wirklich als Uhr zu nutzen möchtest du sie sicher nicht immer am Laptop angesteckt lassen.
Das ist natürlich kein Problem! Der ESP führt den Code auch ohne Thonny aus. Dazu muss aber all der benötigte Code
in einer gewissen Art hochgeladen werden und Hauptdatei muss main.py heißen!

- Wechsle zuerst in der Leiste links in den Ordner *timebox*, klicke dort mit der rechten Maustaste auf *lib* und wähle -> Upload to /
- Mache das gleiche nochmals für die Datei *main.py*
- Drücke auf deinem ESP32 Mikrocontroller den Button EN, um das Programm unabhängig von Thonny zu starten


## Link-Sammlung
- Python-Kurs -> https://www.w3schools.com/python/default.asp
- ESP-Tool Installation
  - https://randomnerdtutorials.com/flashing-micropython-firmware-esptool-py-esp32-esp8266/
- Thonny Installation
  - https://randomnerdtutorials.com/getting-started-thonny-micropython-python-ide-esp32-esp8266/#install-thonny-ide-linux
