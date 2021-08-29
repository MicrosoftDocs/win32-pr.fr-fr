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
ms.openlocfilehash: 97a3447ae17d3d34f2df3afcd92c47ec49f7f97b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984232"
---
# <a name="jet_indexrange-structure"></a>Structure JET_INDEXRANGE


_**S’applique à :** Windows | Windows Serveurs_

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


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitRecordInIndex</p> | <p>Spécifie que la plage d’index doit être traitée normalement.</p> | 
| <p>JET_bitRecordNotInIndex</p> | <p>Réservé pour un usage futur. Ne pas utiliser.</p> | 



### <a name="remarks"></a>Remarques

Chaque **JET_INDEXRANGE** structure transmise à [JetIntersectIndexes](./jetintersectindexes-function.md) représente une plage d’index, qui sera croisée par l’appel d’API. Le curseur fourni dans **JET_INDEXRANGE** doit avoir une plage d’index valide déjà définie, avec un appel réussi à [JetSetIndexRange](./jetsetindexrange-function.md).

### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JET_COLUMNID](./jet-columnid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetIntersectIndexes](./jetintersectindexes-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
