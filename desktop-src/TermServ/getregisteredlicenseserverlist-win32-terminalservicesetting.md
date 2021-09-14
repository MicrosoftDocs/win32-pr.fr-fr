---
title: Méthode GetRegisteredLicenseServerList de la classe Win32_TerminalServiceSetting
description: Obtient la liste des serveurs de licences inscrits.
ms.assetid: 32e06b4b-652f-4977-be1f-6d52983d2605
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetRegisteredLicenseServerList
- Services Bureau à distance de la méthode GetRegisteredLicenseServerList, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode GetRegisteredLicenseServerList
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetRegisteredLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5336910956a0d281fbfc8fbc65e1d3b8d5018cb2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008631"
---
# <a name="getregisteredlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a>Méthode GetRegisteredLicenseServerList de la \_ classe Win32 TerminalServiceSetting

Obtient la liste des serveurs de licences inscrits.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetRegisteredLicenseServerList(
  [out] string RegisteredLSList[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*RegisteredLSList* \[ à\]
</dt> <dd>

Tableau de chaînes qui reçoit la liste des serveurs de licences inscrits. Si aucun serveur de licences n’est inscrit, ce groupe est vide.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                       |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TerminalServiceSetting Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 

 





