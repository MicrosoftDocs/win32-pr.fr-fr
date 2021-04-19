---
title: title, élément (WPL)
description: L’élément title spécifie un titre pour la sélection.
ms.assetid: 8a214b96-d507-4dbf-b5f2-8fdfc4409fb0
keywords:
- title, élément (WPL) lecteur Windows Media
topic_type:
- apiref
api_name:
- title Element (WPL)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5649553ab51a43bd1fb0aeb78d505d7e922bf80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106524047"
---
# <a name="title-element-wpl"></a>title, élément (WPL)

L’élément **title** spécifie un titre pour la sélection.

``` syntax
<head>
    <title>Dance Songs That I Haven't Played Recently</title>
</head>
```

## <a name="attributes"></a>Attributs

Cet élément n’a pas d’attributs.

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy | Éléments                 |
|-----------|--------------------------|
| Parent    | [head](head-element.md) |
| Enfant     | Aucune                     |



 

## <a name="remarks"></a>Notes

Lorsque vous choisissez un titre pour une sélection Windows Media (WPL), considérez que le contenu de la sélection peut être dynamique. Une bonne approche consiste à baser le titre sur la logique dans les éléments d' **argument** , car c’est ce qui définit le contenu de la sélection. Voici des exemples : « mes chansons favorites de 1966 » ou « chansons de danse que je n’ai pas jouées récemment ».

## <a name="examples"></a>Exemples


```
<head>
    <title>Dance Songs That I Haven't Played Recently</title>
</head>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure.<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**argument, élément**](argument-element.md)
</dt> <dt>

[**Head, élément**](head-element.md)
</dt> <dt>

[**Informations de référence sur les éléments de sélection Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





