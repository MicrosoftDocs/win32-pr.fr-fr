---
description: Les codecs Windows Media Audio et vidéo sont un ensemble d’objets que vous pouvez utiliser pour compresser et décompresser des données multimédias numériques.
ms.assetid: 74de2e75-b1ee-436d-8d78-efe366ab7aa6
title: Codecs Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ec98f98fbd0561b291dfc4cc18e4270bf363baf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106525805"
---
# <a name="windows-media-codecs"></a><span data-ttu-id="32480-103">Codecs Windows Media</span><span class="sxs-lookup"><span data-stu-id="32480-103">Windows Media Codecs</span></span>

<span data-ttu-id="32480-104">Les codecs Windows Media Audio et vidéo sont un ensemble d’objets que vous pouvez utiliser pour compresser et décompresser des données multimédias numériques.</span><span class="sxs-lookup"><span data-stu-id="32480-104">The Windows Media Audio and Video codecs are a collection of objects that you can use to compress and decompress digital media data.</span></span> <span data-ttu-id="32480-105">Chaque codec se compose de deux objets : un encodeur et un décodeur.</span><span class="sxs-lookup"><span data-stu-id="32480-105">Each codec consists of two objects, an encoder and a decoder.</span></span> <span data-ttu-id="32480-106">Cette partie de la documentation explique comment utiliser les fonctionnalités des codecs vidéo et Windows Media Audio pour produire et consommer des flux de données compressés.</span><span class="sxs-lookup"><span data-stu-id="32480-106">This part of the documentation describes how to use the features of the Windows Media Audio and Video codecs to produce and consume compressed data streams.</span></span>

> [!Note]  
> <span data-ttu-id="32480-107">Cette documentation concerne principalement les développeurs qui souhaitent utiliser des codecs Windows Media dans leurs applications multimédias basées sur C++.</span><span class="sxs-lookup"><span data-stu-id="32480-107">This documentation is primarily for developers who want to use Windows Media codecs in their C++-based media applications.</span></span> <span data-ttu-id="32480-108">Pour obtenir une vue d’ensemble technique des fonctionnalités des codecs Windows Media, consultez [à propos des codecs Windows Media](about-the-windows-media-codecs.md).</span><span class="sxs-lookup"><span data-stu-id="32480-108">For a technical overview of the features of the Windows Media codecs, see [About the Windows Media Codecs](about-the-windows-media-codecs.md).</span></span>

 

<span data-ttu-id="32480-109">Le terme *codec* est un amalgame des termes compresseur et décompresseur.</span><span class="sxs-lookup"><span data-stu-id="32480-109">The term *codec* is an amalgamation of the terms compressor and decompressor.</span></span> <span data-ttu-id="32480-110">Un codec est généralement implémenté comme une paire d’objets COM : l’un pour l’encodage du contenu et l’autre pour le décodage du contenu.</span><span class="sxs-lookup"><span data-stu-id="32480-110">A codec is usually implemented as a pair of COM objects: one for encoding content, and another for decoding content.</span></span> <span data-ttu-id="32480-111">Dans certains cas, les objets COM occupent la même bibliothèque de liens dynamiques (DLL).</span><span class="sxs-lookup"><span data-stu-id="32480-111">In some cases the COM objects occupy the same dynamically linked library (DLL).</span></span>

<span data-ttu-id="32480-112">Chaque objet codec implémente deux interfaces distinctes mais similaires :</span><span class="sxs-lookup"><span data-stu-id="32480-112">Every codec object implements two separate but similar interfaces:</span></span>



| <span data-ttu-id="32480-113">Interface</span><span class="sxs-lookup"><span data-stu-id="32480-113">Interface</span></span>                              | <span data-ttu-id="32480-114">Description</span><span class="sxs-lookup"><span data-stu-id="32480-114">Description</span></span>                                 |
|----------------------------------------|---------------------------------------------|
| [<span data-ttu-id="32480-115">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="32480-115">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)   | <span data-ttu-id="32480-116">Compatible avec Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="32480-116">Compatible with Microsoft Media Foundation.</span></span> |
| [<span data-ttu-id="32480-117">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="32480-117">**IMediaObject**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) | <span data-ttu-id="32480-118">Compatible avec DirectShow.</span><span class="sxs-lookup"><span data-stu-id="32480-118">Compatible with DirectShow.</span></span>                 |



 

<span data-ttu-id="32480-119">En outre, il existe différents codecs pour l’audio et la vidéo, mais également différents codecs pour différents types de contenu que vous pouvez placer dans un fichier audio ou vidéo.</span><span class="sxs-lookup"><span data-stu-id="32480-119">Not only are there different codecs for audio and for video, but also different codecs for different kinds of content that you might want to put into an audio or video file.</span></span> <span data-ttu-id="32480-120">Les algorithmes utilisés pour compresser et décompresser les données des mots prononcés diffèrent des algorithmes utilisés pour compresser et décompresser les données de musique.</span><span class="sxs-lookup"><span data-stu-id="32480-120">The algorithms used to compress and decompress data for spoken words differ from the algorithms used to compress and decompress music data.</span></span>

