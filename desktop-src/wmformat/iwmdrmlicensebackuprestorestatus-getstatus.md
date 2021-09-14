---
title: IWMDRMLicenseBackupRestoreStatus GetStatus, méthode (wmdrmsdk. h)
description: La méthode GetStatus récupère des informations d’État détaillées sur une opération de sauvegarde ou de restauration de licence.
ms.assetid: 1a695baf-0971-4dbf-90fa-1b10178a3348
keywords:
- Méthode GetStatus Windows Media format
- Méthode GetStatus Windows Media format, interface IWMDRMLicenseBackupRestoreStatus
- Interface IWMDRMLicenseBackupRestoreStatus Windows Media format, GetStatus, méthode
topic_type:
- apiref
api_name:
- IWMDRMLicenseBackupRestoreStatus.GetStatus
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3373e71bcae9dc1054e97e8b758ac72389b9a712
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404465"
---
# <a name="iwmdrmlicensebackuprestorestatusgetstatus-method"></a>IWMDRMLicenseBackupRestoreStatus :: GetStatus, méthode

La méthode **GetStatus** récupère des informations d’État détaillées sur une opération de sauvegarde ou de restauration de licence.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetStatus(
  [out] WM_BACKUP_RESTORE_STATUS *pStatus
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pStatus* \[ à\]
</dt> <dd>

Pointeur vers une structure d' [**\_ État de \_ restauration \_ de sauvegarde WM**](wm-backup-restore-status.md) qui reçoit les informations d’État.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

Aucun.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md)
</dt> </dl>

 

 





