---
title: Ajout d’un contrôle de lecteur Windows Media incorporé
description: Ajout d’un contrôle de lecteur Windows Media incorporé
ms.assetid: e002bf2a-c51a-448a-80a0-a35d6f32e9c0
keywords:
- Sélections de métafichiers Windows Media, ajout de contrôles de lecteur Windows Media incorporés
- sélections, ajout de contrôles de lecteur Windows Media intégrés
- sélections de métafichiers, ajout de contrôles de lecteur Windows Media incorporés
- Sélections de métafichiers Windows Media, contrôles de lecteur Windows Media intégrés
- sélections, contrôles du lecteur Windows Media intégrés
- sélections de métafichiers, contrôles de lecteur Windows Media intégrés
- ajout de contrôles de lecteur Windows Media incorporés
- contrôles du lecteur Windows Media incorporés
- Lecteur Windows Media, ajout de contrôles incorporés
- Windows Media Player, contrôles incorporés
- HTMLView, ajout de contrôles de lecteur Windows Media intégrés
- HTMLView, contrôles Windows Media Player intégrés
- HTMLView, modèle objet du lecteur Windows Media
- HTMLView, modèle objet Player
- Windows Media Player Object Model, à propos de
- modèle objet, à propos de
- Objet Player
- Windows Media, modèle objet Player
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1dea3b11f59bff2edbcef99f1acda5fd0cfcff46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380144"
---
# <a name="adding-an-embedded-windows-media-player-control"></a><span data-ttu-id="609af-121">Ajout d’un contrôle de lecteur Windows Media incorporé</span><span class="sxs-lookup"><span data-stu-id="609af-121">Adding an Embedded Windows Media Player Control</span></span>

<span data-ttu-id="609af-122">Il existe deux raisons pour lesquelles vous pouvez envisager d’ajouter une instance incorporée du lecteur Windows Media à votre présentation HTMLView.</span><span class="sxs-lookup"><span data-stu-id="609af-122">There are two reasons you might consider adding an embedded instance of Windows Media Player to your HTMLView presentation.</span></span> <span data-ttu-id="609af-123">Tout d’abord, si vous souhaitez afficher du contenu vidéo, vous devez utiliser le contrôle ActiveX du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="609af-123">First, if you want to display video content, you need to use the Windows Media Player ActiveX control.</span></span> <span data-ttu-id="609af-124">Deuxièmement, si vous souhaitez tirer parti des fonctionnalités du modèle objet du lecteur Windows Media à partir de votre page Web HTMLView, vous devez utiliser une instance pour le contrôle du lecteur.</span><span class="sxs-lookup"><span data-stu-id="609af-124">Second, if you want to take advantage of features of the Windows Media Player object model from within your HTMLView webpage, you must use an instance the Player control to do so.</span></span>

## <a name="using-the-player-control-to-display-video-in-htmlview-content"></a><span data-ttu-id="609af-125">Utilisation du contrôle du lecteur pour afficher la vidéo dans le contenu HTMLView</span><span class="sxs-lookup"><span data-stu-id="609af-125">Using the Player control to display video in HTMLView content</span></span>

<span data-ttu-id="609af-126">En règle générale, le lecteur Windows Media affiche la vidéo à l’aide du volet vidéo et visualisation de la fonctionnalité de **lecture** en cours.</span><span class="sxs-lookup"><span data-stu-id="609af-126">Usually, Windows Media Player displays video using the Video and Visualization pane of the **Now Playing** feature.</span></span> <span data-ttu-id="609af-127">Comme HTMLView utilise cette zone pour afficher votre page Web, vous devez fournir une zone d’affichage de vidéo supplémentaire si vous souhaitez que le joueur Lise la vidéo.</span><span class="sxs-lookup"><span data-stu-id="609af-127">Since HTMLView uses this area to display your webpage, you must supply an additional video display area if you want the Player to play video.</span></span> <span data-ttu-id="609af-128">Il est facile de le faire à l’aide du contrôle ActiveX du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="609af-128">This is easy to do by using the Windows Media Player ActiveX control.</span></span>

