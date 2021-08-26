---
description: Spécifie si le mode panoramique/numérisation est activé.
ms.assetid: 9e8746c6-13a4-4cf7-9748-82223d9529fa
title: Attribut MF_MT_PAN_SCAN_ENABLED (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee1e78c38cd15f5d735d49b5689905a40d74614b46817a8621ce1dabcdc5a1b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955489"
---
# <a name="mf_mt_pan_scan_enabled-attribute"></a>\_Attribut activé pour l' \_ analyse panoramique MF MT \_ \_

Spécifie si le mode panoramique/numérisation est activé.

## <a name="data-type"></a>Type de données

**UINT32**

Traiter en tant que valeur booléenne.

## <a name="remarks"></a>Remarques

Si cet attribut a la **valeur true**, seule la zone pan/scan de la vidéo doit être affichée. La région Pan/Scan est spécifiée par l’attribut d’ouverture de l' [**\_ \_ \_ \_ analyse panoramique MF MT**](mf-mt-pan-scan-aperture-attribute.md) .

Si cet attribut a la **valeur false** ou n’est pas défini, la totalité de l’ouverture de la vidéo doit s’afficher. L’ouverture d’affichage est spécifiée par l’attribut de l' [**\_ \_ \_ \_ ouverture d’affichage minimum de MF MT**](mf-mt-minimum-display-aperture-attribute.md) .

Si vous affectez la valeur **true** à cet attribut, définissez également la valeur de l’attribut d’ouverture de l' [**\_ \_ \_ \_ analyse panoramique MF MT**](mf-mt-pan-scan-aperture-attribute.md) .

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

[Rapport hauteur/largeur des images](picture-aspect-ratio.md)
</dt> </dl>

 

 




