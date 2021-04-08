---
title: Flux audio et vidéo
description: Flux audio et vidéo
ms.assetid: 809e5bb6-2bc4-4022-9117-a2be5418d7d1
keywords:
- Windows Media Format SDK, flux audio
- ASF (Advanced Systems Format), flux audio
- ASF (format des systèmes avancés), flux audio
- Kit de développement logiciel (SDK) Windows Media format, flux vidéo
- ASF (Advanced Systems Format), flux vidéo
- ASF (format de systèmes avancés), flux vidéo
- Windows Media Format SDK, flux
- ASF (Advanced Systems Format), flux
- ASF (format de systèmes avancés), flux
- flux audio, à propos de
- flux vidéo, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d72eb46a6fb19129da2b9a841eab1710da47013
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029141"
---
# <a name="audio-and-video-streams"></a><span data-ttu-id="61994-114">Flux audio et vidéo</span><span class="sxs-lookup"><span data-stu-id="61994-114">Audio and Video Streams</span></span>

<span data-ttu-id="61994-115">Les types de flux les plus courants utilisés dans les fichiers créés à l’aide du kit de développement logiciel (SDK) Windows Media format sont des flux audio et vidéo.</span><span class="sxs-lookup"><span data-stu-id="61994-115">The most common types of streams used in files created by using the Windows Media Format SDK are audio and video streams.</span></span> <span data-ttu-id="61994-116">Les représentations numériques des données audio et vidéo sont complexes et occupent de grandes quantités de mémoire.</span><span class="sxs-lookup"><span data-stu-id="61994-116">Digital representations of audio and video data are complex and take up large amounts of memory.</span></span> <span data-ttu-id="61994-117">Dans la plupart des cas, l’audio et la vidéo sont compressés avant d’être ajoutés à un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="61994-117">Under most circumstances, both audio and video are compressed before being added to an ASF file.</span></span> <span data-ttu-id="61994-118">La compression s’effectue à l’aide d’un compresseur/décompresseur (codec).</span><span class="sxs-lookup"><span data-stu-id="61994-118">Compression is accomplished using a compressor/decompressor (codec).</span></span>

<span data-ttu-id="61994-119">Plusieurs codecs Windows Media sont inclus dans ce kit de développement logiciel (SDK) et offrent une excellente compression de qualité pour les médias numériques.</span><span class="sxs-lookup"><span data-stu-id="61994-119">Several Windows Media codecs are included with this SDK, and they provide excellent quality compression for digital media.</span></span> <span data-ttu-id="61994-120">Pour plus d’informations sur les codecs Windows Media, consultez [fonctionnalités du codec](codec-features.md).</span><span class="sxs-lookup"><span data-stu-id="61994-120">For more information about the Windows Media codecs, see [Codec Features](codec-features.md).</span></span> <span data-ttu-id="61994-121">De nombreux autres codecs sont disponibles à partir de différentes sources.</span><span class="sxs-lookup"><span data-stu-id="61994-121">Many other codecs are available from various sources.</span></span> <span data-ttu-id="61994-122">Vous pouvez utiliser les codecs de votre choix lors de la création de fichiers ASF, mais seuls les codecs Windows Media sont directement pris en charge par les objets de ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="61994-122">You can use whatever codecs you like when creating ASF files, but only the Windows Media codecs are directly supported by the objects of this SDK.</span></span> <span data-ttu-id="61994-123">Pour utiliser d’autres codecs, vous devez compresser les exemples et les transmettre à l’objet writer en tant que données arbitraires.</span><span class="sxs-lookup"><span data-stu-id="61994-123">To use other codecs, you must compress samples and pass them to the writer object as arbitrary data.</span></span>

<span data-ttu-id="61994-124">La distinction la plus importante entre les flux audio et vidéo et les flux arbitraires est que les flux contenant des données audio ou vidéo Windows Media sont validés par les objets du kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="61994-124">The most important distinction between audio or video streams and arbitrary streams is that streams containing Windows Media audio or video data are validated by the objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="61994-125">Les flux de données arbitraires ne sont pas validés automatiquement et doivent être vérifiés pour vérifier l’intégrité de votre application.</span><span class="sxs-lookup"><span data-stu-id="61994-125">Arbitrary data streams are not validated automatically, and should be checked for integrity by your application.</span></span>

<span data-ttu-id="61994-126">Les propriétés d’un flux audio ou vidéo sont décrites dans le profil utilisé pour créer le fichier.</span><span class="sxs-lookup"><span data-stu-id="61994-126">The properties of an audio or video stream are described in the profile used to create the file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="61994-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="61994-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61994-128">**Flux arbitraires**</span><span class="sxs-lookup"><span data-stu-id="61994-128">**Arbitrary Streams**</span></span>](arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="61994-129">**Fonctionnalités des fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="61994-129">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="61994-130">**Utilisation des profils**</span><span class="sxs-lookup"><span data-stu-id="61994-130">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 




