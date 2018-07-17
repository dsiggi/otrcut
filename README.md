# otrcut
Dieses Script schneidet Filme/Serien von http://www.onlinetvrecorder.de anhand der Schnittlisten von
http://www.cutlist.at.
Dies geschieht entweder durch avidemux oder avisplit/avimerge.
Avidemux schneidet im Gegensatz zu avisplit/avimerge keyframe-genau.
avisplit/avimerge ist Bestandteil von transcode, avidemux muss separat installiert werden.

Dieses Script darf frei verändert und weitergegeben werden.

otrcut.sh [optionen] -i film.mpg.avi

Optionen:

-i, --input [arg]	Input Datei/Dateien

-a, --avisplit		Avisplit und avimerge anstelle von avidemux verwenden

-e, --error		Bei Fehlern das Script beenden

--tmp [arg]		TMP-Ordner angeben (Standard: /tmp/), In diesem Ordner wird noch ein Ordner "otrcut" angelegt, ACHTUNG: ALLE Daten in \$tmp werden gelöscht!!!

-l, --local 		Lokale Cutlists verwenden (Cutlists werden im aktuellen Verzeichnis gesucht)

--delete		Quellvideo nach Schneidevorgang löschen ACHTUNG: Falls es sich bei der Quelle um ein OtrKey handelt wird dies auch gelöscht!!!

-o, --output [arg]	Ausgabeordner wählen (Standard "./cut")

-ow, --overwrite	Schon existierende Ausgabedateien überschreiben

-b, --bewertung		Bewertungsfunktion aktivieren

-p, --play		Zusammen mit "-b, --bewertung" einsetzbar, startet vor dem Bewerten das Video in einem Videoplayer (Wird in der Variablen \$player definiert)

-w, --warn		Verschiedenen Warnungen werden nicht angezeigt.

--toprated		Verwendet die best bewertetste Cutlist

-v, --verbose		Ausführliche Ausgabe von avidemux bzw. avimerge/avisplit aktivieren (Zur Zeit deaktiviert!)

--nosmart		So wird das --force-smart-Argument für avidemux abgeschaltet.

--personal		Die persönliche ID von cutlist.at zum Bewerten benutzen

-av, --avidemux		Bei Verwendung von Avidemux <=2.4 muss diese Schalter gesetzt werden.

-c, --copy		Wenn \$toprated=yes, und keine Cutlist gefunden wird, \$film nach \$output kopieren

-m, --move		Wenn \$toprated=yes, und keine Cutlist gefunden wird, \$film nach \$output verschieben

-s, --other		Auch nach Cutlists in anderen Formaten suchen.

--vcodec [arg]          Videocodec (avidemux) spezifizieren. Wenn nicht gesetzt, dann "copy". Mögliche Elemente für [arg]: Divx/Xvid/FFmpeg4/VCD/SVCD/DVD/XVCD/XSVCD/COPY

-u, --update		Nach einer neuen Version von OtrCut suchen

-h, --help		Diese Hilfe ^^

Danke an MKay für das Aspect-Ratio-Script.
Danke an Florian Knodt für seinen Patch.
