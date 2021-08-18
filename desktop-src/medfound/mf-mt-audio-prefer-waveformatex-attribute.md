---
description: Spécifie la structure de format héritée par défaut à utiliser lors de la conversion d’un type de média audio.
ms.assetid: 9bb045a2-be5b-468b-b30b-aedcb7849945
title: Attribut MF_MT_AUDIO_PREFER_WAVEFORMATEX (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b23e2aeb00e2967b3f031a2aafe3a01f3846d7db077ba344a59680508bd385fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035297"
---
# <a name="mf_mt_audio_prefer_waveformatex-attribute"></a>MF \_ MT \_ audio \_ préférer l' \_ attribut WAVEFORMATEX

Spécifie la structure de format héritée par défaut à utiliser lors de la conversion d’un type de média audio.

## <a name="data-type"></a>Type de données

**UINT32**

Traiter en tant que valeur booléenne.

## <a name="remarks"></a>Remarques

Cet attribut fournit un indicateur à la fonction [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype) . Si l’attribut a la **valeur true**, la fonction convertit le type de média audio en structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) chaque fois que cela est possible, au lieu de le convertir en une structure [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) .

La fonction [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) définit cet attribut. Vous pouvez remplacer la valeur de cet attribut, mais l’affectation de la valeur **true** à cet attribut ne garantit pas qu’un type de média audio peut être converti au format [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



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

 

 
