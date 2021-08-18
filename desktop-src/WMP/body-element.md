---
title: Élément Body
description: L’élément Body contient les éléments qui définissent le contenu d’une sélection.
ms.assetid: 96d09635-c360-4a36-a56e-6cecbbd4ff30
keywords:
- élément body Lecteur Windows Media
topic_type:
- apiref
api_name:
- body Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c785b7db7b44177469596450ee75a460e2bc6224b191a2811baf95380bea25a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135952"
---
# <a name="body-element"></a>Élément Body

L’élément **Body** contient les éléments qui définissent le contenu d’une sélection.

``` syntax
<body>
</body>
```

## <a name="attributes"></a>Attributs

Cet élément n’a pas d’attributs.

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy | Éléments                 |
|-----------|--------------------------|
| Parent    | [SMIL](smil-element.md) |
| Enfant     | [séquentiel](seq-element.md)   |



 

## <a name="remarks"></a>Remarques

Le contenu d’une sélection est organisé dans un élément **Seq** qui est contenu dans l’élément **Body** . En général, il existe soit un élément **Seq** qui définit un ensemble statique d’éléments multimédias **et contient des éléments multimédias,** soit un élément qui définit un ensemble dynamique d’éléments multimédias et contient un élément **smartPlaylist** .

## <a name="examples"></a>Exemples


```XML
<body>
    <seq>
        <media></media>
        <media></media>
        <media></media>
    </seq>
</body>

<body>
    <seq>
        <smartPlaylist></smartPlaylist>
    </seq>
</body>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure.<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément multimédia**](media-element.md)
</dt> <dt>

[**Seq, élément**](seq-element.md)
</dt> <dt>

[**Élément smartPlaylist**](smartplaylist-element.md)
</dt> <dt>

[**Élément smil**](smil-element.md)
</dt> <dt>

[**Windows Référence des éléments de sélection de média**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





