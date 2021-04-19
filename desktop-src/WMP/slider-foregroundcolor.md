---
title: Slider. foregroundColor
description: L’attribut foregroundColor spécifie ou récupère la couleur de premier plan du contrôle Slider.
ms.assetid: 8c8de4a9-0021-41ed-aeb8-75653855b6f1
keywords:
- Slider. foregroundColor lecteur Windows Media
topic_type:
- apiref
api_name:
- SLIDER.foregroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d334dff4d9b7d90582e44018bf8f56c04fa784a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534866"
---
# <a name="sliderforegroundcolor"></a>Slider. foregroundColor

L’attribut **foregroundColor** spécifie ou récupère la couleur de premier plan du contrôle Slider.

``` syntax
        elementID.foregroundColor
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture contenant toute valeur de couleur Microsoft Internet Explorer. La valeur par défaut est « White ».

## <a name="remarks"></a>Notes

Un contrôle Slider de base peut être construit en spécifiant l’une des deux paires d’attributs : **backgroundColor** et **ForegroundColor**, ou **BackgroundImage** et **foregroundImage**.

Quand vous construisez un contrôle Slider à l’aide des attributs Color, les dimensions du contrôle Slider définissent la zone remplie par la couleur d’arrière-plan. La couleur de premier plan couvre la couleur d’arrière-plan lorsque la position du curseur augmente.

Pour créer un remplissage dégradé dans la zone occupée par la couleur d’arrière-plan ou de premier plan, spécifiez les attributs **backgroundEndColor** ou **foregroundEndColor** .

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

[**Slider. backgroundColor**](slider-backgroundcolor.md)
</dt> <dt>

[**Slider. backgroundEndColor**](slider-backgroundendcolor.md)
</dt> <dt>

[**Slider. foregroundEndColor**](slider-foregroundendcolor.md)
</dt> <dt>

[**Slider. foregroundImage**](slider-foregroundimage.md)
</dt> </dl>

 

 





