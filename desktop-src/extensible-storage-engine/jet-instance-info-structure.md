---
description: 'En savoir plus sur : structure JET_INSTANCE_INFO'
title: Structure JET_INSTANCE_INFO
TOCTitle: JET_INSTANCE_INFO Structure
ms:assetid: 8cdd2e48-f1bb-465b-aefc-ffe441bf88a1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269331(v=EXCHG.10)
ms:contentKeyID: 32765621
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
ms.openlocfilehash: fd07d11a8b30e75f30bc5bfcaa3aca665baf1209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868381"
---
# <a name="jet_instance_info-structure"></a>Structure JET_INSTANCE_INFO


_**S’applique à :** Windows | Serveur Windows_

## <a name="jet_instance_info-structure"></a>Structure JET_INSTANCE_INFO

La structure **JET_INSTANCE_INFO** reçoit des informations sur l’exécution d’instances de base de données lorsqu’elle est utilisée avec les fonctions [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) et [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) .

```cpp
    typedef struct _JET_INSTANCE_INFO {
      JET_INSTANCE hInstanceId;
      tchar* szInstanceName;
      JET_API_PTR cDatabases;
      tchar** szDatabaseFileName;
      tchar** szDatabaseDisplayName;
      tchar** szDatabaseSLVFileName;
    } JET_INSTANCE_INFO;
```

### <a name="members"></a>Membres

**hInstanceId**

[JET_INSTANCE](./jet-instance.md) de l’instance donnée.

**szInstanceName**

Nom de l'instance de base de données. Cette valeur peut être **null** si l’instance n’a pas de nom.

**cDatabases**

Nombre de bases de données attachées à l’instance de base de données. **cDatabases** contient également la taille des tableaux de chaînes retournées dans **szDatabaseFileName**, **szDatabaseDisplayName** et **szDatabaseSLVFileName**.

**szDatabaseFileName**

Tableau de chaînes, chacune contenant le nom de fichier d’une base de données attachée à l’instance de base de données. Le tableau contient des éléments **cDatabases** .

**szDatabaseDisplayName**

Tableau de chaînes, chacune contenant le nom complet d’une base de données. Actuellement, la chaîne peut être NULL. Le tableau contient des éléments **cDatabases** .

**szDatabaseSLVFileName**

Tableau de chaînes contenant le nom de fichier du fichier SLV attaché à l’instance de base de données. Le tableau contient des éléments **cDatabases** . Comme les fichiers SLV ne sont pas pris en charge, ce champ doit être ignoré.

### <a name="remarks"></a>Notes

Plusieurs bases de données peuvent être attachées à chaque instance de base de données.

Pour une structure de **JET_INSTANCE_INFO** donnée, le tableau de chaînes retourné pour les bases de données est dans le même ordre. Par exemple, « szDatabaseDisplayName \[ i \] » et « szDatabaseFileName \[ i \] » font tous deux référence à la même base de données.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implémenté comme <strong>JET_INSTANCE_INFO_W</strong> (Unicode) et <strong>JET_INSTANCE_INFO _a</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Voir aussi

[JET_API_PTR](./jet-api-ptr.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetGetInstanceInfo](./jetgetinstanceinfo-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)
