---
title: CUSTOMSLIDER. Cursor
description: L’attribut Cursor spécifie ou récupère la valeur du curseur de contrôle Slider qui apparaît lorsque la souris se trouve sur le curseur.
ms.assetid: 965c21ab-18a0-4459-9d5b-0a35ea2c212f
keywords:
- CUSTOMSLIDER. cursor Lecteur Windows Media
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e836dc7ec6efececf81789efe43d8b19d0df1783
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127228467"
---
# <a name="customslidercursor"></a>CUSTOMSLIDER. Cursor

L’attribut **Cursor** spécifie ou récupère la valeur du curseur de contrôle Slider qui apparaît lorsque la souris se trouve sur le curseur.

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture.



| Valeur            | Description                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| système           | Curseur dépendant de la plateforme (généralement une flèche).                                               |
| Toutefois             | Par défaut. Le curseur est une main.                                                                  |
| help             | Flèche avec un point d’interrogation indiquant que l’aide est disponible.                                      |
| sizeall          | Flèche à quatre pointes pointant vers le Nord, le sud, l’est et l’Ouest.                                   |
| sizenesw         | Flèche à deux pointes pointant vers le nord-est et le sud-ouest.                                      |
| sizens           | Flèche à deux pointes pointant vers le Nord et le sud.                                              |
| sizenwse         | Flèche à deux pointes pointant vers le Nord-Ouest et le sud-est.                                      |
| sizewe           | Flèche à deux pointes pointant vers l’Ouest et l’est.                                                |
| haut          | Flèche verticale pointant vers le haut.                                                             |
| \*. ani ou \* . cur | Tout fichier. ani ou. cur (doit se trouver dans le même répertoire que le fichier. WMS ou dans le fichier. WMZ). |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément CUSTOMSLIDER**](customslider-element.md)
</dt> </dl>

 

 





