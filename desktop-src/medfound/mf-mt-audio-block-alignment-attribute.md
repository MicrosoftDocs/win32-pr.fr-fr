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
# <a name="mf_mt_audio_block_alignment-attribute"></a>\_Attribut d' \_ \_ alignement de bloc audio MF MT \_

Alignement de bloc, en octets, pour un type de média audio. L’alignement de bloc est l’unité atomique minimale des données pour le format audio.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

Pour les formats audio PCM, l’alignement de bloc est égal au nombre de canaux audio multiplié par le nombre d’octets par échantillon audio.

Cet attribut correspond au membre **nBlockAlign** de la structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .

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

 

 
