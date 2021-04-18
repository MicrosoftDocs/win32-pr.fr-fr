---
title: Élément REPEAT
description: L’élément REPEAT définit le nombre de fois où le lecteur Windows Media répète un ou plusieurs éléments ENTRy ou ENTRYREF.
ms.assetid: 1a825f2b-29a7-4180-93df-51b3b5dd14e5
keywords:
- RÉPÉTER l’élément du lecteur Windows Media
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540628"
---
# <a name="repeat-element"></a>Élément REPEAT

L’élément **REPEAT** définit le nombre de fois où le lecteur Windows Media répète un ou plusieurs éléments **entry** ou **ENTRYREF** .

``` syntax
<REPEAT   
   COUNT = "integer"
>
</REPEAT>
```

## <a name="attributes"></a>Attributs

**COUNT**

Entier représentant le nombre de fois où le lecteur Windows Media répète les éléments d' **entrée** et de **ENTRYREF** dans la portée de cet élément.

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Éléments                |
|-----------------|-------------------------|
| Éléments parents | **ASX**                 |
| Éléments enfants  | **entrée**, **ENTRYREF** |



 

## <a name="remarks"></a>Notes

Cet élément définit le nombre de fois que le lecteur Windows Media se répète, ou effectue une boucle, sur les clips définis par les éléments **entry** et **ENTRYREF** dans la portée de cet élément. Seul le premier élément **REPEAT** d’un métafichier est valide ; les éléments **REPEAT** suivants sont ignorés.

Si aucun attribut **Count** n’est défini, le contenu des éléments d' **entrée** et de **ENTRYREF** associés se répète un nombre infini de fois. La valeur zéro amène le lecteur Windows Media à ignorer l’élément **REPEAT** et à lire le contenu une seule fois.

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

 

 





