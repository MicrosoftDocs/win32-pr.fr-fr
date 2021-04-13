---
title: Méthode RdvUndoVMPermissions de la classe Win32_RdvhManagement
description: Restaure les autorisations définies par RdvSetupVMPermissions sur la machine virtuelle spécifiée.
ms.assetid: 3331430e-7427-42f7-ab09-27fece8dc3ca
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RdvUndoVMPermissions
- Services Bureau à distance de la méthode RdvUndoVMPermissions, classe Win32_RdvhManagement
- Win32_RdvhManagement de la classe Services Bureau à distance, méthode RdvUndoVMPermissions
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvUndoVMPermissions
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1dc8892435522dcd2c7457fe4b74a0d9671740
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466742"
---
# <a name="rdvundovmpermissions-method-of-the-win32_rdvhmanagement-class"></a>Méthode RdvUndoVMPermissions de la \_ classe Win32 RdvhManagement

Restaure les autorisations définies par [**RdvSetupVMPermissions**](rdvsetupvmpermissions-win32-rdvhmanagement.md) sur la machine virtuelle spécifiée.

## <a name="syntax"></a>Syntaxe


```mof
uint32 RdvUndoVMPermissions(
  [in] string VmName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*VmName* \[ dans\]
</dt> <dd>

Nom de l’ordinateur virtuel sur lequel annuler les autorisations.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                             |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_RdvhManagement Win32**](win32-rdvhmanagement.md)
</dt> </dl>

 

 





