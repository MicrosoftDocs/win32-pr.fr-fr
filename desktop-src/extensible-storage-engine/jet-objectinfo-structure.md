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
ms.openlocfilehash: cd1f8a876153b5b457cfb153cbf35fa2d388b0f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034911"
---
# <a name="jet_objectinfo-structure"></a>Structure JET_OBJECTINFO


_**S’applique à :** Windows | Serveur Windows_

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
<td><p>JET_bitTableInfoBookmark</p></td>
<td><p>La table peut avoir des signets.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableInfoRollback</p></td>
<td><p>La table peut être restaurée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTableInfoUpdatable</p></td>
<td><p>La table peut être mise à jour.</p></td>
</tr>
</tbody>
</table>


**flags**

Champ de bits qui contient zéro, un ou plusieurs des indicateurs suivants.

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
<td><p>JET_bitObjectSystem</p></td>
<td><p>La table est une table système et est réservée à un usage interne.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitObjectTableDerived</p></td>
<td><p>Table héritée DDL d’une table de modèle.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitObjectTableFixedDDL</p></td>
<td><p>Le DDL pour la table ne peut pas être modifié.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitObjectTableNoFixedVarColumnsInDerivedTables</p></td>
<td><p>Utilisé conjointement avec JET_bitObjectTableTemplate pour interdire les colonnes fixes ou variables dans les tables dérivées (afin que les colonnes fixes ou variables puissent être ajoutées ultérieurement au modèle).</p>
<p><strong>Windows XP :  </strong> Cette valeur est introduite dans Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitObjectTableTemplate</p></td>
<td><p>La table est une table de modèle.</p></td>
</tr>
</tbody>
</table>


**cRecord**

Nombre d’enregistrements dans la table.

Cette valeur est récupérée uniquement si **JET_OBJECTINFO** a été passé à [JetGetObjectInfo](./jetgetobjectinfo-function.md).

**cPage**

Nombre de pages utilisées par la table.

Cette valeur est récupérée uniquement si **JET_OBJECTINFO** a été passé à [JetGetObjectInfo](./jetgetobjectinfo-function.md).

### <a name="remarks"></a>Notes

Une structure **JET_OBJECTINFOe** est remplie par un appel à [JetGetObjectInfo](./jetgetobjectinfo-function.md) ou [JetGetTableInfo](./jetgettableinfo-function.md). Si l’appel d’API échoue, le contenu de la structure n’est pas défini.

Le cas échéant, les statistiques de table incluent le nombre d’enregistrements et le nombre de pages qui se trouvent dans l’index cluster (autrement dit, l’index contenant les données de l’enregistrement). Les statistiques d’index sont accessibles séparément par nom, à l’aide de [JetGetIndexInfo](./jetgetindexinfo-function.md) ou [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).

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

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_OBJTYP](./jet-objtyp.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetObjectInfo](./jetgetobjectinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)
