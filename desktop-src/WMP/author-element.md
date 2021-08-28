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
ms.openlocfilehash: 058753d73049debe01e442f49bf12476642111549ad890e931100026badaeb3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098889"
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



 

## <a name="remarks"></a>Remarques

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



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 70 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Windows Informations de référence sur les éléments de métafichier multimédia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Référence du métafichier multimédia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





