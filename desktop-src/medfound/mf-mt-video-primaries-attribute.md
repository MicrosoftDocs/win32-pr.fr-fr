---
description: Spécifie les couleurs primaires d’un type de média vidéo.
ms.assetid: 56f31c1a-b610-4da0-9df4-76e15add672c
title: Attribut MF_MT_VIDEO_PRIMARIES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6cdf26a3f49c7e2bb3aa0f48c52c9b283edd8cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521965"
---
# <a name="mf_mt_video_primaries-attribute"></a><span data-ttu-id="0376f-103">\_Attribut des \_ primaires de vidéos MF MT \_</span><span class="sxs-lookup"><span data-stu-id="0376f-103">MF\_MT\_VIDEO\_PRIMARIES attribute</span></span>

<span data-ttu-id="0376f-104">Spécifie les couleurs primaires d’un type de média vidéo.</span><span class="sxs-lookup"><span data-stu-id="0376f-104">Specifies the color primaries for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="0376f-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="0376f-105">Data type</span></span>

<span data-ttu-id="0376f-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0376f-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="0376f-107">Notes</span><span class="sxs-lookup"><span data-stu-id="0376f-107">Remarks</span></span>

<span data-ttu-id="0376f-108">La valeur de cet attribut est un membre de l’énumération [**MFVideoPrimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) .</span><span class="sxs-lookup"><span data-stu-id="0376f-108">The value of this attribute is a member of the [**MFVideoPrimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) enumeration.</span></span>

<span data-ttu-id="0376f-109">L’énumération [**MFVideoPrimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) identifie les couleurs primaires associées à certaines normes vidéo courantes.</span><span class="sxs-lookup"><span data-stu-id="0376f-109">The [**MFVideoPrimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) enumeration identifies color primaries associated with certain common video standards.</span></span> <span data-ttu-id="0376f-110">Si le type de média utilise des couleurs primaires qui ne sont pas identifiées dans l’énumération **MFVideoPrimaries** , définissez l’attribut de préversions de [**\_ \_ \_ vidéo personnalisée \_ MF MT personnalisé**](mf-mt-custom-video-primaries-attribute.md) au lieu de cet attribut.</span><span class="sxs-lookup"><span data-stu-id="0376f-110">If the media type uses color primaries that are not identified in the **MFVideoPrimaries** enumeration, set the [**MF\_MT\_CUSTOM\_VIDEO\_PRIMARIES**](mf-mt-custom-video-primaries-attribute.md) attribute instead of this attribute.</span></span>

<span data-ttu-id="0376f-111">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="0376f-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0376f-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0376f-112">Requirements</span></span>



| <span data-ttu-id="0376f-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0376f-113">Requirement</span></span> | <span data-ttu-id="0376f-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="0376f-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0376f-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0376f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0376f-116">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="0376f-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="0376f-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0376f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0376f-118">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="0376f-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="0376f-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="0376f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="0376f-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0376f-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0376f-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0376f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0376f-122">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0376f-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0376f-123">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="0376f-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="0376f-124">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="0376f-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="0376f-125">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="0376f-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="0376f-126">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="0376f-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="0376f-127">Informations sur les couleurs étendues</span><span class="sxs-lookup"><span data-stu-id="0376f-127">Extended Color Information</span></span>](extended-color-information.md)
</dt> </dl>

 

 




