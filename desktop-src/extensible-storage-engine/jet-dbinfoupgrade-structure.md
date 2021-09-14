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
ms.openlocfilehash: 0e2e6d6e812b5f56c89eba2e4b19d2730d589548
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126917367"
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

### <a name="remarks"></a>Notes

Une structure **JET_DBINFOUPGRADE** est remplie par un appel à [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) ou [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md). Si la fonction échoue, le contenu de la structure n’est pas défini.

### <a name="requirements"></a>Spécifications


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetObjectInfo](./jetgetobjectinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)
