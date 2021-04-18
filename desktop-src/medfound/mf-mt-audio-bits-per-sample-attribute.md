---
description: Nombre de bits par échantillon audio dans un type de média audio.
ms.assetid: d78a8c4d-377e-45eb-9cf6-2d61b34e82d6
title: Attribut MF_MT_AUDIO_BITS_PER_SAMPLE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 896e77c937269b63208cb4bff73482a8df8596aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520460"
---
# <a name="mf_mt_audio_bits_per_sample-attribute"></a><span data-ttu-id="477cf-103">\_Bits de \_ sortie audio MF \_ \_ par exemple d' \_ attribut</span><span class="sxs-lookup"><span data-stu-id="477cf-103">MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE attribute</span></span>

<span data-ttu-id="477cf-104">Nombre de bits par échantillon audio dans un type de média audio.</span><span class="sxs-lookup"><span data-stu-id="477cf-104">Number of bits per audio sample in an audio media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="477cf-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="477cf-105">Data type</span></span>

<span data-ttu-id="477cf-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="477cf-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="477cf-107">Notes</span><span class="sxs-lookup"><span data-stu-id="477cf-107">Remarks</span></span>

<span data-ttu-id="477cf-108">Cet attribut correspond au membre **wBitsPerSample** de la structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="477cf-108">This attribute corresponds to the **wBitsPerSample** member of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

<span data-ttu-id="477cf-109">Si certains bits contiennent des marges, définissez l’attribut [**\_ bits de sortie audio de l’exemple MF MT \_ Valid- \_ \_ \_ per \_**](mf-mt-audio-valid-bits-per-sample-attribute.md) pour spécifier le nombre de bits de données audio valides dans chaque échantillon.</span><span class="sxs-lookup"><span data-stu-id="477cf-109">If some bits contain padding, set the [**MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE**](mf-mt-audio-valid-bits-per-sample-attribute.md) attribute to specify the number of bits of valid audio data in each sample.</span></span>

<span data-ttu-id="477cf-110">Si le contenu audio contient 8 bits par échantillon, les exemples audio sont des valeurs non signées.</span><span class="sxs-lookup"><span data-stu-id="477cf-110">If the audio contains 8 bits per sample, the audio samples are unsigned values.</span></span> <span data-ttu-id="477cf-111">(Chaque échantillon audio est compris entre 0 et 255). Si le contenu audio contient 16 bits par échantillon ou plus, les exemples audio sont des valeurs signées.</span><span class="sxs-lookup"><span data-stu-id="477cf-111">(Each audio sample has the range 0–255.) If the audio contains 16 bits per sample or higher, the audio samples are signed values.</span></span>

<span data-ttu-id="477cf-112">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="477cf-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="477cf-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="477cf-113">Requirements</span></span>



| <span data-ttu-id="477cf-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="477cf-114">Requirement</span></span> | <span data-ttu-id="477cf-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="477cf-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="477cf-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="477cf-116">Minimum supported client</span></span><br/> | <span data-ttu-id="477cf-117">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="477cf-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="477cf-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="477cf-118">Minimum supported server</span></span><br/> | <span data-ttu-id="477cf-119">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="477cf-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="477cf-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="477cf-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="477cf-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="477cf-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="477cf-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="477cf-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="477cf-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="477cf-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="477cf-124">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="477cf-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="477cf-125">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="477cf-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="477cf-126">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="477cf-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="477cf-127">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="477cf-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
