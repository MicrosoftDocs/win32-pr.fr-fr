---
description: Fréquence d’images maximale prise en charge par un périphérique de capture vidéo, en images par seconde.
ms.assetid: 8e0c4996-9f78-424e-b012-502228b6a27a
title: Attribut MF_MT_FRAME_RATE_RANGE_MAX (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62399445cd31c7820ea9de7082fce71febbf3ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951535"
---
# <a name="mf_mt_frame_rate_range_max-attribute"></a><span data-ttu-id="76fc1-103">\_ \_ \_ \_ \_ Attribut max de la plage de fréquence d’images MF MT</span><span class="sxs-lookup"><span data-stu-id="76fc1-103">MF\_MT\_FRAME\_RATE\_RANGE\_MAX attribute</span></span>

<span data-ttu-id="76fc1-104">Fréquence d’images maximale prise en charge par un périphérique de capture vidéo, en images par seconde.</span><span class="sxs-lookup"><span data-stu-id="76fc1-104">The maximum frame rate that is supported by a video capture device, in frames per second.</span></span>

## <a name="data-type"></a><span data-ttu-id="76fc1-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="76fc1-105">Data type</span></span>

<span data-ttu-id="76fc1-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="76fc1-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="76fc1-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="76fc1-107">Get/set</span></span>

<span data-ttu-id="76fc1-108">Pour récupérer cet attribut, appelez [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).</span><span class="sxs-lookup"><span data-stu-id="76fc1-108">To get this attribute, call [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).</span></span>

<span data-ttu-id="76fc1-109">Pour définir cet attribut, appelez [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).</span><span class="sxs-lookup"><span data-stu-id="76fc1-109">To set this attribute, call [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).</span></span>

## <a name="remarks"></a><span data-ttu-id="76fc1-110">Notes</span><span class="sxs-lookup"><span data-stu-id="76fc1-110">Remarks</span></span>

<span data-ttu-id="76fc1-111">La fréquence d’images est exprimée sous la forme d’un rapport.</span><span class="sxs-lookup"><span data-stu-id="76fc1-111">The frame rate is expressed as a ratio.</span></span> <span data-ttu-id="76fc1-112">Les 32 bits supérieurs de la valeur d’attribut contiennent le numérateur, et les 32 de bits inférieurs contiennent le dénominateur.</span><span class="sxs-lookup"><span data-stu-id="76fc1-112">The upper 32 bits of the attribute value contain the numerator, and the lower 32 bits contain the denominator.</span></span> <span data-ttu-id="76fc1-113">Par exemple, si la fréquence d’images est de 30 images par seconde (FPS), le ratio est de 30/1.</span><span class="sxs-lookup"><span data-stu-id="76fc1-113">For example, if the frame rate is 30 frames per second (fps), the ratio is 30/1.</span></span>

<span data-ttu-id="76fc1-114">Si l’appareil de capture signale une fréquence d’images maximale, la source du média définit cet attribut sur le type de média.</span><span class="sxs-lookup"><span data-stu-id="76fc1-114">If the capture device reports a maximum frame rate, the media source sets this attribute on the media type.</span></span> <span data-ttu-id="76fc1-115">La fréquence d’images minimale est indiquée dans l’attribut min Mt de la plage de fréquences d' [ \_ \_ images \_ \_ \_ MT](mf-mt-frame-rate-range-min.md) .</span><span class="sxs-lookup"><span data-stu-id="76fc1-115">The minimum frame rate is given in the [MF\_MT\_FRAME\_RATE\_RANGE\_MIN](mf-mt-frame-rate-range-min.md) attribute.</span></span> <span data-ttu-id="76fc1-116">Il n’est pas garanti que l’appareil prenne en charge chaque incrément dans cette plage.</span><span class="sxs-lookup"><span data-stu-id="76fc1-116">The device is not guaranteed to support every increment within this range.</span></span>

<span data-ttu-id="76fc1-117">Pour définir la fréquence d’images de l’appareil, commencez par modifier la valeur de l’attribut de [**\_ \_ \_ fréquence d’images MF MF**](mf-mt-frame-rate-attribute.md) sur le type de média.</span><span class="sxs-lookup"><span data-stu-id="76fc1-117">To set the device's frame rate, first modify the value of the [**MF\_MT\_FRAME\_RATE**](mf-mt-frame-rate-attribute.md) attribute on the media type.</span></span> <span data-ttu-id="76fc1-118">Définissez ensuite le type de média sur la source du média.</span><span class="sxs-lookup"><span data-stu-id="76fc1-118">Then set the media type on the media source.</span></span>

<span data-ttu-id="76fc1-119">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="76fc1-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="76fc1-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="76fc1-120">Requirements</span></span>



| <span data-ttu-id="76fc1-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="76fc1-121">Requirement</span></span> | <span data-ttu-id="76fc1-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="76fc1-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="76fc1-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76fc1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="76fc1-124">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="76fc1-124">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="76fc1-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76fc1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="76fc1-126">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="76fc1-126">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="76fc1-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="76fc1-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="76fc1-128"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="76fc1-128"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76fc1-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76fc1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76fc1-130">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="76fc1-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="76fc1-131">Comment définir la fréquence d’images de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="76fc1-131">How to Set the Video Capture Frame Rate</span></span>](how-to-set-the-video-capture-frame-rate.md)
</dt> <dt>

[<span data-ttu-id="76fc1-132">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="76fc1-132">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="76fc1-133">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="76fc1-133">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="76fc1-134">plage de fréquence d’images MF- \_ \_ \_ \_ \_ min</span><span class="sxs-lookup"><span data-stu-id="76fc1-134">MF\_MT\_FRAME\_RATE\_RANGE\_MIN</span></span>](mf-mt-frame-rate-range-min.md)
</dt> </dl>

 

 




