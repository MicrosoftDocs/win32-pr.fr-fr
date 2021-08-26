---
description: Spécifie le niveau MPEG-2 ou H. 264 dans un type de média vidéo.
ms.assetid: 8dd8e8c4-5a6f-4a87-a643-73af35c362a9
title: Attribut MF_MT_MPEG2_LEVEL (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1ac99f76d458c1c5964e61181f58f53e7bfce19ab04b09615eaf932dfa2939
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060605"
---
# <a name="mf_mt_mpeg2_level-attribute"></a>\_Attribut de \_ niveau de MPEG2 MT MF \_

Spécifie le niveau MPEG-2 ou H. 264 dans un type de média vidéo.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Remarques

Pour la vidéo MPEG-2, la valeur de cet attribut est un membre de l’énumération [**am \_ MPEG2Level**](/previous-versions/windows/desktop/api/dvdmedia/ne-dvdmedia-am_mpeg2level) .

Pour la vidéo H. 264, la valeur est un membre de l’énumération [**eAVEncH264VLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel) .

Cet attribut correspond au membre **dwLevel** de la structure [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) .

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

 

 
