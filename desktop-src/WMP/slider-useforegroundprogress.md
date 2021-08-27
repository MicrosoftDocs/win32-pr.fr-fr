---
title: Slider. useForegroundProgress
description: L’attribut useForegroundProgress spécifie ou récupère une valeur indiquant si la barre de progression du premier plan sera utilisée.
ms.assetid: 10f3b4d9-ba82-4e30-affa-50c15a809ed6
keywords:
- slider. useForegroundProgress Lecteur Windows Media
topic_type:
- apiref
api_name:
- SLIDER.useForegroundProgress
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 563f5776791ba0f140dfe907facf85965bddbdc8fc69f35185f72e3de95518fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118832555"
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



 

## <a name="remarks"></a>Remarques

Cet attribut permet d’utiliser l’attribut **foregroundProgress** , qui est utilisé principalement pour suivre la progression du téléchargement d’un fichier multimédia tout en effectuant un suivi simultané de la position de lecture actuelle du fichier à l’aide de l’attribut **value** .

## <a name="requirements"></a>Conditions requises



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

 

 





