---
title: Structure EDB_RSTMAP (ntdsbcli. h)
description: Utilisé avec la fonction DsRestoreRegister pour mapper une base de données sauvegardée à une nouvelle base de données.
ms.assetid: b2c5d30a-3617-4807-82e8-57f7179b817c
ms.tgt_platform: multiple
keywords:
- EDB_RSTMAP structure Active Directory
- Pointeur de structure PEDB_RSTMAP Active Directory
topic_type:
- apiref
api_name:
- EDB_RSTMAP
- EDB_RSTMAPA
- EDB_RSTMAPW
api_location:
- Ntdsbcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be2c960ab7ebc687508131deac6cd8e7b99bbe81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032977"
---
# <a name="edb_rstmap-structure"></a>\_Structure RSTMAP edb

La **structure \_ RSTMAP edb** est utilisée avec la fonction [**DsRestoreRegister**](dsrestoreregister.md) pour mapper une base de données sauvegardée à une nouvelle base de données.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  LPTSTR szDatabaseName;
  LPTSTR szNewDatabaseName;
} EDB_RSTMAP, *PEDB_RSTMAP;
```



## <a name="members"></a>Membres

<dl> <dt>

**szDatabaseName**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui contient le nom de la base de données lors de sa sauvegarde.

</dd> <dt>

**szNewDatabaseName**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui contient le nouveau nom de la base de données, y compris son nouvel emplacement, le cas échéant.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                        |
| En-tête<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **Edb \_ RSTMAPW** (Unicode) et **edb \_ RSTMAPA** (ANSI)<br/>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DsRestoreRegister**](dsrestoreregister.md)
</dt> <dt>

[Structures de sauvegarde d’annuaire](directory-backup-structures.md)
</dt> </dl>

 

 





