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
ms.openlocfilehash: a7a66bb3b7f7dfbbfd1087d1fe0ce32c4144a8bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319982"
---
# <a name="jet_objectlist-structure"></a>Structure JET_OBJECTLIST


_**S’applique à :** Windows | Serveur Windows_

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

### <a name="remarks"></a>Notes

Chaque ligne de la table temporaire correspond à un objet dans la base de données.

Lorsque la table temporaire est créée avec le paramètre *InfoLevel* dans la fonction [JetGetObjectInfo](./jetgetobjectinfo-function.md) définie sur JET_ObjInfoListNoStats, les colonnes identifiées par **columnidcRecord** et **columnidcPage** ne contiennent pas d’informations significatives.

Actuellement, seules les informations sur les tables se trouvent dans la table temporaire.

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

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_TABLECREATE](./jet-tablecreate-structure.md)  
[JetGetObjectInfo](./jetgetobjectinfo-function.md)
