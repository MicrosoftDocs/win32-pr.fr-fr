---
description: 'En savoir plus sur : structure JET_BKLOGTIME'
title: Structure JET_BKLOGTIME
TOCTitle: JET_BKLOGTIME Structure
ms:assetid: 31460079-7c5b-4145-837d-b112ba0117d6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269219(v=EXCHG.10)
ms:contentKeyID: 32765522
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0b3ebfd1c0b807a491695ba18d6735e0230a16fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519480"
---
# <a name="jet_bklogtime-structure"></a>Structure JET_BKLOGTIME


_**S’applique à :** Windows | Serveur Windows_

## <a name="jet_bklogtime-structure"></a>Structure JET_BKLOGTIME

La structure **JET_BKLOGTIME** contient les éléments de date et d’heure d’un événement. Il s’agit d’une extension de [JET_LOGTIME](./jet-logtime-structure.md).

**Windows Vista : JET_BKLOGTIME** est introduite dans Windows Vista.

```cpp
    typedef struct {
      char bSeconds;
      char bMinutes;
      char bHours;
      char bDay;
      char bMonth;
        char bYear;
        union {
        char bFiller1;
        struct {
          unsigned char fTimeIsUTC: 1;
          unsigned char fUnused: 7;
        };
      };
      union {
        char bFiller2;
        struct {
          unsigned char fOSSnapshot  :1;
          unsigned char fReserved  :7;
        };
      };
    } JET_BKLOGTIME;
```

### <a name="members"></a>Membres

**bSeconds**

Heure de l’événement, en secondes. La valeur peut être comprise entre 0 (zéro) et 60. 0 (zéro) est utilisé lorsque la structure **JET_BKLOGTIME** a la valeur « null ».

**bMinutes**

Heure de l’événement, en minutes. La valeur peut être comprise entre 0 (zéro) et 60. 0 (zéro) est utilisé lorsque la structure **JET_BKLOGTIME** a la valeur « null ».

**bHours**

Heure de l’événement, en heures. La valeur peut être comprise entre 0 (zéro) et 24. 0 (zéro) est utilisé lorsque la structure **JET_BKLOGTIME** a la valeur « null ».

**bDay**

Jour du mois de l’événement. La valeur peut être comprise entre 0 (zéro) et 31. 0 (zéro) est utilisé lorsque la structure **JET_BKLOGTIME** a la valeur « null ».

**bMonth**

Mois de l’année de l’événement. La valeur peut être comprise entre 0 (zéro) et 12. 0 (zéro) est utilisé lorsque la structure **JET_BKLOGTIME** a la valeur « null ».

**bYear**

Année (décalage par 1900) de l’événement. Pour obtenir l’année réelle, ajoutez 1900 à cette valeur. 0 (zéro) est utilisé lorsque la structure **JET_BKLOGTIME** a la valeur « null ».

**bFiller1**

Ce champ doit être ignoré.

**fTimeIsUTC**

L’heure est au format UTC.

**fUnused**

Ce champ doit être ignoré.

**bFiller2**

Ce champ doit être ignoré.

**fOSSnapshot**

Si cet événement est une sauvegarde, cet indicateur contient l’une des valeurs possibles suivantes :

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom</p></th>
<th><p>Valeur</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>sauvegarde en continu</p></td>
<td><p>0 (zéro)</p></td>
</tr>
<tr class="even">
<td><p>sauvegarde d’instantané</p></td>
<td><p>1</p></td>
</tr>
</tbody>
</table>


**fReserved**

Ce champ doit être ignoré.

### <a name="remarks"></a>Notes

Cette structure est utilisée lors du débogage.

### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Nécessite Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>Requiert Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>En-tête</strong></p></td>
<td><p>Déclaré dans esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Voir aussi

[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
