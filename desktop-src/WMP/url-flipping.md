---
title: Retournement d’URL
description: Retournement d’URL
ms.assetid: 2921dff1-f740-491c-9b5e-79b7638e2065
keywords:
- Windows Media Player, présentations basées sur le Web
- Modèle objet du lecteur Windows Media, présentations basées sur le Web
- modèle objet, présentations basées sur le Web
- Windows Media Player Mobile, présentations basées sur le Web
- Contrôle ActiveX du lecteur Windows Media, présentations basées sur le Web
- Windows Media Player Mobile contrôle ActiveX, présentations basées sur le Web
- Contrôle ActiveX, présentations basées sur le Web
- Lecteur Windows Media, basculement d’URL
- Windows Media Player Object Model, retournement d’URL
- modèle objet, basculement d’URL
- Windows Media Player Mobile, basculement d’URL
- Contrôle ActiveX du lecteur Windows Media, retournement d’URL
- Windows Media Player Mobile Control, basculement d’URL
- Contrôle ActiveX, basculement d’URL
- Présentations basées sur le Web, retournement d’URL
- création de présentations basées sur le Web, retournement d’URL
- Retournement d’URL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 141fdd6b4a7ffc57288a08ffa2f6760cfb029847
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2019
ms.locfileid: "103676014"
---
# <a name="url-flipping"></a><span data-ttu-id="eea43-120">Retournement d’URL</span><span class="sxs-lookup"><span data-stu-id="eea43-120">URL Flipping</span></span>

<span data-ttu-id="eea43-121">L’utilisation de pages Web pour les diaporamas s’appelle le basculement d’URL et est gérée automatiquement par le lecteur Windows Media lorsqu’il rencontre des commandes de script d’URL incorporées dans le flux de médias numériques qu’il lit.</span><span class="sxs-lookup"><span data-stu-id="eea43-121">Using webpages for slide shows is called URL flipping, and is handled automatically by Windows Media Player when it encounters URL script commands embedded in the digital media stream it is playing.</span></span> <span data-ttu-id="eea43-122">Vous pouvez spécifier un frame cible pour vos pages dans chaque commande de script, ou vous pouvez le spécifier en définissant la propriété **Settings. defaultFrame** .</span><span class="sxs-lookup"><span data-stu-id="eea43-122">You can specify a target frame for your pages in each script command, or you can specify it by setting the **Settings.defaultFrame** property.</span></span> <span data-ttu-id="eea43-123">Vous pouvez définir cette propriété dans le code de script ou à l’aide d’un élément PARAM au sein de l’élément OBJECT qui incorpore le contrôle du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="eea43-123">You can set this property in script code or by using a PARAM element within the OBJECT element that embeds the Windows Media Player control.</span></span>

<span data-ttu-id="eea43-124">Vous êtes libre de gérer les commandes de script d’URL dans votre code JScript tout comme vous le feriez pour gérer des commandes de script personnalisées.</span><span class="sxs-lookup"><span data-stu-id="eea43-124">You are free to handle the URL script commands in your JScript code just as you would handle custom script commands.</span></span> <span data-ttu-id="eea43-125">Si vous souhaitez que le contrôle du lecteur Windows Media ignore les commandes de script d’URL afin que vous puissiez les gérer entièrement par vous-même, définissez les *paramètres*. propriété **invokeURLs** la valeur false dans le code de script ou à l’aide d’un élément param comme décrit précédemment.</span><span class="sxs-lookup"><span data-stu-id="eea43-125">If you want the Windows Media Player control to ignore URL script commands so that you can handle them entirely by yourself, set the *Settings*.**invokeURLs** property to false either in script code or using a PARAM element as previously described.</span></span>

<span data-ttu-id="eea43-126">L’exemple suivant illustre un jeu de frames standard pour le basculement d’URL.</span><span class="sxs-lookup"><span data-stu-id="eea43-126">The following example illustrates a typical frameset for URL flipping.</span></span> <span data-ttu-id="eea43-127">Tout d’abord, créez une page décrivant le jeu de frames :</span><span class="sxs-lookup"><span data-stu-id="eea43-127">First, create a page that describes the frameset:</span></span>


```HTML
<HTML>
<FRAMESET cols="300,*">
  <FRAME name="player" src="player.html">
  <FRAME name="content">
</FRAMESET>
</HTML>

```



<span data-ttu-id="eea43-128">Ensuite, créez le fichier player.html référencé dans le jeu de frames à l’aide du code suivant (le fichier Video. wmv est supposé exister dans le même répertoire que les fichiers HTML) :</span><span class="sxs-lookup"><span data-stu-id="eea43-128">Next, create the player.html file referenced in the frameset by using the following code (the video.wmv file is assumed to exist in the same directory as the HTML files):</span></span>


```HTML
<HTML>
<BODY>
<OBJECT ID="Player" CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
  <PARAM name="URL" value="https://www.proseware.com/Media/video.wmv"/>
  <PARAM name="defaultFrame" value="content"/>
</OBJECT>
</BODY>
</HTML>

```



<span data-ttu-id="eea43-129">Si vos pages Web sont suffisamment petites pour être chargées rapidement, cette configuration peut suffire à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="eea43-129">If your webpages are small enough to load rapidly, this setup may be sufficient for your needs.</span></span> <span data-ttu-id="eea43-130">Si, en revanche, vos pages Web sont complexes, le streaming multimédia enrichi peut être plus efficace en fonction de la vitesse de connexion de votre public.</span><span class="sxs-lookup"><span data-stu-id="eea43-130">If, on the other hand, your webpages are complex, rich media streaming may be more effective depending on the connection speed of your audience.</span></span>

> [!Note]  
> <span data-ttu-id="eea43-131">Le retournement d’URL ne fonctionne pas correctement avec les pages affichées dans Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="eea43-131">URL flipping does not work correctly with pages viewed in Netscape Navigator.</span></span> <span data-ttu-id="eea43-132">Au lieu d’apparaître dans le frame spécifié par **defaultFrame**, chaque commande de script d’URL reçue dans le navigateur affiche l’URL dans une nouvelle fenêtre de navigateur.</span><span class="sxs-lookup"><span data-stu-id="eea43-132">Instead of appearing in the frame specified by **defaultFrame**, each URL script command received in Navigator displays the URL in a new browser window.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="eea43-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eea43-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eea43-134">**Création de présentations Web-Based**</span><span class="sxs-lookup"><span data-stu-id="eea43-134">**Creating Web-Based Presentations**</span></span>](creating-web-based-presentations.md)
</dt> <dt>

[<span data-ttu-id="eea43-135">**Utilisation d’un script pour contrôler le basculement d’URL**</span><span class="sxs-lookup"><span data-stu-id="eea43-135">**Using Script to Control URL Flipping**</span></span>](using-script-to-control-url-flipping.md)
</dt> </dl>

 

 




