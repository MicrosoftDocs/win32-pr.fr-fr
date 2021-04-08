---
description: Types de médias principaux
ms.assetid: 1cca3539-a920-4938-93b9-ae41e1c0a287
title: Types de médias principaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a93a1aa430a720ff4b2f3591071d0bc8b178d6a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103953438"
---
# <a name="major-media-types"></a><span data-ttu-id="6109f-103">Types de médias principaux</span><span class="sxs-lookup"><span data-stu-id="6109f-103">Major Media Types</span></span>

<span data-ttu-id="6109f-104">Dans un type de média, le *type principal* décrit la catégorie globale des données, telles que l’audio ou la vidéo.</span><span class="sxs-lookup"><span data-stu-id="6109f-104">In a media type, the *major type* describes the overall category of the data, such as audio or video.</span></span> <span data-ttu-id="6109f-105">Le sous- *type*, s’il est présent, affine davantage le type principal.</span><span class="sxs-lookup"><span data-stu-id="6109f-105">The *subtype*, if present, further refines the major type.</span></span> <span data-ttu-id="6109f-106">Par exemple, si le type principal est vidéo, le sous-type peut être une vidéo RGB de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6109f-106">For example, if the major type is video, the subtype might be 32-bit RGB video.</span></span> <span data-ttu-id="6109f-107">Les sous-types distinguent également les formats encodés, tels que la vidéo H. 264, des formats non compressés.</span><span class="sxs-lookup"><span data-stu-id="6109f-107">Subtypes also distinguish encoded formats, such as H.264 video, from uncompressed formats.</span></span>

<span data-ttu-id="6109f-108">Le type et le sous-type principaux sont identifiés par des GUID et stockés dans les attributs suivants :</span><span class="sxs-lookup"><span data-stu-id="6109f-108">Major type and subtype are identified by GUIDs and stored in the following attributes:</span></span>



