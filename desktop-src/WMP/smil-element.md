---
title: Élément smil
description: l’élément smil est toujours l’élément de niveau supérieur dans un fichier de sélection de média Windows (WPL). Il spécifie que le fichier utilise la syntaxe et la grammaire du langage SMIL (Synchronized Multimedia Integration Language).
ms.assetid: bb14f1b8-53d0-47ff-9fd3-4620a1467985
keywords:
- Lecteur Windows Media de l’élément smil
topic_type:
- apiref
api_name:
- smil Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 15ed9c3d70b0af65019cd384bc68ab9c26f8d01673481b9ced3595730379bf1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763459"
---
# <a name="smil-element"></a>Élément smil

l’élément **smil** est toujours l’élément de niveau supérieur dans un fichier de sélection de média Windows (WPL). Il spécifie que le fichier utilise la syntaxe et la grammaire du langage SMIL (Synchronized Multimedia Integration Language).

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



 

## <a name="remarks"></a>Remarques

chaque sélection de média Windows doit avoir l’élément **smil** à sa racine.

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

[**Windows Référence des éléments de sélection de média**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





