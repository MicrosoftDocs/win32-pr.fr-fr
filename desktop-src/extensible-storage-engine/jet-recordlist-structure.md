---
description: 'En savoir plus sur : structure JET_RECORDLIST'
title: Structure JET_RECORDLIST
TOCTitle: JET_RECORDLIST Structure
ms:assetid: 6b4d97a0-4b42-4f7c-bb18-b6db3c92668a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269287(v=EXCHG.10)
ms:contentKeyID: 32765579
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
ms.openlocfilehash: e83145f74d5edf97658fdadc62f018a151ee8b55
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988225"
---
# <a name="jet_recordlist-structure"></a>Structure JET_RECORDLIST


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_recordlist-structure"></a>Structure JET_RECORDLIST

La structure **JET_RECORDLIST** trouve les enregistrements qui se trouvent à l’intersection des plages d’index spécifiées lorsqu’elles sont utilisées avec la fonction [JetIntersectIndexes](./jetintersectindexes-function.md) .

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidBookmark;
    } JET_RECORDLIST;
```

### <a name="members"></a>Membres

**cbStruct**

Taille de la structure **JET_RECORDLIST** , en octets.

**TableID**

Identificateur de table d’une table temporaire qui contient les signets pour les résultats de la requête. La table est automatiquement fermée si la transaction en cours est restaurée avec [JetRollback](./jetrollback-function.md); dans le cas contraire, il doit être fermé avec [JetCloseTable](./jetclosetable-function.md).

**cRecord**

Nombre de lignes dans la table temporaire.

**columnidBookmark**

Identificateur de colonne de la colonne de signets dans la table temporaire.

### <a name="remarks"></a>Remarques

La table temporaire qui est identifiée par **TableID** a une seule colonne. Cette colonne unique contient des signets et chaque enregistrement doit tenir dans une mémoire tampon de taille JET_cbBookmarkMost octets.

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
[JetRollback](./jetrollback-function.md)
