---
description: Code d’heure de début de groupe d’images (GOP) pour un type de média vidéo MPEG-1 ou MPEG-2.
ms.assetid: 8313b83c-5a0a-4aaa-bdc8-58a987c329c7
title: Attribut MF_MT_MPEG_START_TIME_CODE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73b19a041dbcd791359d704b407445779927d0fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530636"
---
# <a name="mf_mt_mpeg_start_time_code-attribute"></a><span data-ttu-id="374f9-103">Attribut de code de l' \_ heure de début du MPEG MF MT \_ \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="374f9-103">MF\_MT\_MPEG\_START\_TIME\_CODE attribute</span></span>

<span data-ttu-id="374f9-104">Code d’heure de début de groupe d’images (GOP) pour un type de média vidéo MPEG-1 ou MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="374f9-104">Group-of-pictures (GOP) start time code, for an MPEG-1 or MPEG-2 video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="374f9-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="374f9-105">Data type</span></span>

<span data-ttu-id="374f9-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="374f9-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="374f9-107">Notes</span><span class="sxs-lookup"><span data-stu-id="374f9-107">Remarks</span></span>

<span data-ttu-id="374f9-108">Cet attribut correspond au membre **dwStartTimeCode** des structures [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) et [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="374f9-108">This attribute corresponds to the **dwStartTimeCode** member of the [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) and [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structures.</span></span>

<span data-ttu-id="374f9-109">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="374f9-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="374f9-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="374f9-110">Requirements</span></span>



| <span data-ttu-id="374f9-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="374f9-111">Requirement</span></span> | <span data-ttu-id="374f9-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="374f9-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="374f9-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="374f9-113">Minimum supported client</span></span><br/> | <span data-ttu-id="374f9-114">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="374f9-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="374f9-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="374f9-115">Minimum supported server</span></span><br/> | <span data-ttu-id="374f9-116">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="374f9-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="374f9-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="374f9-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="374f9-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="374f9-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="374f9-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="374f9-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="374f9-120">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="374f9-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="374f9-121">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="374f9-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="374f9-122">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="374f9-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="374f9-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="374f9-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="374f9-124">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="374f9-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="374f9-125">Attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="374f9-125">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 
