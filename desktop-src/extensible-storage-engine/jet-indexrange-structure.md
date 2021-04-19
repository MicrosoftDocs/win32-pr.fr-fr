---
description: 'En savoir plus sur : structure JET_INDEXRANGE'
title: Structure JET_INDEXRANGE
TOCTitle: JET_INDEXRANGE Structure
ms:assetid: 8e437f7d-1e21-4a0b-a5a5-1c78235a4f80
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269335(v=EXCHG.10)
ms:contentKeyID: 32765624
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
ms.openlocfilehash: ecbd8151be8ef278fc1bddc12323f41abd05b09e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544985"
---
# <a name="jet_indexrange-structure"></a>Structure JET_INDEXRANGE


_**S’applique à :** Windows | Serveur Windows_

## <a name="jet_indexrange-structure"></a>Structure JET_INDEXRANGE

La structure **JET_INDEXRANGE** identifie une plage d’index lorsqu’elle est utilisée avec la fonction [JetIntersectIndexes](./jetintersectindexes-function.md) .

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      JET_GRBIT grbit;
    } JET_INDEXRANGE;
```

### <a name="members"></a>Membres

**cbStruct**

Taille, en octets, de la **JET_INDEXRANGE**.

**TableID**

Un curseur ayant précédemment une plage d’index définie avec [JetSetIndexRange](./jetsetindexrange-function.md).

**grbit**

Masque de masque composé exactement d’un des éléments suivants.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valeur</p></th>
<th><p>Signification</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitRecordInIndex</p></td>
<td><p>Spécifie que la plage d’index doit être traitée normalement.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRecordNotInIndex</p></td>
<td><p>Réservé pour un usage futur. Ne pas utiliser.</p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a>Notes

Chaque **JET_INDEXRANGE** structure transmise à [JetIntersectIndexes](./jetintersectindexes-function.md) représente une plage d’index, qui sera croisée par l’appel d’API. Le curseur fourni dans **JET_INDEXRANGE** doit avoir une plage d’index valide déjà définie, avec un appel réussi à [JetSetIndexRange](./jetsetindexrange-function.md).

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

[JET_COLUMNID](./jet-columnid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetIntersectIndexes](./jetintersectindexes-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
