---
title: ABSTRACT, élément
description: L’élément ABSTRACT contient du texte qui décrit l’élément ASX, BANNER ou ENTRy associé.
ms.assetid: 7866fee8-1778-433a-be2f-9df0baa1c13e
keywords:
- Élément abstrait lecteur Windows Media
topic_type:
- apiref
api_name:
- ABSTRACT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e90b6f52b697242be23303ab3597dac549a6177
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540595"
---
# <a name="abstract-element"></a>ABSTRACT, élément

L’élément **abstract** contient du texte qui décrit l’élément **ASX**, **Banner** ou **entry** associé.

``` syntax
<ABSTRACT>
   text string
</ABSTRACT>
      
```

## <a name="attributes"></a>Attributs

Cet élément n’a pas d’attributs.

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy | Éléments                       |
|-----------|--------------------------------|
| Parent    | **ASX**, **entrée**, **bannière** |
| Enfant     | Aucune                           |



 

## <a name="remarks"></a>Notes

Si cet élément apparaît dans un élément **ASX** , le texte s’affiche sous la forme d’une info-bulle lorsque la souris pointe sur le titre de l’affichage.

Si cet élément apparaît dans un élément d' **entrée** , le texte s’affiche sous la forme d’une info-bulle lorsque la souris pointe sur le titre du clip.

Si cet élément apparaît dans un élément de **bannière** , le texte s’affiche sous la forme d’une info-bulle pour le graphique de bannière.

Utilisez un seul élément **abstrait** par portée. Seul le premier élément **abstrait** au sein de la portée d’un autre élément est utilisé lors du traitement d’un fichier de métafichier. Tous les éléments **abstraits** suivants dans cette portée sont ignorés.

## <a name="examples"></a>Exemples


```XML
<ASX VERSION="3.0">
    <TITLE>The Title of the Show<TITLE>
    <ABSTRACT>
        Brief description of the show. 
    </ABSTRACT>

<ENTRY>    
    <REF HREF="YourMediaFilename.asf" />
    <TITLE>The Title of the Track</TITLE>
    <ABSTRACT>
        Brief description of the track.
    </ABSTRACT>
</ENTRY>
</ASX>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 70 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Informations de référence sur les éléments de métafichier Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Informations de référence sur les métafichiers Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





