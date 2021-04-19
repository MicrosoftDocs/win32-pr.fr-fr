---
title: Utilisation de la propriété invokeURLs dans une page Web affichée par Firefox
description: Utilisation de la propriété invokeURLs dans une page Web affichée par Firefox
ms.assetid: cec2ba89-b08f-4c83-bcb2-a4df1ce6f179
keywords:
- Lecteur Windows Media, incorporer un contrôle ActiveX
- Modèle objet du lecteur Windows Media, incorporer un contrôle ActiveX
- modèle objet, incorporer un contrôle ActiveX
- Windows Media Player Mobile, incorporer un contrôle ActiveX
- Contrôle ActiveX du lecteur Windows Media, incorporation
- Windows Media Player Mobile, contrôle ActiveX, incorporation
- Contrôle ActiveX du lecteur Windows Media, pages Web
- Windows Media Player Mobile contrôle ActiveX, pages Web
- Contrôle ActiveX du lecteur Windows Media, propriété invokeURLs
- Contrôle ActiveX Windows Media Player Mobile, propriété invokeURLs
- incorporation, pages Web
- Incorporation de page Web, propriété invokeURLs
- Lecteur Windows Media, Firefox
- Windows Media Player Object Model, Firefox
- modèle objet, Firefox
- Contrôle ActiveX du lecteur Windows Media, Firefox
- Contrôle ActiveX, Firefox
- Firefox, propriété invokeURLs
- Incorporation de pages Web, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0a2eb96e65d8fa6d2758669e3c844b2d13c0bc
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2019
ms.locfileid: "106531599"
---
# <a name="using-the-invokeurls-property-in-a-web-page-displayed-by-firefox"></a><span data-ttu-id="5c2ff-122">Utilisation de la propriété invokeURLs dans une page Web affichée par Firefox</span><span class="sxs-lookup"><span data-stu-id="5c2ff-122">Using the invokeURLs Property in a Web Page Displayed by Firefox</span></span>

<span data-ttu-id="5c2ff-123">Certains fichiers multimédias contiennent des URL incorporées pour lesquelles le lecteur Windows Media affiche des pages Web dans une fenêtre de navigateur Web ou un frame à mesure que le fichier multimédia est lu.</span><span class="sxs-lookup"><span data-stu-id="5c2ff-123">Some media files contain embedded URLs for which Windows Media Player displays webpages in a Web browser window or frame as the media file plays.</span></span> <span data-ttu-id="5c2ff-124">Dans Windows Internet Explorer, vous pouvez utiliser la propriété [Settings. invokeURLs](settings-invokeurls.md) pour spécifier si les pages sont affichées pour les URL incorporées, et vous pouvez utiliser la propriété [Settings. defaultFrame](settings-defaultframe.md) pour spécifier un frame pour l’affichage de ces pages.</span><span class="sxs-lookup"><span data-stu-id="5c2ff-124">In Windows Internet Explorer, you can use the [Settings.invokeURLs](settings-invokeurls.md) property to specify whether pages are displayed for embedded URLs, and you can use the [Settings.defaultFrame](settings-defaultframe.md) property to specify a frame for displaying such pages.</span></span>

<span data-ttu-id="5c2ff-125">Dans Firefox, certaines solutions de contournement sont requises pour définir la propriété **invokeURLs** et pour spécifier un frame permettant d’afficher les pages des URL incorporées.</span><span class="sxs-lookup"><span data-stu-id="5c2ff-125">In Firefox, some workarounds are required to set the **invokeURLs** property and to specify a frame for displaying pages for embedded URLs.</span></span>

## <a name="setting-the-invokeurls-property"></a><span data-ttu-id="5c2ff-126">Définition de la propriété invokeURLs</span><span class="sxs-lookup"><span data-stu-id="5c2ff-126">Setting the invokeURLs property</span></span>

<span data-ttu-id="5c2ff-127">La valeur par défaut de la propriété **Settings. invokeURLs** est true. par conséquent, si vous souhaitez que la valeur soit false, vous devez la définir explicitement.</span><span class="sxs-lookup"><span data-stu-id="5c2ff-127">The default value of the **Settings.invokeURLs** property is true, so if you want the value to be false, you must set it explicitly.</span></span> <span data-ttu-id="5c2ff-128">Dans Internet Explorer, vous pouvez affecter à **invokeURLs** la valeur false dans un élément param à l’intérieur de l’élément Object du contrôle Player.</span><span class="sxs-lookup"><span data-stu-id="5c2ff-128">In Internet Explorer, you can set **invokeURLs** to false in a PARAM element inside the Player control's OBJECT element.</span></span>

<span data-ttu-id="5c2ff-129">Le plug-in Firefox ne prend pas en charge la définition de la propriété **invokeURLs** dans un élément param.</span><span class="sxs-lookup"><span data-stu-id="5c2ff-129">The Firefox plug-in does not support setting the **invokeURLs** property in a PARAM element.</span></span>

<span data-ttu-id="5c2ff-130">Vous pouvez contourner cette limitation en définissant la propriété **invokeURLs** dans le script.</span><span class="sxs-lookup"><span data-stu-id="5c2ff-130">You can work around this limitation by setting the **invokeURLs** property in script.</span></span> <span data-ttu-id="5c2ff-131">Le code suivant montre comment définir la propriété **invokeURLs** sur false dans une page Web qui peut être affichée par Internet Explorer et Firefox.</span><span class="sxs-lookup"><span data-stu-id="5c2ff-131">The following code shows how to set the **invokeURLs** property to false in a webpage that can be displayed by both Internet Explorer and Firefox.</span></span>


