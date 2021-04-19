---
title: Extensions de noms de fichiers
description: Extensions de noms de fichiers
ms.assetid: c17bf4e5-b469-45b6-bc22-2b451723d85e
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
ms.openlocfilehash: d95d5bcba9bbad5f04b0d085ba712d5b9306c8b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509401"
---
# <a name="file-name-extensions"></a><span data-ttu-id="c3dea-109">Extensions de noms de fichiers</span><span class="sxs-lookup"><span data-stu-id="c3dea-109">File Name Extensions</span></span>

<span data-ttu-id="c3dea-110">Il existe des instructions spécifiques pour l’utilisation des extensions de nom de fichier pour les fichiers Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c3dea-110">There are specific guidelines for the use of file name extensions for Windows Media metafiles.</span></span> <span data-ttu-id="c3dea-111">Les extensions de nom de métafichier Windows Media sont utilisées pour identifier les différents types de fichiers Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c3dea-111">Windows Media metafile name extensions are used to identify the different types of Windows Media files.</span></span> <span data-ttu-id="c3dea-112">Une extension de nom de fichier fournit à un éditeur de logiciels indépendant (ISV) des informations sur les exigences de rendu d’une application qui utilise une extension particulière, et permet aux créateurs de contenu de cibler des types généraux de lecteurs multimédias.</span><span class="sxs-lookup"><span data-stu-id="c3dea-112">A file name extension provides an Independent Software Vendor (ISV) with information about the rendering requirements of an application that uses a particular extension, and enables content authors to target general types of media players.</span></span>

<span data-ttu-id="c3dea-113">Les règles d’extension de nom de fichier sont répertoriées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c3dea-113">The file name extension guidelines are listed in the following table.</span></span> <span data-ttu-id="c3dea-114">Il est recommandé d’utiliser le type MIME d’un fichier, situé dans l’en-tête de fichier, pour l’identification du type de fichier.</span><span class="sxs-lookup"><span data-stu-id="c3dea-114">It is recommended that a file's MIME type, located in the file header, be used for file-type identification.</span></span>



