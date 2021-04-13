---
description: Nombre de bits de données audio valides dans chaque exemple audio.
ms.assetid: b5b97700-c98a-4394-a184-661852add0b4
title: Attribut MF_MT_AUDIO_VALID_BITS_PER_SAMPLE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4e5efb41bf3b79d4feded2872b601eea43723a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320945"
---
# <a name="mf_mt_audio_valid_bits_per_sample-attribute"></a><span data-ttu-id="3cb5d-103">\_Bits de \_ sortie audio MF- \_ octets valides \_ \_ par \_ exemple</span><span class="sxs-lookup"><span data-stu-id="3cb5d-103">MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE attribute</span></span>

<span data-ttu-id="3cb5d-104">Nombre de bits de données audio valides dans chaque exemple audio.</span><span class="sxs-lookup"><span data-stu-id="3cb5d-104">Number of valid bits of audio data in each audio sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="3cb5d-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="3cb5d-105">Data type</span></span>

<span data-ttu-id="3cb5d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="3cb5d-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="3cb5d-107">Notes</span><span class="sxs-lookup"><span data-stu-id="3cb5d-107">Remarks</span></span>

<span data-ttu-id="3cb5d-108">L' **attribut \_ \_ bits de sortie audio compatible MF MT \_ \_ \_ per \_ Sample** est utilisé pour les formats audio qui contiennent le remplissage après chaque échantillon audio.</span><span class="sxs-lookup"><span data-stu-id="3cb5d-108">The **MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE** attribute is used for audio formats that contain padding after each audio sample.</span></span> <span data-ttu-id="3cb5d-109">La taille totale de chaque échantillon audio, y compris les bits de remplissage, est indiquée dans l’attribut [**\_ \_ bits MF audio \_ bits \_ per \_ Sample**](mf-mt-audio-bits-per-sample-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="3cb5d-109">The total size of each audio sample, including padding bits, is given in the [**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**](mf-mt-audio-bits-per-sample-attribute.md) attribute.</span></span>

<span data-ttu-id="3cb5d-110">Si l' **attribut \_ \_ \_ \_ bits \_ par \_ exemple de bits de sortie audio MF MT valid** n’est pas défini, utilisez l’attribut [**bits de \_ \_ sortie audio MF \_ \_ par \_ échantillon**](mf-mt-audio-bits-per-sample-attribute.md) pour rechercher le nombre de bits valides par échantillon.</span><span class="sxs-lookup"><span data-stu-id="3cb5d-110">If the **MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE** attribute is not set, use the [**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**](mf-mt-audio-bits-per-sample-attribute.md) attribute to find the number of valid bits per sample.</span></span>

<span data-ttu-id="3cb5d-111">Si un format audio ne contient pas de bits de remplissage, cet attribut ne doit pas être défini ou doit avoir la même valeur que l’attribut de [**\_ \_ bits audio MF MT \_ \_ per \_ Sample**](mf-mt-audio-bits-per-sample-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="3cb5d-111">If an audio format does not contain any padding bits, then this attribute should not be set, or should be set to the same value as the [**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**](mf-mt-audio-bits-per-sample-attribute.md) attribute.</span></span>

<span data-ttu-id="3cb5d-112">Cet attribut correspond au membre **wValidBitsPerSample** de la structure [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible) .</span><span class="sxs-lookup"><span data-stu-id="3cb5d-112">This attribute corresponds to the **wValidBitsPerSample** member of the [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible) structure.</span></span>

<span data-ttu-id="3cb5d-113">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="3cb5d-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cb5d-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3cb5d-114">Requirements</span></span>



| <span data-ttu-id="3cb5d-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3cb5d-115">Requirement</span></span> | <span data-ttu-id="3cb5d-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="3cb5d-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3cb5d-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3cb5d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3cb5d-118">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="3cb5d-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="3cb5d-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3cb5d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3cb5d-120">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="3cb5d-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="3cb5d-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="3cb5d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3cb5d-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3cb5d-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cb5d-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3cb5d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cb5d-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3cb5d-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3cb5d-125">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="3cb5d-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="3cb5d-126">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="3cb5d-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="3cb5d-127">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="3cb5d-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="3cb5d-128">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="3cb5d-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
