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
ms.openlocfilehash: 0b54ba5bb6b4f5ed3f08b5d4cc950f77d199c525
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988242"
---
# <a name="jet_bklogtime-structure"></a>Structure JET_BKLOGTIME


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_bklogtime-structure"></a>Structure JET_BKLOGTIME

La structure **JET_BKLOGTIME** contient les éléments de date et d’heure d’un événement. Il s’agit d’une extension de [JET_LOGTIME](./jet-logtime-structure.md).

**Windows vista : JET_BKLOGTIME** est introduite dans Windows vista.

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


| <p>Name</p> | <p>Valeur</p> | 
|-------------|--------------|
| <p>sauvegarde en continu</p> | <p>0 (zéro)</p> | 
| <p>sauvegarde d’instantané</p> | <p>1</p> | 



**fReserved**

Ce champ doit être ignoré.

### <a name="remarks"></a>Remarques

Cette structure est utilisée lors du débogage.

### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista.</p> | 
| <p><strong>Serveur</strong></p> | <p>requiert Windows Server 2008.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
