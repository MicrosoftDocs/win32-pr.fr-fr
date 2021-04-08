---
title: Utilisation du HTML avec le lecteur Windows Media
description: Utilisation du HTML avec le lecteur Windows Media
ms.assetid: 321d4396-511b-4f0d-9ee9-8bdddceedc0e
keywords:
- Lecteur Windows Media, HTML
- Windows Media Player Object Model, HTML
- modèle objet, HTML
- Contrôle ActiveX du lecteur Windows Media, HTML pour le modèle objet
- Contrôle ActiveX, HTML pour le modèle objet
- Contrôle ActiveX mobile pour Windows Media Player, HTML pour modèle objet
- Windows Media Player Mobile, HTML pour le modèle objet
- HTML avec Windows Media Player
- Incorporation de pages Web, HTML
- incorporation, pages Web
- commandes de script
- Retournement d’URL
- diffusion multimédia enrichie
- prise en charge d'un navigateur
- affichage des pages Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7cd96932573802d0a75f95a437b2c7284b3de44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840146"
---
# <a name="using-html-with-windows-media-player"></a><span data-ttu-id="74704-118">Utilisation du HTML avec le lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="74704-118">Using HTML with Windows Media Player</span></span>

## <a name="overview"></a><span data-ttu-id="74704-119">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="74704-119">Overview</span></span>

<span data-ttu-id="74704-120">L’utilisation du HTML avec le lecteur Windows Media est un excellent moyen de combiner des fichiers audio et vidéo avec du texte et des graphiques.</span><span class="sxs-lookup"><span data-stu-id="74704-120">Using HTML with Windows Media Player is an excellent way to combine audio and video with text and graphics.</span></span> <span data-ttu-id="74704-121">Vous pouvez incorporer le contrôle du lecteur Windows Media dans une page Web lorsque vous souhaitez compléter votre contenu statique ou créer des applications Web avec des médias numériques.</span><span class="sxs-lookup"><span data-stu-id="74704-121">You can embed the Windows Media Player control in a webpage when you want to supplement your static content or create Web applications with digital media.</span></span> <span data-ttu-id="74704-122">Si vous souhaitez compléter vos fichiers multimédias numériques à l’aide de HTML, vous pouvez, en revanche, afficher les pages Web en mode complet du lecteur en les référençant dans les sélections de métafichiers Windows Media.</span><span class="sxs-lookup"><span data-stu-id="74704-122">When you want to supplement your digital media with HTML, on the other hand, you can display webpages in the full mode of the Player by referencing them in Windows Media metafile playlists.</span></span>

<span data-ttu-id="74704-123">Si vous écrivez des programmes personnalisés qui incorporent le contrôle du lecteur Windows Media en mode distant, vous pouvez également contrôler les pages Web affichées dans les différents volets du mode complet du lecteur lorsque vos utilisateurs détachent le contrôle.</span><span class="sxs-lookup"><span data-stu-id="74704-123">If you write custom programs that embed the Windows Media Player control in remote mode, you can also control the webpages displayed in the various panes of the full mode of the Player when your users undock the control.</span></span> <span data-ttu-id="74704-124">Cela vous permet de préserver la continuité entre les États ancrés et non ancrés.</span><span class="sxs-lookup"><span data-stu-id="74704-124">This lets you preserve continuity between the docked and undocked states.</span></span>

## <a name="web-embedding"></a><span data-ttu-id="74704-125">Incorporation de sites Web</span><span class="sxs-lookup"><span data-stu-id="74704-125">Web Embedding</span></span>

<span data-ttu-id="74704-126">Vous pouvez utiliser le contrôle du lecteur Windows Media dans le cadre d’une page Web que vous créez.</span><span class="sxs-lookup"><span data-stu-id="74704-126">You can use the Windows Media Player control as part of a webpage you create.</span></span> <span data-ttu-id="74704-127">Consultez [incorporation du contrôle du lecteur Windows Media dans une page Web](embedding-the-windows-media-player-control-in-a-web-page.md).</span><span class="sxs-lookup"><span data-stu-id="74704-127">See [Embedding the Windows Media Player Control in a Web Page](embedding-the-windows-media-player-control-in-a-web-page.md).</span></span>

## <a name="script-commands-and-url-flipping"></a><span data-ttu-id="74704-128">Commandes de script et retournement d’URL</span><span class="sxs-lookup"><span data-stu-id="74704-128">Script Commands and URL Flipping</span></span>

