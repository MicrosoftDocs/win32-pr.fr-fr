---
title: Slider. thumbImage
description: L’attribut thumbImage spécifie ou récupère l’image qui sera utilisée pour représenter la position actuelle du curseur.
ms.assetid: 3aa69188-3443-483c-81a9-bf22832509d8
keywords:
- slider. thumbImage Lecteur Windows Media
topic_type:
- apiref
api_name:
- SLIDER.thumbImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0711cb7a652032db4b167040fbd604d1e561885926bf8fc7c31d1fedb65049e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995139"
---
# <a name="sliderthumbimage"></a>Slider. thumbImage

L’attribut **thumbImage** spécifie ou récupère l’image qui sera utilisée pour représenter la position actuelle du curseur.

``` syntax
        elementID.thumbImage
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture contenant le nom d’un fichier image.

## <a name="remarks"></a>Remarques

Le **thumbImage** spécifie l’image qui sera utilisée pour représenter la position actuelle, ainsi que pour indiquer que l’utilisateur peut agir avec le contrôle. Si aucune image Thumb n’est spécifiée, le curseur est non interactif.

L’image Thumb est centrée dans la dimension étroite du contrôle Slider. Si l’image Thumb est plus étroite que le contrôle, l’image apparaît au milieu de l’arrière-plan. Si l’image Thumb est plus grande que le contrôle, les extrémités de l’image sont coupées.

La position du curseur est spécifiée par le centre de l’image Thumb. Si la **bordure** est égale à zéro, seule la moitié de l’image Thumb sera visible aux positions des curseurs de début et de fin. Pour éviter cela, définissez la **bordure** sur une valeur supérieure ou égale à la moitié de la largeur de l’image Thumb (ou de la moitié de la hauteur si la **direction** est définie sur « vertical »).

Les formats pris en charge sont BMP, JPG, PNG et GIF (à l’exclusion des GIF animés).

Consultez **CUSTOMSLIDER**. attribut [positionImage](customslider-positionimage.md) pour un exemple illustrant l’utilisation des attributs de l’élément **Slider** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Slider (élément)**](slider-element.md)
</dt> <dt>

[**Slider. bordure**](slider-bordersize.md)
</dt> <dt>

[**Slider. direction**](slider-direction.md)
</dt> </dl>

 

 





