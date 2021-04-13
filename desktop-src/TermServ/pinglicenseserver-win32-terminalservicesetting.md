---
title: Méthode PingLicenseServer de la classe Win32_TerminalServiceSetting
description: PingLicenseServer n’est plus disponible.
ms.assetid: d2a9f273-1ff9-4391-889b-a3b9c9f95c3b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode PingLicenseServer
- Services Bureau à distance de la méthode PingLicenseServer, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode PingLicenseServer
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.PingLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fe7277b3130c88c1aec7716c1a3bf560b81db64
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384575"
---
# <a name="pinglicenseserver-method-of-the-win32_terminalservicesetting-class"></a>Méthode PingLicenseServer de la \_ classe Win32 TerminalServiceSetting

\[**PingLicenseServer** ne peut plus être utilisé à partir de Windows Server 2008 R2.\]

**Windows Server 2008 :** Exécute une commande ping sur le serveur de licences pour déterminer s’il s’agit d’un serveur de licences valide.

## <a name="syntax"></a>Syntaxe


```mof
uint32 PingLicenseServer(
  [in] string ServerName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom du serveur* \[ dans\]
</dt> <dd>

Nom du serveur de licences.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

<dl> <dt>

**\_OK**
</dt> <dd>

Le serveur est un serveur de licences valide.

</dd> <dt>

**S \_ false**
</dt> <dd>

Le serveur de licences n’est pas valide.

</dd> </dl>

## <a name="remarks"></a>Notes

Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Fin de la prise en charge des clients<br/>    | Aucun pris en charge<br/>                                                               |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TerminalServiceSetting Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 

