---
title: Instructions relatives aux extensions de métafichiers
description: Instructions relatives aux extensions de métafichiers
ms.assetid: 079fac31-7a6f-4775-a337-870ad25a56a0
keywords:
- Fichiers Windows Media, extensions
- Fichiers Windows Media, extensions de nom de fichier
- refichiers, extensions
- sous-fichiers, extensions de nom de fichier
- Windows Media, sous-fichiers
- extensions de nom de fichier pour les fichiers Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 31d2793b19576e26096bc30c834666828cf9ed29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029784"
---
# <a name="metafile-extension-guidelines"></a><span data-ttu-id="2591d-109">Instructions relatives aux extensions de métafichiers</span><span class="sxs-lookup"><span data-stu-id="2591d-109">Metafile Extension Guidelines</span></span>

<span data-ttu-id="2591d-110">Une extension de nom de fichier fournit à un éditeur de logiciels indépendant (ISV) des informations sur les exigences de rendu d’une application qui utilise l’extension et permet aux créateurs de contenu de cibler les types généraux de joueurs.</span><span class="sxs-lookup"><span data-stu-id="2591d-110">A file name extension provides an independent software vendor (ISV) with information about the rendering requirements of an application that uses the extension, and enables content authors to target general types of players.</span></span>

<span data-ttu-id="2591d-111">Les extensions de nom de métafichier Windows Media sont utilisées pour identifier le format des fichiers Windows Media référencés par un métafichier.</span><span class="sxs-lookup"><span data-stu-id="2591d-111">Windows Media metafile name extensions are used to identify the format of the Windows Media files that a metafile references.</span></span> <span data-ttu-id="2591d-112">Les sous-fichiers Windows Media avec des extensions. Wax,. wvx ou. asx sont respectivement des fichiers de référence. WMA,. wmv et. ASF.</span><span class="sxs-lookup"><span data-stu-id="2591d-112">Windows Media metafiles with .wax, .wvx, or .asx extensions reference files with .wma, .wmv, and .asf extensions, respectively.</span></span> <span data-ttu-id="2591d-113">Tous les sous-fichiers, quelle que soit l’extension de nom de fichier utilisée, comportent la balise d’élément **ASX** au début du fichier avec l’attribut de **version** spécifié.</span><span class="sxs-lookup"><span data-stu-id="2591d-113">All metafiles, regardless of the file name extension used, have the **ASX** element tag at the beginning of the file with the **version** attribute specified.</span></span>

<span data-ttu-id="2591d-114">Le tableau suivant présente les types de fichiers multimédias référencés par chaque type d’extension de nom de fichier de métafichier.</span><span class="sxs-lookup"><span data-stu-id="2591d-114">The following table shows the media file types referenced by each type of metafile file name extension.</span></span> <span data-ttu-id="2591d-115">Les colonnes répertorient les extensions de nom de fichier multimédia, les lignes répertorient les extensions de nom de métafichier.</span><span class="sxs-lookup"><span data-stu-id="2591d-115">The columns list media file name extensions, the rows list metafile name extensions.</span></span> <span data-ttu-id="2591d-116">Un X dans une colonne indique un type de fichier multimédia qui peut être référencé par une extension de nom de fichier de métafichier particulière.</span><span class="sxs-lookup"><span data-stu-id="2591d-116">An X in a column indicates a media file type that can be referenced by a particular metafile file name extension.</span></span>



| <span data-ttu-id="2591d-117">Extension</span><span class="sxs-lookup"><span data-stu-id="2591d-117">Extension</span></span> | <span data-ttu-id="2591d-118">.asf</span><span class="sxs-lookup"><span data-stu-id="2591d-118">.asf</span></span> | <span data-ttu-id="2591d-119">.wma</span><span class="sxs-lookup"><span data-stu-id="2591d-119">.wma</span></span> | <span data-ttu-id="2591d-120">.wmv</span><span class="sxs-lookup"><span data-stu-id="2591d-120">.wmv</span></span> |
|-----------|------|------|------|
| <span data-ttu-id="2591d-121">. wvx</span><span class="sxs-lookup"><span data-stu-id="2591d-121">.wvx</span></span>      | <span data-ttu-id="2591d-122">X</span><span class="sxs-lookup"><span data-stu-id="2591d-122">X</span></span>    | <span data-ttu-id="2591d-123">X</span><span class="sxs-lookup"><span data-stu-id="2591d-123">X</span></span>    | <span data-ttu-id="2591d-124">X</span><span class="sxs-lookup"><span data-stu-id="2591d-124">X</span></span>    |
| <span data-ttu-id="2591d-125">. Wax</span><span class="sxs-lookup"><span data-stu-id="2591d-125">.wax</span></span>      | <span data-ttu-id="2591d-126">X</span><span class="sxs-lookup"><span data-stu-id="2591d-126">X</span></span>    | <span data-ttu-id="2591d-127">X</span><span class="sxs-lookup"><span data-stu-id="2591d-127">X</span></span>    |      |
| <span data-ttu-id="2591d-128">.asx</span><span class="sxs-lookup"><span data-stu-id="2591d-128">.asx</span></span>      | <span data-ttu-id="2591d-129">X</span><span class="sxs-lookup"><span data-stu-id="2591d-129">X</span></span>    |      |      |



 

## <a name="related-topics"></a><span data-ttu-id="2591d-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2591d-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2591d-131">**Extensions de noms de fichiers**</span><span class="sxs-lookup"><span data-stu-id="2591d-131">**File Name Extensions**</span></span>](file-name-extensions.md)
</dt> <dt>

[<span data-ttu-id="2591d-132">**Sélections de métafichiers**</span><span class="sxs-lookup"><span data-stu-id="2591d-132">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="2591d-133">**Guide des métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="2591d-133">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




