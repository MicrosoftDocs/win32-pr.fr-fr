---
description: Spécifie le profil MPEG-2 ou H. 264 dans un type de média vidéo.
ms.assetid: 8c6a68cb-d976-4099-8934-064f0e8f6374
title: Attribut MF_MT_MPEG2_PROFILE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee5c64ea9f5bdf73a78d6ae29124c7cd5b37df43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866570"
---
# <a name="mf_mt_mpeg2_profile-attribute"></a><span data-ttu-id="1c1f4-103">\_Attribut de \_ Profil MPEG2 MT \_ MF</span><span class="sxs-lookup"><span data-stu-id="1c1f4-103">MF\_MT\_MPEG2\_PROFILE attribute</span></span>

<span data-ttu-id="1c1f4-104">Spécifie le profil MPEG-2 ou H. 264 dans un type de média vidéo.</span><span class="sxs-lookup"><span data-stu-id="1c1f4-104">Specifies the MPEG-2 or H.264 profile in a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="1c1f4-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="1c1f4-105">Data type</span></span>

<span data-ttu-id="1c1f4-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1c1f4-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="1c1f4-107">Notes</span><span class="sxs-lookup"><span data-stu-id="1c1f4-107">Remarks</span></span>

<span data-ttu-id="1c1f4-108">Pour la vidéo MPEG-2, la valeur de cet attribut est un membre de l’énumération [**am \_ MPEG2Profile**](/previous-versions/windows/desktop/api/dvdmedia/ne-dvdmedia-am_mpeg2profile) .</span><span class="sxs-lookup"><span data-stu-id="1c1f4-108">For MPEG-2 video, the value of this attribute is a member of the [**AM\_MPEG2Profile**](/previous-versions/windows/desktop/api/dvdmedia/ne-dvdmedia-am_mpeg2profile) enumeration.</span></span>

<span data-ttu-id="1c1f4-109">Pour la vidéo H. 264, la valeur est un membre de l’énumération [**eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) .</span><span class="sxs-lookup"><span data-stu-id="1c1f4-109">For H.264 video, the value is a member of the [**eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) enumeration.</span></span>

<span data-ttu-id="1c1f4-110">Cet attribut correspond au membre **dwProfile** de la structure [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="1c1f4-110">This attribute corresponds to the **dwProfile** member of the [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure.</span></span>

<span data-ttu-id="1c1f4-111">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="1c1f4-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c1f4-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1c1f4-112">Requirements</span></span>



| <span data-ttu-id="1c1f4-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1c1f4-113">Requirement</span></span> | <span data-ttu-id="1c1f4-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c1f4-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1c1f4-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c1f4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1c1f4-116">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="1c1f4-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="1c1f4-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c1f4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1c1f4-118">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="1c1f4-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="1c1f4-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="1c1f4-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c1f4-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c1f4-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c1f4-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c1f4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c1f4-122">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1c1f4-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1c1f4-123">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="1c1f4-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="1c1f4-124">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="1c1f4-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="1c1f4-125">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="1c1f4-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="1c1f4-126">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="1c1f4-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