<span data-ttu-id="609af-129">Pour utiliser le contrôle Player pour afficher une vidéo, incorporez le contrôle dans votre page Web HTMLView à l’aide de la balise **Object** .</span><span class="sxs-lookup"><span data-stu-id="609af-129">To use the Player control to display video, embed the control in your HTMLView webpage by using the **OBJECT** tag.</span></span> <span data-ttu-id="609af-130">Il s’agit de la même technique que celle utilisée pour incorporer le contrôle Player dans une page Web dans laquelle vous souhaitez afficher une vidéo.</span><span class="sxs-lookup"><span data-stu-id="609af-130">This is the same technique you use to embed the Player control into any webpage in which you want to display video.</span></span> <span data-ttu-id="609af-131">L’exemple de code suivant illustre la syntaxe de base pour incorporer le contrôle Player dans Internet Explorer :</span><span class="sxs-lookup"><span data-stu-id="609af-131">The following example code shows the basic syntax for embedding the Player control in Internet Explorer:</span></span>


```XML
<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6"> 
        <PARAM Name = "autoStart"  Value = "true">
        <PARAM Name = "uiMode" Value = "none">
</OBJECT>

```



<span data-ttu-id="609af-132">Le paramètre de *démarrage* automatique garantit que le contenu est lu automatiquement chaque fois qu’une nouvelle URL est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="609af-132">The *autoStart* parameter ensures that content plays automatically whenever a new URL is specified.</span></span> <span data-ttu-id="609af-133">La valeur que vous spécifiez pour *UIMODE* dépend de vous, mais vous souhaiterez généralement spécifier « None » lors de la création de contenu pour les présentations HTMLView.</span><span class="sxs-lookup"><span data-stu-id="609af-133">The value you specify for *uiMode* is up to you, but you will usually want to specify "none" when creating content for HTMLView presentations.</span></span> <span data-ttu-id="609af-134">Lorsque vous incorporez le contrôle du lecteur Windows Media pour afficher la vidéo de cette manière, l’utilisateur peut contrôler la lecture à l’aide des contrôles du lecteur en mode plein. il n’est donc pas nécessaire de fournir des contrôles de transport supplémentaires dans la page Web.</span><span class="sxs-lookup"><span data-stu-id="609af-134">When you embed the Windows Media Player control to display video in this manner, the user can control playback using the controls of the full-mode Player, so there's no need to provide additional transport controls in the webpage.</span></span> <span data-ttu-id="609af-135">Vous pouvez utiliser l’espace que vous allouez habituellement pour les contrôles de transport pour afficher davantage de texte, de graphiques ou de liens vers d’autres contenus.</span><span class="sxs-lookup"><span data-stu-id="609af-135">You can use the space you would usually allocate for transport controls to display more text, graphics, or links to other content.</span></span>

<span data-ttu-id="609af-136">Ne spécifiez pas de paramètre d' *URL* lors de l’incorporation du contrôle du lecteur Windows Media dans une page Web conçue pour s’afficher dans une présentation HTMLView.</span><span class="sxs-lookup"><span data-stu-id="609af-136">Do not specify a *URL* parameter when embedding the Windows Media Player control in a webpage designed to display in an HTMLView presentation.</span></span> <span data-ttu-id="609af-137">Au lieu de cela, spécifiez les fichiers multimédias numériques dans le fichier. asx qui ouvre le contenu.</span><span class="sxs-lookup"><span data-stu-id="609af-137">Instead, specify the digital media files in the .asx file that opens the content.</span></span>

