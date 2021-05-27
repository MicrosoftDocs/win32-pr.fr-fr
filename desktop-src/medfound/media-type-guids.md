---
description: Types de médias principaux
ms.assetid: 1cca3539-a920-4938-93b9-ae41e1c0a287
title: Types de médias principaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56553ac635f0e767e43e057b2a468027dcefb730
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549574"
---
# <a name="major-media-types"></a><span data-ttu-id="87671-103">Types de médias principaux</span><span class="sxs-lookup"><span data-stu-id="87671-103">Major Media Types</span></span>

<span data-ttu-id="87671-104">Dans un type de média, le *type principal* décrit la catégorie globale des données, telles que l’audio ou la vidéo.</span><span class="sxs-lookup"><span data-stu-id="87671-104">In a media type, the *major type* describes the overall category of the data, such as audio or video.</span></span> <span data-ttu-id="87671-105">Le sous- *type*, s’il est présent, affine davantage le type principal.</span><span class="sxs-lookup"><span data-stu-id="87671-105">The *subtype*, if present, further refines the major type.</span></span> <span data-ttu-id="87671-106">Par exemple, si le type principal est vidéo, le sous-type peut être une vidéo RGB de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="87671-106">For example, if the major type is video, the subtype might be 32-bit RGB video.</span></span> <span data-ttu-id="87671-107">Les sous-types distinguent également les formats encodés, tels que la vidéo H. 264, des formats non compressés.</span><span class="sxs-lookup"><span data-stu-id="87671-107">Subtypes also distinguish encoded formats, such as H.264 video, from uncompressed formats.</span></span>

<span data-ttu-id="87671-108">Le type et le sous-type principaux sont identifiés par des GUID et stockés dans les attributs suivants :</span><span class="sxs-lookup"><span data-stu-id="87671-108">Major type and subtype are identified by GUIDs and stored in the following attributes:</span></span>



