---
description: Spécifie les modes de contrôle de fréquence pris en charge pour un flux vidéo H. 264.
ms.assetid: DAA62ECD-AFA2-40C2-9B52-F2D581F4D894
title: Attribut MF_MT_H264_SUPPORTED_RATE_CONTROL_MODES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c7b315bf41d662dd5abb283c346710f485789ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544229"
---
# <a name="mf_mt_h264_supported_rate_control_modes-attribute"></a><span data-ttu-id="b2f32-103">\_Attribut de \_ \_ mode de \_ contrôle de taux pris en charge \_ \_ pour MF MT H264 –</span><span class="sxs-lookup"><span data-stu-id="b2f32-103">MF\_MT\_H264\_SUPPORTED\_RATE\_CONTROL\_MODES attribute</span></span>

<span data-ttu-id="b2f32-104">Spécifie les modes de contrôle de fréquence pris en charge pour un flux vidéo H. 264.</span><span class="sxs-lookup"><span data-stu-id="b2f32-104">Specifies the supported rate-control modes for an H.264 video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="b2f32-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="b2f32-105">Data type</span></span>

<span data-ttu-id="b2f32-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b2f32-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="b2f32-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="b2f32-107">Get/set</span></span>

<span data-ttu-id="b2f32-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="b2f32-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="b2f32-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="b2f32-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="b2f32-110">S’applique à</span><span class="sxs-lookup"><span data-stu-id="b2f32-110">Applies to</span></span>

[<span data-ttu-id="b2f32-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="b2f32-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="b2f32-112">Notes</span><span class="sxs-lookup"><span data-stu-id="b2f32-112">Remarks</span></span>

<span data-ttu-id="b2f32-113">Cet attribut s’applique aux types de média pour les flux H. 264 transmis sur USB.</span><span class="sxs-lookup"><span data-stu-id="b2f32-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="b2f32-114">La valeur correspond au champ **bmSupportedRateControlModes** dans le descripteur de format vidéo 1,5 UVC H. 264.</span><span class="sxs-lookup"><span data-stu-id="b2f32-114">The value corresponds to the **bmSupportedRateControlModes** field in the UVC 1.5 H.264 video format descriptor.</span></span>

<span data-ttu-id="b2f32-115">Cet attribut est également utilisé avec les [encodeurs de caméra H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="b2f32-115">This attribute is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b2f32-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b2f32-116">Requirements</span></span>



| <span data-ttu-id="b2f32-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b2f32-117">Requirement</span></span> | <span data-ttu-id="b2f32-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2f32-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b2f32-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2f32-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b2f32-120">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b2f32-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="b2f32-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2f32-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b2f32-122">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="b2f32-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="b2f32-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="b2f32-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2f32-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2f32-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2f32-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2f32-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2f32-126">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b2f32-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b2f32-127">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="b2f32-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




