---
description: Dans un type de média audio, spécifie l’affectation de canaux audio aux positions des haut-parleurs.
ms.assetid: fa5f6baa-0a21-4162-8870-38e71763aba0
title: Attribut MF_MT_AUDIO_CHANNEL_MASK (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5293f5387a2c293b97ee32db54fcfb3f3ff304d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034206"
---
# <a name="mf_mt_audio_channel_mask-attribute"></a><span data-ttu-id="5a79b-103">\_Attribut de \_ \_ masque de canal audio MF MT \_</span><span class="sxs-lookup"><span data-stu-id="5a79b-103">MF\_MT\_AUDIO\_CHANNEL\_MASK attribute</span></span>

<span data-ttu-id="5a79b-104">Dans un type de média audio, spécifie l’affectation de canaux audio aux positions des haut-parleurs.</span><span class="sxs-lookup"><span data-stu-id="5a79b-104">In an audio media type, specifies the assignment of audio channels to speaker positions.</span></span>

## <a name="data-type"></a><span data-ttu-id="5a79b-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="5a79b-105">Data type</span></span>

<span data-ttu-id="5a79b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5a79b-106">**UINT32**</span></span>

<span data-ttu-id="5a79b-107">La valeur de cet attribut est **une opération or au niveau du bit** des indicateurs suivants, qui sont définis dans le fichier d’en-tête mmreg. h.</span><span class="sxs-lookup"><span data-stu-id="5a79b-107">The value of this attribute is a bitwise **OR** of the following flags, which are defined in the header file mmreg.h.</span></span>

<dl> <dt>

<span data-ttu-id="5a79b-108"><span id="SPEAKER_FRONT_LEFT"></span><span id="speaker_front_left"></span>**Haut-parleur \_ AVANT \_ gauche** (0x1)</span><span class="sxs-lookup"><span data-stu-id="5a79b-108"><span id="SPEAKER_FRONT_LEFT"></span><span id="speaker_front_left"></span>**SPEAKER\_FRONT\_LEFT** (0x1)</span></span>
</dt> <dt>

<span data-ttu-id="5a79b-109"><span id="SPEAKER_FRONT_RIGHT"></span><span id="speaker_front_right"></span>**Haut-parleur \_ AVANT \_ droit** (0X2)</span><span class="sxs-lookup"><span data-stu-id="5a79b-109"><span id="SPEAKER_FRONT_RIGHT"></span><span id="speaker_front_right"></span>**SPEAKER\_FRONT\_RIGHT** (0x2)</span></span>
</dt> <dt>

<span data-ttu-id="5a79b-110"><span id="SPEAKER_FRONT_CENTER"></span><span id="speaker_front_center"></span>**Haut-parleur \_ \_Centre avant** (0x4)</span><span class="sxs-lookup"><span data-stu-id="5a79b-110"><span id="SPEAKER_FRONT_CENTER"></span><span id="speaker_front_center"></span>**SPEAKER\_FRONT\_CENTER** (0x4)</span></span>
</dt> <dt>

<span data-ttu-id="5a79b-111"><span id="SPEAKER_LOW_FREQUENCY"></span><span id="speaker_low_frequency"></span>**Haut-parleur \_ \_Fréquence faible** (0x8)</span><span class="sxs-lookup"><span data-stu-id="5a79b-111"><span id="SPEAKER_LOW_FREQUENCY"></span><span id="speaker_low_frequency"></span>**SPEAKER\_LOW\_FREQUENCY** (0x8)</span></span>
</dt> <dt>

<span data-ttu-id="5a79b-112"><span id="SPEAKER_BACK_LEFT"></span><span id="speaker_back_left"></span>**Haut-parleur \_ ARRIÈRE \_ gauche** (0x10)</span><span class="sxs-lookup"><span data-stu-id="5a79b-112"><span id="SPEAKER_BACK_LEFT"></span><span id="speaker_back_left"></span>**SPEAKER\_BACK\_LEFT** (0x10)</span></span>
</dt> <dt>

<span data-ttu-id="5a79b-113"><span id="SPEAKER_BACK_RIGHT"></span><span id="speaker_back_right"></span>**Haut-parleur \_ ARRIÈRE \_ droit** (0x20)</span><span class="sxs-lookup"><span data-stu-id="5a79b-113"><span id="SPEAKER_BACK_RIGHT"></span><span id="speaker_back_right"></span>**SPEAKER\_BACK\_RIGHT** (0x20)</span></span>
</dt> <dt>

<span data-ttu-id="5a79b-114"><span id="SPEAKER_FRONT_LEFT_OF_CENTER"></span><span id="speaker_front_left_of_center"></span>**Haut-parleur \_ AVANT \_ gauche \_ du \_ Centre** (0x40)</span><span class="sxs-lookup"><span data-stu-id="5a79b-114"><span id="SPEAKER_FRONT_LEFT_OF_CENTER"></span><span id="speaker_front_left_of_center"></span>**SPEAKER\_FRONT\_LEFT\_OF\_CENTER** (0x40)</span></span>
</dt> <dt>

<span data-ttu-id="5a79b-115"><span id="SPEAKER_FRONT_RIGHT_OF_CENTER"></span><span id="speaker_front_right_of_center"></span>**Haut-parleur \_ AVANT \_ droit \_ du \_ Centre** (0x80)</span><span class="sxs-lookup"><span data-stu-id="5a79b-115"><span id="SPEAKER_FRONT_RIGHT_OF_CENTER"></span><span id="speaker_front_right_of_center"></span>**SPEAKER\_FRONT\_RIGHT\_OF\_CENTER** (0x80)</span></span>
</dt> <dt>

<span data-ttu-id="5a79b-116"><span id="SPEAKER_BACK_CENTER"></span><span id="speaker_back_center"></span>**Haut-parleur \_ \_Centre arrière** (0x100)</span><span class="sxs-lookup"><span data-stu-id="5a79b-116"><span id="SPEAKER_BACK_CENTER"></span><span id="speaker_back_center"></span>**SPEAKER\_BACK\_CENTER** (0x100)</span></span>
</dt> <dt>

<span data-ttu-id="5a79b-117"><span id="SPEAKER_SIDE_LEFT"></span><span id="speaker_side_left"></span>**Haut-parleur \_ CÔTÉ \_ gauche** (0x200)</span><span class="sxs-lookup"><span data-stu-id="5a79b-117"><span id="SPEAKER_SIDE_LEFT"></span><span id="speaker_side_left"></span>**SPEAKER\_SIDE\_LEFT** (0x200)</span></span>
</dt> <dt>

<span data-ttu-id="5a79b-118"><span id="SPEAKER_SIDE_RIGHT"></span><span id="speaker_side_right"></span>**Haut-parleur \_ CÔTÉ \_ droit** (0x400)</span><span class="sxs-lookup"><span data-stu-id="5a79b-118"><span id="SPEAKER_SIDE_RIGHT"></span><span id="speaker_side_right"></span>**SPEAKER\_SIDE\_RIGHT** (0x400)</span></span>
</dt> <dt>

<span data-ttu-id="5a79b-119"><span id="SPEAKER_TOP_CENTER"></span><span id="speaker_top_center"></span>**Haut-parleur \_ \_Centre supérieur** (0x800)</span><span class="sxs-lookup"><span data-stu-id="5a79b-119"><span id="SPEAKER_TOP_CENTER"></span><span id="speaker_top_center"></span>**SPEAKER\_TOP\_CENTER** (0x800)</span></span>
</dt> <dt>

<span data-ttu-id="5a79b-120"><span id="SPEAKER_TOP_FRONT_LEFT"></span><span id="speaker_top_front_left"></span>**Haut-parleur \_ HAUT \_ avant \_ gauche** (0x1000)</span><span class="sxs-lookup"><span data-stu-id="5a79b-120"><span id="SPEAKER_TOP_FRONT_LEFT"></span><span id="speaker_top_front_left"></span>**SPEAKER\_TOP\_FRONT\_LEFT** (0x1000)</span></span>
</dt> <dt>

<span data-ttu-id="5a79b-121"><span id="SPEAKER_TOP_FRONT_CENTER"></span><span id="speaker_top_front_center"></span>**Haut-parleur \_ HAUT \_ avant- \_ Centre** (0x2000)</span><span class="sxs-lookup"><span data-stu-id="5a79b-121"><span id="SPEAKER_TOP_FRONT_CENTER"></span><span id="speaker_top_front_center"></span>**SPEAKER\_TOP\_FRONT\_CENTER** (0x2000)</span></span>
</dt> <dt>

<span data-ttu-id="5a79b-122"><span id="SPEAKER_TOP_FRONT_RIGHT"></span><span id="speaker_top_front_right"></span>**Haut-parleur \_ En haut à \_ \_ droite** (0x4000)</span><span class="sxs-lookup"><span data-stu-id="5a79b-122"><span id="SPEAKER_TOP_FRONT_RIGHT"></span><span id="speaker_top_front_right"></span>**SPEAKER\_TOP\_FRONT\_RIGHT** (0x4000)</span></span>
</dt> <dt>

<span data-ttu-id="5a79b-123"><span id="SPEAKER_TOP_BACK_LEFT"></span><span id="speaker_top_back_left"></span>**Haut-parleur \_ HAUT \_ arrière \_ gauche** (0x8000)</span><span class="sxs-lookup"><span data-stu-id="5a79b-123"><span id="SPEAKER_TOP_BACK_LEFT"></span><span id="speaker_top_back_left"></span>**SPEAKER\_TOP\_BACK\_LEFT** (0x8000)</span></span>
</dt> <dt>

<span data-ttu-id="5a79b-124"><span id="SPEAKER_TOP_BACK_CENTER"></span><span id="speaker_top_back_center"></span>**Haut-parleur \_ \_ \_ Centre** de l’arrière-plan (0x10000)</span><span class="sxs-lookup"><span data-stu-id="5a79b-124"><span id="SPEAKER_TOP_BACK_CENTER"></span><span id="speaker_top_back_center"></span>**SPEAKER\_TOP\_BACK\_CENTER** (0x10000)</span></span>
</dt> <dt>

<span data-ttu-id="5a79b-125"><span id="SPEAKER_TOP_BACK_RIGHT"></span><span id="speaker_top_back_right"></span>**Haut-parleur \_ HAUT \_ arrière \_ droit** (0x20000)</span><span class="sxs-lookup"><span data-stu-id="5a79b-125"><span id="SPEAKER_TOP_BACK_RIGHT"></span><span id="speaker_top_back_right"></span>**SPEAKER\_TOP\_BACK\_RIGHT** (0x20000)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="5a79b-126">Notes</span><span class="sxs-lookup"><span data-stu-id="5a79b-126">Remarks</span></span>

<span data-ttu-id="5a79b-127">Cet attribut correspond au membre **dwChannelMask** de la structure [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible) .</span><span class="sxs-lookup"><span data-stu-id="5a79b-127">This attribute corresponds to the **dwChannelMask** member of the [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible) structure.</span></span>

<span data-ttu-id="5a79b-128">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="5a79b-128">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a79b-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a79b-129">Requirements</span></span>



| <span data-ttu-id="5a79b-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a79b-130">Requirement</span></span> | <span data-ttu-id="5a79b-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a79b-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5a79b-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a79b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5a79b-133">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="5a79b-133">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="5a79b-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a79b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5a79b-135">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="5a79b-135">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="5a79b-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="5a79b-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a79b-137"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a79b-137"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a79b-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a79b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a79b-139">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5a79b-139">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5a79b-140">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="5a79b-140">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="5a79b-141">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="5a79b-141">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="5a79b-142">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="5a79b-142">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="5a79b-143">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="5a79b-143">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
