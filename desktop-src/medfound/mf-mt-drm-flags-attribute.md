---
description: Spécifie si un type de média vidéo requiert l’application de la protection de copie.
ms.assetid: fb12ba38-a4f4-44fe-bf31-e731c56bb145
title: Attribut MF_MT_DRM_FLAGS (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa8ef771cb72050b2273d822ce799092ce51e64c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520042"
---
# <a name="mf_mt_drm_flags-attribute"></a><span data-ttu-id="588b6-103">\_ \_ Attribut indicateurs DRM pour MF MT \_</span><span class="sxs-lookup"><span data-stu-id="588b6-103">MF\_MT\_DRM\_FLAGS attribute</span></span>

<span data-ttu-id="588b6-104">Spécifie si un type de média vidéo requiert l’application de la protection de copie.</span><span class="sxs-lookup"><span data-stu-id="588b6-104">Specifies whether a video media type requires the enforcement of copy protection.</span></span>

## <a name="data-type"></a><span data-ttu-id="588b6-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="588b6-105">Data type</span></span>

<span data-ttu-id="588b6-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="588b6-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="588b6-107">Notes</span><span class="sxs-lookup"><span data-stu-id="588b6-107">Remarks</span></span>

<span data-ttu-id="588b6-108">La valeur de cet attribut est un membre de l’énumération [**MFVideoDRMFlags**](/windows/desktop/api/mfapi/ne-mfapi-mfvideodrmflags) .</span><span class="sxs-lookup"><span data-stu-id="588b6-108">The value of this attribute is a member of the [**MFVideoDRMFlags**](/windows/desktop/api/mfapi/ne-mfapi-mfvideodrmflags) enumeration.</span></span>

<span data-ttu-id="588b6-109">Cet attribut fournit une indication à l’application.</span><span class="sxs-lookup"><span data-stu-id="588b6-109">This attribute provides a hint to the application.</span></span> <span data-ttu-id="588b6-110">Elle n’est pas utilisée pour appliquer la protection contre la copie ou pour spécifier le mécanisme de protection contre la copie.</span><span class="sxs-lookup"><span data-stu-id="588b6-110">It is not used to enforce copy protection or to specify the copy protection mechanism.</span></span>

<span data-ttu-id="588b6-111">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="588b6-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="588b6-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="588b6-112">Requirements</span></span>



| <span data-ttu-id="588b6-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="588b6-113">Requirement</span></span> | <span data-ttu-id="588b6-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="588b6-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="588b6-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="588b6-115">Minimum supported client</span></span><br/> | <span data-ttu-id="588b6-116">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="588b6-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="588b6-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="588b6-117">Minimum supported server</span></span><br/> | <span data-ttu-id="588b6-118">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="588b6-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="588b6-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="588b6-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="588b6-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="588b6-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="588b6-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="588b6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="588b6-122">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="588b6-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="588b6-123">\_protégé SD \_ sécurisé</span><span class="sxs-lookup"><span data-stu-id="588b6-123">MF\_SD\_PROTECTED</span></span>](mf-sd-protected-attribute.md)
</dt> <dt>

[<span data-ttu-id="588b6-124">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="588b6-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="588b6-125">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="588b6-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="588b6-126">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="588b6-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="588b6-127">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="588b6-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