| <span data-ttu-id="c3dea-115">Extension de nom de fichier</span><span class="sxs-lookup"><span data-stu-id="c3dea-115">File name extension</span></span> | <span data-ttu-id="c3dea-116">type MIME</span><span class="sxs-lookup"><span data-stu-id="c3dea-116">MIME type</span></span>      | <span data-ttu-id="c3dea-117">le contenu d’un fichier ;</span><span class="sxs-lookup"><span data-stu-id="c3dea-117">File content</span></span>                                                                                                                                                                            |
|---------------------|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3dea-118">.wma</span><span class="sxs-lookup"><span data-stu-id="c3dea-118">.wma</span></span>                | <span data-ttu-id="c3dea-119">audio/x-ms-WMA</span><span class="sxs-lookup"><span data-stu-id="c3dea-119">audio/x-ms-wma</span></span> | <span data-ttu-id="c3dea-120">Fichier Windows Media avec contenu audio uniquement.</span><span class="sxs-lookup"><span data-stu-id="c3dea-120">Windows Media file with audio content only.</span></span> <span data-ttu-id="c3dea-121">Généralement utilisé pour télécharger et lire des fichiers ou pour diffuser du contenu en continu.</span><span class="sxs-lookup"><span data-stu-id="c3dea-121">Typically used to download and play files or to stream content.</span></span>                                                                             |
| <span data-ttu-id="c3dea-122">.wmv</span><span class="sxs-lookup"><span data-stu-id="c3dea-122">.wmv</span></span>                | <span data-ttu-id="c3dea-123">vidéo/x-ms-WMV</span><span class="sxs-lookup"><span data-stu-id="c3dea-123">video/x-ms-wmv</span></span> | <span data-ttu-id="c3dea-124">Fichier Windows Media avec du contenu audio et/ou vidéo.</span><span class="sxs-lookup"><span data-stu-id="c3dea-124">Windows Media file with audio and/or video content.</span></span> <span data-ttu-id="c3dea-125">Généralement utilisé pour télécharger et lire des fichiers ou pour diffuser du contenu en continu.</span><span class="sxs-lookup"><span data-stu-id="c3dea-125">Typically used to download and play files or to stream content.</span></span>                                                                     |
| <span data-ttu-id="c3dea-126">.asf</span><span class="sxs-lookup"><span data-stu-id="c3dea-126">.asf</span></span>                | <span data-ttu-id="c3dea-127">vidéo/x-ms-asf</span><span class="sxs-lookup"><span data-stu-id="c3dea-127">video/x-ms-asf</span></span> | <span data-ttu-id="c3dea-128">Contenu hérité.</span><span class="sxs-lookup"><span data-stu-id="c3dea-128">Legacy content.</span></span> <span data-ttu-id="c3dea-129">Généralement utilisé pour télécharger et lire des fichiers ou pour diffuser du contenu en continu.</span><span class="sxs-lookup"><span data-stu-id="c3dea-129">Typically used to download and play files or to stream content.</span></span> <span data-ttu-id="c3dea-130">Peut contenir du contenu audio et/ou vidéo.</span><span class="sxs-lookup"><span data-stu-id="c3dea-130">May contain audio and/or video content.</span></span> <span data-ttu-id="c3dea-131">Généralement utilisé pour télécharger et lire des fichiers ou pour diffuser du contenu en continu.</span><span class="sxs-lookup"><span data-stu-id="c3dea-131">Typically used to download and play files or to stream content.</span></span> |
| <span data-ttu-id="c3dea-132">. WM</span><span class="sxs-lookup"><span data-stu-id="c3dea-132">.wm</span></span>                 | <span data-ttu-id="c3dea-133">vidéo/x-ms-WM</span><span class="sxs-lookup"><span data-stu-id="c3dea-133">video/x-ms-wm</span></span>  | <span data-ttu-id="c3dea-134">Réservé</span><span class="sxs-lookup"><span data-stu-id="c3dea-134">Reserved</span></span>                                                                                                                                                                                |
| <span data-ttu-id="c3dea-135">. Wax</span><span class="sxs-lookup"><span data-stu-id="c3dea-135">.wax</span></span>                | <span data-ttu-id="c3dea-136">audio/x-ms-Wax</span><span class="sxs-lookup"><span data-stu-id="c3dea-136">audio/x-ms-wax</span></span> | <span data-ttu-id="c3dea-137">Les sous-fichiers qui font référence à des fichiers Windows Media avec des extensions de nom de fichier. ASF,. WMA ou. Wax.</span><span class="sxs-lookup"><span data-stu-id="c3dea-137">Metafiles that reference Windows Media files with .asf, .wma, or .wax file name extensions.</span></span>                                                                                             |
| <span data-ttu-id="c3dea-138">. wvx</span><span class="sxs-lookup"><span data-stu-id="c3dea-138">.wvx</span></span>                | <span data-ttu-id="c3dea-139">vidéo/x-ms-wvx</span><span class="sxs-lookup"><span data-stu-id="c3dea-139">video/x-ms-wvx</span></span> | <span data-ttu-id="c3dea-140">Les sous-fichiers qui font référence à des fichiers Windows Media avec des extensions de nom de fichier. WMA,. wmv,. wvx ou. Wax.</span><span class="sxs-lookup"><span data-stu-id="c3dea-140">Metafiles that reference Windows Media files with .wma, .wmv, .wvx, or .wax file name extensions.</span></span>                                                                                       |
| <span data-ttu-id="c3dea-141">.asx</span><span class="sxs-lookup"><span data-stu-id="c3dea-141">.asx</span></span>                | <span data-ttu-id="c3dea-142">vidéo/x-ms-asf</span><span class="sxs-lookup"><span data-stu-id="c3dea-142">video/x-ms-asf</span></span> | <span data-ttu-id="c3dea-143">Les sous-fichiers qui font référence à des fichiers Windows Media avec des extensions de nom de fichier. WMA,. Wax,. wmv,. wvx,. ASF ou. asx.</span><span class="sxs-lookup"><span data-stu-id="c3dea-143">Metafiles that reference Windows Media files with .wma, .wax, .wmv, .wvx, .asf, or .asx file name extensions.</span></span>                                                                           |
| <span data-ttu-id="c3dea-144">. WMX</span><span class="sxs-lookup"><span data-stu-id="c3dea-144">.wmx</span></span>                | <span data-ttu-id="c3dea-145">vidéo/x-ms-wvx</span><span class="sxs-lookup"><span data-stu-id="c3dea-145">video/x-ms-wvx</span></span> | <span data-ttu-id="c3dea-146">Réservé.</span><span class="sxs-lookup"><span data-stu-id="c3dea-146">Reserved.</span></span>                                                                                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="c3dea-147">Notes</span><span class="sxs-lookup"><span data-stu-id="c3dea-147">Remarks</span></span>

<span data-ttu-id="c3dea-148">La gestion des scripts et de la gestion des droits numériques (DRM) doit être prise en charge par toutes les applications qui affichent des fichiers Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c3dea-148">Scripting and digital rights management (DRM) must be supported by any application that renders Windows Media files.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3dea-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c3dea-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3dea-150">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="c3dea-150">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="c3dea-151">**Guide des métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="c3dea-151">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> <dt>

[<span data-ttu-id="c3dea-152">**Informations de référence sur les métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="c3dea-152">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 




