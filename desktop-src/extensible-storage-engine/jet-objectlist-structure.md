---
description: 'En savoir plus sur : structure JET_OBJECTLIST'
title: Structure JET_OBJECTLIST
TOCTitle: JET_OBJECTLIST Structure
ms:assetid: 95f12f2a-13da-48d4-a254-fc0cb718b17d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269348(v=EXCHG.10)
ms:contentKeyID: 32765635
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 21a3ea030421406a5bc571bb5cc1887f77b4710d
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983122"
---
# <a name="jet_objectlist-structure"></a>Structure JET_OBJECTLIST


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_objectlist-structure"></a>Structure JET_OBJECTLIST

La structure **JET_OBJECTLIST** parcourt une table temporaire qui a été créée avec [JetGetObjectInfo](./jetgetobjectinfo-function.md). Chaque ligne de la table temporaire décrit un objet dans la base de données.

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidcontainername;
      JET_COLUMNID columnidobjectname;
      JET_COLUMNID columnidobjtyp;
      JET_COLUMNID columniddtCreate;
      JET_COLUMNID columniddtUpdate;
      JET_COLUMNID columnidgrbit;
      JET_COLUMNID columnidflags;
      JET_COLUMNID columnidcRecord;
      JET_COLUMNID columnidcPage;
    } JET_OBJECTLIST;
```

### <a name="members"></a>Membres

**cbStruct**

Taille de la structure en octets. L’appel d’API met à jour ce champ, de sorte que l’appelant doit s’assurer que cette valeur correspond à sizeof (JET_INDEXLIST).

**TableID**

Identificateur de table de la table temporaire qui a été créée. L’appelant doit contenir le code qui va fermer la table.

**cRecord**

Nombre d’enregistrements dans la table temporaire qui a été créée.

**columnidcontainername**

Identificateur de colonne du nom du type de conteneur.

Les seuls conteneurs actuellement pris en charge sont les tables. Cette colonne est une [JET_coltypText](./jet-coltyp.md).

**columnidobjectname**

Identificateur de colonne du nom de l’objet.

Cette colonne est une [JET_coltypText](./jet-coltyp.md).

**columnidobjtyp**

Identificateur de colonne du type de l’objet. Les seuls conteneurs actuellement pris en charge sont des tables, ce qui signifie que ce champ sera JET_objtypTable.

Cette colonne est une [JET_coltypLong](./jet-coltyp.md).

**columniddtCreate**

Obsolète. Ne pas utiliser.

**columniddtUpdate**

Obsolète. Ne pas utiliser.

**columnidgrbit**

Identificateur de colonne des **grbits** applicables à l’objet. Pour obtenir la liste des **grbits** applicables, consultez [JET_TABLECREATE](./jet-tablecreate-structure.md).

Cette colonne est une [JET_coltypLong](./jet-coltyp.md).

**columnidflags**

Identificateur de colonne des indicateurs applicables à l’objet. Pour obtenir la liste des indicateurs applicables, consultez [JET_OBJECTINFO](./jet-objectinfo-structure.md).

Cette colonne est une [JET_coltypLong](./jet-coltyp.md).

**columnidcRecord**

Identificateur de colonne du nombre d’enregistrements qui sont présents dans la table nommée dans **columnidobjectname**.

Cette colonne est une [JET_coltypLong](./jet-coltyp.md).

**columnidcPage**

Identificateur de colonne du nombre de pages que l’objet utilise.

Cette colonne est une [JET_coltypLong](./jet-coltyp.md).

### <a name="remarks"></a>Remarques

Chaque ligne de la table temporaire correspond à un objet dans la base de données.

Lorsque la table temporaire est créée avec le paramètre *InfoLevel* dans la fonction [JetGetObjectInfo](./jetgetobjectinfo-function.md) définie sur JET_ObjInfoListNoStats, les colonnes identifiées par **columnidcRecord** et **columnidcPage** ne contiennent pas d’informations significatives.

Actuellement, seules les informations sur les tables se trouvent dans la table temporaire.

### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_TABLECREATE](./jet-tablecreate-structure.md)  
[JetGetObjectInfo](./jetgetobjectinfo-function.md)
