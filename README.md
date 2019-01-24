
# Vorgang Anlegen (BEX) API

API zum automatisierten Anlegen von BaufiSmart Vorgängen.

# Dokumentaion

#### Aktuelle Version 13

Diese Schnittstelle wird auch als "Baufismart EXtern" - kurz: "BEX" bezeichnet. Es werden immer die letzten 3 Versionen der Schnittstelle unterstützt.

Die BEX API wird durch die Datei [bex-v13-VorgangAnlegen.wsdl](bex-v13-VorgangAnlegen.wsdl)
vollständig beschrieben. Die Datei [bex-v13-VorgangAnlegen.xsd](bex-v13-VorgangAnlegen.xsd)
kann genutzt werden, um mit eigenen Programmen/Werkzeugen
die Anfragen zu validieren.

# Beispiele


In [Beispiele](Beispiele) befinden sich XML-Dateien Anfragen und Antworten
an den BEX SOAP Service. für eine bessere Lesbarkeit ist
der SOAP-Envelope und SOAP-Body nicht dargestellt,
sondern nur der Inhalt
der [Vorgang.xml](Beispiele/bex-v13-Vorgang.xml) (Anfrage)
und der [VorgangMetadaten.xml](Beispiele/bex-v13-VorgangMetadaten.xml) (Antwort).

## Code-Generierung für Client-Stubs

Aus der WSDL-Beschreibung kann automatisch Code generiert werden.

#### Beispiel für Java

````bash
wsimport -keep -extension bex-v13-VorgangAnlegen.wsdl
````
