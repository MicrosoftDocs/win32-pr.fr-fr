---
title: Seq, élément
description: L’élément SEQ contient des éléments qui définissent une sélection statique ou des éléments qui définissent une sélection intelligente.
ms.assetid: 849f7b38-25f2-4708-a83c-e651812a1a72
keywords:
- Seq, élément Windows Media Player
topic_type:
- apiref
api_name:
- seq Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b08b3f4dfa448e48f3a9d2472c6ddb46a4d4dfaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542263"
---
# <a name="seq-element"></a>Seq, élément

L’élément **Seq** contient des éléments qui définissent une sélection statique ou des éléments qui définissent une sélection intelligente.

``` syntax
<seq>
</seq>
```

## <a name="attributes"></a>Attributs

Cet élément n’a pas d’attributs.

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy | Éléments                                                               |
|-----------|------------------------------------------------------------------------|
| Parent    | [body](body-element.md)                                               |
| Enfant     | [média](media-element.md), [smartPlaylist](smartplaylist-element.md) |



 

## <a name="remarks"></a>Notes

Lorsqu’un élément **Seq** contient uniquement des éléments **multimédias** qui font référence à des éléments multimédias spécifiques, la sélection est considérée comme statique. Lorsqu’un élément **Seq** contient un élément **smartPlaylist** , il est considéré comme une sélection « intelligente » dynamique.

## <a name="examples"></a>Exemples


```
<seq>
    <media></media>
    <media></media>
</seq>

<seq>
    <smartPlaylist></smartPlaylist>
</seq>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure.<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément Body**](body-element.md)
</dt> <dt>

[**Élément multimédia**](media-element.md)
</dt> <dt>

[**Élément smartPlaylist**](smartplaylist-element.md)
</dt> <dt>

[**Informations de référence sur les éléments de sélection Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





