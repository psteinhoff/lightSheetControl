Kurzanleitung:

Kopieren Sie den Ordner in ihr lokales Arbeitsverzeichnis.
Die Konfigurationsdateien und die Datei FlowVis_Control.exe 
m�ssen im gleichen Verzeichnis liegen wie wie die FlowVis_Control_GUI.exe!

Ansteuerung der Hardware:
Entweder nutzen Sie die beiliegende hb628.dll im gleichen Verzeichnis oder
Sie installieren die Hardwaretreiber mithilfe der technischen Dokumente:
http://www.h-tronic.com/Presse/download/1191030Treiberinstallation.pdf
http://www.h-tronic.com/Presse/download/1191030_1191035_Treiber_Installation_Win7_x86_und_x64.zip
http://www.h-tronic.com/Presse/download/1191030BA.pdf




Vorgehensweise:

1) Installation der USB-Treiber (HB 628) (Windows: Treiber aus Installationsverzeichnis ausw�hlen.)

	Verzeichnis: HB_628_USB_Daten_IO/...

2) Pr�fen der Funktionalit�t:

	- USB-Verbindung herstellen
	- 	.../HB_628_USB_Daten_IO/examples/visual_basic/Digital_Demo/hb628_Digital_Demo.exe* aufrufen, 
		den korrekten com-Port einstellen und eine Verbindung herstellen.
		(Der Com-Port kann unter Windows im Ger�te-Manager gefunden werden.)

-->Sollten hier Probleme auftauchen, den bzw. die Treiber erneut installieren, bis Schritt 2 erfolgreich war.

3) Nutung von FlowVis_Control_GUI.exe:

 	3.0) Settings FlowVis --> Sequence Parameter:
		
		- com-Port: 		Adresse des Com-Port an dem die Steuerung angeschlossen ist

		- Cam_delay: 		Verz�gerungszeit in ms zwischen Ausl�sung der Bildaufzeichnung und der ersten Belichtung
					(Abh�ngig von der verwendeten Kamera:	Nikon D3 ~ 70ms mit Fernausl�ser)

		- 1st lighting period:	Dauer eines ersten Belichtungsabschnitts in ms

		- 1st dark period:	Wartezeit zwischen den Lichtpulsen in ms

		- 2nd lighting period:	Dauer eines zweiten Belichtungsabschnitts in ms
	
		- 2nd dark period:	Wartezeit zwischen zwei aufeinanderfolgenden Bildern 
					(H�ngt stark von der Speichergeschwindigkeit der Kamera ab!, Nikon D3 ~ 450ms)
		
		- Quantity of frames to grab: Anzahl der aufzuzeichnenden Bilder


	3.1) Settings FlowVis --> Controller Settings:       !***Nicht ver�ndern***!

				- Die Bildaufzeichnung wird �ber die Ports 7 und 8 angesteuert.	
				- Die Ansteuerung der Lichtschnitte �ber Port 6.

	3.2) Kameraeinstellungen:      	
				- Die Kamera sollte im Bulb-Modus betrieben werden. Ein Betrieb mist fester Belichtungszeit ist aber ebenso m�glich.
				- Der Auto-fokus der Kamera muss deaktiviert werden, da die Objektiveinstellung sonst verloren geht.

