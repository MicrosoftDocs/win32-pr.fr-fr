---
title: Slider. bordure
description: L’attribut de bordure spécifie ou récupère la largeur de la bordure en pixels.
ms.assetid: ca766b45-1be3-4207-8cd0-ad50c33d52be
keywords:
- Slider. bordure du lecteur Windows Media
topic_type:
- apiref
api_name:
- SLIDER.borderSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c3ebc95e3ecf04ae78fa78c4b46f38fdd910004
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539286"
---
# <a name="sliderbordersize"></a>Slider. bordure

L’attribut de **bordure** spécifie ou récupère la largeur de la bordure en pixels.

``` syntax
        elementID.borderSize
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **nombre** en lecture/écriture (**long**) représentant la largeur de la bordure en pixels. La valeur par défaut est zéro.

## <a name="remarks"></a>Notes

Cet attribut définit un décalage à partir du début et de la fin du contrôle Slider, de gauche à droite si l’attribut **direction** est défini sur « horizontal », et du haut et du bas s’il est défini sur « vertical ». Ces positions de décalage déterminent les positions minimale et maximale du curseur de défilement, au-delà duquel la couleur ou l’image de premier plan ne sera pas appliquée.

Si une image d’arrière-plan est utilisée avec l’attribut **tileed** défini sur true, le décalage est appliqué à l’image, en dictant la quantité d’image (à partir de la gauche et de la droite ou du haut et du bas) à utiliser pour les bordures de début et de fin du contrôle Slider, avec la partie centrale de l’image en mosaïque dans le reste. De cette façon, une petite image d’arrière-plan peut être utilisée pour couvrir la longueur totale d’un contrôle Slider plus grand.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Slider (élément)**](slider-element.md)
</dt> <dt>

[**Slider. foregroundColor**](slider-foregroundcolor.md)
</dt> <dt>

[**Slider. foregroundImage**](slider-foregroundimage.md)
</dt> <dt>

[**Slider. thumbImage**](slider-thumbimage.md)
</dt> <dt>

[**Slider. en mosaïque**](slider-tiled.md)
</dt> </dl>

 

 





