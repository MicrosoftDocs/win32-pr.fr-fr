---
title: Élément REPEAT
description: l’élément repeat définit le nombre de fois Lecteur Windows Media répète un ou plusieurs éléments entry ou ENTRYREF.
ms.assetid: 1a825f2b-29a7-4180-93df-51b3b5dd14e5
keywords:
- répéter l’élément Lecteur Windows Media
topic_type:
- apiref
api_name:
- REPEAT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aff7d5eaa9594882b029f0b02f4888d93fff01d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416200"
---
# <a name="repeat-element"></a>Élément REPEAT

l’élément **repeat** définit le nombre de fois Lecteur Windows Media répète un ou plusieurs éléments **entry** ou **ENTRYREF** .

``` syntax
<REPEAT   
   COUNT = "integer"
>
</REPEAT>
```

## <a name="attributes"></a>Attributs

**COUNT**

entier représentant le nombre de fois Lecteur Windows Media répète les éléments **entry** et **ENTRYREF** dans la portée de cet élément.

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Éléments                |
|-----------------|-------------------------|
| Éléments parents | **ASX**                 |
| Éléments enfants  | **entrée**, **ENTRYREF** |



 

## <a name="remarks"></a>Notes

cet élément définit le nombre de fois Lecteur Windows Media répète, ou parcourt, les clips définis par les éléments **entry** et **ENTRYREF** dans la portée de cet élément. Seul le premier élément **REPEAT** d’un métafichier est valide ; les éléments **REPEAT** suivants sont ignorés.

Si aucun attribut **Count** n’est défini, le contenu des éléments d' **entrée** et de **ENTRYREF** associés se répète un nombre infini de fois. si la valeur est zéro, Lecteur Windows Media ignore l’élément **REPEAT** et joue le contenu une seule fois.

## <a name="examples"></a>Exemples


```XML
<ASX VERSION="3.0">
   <ENTRY>
        <REF HREF="mms://example.microsoft.com/clip1.asf" />
<!-- This clip plays once. -->
   </ENTRY>

   <REPEAT COUNT="2">
      <ENTRY>
     <REF HREF="mms://example.microsoft.com/clip2.asf" />
     <REF HREF="mms://example.microsoft.com/clip3.asf" />
 <!-- These clips play twice. -->
      </ENTRY>
   </REPEAT>
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

 

 





