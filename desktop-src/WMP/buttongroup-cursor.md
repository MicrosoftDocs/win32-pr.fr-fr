---
title: BUTTONGROUP. Cursor
description: L’attribut Cursor spécifie ou récupère le type de curseur qui apparaît lorsque la souris se trouve sur un bouton dans le BUTTONGROUP.
ms.assetid: c1b7e3e1-862b-48c1-bd2d-d9abd9ada14c
keywords:
- BUTTONGROUP. cursor Lecteur Windows Media
topic_type:
- apiref
api_name:
- BUTTONGROUP.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b3de12950aed383f48dcde5d8978724037f86e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126855640"
---
# <a name="buttongroupcursor"></a>BUTTONGROUP. Cursor

L’attribut **Cursor** spécifie ou récupère le type de curseur qui apparaît lorsque la souris se trouve sur un bouton dans le **BUTTONGROUP**.

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture contenant l’une des valeurs suivantes.



| Valeur            | Description                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| système           | Par défaut. Curseur dépendant de la plateforme (généralement une flèche).                                      |
| Toutefois             | Toutefois.                                                                                       |
| help             | Flèche avec un point d’interrogation indiquant que l’aide est disponible.                                      |
| sizeall          | Flèche à quatre pointes pointant vers le Nord, le sud, l’est et l’Ouest.                                   |
| sizenesw         | Flèche à deux pointes pointant vers le nord-est et le sud-ouest.                                      |
| sizens           | Flèche à deux pointes pointant vers le Nord et le sud.                                              |
| sizenwse         | Flèche à deux pointes pointant vers le Nord-Ouest et le sud-est.                                      |
| sizewe           | Flèche à deux pointes pointant vers l’Ouest et l’est.                                                |
| haut          | Flèche verticale pointant vers le haut.                                                             |
| \*. ani ou \* . cur | Tout fichier. ani ou. cur (doit se trouver dans le même répertoire que le fichier. WMS ou dans le fichier. WMZ). |



 

## <a name="remarks"></a>Notes

Le curseur spécifié s’applique à tous les boutons du **BUTTONGROUP**.

Si vous spécifiez une valeur de curseur non valide, elle reste à la valeur précédemment définie.

Les chemins d’accès aux noms de fichiers de curseur sont ignorés, donc le fichier curseur doit se trouver dans le répertoire par défaut.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément BUTTONGROUP**](buttongroup-element.md)
</dt> </dl>

 

 





