---
description: Spécifie la structure de format héritée par défaut à utiliser lors de la conversion d’un type de média audio.
ms.assetid: 9bb045a2-be5b-468b-b30b-aedcb7849945
title: Attribut MF_MT_AUDIO_PREFER_WAVEFORMATEX (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7be5f5ac0aadfb2a4d8d2b8394a06f270e1b4d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528245"
---
# <a name="mf_mt_audio_prefer_waveformatex-attribute"></a>MF \_ MT \_ audio \_ préférer l' \_ attribut WAVEFORMATEX

Spécifie la structure de format héritée par défaut à utiliser lors de la conversion d’un type de média audio.

## <a name="data-type"></a>Type de données

**UINT32**

Traiter en tant que valeur booléenne.

## <a name="remarks"></a>Notes

Cet attribut fournit un indicateur à la fonction [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype) . Si l’attribut a la **valeur true**, la fonction convertit le type de média audio en structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) chaque fois que cela est possible, au lieu de le convertir en une structure [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) .

La fonction [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) définit cet attribut. Vous pouvez remplacer la valeur de cet attribut, mais l’affectation de la valeur **true** à cet attribut ne garantit pas qu’un type de média audio peut être converti au format [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .

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

 

 
