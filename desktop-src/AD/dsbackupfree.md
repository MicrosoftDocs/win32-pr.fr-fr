---
title: DsBackupFree, fonction (ntdsbcli. h)
description: Libère la mémoire allouée par les fonctions de sauvegarde et de restauration Active Directory Domain Services.
ms.assetid: cde2a530-60e6-440c-9d4e-a90d55846973
ms.tgt_platform: multiple
keywords:
- Active Directory de la fonction DsBackupFree
topic_type:
- apiref
api_name:
- DsBackupFree
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 682bc8d8c4938544c85d22658b1ea175223a6e89d07416aa1fa3717285c67892
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191892"
---
# <a name="dsbackupfree-function"></a>DsBackupFree fonction)

\[Cette fonction peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. à partir de Windows Vista, utilisez [Service VSS (VSS)](../vss/volume-shadow-copy-service-overview.md) à la place.\]

La fonction **DsBackupFree** libère la mémoire allouée par les fonctions de sauvegarde et de restauration Active Directory Domain Services. Les fonctions suivantes allouent de la mémoire qui doit être libérée avec la fonction **DsBackupFree** .

-   [**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md)
-   [**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md)
-   [**DsBackupPrepare**](dsbackupprepare.md)
-   [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md)

## <a name="syntax"></a>Syntaxe


```C++
VOID NTDSBCLI_API DsBackupFree(
  _In_ PVOID pvBuffer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pvBuffer* \[ dans\]
</dt> <dd>

Pointeur vers la mémoire tampon à libérer.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md)
</dt> <dt>

[**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md)
</dt> <dt>

[**DsBackupPrepare**](dsbackupprepare.md)
</dt> <dt>

[**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md)
</dt> <dt>

[Sauvegarde d’un serveur de Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Fonctions de sauvegarde d’annuaire](directory-backup-functions.md)
</dt> </dl>

 

