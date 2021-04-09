---
title: Modification de l’affichage
description: Modification de l’affichage
ms.assetid: 21d68a34-d3d8-4b5b-b8fe-0489dc6247ec
keywords:
- Sélections de métafichiers Windows Media, modification des affichages
- sélections, modification d’affichages
- sélections de métafichiers, modification des affichages
- Sélections de métafichiers Windows Media, modification de l’affichage
- sélections, modification de l’affichage
- sélections de métafichiers, modification d’affichage
- Lecteur Windows Media, modification de l’affichage
- Lecteur Windows Media, modification des affichages
- Windows Media Player, propriétés de texte
- Windows Media Player, propriétés de l’image
- Windows Media Player, propriétés MOREINFO
- Lecteur Windows Media, texte abstrait
- Propriétés MOREINFO
- Texte abstrait
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5c36c55b455b797446cde627449ea705b3bd2ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028996"
---
# <a name="modifying-the-display"></a><span data-ttu-id="e163a-117">Modification de l’affichage</span><span class="sxs-lookup"><span data-stu-id="e163a-117">Modifying the Display</span></span>

<span data-ttu-id="e163a-118">Les sélections peuvent modifier l’interface utilisateur du lecteur Windows Media de quatre manières principales :</span><span class="sxs-lookup"><span data-stu-id="e163a-118">Playlists can alter the Windows Media Player user interface in four main ways:</span></span>

-   <span data-ttu-id="e163a-119">Propriétés du texte</span><span class="sxs-lookup"><span data-stu-id="e163a-119">Text properties</span></span>
-   <span data-ttu-id="e163a-120">Propriétés de l’image</span><span class="sxs-lookup"><span data-stu-id="e163a-120">Image properties</span></span>
-   <span data-ttu-id="e163a-121">Propriétés MOREINFO</span><span class="sxs-lookup"><span data-stu-id="e163a-121">MOREINFO properties</span></span>
-   <span data-ttu-id="e163a-122">Texte abstrait</span><span class="sxs-lookup"><span data-stu-id="e163a-122">ABSTRACT text</span></span>

## <a name="text-properties"></a><span data-ttu-id="e163a-123">Propriétés du texte</span><span class="sxs-lookup"><span data-stu-id="e163a-123">Text properties</span></span>

<span data-ttu-id="e163a-124">Le lecteur Windows Media permet d’afficher le titre, l’auteur, le Copyright et le texte des métadonnées de description.</span><span class="sxs-lookup"><span data-stu-id="e163a-124">Windows Media Player enables the display of Title, Author, Copyright, and Description metadata text.</span></span> <span data-ttu-id="e163a-125">Les métadonnées de clip peuvent provenir du flux ou du fichier multimédia, ou elles peuvent provenir d’une sélection.</span><span class="sxs-lookup"><span data-stu-id="e163a-125">Clip metadata can come from the stream or media file, or it can come from a playlist.</span></span> <span data-ttu-id="e163a-126">Afficher les métadonnées proviennent de la playlist.</span><span class="sxs-lookup"><span data-stu-id="e163a-126">Show metadata comes from the playlist.</span></span> <span data-ttu-id="e163a-127">En général, les sélections sont une meilleure méthode de transmission des propriétés de texte au lecteur Windows Media, en particulier si les éléments de texte sont susceptibles d’être modifiés.</span><span class="sxs-lookup"><span data-stu-id="e163a-127">In general, playlists are a better method of passing text properties to Windows Media Player, especially if text elements are likely to change.</span></span> <span data-ttu-id="e163a-128">Il est plus facile de modifier le texte d’une sélection que de recréer un fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="e163a-128">It is easier to edit text in a playlist than to re-author a media file.</span></span> <span data-ttu-id="e163a-129">Et étant donné que les propriétés lues à partir d’une sélection remplacent celles contenues dans le fichier multimédia, vous pouvez facilement mettre à jour le texte affiché en ajoutant le nouveau texte à la propriété correspondante dans une sélection.</span><span class="sxs-lookup"><span data-stu-id="e163a-129">And because properties read from a playlist override those contained in the media file, you can easily update display text by adding the new text to the corresponding property in a playlist.</span></span> <span data-ttu-id="e163a-130">Dans l’exemple suivant, le texte du titre et les métadonnées de l’auteur de la sélection remplace le titre et le texte de l’auteur contenu dans le fichier multimédia, Sample. WMA.</span><span class="sxs-lookup"><span data-stu-id="e163a-130">In the following example, the text of the Title and Author metadata in the playlist overrides the Title and Author text contained in the media file, sample.wma.</span></span>

