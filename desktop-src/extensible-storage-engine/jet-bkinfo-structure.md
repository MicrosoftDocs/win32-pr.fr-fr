---
description: 'En savoir plus sur : structure JET_BKINFO'
title: Structure JET_BKINFO
TOCTitle: JET_BKINFO Structure
ms:assetid: dfaf1d72-1d5f-4777-91c1-6affb735b092
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294120(v=EXCHG.10)
ms:contentKeyID: 32765734
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
ms.openlocfilehash: 477c84ee0b466fb43ee0bb06ef14a2a1be6dd00e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472185"
---
# <a name="jet_bkinfo-structure"></a>Structure JET_BKINFO


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_bkinfo-structure"></a>Structure JET_BKINFO

La structure **JET_BKINFO** contient une collection de données relatives à un événement de sauvegarde spécifique.

```cpp
    typedef struct {
      JET_LGPOS lgposMark;
      union {
        JET_LOGTIME logtimeMark;
        JET_BKLOGTIME bklogtimeMark;
      };
      unsigned long genLow;
      unsigned long genHigh;
    } JET_BKINFO;
```

### <a name="members"></a>Membres

**lgposMark**

ID de cette sauvegarde.

**logtimeMark**

Heure de l’événement de sauvegarde.

**bklogtimeMark**

L’heure de cet événement de sauvegarde, avec des bits supplémentaires pour indiquer une sauvegarde d’instantané.

**Windows vista : bklogtimeMark** est introduit dans Windows vista.

**genLow**

Numéro de génération de journal faible associé à cet événement de sauvegarde.

**genHigh**

Numéro de génération de journal élevé associé à cet événement de sauvegarde.

### <a name="remarks"></a>Remarques

Cette structure est utilisée à l’intérieur de la structure [JET_DBINFOMISC](./jet-dbinfomisc-structure.md) pour représenter des données relatives à l’événement de sauvegarde de la base de données.

### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JET_LGPOS](./jet-lgpos-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_BKLOGTIME](./jet-bklogtime-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
