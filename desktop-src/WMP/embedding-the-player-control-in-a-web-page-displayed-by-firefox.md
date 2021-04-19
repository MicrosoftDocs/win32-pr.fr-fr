---
title: Incorporation du contrôle Player dans une page Web affichée par Firefox
description: Incorporation du contrôle Player dans une page Web affichée par Firefox
ms.assetid: 57e725dc-6430-43ec-a39c-c17854a7d8db
keywords:
- Lecteur Windows Media, incorporer un contrôle ActiveX
- Modèle objet du lecteur Windows Media, incorporer un contrôle ActiveX
- modèle objet, incorporer un contrôle ActiveX
- Windows Media Player Mobile, incorporer un contrôle ActiveX
- Contrôle ActiveX du lecteur Windows Media, incorporation
- Windows Media Player Mobile, contrôle ActiveX, incorporation
- Contrôle ActiveX, incorporation
- Contrôle ActiveX du lecteur Windows Media, pages Web
- Windows Media Player Mobile contrôle ActiveX, pages Web
- Contrôle ActiveX, pages Web
- Lecteur Windows Media, Firefox
- Windows Media Player Object Model, Firefox
- modèle objet, Firefox
- Windows Media Player Mobile, Firefox
- Contrôle ActiveX du lecteur Windows Media, Firefox
- Windows Media Player Mobile contrôle ActiveX, Firefox
- Contrôle ActiveX, Firefox
- Firefox, à propos de l’incorporation de pages Web
- incorporation, pages Web
- Incorporation de pages Web, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16063ea07a0262ab798e58ed02e4d5a5b6b5d65
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2019
ms.locfileid: "106510445"
---
# <a name="embedding-the-player-control-in-a-web-page-displayed-by-firefox"></a><span data-ttu-id="a0570-123">Incorporation du contrôle Player dans une page Web affichée par Firefox</span><span class="sxs-lookup"><span data-stu-id="a0570-123">Embedding the Player Control in a Web Page Displayed by Firefox</span></span>

<span data-ttu-id="a0570-124">Pour incorporer le contrôle du lecteur Windows Media dans une page Web qui peut être affichée par un navigateur Firefox, créez un élément objet ou un élément EMBED dont l’attribut **type** est l’un des types MIME suivants :</span><span class="sxs-lookup"><span data-stu-id="a0570-124">To embed the Windows Media Player control in a webpage that can be displayed by a Firefox browser, create an OBJECT element or an EMBED element that has one of the following mime types as its **type** attribute:</span></span>

-   <span data-ttu-id="a0570-125">application/x-ms-WMP</span><span class="sxs-lookup"><span data-stu-id="a0570-125">application/x-ms-wmp</span></span>
-   <span data-ttu-id="a0570-126">application/ASX</span><span class="sxs-lookup"><span data-stu-id="a0570-126">application/asx</span></span>
-   <span data-ttu-id="a0570-127">vidéo/x-ms-asf-plug-in</span><span class="sxs-lookup"><span data-stu-id="a0570-127">video/x-ms-asf-plugin</span></span>
-   <span data-ttu-id="a0570-128">application/x-Mplayer2</span><span class="sxs-lookup"><span data-stu-id="a0570-128">application/x-mplayer2</span></span>
-   <span data-ttu-id="a0570-129">vidéo/x-ms-asf</span><span class="sxs-lookup"><span data-stu-id="a0570-129">video/x-ms-asf</span></span>
-   <span data-ttu-id="a0570-130">vidéo/x-ms-WM</span><span class="sxs-lookup"><span data-stu-id="a0570-130">video/x-ms-wm</span></span>
-   <span data-ttu-id="a0570-131">audio/x-ms-WMA</span><span class="sxs-lookup"><span data-stu-id="a0570-131">audio/x-ms-wma</span></span>
-   <span data-ttu-id="a0570-132">audio/x-ms-Wax</span><span class="sxs-lookup"><span data-stu-id="a0570-132">audio/x-ms-wax</span></span>
-   <span data-ttu-id="a0570-133">vidéo/x-ms-WMV</span><span class="sxs-lookup"><span data-stu-id="a0570-133">video/x-ms-wmv</span></span>
-   <span data-ttu-id="a0570-134">vidéo/x-ms-wvx</span><span class="sxs-lookup"><span data-stu-id="a0570-134">video/x-ms-wvx</span></span>

<span data-ttu-id="a0570-135">Le type MIME par défaut est application/x-ms-WMP.</span><span class="sxs-lookup"><span data-stu-id="a0570-135">The preferred mime type is application/x-ms-wmp.</span></span>

<span data-ttu-id="a0570-136">Les exemples suivants montrent comment incorporer le contrôle Player à l’aide d’un élément OBJECT ou d’un élément EMBED.</span><span class="sxs-lookup"><span data-stu-id="a0570-136">The following examples show how to embed the Player control using an OBJECT element or an EMBED element.</span></span>


```HTML
<OBJECT id="Player"
  type="application/x-ms-wmp" 
  width="320" height="320">
  <PARAM name="autostart" value="false"/>
</OBJECT>

<EMBED id="Player"
  type="application/x-ms-wmp" 
  width="320" height="320"
  autostart="false"/>

```



<span data-ttu-id="a0570-137">Les exemples précédents fonctionnent dans Firefox, mais pas dans Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="a0570-137">The preceeding examples work in Firefox but not in Internet Explorer.</span></span> <span data-ttu-id="a0570-138">Pour incorporer le contrôle du lecteur dans une page Web qui peut être affichée par Internet Explorer, vous devez créer un élément objet dont l’attribut **ClassID** a pour valeur l’ID de classe du contrôle du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a0570-138">To embed the Player control in a webpage that can be displayed by Internet Explorer, you must create an OBJECT element that has a **classid** attribute set to the class ID of the Windows Media Player control.</span></span>

<span data-ttu-id="a0570-139">L’exemple suivant montre comment incorporer le contrôle du lecteur Windows Media dans une page Web qui peut être affichée correctement à la fois par Internet Explorer et Firefox.</span><span class="sxs-lookup"><span data-stu-id="a0570-139">The following example shows how to embed the Windows Media Player control in a webpage that can be displayed correctly by both Internet Explorer and Firefox.</span></span> <span data-ttu-id="a0570-140">Le script sur la page détecte le type de navigateur et génère la balise d’objet appropriée.</span><span class="sxs-lookup"><span data-stu-id="a0570-140">Script on the page detects the browser type and generates the appropriate OBJECT tag.</span></span>


```HTML
<HTML>
  <BODY>
    <SCRIPT type="text/javascript">
      if(-1 != navigator.userAgent.indexOf("MSIE"))
      {
        document.write('<OBJECT id="Player"');
        document.write(' classid="clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6"');
        document.write(' width=300 height=200></OBJECT>');
      }
      else if(-1 != navigator.userAgent.indexOf("Firefox"))
      {
        document.write('<OBJECT id="Player"'); 
        document.write(' type="application/x-ms-wmp"'); 
        document.write(' width=300 height=200></OBJECT>');
      }         
    </SCRIPT>
  </BODY>
</HTML>

```



## <a name="related-topics"></a><span data-ttu-id="a0570-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a0570-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0570-142">**Utilisation du contrôle du lecteur Windows Media avec Firefox**</span><span class="sxs-lookup"><span data-stu-id="a0570-142">**Using the Windows Media Player Control with Firefox**</span></span>](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




