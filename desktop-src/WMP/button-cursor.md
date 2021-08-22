---
title: BOUTON. curseur
description: L’attribut Cursor spécifie ou récupère le curseur qui apparaît lorsque le pointeur de la souris est positionné sur le bouton.
ms.assetid: 19bdbb23-00e2-45cf-b67d-9ada036b9c3b
keywords:
- BUTTON. cursor Lecteur Windows Media
topic_type:
- apiref
api_name:
- BUTTON.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa98c91080bc6d108e8ab62f0de99758c4eb6ba4229a83f8ded8b22bb2ec9695
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123789"
---
# <a name="buttoncursor"></a>BOUTON. curseur

L’attribut **Cursor** spécifie ou récupère le curseur qui apparaît lorsque le pointeur de la souris est positionné sur le **bouton**.

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture.



| Valeur            | Description                                                                                |
|------------------|--------------------------------------------------------------------------------------------|
| système           | Par défaut. Curseur dépendant de la plateforme (généralement une flèche).                                     |
| Toutefois             | Toutefois.                                                                                      |
| help             | Flèche avec un point d’interrogation indiquant que l’aide est disponible.                                     |
| sizeall          | Flèche à quatre pointes pointant vers le Nord, le sud, l’est et l’Ouest.                                  |
| sizenesw         | Flèche à deux pointes pointant vers le nord-est et le sud-ouest.                                     |
| sizens           | Flèche à deux pointes pointant vers le Nord et le sud.                                             |
| sizenwse         | Flèche à deux pointes pointant vers le Nord-Ouest et le sud-est.                                     |
| sizewe           | Flèche à deux pointes pointant vers l’Ouest et l’est.                                               |
| haut          | Flèche verticale pointant vers le haut.                                                            |
| \*. ani ou \* . cur | Tout fichier. ani ou. cur (doit se trouver dans le même répertoire que le fichier. WMS ou dans le fichier. WMZ) |



 

## <a name="remarks"></a>Remarques

Si le système ne reconnaît pas la valeur de curseur spécifiée, la valeur de curseur reste à la valeur précédemment définie.

Les chemins d’accès aux noms de fichiers de curseur sont ignorés, donc le fichier curseur doit se trouver dans le répertoire par défaut.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**BUTTON, élément**](button-element.md)
</dt> </dl>

 

 





