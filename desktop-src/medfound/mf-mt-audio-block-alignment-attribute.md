---
description: Alignement de bloc, en octets, pour un type de média audio. L’alignement de bloc est l’unité atomique minimale des données pour le format audio.
ms.assetid: 7d304826-ad81-4243-a675-2f55b668b348
title: Attribut MF_MT_AUDIO_BLOCK_ALIGNMENT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21efb14cbb89d1773fe9bc3b5ade8d0a50555a1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536378"
---
# <a name="mf_mt_audio_block_alignment-attribute"></a><span data-ttu-id="2633d-104">\_Attribut d' \_ \_ alignement de bloc audio MF MT \_</span><span class="sxs-lookup"><span data-stu-id="2633d-104">MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT attribute</span></span>

<span data-ttu-id="2633d-105">Alignement de bloc, en octets, pour un type de média audio.</span><span class="sxs-lookup"><span data-stu-id="2633d-105">Block alignment, in bytes, for an audio media type.</span></span> <span data-ttu-id="2633d-106">L’alignement de bloc est l’unité atomique minimale des données pour le format audio.</span><span class="sxs-lookup"><span data-stu-id="2633d-106">The block alignment is the minimum atomic unit of data for the audio format.</span></span>

## <a name="data-type"></a><span data-ttu-id="2633d-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="2633d-107">Data type</span></span>

<span data-ttu-id="2633d-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="2633d-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="2633d-109">Notes</span><span class="sxs-lookup"><span data-stu-id="2633d-109">Remarks</span></span>

<span data-ttu-id="2633d-110">Pour les formats audio PCM, l’alignement de bloc est égal au nombre de canaux audio multiplié par le nombre d’octets par échantillon audio.</span><span class="sxs-lookup"><span data-stu-id="2633d-110">For PCM audio formats, the block alignment is equal to the number of audio channels multiplied by the number of bytes per audio sample.</span></span>

<span data-ttu-id="2633d-111">Cet attribut correspond au membre **nBlockAlign** de la structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2633d-111">This attribute corresponds to the **nBlockAlign** member of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

<span data-ttu-id="2633d-112">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="2633d-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="2633d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2633d-113">Requirements</span></span>



| <span data-ttu-id="2633d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2633d-114">Requirement</span></span> | <span data-ttu-id="2633d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="2633d-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2633d-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2633d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2633d-117">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="2633d-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="2633d-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2633d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2633d-119">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="2633d-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="2633d-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="2633d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2633d-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2633d-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2633d-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2633d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2633d-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2633d-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2633d-124">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="2633d-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="2633d-125">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="2633d-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="2633d-126">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="2633d-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="2633d-127">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="2633d-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
