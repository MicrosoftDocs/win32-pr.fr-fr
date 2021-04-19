---
description: Nombre d’échantillons audio contenus dans un bloc compressé de données audio. Cet attribut peut être utilisé dans des formats audio compressés qui ont un nombre fixe d’échantillons dans chaque bloc.
ms.assetid: 6ae31548-4d78-4e38-9cfc-01b611a6022d
title: Attribut MF_MT_AUDIO_SAMPLES_PER_BLOCK (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7c453fa4daeaa310b5e41add44b63b0fb45372d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518790"
---
# <a name="mf_mt_audio_samples_per_block-attribute"></a><span data-ttu-id="c67ef-104">\_Exemples d' \_ éléments audio MF MT \_ \_ par \_ bloc</span><span class="sxs-lookup"><span data-stu-id="c67ef-104">MF\_MT\_AUDIO\_SAMPLES\_PER\_BLOCK attribute</span></span>

<span data-ttu-id="c67ef-105">Nombre d’échantillons audio contenus dans un bloc compressé de données audio.</span><span class="sxs-lookup"><span data-stu-id="c67ef-105">Number of audio samples contained in one compressed block of audio data.</span></span> <span data-ttu-id="c67ef-106">Cet attribut peut être utilisé dans des formats audio compressés qui ont un nombre fixe d’échantillons dans chaque bloc.</span><span class="sxs-lookup"><span data-stu-id="c67ef-106">This attribute can be used in compressed audio formats that have a fixed number of samples within each block.</span></span>

## <a name="data-type"></a><span data-ttu-id="c67ef-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="c67ef-107">Data type</span></span>

<span data-ttu-id="c67ef-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c67ef-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="c67ef-109">Notes</span><span class="sxs-lookup"><span data-stu-id="c67ef-109">Remarks</span></span>

<span data-ttu-id="c67ef-110">Cet attribut correspond au membre **wSamplesPerBlock** de la structure [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c67ef-110">This attribute corresponds to the **wSamplesPerBlock** member of the [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure.</span></span>

<span data-ttu-id="c67ef-111">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c67ef-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c67ef-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c67ef-112">Requirements</span></span>



| <span data-ttu-id="c67ef-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c67ef-113">Requirement</span></span> | <span data-ttu-id="c67ef-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="c67ef-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c67ef-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c67ef-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c67ef-116">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="c67ef-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="c67ef-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c67ef-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c67ef-118">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="c67ef-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="c67ef-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="c67ef-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c67ef-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c67ef-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c67ef-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c67ef-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c67ef-122">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c67ef-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c67ef-123">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="c67ef-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="c67ef-124">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="c67ef-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="c67ef-125">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="c67ef-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="c67ef-126">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="c67ef-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
