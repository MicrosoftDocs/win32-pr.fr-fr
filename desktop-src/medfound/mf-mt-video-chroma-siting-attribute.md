---
description: Décrit comment chroma a été échantillonné pour un type de média vidéo YCbCr.
ms.assetid: 0c930348-8669-42cc-9d74-df9ef475bdc8
title: Attribut MF_MT_VIDEO_CHROMA_SITING (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5954f6d1649c366056bf9362a4226314d79ad78708fd4140f355506f7ee637d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118741525"
---
# <a name="mf_mt_video_chroma_siting-attribute"></a>MF \_ MT \_ vidéo \_ Chroma emplacement \_ attribut

Décrit comment la chrominance a été échantillonnée pour un type de média vidéo « Y’Cb’Cr ».

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Remarques

La valeur de cet attribut est **une opération or au niveau du bit** des indicateurs de l’énumération [**MFVideoChromaSubsampling**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideochromasubsampling) .

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
</dt> <dt>

[Informations sur les couleurs étendues](extended-color-information.md)
</dt> </dl>

 

 




