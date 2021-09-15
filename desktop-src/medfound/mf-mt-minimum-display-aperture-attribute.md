---
description: Définit l’ouverture d’affichage, qui est la région d’une image vidéo qui contient des données d’image valides.
ms.assetid: 86a7509b-c690-49c2-bbe4-8b02d64c307c
title: Attribut MF_MT_MINIMUM_DISPLAY_APERTURE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d13252378422081044d7f2cb21e5a31098702a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127531205"
---
# <a name="mf_mt_minimum_display_aperture-attribute"></a>\_Attribut d' \_ \_ ouverture d’affichage \_ de la version MF-minimum

Définit l’ouverture d’affichage, qui est la région d’une image vidéo qui contient des données d’image valides.

## <a name="data-type"></a>Type de données

Tableau d’octets

## <a name="remarks"></a>Notes

La valeur de l’attribut est une structure [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) .

L’ouverture d’affichage minimale est la région qui contient la partie valide du signal. Les pixels en dehors de l’ouverture contiennent des données non valides et ne doivent pas être affichés.

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

[Attributs du type de média](media-type-attributes.md)
</dt> <dt>

[Rapport hauteur/largeur des images](picture-aspect-ratio.md)
</dt> <dt>

[Types de média vidéo](video-media-types.md)
</dt> <dt>

[**IMFAttributes :: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes :: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[**\_ \_ ouverture géométrique MF \_ MF**](mf-mt-geometric-aperture-attribute.md)
</dt> <dt>

[**\_ouverture de \_ l' \_ analyse \_ panoramique MF MT**](mf-mt-pan-scan-aperture-attribute.md)
</dt> </dl>

 

 




