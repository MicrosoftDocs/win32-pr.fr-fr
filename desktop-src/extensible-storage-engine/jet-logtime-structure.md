---
description: 'En savoir plus sur : structure JET_LOGTIME'
title: Structure JET_LOGTIME
TOCTitle: JET_LOGTIME Structure
ms:assetid: cb7c0b74-db7a-4e48-80b8-37b3fdf6d088
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294089(v=EXCHG.10)
ms:contentKeyID: 32765704
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
ms.openlocfilehash: 9c99e2c1f77a01c33a75d3e5d16c4fe58c122a4e
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "103762427"
---
# <a name="jet_logtime-structure"></a>Structure JET_LOGTIME


_**S’applique à :** Windows | Serveur Windows_

## <a name="jet_logtime-structure"></a>Structure JET_LOGTIME

La structure **JET_LOGTIME** contient les éléments de la date et de l’heure d’un événement.

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
  char bFiller2;
} JET_LOGTIME;
```

### <a name="members"></a>Membres

**bSeconds**

Heure de l’événement, en secondes. Cette valeur peut être comprise entre 0 et 59. la valeur 0 est utilisée lorsque la structure a la valeur null.

**bMinutes**

Heure de l’événement, en minutes. Cette valeur peut être comprise entre 0 et 59. la valeur 0 est utilisée lorsque la structure a la valeur null.

**bHours**

Heure de l’événement, en heures. Cette valeur peut être comprise entre 0 et 23. la valeur 0 est utilisée lorsque la structure a la valeur null.

**bDay**

Jour du mois de l’événement. Cette valeur peut être comprise entre 0 et 31. la valeur 0 est utilisée lorsque la structure a la valeur null.

**bMonth**

Mois de l’année de l’événement. Cette valeur peut être comprise entre 0 et 12. la valeur 0 est utilisée lorsque la structure a la valeur null.

**bYear**

Année de l’événement (décalage par 1900). Pour obtenir l’année réelle, ajoutez 1900 à cette valeur. la valeur 0 est utilisée lorsque la structure a la valeur null.

**bFiller1**

Ce champ doit être ignoré.

**fTimeIsUTC**

L’heure est au format UTC.

**fUnused**

Ce champ doit être ignoré.

**bFiller2**

Ce champ doit être ignoré.

### <a name="remarks"></a>Notes

Cette structure est principalement destinée à être utilisée dans le débogage.

### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>En-tête</strong></p></td>
<td><p>Déclaré dans esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Voir aussi

[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
