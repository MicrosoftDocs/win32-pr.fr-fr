---
description: Débit de données approximatif du flux vidéo, en bits par seconde, pour un type de média vidéo.
ms.assetid: cf9374a7-3688-4a6c-8339-d68c267c9bed
title: Attribut MF_MT_AVG_BITRATE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e4497c58abf8587e72dea47d4f8ac222a1b0692
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393748"
---
# <a name="mf_mt_avg_bitrate-attribute"></a>\_Attribut de \_ vitesse de \_ transmission moy. MF

Débit de données approximatif du flux vidéo, en bits par seconde, pour un type de média vidéo.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

Cet attribut correspond au membre **dwBitRate** des structures [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) et [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .

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

 

 
