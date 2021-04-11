---
title: Fonctionnement des packages de téléchargement Windows Media (déconseillé)
description: Fonctionnement des packages de téléchargement Windows Media (déconseillé)
ms.assetid: 8bab1764-93da-4abc-a8b7-17bc44b381ce
keywords:
- Fichiers Windows Media, packages de téléchargement Windows Media
- Windows Media Player, packages de téléchargement Windows Media
- sous-fichiers, packages de téléchargement Windows Media
- Windows Media, packages de téléchargement Windows Media
- Packages de téléchargement Windows Media, à propos de
- Packages de téléchargement Windows Media, mode de fonctionnement des packages
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1db477791bb93cd599dcef38a90b230c6cd7ddde
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100680"
---
# <a name="how-windows-media-download-packages-work-deprecated"></a><span data-ttu-id="62643-109">Fonctionnement des packages de téléchargement Windows Media (déconseillé)</span><span class="sxs-lookup"><span data-stu-id="62643-109">How Windows Media Download Packages Work (deprecated)</span></span>

<span data-ttu-id="62643-110">Cette page décrit une fonctionnalité qui peut ne pas être disponible dans les versions ultérieures du lecteur Windows Media et du kit de développement logiciel (SDK) du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="62643-110">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="62643-111">Un package de téléchargement Windows Media est lancé à partir d’un site Web lorsqu’un utilisateur clique sur un lien dans un navigateur Web, tel que Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="62643-111">A Windows Media Download package is launched from a website when a user clicks a link in a Web browser, such as Microsoft Internet Explorer.</span></span> <span data-ttu-id="62643-112">Cette action ouvre le lecteur Windows Media, puis télécharge et décompresse le package de téléchargement Windows Media sur le disque dur de l’utilisateur dans un dossier par défaut.</span><span class="sxs-lookup"><span data-stu-id="62643-112">This action opens Windows Media Player and then downloads and un-packages the Windows Media Download package on the user's hard disk in a default folder.</span></span>

<span data-ttu-id="62643-113">Une fois que les fichiers ont été extraits du package de téléchargement Windows Media, le lecteur Windows Media localise une sélection de métafichiers Windows Media avec une extension de nom de fichier. asx parmi les fichiers empaquetés.</span><span class="sxs-lookup"><span data-stu-id="62643-113">Once the files have been extracted from the Windows Media Download package, Windows Media Player locates a Windows Media metafile playlist with an .asx file name extension among the packaged files.</span></span> <span data-ttu-id="62643-114">S’il en trouve un, le lecteur crée une sélection basée sur le métafichier inclus.</span><span class="sxs-lookup"><span data-stu-id="62643-114">If it finds one, the Player creates a playlist based on the included metafile.</span></span> <span data-ttu-id="62643-115">Les fichiers qui contiennent du contenu multimédia sont ensuite ajoutés à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="62643-115">Files that contain multimedia content are then added to the library.</span></span>

<span data-ttu-id="62643-116">Le lecteur Windows Media recherche également un élément d' **apparence** dans le métafichier.</span><span class="sxs-lookup"><span data-stu-id="62643-116">Windows Media Player also looks for a **SKIN** element in the metafile.</span></span> <span data-ttu-id="62643-117">Si l’élément d' **apparence** contient une référence à un fichier de bordure avec l’extension de nom de fichier. WMZ, le joueur charge la bordure dans le volet de **lecture en cours** .</span><span class="sxs-lookup"><span data-stu-id="62643-117">If the **SKIN** element contains a reference to a border file with a .wmz file name extension, the Player loads the border into the **Now Playing** pane.</span></span> <span data-ttu-id="62643-118">Le lecteur commence ensuite à lire le contenu fourni dans le package.</span><span class="sxs-lookup"><span data-stu-id="62643-118">The Player then starts to play the content provided in the package.</span></span>

