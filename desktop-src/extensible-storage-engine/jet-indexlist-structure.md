---
description: 'En savoir plus sur : structure JET_INDEXLIST'
title: Structure JET_INDEXLIST
TOCTitle: JET_INDEXLIST Structure
ms:assetid: 0c092b48-e583-49f3-8f5e-1428a84d9265
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269185(v=EXCHG.10)
ms:contentKeyID: 32765488
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
ms.openlocfilehash: e21353fb780ed7346c1ff82cbc5057469da25a4b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517845"
---
# <a name="jet_indexlist-structure"></a>Structure JET_INDEXLIST


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_indexlist-structure"></a>Structure JET_INDEXLIST

La structure **JET_INDEXLIST** contient les informations nécessaires pour traverser une table temporaire créée par les fonctions [JetGetIndexInfo](./jetgetindexinfo-function.md) ou [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) . Chaque ligne de la table temporaire décrit une colonne d’un index.

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      gned long cRecord;
      JET_COLUMNID columnidindexname;
      JET_COLUMNID columnidgrbitIndex;
      JET_COLUMNID columnidcKey;
      JET_COLUMNID columnidcEntry;
      JET_COLUMNID columnidcPage;
      JET_COLUMNID columnidcColumn;
      JET_COLUMNID columnidiColumn;
      JET_COLUMNID columnidcolumnid;
      JET_COLUMNID columnidcoltyp;
      JET_COLUMNID columnidCountry;
      JET_COLUMNID columnidLangid;
      JET_COLUMNID columnidCp;
      JET_COLUMNID columnidCollate;
      JET_COLUMNID columnidgrbitColumn;
      JET_COLUMNID columnidcolumnname;
      JET_COLUMNID columnidLCMapFlags;
    } JET_INDEXLIST;
