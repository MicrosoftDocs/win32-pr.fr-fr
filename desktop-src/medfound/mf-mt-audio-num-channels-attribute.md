---
description: Nombre de canaux audio dans un type de média audio.
ms.assetid: 524283fb-d046-4f8c-a30f-4fe7ddb43174
title: Attribut MF_MT_AUDIO_NUM_CHANNELS (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ede561fbfe178d4086d1d7f7232d831d5133d6b368c1205fa2e8c1280fbeba29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955909"
---
# <a name="mf_mt_audio_num_channels-attribute"></a>\_Attribut des \_ canaux de nombre de \_ \_ canaux audio MF

Nombre de canaux audio dans un type de média audio.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Remarques

Cet attribut correspond au membre **nChannels** de la structure [WAVEFORMATEX](mf-mt-audio-prefer-waveformatex-attribute.md) .

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

 

 




