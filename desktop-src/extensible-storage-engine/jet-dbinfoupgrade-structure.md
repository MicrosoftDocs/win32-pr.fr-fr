---
description: 'En savoir plus sur : structure JET_DBINFOUPGRADE'
title: Structure JET_DBINFOUPGRADE
TOCTitle: JET_DBINFOUPGRADE Structure
ms:assetid: dd8a881a-33b5-4314-8cfb-b1d75ad37b21
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294114(v=EXCHG.10)
ms:contentKeyID: 32765728
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
ms.openlocfilehash: f8a62245ee4b09ec3e8764e6d4e51841fa057c789bdc2fb4a142380d62e8d598
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119112178"
---
# <a name="jet_dbinfoupgrade-structure"></a>Structure JET_DBINFOUPGRADE


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_dbinfoupgrade-structure"></a>Structure JET_DBINFOUPGRADE

La structure **JET_DBINFOUPGRADE** contient des informations sur l’état de mise à niveau de la base de données. Cette valeur est récupérée uniquement si **JET_DBINFOUPGRADE** a été passé à [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) ou [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md). Cette structure n’est pas requise pour les versions de système d’exploitation actuelles du moteur de base de données.

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cbFilesizeLow;
      unsigned long cbFilesizeHigh;
      unsigned long cbFreeSpaceRequiredLow;
      unsigned long  cbFreeSpaceRequiredHigh;
      unsigned long csecToUpgrade;
      union {
        unsigned long ulFlags;
        struct {
          unsigned long fUpgradable  :1;
          unsigned long fAlreadyUpgraded  :1;
        };
      };
    } JET_DBINFOUPGRADE;
```

### <a name="members"></a>Membres

**cbStruct**

Défini sur la taille de la structure **JET_DBINFOUPGRADE** , en octets.

**cbFilesizeLow**

**Valeur DWORD** basse qui reflète la taille de fichier actuelle pour la base de données.

**cbFilesizeHigh**

**Valeur DWORD** haute qui reflète la taille de fichier actuelle pour la base de données.

**cbFreeSpaceRequiredLow**

**Valeur DWORD** faible de l’espace disque disponible estimé nécessaire pour une mise à niveau sur place.

**cbFreeSpaceRequiredHigh**

**Valeur DWORD** élevée de l’espace disque disponible estimé requis pour une mise à niveau sur place.

**csecToUpgrade**

Durée estimée nécessaire à la mise à niveau, en secondes.

**ulFlags**

Un champ de bits constitué de zéro, un ou plusieurs des indicateurs suivants : **fUpgradable**, **fAlreadyUpgraded**.

**fUpgradable**

La base de données peut être mise à niveau.

**fAlreadyUpgraded**

La base de données est mise à niveau vers le format de base de données actuel.

### <a name="remarks"></a>Remarques

Une structure **JET_DBINFOUPGRADE** est remplie par un appel à [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) ou [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md). Si la fonction échoue, le contenu de la structure n’est pas défini.

### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p></td>
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
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetObjectInfo](./jetgetobjectinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)
