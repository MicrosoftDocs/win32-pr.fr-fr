---
title: BUTTONELEMENT. Cursor
description: L’attribut Cursor spécifie ou récupère la valeur du curseur BUTTONELEMENT qui apparaît lorsque la souris se trouve sur le BUTTONELEMENT.
ms.assetid: 29e7fadb-30d8-40e4-9a64-6b6f45eac80a
keywords:
- BUTTONELEMENT. cursor Lecteur Windows Media
topic_type:
- apiref
api_name:
- BUTTONELEMENT.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82f08d8e6b26ac2227d9040249b2daca55dcbe0ec068e120f1aba962bea0f089
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764479"
---
# <a name="buttonelementcursor"></a>BUTTONELEMENT. Cursor

L’attribut **Cursor** spécifie ou récupère la valeur du curseur **BUTTONELEMENT** qui apparaît lorsque la souris se trouve sur le **BUTTONELEMENT**.

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture.



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



 

## <a name="remarks"></a>Remarques

Si une valeur non valide est spécifiée, la valeur précédente est conservée.

Les chemins d’accès aux noms de fichiers de curseur sont ignorés, donc le fichier curseur doit se trouver dans le répertoire par défaut.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément BUTTONELEMENT**](buttonelement-element.md)
</dt> </dl>

 

 





