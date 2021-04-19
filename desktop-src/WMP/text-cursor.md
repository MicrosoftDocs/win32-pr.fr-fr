---
title: TEXT. Cursor
description: L’attribut Cursor spécifie ou récupère une valeur indiquant le curseur qui apparaît lorsque la souris se trouve sur le contrôle Text.
ms.assetid: 360d4ed1-9c4f-4210-8e77-2dfbe7573869
keywords:
- TEXT. Cursor lecteur Windows Media
topic_type:
- apiref
api_name:
- TEXT.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8cf7b135ed0a99b5c65f760a08e4e7083234674
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528640"
---
# <a name="textcursor"></a>TEXT. Cursor

L’attribut **Cursor** spécifie ou récupère une valeur indiquant le curseur qui apparaît lorsque la souris se trouve sur le contrôle Text.

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



 

Pour obtenir un exemple illustrant l’utilisation des attributs de l’élément de **texte** , consultez l’attribut [value](text-value.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément de texte**](text-element.md)
</dt> </dl>

 

 





