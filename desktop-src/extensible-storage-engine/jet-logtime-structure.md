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
ms.openlocfilehash: 4cb99f2a64877ec76afda993a76be4aeaa14c895
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987033"
---
# <a name="jet_logtime-structure"></a>Structure JET_LOGTIME


_**S’applique à :** Windows | Windows Serveurs_

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

### <a name="remarks"></a>Remarques

Cette structure est principalement destinée à être utilisée dans le débogage.

### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
