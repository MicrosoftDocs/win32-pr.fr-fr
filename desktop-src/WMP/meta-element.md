---
title: Élément meta
description: L’élément Meta spécifie les métadonnées qui s’appliquent à la sélection entière.
ms.assetid: 7248e1d9-ebd1-48cb-9019-89a35eac27ae
keywords:
- élément méta Lecteur Windows Media
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311102"
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
| Enfant     | None                     |



 

## <a name="remarks"></a>Notes

le créateur d’une sélection de média Windows peut définir l’attribut name d’un élément meta sur n’importe quelle chaîne. la liste suivante répertorie des attributs de nom standard qui se trouvent dans Windows les sélections de média créées par Lecteur Windows Media et d’autres composants Microsoft.

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



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure.<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Head, élément**](head-element.md)
</dt> <dt>

[**Windows Référence des éléments de sélection de média**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