## <a name="codec-descriptions"></a><span data-ttu-id="32480-121">Descriptions des codecs</span><span class="sxs-lookup"><span data-stu-id="32480-121">Codec Descriptions</span></span>

<span data-ttu-id="32480-122">Le tableau suivant décrit les utilisations prévues des codecs Windows Media.</span><span class="sxs-lookup"><span data-stu-id="32480-122">The following table describes the intended uses of the Windows Media codecs.</span></span>



| <span data-ttu-id="32480-123">Codec</span><span class="sxs-lookup"><span data-stu-id="32480-123">Codec</span></span>                                                                     | <span data-ttu-id="32480-124">Description</span><span class="sxs-lookup"><span data-stu-id="32480-124">Description</span></span>                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="32480-125">Windows Media Audio</span><span class="sxs-lookup"><span data-stu-id="32480-125">Windows Media Audio</span></span>](windowsmediaaudioencoder.md)                       | <span data-ttu-id="32480-126">Un codec audio qui prend en charge trois catégories de contenu encodé : standard, Professional et Lossless.</span><span class="sxs-lookup"><span data-stu-id="32480-126">An audio codec that supports three categories of encoded content: Standard, Professional, and Lossless.</span></span>                                                                                                                                                                                      |
| [<span data-ttu-id="32480-127">Windows Media Audio Voice</span><span class="sxs-lookup"><span data-stu-id="32480-127">Windows Media Audio Voice</span></span>](windowsmediaaudiovoiceencoder.md)            | <span data-ttu-id="32480-128">Codec audio optimisé pour l’encodage de la voix humaine à des taux de compression élevés.</span><span class="sxs-lookup"><span data-stu-id="32480-128">Audio codec optimized for encoding the human voice at high compression ratios.</span></span> <span data-ttu-id="32480-129">Il s’agit du codec préféré pour les flux composés principalement de mots prononcés.</span><span class="sxs-lookup"><span data-stu-id="32480-129">This is the preferred codec for streams consisting mostly of spoken words.</span></span> <span data-ttu-id="32480-130">Pour le contenu mixte musical et vocal, ce codec peut modifier dynamiquement l’algorithme d’encodage utilisé, pour obtenir une qualité optimale.</span><span class="sxs-lookup"><span data-stu-id="32480-130">For content that is mixed music and speech, this codec can dynamically change the encoding algorithm used, to get optimal quality.</span></span> |
| [<span data-ttu-id="32480-131">Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="32480-131">Windows Media Video 9</span></span>](windowsmediavideo9encoder.md)                    | <span data-ttu-id="32480-132">Codec vidéo qui prend en charge quatre catégories de contenu encodé : profil simple, profil principal, profil avancé et image.</span><span class="sxs-lookup"><span data-stu-id="32480-132">A video codec that supports four categories of encoded content: Simple Profile, Main Profile, Advanced Profile, and Image..</span></span>                                                                                                                                                                  |
| [<span data-ttu-id="32480-133">Écran Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="32480-133">Windows Media Video 9 Screen</span></span>](usingthewindowsmediavideo9screencodec.md) | <span data-ttu-id="32480-134">Codec vidéo optimisé pour l’encodage des captures d’écran séquentielles à partir des moniteurs d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="32480-134">Video codec optimized for encoding sequential screen shots from computer monitors.</span></span> <span data-ttu-id="32480-135">Ce codec est souvent utilisé pour la formation ou le support logiciel en enregistrant les images du moniteur pendant l’utilisation des applications de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="32480-135">This codec is often used for software training or support by recording monitor images while computer applications are being used.</span></span>                                                                         |



 

<span data-ttu-id="32480-136">Les versions les plus récentes des objets codec permettent également d’accéder à certains codecs hérités, notamment les Windows Media Video 7 et 8, Windows Media Screen 7, les codecs Microsoft MPEG-4 plus anciens et les codecs Microsoft ISO MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="32480-136">The most recent versions of the codec objects also enable access to some legacy codecs, including Windows Media Video 7 and 8, Windows Media Screen 7, the older Microsoft MPEG-4 codecs, and the Microsoft ISO MPEG-4 codecs.</span></span>

> [!Note]  
> <span data-ttu-id="32480-137">Cette documentation ne couvre pas ces codecs hérités. Il couvre uniquement les versions actuelles des codecs.</span><span class="sxs-lookup"><span data-stu-id="32480-137">This documentation does not cover these legacy codecs; it covers only the current versions of codecs.</span></span>

 

