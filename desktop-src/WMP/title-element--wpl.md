---
title: title, élément (WPL)
description: L’élément title spécifie un titre pour la sélection.
ms.assetid: 8a214b96-d507-4dbf-b5f2-8fdfc4409fb0
keywords:
- titre, élément (WPL) Lecteur Windows Media
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403828"
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
| Enfant     | None                     |



 

## <a name="remarks"></a>Notes

lorsque vous choisissez un titre pour une sélection de média Windows (WPL), vous pouvez considérer que le contenu de la sélection peut être dynamique. Une bonne approche consiste à baser le titre sur la logique dans les éléments d' **argument** , car c’est ce qui définit le contenu de la sélection. Voici des exemples : « mes chansons favorites de 1966 » ou « chansons de danse que je n’ai pas jouées récemment ».

## <a name="examples"></a>Exemples


```
<head>
    <title>Dance Songs That I Haven't Played Recently</title>
</head>
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure.<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**argument, élément**](argument-element.md)
</dt> <dt>

[**Head, élément**](head-element.md)
</dt> <dt>

[**Windows Référence des éléments de sélection de média**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





