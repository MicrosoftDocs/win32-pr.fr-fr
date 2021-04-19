---
description: Contient l’en-tête de séquence MPEG-1 ou MPEG-2 pour un type de média vidéo.
ms.assetid: 17b7f76c-404c-4aa9-9746-1488fee027f2
title: Attribut MF_MT_MPEG_SEQUENCE_HEADER (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4003137ec4d2942bc95f56b2ce54644eb7b678d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541876"
---
# <a name="mf_mt_mpeg_sequence_header-attribute"></a><span data-ttu-id="99f9e-103">\_Attribut d' \_ \_ \_ en-tête de séquence MPEG MF MT</span><span class="sxs-lookup"><span data-stu-id="99f9e-103">MF\_MT\_MPEG\_SEQUENCE\_HEADER attribute</span></span>

<span data-ttu-id="99f9e-104">Contient l’en-tête de séquence MPEG-1 ou MPEG-2 pour un type de média vidéo.</span><span class="sxs-lookup"><span data-stu-id="99f9e-104">Contains the MPEG-1 or MPEG-2 sequence header for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="99f9e-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="99f9e-105">Data type</span></span>

<span data-ttu-id="99f9e-106">Tableau d’octets</span><span class="sxs-lookup"><span data-stu-id="99f9e-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="99f9e-107">Notes</span><span class="sxs-lookup"><span data-stu-id="99f9e-107">Remarks</span></span>

<span data-ttu-id="99f9e-108">Cet attribut correspond au membre **dwSequenceHeader** de la structure [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) ou au membre **bSequenceHeader** de la structure [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="99f9e-108">This attribute corresponds to the **dwSequenceHeader** member of the [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure, or the **bSequenceHeader** member of the [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) structure.</span></span>

<span data-ttu-id="99f9e-109">Pour la vidéo H264 – et H265, l’objet BLOB contient des [unités nal](https://en.wikipedia.org/wiki/Network_Abstraction_Layer) concaténées au format annexe B, ainsi que leurs codes de début.</span><span class="sxs-lookup"><span data-stu-id="99f9e-109">For h264 and h265 video, the blob contains concatenated [NAL units](https://en.wikipedia.org/wiki/Network_Abstraction_Layer) in Annex B format, along with their start codes.</span></span> <span data-ttu-id="99f9e-110">Plus précisément, pour la vidéo H264 –, il s’agit de SPS & unités PPS NAL.</span><span class="sxs-lookup"><span data-stu-id="99f9e-110">Specifically, for h264 video they are SPS & PPS NAL units.</span></span> <span data-ttu-id="99f9e-111">Pour H265, il s’agit de VPS, SPS & PPS.</span><span class="sxs-lookup"><span data-stu-id="99f9e-111">For h265 they are VPS, SPS & PPS.</span></span>

<span data-ttu-id="99f9e-112">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="99f9e-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="99f9e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99f9e-113">Requirements</span></span>



| <span data-ttu-id="99f9e-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99f9e-114">Requirement</span></span> | <span data-ttu-id="99f9e-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="99f9e-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="99f9e-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99f9e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="99f9e-117">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="99f9e-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="99f9e-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99f9e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="99f9e-119">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="99f9e-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="99f9e-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="99f9e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="99f9e-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="99f9e-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99f9e-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99f9e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99f9e-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="99f9e-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="99f9e-124">**IMFAttributes :: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="99f9e-124">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="99f9e-125">**IMFAttributes :: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="99f9e-125">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="99f9e-126">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="99f9e-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="99f9e-127">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="99f9e-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