```HTML
<HTML>
  <BODY OnLoad="Initialize()">

    <SCRIPT type="text/javascript">

      document.write('<OBJECT id="Player"'); 

      if(-1 != navigator.userAgent.indexOf("MSIE"))
      {               
        document.write(' classid="clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6"');       
      }
      else if(-1 != navigator.userAgent.indexOf("Firefox"))
      {      
        document.write(' type="application/x-ms-wmp"');        
      }  

      document.write(' width=300 height=200>');
      document.write('<PARAM name="autoStart" value="false"/>');
      document.write('<PARAM name="url" value="c:\\MediaFiles\\Glass.wmv"/>');
      document.write('</OBJECT>'); 
      
    </SCRIPT>

    <SCRIPT>
      function Initialize()
      {
        Player.settings.invokeURLs = false;
        Player.controls.play();
      }
    </SCRIPT>

  </BODY>
</HTML>

```



## <a name="displaying-webpages-in-a-frame"></a><span data-ttu-id="5c2ff-132">Affichage des pages Web dans un frame</span><span class="sxs-lookup"><span data-stu-id="5c2ff-132">Displaying webpages in a frame</span></span>

<span data-ttu-id="5c2ff-133">Un fichier multimédia peut contenir des URL qui affichent des pages Web dans une fenêtre ou un frame du navigateur lorsque le fichier multimédia est lu.</span><span class="sxs-lookup"><span data-stu-id="5c2ff-133">A media file can contain URLs that display webpages in a browser window or frame as the media file is played.</span></span> <span data-ttu-id="5c2ff-134">Dans Internet Explorer, vous pouvez utiliser la propriété [Settings. defaultFrame](settings-defaultframe.md) pour spécifier le frame dans lequel ces pages sont affichées.</span><span class="sxs-lookup"><span data-stu-id="5c2ff-134">In Internet Explorer, you can use the [Settings.defaultFrame](settings-defaultframe.md) property to specify the frame in which those pages are displayed.</span></span> <span data-ttu-id="5c2ff-135">Si vous ne définissez pas la propriété **defaultFrame** , les URL sont affichées dans une fenêtre distincte du navigateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="5c2ff-135">If you do not set the **defaultFrame** property, URLs are displayed in a separate window of the default browser.</span></span> <span data-ttu-id="5c2ff-136">Toutefois, le plug-in Firefox ne prend pas en charge la propriété **Settings. defaultFrame** .</span><span class="sxs-lookup"><span data-stu-id="5c2ff-136">However, the Firefox plug-in does not support the **Settings.defaultFrame** property.</span></span> <span data-ttu-id="5c2ff-137">Pour contourner cette limitation, affectez la valeur false à la propriété **Settings. invokeURLs** et écrivez un gestionnaire d’événements [commande](player-player-scriptcommand.md) qui définit l’emplacement du frame cible.</span><span class="sxs-lookup"><span data-stu-id="5c2ff-137">To work around this limitation, set the **Settings.invokeURLs** property to false and write a [ScriptCommand](player-player-scriptcommand.md) event handler that sets the location of the target frame.</span></span> <span data-ttu-id="5c2ff-138">L’exemple suivant, qui fonctionne dans Internet Explorer et Firefox, illustre cette technique.</span><span class="sxs-lookup"><span data-stu-id="5c2ff-138">The following example, which works in Internet Explorer and Firefox, illustrates this technique.</span></span> <span data-ttu-id="5c2ff-139">Supposons que la page Web affichée dans l’exemple se trouve dans le frame \[ 0 \] et que vous souhaitiez que la page de l’URL s’affiche dans le cadre \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="5c2ff-139">Assume that the webpage shown in the example is in frames\[0\] and you want the URL's page to be displayed in frames\[1\].</span></span>


```HTML
<HTML>
  <BODY OnLoad="Initialize()">

    <SCRIPT type="text/javascript">

      document.write('<OBJECT id="Player"'); 

      if(-1 != navigator.userAgent.indexOf("MSIE"))
      {               
        document.write(' classid="clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6"');       
      }
      else if(-1 != navigator.userAgent.indexOf("Firefox"))
      {      
        document.write(' type="application/x-ms-wmp"');        
      }  

      document.write(' width=300 height=200>');
      document.write('<PARAM name="autoStart" value="false"/>');
      document.write('<PARAM name="url" value="c:\\MediaFiles\\Glass.wmv"/>');
      document.write('</OBJECT>'); 
      
    </SCRIPT>

    <SCRIPT>
      function Initialize()
      {
        Player.settings.invokeURLs = false;
        Player.controls.play();
      }
    </SCRIPT>

    <SCRIPT for="Player" event="ScriptCommand(scType, scParam)">
      if( scType == "URL" )
      {
        parent.frames[1].location = scParam;
      }
    </script>

  </BODY>
</HTML>

```



## <a name="related-topics"></a><span data-ttu-id="5c2ff-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5c2ff-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c2ff-141">**Utilisation du contrôle du lecteur Windows Media avec Firefox**</span><span class="sxs-lookup"><span data-stu-id="5c2ff-141">**Using the Windows Media Player Control with Firefox**</span></span>](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