<span data-ttu-id="74704-129">Les commandes de script sont des paires texte/valeur que vous pouvez incorporer dans vos fichiers multimédias numériques ou vos flux.</span><span class="sxs-lookup"><span data-stu-id="74704-129">Script commands are text/value pairs you can embed in your digital media files or streams.</span></span> <span data-ttu-id="74704-130">Vous pouvez utiliser des commandes de script personnalisées uniquement pour déclencher le code de script, tout en laissant le lecteur Windows Media gérer automatiquement les autres commandes de script.</span><span class="sxs-lookup"><span data-stu-id="74704-130">You might use custom script commands solely to trigger script code, while letting Windows Media Player handle other script commands automatically.</span></span>

<span data-ttu-id="74704-131">Si vous disposez de plusieurs pages Web qui accompagnent une présentation multimédia numérique, les commandes de script d’URL peuvent automatiquement modifier la page dans un cadre, tandis que le contrôle du lecteur Windows Media continue la lecture des médias numériques dans une autre image.</span><span class="sxs-lookup"><span data-stu-id="74704-131">When you have several webpages that accompany a digital media presentation, URL script commands can automatically change the page in one frame while the Windows Media Player control continues playing digital media in another frame.</span></span> <span data-ttu-id="74704-132">C’est ce que l’on appelle le basculement d’URL et est un excellent moyen de créer un diaporama multimédia.</span><span class="sxs-lookup"><span data-stu-id="74704-132">This is called URL flipping, and is an excellent way to create a multimedia slide show.</span></span> <span data-ttu-id="74704-133">D’autres commandes de script gérées automatiquement vous permettent de basculer la lecture vers un fichier ou un flux de média différent, d’afficher du texte de sous-titrage ou de déclencher des événements tels que des insertions de publicités définies dans une sélection de métafichiers Windows Media.</span><span class="sxs-lookup"><span data-stu-id="74704-133">Other automatically handled script commands let you switch playback to a different media file or stream, display captioning text, or trigger events such as ad insertions defined in a Windows Media metafile playlist.</span></span>

<span data-ttu-id="74704-134">Pour plus d’informations sur le basculement d’URL, consultez [création de présentations Web-Based](creating-web-based-presentations.md).</span><span class="sxs-lookup"><span data-stu-id="74704-134">For more information about URL flipping, see [Creating Web-Based Presentations](creating-web-based-presentations.md).</span></span>

## <a name="rich-media-streaming"></a><span data-ttu-id="74704-135">Diffusion multimédia enrichie</span><span class="sxs-lookup"><span data-stu-id="74704-135">Rich Media Streaming</span></span>

<span data-ttu-id="74704-136">Le basculement d’URL fonctionne mieux avec les pages simples qui sont chargées rapidement.</span><span class="sxs-lookup"><span data-stu-id="74704-136">URL flipping works best with simple pages that load rapidly.</span></span> <span data-ttu-id="74704-137">Avec des pages plus complexes, plusieurs composants sont transférés individuellement, ce qui complique la synchronisation de l’affichage des pages avec des médias numériques.</span><span class="sxs-lookup"><span data-stu-id="74704-137">With more complex pages, multiple components are transferred individually, making it difficult to synchronize page display with digital media.</span></span> <span data-ttu-id="74704-138">Pour permettre des présentations multimédias complexes, des pages Web peuvent être ajoutées à un flux multimédia et transmises au lecteur de la même façon que des données audio et vidéo.</span><span class="sxs-lookup"><span data-stu-id="74704-138">To allow complex rich media presentations, webpages can be added to a media stream and delivered to the Player in the same way as audio and video.</span></span> <span data-ttu-id="74704-139">Cela vous permet de synchroniser les composants de votre présentation beaucoup plus facilement, en particulier sur les connexions à faible vitesse.</span><span class="sxs-lookup"><span data-stu-id="74704-139">This lets you synchronize the components of your presentation much more easily, especially over low-speed connections.</span></span>

<span data-ttu-id="74704-140">Pour plus d’informations sur la diffusion multimédia en continu, consultez [création de présentations Web-Based](creating-web-based-presentations.md).</span><span class="sxs-lookup"><span data-stu-id="74704-140">For more information about rich media streaming, see [Creating Web-Based Presentations](creating-web-based-presentations.md).</span></span>

## <a name="browser-support"></a><span data-ttu-id="74704-141">Prise en charge des navigateurs</span><span class="sxs-lookup"><span data-stu-id="74704-141">Browser Support</span></span>

<span data-ttu-id="74704-142">Vous pouvez incorporer le contrôle du lecteur Windows Media dans Microsoft Internet Explorer, Firefox et Netscape Navigator, bien que le processus soit légèrement différent pour chacun.</span><span class="sxs-lookup"><span data-stu-id="74704-142">You can embed the Windows Media Player control in Microsoft Internet Explorer, Firefox, and Netscape Navigator, although the process is slightly different for each.</span></span> <span data-ttu-id="74704-143">Vous pouvez également créer des pages Web conçues pour fonctionner avec les trois navigateurs.</span><span class="sxs-lookup"><span data-stu-id="74704-143">You can also create webpages designed to work with all three browsers.</span></span>