| <span data-ttu-id="87671-109">Attribut</span><span class="sxs-lookup"><span data-stu-id="87671-109">Attribute</span></span>                                             | <span data-ttu-id="87671-110">Description</span><span class="sxs-lookup"><span data-stu-id="87671-110">Description</span></span> |
|-------------------------------------------------------|-------------|
| [<span data-ttu-id="87671-111">\_type de \_ majeurese MF MT \_</span><span class="sxs-lookup"><span data-stu-id="87671-111">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="87671-112">Type principal.</span><span class="sxs-lookup"><span data-stu-id="87671-112">Major type.</span></span> |
| [<span data-ttu-id="87671-113">\_sous- \_ type MF MT</span><span class="sxs-lookup"><span data-stu-id="87671-113">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="87671-114">Sous-type.</span><span class="sxs-lookup"><span data-stu-id="87671-114">Subtype.</span></span>    |



 

<span data-ttu-id="87671-115">Les types principaux suivants sont définis.</span><span class="sxs-lookup"><span data-stu-id="87671-115">The following major types are defined.</span></span>



| <span data-ttu-id="87671-116">Type principal</span><span class="sxs-lookup"><span data-stu-id="87671-116">Major Type</span></span>                    | <span data-ttu-id="87671-117">Description</span><span class="sxs-lookup"><span data-stu-id="87671-117">Description</span></span>                                                                                                                                                | <span data-ttu-id="87671-118">Sous-types</span><span class="sxs-lookup"><span data-stu-id="87671-118">Subtypes</span></span>                                             |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="87671-119">**MFMediaType \_ audio**</span><span class="sxs-lookup"><span data-stu-id="87671-119">**MFMediaType\_Audio**</span></span>        | <span data-ttu-id="87671-120">HD.</span><span class="sxs-lookup"><span data-stu-id="87671-120">Audio.</span></span>                                                                                                                                                     | <span data-ttu-id="87671-121">[GUID de sous-type audio](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="87671-121">[Audio Subtype GUIDs](audio-subtype-guids.md).</span></span>      |
| <span data-ttu-id="87671-122">**\_Binaire MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="87671-122">**MFMediaType\_Binary**</span></span>       | <span data-ttu-id="87671-123">Flux binaire.</span><span class="sxs-lookup"><span data-stu-id="87671-123">Binary stream.</span></span>                                                                                                                                             | <span data-ttu-id="87671-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="87671-124">None.</span></span>                                                |
| <span data-ttu-id="87671-125">**MFMediaType \_ filetransfer**</span><span class="sxs-lookup"><span data-stu-id="87671-125">**MFMediaType\_FileTransfer**</span></span> | <span data-ttu-id="87671-126">Flux qui contient des fichiers de données.</span><span class="sxs-lookup"><span data-stu-id="87671-126">A stream that contains data files.</span></span>                                                                                                                         | <span data-ttu-id="87671-127">Aucun.</span><span class="sxs-lookup"><span data-stu-id="87671-127">None.</span></span>                                                |
| <span data-ttu-id="87671-128">**\_HTML MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="87671-128">**MFMediaType\_HTML**</span></span>         | <span data-ttu-id="87671-129">Flux HTML.</span><span class="sxs-lookup"><span data-stu-id="87671-129">HTML stream.</span></span>                                                                                                                                               | <span data-ttu-id="87671-130">Aucun.</span><span class="sxs-lookup"><span data-stu-id="87671-130">None.</span></span>                                                |
| <span data-ttu-id="87671-131">**\_Image MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="87671-131">**MFMediaType\_Image**</span></span>        | <span data-ttu-id="87671-132">Flux d’images fixes.</span><span class="sxs-lookup"><span data-stu-id="87671-132">Still image stream.</span></span>                                                                                                                                        | <span data-ttu-id="87671-133">[GUID et CLSID WIC](../wic/-wic-guids-clsids.md).</span><span class="sxs-lookup"><span data-stu-id="87671-133">[WIC GUIDs and CLSIDs](../wic/-wic-guids-clsids.md).</span></span>       |
| <span data-ttu-id="87671-134">**\_Métadonnées MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="87671-134">**MFMediaType\_Metadata**</span></span>        | <span data-ttu-id="87671-135">Flux de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="87671-135">Metadata stream.</span></span>                                                                                                                                        | <span data-ttu-id="87671-136">Aucun.</span><span class="sxs-lookup"><span data-stu-id="87671-136">None.</span></span>       |
| <span data-ttu-id="87671-137">**MFMediaType \_ protégé**</span><span class="sxs-lookup"><span data-stu-id="87671-137">**MFMediaType\_Protected**</span></span>    | <span data-ttu-id="87671-138">Média protégé.</span><span class="sxs-lookup"><span data-stu-id="87671-138">Protected media.</span></span>                                                                                                                                           | <span data-ttu-id="87671-139">Le sous-type spécifie le schéma de protection de contenu.</span><span class="sxs-lookup"><span data-stu-id="87671-139">The subtype specifies the content protection scheme.</span></span> |
| <span data-ttu-id="87671-140">**MFMediaType \_ perception**</span><span class="sxs-lookup"><span data-stu-id="87671-140">**MFMediaType\_Perception**</span></span>   | <span data-ttu-id="87671-141">Flux provenant d’un capteur d’appareil photo ou d’une unité de traitement qui justifie et comprend les données vidéo brutes et qui permet de comprendre l’environnement ou les êtres humains.</span><span class="sxs-lookup"><span data-stu-id="87671-141">Streams from a camera sensor or processing unit that reasons and understands raw video data and provides understanding of the environment or humans in it.</span></span> | <span data-ttu-id="87671-142">Aucun.</span><span class="sxs-lookup"><span data-stu-id="87671-142">None.</span></span>                                                |
| <span data-ttu-id="87671-143">**\_Sami MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="87671-143">**MFMediaType\_SAMI**</span></span>         | <span data-ttu-id="87671-144">Les sous-titres SAMI (Synchronized Accessible Media Interchange).</span><span class="sxs-lookup"><span data-stu-id="87671-144">Synchronized Accessible Media Interchange (SAMI) captions.</span></span>                                                                                                 | <span data-ttu-id="87671-145">Aucun.</span><span class="sxs-lookup"><span data-stu-id="87671-145">None.</span></span>                                                |
| <span data-ttu-id="87671-146">**\_Script MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="87671-146">**MFMediaType\_Script**</span></span>       | <span data-ttu-id="87671-147">Flux de script.</span><span class="sxs-lookup"><span data-stu-id="87671-147">Script stream.</span></span>                                                                                                                                             | <span data-ttu-id="87671-148">Aucun.</span><span class="sxs-lookup"><span data-stu-id="87671-148">None.</span></span>                                                |
| <span data-ttu-id="87671-149">**\_Flux MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="87671-149">**MFMediaType\_Stream**</span></span>       | <span data-ttu-id="87671-150">Flux multiplexé ou flux élémentaire.</span><span class="sxs-lookup"><span data-stu-id="87671-150">Multiplexed stream or elementary stream.</span></span>                                                                                                                   | [<span data-ttu-id="87671-151">GUID de sous-type de flux</span><span class="sxs-lookup"><span data-stu-id="87671-151">Stream Subtype GUIDs</span></span>](stream-subtype-guids.md)     |
| <span data-ttu-id="87671-152">**\_Vidéo MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="87671-152">**MFMediaType\_Video**</span></span>        | <span data-ttu-id="87671-153">Vidéo.</span><span class="sxs-lookup"><span data-stu-id="87671-153">Video.</span></span>                                                                                                                                                     | <span data-ttu-id="87671-154">[GUID de sous-type de vidéo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="87671-154">[Video Subtype GUIDs](video-subtype-guids.md).</span></span>      |



 

<span data-ttu-id="87671-155">Les composants tiers peuvent définir de nouveaux types principaux et de nouveaux sous-types.</span><span class="sxs-lookup"><span data-stu-id="87671-155">Third-party components can define new major types and new subtypes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87671-156">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="87671-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87671-157">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="87671-157">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="87671-158">Types de médias</span><span class="sxs-lookup"><span data-stu-id="87671-158">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 
