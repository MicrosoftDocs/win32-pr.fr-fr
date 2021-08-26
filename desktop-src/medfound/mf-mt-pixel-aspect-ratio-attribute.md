---
description: Proportions de pixels pour un type de média vidéo.
ms.assetid: e82cdd22-7d3f-4858-befd-43fa6f9f915e
title: Attribut MF_MT_PIXEL_ASPECT_RATIO (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 230e14e07a8011f89d16b095728bc80cbe19faa16ef9427156868f93c2ccb412
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060489"
---
# <a name="mf_mt_pixel_aspect_ratio-attribute"></a>\_Attribut des \_ \_ \_ proportions de pixels MF MT

Proportions de pixels pour un type de média vidéo.

## <a name="data-type"></a>Type de données

**UINT64**

## <a name="remarks"></a>Remarques

Les 32 bits supérieurs contiennent le numérateur des proportions de pixels et les 32 bits inférieurs contiennent le dénominateur. Le numérateur est le composant horizontal des proportions ; le dénominateur est le composant vertical.

Pour définir cet attribut, utilisez la fonction [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) . Pour récupérer cet attribut, utilisez la fonction [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) .

Les proportions de pixels décrivent la forme des pixels de l’image vidéo affichée. Définissez cet attribut si l’image a des pixels non carrés. Pour afficher correctement sur un appareil d’affichage avec des pixels carrés, l’image doit être mise à l’échelle par l’inverse des proportions de pixels de l’image.

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

[Attributs du type de média](media-type-attributes.md)
</dt> <dt>

[Attributs Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Rapport hauteur/largeur des images](picture-aspect-ratio.md)
</dt> </dl>

 

 