<span data-ttu-id="74704-144">Avec Internet Explorer et Firefox, vous incorporez le contrôle à l’aide de l’élément objet HTML.</span><span class="sxs-lookup"><span data-stu-id="74704-144">With Internet Explorer and Firefox, you embed the control using the HTML OBJECT element.</span></span> <span data-ttu-id="74704-145">Le navigateur requiert toutefois une approche différente, car il ne prend pas directement en charge les contrôles ActiveX.</span><span class="sxs-lookup"><span data-stu-id="74704-145">Navigator requires a different approach, however, because it doesn't directly support ActiveX controls.</span></span> <span data-ttu-id="74704-146">Avec Navigator, vous utilisez l’élément APPLET pour incorporer une applet Java spéciale dans la page.</span><span class="sxs-lookup"><span data-stu-id="74704-146">With Navigator, you use the APPLET element to embed a special Java applet into the page.</span></span> <span data-ttu-id="74704-147">Cette applet gère la communication avec le contrôle ActiveX Player.</span><span class="sxs-lookup"><span data-stu-id="74704-147">This applet handles communication with the Player ActiveX control.</span></span>

<span data-ttu-id="74704-148">Pour plus d’informations sur la prise en charge de Firefox, consultez [utilisation du contrôle du lecteur Windows Media avec Firefox](using-the-windows-media-player-control-with-firefox.md).</span><span class="sxs-lookup"><span data-stu-id="74704-148">For more information about Firefox support, see [Using the Windows Media Player Control with Firefox](using-the-windows-media-player-control-with-firefox.md).</span></span>

<span data-ttu-id="74704-149">Pour plus d’informations sur la prise en charge de Netscape Navigator, consultez [utilisation du lecteur Windows Media avec netscape 7,1](using-windows-media-player-with-netscape-7-1.md).</span><span class="sxs-lookup"><span data-stu-id="74704-149">For more information about Netscape Navigator support, see [Using Windows Media Player with Netscape 7.1](using-windows-media-player-with-netscape-7-1.md).</span></span>

## <a name="displaying-web-pages-in-the-full-mode-of-the-player"></a><span data-ttu-id="74704-150">Affichage des pages Web en mode complet du lecteur</span><span class="sxs-lookup"><span data-stu-id="74704-150">Displaying Web Pages in the Full Mode of the Player</span></span>

<span data-ttu-id="74704-151">Vous pouvez étendre les fonctionnalités du lecteur Windows Media ou fournir une vue personnalisée des informations qui accompagnent vos médias numériques en affichant des pages Web en mode complet du lecteur.</span><span class="sxs-lookup"><span data-stu-id="74704-151">You can extend the functionality of Windows Media Player or provide a custom view of information that accompanies your digital media by displaying webpages in the full mode of the Player.</span></span> <span data-ttu-id="74704-152">Il s’agit de la fonctionnalité HTMLView des fichiers Windows Media.</span><span class="sxs-lookup"><span data-stu-id="74704-152">This is the HTMLView feature of Windows Media metafiles.</span></span> <span data-ttu-id="74704-153">Les fichiers de données vous offrent un contrôle parfait sur le contenu de la sélection, ce qui vous permet de passer en toute transparence entre les clips, d’insérer des publications et d’afficher des images fixes dans le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="74704-153">Metafiles give you great control over playlist content, allowing you to seamlessly transition between clips, insert advertisements, and display still images in Windows Media Player.</span></span> <span data-ttu-id="74704-154">Pour afficher les pages Web en mode complet du lecteur, vous utilisez l’élément PARAM pour ajouter des références d’URL à vos entrées de playlist ou à des sélections entières.</span><span class="sxs-lookup"><span data-stu-id="74704-154">To display webpages in the full mode of the Player, you use the PARAM element to add URL references to your playlist entries or to entire playlists.</span></span>

<span data-ttu-id="74704-155">Pour plus d’informations sur l’utilisation des pages Web dans les sous-fichiers, consultez [affichage de pages Web dans le lecteur Windows Media](displaying-web-pages-in-windows-media-player.md).</span><span class="sxs-lookup"><span data-stu-id="74704-155">For more information about using webpages in metafiles, see [Displaying Web Pages in Windows Media Player](displaying-web-pages-in-windows-media-player.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="74704-156">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="74704-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74704-157">**À propos du modèle objet Player**</span><span class="sxs-lookup"><span data-stu-id="74704-157">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> </dl>

 

 




