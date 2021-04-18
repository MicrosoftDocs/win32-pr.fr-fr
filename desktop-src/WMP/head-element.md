---
title: Head, élément
description: L’élément head contient des métadonnées qui s’appliquent à la sélection entière.
ms.assetid: 9554c84a-34af-4492-964a-4b262cd7c4a4
keywords:
- Élément head Windows Media Player
topic_type:
- apiref
api_name:
- head Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8708a8a683f7457e6568df3a897c71253ad76c02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540501"
---
# <a name="head-element"></a>Head, élément

L’élément **Head** contient des métadonnées qui s’appliquent à la sélection entière.

``` syntax
<head>
</head>
```

## <a name="attributes"></a>Attributs

Cet élément n’a pas d’attributs.

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy | Éléments                                                  |
|-----------|-----------------------------------------------------------|
| Parent    | [SMIL](smil-element.md)                                  |
| Enfant     | [titre](title-element--wpl.md), [méta](meta-element.md) |



 

## <a name="remarks"></a>Notes

En général, l’élément **Head** contient un élément **title** et un ou plusieurs éléments **meta** qui définissent les caractéristiques globales de la sélection.

## <a name="examples"></a>Exemples


```
<head>
    <title>Party Playlist</title>
    <meta name = "Author" CONTENT = "Frank Lee"/>
    <meta name = "Category" CONTENT = "Party Music"/>
    <meta name = "Genre" CONTENT = "Pop"/>
    <meta name = "UserName1" CONTENT = "Frank001"/>
    <meta name = "UserRating1" CONTENT = "82"/>
</head>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure.<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément meta**](meta-element.md)
</dt> <dt>

[**title, élément (WPL)**](title-element--wpl.md)
</dt> <dt>

[**Informations de référence sur les éléments de sélection Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





