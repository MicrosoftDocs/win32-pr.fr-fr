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
# <a name="mf_mt_audio_valid_bits_per_sample-attribute"></a>\_Bits de \_ sortie audio MF- \_ octets valides \_ \_ par \_ exemple

Nombre de bits de données audio valides dans chaque exemple audio.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

L' **attribut \_ \_ bits de sortie audio compatible MF MT \_ \_ \_ per \_ Sample** est utilisé pour les formats audio qui contiennent le remplissage après chaque échantillon audio. La taille totale de chaque échantillon audio, y compris les bits de remplissage, est indiquée dans l’attribut [**\_ \_ bits MF audio \_ bits \_ per \_ Sample**](mf-mt-audio-bits-per-sample-attribute.md) .

Si l' **attribut \_ \_ \_ \_ bits \_ par \_ exemple de bits de sortie audio MF MT valid** n’est pas défini, utilisez l’attribut [**bits de \_ \_ sortie audio MF \_ \_ par \_ échantillon**](mf-mt-audio-bits-per-sample-attribute.md) pour rechercher le nombre de bits valides par échantillon.

Si un format audio ne contient pas de bits de remplissage, cet attribut ne doit pas être défini ou doit avoir la même valeur que l’attribut de [**\_ \_ bits audio MF MT \_ \_ per \_ Sample**](mf-mt-audio-bits-per-sample-attribute.md) .

Cet attribut correspond au membre **wValidBitsPerSample** de la structure [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible) .

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows Vista- \[ \| applications UWP\]<br/>                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ \| apps UWP\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributs du type de média](media-type-attributes.md)
</dt> </dl>

 

 
