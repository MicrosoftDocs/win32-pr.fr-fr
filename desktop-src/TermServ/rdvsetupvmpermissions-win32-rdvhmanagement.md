---
title: Méthode RdvSetupVMPermissions de la classe Win32_RdvhManagement
description: Définit les autorisations sur un ordinateur virtuel pour l’utilisateur actuel.
ms.assetid: 6ac45983-d468-4a3b-875f-48717ba23ed0
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RdvSetupVMPermissions
- Services Bureau à distance de la méthode RdvSetupVMPermissions, classe Win32_RdvhManagement
- Win32_RdvhManagement de la classe Services Bureau à distance, méthode RdvSetupVMPermissions
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvSetupVMPermissions
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd8028a33bc772f9dd37f25a1dc22074baf771b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465306"
---
# <a name="rdvsetupvmpermissions-method-of-the-win32_rdvhmanagement-class"></a>Méthode RdvSetupVMPermissions de la \_ classe Win32 RdvhManagement

Définit les autorisations sur un ordinateur virtuel pour l’utilisateur actuel.

## <a name="syntax"></a>Syntaxe


```mof
uint32 RdvSetupVMPermissions(
  [in] string VmName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*VmName* \[ dans\]
</dt> <dd>

Nom de l’ordinateur virtuel sur lequel définir des autorisations.

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

 

 





