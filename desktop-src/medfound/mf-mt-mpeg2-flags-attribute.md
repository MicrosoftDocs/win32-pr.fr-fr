---
description: Contient divers indicateurs pour un type de média vidéo MPEG-2.
ms.assetid: 2e1bf3e3-c005-418b-b9fd-1d43c42dad6f
title: Attribut MF_MT_MPEG2_FLAGS (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2ef0a0def9c3e5413ec9b9bf7568fcbe9add851
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520753"
---
# <a name="mf_mt_mpeg2_flags-attribute"></a><span data-ttu-id="5f4ce-103">\_Attribut d' \_ indicateurs MPEG2 MT \_ -MF</span><span class="sxs-lookup"><span data-stu-id="5f4ce-103">MF\_MT\_MPEG2\_FLAGS attribute</span></span>

<span data-ttu-id="5f4ce-104">Contient divers indicateurs pour un type de média vidéo MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="5f4ce-104">Contains miscellaneous flags for an MPEG-2 video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="5f4ce-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="5f4ce-105">Data type</span></span>

<span data-ttu-id="5f4ce-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5f4ce-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="5f4ce-107">Notes</span><span class="sxs-lookup"><span data-stu-id="5f4ce-107">Remarks</span></span>

<span data-ttu-id="5f4ce-108">Cet attribut correspond au membre **dwFlags** de la structure [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="5f4ce-108">This attribute corresponds to the **dwFlags** member of the [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure.</span></span> <span data-ttu-id="5f4ce-109">Pour obtenir la liste des indicateurs valides, consultez la documentation de **MPEG2VIDEOINFO**.</span><span class="sxs-lookup"><span data-stu-id="5f4ce-109">For a list of valid flags, see the documentation for **MPEG2VIDEOINFO**.</span></span>

<span data-ttu-id="5f4ce-110">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="5f4ce-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f4ce-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f4ce-111">Requirements</span></span>



| <span data-ttu-id="5f4ce-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f4ce-112">Requirement</span></span> | <span data-ttu-id="5f4ce-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f4ce-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5f4ce-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f4ce-114">Minimum supported client</span></span><br/> | <span data-ttu-id="5f4ce-115">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="5f4ce-115">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="5f4ce-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f4ce-116">Minimum supported server</span></span><br/> | <span data-ttu-id="5f4ce-117">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="5f4ce-117">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="5f4ce-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="5f4ce-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f4ce-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f4ce-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f4ce-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f4ce-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f4ce-121">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5f4ce-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5f4ce-122">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="5f4ce-122">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="5f4ce-123">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="5f4ce-123">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="5f4ce-124">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="5f4ce-124">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="5f4ce-125">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="5f4ce-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
