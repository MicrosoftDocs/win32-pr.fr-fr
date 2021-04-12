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
ms.openlocfilehash: 6c4849c23e742657d8f5eaba8a030426f7a2a440
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210118"
---
# <a name="jet_bkinfo-structure"></a>Structure JET_BKINFO


_**S’applique à :** Windows | Serveur Windows_

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

**Windows Vista : bklogtimeMark** est introduit dans Windows Vista.

**genLow**

Numéro de génération de journal faible associé à cet événement de sauvegarde.

**genHigh**

Numéro de génération de journal élevé associé à cet événement de sauvegarde.

### <a name="remarks"></a>Notes

Cette structure est utilisée à l’intérieur de la structure [JET_DBINFOMISC](./jet-dbinfomisc-structure.md) pour représenter des données relatives à l’événement de sauvegarde de la base de données.

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

[JET_LGPOS](./jet-lgpos-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_BKLOGTIME](./jet-bklogtime-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
