---
title: Sélections statiques et automatiques
description: Sélections statiques et automatiques
ms.assetid: 708c236e-8f3c-4188-aefb-eda7da598944
keywords:
- Lecteur Windows Media, sélections
- Modèle objet du lecteur Windows Media, sélections
- modèle objet, sélections
- Windows Media Player Mobile, sélections
- Contrôle ActiveX du lecteur Windows Media, sélections
- Contrôle ActiveX mobile du lecteur Windows Media, sélections
- Contrôle ActiveX, sélections
- sélections, statiques
- sélections de métafichiers, statiques
- Sélections de métafichiers Windows Media, statiques
- sélections statiques
- sélections automatiques
- sélections, auto
- sélections de métafichiers, auto
- Sélections de métafichiers Windows Media, auto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 083ee2029eec2cfee7510766790f4ca7eb6468e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379687"
---
# <a name="static-and-auto-playlists"></a><span data-ttu-id="aa6ee-118">Sélections statiques et automatiques</span><span class="sxs-lookup"><span data-stu-id="aa6ee-118">Static and Auto Playlists</span></span>

<span data-ttu-id="aa6ee-119">Il existe deux types de sélections :</span><span class="sxs-lookup"><span data-stu-id="aa6ee-119">There are two types of playlists:</span></span>

-   <span data-ttu-id="aa6ee-120">Sélections statiques, qui incluent des éléments multimédias spécifiques</span><span class="sxs-lookup"><span data-stu-id="aa6ee-120">Static playlists, which include specific media items</span></span>
-   <span data-ttu-id="aa6ee-121">Les sélections automatiques, qui recherchent la bibliothèque à chaque ouverture et peuvent contenir différents éléments multimédias à des moments différents.</span><span class="sxs-lookup"><span data-stu-id="aa6ee-121">Auto playlists, which search the library every time they are opened and may contain different media items at different times.</span></span> <span data-ttu-id="aa6ee-122">Une sélection automatique est le résultat d’une requête de base de données.</span><span class="sxs-lookup"><span data-stu-id="aa6ee-122">An auto playlist is the result of a database query.</span></span>

<span data-ttu-id="aa6ee-123">Pour importer une playlist statique à partir d’un métafichier, appelez tout d’abord le *joueur*. **newPlaylist** pour créer un objet **playlist** basé sur les données du métafichier, puis passer cet objet à *PlaylistCollection*. **importPlaylist** pour ajouter la sélection à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="aa6ee-123">To import a static playlist from a metafile, first call *Player*.**newPlaylist** to create a **Playlist** object based on the data in the metafile, and then pass that object to *PlaylistCollection*.**importPlaylist** to add the playlist to the library.</span></span>

<span data-ttu-id="aa6ee-124">Pour importer une sélection automatique à partir d’un métafichier, utilisez *MediaCollection*. **Ajoutez**.</span><span class="sxs-lookup"><span data-stu-id="aa6ee-124">To import an auto playlist from a metafile, use *MediaCollection*.**add**.</span></span> <span data-ttu-id="aa6ee-125">Pour plus d’informations, consultez [playlists et l’objet MediaCollection](playlists-and-the-mediacollection-object.md).</span><span class="sxs-lookup"><span data-stu-id="aa6ee-125">For more information, see [Playlists and the MediaCollection Object](playlists-and-the-mediacollection-object.md).</span></span>

<span data-ttu-id="aa6ee-126">Pour importer une sélection statique à partir d’un métafichier de sélection automatique, utilisez le *lecteur*. **newPlaylist** et *PlaylistCollection*. **importPlaylist** comme décrit précédemment.</span><span class="sxs-lookup"><span data-stu-id="aa6ee-126">To import a static playlist from an auto playlist metafile, use *Player*.**newPlaylist** and *PlaylistCollection*.**importPlaylist** as described earlier.</span></span> <span data-ttu-id="aa6ee-127">La sélection automatique est exécutée une fois et une sélection statique est créée en fonction du résultat de cette exécution.</span><span class="sxs-lookup"><span data-stu-id="aa6ee-127">The auto playlist will be executed once and a static playlist will be created based on the result of that execution.</span></span>

<span data-ttu-id="aa6ee-128">L’utilisation d’une sélection automatique pour interroger la bibliothèque de l’utilisateur n’est pas prise en charge pour les pages Web auxquelles les utilisateurs accèdent via Internet.</span><span class="sxs-lookup"><span data-stu-id="aa6ee-128">Using an auto playlist to query the user's library is not supported for webpages that users access over the Internet.</span></span>

<span data-ttu-id="aa6ee-129">L’exemple de code C# suivant illustre l’importation d’un métafichier de sélection automatique en tant que sélection statique.</span><span class="sxs-lookup"><span data-stu-id="aa6ee-129">The following C# example code demonstrates importing an auto playlist metafile as a static playlist.</span></span> <span data-ttu-id="aa6ee-130">Pour exécuter cet exemple, créez une sélection automatique à l’aide de l’interface utilisateur de la bibliothèque, puis incluez le chemin d’accès correct au métafichier de sélection automatique dans ce code.</span><span class="sxs-lookup"><span data-stu-id="aa6ee-130">To run this sample, create an auto playlist by using the library user interface, and then include the correct path to the auto playlist metafile in this code.</span></span>


```C++
private void addStaticPlaylist()
{
    IWMPPlaylist pList;

    pList = Player.newPlaylist("NewImportedList", "\\\\myServer\\myPath\\artistcollection.wpl");
    if (pList.count == 0)
        MessageBox.Show("The specified playlist is empty.");
    else
        Player.playlistCollection.importPlaylist(pList);
}

```



## <a name="related-topics"></a><span data-ttu-id="aa6ee-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="aa6ee-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa6ee-132">**Gestion des sélections**</span><span class="sxs-lookup"><span data-stu-id="aa6ee-132">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> </dl>

 

 




