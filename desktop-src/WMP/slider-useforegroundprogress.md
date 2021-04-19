---
title: Slider. useForegroundProgress
description: L’attribut useForegroundProgress spécifie ou récupère une valeur indiquant si la barre de progression du premier plan sera utilisée.
ms.assetid: 10f3b4d9-ba82-4e30-affa-50c15a809ed6
keywords:
- Slider. useForegroundProgress lecteur Windows Media
topic_type:
- apiref
api_name:
- SLIDER.useForegroundProgress
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b572933549417713158acea1a24fa9e1434c9dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539580"
---
# <a name="slideruseforegroundprogress"></a>Slider. useForegroundProgress

L’attribut **useForegroundProgress** spécifie ou récupère une valeur indiquant si la barre de progression du premier plan sera utilisée.

``` syntax
        elementID.useForegroundProgress
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **valeur booléenne** en lecture/écriture.



| Valeur | Description                              |
|-------|------------------------------------------|
| true  | Utilisez la progression du premier plan.                 |
| false | Par défaut. N’utilisez pas la progression du premier plan. |



 

## <a name="remarks"></a>Notes

Cet attribut permet d’utiliser l’attribut **foregroundProgress** , qui est utilisé principalement pour suivre la progression du téléchargement d’un fichier multimédia tout en effectuant un suivi simultané de la position de lecture actuelle du fichier à l’aide de l’attribut **value** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Slider (élément)**](slider-element.md)
</dt> <dt>

[**Slider. foregroundProgress**](slider-foregroundprogress.md)
</dt> <dt>

[**Slider. Value**](slider-value.md)
</dt> </dl>

 

 