<span data-ttu-id="609af-138">Étant donné que vous fournissez la zone d’affichage vidéo dans votre page Web HTMLView, vous pouvez choisir l’emplacement de la vidéo et la taille de la zone d’affichage.</span><span class="sxs-lookup"><span data-stu-id="609af-138">Because you provide the video display region in your HTMLView webpage, you can decide where to position the video and how large you want the display region to be.</span></span> <span data-ttu-id="609af-139">Par exemple, vous pouvez contenir l’objet **Player** dans un élément **div** html, puis spécifier la position de la **balise div** pour placer l’affichage vidéo sur la page Web.</span><span class="sxs-lookup"><span data-stu-id="609af-139">For example, you can contain the **Player** object within an HTML **DIV** element and then specify the position for the **DIV** to situate the video display on the webpage.</span></span> <span data-ttu-id="609af-140">Vous pouvez modifier les dimensions de l’affichage vidéo en spécifiant des valeurs pour les attributs de hauteur et de largeur de l’élément **objet** .</span><span class="sxs-lookup"><span data-stu-id="609af-140">You can change the dimensions of the video display by specifying values for the height and width attributes of the **OBJECT** element.</span></span> <span data-ttu-id="609af-141">Vous pouvez également spécifier ces valeurs à l’aide du code de script.</span><span class="sxs-lookup"><span data-stu-id="609af-141">You can also specify these values using script code.</span></span>

## <a name="using-the-player-object-model"></a><span data-ttu-id="609af-142">Utilisation du modèle objet Player</span><span class="sxs-lookup"><span data-stu-id="609af-142">Using the Player object model</span></span>

<span data-ttu-id="609af-143">Le modèle objet du lecteur Windows Media expose des propriétés, des méthodes et des événements que vous pouvez utiliser dans vos pages Web HTMLView.</span><span class="sxs-lookup"><span data-stu-id="609af-143">The Windows Media Player object model exposes properties, methods, and events that you can use in your HTMLView webpages.</span></span> <span data-ttu-id="609af-144">Lorsque vous incorporez le contrôle ActiveX du lecteur Windows Media dans votre page Web HTMLView, vous avez automatiquement accès au modèle objet du lecteur.</span><span class="sxs-lookup"><span data-stu-id="609af-144">When you embed the Windows Media Player ActiveX control in your HTMLView webpage, you automatically have access to the Player object model.</span></span>

<span data-ttu-id="609af-145">Si vous incorporez le contrôle du lecteur Windows Media dans votre page Web HTMLView, n’utilisez pas le modèle objet de lecteur pour spécifier le fichier multimédia numérique à lire.</span><span class="sxs-lookup"><span data-stu-id="609af-145">If you embed the Windows Media Player control in your HTMLView webpage, do not use the Player object model to specify the digital media file to be played.</span></span> <span data-ttu-id="609af-146">Par exemple, si vous utilisez le code de script pour spécifier une valeur pour la propriété **URL** du contrôle incorporé, votre page Web HTMLView est déchargée de la fonctionnalité de **lecture** en cours lors de la lecture du fichier multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="609af-146">For example, if you use script code to specify a value for the **URL** property of the embedded control, your HTMLView webpage will be unloaded from the **Now Playing** feature when the digital media file plays.</span></span> <span data-ttu-id="609af-147">Pour éviter cela, ouvrez toujours les fichiers. asx qui incluent des paramètres HTMLView quand vous devez utiliser un script pour ouvrir le contenu multimédia numérique à partir de votre page Web HTMLView.</span><span class="sxs-lookup"><span data-stu-id="609af-147">To prevent this from happening, always open .asx files that include HTMLView parameters when you need to use script to open digital media content from your HTMLView webpage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="609af-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="609af-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="609af-149">**Affichage des pages Web dans le lecteur Windows Media**</span><span class="sxs-lookup"><span data-stu-id="609af-149">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="609af-150">**Player. uiMode**</span><span class="sxs-lookup"><span data-stu-id="609af-150">**Player.uiMode**</span></span>](player-uimode.md)
</dt> <dt>

[<span data-ttu-id="609af-151">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="609af-151">**Player.URL**</span></span>](player-url.md)
</dt> <dt>

[<span data-ttu-id="609af-152">**Paramètres. démarrage automatique**</span><span class="sxs-lookup"><span data-stu-id="609af-152">**Settings.autoStart**</span></span>](settings-autostart.md)
</dt> </dl>

 

 




