---
title: Élément meta
description: L’élément Meta spécifie les métadonnées qui s’appliquent à la sélection entière.
ms.assetid: 7248e1d9-ebd1-48cb-9019-89a35eac27ae
keywords:
- Élément méta Windows Media Player
topic_type:
- apiref
api_name:
- meta Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9f3c41c25a0df0895c645c34f97495712b113ffc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537463"
---
# <a name="meta-element"></a>Élément meta

L’élément **meta** spécifie les métadonnées qui s’appliquent à la sélection entière.

``` syntax
<meta
    name = "string"
    content = "string"
/>
```

## <a name="attributes"></a>Attributs



| Terme                                                                       | Description                                                                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="name"></span><span id="NAME"></span>**nomme**<br/>          | Nom d’un élément de métadonnées.<br/>                                                                                       |
| <span id="content"></span><span id="CONTENT"></span>**humidité**<br/> | Valeur d’un élément de métadonnées. Par exemple, si l’attribut de nom est « genre », l’attribut de contenu peut être « Rock ».<br/> |



 

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy | Éléments                 |
|-----------|--------------------------|
| Parent    | [head](head-element.md) |
| Enfant     | Aucune                     |



 

## <a name="remarks"></a>Notes

Le créateur d’une sélection Windows Media peut définir l’attribut Name d’un élément Meta sur n’importe quelle chaîne. La liste suivante répertorie des attributs de nom standard qui se trouvent dans les listes de sélection Windows Media créées par le lecteur Windows Media et d’autres composants Microsoft.

-   Auteur
-   Category
-   Genre
-   UserName
-   UserRating
-   Générateur

## <a name="examples"></a>Exemples


```
<head>
    <meta name = "Author" content = "Frank Lee"/>
    <meta name = "Category" content = "Classic"/>
    <meta name = "Genre" content = "Rock"/>
</head>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure.<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Head, élément**](head-element.md)
</dt> <dt>

[**Informations de référence sur les éléments de sélection Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





