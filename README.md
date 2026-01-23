# Lernperiode 8

Ich wollte ein eigenes Spiel programmieren, mit dem man richtig interagieren und es auch tatsächlich spielen kann. Dafür habe ich mir verschiedene Plattformen angeschaut (z. B. Phaser.js oder MonoGame). Schlussendlich habe ich mich dazu entschieden, mein Spiel mit **Godot** zu erstellen. Ich finde, dass dies die geeignetste Engine für mich ist, da sie mich persönlich sehr fasziniert hat. Godot ist eine einfache, aber dennoch leistungsfähige und gut strukturierte Entwicklungsumgebung. In der es ein einfaches Tutorial habe. 

In dieser Lernperiode möchte ich ein **Jump-and-Run-Spiel** umsetzen. Als Einstieg habe ich zwei Tutorials angeschaut, die mir die Grundlagen von Godot erklärt haben, insbesondere Szenen und Nodes.

[➡️ Tutorial](https://www.youtube.com/watch?Tutorialv=qYiDF6ldbu8&list=PL_pqkvxZ6ho0nVXxQCdND2cbWSVAX2nhs&index=2)

[➡️ Tutorial](https://www.youtube.com/watch?v=R5fXm3vCJAw&list=PL_pqkvxZ6ho0nVXxQCdND2cbWSVAX2nhs&index=3)

Mithilfe dieser Tutorials habe ich anschliessend ein erstes **Hello-World-Projekt** erstellt:

<img width="1916" height="1106" alt="image" src="https://github.com/user-attachments/assets/6d06f723-63df-4319-9719-30353dc74ef6" />

Nach diesen Tutorials habe ich festgestellt, dass der YouTuber kein vollständiges Spiel erstellt, sondern hauptsächlich die Grundlagen erklärt. Deshalb habe ich mir ein weiteres Tutorial gesucht und dieses gefunden:

[➡️ Tutorial](https://www.youtube.com/watch?v=WRDl2gQObg8&list=PL1td_Fr5vMGOW0hasVEYlvfdm_oYh0xi9&index=1)

Ich habe mit dem ersten Teil dieses Tutorials begonnen, bin jedoch noch nicht ganz fertig geworden.

## 16.01

- [x] Spieler hinzufügen  
- [x] Spielerlogik für Vorwärts- und Rückwärtsbewegung programmieren  
- [ ] Spieler springen lassen  
- [ ] Umgebung hinzufügen  

Heute habe ich viel umgesetzt. Ich habe den Spieler, der im Tutorial zur Verfügung gestellt wurde, eingebunden und ihn als **CharacterBody2D** hinzugefügt. An den CharacterBody2D habe ich ein **CollisionShape2D** angehängt sowie eine erste Codelogik implementiert, um den Charakter vorwärts und rückwärts bewegen zu können. Zusätzlich habe ich Gravitation hinzugefügt, sodass der Spieler nach unten fällt. Das Springen sowie die Umgebung habe ich jedoch noch nicht umgesetzt.

## 23.01

- [x] Spieler springen lassen  
- [x] Umgebung hinzufügen  
- [x] Ersten Jump einbauen  
- [x] Logik implementieren, sodass der Spieler beim Herunterfallen wieder bei der Position `0 | 0` spawnt  

Heute habe ich wichtige Grundlagen für mein Jump-and-Run-Spiel umgesetzt. Ich habe die Umgebung mit einer TileMap aufgebaut und eigene Blöcke erstellt, bei denen der Boden korrekt mit Kollisionen versehen ist. Zusätzlich habe ich die Spielerbewegung erweitert, sodass der Charakter sich nach links und rechts bewegen sowie springen kann. Die Gravitation funktioniert nun korrekt, wodurch der Spieler realistisch nach unten fällt. Falls der Spieler neben die Plattform springt und herunterfällt, wird er automatisch an die Startposition zurückgesetzt. Zudem habe ich eine Camera2D eingebunden, damit sich die Szene beim Laufen mit dem Spieler mitbewegt.

## 13.02

- [ ] Hintergrund einfügen
- [ ] Ziellinie einfügen
