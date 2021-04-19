---
title: Élément smil
description: L’élément smil est toujours l’élément de niveau supérieur dans un fichier de sélection Windows Media (WPL). Il spécifie que le fichier utilise la syntaxe et la grammaire du langage SMIL (Synchronized Multimedia Integration Language).
ms.assetid: bb14f1b8-53d0-47ff-9fd3-4620a1467985
keywords:
- Élément smil lecteur Windows Media
topic_type:
- apiref
api_name:
- smil Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 78ec8900139cfbd5982228c59010674bbc14765e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541459"
---
# <a name="smil-element"></a>Élément smil

L’élément **SMIL** est toujours l’élément de niveau supérieur dans un fichier de sélection Windows Media (WPL). Il spécifie que le fichier utilise la syntaxe et la grammaire du langage SMIL (Synchronized Multimedia Integration Language).

``` syntax
<smil>
</smil>
```

## <a name="attributes"></a>Attributs

Cet élément n’a pas d’attributs.

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy | Éléments                                           |
|-----------|----------------------------------------------------|
| Parent    | Aucun                                               |
| Enfant     | [Head](head-element.md), [corps](body-element.md) |



 

## <a name="remarks"></a>Notes

Chaque playlist Windows Media doit avoir l’élément **SMIL** à sa racine.

## <a name="examples"></a>Exemples


```
<?wpl version = "1.0"?>
<smil>
    <head>
        <entity type="hellip"/>
    </head>

    <body>
        <entity type="hellip"/>
    </body>
</smil>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure.<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément Body**](body-element.md)
</dt> <dt>

[**Head, élément**](head-element.md)
</dt> <dt>

[**Informations de référence sur les éléments de sélection Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





