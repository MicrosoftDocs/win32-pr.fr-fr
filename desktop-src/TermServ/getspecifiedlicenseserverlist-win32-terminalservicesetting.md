---
title: Méthode GetSpecifiedLicenseServerList de la classe Win32_TerminalServiceSetting
description: Récupère la liste des serveurs de licences spécifiés.
ms.assetid: 800be0ce-1002-48e1-be4e-88db22590f12
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetSpecifiedLicenseServerList
- Services Bureau à distance de la méthode GetSpecifiedLicenseServerList, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode GetSpecifiedLicenseServerList
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 359d348dc759534d1f3ca070f443f4207aa8ddba0c73ab989d0fa8c0ab5397fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033749"
---
# <a name="getspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a>Méthode GetSpecifiedLicenseServerList de la \_ classe Win32 TerminalServiceSetting

Récupère la liste des serveurs de licences spécifiés.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetSpecifiedLicenseServerList(
  [out] string SpecifiedLSList[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SpecifiedLSList* \[ à\]
</dt> <dd>

Tableau de chaînes qui reçoit la liste des serveurs de licences. S’il n’y a aucun serveur de licences, ce groupe est vide.

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

[**RemoveLSFromSpecifiedLicenseServerList**](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[**SetSpecifiedLicenseServerList**](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