<span data-ttu-id="e163a-131">Le texte de **Description** est récupéré à partir d’un fichier Windows Media référencé dans un élément **entry** , sauf s’il existe un élément **abstract** dans une sélection de métafichiers.</span><span class="sxs-lookup"><span data-stu-id="e163a-131">**DESCRIPTION** text is retrieved from a Windows Media file referenced in an **ENTRY** element unless there is an **ABSTRACT** element in a metafile playlist.</span></span> <span data-ttu-id="e163a-132">S’il y a du texte **abstrait** , il est affiché, remplaçant le texte de **Description** .</span><span class="sxs-lookup"><span data-stu-id="e163a-132">If there is **ABSTRACT** text, it will be displayed, overriding the **DESCRIPTION** text.</span></span>


```XML
<ASX version="3.0" BANNERBAR="AUTO" >
    <ENTRY>
        <BANNER HREF="YourPath\2.gif">
        </BANNER>
        <TITLE>Upgrade</TITLE>
        <AUTHOR>Ad Department</AUTHOR>
        <REF href="YourPath\sample.wma"/>
    </ENTRY>
</ASX>

```



## <a name="image-properties"></a><span data-ttu-id="e163a-133">Propriétés de l’image</span><span class="sxs-lookup"><span data-stu-id="e163a-133">Image properties</span></span>

<span data-ttu-id="e163a-134">Les images de bannière peuvent être ajoutées à l’interface utilisateur du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e163a-134">Banner images can be added to the user interface of Windows Media Player.</span></span> <span data-ttu-id="e163a-135">Le graphique peut être utilisé pour la publicité, fournir des informations et fournir un accès à des sites Web, pour nommer quelques possibilités.</span><span class="sxs-lookup"><span data-stu-id="e163a-135">The graphic can be used for advertising, providing information, and providing access to websites, to name a few possibilities.</span></span>

<span data-ttu-id="e163a-136">Utilisez l’élément **bannière** pour spécifier une image graphique (32 pixels de haut en 194 pixels de large) à afficher par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e163a-136">Use the **BANNER** element to specify a graphic image (32 pixels high by 194 pixels wide) for display by Windows Media Player.</span></span> <span data-ttu-id="e163a-137">Le graphique est affiché sous tout le contenu de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="e163a-137">The graphic is displayed below any video content.</span></span> <span data-ttu-id="e163a-138">Un lien hypertexte peut être ajouté à la bannière à l’aide de l’élément enfant **moreinfo** .</span><span class="sxs-lookup"><span data-stu-id="e163a-138">A hyperlink can be added to the banner using the **MOREINFO** child element.</span></span>

<span data-ttu-id="e163a-139">Une info-bulle peut être définie par un élément **abstrait** au sein de la portée de l’élément **Banner** .</span><span class="sxs-lookup"><span data-stu-id="e163a-139">A ToolTip can be defined by an **ABSTRACT** element within the scope of the **BANNER** element.</span></span> <span data-ttu-id="e163a-140">Tout texte d’info-bulle défini peut être affiché en plaçant le pointeur de la souris sur le graphique de la bannière.</span><span class="sxs-lookup"><span data-stu-id="e163a-140">Any defined ToolTip text can be displayed by pausing the mouse pointer over the banner graphic.</span></span> <span data-ttu-id="e163a-141">Si vous sélectionnez le graphique de bannière avec le pointeur de la souris, tout lien hypertexte défini avec l’élément **moreinfo** est activé.</span><span class="sxs-lookup"><span data-stu-id="e163a-141">Selecting the banner graphic with the mouse pointer will activate any hyperlink defined with the **MOREINFO** element.</span></span>

<span data-ttu-id="e163a-142">Le format de la **bannière** graphique par défaut est le format GIF.</span><span class="sxs-lookup"><span data-stu-id="e163a-142">The preferred **BANNER** graphics format is the GIF format.</span></span> <span data-ttu-id="e163a-143">Le format JPG peut être utilisé si le graphique est correctement dimensionné.</span><span class="sxs-lookup"><span data-stu-id="e163a-143">The JPG format can be used if the graphic is properly sized.</span></span>