| <span data-ttu-id="6109f-109">Attribut</span><span class="sxs-lookup"><span data-stu-id="6109f-109">Attribute</span></span>                                             | <span data-ttu-id="6109f-110">Description</span><span class="sxs-lookup"><span data-stu-id="6109f-110">Description</span></span> |
|-------------------------------------------------------|-------------|
| [<span data-ttu-id="6109f-111">\_type de \_ majeurese MF MT \_</span><span class="sxs-lookup"><span data-stu-id="6109f-111">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="6109f-112">Type principal.</span><span class="sxs-lookup"><span data-stu-id="6109f-112">Major type.</span></span> |
| [<span data-ttu-id="6109f-113">\_sous- \_ type MF MT</span><span class="sxs-lookup"><span data-stu-id="6109f-113">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="6109f-114">Sous-type.</span><span class="sxs-lookup"><span data-stu-id="6109f-114">Subtype.</span></span>    |



 

<span data-ttu-id="6109f-115">Les types principaux suivants sont définis.</span><span class="sxs-lookup"><span data-stu-id="6109f-115">The following major types are defined.</span></span>



| <span data-ttu-id="6109f-116">Type principal</span><span class="sxs-lookup"><span data-stu-id="6109f-116">Major Type</span></span>                    | <span data-ttu-id="6109f-117">Description</span><span class="sxs-lookup"><span data-stu-id="6109f-117">Description</span></span>                                                                                                                                                | <span data-ttu-id="6109f-118">Sous-types</span><span class="sxs-lookup"><span data-stu-id="6109f-118">Subtypes</span></span>                                             |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6109f-119">**MFMediaType \_ audio**</span><span class="sxs-lookup"><span data-stu-id="6109f-119">**MFMediaType\_Audio**</span></span>        | <span data-ttu-id="6109f-120">HD.</span><span class="sxs-lookup"><span data-stu-id="6109f-120">Audio.</span></span>                                                                                                                                                     | <span data-ttu-id="6109f-121">[GUID de sous-type audio](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="6109f-121">[Audio Subtype GUIDs](audio-subtype-guids.md).</span></span>      |
| <span data-ttu-id="6109f-122">**\_Binaire MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="6109f-122">**MFMediaType\_Binary**</span></span>       | <span data-ttu-id="6109f-123">Flux binaire.</span><span class="sxs-lookup"><span data-stu-id="6109f-123">Binary stream.</span></span>                                                                                                                                             | <span data-ttu-id="6109f-124">Aucun</span><span class="sxs-lookup"><span data-stu-id="6109f-124">None.</span></span>                                                |
| <span data-ttu-id="6109f-125">**MFMediaType \_ filetransfer**</span><span class="sxs-lookup"><span data-stu-id="6109f-125">**MFMediaType\_FileTransfer**</span></span> | <span data-ttu-id="6109f-126">Flux qui contient des fichiers de données.</span><span class="sxs-lookup"><span data-stu-id="6109f-126">A stream that contains data files.</span></span>                                                                                                                         | <span data-ttu-id="6109f-127">Aucun</span><span class="sxs-lookup"><span data-stu-id="6109f-127">None.</span></span>                                                |
| <span data-ttu-id="6109f-128">**\_HTML MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="6109f-128">**MFMediaType\_HTML**</span></span>         | <span data-ttu-id="6109f-129">Flux HTML.</span><span class="sxs-lookup"><span data-stu-id="6109f-129">HTML stream.</span></span>                                                                                                                                               | <span data-ttu-id="6109f-130">Aucun</span><span class="sxs-lookup"><span data-stu-id="6109f-130">None.</span></span>                                                |
| <span data-ttu-id="6109f-131">**\_Image MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="6109f-131">**MFMediaType\_Image**</span></span>        | <span data-ttu-id="6109f-132">Flux d’images fixes.</span><span class="sxs-lookup"><span data-stu-id="6109f-132">Still image stream.</span></span>                                                                                                                                        | <span data-ttu-id="6109f-133">[GUID et CLSID WIC](../wic/-wic-guids-clsids.md).</span><span class="sxs-lookup"><span data-stu-id="6109f-133">[WIC GUIDs and CLSIDs](../wic/-wic-guids-clsids.md).</span></span>       |
| <span data-ttu-id="6109f-134">**MFMediaType \_ protégé**</span><span class="sxs-lookup"><span data-stu-id="6109f-134">**MFMediaType\_Protected**</span></span>    | <span data-ttu-id="6109f-135">Média protégé.</span><span class="sxs-lookup"><span data-stu-id="6109f-135">Protected media.</span></span>                                                                                                                                           | <span data-ttu-id="6109f-136">Le sous-type spécifie le schéma de protection de contenu.</span><span class="sxs-lookup"><span data-stu-id="6109f-136">The subtype specifies the content protection scheme.</span></span> |
| <span data-ttu-id="6109f-137">**MFMediaType \_ perception**</span><span class="sxs-lookup"><span data-stu-id="6109f-137">**MFMediaType\_Perception**</span></span>   | <span data-ttu-id="6109f-138">Flux provenant d’un capteur d’appareil photo ou d’une unité de traitement qui justifie et comprend les données vidéo brutes et qui permet de comprendre l’environnement ou les êtres humains.</span><span class="sxs-lookup"><span data-stu-id="6109f-138">Streams from a camera sensor or processing unit that reasons and understands raw video data and provides understanding of the environment or humans in it.</span></span> | <span data-ttu-id="6109f-139">Aucun</span><span class="sxs-lookup"><span data-stu-id="6109f-139">None.</span></span>                                                |
| <span data-ttu-id="6109f-140">**\_Sami MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="6109f-140">**MFMediaType\_SAMI**</span></span>         | <span data-ttu-id="6109f-141">Les sous-titres SAMI (Synchronized Accessible Media Interchange).</span><span class="sxs-lookup"><span data-stu-id="6109f-141">Synchronized Accessible Media Interchange (SAMI) captions.</span></span>                                                                                                 | <span data-ttu-id="6109f-142">Aucun</span><span class="sxs-lookup"><span data-stu-id="6109f-142">None.</span></span>                                                |
| <span data-ttu-id="6109f-143">**\_Script MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="6109f-143">**MFMediaType\_Script**</span></span>       | <span data-ttu-id="6109f-144">Flux de script.</span><span class="sxs-lookup"><span data-stu-id="6109f-144">Script stream.</span></span>                                                                                                                                             | <span data-ttu-id="6109f-145">Aucun</span><span class="sxs-lookup"><span data-stu-id="6109f-145">None.</span></span>                                                |
| <span data-ttu-id="6109f-146">**\_Flux MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="6109f-146">**MFMediaType\_Stream**</span></span>       | <span data-ttu-id="6109f-147">Flux multiplexé ou flux élémentaire.</span><span class="sxs-lookup"><span data-stu-id="6109f-147">Multiplexed stream or elementary stream.</span></span>                                                                                                                   | [<span data-ttu-id="6109f-148">GUID de sous-type de flux</span><span class="sxs-lookup"><span data-stu-id="6109f-148">Stream Subtype GUIDs</span></span>](stream-subtype-guids.md)     |
| <span data-ttu-id="6109f-149">**\_Vidéo MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="6109f-149">**MFMediaType\_Video**</span></span>        | <span data-ttu-id="6109f-150">Vidéo.</span><span class="sxs-lookup"><span data-stu-id="6109f-150">Video.</span></span>                                                                                                                                                     | <span data-ttu-id="6109f-151">[GUID de sous-type de vidéo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="6109f-151">[Video Subtype GUIDs](video-subtype-guids.md).</span></span>      |



 

<span data-ttu-id="6109f-152">Les composants tiers peuvent définir de nouveaux types principaux et de nouveaux sous-types.</span><span class="sxs-lookup"><span data-stu-id="6109f-152">Third-party components can define new major types and new subtypes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6109f-153">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6109f-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6109f-154">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="6109f-154">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="6109f-155">Types de médias</span><span class="sxs-lookup"><span data-stu-id="6109f-155">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 
