---
description: Nombre moyen d’octets par seconde dans un type de média audio.
ms.assetid: 0ee371fb-d980-44de-a9bd-201e2b72e874
title: Attribut MF_MT_AUDIO_AVG_BYTES_PER_SECOND (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eca86276e816ea1ef058946bad29f1565fe1c841
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203471"
---
# <a name="mf_mt_audio_avg_bytes_per_second-attribute"></a>\_ \_ \_ Attribut nombre moyen d' \_ octets \_ par \_ seconde de sortie audio MF MT

Nombre moyen d’octets par seconde dans un type de média audio.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

Cet attribut correspond au membre **nAvgBytesPerSec** de la structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .

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

 

 