<span data-ttu-id="e163a-144">L’exemple précédent illustre l’utilisation de l’élément **Banner** .</span><span class="sxs-lookup"><span data-stu-id="e163a-144">The previous example illustrates use of the **BANNER** element.</span></span>

> [!Note]  
> <span data-ttu-id="e163a-145">Les images de **bannière** ne sont pas prises en charge avec les fichiers DRM ou lorsque le lecteur Windows Media est incorporé dans une page Web.</span><span class="sxs-lookup"><span data-stu-id="e163a-145">**BANNER** images are not supported with DRM files or when Windows Media Player is embedded in a webpage.</span></span>

 

<span data-ttu-id="e163a-146">Pour plus d’informations sur les bannières, consultez [graphiques personnalisés dans le lecteur Windows Media](custom-graphics-in-windows-media-player.md).</span><span class="sxs-lookup"><span data-stu-id="e163a-146">For more information about banners, see [Custom Graphics in Windows Media Player](custom-graphics-in-windows-media-player.md).</span></span>

## <a name="moreinfo-properties"></a><span data-ttu-id="e163a-147">Propriétés MOREINFO</span><span class="sxs-lookup"><span data-stu-id="e163a-147">MOREINFO properties</span></span>

<span data-ttu-id="e163a-148">Les zones de texte et d’image de l’interface utilisateur peuvent être associées à des URL.</span><span class="sxs-lookup"><span data-stu-id="e163a-148">Text and image areas of the user interface can be associated with URLs.</span></span> <span data-ttu-id="e163a-149">Pendant la lecture, les utilisateurs peuvent sélectionner l’une de ces sections pour se connecter à l’URL qui leur est associée dans leur navigateur Web.</span><span class="sxs-lookup"><span data-stu-id="e163a-149">During playback, users can select one of these sections to connect to the URL associated with it in their Web browser.</span></span> <span data-ttu-id="e163a-150">Par exemple, vous pouvez associer le site Web d’un annonceur à une image de bannière ad, comme illustré dans l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="e163a-150">For example, you can associate an advertiser's website with an ad banner image as shown in the following code snippet.</span></span>


```XML
<BANNER HREF="YourPath\2.gif">
    <ABSTRACT>More Information.</ABSTRACT>
    <MOREINFO HREF="https://www.proseware.com" />
</BANNER>

```



## <a name="abstract-text"></a><span data-ttu-id="e163a-151">Texte abstrait</span><span class="sxs-lookup"><span data-stu-id="e163a-151">ABSTRACT text</span></span>

<span data-ttu-id="e163a-152">Le texte **abstrait** est utilisé pour afficher une brève description du texte ou des zones d’image de l’interface utilisateur à laquelle il est associé.</span><span class="sxs-lookup"><span data-stu-id="e163a-152">**ABSTRACT** text is used to display a short pop-up description of the text or image areas of the user interface it is associated with.</span></span> <span data-ttu-id="e163a-153">Pendant la lecture, si le pointeur de la souris se trouve au-dessus de l’une de ces zones, une info-bulle s’affiche à côté du pointeur de la souris qui affiche le texte **abstrait** associé à la zone.</span><span class="sxs-lookup"><span data-stu-id="e163a-153">During playback, if the mouse pointer hovers over one of these areas, a ToolTip appears beside the mouse pointer displaying the **ABSTRACT** text associated with the area.</span></span> <span data-ttu-id="e163a-154">Le texte **abstrait** est récupéré à partir d’un métafichier et est défini avec l’élément **abstrait** .</span><span class="sxs-lookup"><span data-stu-id="e163a-154">**ABSTRACT** text is retrieved from a metafile and is defined with the **ABSTRACT** element.</span></span> <span data-ttu-id="e163a-155">L’élément **abstract** peut être un élément enfant d’un élément d' **entrée** ou de **bannière** .</span><span class="sxs-lookup"><span data-stu-id="e163a-155">The **ABSTRACT** element can be a child element of either an **ENTRY** or a **BANNER** element.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e163a-156">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e163a-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e163a-157">**Sélections de métafichiers**</span><span class="sxs-lookup"><span data-stu-id="e163a-157">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="e163a-158">**Utilisation des sélections de métafichiers**</span><span class="sxs-lookup"><span data-stu-id="e163a-158">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="e163a-159">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="e163a-159">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="e163a-160">**Guide des métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="e163a-160">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




