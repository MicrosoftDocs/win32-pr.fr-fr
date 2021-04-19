---
title: Slider. backgroundColor
description: L’attribut backgroundColor spécifie ou récupère la couleur d’arrière-plan du contrôle Slider.
ms.assetid: 8f2c48ec-29f5-4fbe-aa62-c7cfb8a8678c
keywords:
- Slider. backgroundColor lecteur Windows Media
topic_type:
- apiref
api_name:
- SLIDER.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06cc595af13b28541fcc570e130da4e804fdeafe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542226"
---
# <a name="sliderbackgroundcolor"></a>Slider. backgroundColor

L’attribut **backgroundColor** spécifie ou récupère la couleur d’arrière-plan du contrôle Slider.

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture contenant toute valeur de couleur Microsoft Internet Explorer. Il n'a aucune valeur par défaut.

## <a name="remarks"></a>Notes

Un contrôle Slider de base peut être construit en spécifiant **backgroundColor** ou **BackgroundImage**, et **foregroundColor** ou **foregroundImage**.

Lorsque vous utilisez les couleurs, les dimensions du contrôle Slider définissent la zone remplie par la couleur d’arrière-plan. La couleur de premier plan couvre la couleur d’arrière-plan lorsque la position du curseur augmente.

Pour créer un remplissage dégradé de la zone occupée par la couleur d’arrière-plan ou de premier plan, spécifiez les attributs **backgroundEndColor** ou **foregroundEndColor** .

Consultez *CUSTOMSLIDER*. attribut [positionImage](customslider-positionimage.md) pour un exemple illustrant l’utilisation des attributs de l’élément **Slider** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence de couleur**](color-reference.md)
</dt> <dt>

[**Slider (élément)**](slider-element.md)
</dt> <dt>

[**Slider. backgroundEndColor**](slider-backgroundendcolor.md)
</dt> <dt>

[**Slider. backgroundImage**](slider-backgroundimage.md)
</dt> <dt>

[**Slider. foregroundColor**](slider-foregroundcolor.md)
</dt> <dt>

[**Slider. foregroundEndColor**](slider-foregroundendcolor.md)
</dt> <dt>

[**Slider. foregroundImage**](slider-foregroundimage.md)
</dt> </dl>

 

 





