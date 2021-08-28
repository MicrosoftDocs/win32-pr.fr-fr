---
description: 'En savoir plus sur : structure JET_COLUMNLIST'
title: Structure JET_COLUMNLIST
TOCTitle: JET_COLUMNLIST Structure
ms:assetid: 3899676f-c96e-4f15-9089-4faea6808bc2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269228(v=EXCHG.10)
ms:contentKeyID: 32765530
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
ms.openlocfilehash: 6b7f874c95352ce29954adf46b1682dec89c7a9a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471795"
---
# <a name="jet_columnlist-structure"></a>Structure JET_COLUMNLIST


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_columnlist-structure"></a>Structure JET_COLUMNLIST

La structure **JET_COLUMNLIST** contient les informations nécessaires pour parcourir la table temporaire créée par les fonctions [JetGetColumnInfo](./jetgetcolumninfo-function.md) et [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) . Chaque ligne de la table temporaire décrit une colonne de la table spécifiée dans l’appel d’API. Cette structure est utilisée uniquement avec [JetGetColumnInfo](./jetgetcolumninfo-function.md) et [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidPresentationOrder;
      JET_COLUMNID columnidcolumnname;
      JET_COLUMNID columnidcolumnid;
      JET_COLUMNID columnidcoltyp;
      JET_COLUMNID columnidCountry;
      JET_COLUMNID columnidLangid;
      JET_COLUMNID columnidCp;
      JET_COLUMNID columnidCollate;
      JET_COLUMNID columnidcbMax;
      JET_COLUMNID columnidgrbit;
      JET_COLUMNID columnidDefault;
      JET_COLUMNID columnidBaseTableName;
      JET_COLUMNID columnidBaseColumnName;
      JET_COLUMNID columnidDefinitionName;
    } JET_COLUMNLIST;
```

### <a name="members"></a>Membres

**cbStruct**

Taille de la structure en octets. L’appel d’API met à jour ce champ, de sorte que l’appelant doit s’assurer que cette valeur correspond à sizeof (JET_COLUMNLIST).

**TableID**

Identificateur de table de la table temporaire qui a été créée. Il incombe à l’appelant de fermer la table.

**cRecord**

Nombre d’enregistrements dans la table temporaire qui a été créée par l’appel d’API.

**columnidPresentationOrder**

Identificateur de colonne de l’ordre de présentation.

L’ordre de présentation est utilisé pour trier les lignes de la table temporaire. L’ordre de présentation est un [JET_coltypLong](./jet-coltyp.md)fixe. Si le niveau d’information spécifié n’était pas un niveau compact, il est également marqué comme JET_bitColumnTTKey.

**columnidcolumnname**

Identificateur de colonne du nom de la colonne.

Si le niveau d’information spécifié n’était pas compact, il est également marqué comme JET_bitColumnTTKey.

**columnidcolumnid**

Identificateur de colonne de l’identificateur de colonne.

L’identificateur de colonne est un [JET_coltypLong](./jet-coltyp.md)fixe.

**columnidcoltyp**

Identificateur de colonne du type de colonne.

Le type de colonne est un [JET_coltypLong](./jet-coltyp.md)fixe.

**columnidCountry**

Identificateur de colonne de l’indicatif du pays.

L’indicatif du pays est un [JET_coltypShort](./jet-coltyp.md)fixe.

**columnidLangid**

Identificateur de colonne de l’identificateur de langue.

L’identificateur de langue est un [JET_coltypShort](./jet-coltyp.md)fixe.

**columnidCp**

Identificateur de colonne de la page de codes.

La page de codes est un [JET_coltypShort](./jet-coltyp.md)fixe.

**columnidCollate**

Identificateur de colonne de la séquence de classement.

La séquence de classement est un [JET_coltypShort](./jet-coltyp.md)fixe.

**columnidcbMax**

Identificateur de colonne du champ **cbMax** .

Le **cbMax** est un [JET_coltypLong](./jet-coltyp.md)fixe.

**columnidgrbit**

Identificateur de colonne du *grbits* de la colonne. Le champ *Grbit* est un [JET_coltypLong](./jet-coltyp.md)fixe. Pour plus d’informations sur ces bits, consultez [JET_COLUMNDEF](./jet-columndef-structure.md).

Les valeurs possibles pour **columnidgrbit** sont les suivantes :

JET_bitColumnTagged

JET_bitColumnFixed

JET_bitColumnUpdatable

JET_bitColumnNotNULL

JET_bitColumnAutoincrement

JET_bitColumnVersion

JET_bitColumnMultiValued

JET_bitColumnEscrowUpdate

JET_bitColumnFinalize

JET_bitColumnDeleteOnZero

JET_bitColumnUserDefinedDefault

**columnidDefault**

Identificateur de colonne de la valeur par défaut de la colonne.

La valeur par défaut est un [JET_coltypLongBinary](./jet-coltyp.md).

**columnidBaseTableName**

Identificateur de colonne du nom de la table à partir de laquelle la table a été dérivée.

Le nom de la table est un [JET_coltypText](./jet-coltyp.md).

**columnidBaseColumnName**

Identificateur de colonne du nom de la colonne à partir de laquelle la colonne a été dérivée.

Le nom de la colonne est un [JET_coltypText](./jet-coltyp.md).

**columnidDefinitionName**

Identificateur de colonne du nom de la définition de colonne.

Le nom de la définition de colonne est un [JET_coltypText](./jet-coltyp.md).

### <a name="remarks"></a>Remarques

Par défaut, l’ordre des lignes dans la table temporaire est trié par le nom de la colonne. Elle peut également être triée par identificateur de colonne. Pour plus d’informations sur le tri par identificateur de colonne, consultez [JetGetColumnInfo](./jetgetcolumninfo-function.md) et [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).

L’appel à [JetGetColumnInfo](./jetgetcolumninfo-function.md) ou [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) peut spécifier une forme compacte de résultats. Si des colonnes ont été héritées d’une table de modèle, les résultats Compact ne les stockent pas.

### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JET_COLTYP](./jet-coltyp.md)

[JET_COLUMNDEF](./jet-columndef-structure.md)

[JET_COLUMNID](./jet-columnid.md)

[JET_ERR](./jet-err.md)

[JET_GRBIT](./jet-grbit.md)

[JET_SESID](./jet-sesid.md)

[JET_TABLEID](./jet-tableid.md)

[JetGetColumnInfo](./jetgetcolumninfo-function.md)

[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)
