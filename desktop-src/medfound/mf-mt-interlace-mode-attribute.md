---
description: Décrit comment les frames d’un type de média vidéo sont entrelacés.
ms.assetid: 19aa0147-ac49-4a2e-ac75-e967fec9ca68
title: Attribut MF_MT_INTERLACE_MODE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1826978c39ff8cd80b2aa66b91161ee8b476944f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113427"
---
# <a name="mf_mt_interlace_mode-attribute"></a><span data-ttu-id="d7fdd-103">\_ \_ Attribut mode entrelacé MF MT \_</span><span class="sxs-lookup"><span data-stu-id="d7fdd-103">MF\_MT\_INTERLACE\_MODE attribute</span></span>

<span data-ttu-id="d7fdd-104">Décrit comment les frames d’un type de média vidéo sont entrelacés.</span><span class="sxs-lookup"><span data-stu-id="d7fdd-104">Describes how the frames in a video media type are interlaced.</span></span>

## <a name="data-type"></a><span data-ttu-id="d7fdd-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="d7fdd-105">Data type</span></span>

<span data-ttu-id="d7fdd-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d7fdd-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="d7fdd-107">Notes</span><span class="sxs-lookup"><span data-stu-id="d7fdd-107">Remarks</span></span>

<span data-ttu-id="d7fdd-108">La valeur de cet attribut est un membre de l’énumération [**MFVideoInterlaceMode**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideointerlacemode) .</span><span class="sxs-lookup"><span data-stu-id="d7fdd-108">The value of this attribute is a member of the [**MFVideoInterlaceMode**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideointerlacemode) enumeration.</span></span>

<span data-ttu-id="d7fdd-109">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="d7fdd-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7fdd-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7fdd-110">Requirements</span></span>



| <span data-ttu-id="d7fdd-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7fdd-111">Requirement</span></span> | <span data-ttu-id="d7fdd-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7fdd-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d7fdd-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7fdd-113">Minimum supported client</span></span><br/> | <span data-ttu-id="d7fdd-114">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="d7fdd-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="d7fdd-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7fdd-115">Minimum supported server</span></span><br/> | <span data-ttu-id="d7fdd-116">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="d7fdd-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="d7fdd-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="d7fdd-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7fdd-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7fdd-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7fdd-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7fdd-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7fdd-120">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d7fdd-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d7fdd-121">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="d7fdd-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="d7fdd-122">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="d7fdd-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="d7fdd-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="d7fdd-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="d7fdd-124">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="d7fdd-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="d7fdd-125">Entrelacement de vidéos</span><span class="sxs-lookup"><span data-stu-id="d7fdd-125">Video Interlacing</span></span>](video-interlacing.md)
</dt> </dl>

 

 




