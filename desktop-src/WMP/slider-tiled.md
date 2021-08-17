---
title: Slider. en mosaïque
description: L’attribut tileed spécifie ou récupère une valeur indiquant si l’image du curseur sera affichée en mosaïque.
ms.assetid: 159a2972-a0eb-4e43-a083-e124e56782f5
keywords:
- slider. mosaïque Lecteur Windows Media
topic_type:
- apiref
api_name:
- SLIDER.tiled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a97be7ee857574b24585ffd7ffd9b63acdfad0a37762445699daa3a06f94e97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118832535"
---
# <a name="slidertiled"></a>Slider. en mosaïque

L’attribut **tileed** spécifie ou récupère une valeur indiquant si l’image du curseur sera affichée en mosaïque.

``` syntax
        elementID.tiled
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **valeur booléenne** en lecture/écriture.



| Valeur | Description                                                                                 |
|-------|---------------------------------------------------------------------------------------------|
| true  | Par défaut. La bitmap de l’image est répétée jusqu’à ce qu’elle remplisse toute la région du contrôle. |
| false | L’image ne sera pas affichée en mosaïque.                                                                |



 

## <a name="remarks"></a>Remarques

Cet attribut s’applique uniquement si vous utilisez des images de premier plan et d’arrière-plan pour définir un contrôle Slider. Si les images sont plus petites que la zone définie du curseur et que l’attribut **tileed** a la valeur true, les images sont répétées jusqu’à ce qu’elles remplissent la longueur totale du contrôle.

Vous pouvez utiliser cet attribut conjointement avec l’attribut de **bordure** . L’attribut de **bordure** vous permet de définir une bordure qui n’est pas répétée pendant la mosaïque.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Slider (élément)**](slider-element.md)
</dt> <dt>

[**Slider. backgroundImage**](slider-backgroundimage.md)
</dt> <dt>

[**Slider. bordure**](slider-bordersize.md)
</dt> <dt>

[**Slider. foregroundImage**](slider-foregroundimage.md)
</dt> </dl>

 

 





