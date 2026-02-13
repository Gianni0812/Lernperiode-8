---
title: Mein Tutorial
---

# Goal

In diesem Tutorial lernst du, wie man mit der Godot Engine ein einfaches 2D-Jump-and-Run-Spiel erstellt. Wir bauen Schritt für Schritt eine Spielfigur mit Bewegung, Gravitation und Sprungfunktion auf. Zusätzlich erstellen wir eine Umgebung mit einer TileMap, fügen Kollisionen hinzu und sorgen mit einer Camera2D dafür, dass die Szene dem Spieler folgt.

# Previous Knowledge

Für dieses Tutorial solltest du die grundlegende Bedienung von Godot kennen. Dazu gehört das Erstellen einer Szene, das Hinzufügen von Nodes (z. B. CharacterBody2D, Sprite2D, CollisionShape2D) sowie das Schreiben einfacher GDScript-Skripte. Grundkenntnisse in Programmierung wie Variablen, Funktionen und Bedingungen sind hilfreich.

# What you'll learn

In diesem Tutorial lernst du:

- Eine Spielfigur mit CharacterBody2D zu erstellen  
- Bewegung nach links und rechts umzusetzen  
- Gravitation und realistische Fallbewegung einzubauen  
- Eine Sprungfunktion mit is_on_floor() zu programmieren  
- Eine TileMap mit Blöcken und Kollisionen zu erstellen  
- Einen Respawn-Mechanismus bei Absturz zu programmieren  
- Eine Camera2D zu verwenden, damit die Szene dem Spieler folgt  

# Tutorial

Zuerst erstellen wir eine neue Szene und fügen einen CharacterBody2D als Spieler hinzu. Anschliessend hängen wir ein Sprite2D sowie ein CollisionShape2D an.

<img width="266" height="223" alt="image" src="https://github.com/user-attachments/assets/7a879df1-4c0f-4679-aca9-67d5cfb0fbd5" />


Danach implementieren wir die grundlegende Bewegung:

```gdscript
extends CharacterBody2D

const GRAVITY = 800
const SPEED = 200
const JUMP_FORCE = -350

func _physics_process(delta):
	if not is_on_floor():
		velocity.y += GRAVITY * delta

	velocity.x = 0
	if Input.is_action_pressed("left"):
		velocity.x = -SPEED
	elif Input.is_action_pressed("right"):
		velocity.x = SPEED

	if Input.is_action_just_pressed("jump") and is_on_floor():
		velocity.y = JUMP_FORCE

	move_and_slide()
```
Anschliessend erstellen wir eine TileMap, definieren ein TileSet und fügen für die Boden-Tiles Kollisionen hinzu. So bleibt der Spieler korrekt auf dem Boden stehen und fällt nicht durch.

Zusätzlich implementieren wir eine Respawn-Funktion, die den Spieler zurück zur Startposition setzt, wenn er von der Plattform herunterfällt.

Zum Schluss fügen wir eine Camera2D als Kind-Node des Spielers hinzu und aktivieren sie, damit sich die Szene beim Laufen mitbewegt.

# Result 

Am Ende dieses Tutorials hast du ein funktionierendes 2D-Jump-and-Run-Spiel mit:

- Spielerbewegung

- Springen

- Gravitation

- Kollision mit der Umgebung

- Respawn-System

- Scrollender Kamera

Die grundlegende Spielmechanik ist damit vollständig umgesetzt und kann weiter ausgebaut werden.



# What could go wrong?

Mögliche Probleme:

- Der Spieler fällt durch den Boden → Kollision im TileSet fehlt

- Der Spieler springt unendlich → is_on_floor() wurde nicht verwendet

- Die Kamera bewegt sich nicht → Camera2D ist nicht aktiviert

- Bewegungen fühlen sich komisch an → Physik nicht in _physics_process verwendet

- Diese Fehler lassen sich durch Überprüfen der Node-Struktur und der Kollisionseinstellungen beheben.
