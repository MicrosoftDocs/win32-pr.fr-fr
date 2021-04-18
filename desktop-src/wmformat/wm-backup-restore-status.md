---
title: Structure WM_BACKUP_RESTORE_STATUS (wmdrmsdk. h)
description: La \_ structure d’état de la restauration de la sauvegarde WM contient des \_ \_ informations sur une opération de sauvegarde ou de restauration de licence en attente.
ms.assetid: 74e94bc6-376b-4848-a9f9-11c9cb4005f2
keywords:
- Structure WM_BACKUP_RESTORE_STATUS format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- WM_BACKUP_RESTORE_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476cd4ddab42ec9f8f44ff51b492bd3913824cf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526812"
---
# <a name="wm_backup_restore_status-structure"></a>\_Structure d' \_ État de restauration de la sauvegarde WM \_

La structure d’état de la restauration de la **\_ sauvegarde \_ \_ WM** contient des informations sur une opération de sauvegarde ou de restauration de licence en attente.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct WM_BACKUP_RESTORE_STATUS {
  MSDRM_STATUS eStatus;
  BSTR         bstrError;
} ;
```



## <a name="members"></a>Membres

<dl> <dt>

**eStatus**
</dt> <dd>

Membre de l’énumération d' [**\_ État msdrm**](msdrm-status.md) spécifiant l’État.

</dd> <dt>

**bstrError**
</dt> <dd>

Chaîne contenant l’erreur.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette structure est reçue lorsque vous appelez la méthode [**IWMDRMLicenseBackupRestoreStatus :: GetStatus**](iwmdrmlicensebackuprestorestatus-getstatus.md) . Elle contient l’état de l’opération de sauvegarde ou de restauration en attente au moment de l’appel.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures**](drm-structures.md)
</dt> </dl>

 

 





