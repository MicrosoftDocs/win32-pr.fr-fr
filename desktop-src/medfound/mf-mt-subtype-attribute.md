---
description: GUID de sous-type pour un type de média.
ms.assetid: 8e600943-92f1-4936-8c00-842fc7f4cb57
title: Attribut MF_MT_SUBTYPE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34f156e356a0e80d6b2c4bff1ae6f266e4d64b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034589"
---
# <a name="mf_mt_subtype-attribute"></a><span data-ttu-id="dcfc7-103">\_Attribut de \_ sous-type MF MT</span><span class="sxs-lookup"><span data-stu-id="dcfc7-103">MF\_MT\_SUBTYPE attribute</span></span>

<span data-ttu-id="dcfc7-104">GUID de sous-type pour un type de média.</span><span class="sxs-lookup"><span data-stu-id="dcfc7-104">Subtype GUID for a media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="dcfc7-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="dcfc7-105">Data type</span></span>

<span data-ttu-id="dcfc7-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="dcfc7-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="dcfc7-107">Notes</span><span class="sxs-lookup"><span data-stu-id="dcfc7-107">Remarks</span></span>

<span data-ttu-id="dcfc7-108">Le GUID de sous-type définit un type de format de média spécifique dans un type principal.</span><span class="sxs-lookup"><span data-stu-id="dcfc7-108">The subtype GUID defines a specific media format type within a major type.</span></span> <span data-ttu-id="dcfc7-109">Par exemple, dans la vidéo, les sous-types sont RVB-24, RVB-32, UYVY, AYUV, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="dcfc7-109">For example, within video, the subtypes include RGB-24, RGB-32, UYVY, AYUV, and so forth.</span></span> <span data-ttu-id="dcfc7-110">Dans l’audio, les sous-types incluent l’audio PCM, le Windows Media Audio 9, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="dcfc7-110">Within audio, the subtypes include PCM audio, Windows Media Audio 9, and so forth.</span></span>

<span data-ttu-id="dcfc7-111">Pour connaître les valeurs possibles, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="dcfc7-111">For possible values, see the following topics:</span></span>

-   [<span data-ttu-id="dcfc7-112">GUID de sous-type audio</span><span class="sxs-lookup"><span data-stu-id="dcfc7-112">Audio Subtype GUIDs</span></span>](audio-subtype-guids.md)
-   [<span data-ttu-id="dcfc7-113">GUID de sous-type de vidéo</span><span class="sxs-lookup"><span data-stu-id="dcfc7-113">Video Subtype GUIDs</span></span>](video-subtype-guids.md)

<span data-ttu-id="dcfc7-114">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="dcfc7-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcfc7-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dcfc7-115">Requirements</span></span>



| <span data-ttu-id="dcfc7-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dcfc7-116">Requirement</span></span> | <span data-ttu-id="dcfc7-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="dcfc7-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dcfc7-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dcfc7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="dcfc7-119">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="dcfc7-119">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="dcfc7-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dcfc7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="dcfc7-121">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="dcfc7-121">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="dcfc7-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="dcfc7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcfc7-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcfc7-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcfc7-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dcfc7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcfc7-125">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dcfc7-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="dcfc7-126">**IMFAttributes :: GetGUID**</span><span class="sxs-lookup"><span data-stu-id="dcfc7-126">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="dcfc7-127">**IMFAttributes :: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="dcfc7-127">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="dcfc7-128">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="dcfc7-128">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="dcfc7-129">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="dcfc7-129">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