<span data-ttu-id="62643-119">Le diagramme suivant montre comment le contenu est empaqueté dans un fichier de téléchargement Windows Media, publié sur un site Web, téléchargé et lu sur un ordinateur client à l’aide du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="62643-119">The following diagram shows how content is packaged in a Windows Media Download file, posted to a website, downloaded, and played on a client computer using Windows Media Player.</span></span>

![obtention et lecture d’un fichier de téléchargement Windows Media.](images/wmd-image.png) <span data-ttu-id="62643-121">Téléchargement Windows Media</span><span class="sxs-lookup"><span data-stu-id="62643-121">Windows Media Download</span></span>

<span data-ttu-id="62643-122">Le tableau suivant décrit les trois éléments qui composent un package de téléchargement Windows Media.</span><span class="sxs-lookup"><span data-stu-id="62643-122">The following table describes the three elements that make up a Windows Media Download package.</span></span>



| <span data-ttu-id="62643-123">Élément package</span><span class="sxs-lookup"><span data-stu-id="62643-123">Package element</span></span>    | <span data-ttu-id="62643-124">Fonction</span><span class="sxs-lookup"><span data-stu-id="62643-124">Function</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="62643-125">Extensions de nom de fichier</span><span class="sxs-lookup"><span data-stu-id="62643-125">File name extensions</span></span>                     |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span data-ttu-id="62643-126">Bordure</span><span class="sxs-lookup"><span data-stu-id="62643-126">Border</span></span>             | <span data-ttu-id="62643-127">Interface utilisateur personnalisée et fixe créée par le propriétaire du contenu pour l’affichage, la liaison et la diffusion de tous les supports empaquetés dans le package de téléchargement Windows Media.</span><span class="sxs-lookup"><span data-stu-id="62643-127">A fixed, customized user interface created by the content owner for displaying, linking, and playing all media packaged in the Windows Media Download package.</span></span> <span data-ttu-id="62643-128">Les techniques utilisées pour créer des bordures sont similaires à celles utilisées pour créer des apparences.</span><span class="sxs-lookup"><span data-stu-id="62643-128">The techniques used to create borders are similar to those used to create skins.</span></span> | <span data-ttu-id="62643-129">.wmz</span><span class="sxs-lookup"><span data-stu-id="62643-129">.wmz</span></span>                                     |
| <span data-ttu-id="62643-130">Sélection de métafichiers</span><span class="sxs-lookup"><span data-stu-id="62643-130">Metafile Playlist</span></span>  | <span data-ttu-id="62643-131">Métafichier Windows Media qui contient des éléments d' **entrée** , des informations de sélection et une identité d’élément d' **apparence** pour les fichiers de contenu.</span><span class="sxs-lookup"><span data-stu-id="62643-131">A Windows Media metafile that contains **ENTRY** elements, playlist information, and a **SKIN** element identity for content files.</span></span>                                                                                                             | <span data-ttu-id="62643-132">.asx</span><span class="sxs-lookup"><span data-stu-id="62643-132">.asx</span></span>                                     |
| <span data-ttu-id="62643-133">Contenu multimédia</span><span class="sxs-lookup"><span data-stu-id="62643-133">Multimedia Content</span></span> | <span data-ttu-id="62643-134">Fichier contenant un format audio ou vidéo pris en charge par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="62643-134">A file containing any audio or video format that is supported by Windows Media Player.</span></span>                                                                                                                                                          | <span data-ttu-id="62643-135">. WMA,. wmv,. ASF,. wav,. avi,. mpg,. mp3</span><span class="sxs-lookup"><span data-stu-id="62643-135">.wma, .wmv, .asf, .wav, .avi, .mpg, .mp3</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="62643-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="62643-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62643-137">**Packages de téléchargement Windows Media (déconseillés)**</span><span class="sxs-lookup"><span data-stu-id="62643-137">**Windows Media Download Packages (deprecated)**</span></span>](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




