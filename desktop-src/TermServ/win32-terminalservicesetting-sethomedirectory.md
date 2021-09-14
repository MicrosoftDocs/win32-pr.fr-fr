---
title: Méthode SetHomeDirectory de la classe Win32_TerminalServiceSetting
description: Définit la propriété TerminalServicesHomeDirectory de la classe.
ms.assetid: 8173cd5b-965e-41bc-97cf-70d8729b8cea
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetHomeDirectory
- Services Bureau à distance de la méthode SetHomeDirectory, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode SetHomeDirectory
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetHomeDirectory
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1be732cae76b0681afd77693a07f673ef37c4a12
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919603"
---
# <a name="sethomedirectory-method-of-the-win32_terminalservicesetting-class"></a>Méthode SetHomeDirectory de la \_ classe Win32 TerminalServiceSetting

La méthode **SetHomeDirectory** définit la propriété **TerminalServicesHomeDirectory** de la classe.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetHomeDirectory(
  [in] string HomeDirectory
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HomeDirectory* \[ dans\]
</dt> <dd>

Nouvelle valeur de la propriété **TerminalServicesHomeDirectory** , qui spécifie le répertoire racine de l’ordinateur.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une réussite en cas de réussite ; Sinon, retourne un code d’erreur WMI. Pour obtenir la liste des codes d’erreur WMI, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Notes

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TerminalServiceSetting Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 

