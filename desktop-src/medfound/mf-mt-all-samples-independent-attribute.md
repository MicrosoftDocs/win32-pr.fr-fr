---
description: Spécifie pour un type de média si chaque échantillon est indépendant des autres exemples dans le flux.
ms.assetid: 40434f63-e191-45e1-b788-5f80fe7f49ae
title: Attribut MF_MT_ALL_SAMPLES_INDEPENDENT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f82173e99a30e033b3d90f6cfec0dc2aa8b3af97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524114"
---
# <a name="mf_mt_all_samples_independent-attribute"></a><span data-ttu-id="f0703-103">Attribut indépendant de l’exemple MF \_ MT \_ All \_ \_</span><span class="sxs-lookup"><span data-stu-id="f0703-103">MF\_MT\_ALL\_SAMPLES\_INDEPENDENT attribute</span></span>

<span data-ttu-id="f0703-104">Spécifie pour un type de média si chaque échantillon est indépendant des autres exemples dans le flux.</span><span class="sxs-lookup"><span data-stu-id="f0703-104">Specifies for a media type whether each sample is independent of the other samples in the stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="f0703-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="f0703-105">Data type</span></span>

<span data-ttu-id="f0703-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f0703-106">**UINT32**</span></span>

<span data-ttu-id="f0703-107">Traiter en tant que valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="f0703-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0703-108">Notes</span><span class="sxs-lookup"><span data-stu-id="f0703-108">Remarks</span></span>

<span data-ttu-id="f0703-109">Si cet attribut a la **valeur false**, certains exemples ne peuvent pas être utilisés sans faire référence à d’autres exemples dans le flux.</span><span class="sxs-lookup"><span data-stu-id="f0703-109">If this attribute is **FALSE**, some samples cannot be used without referring to other samples in the stream.</span></span> <span data-ttu-id="f0703-110">Par exemple, si un format vidéo contient des images Delta, cet attribut doit avoir la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="f0703-110">For example, if a video format contains delta frames, this attribute should be **FALSE**.</span></span>

<span data-ttu-id="f0703-111">Cet attribut correspond au champ **bTemporalCompression** dans la structure de [**\_ \_ type de média du matin**](/windows/win32/api/strmif/ns-strmif-am_media_type) DirectShow.</span><span class="sxs-lookup"><span data-stu-id="f0703-111">This attribute corresponds to the **bTemporalCompression** field in the DirectShow [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

<span data-ttu-id="f0703-112">Affectez la valeur **true** à cet attribut pour tous les types de média non compressés.</span><span class="sxs-lookup"><span data-stu-id="f0703-112">Set this attribute to **TRUE** for all uncompressed media types.</span></span>

<span data-ttu-id="f0703-113">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="f0703-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0703-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0703-114">Requirements</span></span>



| <span data-ttu-id="f0703-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f0703-115">Requirement</span></span> | <span data-ttu-id="f0703-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="f0703-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f0703-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0703-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f0703-118">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="f0703-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="f0703-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0703-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f0703-120">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="f0703-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="f0703-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="f0703-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0703-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0703-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0703-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0703-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0703-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f0703-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f0703-125">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="f0703-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="f0703-126">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="f0703-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="f0703-127">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="f0703-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="f0703-128">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="f0703-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
