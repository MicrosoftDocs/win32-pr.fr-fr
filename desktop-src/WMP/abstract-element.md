---
title: ABSTRACT, élément
description: L’élément ABSTRACT contient du texte qui décrit l’élément ASX, BANNER ou ENTRy associé.
ms.assetid: 7866fee8-1778-433a-be2f-9df0baa1c13e
keywords:
- Lecteur Windows Media d’élément abstrait
topic_type:
- apiref
api_name:
- ABSTRACT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 153759dbe4bef47693cba13549b58215e4992686eab81cdcb4dadb33aa30279f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903049"
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
| Enfant     | None                           |



 

## <a name="remarks"></a>Remarques

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

[**Windows Informations de référence sur les éléments de métafichier multimédia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Référence du métafichier multimédia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





