---
description: Diese Referenz enthält weitere Informationen zu den Tests, die Auditor für die Tag-Präsenz durchführt.
seo-description: Diese Referenz enthält weitere Informationen zu den Tests, die Auditor für die Tag-Präsenz durchführt.
seo-title: Tag-Präsenz
title: Tag-Präsenz
uuid: 91aa355b-7022-431c-9837-e108b5ce604d
translation-type: tm+mt
source-git-commit: c697f3d759ad1f086f16a39e03062431583ffd7f

---


# Tag-Präsenz

Diese Referenz enthält weitere Informationen zu den Tests, die Auditor für die Tag-Präsenz durchführt.

Auditor bewertet, ob das Tag vorhanden ist und ob es sich an der richtigen Stelle im Seiten-Code befindet.

<table id="table_98A2E3F7B3154EEFA76D0CAE2FE97CAB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Test </th> 
   <th colname="col2" class="entry"> Kriterien </th> 
   <th colname="col3" class="entry"> Empfehlung </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>Advertising Cloud - Code-Präsenz</b> </p> <p>Gewicht: 5 </p> </td> 
   <td colname="col2"> <p> Das Advertising Cloud-Tag ist im DOM nicht verfügbar. </p> </td> 
   <td colname="col3"> <p>Implementieren Sie das Tag Advertising Cloud mit der Advertising Cloud Launch Extension. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Advertising Cloud - Segmentpixel implementiert</b> </p> <p>Gewicht: 5 </p> </td> 
   <td colname="col2"> <p> Aktualisieren Sie Ihre Advertising Cloud-Segmentpixel auf die neuen Image-only-Tags der Advertising Cloud. Die Verwendung der nicht mehr unterstützten AMO-Segment-Tags kann zu Datenverlusten führen. </p> </td> 
   <td colname="col3"> <p>Implementieren Sie das Segment-Pixel der Advertising Cloud mit der Advertising Cloud Launch Extension. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Analytics - In DOM geladen</b> </p> <p>Gewicht: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/" format="https" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Das Adobe Analytics-Tag wurde nicht erkannt. </p> </td> 
   <td colname="col3"> <p>Installieren Sie die neueste Version von Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b> DTM - Bibliothek geladen</b> </p> <p>Gewicht: 5 </p> <p>Weitere Informationen: </p> <p> 
     <ul id="ul_7E706EBC2E4649A69732E6982E116E22"> 
      <li id="li_9AF0257E39C347A9AE6D8D8FFBD66B38"><a href="https://docs.adobe.com/content/help/en/dtm/using/admin/c-troubleshooting.html" format="html" scope="external"> DTM-Fehlerbehebung</a> </li> 
      <li id="li_7B422BCCD2654B0A9059799FB5276BE8"><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Kopf- und Fußzeilencode hinzufügen</a> </li> 
     </ul> </p> </td> 
   <td colname="col2"> <p> Ein globales _satellite-Objekt wurde im DOM nicht gefunden. Das dynamische Tag-Management ist entweder nicht installiert oder kann nicht ausgeführt werden. </p> </td> 
   <td colname="col3"> <p>Vergewissern Sie sich, dass die DTM-Bibliothek auf der Seite implementiert ist und nicht durch nachfolgende Skriptaktivitäten blockiert wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b> DTM - Einbettungscode</b> </p> <p>Gewicht: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/code.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Produktions-Sites sollten nur eine DTM-Bibliothek laden. </p> </td> 
   <td colname="col3"> <p>Vergewissern Sie sich, dass nur die Produktionsbibliothek auf der Seite geladen wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>DTM - Rückruf pageBottom vorhanden in &lt;body&gt;</b> </p> <p>Gewicht: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Der Rückruf <span class="codeph"> _satellite.pageBottom()</span> wurde nicht im <span class="codeph"> &lt;body&gt;</span> der Seite gefunden, was für das dynamische Tag-Management erforderlich ist. </p> <p>Dieser Test schlägt fehl, wenn der <span class="codeph"> pageBottom- </span>Aufruf überhaupt nicht auf der Seite gefunden wird oder wenn er sich im <span class="codeph"> &lt;head&gt;</span> -Tag (oder einer anderen unerwarteten Position) befindet. Sie wird nur dann übernommen, wenn <span class="codeph"> pageBottom</span> irgendwo im <span class="codeph"> &lt;body&gt;</span> -Tag gefunden wird. Wenn es sich nicht auf der Seite befindet, funktioniert es nicht und die anderen beiden <span class="codeph"> SeitenBottom</span> -Tests schlagen ebenfalls fehl. </p> </td> 
   <td colname="col3"> <p>Fügen Sie das Inline-Skript unmittelbar vor dem schließenden Tag <span class="codeph"> &lt;/body&gt;</span> hinzu, um eine ordnungsgemäße DTM-Funktionalität sicherzustellen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>DTM - pageBottom-Tag ausgelöst</b> </p> <p>Gewicht: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Das DTM- <code> pageBottom</code> Tag wurde nicht erkannt. </p> <p>Dies kann vorkommen, wenn sich der Aufruf in einer <code> if</code> Anweisung befindet, die in etwa <code> if (false) {_satellite.pageBottom()}</code>der Während es also existiert und korrekt platziert ist, wird das Tag möglicherweise nicht ausgelöst. </p> </td> 
   <td colname="col3"> <p>Installieren Sie den DTM- <code> pageBottom</code> Aufruf auf jeder Seite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID-Dienst - Code-Präsenz</b> </p> <p>Gewicht: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/intro/overview.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p>Der Experience Cloud ID-Dienst-Code wurde nicht gefunden. Die Experience Cloud ID (MCID) wird dringend empfohlen, um sicherzustellen, dass Sie den größtmöglichen Nutzen aus Ihren Experience Cloud-Lösungen ziehen, und ist für das ID-Management in allen Experience Cloud-Lösungen von entscheidender Bedeutung. </p> </td> 
   <td colname="col3"> <p> Installieren Sie die neueste Version von MCID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID-Dienst - Cookie-Präsenz</b> </p> <p>Gewicht: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/implementation-guides/implementation-guides.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Das <span class="codeph"> AMCV_</span> -Cookie wurde nicht gefunden. Sie müssen ein Besucherobjekt aus dem Code VisitorAPI.js<span class="codeph"> </span> instanziieren. </p> </td> 
   <td colname="col3"> <p> Ist dies eine DTM-Implementierung, überprüfen Sie, ob die AdobeOrg-ID korrekt in das MCID-Tool eingegeben wurde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID-Dienst - MID-Wert vorhanden</b> </p> <p>Gewicht: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/intro/cookies.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Der MID-Wert wurde im <span class="codeph"> AMCV_</span> -Cookie nicht gefunden. </p> </td> 
   <td colname="col3"> <p>Testen Sie erneut, um nach einer MCID-API-Latenz zu suchen. Wenn die Bedingung weiterhin besteht, wenden Sie sich an den Adobe-Kundendienst. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b> Start - Bibliothek geladen</b> </p> <p>Gewicht: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Ein globales _satellite-Objekt wurde im DOM nicht gefunden. Launch ist entweder nicht installiert oder kann nicht ausgeführt werden. </p> </td> 
   <td colname="col3"> <p>Vergewissern Sie sich, dass die Launch-Bibliothek auf der Seite implementiert ist und nicht von nachfolgenden Skriptaktivitäten blockiert wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Start - Es stehen nicht mehrere Einbettungsskripten zur Verfügung</b> </p> <p>Gewicht: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p>Es sollten nicht mehrere Einbettungsskripte auf der Seite geladen werden. Produktions-Sites sollten nur eine Startbibliothek laden. </p> </td> 
   <td colname="col3"> <p>Vergewissern Sie sich, dass nur die Produktionsbibliothek auf der Seite geladen wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Start - Rückruf pageBottom vorhanden in &lt;body&gt;</b> </p> <p>Gewicht: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Der Rückruf <span class="codeph"> _satellite.pageBottom()</span> wurde nicht im <span class="codeph"> &lt;body&gt;</span> der Seite gefunden, was für Launch erforderlich ist. </p> <p>Dieser Test schlägt fehl, wenn der <span class="codeph"> pageBottom- </span>Aufruf überhaupt nicht auf der Seite gefunden wird oder wenn er sich im <span class="codeph"> &lt;head&gt;</span> -Tag (oder einer anderen unerwarteten Position) befindet. Sie wird nur dann übernommen, wenn <span class="codeph"> pageBottom</span> irgendwo im <span class="codeph"> &lt;body&gt;</span> -Tag gefunden wird. Wenn es sich nicht auf der Seite befindet, funktioniert es nicht und die anderen beiden <span class="codeph"> SeitenBottom</span> -Tests schlagen ebenfalls fehl. </p> </td> 
   <td colname="col3"> <p>Fügen Sie das Inline-Skript unmittelbar vor dem schließenden <span class="codeph"> &lt;/body&gt;</span> -Tag hinzu, um eine ordnungsgemäße Startfunktion sicherzustellen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Start - Rückruffunktion "pageBottom"sollte bei asynchroner Bereitstellung nicht vorhanden sein</b> </p> <p>Gewicht: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p>Der Rückruf <span class="codeph"> _satellite.pageBottom()</span> wurde auf der Seite gefunden, was bei asynchroner Bereitstellung von Launch nicht der Fall sein sollte. </p> </td> 
   <td colname="col3"> <p>Entfernen Sie das<span class="codeph"> Skript _satellite.pageBottom()</span> , um eine ordnungsgemäße Startfunktion zu aktivieren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Target - Code-Präsenz</b> </p> <p>Gewicht: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p>Target sollte im DOM definiert werden. </p> </td> 
   <td colname="col3"> <p>Installieren Sie die neueste Version von Target (at.js). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b> Target - Bibliothek geladen in &lt;head&gt;</b> </p> <p>Gewicht: 4 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external"> Weitere Informationen</a> </p> </td> 
   <td colname="col2"> <p> Die Target-Bibliothek sollte im Tag <span class="codeph"> &lt;head&gt;</span> geladen werden. </p> </td> 
   <td colname="col3"> <p> Vergewissern Sie sich, dass die Target-Bibliothek im Tag <span class="codeph"> &lt;head&gt;</span> geladen ist. </p> </td> 
  </tr> 
 </tbody> 
</table>