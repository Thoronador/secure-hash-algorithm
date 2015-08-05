======================================================================
                sha256 - SHA-256-Prüfsummen berechnen
                           (von Thoronador)
======================================================================


Zweck des Programmes:
=====================

Das Programm sha256 soll dazu dienen, SHA-256-Prüfsummen (256bit) zu
allen Dateien, die dem Programm als Befehlszeilenparameter übergeben
werden, zu berechnen und auszugeben.
Seit Version 1.1 kann man alternativ auch SHA-1-Prüfsummen (160bit)
berechnen lassen, falls dies gewünscht wird.


Programmaufruf:
===============

Da dies (offensichtlich) ein Kommandozeilenprogramm ist, kann man es
via Kommandozeile/ Shell aufrufen. Eine Liste der erlaubten Parameter
folgt.


Übersicht:
----------

  sha256 [--sha1 | --sha224 | --sha256 | --sha384 | --sha512] DATEINAME ...


Optionen + Parameter:
---------------------

  --sha1
      Berechnet SHA-1-Pr�fsummen (160bit) anstelle von SHA-256.

  --sha224
      Berechnet SHA-224-Pr�fsummen (224bit) anstelle von SHA-256.

  --sha256
      Berechnet SHA-256-Pr�fsummen (256bit). Dies ist die Standard-
      vorgabe.

  --sha384
      Berechnet SHA-384-Pr�fsummen (384bit) anstelle von SHA-256.

  --sha512
      Berechnet SHA-512-Pr�fsummen (512bit) anstelle von SHA-256.

  --help
      Zeigt einen (englischen) Hilfetext und listet g�ltige Programm-
      optionen auf.

  --version
      Gibt Versionsinformationen aus und beendet das Programm.

  DATEINAME
        Pfad zu einer Datei, deren Pr�fsumme berechnet werden soll.
        Kann mehrmals angegeben werden, um mehrere Dateien auszu-
        werten.

Ein typischer Aufruf kann so aussehen:

  sha256 foo.txt some_dir/bar.baz

Damit w�rden die SHA-256-Pr�fsummen von foo.txt und bar.baz im Unter-
verzeichnis some_dir berechnet (und ausgegeben) werden. Falls eine der
angegebenen Dateien nicht existiert, bricht das Programm ab.


Lizenz und Quellcode
====================

Das Programm sha256 steht unter der GNU General Public License 3,
einer freien Softwarelizenz. Der volle Text der Lizenz ist in der
Datei LICENSE enthalten und kann auch auf
  http://www.gnu.org/licenses/gpl-3.0.html
eingesehen werden.

Das Programm wurde in der Hoffnung, dass es n�tzlich ist, erstellt
und verf�gbar gemacht. Das Programm ist nicht vollendet und kann daher
Fehler ("Bugs") enthalten. Aus den genannten Gr�nden wird es unter
dieser Lizenz "so wie es ist" ohne jegliche Gew�hrleistung zur Verf�-
gung gestellt. Dies gilt unter anderem - aber nicht ausschlie�lich -
f�r Verwendbarkeit f�r einen bestimmten Zweck, M�ngelfreiheit und
Richtigkeit (siehe dazu die entsprechenden Abschnitte der GNU General
Public License 3).

Der Quellcode des Programms l�sst sich auf GitHub.com einsehen,
das Projekt findet sich unter
  https://github.com/Thoronador/secure-hash-algorithm
