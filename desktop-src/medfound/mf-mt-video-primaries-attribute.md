---
description: Spécifie les couleurs primaires d’un type de média vidéo.
ms.assetid: 56f31c1a-b610-4da0-9df4-76e15add672c
title: Attribut MF_MT_VIDEO_PRIMARIES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6cdf26a3f49c7e2bb3aa0f48c52c9b283edd8cc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127531200"
---
# <a name="mf_mt_video_primaries-attribute"></a>\_Attribut des \_ primaires de vidéos MF MT \_

Spécifie les couleurs primaires d’un type de média vidéo.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

La valeur de cet attribut est un membre de l’énumération [**MFVideoPrimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) .

L’énumération [**MFVideoPrimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) identifie les couleurs primaires associées à certaines normes vidéo courantes. Si le type de média utilise des couleurs primaires qui ne sont pas identifiées dans l’énumération **MFVideoPrimaries** , définissez l’attribut de préversions de [**\_ \_ \_ vidéo personnalisée \_ MF MT personnalisé**](mf-mt-custom-video-primaries-attribute.md) au lieu de cet attribut.

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
</dt> <dt>

[Informations sur les couleurs étendues](extended-color-information.md)
</dt> </dl>

 

 




