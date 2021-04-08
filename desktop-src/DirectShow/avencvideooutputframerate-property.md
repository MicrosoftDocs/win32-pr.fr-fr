---
description: Spécifie la fréquence d’images sur le flux de sortie de l’encodeur, en images par seconde.
ms.assetid: 72e16c7d-977e-4269-9576-afc789e31826
title: Propriété AVEncVideoOutputFrameRate (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad4cb675c266d146936a3402934e51486ded5b02
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746229"
---
# <a name="avencvideooutputframerate-property"></a><span data-ttu-id="7e018-103">Propriété AVEncVideoOutputFrameRate</span><span class="sxs-lookup"><span data-stu-id="7e018-103">AVEncVideoOutputFrameRate property</span></span>

<span data-ttu-id="7e018-104">Spécifie la fréquence d’images sur le flux de sortie de l’encodeur, en images par seconde.</span><span class="sxs-lookup"><span data-stu-id="7e018-104">Specifies the frame rate on the encoder's output stream, in frames per second.</span></span>

<span data-ttu-id="7e018-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="7e018-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="7e018-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="7e018-106">Data type</span></span>

<span data-ttu-id="7e018-107">**UINT64** (**VT \_ UI8**)</span><span class="sxs-lookup"><span data-stu-id="7e018-107">**UINT64** (**VT\_UI8**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="7e018-108">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="7e018-108">Property GUID</span></span>

<span data-ttu-id="7e018-109">**CODECAPI \_ AVEncVideoOutputFrameRate**</span><span class="sxs-lookup"><span data-stu-id="7e018-109">**CODECAPI\_AVEncVideoOutputFrameRate**</span></span>

## <a name="property-value"></a><span data-ttu-id="7e018-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="7e018-110">Property value</span></span>

<span data-ttu-id="7e018-111">La valeur de cette propriété est un ratio qui définit la fréquence d’images.</span><span class="sxs-lookup"><span data-stu-id="7e018-111">The value of this property is a ratio that defines the frame rate.</span></span> <span data-ttu-id="7e018-112">Les 32 bits supérieurs contiennent le numérateur et les 32 bits inférieurs contiennent le dénominateur.</span><span class="sxs-lookup"><span data-stu-id="7e018-112">The upper 32 bits contain the numerator, and the lower 32 bits contain the denominator.</span></span> <span data-ttu-id="7e018-113">Le tableau suivant présente les fréquences d’images courantes, en images par seconde.</span><span class="sxs-lookup"><span data-stu-id="7e018-113">The following table shows common frame rates, in frames per second.</span></span>



| <span data-ttu-id="7e018-114">Fréquence d’images</span><span class="sxs-lookup"><span data-stu-id="7e018-114">Frame rate</span></span> | <span data-ttu-id="7e018-115">Proportions</span><span class="sxs-lookup"><span data-stu-id="7e018-115">Ratio</span></span>      |
|------------|------------|
| <span data-ttu-id="7e018-116">23,97</span><span class="sxs-lookup"><span data-stu-id="7e018-116">23.97</span></span>      | <span data-ttu-id="7e018-117">24000/1001</span><span class="sxs-lookup"><span data-stu-id="7e018-117">24000/1001</span></span> |
| <span data-ttu-id="7e018-118">24</span><span class="sxs-lookup"><span data-stu-id="7e018-118">24</span></span>         | <span data-ttu-id="7e018-119">24/1</span><span class="sxs-lookup"><span data-stu-id="7e018-119">24/1</span></span>       |
| <span data-ttu-id="7e018-120">25</span><span class="sxs-lookup"><span data-stu-id="7e018-120">25</span></span>         | <span data-ttu-id="7e018-121">25/1</span><span class="sxs-lookup"><span data-stu-id="7e018-121">25/1</span></span>       |
| <span data-ttu-id="7e018-122">29,97</span><span class="sxs-lookup"><span data-stu-id="7e018-122">29.97</span></span>      | <span data-ttu-id="7e018-123">30000/1001</span><span class="sxs-lookup"><span data-stu-id="7e018-123">30000/1001</span></span> |
| <span data-ttu-id="7e018-124">30</span><span class="sxs-lookup"><span data-stu-id="7e018-124">30</span></span>         | <span data-ttu-id="7e018-125">30/1</span><span class="sxs-lookup"><span data-stu-id="7e018-125">30/1</span></span>       |
| <span data-ttu-id="7e018-126">50</span><span class="sxs-lookup"><span data-stu-id="7e018-126">50</span></span>         | <span data-ttu-id="7e018-127">50/1</span><span class="sxs-lookup"><span data-stu-id="7e018-127">50/1</span></span>       |
| <span data-ttu-id="7e018-128">59,94</span><span class="sxs-lookup"><span data-stu-id="7e018-128">59.94</span></span>      | <span data-ttu-id="7e018-129">60000/1001</span><span class="sxs-lookup"><span data-stu-id="7e018-129">60000/1001</span></span> |
| <span data-ttu-id="7e018-130">60</span><span class="sxs-lookup"><span data-stu-id="7e018-130">60</span></span>         | <span data-ttu-id="7e018-131">60/1</span><span class="sxs-lookup"><span data-stu-id="7e018-131">60/1</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="7e018-132">Notes</span><span class="sxs-lookup"><span data-stu-id="7e018-132">Remarks</span></span>

<span data-ttu-id="7e018-133">Les applications peuvent définir cette propriété pour spécifier la fréquence d’images de sortie.</span><span class="sxs-lookup"><span data-stu-id="7e018-133">Applications can set this property to specify the output frame rate.</span></span> <span data-ttu-id="7e018-134">Les encodeurs peuvent également retourner cette propriété en tant que fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="7e018-134">Encoders can also return this property as a capability.</span></span> <span data-ttu-id="7e018-135">En fonction de l’encodeur, la valeur peut être limitée à la fréquence d’images d’entrée.</span><span class="sxs-lookup"><span data-stu-id="7e018-135">Depending on the encoder, the value might be restricted to the input frame rate.</span></span> <span data-ttu-id="7e018-136">Si ce n’est pas le cas, l’encodeur est en mesure de convertir la fréquence d’images en interne.</span><span class="sxs-lookup"><span data-stu-id="7e018-136">If not, the encoder is able to convert the frame rate internally.</span></span> <span data-ttu-id="7e018-137">Consultez la [**propriété AVEncVideoOutputFrameRateConversion**](avencvideooutputframerateconversion-property.md).</span><span class="sxs-lookup"><span data-stu-id="7e018-137">See [**AVEncVideoOutputFrameRateConversion Property**](avencvideooutputframerateconversion-property.md).</span></span>

<span data-ttu-id="7e018-138">Cette propriété est également utilisée avec les [encodeurs de caméra H. 264 UVC 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span><span class="sxs-lookup"><span data-stu-id="7e018-138">This property is also used with [H.264 UVC 1.5 camera encoders](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span></span>

## <a name="requirements"></a><span data-ttu-id="7e018-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e018-139">Requirements</span></span>



| <span data-ttu-id="7e018-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e018-140">Requirement</span></span> | <span data-ttu-id="7e018-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e018-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7e018-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e018-142">Minimum supported client</span></span><br/> | <span data-ttu-id="7e018-143">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="7e018-143">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="7e018-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e018-144">Minimum supported server</span></span><br/> | <span data-ttu-id="7e018-145">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="7e018-145">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="7e018-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="7e018-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e018-147"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e018-147"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e018-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e018-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e018-149">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="7e018-149">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="7e018-150">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="7e018-150">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