<span data-ttu-id="32480-138">Pour les codecs plus anciens, utilisez les mêmes procédures que lors de l’utilisation des codecs actuels. Toutefois, n’oubliez pas que toutes les fonctionnalités ne sont pas prises en charge dans tous les codecs.</span><span class="sxs-lookup"><span data-stu-id="32480-138">For older codecs, use the same procedures as when using the current codecs; however, remember that not all features are supported in all codecs.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="32480-139">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="32480-139">In this section</span></span>

-   [<span data-ttu-id="32480-140">À propos des codecs Windows Media</span><span class="sxs-lookup"><span data-stu-id="32480-140">About the Windows Media Codecs</span></span>](about-the-windows-media-codecs.md)
-   [<span data-ttu-id="32480-141">Utilisation des objets codec et DSP</span><span class="sxs-lookup"><span data-stu-id="32480-141">Using the Codec and DSP Objects</span></span>](decidinghowtousethewindowsmediaaudioandvideocodecs.md)
-   [<span data-ttu-id="32480-142">Méthodes d’encodage</span><span class="sxs-lookup"><span data-stu-id="32480-142">Encoding Methods</span></span>](encodingmethods.md)
-   [<span data-ttu-id="32480-143">Implémentation du codec</span><span class="sxs-lookup"><span data-stu-id="32480-143">Codec Implementation</span></span>](codecimplementation.md)
-   [<span data-ttu-id="32480-144">Modèle de mémoire tampon de compartiment avec fuite</span><span class="sxs-lookup"><span data-stu-id="32480-144">The Leaky Bucket Buffer Model</span></span>](the-leaky-bucket-buffer-model.md)
-   [<span data-ttu-id="32480-145">Utilisation du codec DMOs</span><span class="sxs-lookup"><span data-stu-id="32480-145">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
-   [<span data-ttu-id="32480-146">Utilisation du codec MFTs</span><span class="sxs-lookup"><span data-stu-id="32480-146">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
-   [<span data-ttu-id="32480-147">Utilisation de l’audio</span><span class="sxs-lookup"><span data-stu-id="32480-147">Working with Audio</span></span>](workingwithaudio.md)
-   [<span data-ttu-id="32480-148">Utilisation de la vidéo</span><span class="sxs-lookup"><span data-stu-id="32480-148">Working with Video</span></span>](workingwithvideo.md)
-   [<span data-ttu-id="32480-149">Stockage d’un média compressé dans des fichiers AVI</span><span class="sxs-lookup"><span data-stu-id="32480-149">Storing Compressed Media in AVI Files</span></span>](storingcompressedmediainavifiles.md)
-   [<span data-ttu-id="32480-150">Utilisation de l’encodage VBR</span><span class="sxs-lookup"><span data-stu-id="32480-150">Using VBR Encoding</span></span>](usingvbrencoding.md)
-   [<span data-ttu-id="32480-151">Utilisation de l’encodage Two-Pass</span><span class="sxs-lookup"><span data-stu-id="32480-151">Using Two-Pass Encoding</span></span>](usingtwoencodingpasses.md)
-   [<span data-ttu-id="32480-152">Obtention des statistiques d’encodage</span><span class="sxs-lookup"><span data-stu-id="32480-152">Getting Encoding Statistics</span></span>](gettingencodingstatistics.md)
-   [<span data-ttu-id="32480-153">Utilisation des extensions d’unité de données</span><span class="sxs-lookup"><span data-stu-id="32480-153">Using Data Unit Extensions</span></span>](usingdataunitextensions.md)
-   [<span data-ttu-id="32480-154">Constantes codec et DSP IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="32480-154">Codec and DSP IPropertyBag Constants</span></span>](codecanddspproperties.md)
-   [<span data-ttu-id="32480-155">Analyseur de table des matières</span><span class="sxs-lookup"><span data-stu-id="32480-155">Table of Contents Parser</span></span>](toc-parser.md)
-   [<span data-ttu-id="32480-156">FAQ sur les codecs Windows Media</span><span class="sxs-lookup"><span data-stu-id="32480-156">Windows Media Codec FAQ</span></span>](frequentlyaskedquestions.md)

## <a name="related-topics"></a><span data-ttu-id="32480-157">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="32480-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32480-158">Guide de programmation Media Foundation</span><span class="sxs-lookup"><span data-stu-id="32480-158">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> <dt>

<span data-ttu-id="32480-159">[Technologies multimédias pour Windows](/previous-versions/bg125389(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="32480-159">[Media Technologies for Windows](/previous-versions/bg125389(v=msdn.10))</span></span>
</dt> </dl>

 

 
