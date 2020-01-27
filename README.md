
# Vorgang Anlegen (BEX) API

#### Aktuelle Version 14

Diese Schnittstelle wird auch als "Baufismart EXtern" - kurz: "BEX" bezeichnet. Es werden immer die letzten 3 Versionen der Schnittstelle unterstützt.

Die BEX API wird durch die Datei [bex-v14-VorgangAnlegen.wsdl](https://github.com/europace/baufismart-vorgang-anlegen-api/blob/master/bex-v14-VorgangAnlegen.wsdl)
vollständig beschrieben. Die Datei [bex-v14-VorgangAnlegen.xsd](https://github.com/europace/baufismart-vorgang-anlegen-api/blob/master/bex-v14-VorgangAnlegen.xsd)
kann genutzt werden, um mit eigenen Programmen/Werkzeugen
die Anfragen zu validieren.

# Beispiele


In [Beispiele](https://github.com/europace/baufismart-vorgang-anlegen-api/tree/master/Beispiele) befinden sich XML-Dateien Anfragen und Antworten
an den BEX SOAP Service. für eine bessere Lesbarkeit ist
der SOAP-Envelope und SOAP-Body nicht dargestellt,
sondern nur der Inhalt
der [Vorgang.xml](https://github.com/europace/baufismart-vorgang-anlegen-api/blob/master/Beispiele/bex-v14-Vorgang.xml) (Anfrage)
und der [VorgangMetadaten.xml](https://github.com/europace/baufismart-vorgang-anlegen-api/blob/master/Beispiele/bex-v14-VorgangMetadaten.xml) (Antwort).

## Kurzanleitung um ein Vorgang mit SoapUI anzulegen
Ein Probeaufruf der API ist sehr hilfreich, um schnell einzusteigen. Dafür empfehlen wir SoapUI, was auf Windows, Mac OS und Linux funktioniert.

Schritte:
1. SoapUI installieren: https://www.soapui.org/
2. Ein neues SOAP Projekt anlegen
3. Folgende URL in das WSDL Feld eintragen: `https://www.europace2.de/baufiSmart/soap/bex/v14/vorgangAnlegen?wsdl`
4. Ein neuen Request anlegen und mit [diesem Beispiel XML](https://raw.githubusercontent.com/europace/baufismart-vorgang-anlegen-api/master/Beispiele/bex-v14-vorgangAnlegen-SoapUI.xml) befüllen.
4. Eigene PartnerID hier eintragen: `<bex:EmpfaengerPartnerId>XXXXXX</bex:EmpfaengerPartnerId>`
5. Eigenen API Key hier eintragen: `<bex:ApiKey>YYYYYY</bex:ApiKey>`
6. Request absetzen. Als Antwort sollte unter anderem eine VorgangsID kommen.


## Code-Generierung für Client-Stubs

Aus der WSDL-Beschreibung kann automatisch Code generiert werden.

#### Beispiel für Java

````bash
wsimport -keep -extension bex-v14-VorgangAnlegen.wsdl
````
