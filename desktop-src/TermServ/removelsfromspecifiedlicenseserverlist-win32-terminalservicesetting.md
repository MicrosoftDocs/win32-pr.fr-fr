---
title: Méthode RemoveLSFromSpecifiedLicenseServerList de la classe Win32_TerminalServiceSetting
description: Supprime le serveur de licences donné de la liste des serveurs de licences spécifiés.
ms.assetid: c25eebf9-3a21-41a0-bb7d-c3f909cd8087
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RemoveLSFromSpecifiedLicenseServerList
- Services Bureau à distance de la méthode RemoveLSFromSpecifiedLicenseServerList, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode RemoveLSFromSpecifiedLicenseServerList
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.RemoveLSFromSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 901c2676748e819290855df2de51e5d7936dc793
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843585"
---
# <a name="removelsfromspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a>Méthode RemoveLSFromSpecifiedLicenseServerList de la \_ classe Win32 TerminalServiceSetting

Supprime le serveur de licences donné de la liste des serveurs de licences spécifiés.

## <a name="syntax"></a>Syntaxe


```mof
uint32 RemoveLSFromSpecifiedLicenseServerList(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*LicenseServerName* \[ dans\]
</dt> <dd>

Nom du serveur de licences à supprimer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

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
</dt> <dt>

[**AddLSToSpecifiedLicenseServerList**](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[**EmptySpecifiedLicenseServerList**](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[**GetSpecifiedLicenseServerList**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[**SetSpecifiedLicenseServerList**](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





