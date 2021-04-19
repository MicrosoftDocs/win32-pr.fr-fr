---
title: À propos de la bibliothèque
description: À propos de la bibliothèque
ms.assetid: a43c57ac-deb4-4c86-a8a2-bcfd214b9d0a
keywords:
- Lecteur Windows Media, bibliothèque
- Modèle objet du lecteur Windows Media, bibliothèque
- modèle objet, bibliothèque
- Contrôle ActiveX du lecteur Windows Media, bibliothèque pour le modèle objet
- Contrôle ActiveX, bibliothèque pour le modèle objet
- Windows Media Player Mobile contrôle ActiveX, bibliothèque pour le modèle objet
- Windows Media Player Mobile, bibliothèque pour le modèle objet
- Bibliothèque du lecteur Windows Media, à propos de
- bibliothèque, à propos de
- métadonnées, bibliothèque du lecteur Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1781329a78bcb2e9cb25c45135e03465b9d63df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509779"
---
# <a name="about-the-library"></a><span data-ttu-id="51021-113">À propos de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="51021-113">About the Library</span></span>

<span data-ttu-id="51021-114">La bibliothèque est une base de données d’informations, ou *métadonnées*, sur le contenu multimédia numérique disponible pour le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="51021-114">The library is a database of information, or *metadata*, about the digital media content that is available to Windows Media Player.</span></span> <span data-ttu-id="51021-115">Certaines des informations s’affichent dans le volet **bibliothèque** du lecteur. une plus grande disponibilité est disponible par le biais du code.</span><span class="sxs-lookup"><span data-stu-id="51021-115">Some of the information is displayed in the **Library** pane in the Player; more of it is available through code.</span></span>

<span data-ttu-id="51021-116">(Dans le lecteur Windows Media série 9 et versions antérieures, cette fonctionnalité est appelée **bibliothèque multimédia**.)</span><span class="sxs-lookup"><span data-stu-id="51021-116">(In Windows Media Player 9 Series and earlier, this feature is called **Media Library**.)</span></span>

<span data-ttu-id="51021-117">La bibliothèque offre aux utilisateurs un moyen simple d’organiser et d’accéder à du contenu multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="51021-117">The library gives users an easy way to organize and access digital media content.</span></span> <span data-ttu-id="51021-118">Par exemple, les utilisateurs peuvent afficher la musique organisée par album, par artiste, par genre ou simplement comme une liste de toutes les musiques.</span><span class="sxs-lookup"><span data-stu-id="51021-118">For example, users can view music organized by album, by artist, by genre, or simply as a list of all music.</span></span> <span data-ttu-id="51021-119">Vous pouvez utiliser le modèle objet du kit de développement logiciel (SDK) du lecteur Windows Media pour accéder à la bibliothèque et lire du contenu, récupérer des sélections, ajouter du contenu, supprimer du contenu et modifier les métadonnées associées.</span><span class="sxs-lookup"><span data-stu-id="51021-119">You can use the Windows Media Player SDK object model to access the library to play content, retrieve playlists, add content, remove content, and change the associated metadata.</span></span> <span data-ttu-id="51021-120">Le lecteur Windows Media protège la confidentialité des utilisateurs en restreignant votre capacité à accéder à la bibliothèque à partir du code sous certaines conditions.</span><span class="sxs-lookup"><span data-stu-id="51021-120">Windows Media Player protects users' privacy by restricting your ability to access the library from code under certain conditions.</span></span> <span data-ttu-id="51021-121">Pour plus d’informations sur les droits d’accès, consultez accès à la [bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="51021-121">For more information about access rights, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="51021-122">La bibliothèque stocke les métadonnées sur deux types de contenu multimédia numérique de base.</span><span class="sxs-lookup"><span data-stu-id="51021-122">The library stores metadata about two basic types of digital media content.</span></span> <span data-ttu-id="51021-123">Le premier type, les éléments multimédias numériques, sont des fichiers de contenu individuels, tels qu’une piste musicale ou une photo.</span><span class="sxs-lookup"><span data-stu-id="51021-123">The first type, digital media items, are individual content files, such as a music track or a photo.</span></span> <span data-ttu-id="51021-124">Le deuxième type, les sélections, sont des fichiers qui représentent un groupe d’éléments multimédias numériques, généralement destinés à être lus dans un ordre spécifié.</span><span class="sxs-lookup"><span data-stu-id="51021-124">The second type, playlists, are files that represent a group of digital media items, typically intended to be played in a specified order.</span></span> <span data-ttu-id="51021-125">Les métadonnées associées au contenu multimédia numérique sont stockées en tant que paires nom-valeur.</span><span class="sxs-lookup"><span data-stu-id="51021-125">The metadata associated with digital media content is stored as name-value pairs.</span></span> <span data-ttu-id="51021-126">Par exemple, les métadonnées qui décrivent la personne qui a effectué une chanson sont nommées « Artist » et la valeur qui lui est associée est généralement une chaîne de texte contenant le nom de l’artiste.</span><span class="sxs-lookup"><span data-stu-id="51021-126">For example, the metadata that describes the person who performed a song is named "Artist" and the value associated with it typically is a text string containing the performer's name.</span></span> <span data-ttu-id="51021-127">Chaque nom de métadonnées unique est appelé *attribut*.</span><span class="sxs-lookup"><span data-stu-id="51021-127">Each unique metadata name is called an *attribute*.</span></span> <span data-ttu-id="51021-128">Pour obtenir la liste des attributs pris en charge, consultez la [référence d’attribut](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="51021-128">For a listing of supported attributes, see the [Attribute Reference](attribute-reference.md).</span></span> <span data-ttu-id="51021-129">Pour plus d’informations sur l’utilisation d’attributs dans le code, consultez [attributs d’élément multimédia](media-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="51021-129">For information about using attributes in code, see [Media Item Attributes](media-item-attributes.md).</span></span>

<span data-ttu-id="51021-130">Les sections suivantes fournissent plus d’informations sur l’utilisation de la bibliothèque :</span><span class="sxs-lookup"><span data-stu-id="51021-130">The following sections provide more information about working with the library:</span></span>

-   [<span data-ttu-id="51021-131">Accès à la bibliothèque par programmation</span><span class="sxs-lookup"><span data-stu-id="51021-131">Accessing the Library Programmatically</span></span>](accessing-the-library-programmatically.md)
-   [<span data-ttu-id="51021-132">À propos des services de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="51021-132">About Library Services</span></span>](about-library-services.md)

## <a name="related-topics"></a><span data-ttu-id="51021-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="51021-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51021-134">**À propos du modèle objet Player**</span><span class="sxs-lookup"><span data-stu-id="51021-134">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> </dl>

 

 




