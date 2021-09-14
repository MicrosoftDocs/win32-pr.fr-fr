---
title: Élément AUTHOR
description: l’élément author contient le nom de l’auteur d’un métafichier Windows ou d’un clip multimédia.
ms.assetid: d80aad3d-4471-4310-8d43-2733ed83103c
keywords:
- élément AUTHOR Lecteur Windows Media
topic_type:
- apiref
api_name:
- AUTHOR Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d20498ebd7c8a56edc2e32bc2e76422c9b22242
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126856083"
---
# <a name="author-element"></a>Élément AUTHOR

l’élément **author** contient le nom de l’auteur d’un métafichier Windows ou d’un clip multimédia.

``` syntax
<AUTHOR>   
   text string
</AUTHOR>
```

## <a name="attributes"></a>Attributs

Cet élément n’a pas d’attributs.

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Élément            |
|-----------------|--------------------|
| Éléments parents | **ASX**, **entrée** |
| Éléments enfants  | None               |



 

## <a name="remarks"></a>Notes

cet élément contient une chaîne de texte représentant le nom de l’auteur d’un métafichier Windows ou d’un clip multimédia. Vous pouvez utiliser l’élément **Author** au sein de l’élément **ASX** et dans les éléments d' **entrée** .

Si cet élément apparaît dans l’élément **ASX** , le texte est affiché sous la forme **Afficher** les informations.

Si cet élément apparaît dans un élément d' **entrée** , le texte est affiché en tant qu’auteur de clip.

Chaque **ASX** parent et élément d' **entrée** doit contenir au plus un élément **Author** enfant. Plusieurs éléments d' **auteur** après le premier seront ignorés et ne seront pas affichés.

## <a name="examples"></a>Exemples


```XML
<ASX VERSION="3.0">
   <AUTHOR>Neal S.</AUTHOR>   <!-- Show author -->
   <ENTRY>
      <REF HREF="mms://example.microsoft.com/clip1.asf" />
      <AUTHOR>Robert P.</AUTHOR>  <!-- Clip author -->
   </ENTRY>
</ASX>

```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 70 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Windows Informations de référence sur les éléments de métafichier multimédia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Référence du métafichier multimédia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





