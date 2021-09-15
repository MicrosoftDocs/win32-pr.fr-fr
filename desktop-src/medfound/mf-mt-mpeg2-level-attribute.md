---
description: Spécifie le niveau MPEG-2 ou H. 264 dans un type de média vidéo.
ms.assetid: 8dd8e8c4-5a6f-4a87-a643-73af35c362a9
title: Attribut MF_MT_MPEG2_LEVEL (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 111c4b30befb1d4b25a688d25f46f02bcef21541
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525769"
---
# <a name="mf_mt_mpeg2_level-attribute"></a>\_Attribut de \_ niveau de MPEG2 MT MF \_

Spécifie le niveau MPEG-2 ou H. 264 dans un type de média vidéo.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

Pour la vidéo MPEG-2, la valeur de cet attribut est un membre de l’énumération [**am \_ MPEG2Level**](/previous-versions/windows/desktop/api/dvdmedia/ne-dvdmedia-am_mpeg2level) .

Pour la vidéo H. 264, la valeur est un membre de l’énumération [**eAVEncH264VLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel) .

Cet attribut correspond au membre **dwLevel** de la structure [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) .

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

 

 
