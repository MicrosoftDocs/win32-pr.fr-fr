---
description: Spécifie les modes de tranche pris en charge pour un flux vidéo H. 264.
ms.assetid: 72DA62EC-A509-4C3B-A51D-7313C176AAA9
title: Attribut MF_MT_H264_SUPPORTED_SLICE_MODES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9258a2ce2b9bef050fc6ea4468026539ff67f1be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516488"
---
# <a name="mf_mt_h264_supported_slice_modes-attribute"></a><span data-ttu-id="2aa8f-103">MF \_ MT \_ H264 – \_ - \_ attribut de mode de tranche pris en charge \_</span><span class="sxs-lookup"><span data-stu-id="2aa8f-103">MF\_MT\_H264\_SUPPORTED\_SLICE\_MODES attribute</span></span>

<span data-ttu-id="2aa8f-104">Spécifie les modes de tranche pris en charge pour un flux vidéo H. 264.</span><span class="sxs-lookup"><span data-stu-id="2aa8f-104">Specifies the supported slice modes for an H.264 video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="2aa8f-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="2aa8f-105">Data type</span></span>

<span data-ttu-id="2aa8f-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="2aa8f-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="2aa8f-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="2aa8f-107">Get/set</span></span>

<span data-ttu-id="2aa8f-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="2aa8f-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="2aa8f-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="2aa8f-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="2aa8f-110">S’applique à</span><span class="sxs-lookup"><span data-stu-id="2aa8f-110">Applies to</span></span>

[<span data-ttu-id="2aa8f-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="2aa8f-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="2aa8f-112">Notes</span><span class="sxs-lookup"><span data-stu-id="2aa8f-112">Remarks</span></span>

<span data-ttu-id="2aa8f-113">Cet attribut s’applique aux types de média pour les flux H. 264 transmis sur USB.</span><span class="sxs-lookup"><span data-stu-id="2aa8f-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="2aa8f-114">La valeur correspond au champ **bmSupportedSliceModes** dans le descripteur de format vidéo 1,5 UVC H. 264.</span><span class="sxs-lookup"><span data-stu-id="2aa8f-114">The value corresponds to the **bmSupportedSliceModes** field in the UVC 1.5 H.264 video format descriptor.</span></span>

<span data-ttu-id="2aa8f-115">Cet attribut est également utilisé avec les [encodeurs de caméra H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="2aa8f-115">This attribute is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2aa8f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2aa8f-116">Requirements</span></span>



| <span data-ttu-id="2aa8f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2aa8f-117">Requirement</span></span> | <span data-ttu-id="2aa8f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="2aa8f-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2aa8f-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2aa8f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2aa8f-120">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2aa8f-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="2aa8f-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2aa8f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2aa8f-122">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="2aa8f-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="2aa8f-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="2aa8f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2aa8f-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2aa8f-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2aa8f-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2aa8f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2aa8f-126">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2aa8f-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2aa8f-127">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="2aa8f-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




