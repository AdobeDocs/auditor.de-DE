---
description: 'null'
seo-description: 'null'
seo-title: Auditor FAQs
title: Häufig gestellte Fragen zum Prüfer
uuid: 4db0781a-b288-4ec2-97ff-410a8241a61d
translation-type: tm+mt
source-git-commit: c697f3d759ad1f086f16a39e03062431583ffd7f

---


# Häufig gestellte Fragen zum Prüfer{#auditor-faq}

Dieser Artikel enthält Antworten auf häufig gestellte Fragen zu Adobe Experience Platform Auditor.

* [Was ist Auditor?](auditor-faq.md#section-c4a9bc8d8eef41598c27e0951a2518e4)
* [Ist mein Unternehmen berechtigt, Auditor zu verwenden?](auditor-faq.md#section-f90094050d1e44929066a942833435cf)
* [Welche Adobe-Technologien werden von Auditor bewertet?](auditor-faq.md#section-52833b71c05448aaae508e6070a387f5)
* [Wie viele Prüfungen kann ich durchführen?](auditor-faq.md#section-caac1e50ce1249aeba76308f3ef03fa0)
* [Was wird für eine Prüfung durchsucht?](auditor-faq.md#section-6d068ed69ece4a1bb6d0c34454550c45)
* [Wie lange dauert eine Prüfung?](auditor-faq.md#section-5086ae27ef1f4671a9d951348654633a)
* [Welche Informationen enthält ein Bericht?](auditor-faq.md#section-752d6b82f6744a3182c4ce16ea6b5d3f)
* [Wie umsetzbar sind diese Informationen?](auditor-faq.md#section-9308c1ea882048b781087ae6d2eee9f0)
* [Kann der Prüfer die Nicht-Adobe-Technologie prüfen?](auditor-faq.md#section-f6e73c56083b4815bbf901296038bcd4)
* [Kann ich meine IP-Adressen auf eine weiße Liste setzen, um Scannerseiten zuzulassen...](auditor-faq.md#section-011e4f54c58140ffb93bedeb0745b6cc)
* [Verwendet Auditor dieselben IP-Bereiche wie Observepoint?](auditor-faq.md#section-39512b156e194787981bdd572ff5b5a9)

## Was ist Auditor? {#section-c4a9bc8d8eef41598c27e0951a2518e4}

Auditor ist ein Dienst der Adobe Experience Cloud, der gemeinsam mit ObservePoint, Experten für die Validierung digitaler Implementierungen, entwickelt wurde.

Mit Auditor können Kunden bis zu 500 Webseiten gleichzeitig scannen und einen Bericht erhalten, der zeigt, wie sie ihre Adobe Experience Cloud-Implementierungen verbessern können, sodass sie den vollen Wert ihrer Adobe-Investition erhalten.

## Kann ich Auditor verwenden? {#section-f90094050d1e44929066a942833435cf}

Alle Adobe Experience Cloud-Kundenorganisationen erhalten kostenlosen Zugriff auf Auditor (ab 1. Mai 2018). Jeder Benutzer muss die Nutzungsbedingungen von Adobe/ObservePoint in der Benutzeroberfläche von Adobe Experience Cloud akzeptieren, bevor er auf die Funktion zugreifen kann. Wenden Sie sich an Ihren Kundenbetreuer, um die Bedingungen abzuwählen.

## Wie greife ich auf Auditor zu? {#section-531ff85f94384831a89cbb4109549daf}

Nach der Anmeldung bei [https://experiencecloud.adobe.com](https://experiencecloud.adobe.com) können Sie den Auditor finden, indem Sie oben in der Navigation auf **[!UICONTROL Aktivierung]** klicken. Sie können auch direkt zu [https://auditor.adobe.com](https://auditor.adobe.com) gehen.

## Welche Adobe-Technologien werden von Auditor bewertet? {#section-52833b71c05448aaae508e6070a387f5}

* Advertising Cloud DSP
* Advertising Cloud Search
* Analytics
* DTM
* Experience Cloud ID-Dienst (früher Marketing Cloud ID-Dienst)
* Target

Die folgenden Adobe-Lösungen sind derzeit nicht in der Testrubrik enthalten. Die Unterstützung für diese Lösungen ist für zukünftige Updates geplant.

* Advertising Cloud Creative
* Audience Manager
* Campaign
* Launch

## Wie viele Prüfungen kann ich durchführen? {#section-caac1e50ce1249aeba76308f3ef03fa0}

Die Anzahl der Prüfungen, die Sie durchführen können, ist unbegrenzt. Benutzer sind auf eine Prüfung beschränkt, die gleichzeitig ausgeführt wird. Es tritt ein Fehler auf, wenn Sie versuchen, eine Prüfung mit denselben Einstellungen wie die ausgeführte zu starten.

## Was wird für eine Prüfung durchsucht? {#section-6d068ed69ece4a1bb6d0c34454550c45}

Die ObservePoint-Technologie durchsucht derzeit URLs, die in Dokumentlinks enthalten sind. In Schaltflächen, Paginierungs-Widgets und anderen solchen Seitenelementen gefundene Links werden nicht durchsucht.

## Wie schlage ich neue Kriterien für Prüfungen vor? {#section-926e6ef9225b4f0bb19c2927d634cd77}

Sie können in der Auditor-Community Testvorschläge senden, indem Sie auf dieser Seite auf **[!UICONTROL Feedback teilen]** klicken: [https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor](https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor)

## Wie lange dauert eine Prüfung? {#section-5086ae27ef1f4671a9d951348654633a}

Es gibt viele Faktoren, die dazu beitragen, dass eine Prüfung abgeschlossen werden kann, unter anderem:

* Seitenladezeit

   Die ObservePoint-Engine lädt jede Seite der Prüfung in einen Browser. Je schneller eine Seite geladen wird, desto schneller erfolgt die Prüfung.
* Gleichzeitige Verbindungen

   Adobe Auditor verwendet eine einzelne Verbindung, um jede Seite zu besuchen. Vollständige ObservePoint-Konten verwenden bis zu 10 Motoren auf einmal.
* Netzwerkstille

   Nachdem jede Seite geladen wurde, wartet die Prüfung auf eine Netzwerkstille von sieben Sekunden, bevor die nächste Seite aufgerufen wird. Wenn eine Seite viele Netzwerkanforderungen sendet, die nach dem Laden der Seite auftreten, wird nach 60 Sekunden ein Timeout für die Wartezeit ausgeführt.
* Seitenaufrufe

   Wenn eine Seite oder ein Tag nicht gefunden werden kann, speichert die Prüfung diese URL und kehrt später im Audit zurück. Die Prüfung besucht bis zu dreimal eine Seite, um sicherzustellen, dass der Fehler nicht durch ein vorübergehendes Problem verursacht wurde.
* Verarbeitung

   Nachdem eine Prüfung ausgeführt wurde, werden alle erfassten Daten verarbeitet und durch die Regeln gefiltert. Diese Verarbeitungszeit ist erheblich, allerdings dauert sie nicht so viel Zeit wie der Scan selbst.

>[!NOTE]
>
>Adobe Auditor führt jeweils eine einzige Überprüfung aus. Volle ObservePoint-Konten können viele Prüfungen nacheinander ausführen.

## Welche Informationen enthält ein Bericht? {#section-752d6b82f6744a3182c4ce16ea6b5d3f}

Jeder Scan generiert einen Bericht, der anzeigt, welche URLs gescannt wurden, welche Probleme auf diesen Webseiten gefunden wurden und wie die gefundenen Probleme zu beheben sind.

Die Ergebnisse von Prüfungen werden in drei Kategorien unterteilt:

* Konfiguration
* Tag-Konsistenz
* Tag-Präsenz

Zusätzlich zu diesen drei Kategorien enthält der Bericht Warnungen mit Informationen, die Sie kennen sollten, die jedoch nicht unbedingt sofortiges Handeln erfordern.

Die Empfehlungen, die in diese Kategorien fallen, werden dann in drei weitere Kategorien unterteilt:

* Sehr empfohlen
* Empfohlen
* Übergeben

## Wie umsetzbar sind diese Informationen? {#section-9308c1ea882048b781087ae6d2eee9f0}

Alle Empfehlungen von Auditor sollen Ihnen dabei helfen, ein Problem bei der Implementierung von Adobe Experience Cloud-Lösungen wie DTM oder Target zu beheben. Um dies zu erleichtern, hat das Auditor-Team intensiv daran gearbeitet, sehr detaillierte Anweisungen darüber zu geben, was dort getan werden muss. Sie können eine Tabelle mit allen gescannten URLs und allen Testergebnissen exportieren, um problematische Bereiche einfach zu identifizieren. Hier ein Beispiel für eine Empfehlung für eine DTM-Implementierung:

<table id="table_EE67775088344BDAA5126268072D6089"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>pageBottom-Rückruf zuletzt</b> </p> <p>Für eine korrekte DTM-Implementierung ist eine Funktion _satellite.pageBottom() erforderlich. Fügen Sie das Inline-Skript unmittelbar vor dem schließenden &lt;/body&gt;-Tag hinzu, um eine ordnungsgemäße DTM-Funktionalität sicherzustellen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Kann der Prüfer die Nicht-Adobe-Technologie prüfen? {#section-f6e73c56083b4815bbf901296038bcd4}

Nein. Das vollständige Angebot von ObservePoint ermöglicht es Kunden jedoch, alle Marketing-Tags und -Technologien zu prüfen und zu überwachen. Als Adobe-Kunde haben Sie Zugriff auf ein kostenloses Testkonto. Um auf Ihr Testkonto zuzugreifen, besuchen Sie [die Seite](https://www.observepoint.com/adobe-auditor/?utm_source=Adobe&utm_medium=Auditor&utm_campaign=Premium)&quot;Auditor&quot;von ObservePoint.

## Kann ich meine IP-Adressen auf eine weiße Liste setzen, um Seiten zu prüfen, die durch eine Anmeldung geschützt sind? {#section-011e4f54c58140ffb93bedeb0745b6cc}

Diese Funktion wird derzeit ohne das vollständige ObservePoint-Angebot nicht unterstützt.

## Verwendet Auditor dieselben IP-Bereiche wie ObservePoint? {#section-39512b156e194787981bdd572ff5b5a9}

Das Crawling wird von ObservePoint ausgeführt, sodass dieselben IP-Adressen verwendet werden.

Weitere Informationen finden Sie in der [ObservePoint-Dokumentation](https://help.observepoint.com/articles/2312494-observepoint-whitelisting-and-proxy-list) .