---
description: Spécifie le taux de traitement bloc macro maximal pour un flux vidéo H. 264.
ms.assetid: 882F54D1-A963-4016-BEC7-F9C1AC5885FD
title: Attribut MF_MT_H264_MAX_MB_PER_SEC (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b53bdbabd9a633464ed388f2309627b69413c27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518382"
---
# <a name="mf_mt_h264_max_mb_per_sec-attribute"></a><span data-ttu-id="8470f-103">\_Attribut de \_ \_ nombre maximal de \_ Mo \_ par \_ seconde pour MF MT H264 –</span><span class="sxs-lookup"><span data-stu-id="8470f-103">MF\_MT\_H264\_MAX\_MB\_PER\_SEC attribute</span></span>

<span data-ttu-id="8470f-104">Spécifie le taux de traitement bloc macro maximal pour un flux vidéo H. 264.</span><span class="sxs-lookup"><span data-stu-id="8470f-104">Specifies the maximum macroblock processing rate for an H.264 video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="8470f-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="8470f-105">Data type</span></span>

<span data-ttu-id="8470f-106">**\[ UInt32 \]** stocké en tant que **UINT8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="8470f-106">**UINT32\[\]** stored as **UINT8\[\]**</span></span>

## <a name="applies-to"></a><span data-ttu-id="8470f-107">S’applique à</span><span class="sxs-lookup"><span data-stu-id="8470f-107">Applies to</span></span>

[<span data-ttu-id="8470f-108">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="8470f-108">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="8470f-109">Notes</span><span class="sxs-lookup"><span data-stu-id="8470f-109">Remarks</span></span>

<span data-ttu-id="8470f-110">Cet attribut s’applique aux types de média pour les flux H. 264 transmis sur USB.</span><span class="sxs-lookup"><span data-stu-id="8470f-110">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="8470f-111">La valeur de l’attribut est un tableau de valeurs UINT32 qui correspondent aux champs suivants dans le descripteur de format vidéo UVC 1,5 H. 264.</span><span class="sxs-lookup"><span data-stu-id="8470f-111">The value of the attribute is an array of UINT32 values, which correspond to the following fields in the UVC 1.5 H.264 video format descriptor.</span></span>

| <span data-ttu-id="8470f-112">Élément de tableau</span><span class="sxs-lookup"><span data-stu-id="8470f-112">Array Element</span></span> | <span data-ttu-id="8470f-113">Champ de descripteur</span><span class="sxs-lookup"><span data-stu-id="8470f-113">Descriptor Field</span></span>                                           |
|---------------|------------------------------------------------------------|
| <span data-ttu-id="8470f-114">0</span><span class="sxs-lookup"><span data-stu-id="8470f-114">0</span></span>             | <span data-ttu-id="8470f-115">**dwMaxMBperSecOneResolutionNoScalability**</span><span class="sxs-lookup"><span data-stu-id="8470f-115">**dwMaxMBperSecOneResolutionNoScalability**</span></span>                |
| <span data-ttu-id="8470f-116">1</span><span class="sxs-lookup"><span data-stu-id="8470f-116">1</span></span>             | <span data-ttu-id="8470f-117">**dwMaxMBperSecTwoResolutionsNoScalability**</span><span class="sxs-lookup"><span data-stu-id="8470f-117">**dwMaxMBperSecTwoResolutionsNoScalability**</span></span>               |
| <span data-ttu-id="8470f-118">2</span><span class="sxs-lookup"><span data-stu-id="8470f-118">2</span></span>             | <span data-ttu-id="8470f-119">**dwMaxMBperSecThreeResolutionsNoScalability**</span><span class="sxs-lookup"><span data-stu-id="8470f-119">**dwMaxMBperSecThreeResolutionsNoScalability**</span></span>             |
| <span data-ttu-id="8470f-120">3</span><span class="sxs-lookup"><span data-stu-id="8470f-120">3</span></span>             | <span data-ttu-id="8470f-121">**dwMaxMBperSecFourResolutionsNoScalability**</span><span class="sxs-lookup"><span data-stu-id="8470f-121">**dwMaxMBperSecFourResolutionsNoScalability**</span></span>              |
| <span data-ttu-id="8470f-122">4</span><span class="sxs-lookup"><span data-stu-id="8470f-122">4</span></span>             | <span data-ttu-id="8470f-123">**dwMaxMBperSecOneResolutionTemporalScalability**</span><span class="sxs-lookup"><span data-stu-id="8470f-123">**dwMaxMBperSecOneResolutionTemporalScalability**</span></span>          |
| <span data-ttu-id="8470f-124">5</span><span class="sxs-lookup"><span data-stu-id="8470f-124">5</span></span>             | <span data-ttu-id="8470f-125">**dwMaxMBperSecTwoResolutionsTemporalScalablility**</span><span class="sxs-lookup"><span data-stu-id="8470f-125">**dwMaxMBperSecTwoResolutionsTemporalScalablility**</span></span>        |
| <span data-ttu-id="8470f-126">6</span><span class="sxs-lookup"><span data-stu-id="8470f-126">6</span></span>             | <span data-ttu-id="8470f-127">**dwMaxMBperSecThreeResolutionsTemporalScalability**</span><span class="sxs-lookup"><span data-stu-id="8470f-127">**dwMaxMBperSecThreeResolutionsTemporalScalability**</span></span>       |
| <span data-ttu-id="8470f-128">7</span><span class="sxs-lookup"><span data-stu-id="8470f-128">7</span></span>             | <span data-ttu-id="8470f-129">**dwMaxMBperSecFourResolutionsTemporalScalability**</span><span class="sxs-lookup"><span data-stu-id="8470f-129">**dwMaxMBperSecFourResolutionsTemporalScalability**</span></span>        |
| <span data-ttu-id="8470f-130">8</span><span class="sxs-lookup"><span data-stu-id="8470f-130">8</span></span>             | <span data-ttu-id="8470f-131">**dwMaxMBperSecOneResolutionTemporalQualityScalability**</span><span class="sxs-lookup"><span data-stu-id="8470f-131">**dwMaxMBperSecOneResolutionTemporalQualityScalability**</span></span>   |
| <span data-ttu-id="8470f-132">9</span><span class="sxs-lookup"><span data-stu-id="8470f-132">9</span></span>             | <span data-ttu-id="8470f-133">**dwMaxMBperSecTwoResolutionsTemporalQualityScalability**</span><span class="sxs-lookup"><span data-stu-id="8470f-133">**dwMaxMBperSecTwoResolutionsTemporalQualityScalability**</span></span>  |
| <span data-ttu-id="8470f-134">10</span><span class="sxs-lookup"><span data-stu-id="8470f-134">10</span></span>            | <span data-ttu-id="8470f-135">**dwMaxMBperSecThreeResolutionsTemporalQualityScalablity**</span><span class="sxs-lookup"><span data-stu-id="8470f-135">**dwMaxMBperSecThreeResolutionsTemporalQualityScalablity**</span></span> |
| <span data-ttu-id="8470f-136">11</span><span class="sxs-lookup"><span data-stu-id="8470f-136">11</span></span>            | <span data-ttu-id="8470f-137">**dwMaxMBperSecFourResolutionsTemporalQualityScalability**</span><span class="sxs-lookup"><span data-stu-id="8470f-137">**dwMaxMBperSecFourResolutionsTemporalQualityScalability**</span></span> |
| <span data-ttu-id="8470f-138">12</span><span class="sxs-lookup"><span data-stu-id="8470f-138">12</span></span>            | <span data-ttu-id="8470f-139">**dwMaxMBperSecOneResolutionFullScalability**</span><span class="sxs-lookup"><span data-stu-id="8470f-139">**dwMaxMBperSecOneResolutionFullScalability**</span></span>              |
| <span data-ttu-id="8470f-140">13</span><span class="sxs-lookup"><span data-stu-id="8470f-140">13</span></span>            | <span data-ttu-id="8470f-141">**dwMaxMBperSecTwoResolutionsFullScalability**</span><span class="sxs-lookup"><span data-stu-id="8470f-141">**dwMaxMBperSecTwoResolutionsFullScalability**</span></span>             |
| <span data-ttu-id="8470f-142">14</span><span class="sxs-lookup"><span data-stu-id="8470f-142">14</span></span>            | <span data-ttu-id="8470f-143">**dwMaxMBperSecThreeResolutionsFullScalability**</span><span class="sxs-lookup"><span data-stu-id="8470f-143">**dwMaxMBperSecThreeResolutionsFullScalability**</span></span>           |
| <span data-ttu-id="8470f-144">15</span><span class="sxs-lookup"><span data-stu-id="8470f-144">15</span></span>            | <span data-ttu-id="8470f-145">**dwMaxMBperSecFourResolutionsFullScalability**</span><span class="sxs-lookup"><span data-stu-id="8470f-145">**dwMaxMBperSecFourResolutionsFullScalability**</span></span>            |



 

<span data-ttu-id="8470f-146">Cet attribut est également utilisé avec les [encodeurs de caméra H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="8470f-146">This attribute is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8470f-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8470f-147">Requirements</span></span>



| <span data-ttu-id="8470f-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8470f-148">Requirement</span></span> | <span data-ttu-id="8470f-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="8470f-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8470f-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8470f-150">Minimum supported client</span></span><br/> | <span data-ttu-id="8470f-151">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="8470f-151">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="8470f-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8470f-152">Minimum supported server</span></span><br/> | <span data-ttu-id="8470f-153">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="8470f-153">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="8470f-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="8470f-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="8470f-155"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8470f-155"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8470f-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8470f-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8470f-157">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8470f-157">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8470f-158">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="8470f-158">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




