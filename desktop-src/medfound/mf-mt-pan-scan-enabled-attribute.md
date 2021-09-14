---
description: Spécifie si le mode panoramique/numérisation est activé.
ms.assetid: 9e8746c6-13a4-4cf7-9748-82223d9529fa
title: Attribut MF_MT_PAN_SCAN_ENABLED (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b347c898ce827ff37796a9698e843f6321db8a1d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313945"
---
# <a name="mf_mt_pan_scan_enabled-attribute"></a>\_Attribut activé pour l' \_ analyse panoramique MF MT \_ \_

Spécifie si le mode panoramique/numérisation est activé.

## <a name="data-type"></a>Type de données

**UINT32**

Traiter en tant que valeur booléenne.

## <a name="remarks"></a>Notes

Si cet attribut a la **valeur true**, seule la zone pan/scan de la vidéo doit être affichée. La région Pan/Scan est spécifiée par l’attribut d’ouverture de l' [**\_ \_ \_ \_ analyse panoramique MF MT**](mf-mt-pan-scan-aperture-attribute.md) .

Si cet attribut a la **valeur false** ou n’est pas défini, la totalité de l’ouverture de la vidéo doit s’afficher. L’ouverture d’affichage est spécifiée par l’attribut de l' [**\_ \_ \_ \_ ouverture d’affichage minimum de MF MT**](mf-mt-minimum-display-aperture-attribute.md) .

Si vous affectez la valeur **true** à cet attribut, définissez également la valeur de l’attribut d’ouverture de l' [**\_ \_ \_ \_ analyse panoramique MF MT**](mf-mt-pan-scan-aperture-attribute.md) .

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

[Rapport hauteur/largeur des images](picture-aspect-ratio.md)
</dt> </dl>

 

 




