---
description: Proportions de pixels pour un type de média vidéo.
ms.assetid: e82cdd22-7d3f-4858-befd-43fa6f9f915e
title: Attribut MF_MT_PIXEL_ASPECT_RATIO (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50c0d28ea11ba664208fcfe5fc356f1f57f2878e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313941"
---
# <a name="mf_mt_pixel_aspect_ratio-attribute"></a>\_Attribut des \_ \_ \_ proportions de pixels MF MT

Proportions de pixels pour un type de média vidéo.

## <a name="data-type"></a>Type de données

**UINT64**

## <a name="remarks"></a>Notes

Les 32 bits supérieurs contiennent le numérateur des proportions de pixels et les 32 bits inférieurs contiennent le dénominateur. Le numérateur est le composant horizontal des proportions ; le dénominateur est le composant vertical.

Pour définir cet attribut, utilisez la fonction [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) . Pour récupérer cet attribut, utilisez la fonction [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) .

Les proportions de pixels décrivent la forme des pixels de l’image vidéo affichée. Définissez cet attribut si l’image a des pixels non carrés. Pour afficher correctement sur un appareil d’affichage avec des pixels carrés, l’image doit être mise à l’échelle par l’inverse des proportions de pixels de l’image.

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

[Attributs Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Rapport hauteur/largeur des images](picture-aspect-ratio.md)
</dt> </dl>

 

 




