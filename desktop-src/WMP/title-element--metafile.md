---
title: TITLE, élément (Metafile)
description: L’élément TITLE définit une chaîne de texte spécifiant le titre d’un élément ASX ou d’un élément d’entrée.
ms.assetid: d7ad7f00-fcf2-456d-a106-98bf0a258b81
keywords:
- TITLE, élément (metafile) Lecteur Windows Media
topic_type:
- apiref
api_name:
- TITLE Element (metafile)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bdb58edbb3ffd99e8be557fdb05a7e51298fda14
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403829"
---
# <a name="title-element-metafile"></a>TITLE, élément (Metafile)

L’élément **title** définit une chaîne de texte spécifiant le titre d’un élément **ASX** ou d’un élément d' **entrée** .

``` syntax
<TITLE>
   text string
</TITLE>
```

## <a name="attributes"></a>Attributs

Cet élément n’a pas d’attributs.

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Éléments           |
|-----------------|--------------------|
| Éléments parents | **ASX**, **entrée** |
| Éléments enfants  | None               |



 

## <a name="remarks"></a>Notes

Cet élément définit une chaîne de texte qui spécifie le titre d’un élément **ASX** ou d’un élément d' **entrée** . Le titre s’affiche dans la boîte de dialogue **Propriétés** et panneau d’affichage.

Lorsque cet élément apparaît dans un élément **ASX** , le texte est affiché sous la forme **Afficher** les informations. Lorsque cet élément apparaît dans un élément **entry** , le texte est affiché sous forme d’informations de **clips** .

Si un élément **moreinfo** est également utilisé avec l’élément (parent) associé, il s’agit du texte du titre sur lequel l’utilisateur clique pour accéder à l’URL définie dans l’élément **moreinfo** .

Chaque **ASX** parent et élément d' **entrée** doit contenir au plus un élément **title** enfant. Plusieurs éléments **titre** après le premier seront ignorés et ne seront pas affichés.

## <a name="examples"></a>Exemples


```XML
<ASX VERSION="3.0">
   <TITLE>Title of the Show</TITLE>
   <ENTRY>
      <TITLE>Title of the Clip</TITLE>
      <REF HREF="mms://example.microsoft.com/clip1.asf" />
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

 

 





