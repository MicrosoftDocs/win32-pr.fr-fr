---
description: Nombre de bits par échantillon audio dans un type de média audio.
ms.assetid: d78a8c4d-377e-45eb-9cf6-2d61b34e82d6
title: Attribut MF_MT_AUDIO_BITS_PER_SAMPLE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 896e77c937269b63208cb4bff73482a8df8596aa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127231816"
---
# <a name="mf_mt_audio_bits_per_sample-attribute"></a>\_Bits de \_ sortie audio MF \_ \_ par exemple d' \_ attribut

Nombre de bits par échantillon audio dans un type de média audio.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

Cet attribut correspond au membre **wBitsPerSample** de la structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .

Si certains bits contiennent des marges, définissez l’attribut [**\_ bits de sortie audio de l’exemple MF MT \_ Valid- \_ \_ \_ per \_**](mf-mt-audio-valid-bits-per-sample-attribute.md) pour spécifier le nombre de bits de données audio valides dans chaque échantillon.

Si le contenu audio contient 8 bits par échantillon, les exemples audio sont des valeurs non signées. (Chaque échantillon audio est compris entre 0 et 255). Si le contenu audio contient 16 bits par échantillon ou plus, les exemples audio sont des valeurs signées.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications UWP pour applications de bureau Vista \|\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows Applications de bureau du serveur 2008 \[ \| applications UWP\]<br/>                        |
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

 

 