```

### <a name="members"></a>Membres

**cbStruct**

Taille de la structure en octets. L’appel d’API met à jour ce champ, de sorte que l’appelant doit s’assurer que cette valeur correspond à sizeof (JET_INDEXLIST).

**TableID**

Identificateur de table de la table temporaire qui a été créée. Il incombe à l’appelant de fermer la table.

**cRecord**

Nombre d’enregistrements dans la table temporaire qui a été créée.

**columnidindexname**

Identificateur de colonne du nom de l’index.

Cette colonne est une [JET_coltypText](./jet-coltyp.md).

**columnidgrbitIndex**

Identificateur de colonne du *grbits* utilisé sur l’index. Pour obtenir la liste des bits valides, consultez [JET_INDEXCREATE](./jet-indexcreate-structure.md) .

Cette colonne est une [JET_coltypLong](./jet-coltyp.md).

**columnidcKey**

Identificateur de colonne du nombre de clés dans l’index.

Cette colonne est une [JET_coltypLong](./jet-coltyp.md).

**columnidcEntry**

Identificateur de colonne du nombre d’entrées dans l’index.

Cette colonne est une [JET_coltypLong](./jet-coltyp.md).

**columnidcPage**

Identificateur de colonne du nombre de pages utilisées par l’index. Cette colonne est une [JET_coltypLong](./jet-coltyp.md).

**columnidcColumn**

Identificateur de colonne du nombre total de colonnes sur lesquelles l’index s’étend.

Cette colonne est une [JET_coltypLong](./jet-coltyp.md).

**columnidiColumn**

Identificateur de colonne du nombre de colonnes dans l’index. Pour plus d’informations, consultez la section Notes de cette rubrique.

Cette colonne est une [JET_coltypLong](./jet-coltyp.md).


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>cIndexInfoCols<br />15</p> | <p>Spécifie que 15 colonnes sont autorisées.</p> | 
| <p>cColumnInfoCols<br />14</p> | <p>Spécifie que 14 colonnes sont autorisées.</p> | 
| <p>cObjectInfoCols<br />9</p> | <p>Spécifie que 9 colonnes sont autorisées.</p> | 



**columnidcolumnid**

Identificateur de colonne de la colonne indexée. Pour plus d’informations, consultez la section Notes de cette rubrique. Cette colonne est une [JET_coltypLong](./jet-coltyp.md).

**columnidcoltyp**

Identificateur de colonne de la coltyp de la colonne indexée. Pour plus d’informations, consultez la section Notes de cette rubrique. Cette colonne est une [JET_coltypLong](./jet-coltyp.md).

**columnidCountry**

Identificateur de colonne de l’indicatif de pays de la colonne indexée. L’indicatif du pays est déconseillé.

Cette colonne est une [JET_coltypShort](./jet-coltyp.md).

**columnidLangid**

Identificateur de colonne de l’identificateur de langue (LCID) sous lequel l’index a été créé. Pour plus d’informations, consultez [JET_INDEXCREATE](./jet-indexcreate-structure.md).

Cette colonne est une [JET_coltypShort](./jet-coltyp.md).

**columnidCp**

Identificateur de colonne de la page de codes sous laquelle l’index a été créé. Pour plus d’informations, consultez [JET_COLUMNCREATE](./jet-columncreate-structure.md).

Cette colonne est une [JET_coltypShort](./jet-coltyp.md).

**columnidCollate**

Identificateur de colonne de la séquence de classement sous laquelle l’index a été créé. La séquence de classement est déconseillée.

Cette colonne est une [JET_coltypShort](./jet-coltyp.md).

**columnidgrbitColumn**

Identificateur de colonne des *grbits* qui s’appliquent à l’ordre de la colonne dans l’index.

Les données de cette colonne peuvent être classées en tant que JET_bitKeyAscending ou JET_bitKeyDescending. Cette colonne est une [JET_coltypLong](./jet-coltyp.md). Par exemple, un index défini en tant que « -Column1 \\ 0 + Column2 \\ 0 » aura JET_bitKeyDescending pour « Column1 » et JET_bitKeyAscending pour « Column2 ».

Les options suivantes sont valides pour ce membre.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitKeyAscending</p> | <p>Segment d’index dans l’ordre croissant.</p> | 
| <p>JET_bitKeyDescending</p> | <p>Segment d’index dans l’ordre décroissant.</p> | 



**columnidcolumnname**

Identificateur de colonne du nom de la colonne.

Cette colonne est une [JET_coltypText](./jet-coltyp.md).

**columnidLCMapFlags**

Identificateur de colonne des indicateurs utilisés pour créer l’index. Pour plus d’informations, consultez la section **dwMapFlags** de [JET_UNICODEINDEX](./jet-unicodeindex-structure.md).

Cette colonne est une [JET_coltypLong](./jet-coltyp.md).

### <a name="remarks"></a>Remarques

Chaque ligne de la table temporaire correspond à une colonne dans un index particulier.

Par exemple, l’index « + A \\ 0 + B \\ 0 + C \\ 0 + D \\ 0 + E \\ 0 » est supérieur à cinq colonnes et occupe cinq lignes dans la table temporaire. Chacune de ces cinq lignes aura une valeur de 5 dans la colonne identifiée par la colonne ColumnID. Toutefois, chaque ligne a une valeur différente pour la colonne ColumnId, comprise entre 0 et 4.

Le nombre de clés dans un index particulier correspond au nombre de valeurs uniques qu’un appelant peut rechercher et obtenir une correspondance exacte. Le nombre d’entrées est le nombre de lignes correspondant à un index. Si un index a une contrainte d’unicité, le nombre de clés est égal au nombre d’entrées. Par exemple, si une table contient les informations suivantes et qu’un index est créé sur la colonne nommée « Key », il existe trois clés (100, 200 et 500), mais il existe quatre entrées (« This », « is », « an » et « example »).


| <p>Clé</p> | <p>Entrée</p> | 
|------------|--------------|
| <p>100</p> | <p>Voici</p> | 
| <p>100</p> | <p>non</p> | 
| <p>200</p> | <p>pièce</p> | 
| <p>500</p> | <p>tels</p> | 



### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNCREATE](./jet-columncreate-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)
