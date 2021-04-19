---
description: Nombre maximal de frames que l’encodeur H. 264 prend pour répondre à une commande.
ms.assetid: C856B2B0-4A06-436D-B589-B01DA86DB53D
title: Attribut MF_MT_H264_MAX_CODEC_CONFIG_DELAY (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a835d5b5a37be0c722f313aaf4fe8ed8aa55f00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518641"
---
# <a name="mf_mt_h264_max_codec_config_delay-attribute"></a><span data-ttu-id="e76eb-103">\_Attribut de \_ \_ délai de \_ configuration du codec Max H264 – \_ MF \_ MT</span><span class="sxs-lookup"><span data-stu-id="e76eb-103">MF\_MT\_H264\_MAX\_CODEC\_CONFIG\_DELAY attribute</span></span>

<span data-ttu-id="e76eb-104">Nombre maximal de frames que l’encodeur H. 264 prend pour répondre à une commande.</span><span class="sxs-lookup"><span data-stu-id="e76eb-104">The maximum number of frames the H.264 encoder takes to respond to a command.</span></span>

## <a name="data-type"></a><span data-ttu-id="e76eb-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="e76eb-105">Data type</span></span>

<span data-ttu-id="e76eb-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e76eb-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="e76eb-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="e76eb-107">Get/set</span></span>

<span data-ttu-id="e76eb-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="e76eb-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="e76eb-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="e76eb-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="e76eb-110">S’applique à</span><span class="sxs-lookup"><span data-stu-id="e76eb-110">Applies to</span></span>

[<span data-ttu-id="e76eb-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="e76eb-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="e76eb-112">Notes</span><span class="sxs-lookup"><span data-stu-id="e76eb-112">Remarks</span></span>

<span data-ttu-id="e76eb-113">Cet attribut s’applique aux types de média pour les flux H. 264 transmis sur USB.</span><span class="sxs-lookup"><span data-stu-id="e76eb-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="e76eb-114">La valeur correspond au champ **bMaxCodecConfigDelay** dans le descripteur de format vidéo 1,2 UVC H. 264.</span><span class="sxs-lookup"><span data-stu-id="e76eb-114">The value corresponds to the **bMaxCodecConfigDelay** field in the UVC 1.2 H.264 video format descriptor.</span></span>

<span data-ttu-id="e76eb-115">Cet attribut est également utilisé avec les [encodeurs de caméra H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="e76eb-115">This attribute is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e76eb-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e76eb-116">Requirements</span></span>



| <span data-ttu-id="e76eb-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e76eb-117">Requirement</span></span> | <span data-ttu-id="e76eb-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="e76eb-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e76eb-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e76eb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e76eb-120">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e76eb-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="e76eb-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e76eb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e76eb-122">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="e76eb-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="e76eb-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="e76eb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e76eb-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e76eb-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e76eb-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e76eb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e76eb-126">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e76eb-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e76eb-127">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="e76eb-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




