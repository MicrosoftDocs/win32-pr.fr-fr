---
description: Décrit comment chroma a été échantillonné pour un type de média vidéo YCbCr.
ms.assetid: 0c930348-8669-42cc-9d74-df9ef475bdc8
title: Attribut MF_MT_VIDEO_CHROMA_SITING (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa634cf9a9ca7f5c292eb0cf06c6a1a14c788d43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520584"
---
# <a name="mf_mt_video_chroma_siting-attribute"></a><span data-ttu-id="270b3-103">MF \_ MT \_ vidéo \_ Chroma emplacement \_ attribut</span><span class="sxs-lookup"><span data-stu-id="270b3-103">MF\_MT\_VIDEO\_CHROMA\_SITING attribute</span></span>

<span data-ttu-id="270b3-104">Décrit comment la chrominance a été échantillonnée pour un type de média vidéo « Y’Cb’Cr ».</span><span class="sxs-lookup"><span data-stu-id="270b3-104">Describes how chroma was sampled for a Y'Cb'Cr' video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="270b3-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="270b3-105">Data type</span></span>

<span data-ttu-id="270b3-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="270b3-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="270b3-107">Notes</span><span class="sxs-lookup"><span data-stu-id="270b3-107">Remarks</span></span>

<span data-ttu-id="270b3-108">La valeur de cet attribut est **une opération or au niveau du bit** des indicateurs de l’énumération [**MFVideoChromaSubsampling**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideochromasubsampling) .</span><span class="sxs-lookup"><span data-stu-id="270b3-108">The value of this attribute is a bitwise **OR** of flags from the [**MFVideoChromaSubsampling**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideochromasubsampling) enumeration.</span></span>

<span data-ttu-id="270b3-109">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="270b3-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="270b3-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="270b3-110">Requirements</span></span>



| <span data-ttu-id="270b3-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="270b3-111">Requirement</span></span> | <span data-ttu-id="270b3-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="270b3-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="270b3-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="270b3-113">Minimum supported client</span></span><br/> | <span data-ttu-id="270b3-114">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="270b3-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="270b3-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="270b3-115">Minimum supported server</span></span><br/> | <span data-ttu-id="270b3-116">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="270b3-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="270b3-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="270b3-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="270b3-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="270b3-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="270b3-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="270b3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="270b3-120">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="270b3-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="270b3-121">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="270b3-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="270b3-122">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="270b3-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="270b3-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="270b3-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="270b3-124">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="270b3-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="270b3-125">Informations sur les couleurs étendues</span><span class="sxs-lookup"><span data-stu-id="270b3-125">Extended Color Information</span></span>](extended-color-information.md)
</dt> </dl>

 

 




