---
title: Slider. en mosaïque
description: L’attribut tileed spécifie ou récupère une valeur indiquant si l’image du curseur sera affichée en mosaïque.
ms.assetid: 159a2972-a0eb-4e43-a083-e124e56782f5
keywords:
- Slider. lecteur Windows Media en mosaïque
topic_type:
- apiref
api_name:
- SLIDER.tiled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b1448f496ee45d6c8b01356499b9628c745d69f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528739"
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



 

## <a name="remarks"></a>Notes

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

 

 





