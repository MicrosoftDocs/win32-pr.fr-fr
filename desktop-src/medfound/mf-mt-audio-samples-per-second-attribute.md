---
description: Nombre d’échantillons audio par seconde dans un type de média audio.
ms.assetid: f640016d-595e-4b20-8ce8-23a029c2b064
title: Attribut MF_MT_AUDIO_SAMPLES_PER_SECOND (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5080f6df87bafe8d4ee86e7b25332a12214ff3cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863586"
---
# <a name="mf_mt_audio_samples_per_second-attribute"></a><span data-ttu-id="963f2-103">\_Attribut d' \_ échantillons audio MF MT \_ \_ par \_ seconde</span><span class="sxs-lookup"><span data-stu-id="963f2-103">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND attribute</span></span>

<span data-ttu-id="963f2-104">Nombre d’échantillons audio par seconde dans un type de média audio.</span><span class="sxs-lookup"><span data-stu-id="963f2-104">Number of audio samples per second in an audio media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="963f2-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="963f2-105">Data type</span></span>

<span data-ttu-id="963f2-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="963f2-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="963f2-107">Notes</span><span class="sxs-lookup"><span data-stu-id="963f2-107">Remarks</span></span>

<span data-ttu-id="963f2-108">Cet attribut correspond au membre **nSamplesPerSec** de la structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="963f2-108">This attribute corresponds to the **nSamplesPerSec** member of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

<span data-ttu-id="963f2-109">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="963f2-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="963f2-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="963f2-110">Requirements</span></span>



| <span data-ttu-id="963f2-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="963f2-111">Requirement</span></span> | <span data-ttu-id="963f2-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="963f2-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="963f2-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="963f2-113">Minimum supported client</span></span><br/> | <span data-ttu-id="963f2-114">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="963f2-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="963f2-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="963f2-115">Minimum supported server</span></span><br/> | <span data-ttu-id="963f2-116">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="963f2-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="963f2-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="963f2-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="963f2-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="963f2-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="963f2-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="963f2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="963f2-120">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="963f2-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="963f2-121">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="963f2-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="963f2-122">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="963f2-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="963f2-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="963f2-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="963f2-124">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="963f2-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="963f2-125">**\_échantillons MF \_ audio flottant MF MT \_ \_ \_ par \_ seconde**</span><span class="sxs-lookup"><span data-stu-id="963f2-125">**MF\_MT\_AUDIO\_FLOAT\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-float-samples-per-second-attribute.md)
</dt> </dl>

 

 
