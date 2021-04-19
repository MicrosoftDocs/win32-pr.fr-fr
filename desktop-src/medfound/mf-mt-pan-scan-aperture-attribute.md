---
description: Définit l’ouverture panoramique/numérisation, qui est la 4&\# 215 ; 3 régions de vidéo qui doivent être affichées en mode panoramique/numérisation.
ms.assetid: faa577fd-6572-46b9-9c6c-f91c47832cb5
title: Attribut MF_MT_PAN_SCAN_APERTURE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a798ba96315126daab94ba92e8791bfeac77db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521421"
---
# <a name="mf_mt_pan_scan_aperture-attribute"></a>Attribut d’ouverture de l' \_ \_ analyse panoramique MF MT \_ \_

Définit l’ouverture Pan/Scan, qui est la région 4 × 3 de la vidéo qui doit être affichée en mode panoramique/numérisation.

## <a name="data-type"></a>Type de données

Tableau d’octets

## <a name="remarks"></a>Notes

La valeur de l’attribut est une structure [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) .

Cet attribut est utilisé pour rogner la vidéo grand écran avec un proportions de 4:3. L’ouverture Pan/Scan est utilisée uniquement en mode panoramique/numérisation, qui est activée en affectant la **valeur true** à l’attribut [**\_ \_ \_ \_ analyse panoramique MF MT**](mf-mt-pan-scan-enabled-attribute.md) .

Si le mode panoramique/numérisation n’est pas activé, utilisez l’ouverture d’affichage, spécifiée par l’attribut de l' [**\_ \_ \_ \_ ouverture d’affichage minimum MF MT**](mf-mt-minimum-display-aperture-attribute.md) .

Si cet attribut n’est pas défini, l’ouverture Pan/Scan est supposée être la totalité de l’image vidéo.

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

[**\_ouverture de \_ l' \_ affichage \_ de la version MF**](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[**\_ \_ analyse panoramique MF \_ MT \_ activée**](mf-mt-pan-scan-enabled-attribute.md)
</dt> </dl>

 

 




