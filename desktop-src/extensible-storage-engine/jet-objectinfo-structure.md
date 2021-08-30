---
description: 'En savoir plus sur : structure JET_OBJECTINFO'
title: Structure JET_OBJECTINFO
TOCTitle: JET_OBJECTINFO Structure
ms:assetid: 9d348ab3-d453-4316-9233-681f165e8ef1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269353(v=EXCHG.10)
ms:contentKeyID: 32765640
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
ms.openlocfilehash: a24f27982285622e3b5f0893768757d27041f1c0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465106"
---
# <a name="jet_objectinfo-structure"></a>Structure JET_OBJECTINFO


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_objectinfo-structure"></a>Structure JET_OBJECTINFO

La structure **JET_OBJECTINFO** contient des informations sur un objet. Les tables sont les seuls types d’objets actuellement pris en charge.

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_OBJTYP objtyp;
      JET_DATESERIAL dtCreate;
      JET_DATESERIAL dtUpdate;
      JET_GRBIT grbit;
      unsigned long flags;
      unsigned long cRecord;
      unsigned long cPage;
    } JET_OBJECTINFO;
```

### <a name="members"></a>Membres

**cbStruct**

Taille, en octets, de la structure **JET_OBJECTINFO** .

**objtyp**

Contient le [JET_OBJTYP](./jet-objtyp.md) de la structure. Actuellement, seules les tables sont retournées (autrement dit, JET_objtypTable).

**dtCreate**

Obsolète. Ne pas utiliser.

**dtUpdate**

Obsolète. Ne pas utiliser.

**grbit**

Groupe de bits qui contiennent les options disponibles pour cet appel, qui incluent zéro ou plusieurs des éléments suivants.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitTableInfoBookmark</p> | <p>La table peut avoir des signets.</p> | 
| <p>JET_bitTableInfoRollback</p> | <p>La table peut être restaurée.</p> | 
| <p>JET_bitTableInfoUpdatable</p> | <p>La table peut être mise à jour.</p> | 



**flags**

Champ de bits qui contient zéro, un ou plusieurs des indicateurs suivants.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitObjectSystem</p> | <p>La table est une table système et est réservée à un usage interne.</p> | 
| <p>JET_bitObjectTableDerived</p> | <p>Table héritée DDL d’une table de modèle.</p> | 
| <p>JET_bitObjectTableFixedDDL</p> | <p>Le DDL pour la table ne peut pas être modifié.</p> | 
| <p>JET_bitObjectTableNoFixedVarColumnsInDerivedTables</p> | <p>Utilisé conjointement avec JET_bitObjectTableTemplate pour interdire les colonnes fixes ou variables dans les tables dérivées (afin que les colonnes fixes ou variables puissent être ajoutées ultérieurement au modèle).</p><p><strong>Windows XP :</strong> cette valeur est introduite dans Windows XP.</p> | 
| <p>JET_bitObjectTableTemplate</p> | <p>La table est une table de modèle.</p> | 



**cRecord**

Nombre d’enregistrements dans la table.

Cette valeur est récupérée uniquement si **JET_OBJECTINFO** a été passé à [JetGetObjectInfo](./jetgetobjectinfo-function.md).

**cPage**

Nombre de pages utilisées par la table.

Cette valeur est récupérée uniquement si **JET_OBJECTINFO** a été passé à [JetGetObjectInfo](./jetgetobjectinfo-function.md).

### <a name="remarks"></a>Remarques

Une structure **JET_OBJECTINFOe** est remplie par un appel à [JetGetObjectInfo](./jetgetobjectinfo-function.md) ou [JetGetTableInfo](./jetgettableinfo-function.md). Si l’appel d’API échoue, le contenu de la structure n’est pas défini.

Le cas échéant, les statistiques de table incluent le nombre d’enregistrements et le nombre de pages qui se trouvent dans l’index cluster (autrement dit, l’index contenant les données de l’enregistrement). Les statistiques d’index sont accessibles séparément par nom, à l’aide de [JetGetIndexInfo](./jetgetindexinfo-function.md) ou [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).

### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_OBJTYP](./jet-objtyp.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetObjectInfo](./jetgetobjectinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)
