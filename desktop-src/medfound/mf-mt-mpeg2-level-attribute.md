---
description: Spécifie le niveau MPEG-2 ou H. 264 dans un type de média vidéo.
ms.assetid: 8dd8e8c4-5a6f-4a87-a643-73af35c362a9
title: Attribut MF_MT_MPEG2_LEVEL (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 111c4b30befb1d4b25a688d25f46f02bcef21541
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203722"
---
# <a name="mf_mt_mpeg2_level-attribute"></a><span data-ttu-id="39b1b-103">\_Attribut de \_ niveau de MPEG2 MT MF \_</span><span class="sxs-lookup"><span data-stu-id="39b1b-103">MF\_MT\_MPEG2\_LEVEL attribute</span></span>

<span data-ttu-id="39b1b-104">Spécifie le niveau MPEG-2 ou H. 264 dans un type de média vidéo.</span><span class="sxs-lookup"><span data-stu-id="39b1b-104">Specifies the MPEG-2 or H.264 level in a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="39b1b-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="39b1b-105">Data type</span></span>

<span data-ttu-id="39b1b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="39b1b-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="39b1b-107">Notes</span><span class="sxs-lookup"><span data-stu-id="39b1b-107">Remarks</span></span>

<span data-ttu-id="39b1b-108">Pour la vidéo MPEG-2, la valeur de cet attribut est un membre de l’énumération [**am \_ MPEG2Level**](/previous-versions/windows/desktop/api/dvdmedia/ne-dvdmedia-am_mpeg2level) .</span><span class="sxs-lookup"><span data-stu-id="39b1b-108">For MPEG-2 video, the value of this attribute is a member of the [**AM\_MPEG2Level**](/previous-versions/windows/desktop/api/dvdmedia/ne-dvdmedia-am_mpeg2level) enumeration.</span></span>

<span data-ttu-id="39b1b-109">Pour la vidéo H. 264, la valeur est un membre de l’énumération [**eAVEncH264VLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel) .</span><span class="sxs-lookup"><span data-stu-id="39b1b-109">For H.264 video, the value is a member of the [**eAVEncH264VLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel) enumeration.</span></span>

<span data-ttu-id="39b1b-110">Cet attribut correspond au membre **dwLevel** de la structure [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="39b1b-110">This attribute corresponds to the **dwLevel** member of the [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure.</span></span>

<span data-ttu-id="39b1b-111">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="39b1b-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="39b1b-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39b1b-112">Requirements</span></span>



| <span data-ttu-id="39b1b-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39b1b-113">Requirement</span></span> | <span data-ttu-id="39b1b-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="39b1b-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="39b1b-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39b1b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="39b1b-116">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="39b1b-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="39b1b-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39b1b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="39b1b-118">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="39b1b-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="39b1b-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="39b1b-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="39b1b-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="39b1b-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39b1b-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39b1b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39b1b-122">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="39b1b-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="39b1b-123">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="39b1b-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="39b1b-124">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="39b1b-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="39b1b-125">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="39b1b-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="39b1b-126">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="39b1b-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
