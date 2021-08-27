---
title: Méthode GetGracePeriodDays de la classe Win32_TerminalServiceSetting
description: Récupère le nombre de jours restants dans la période de grâce des licences Services Bureau à distance pour un serveur hôte de session Bureau à distance (hôte de session Bureau à distance). Une valeur zéro indique que la période de grâce est terminée.
ms.assetid: d84d7815-ee09-43d9-a370-993d23f14898
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetGracePeriodDays
- Services Bureau à distance de la méthode GetGracePeriodDays, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode GetGracePeriodDays
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetGracePeriodDays
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbfe1a99fb0b4f12db19f018d8acb3aaee6ab15a3560cd9140c3a05f36986585
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010119"
---
# <a name="getgraceperioddays-method-of-the-win32_terminalservicesetting-class"></a>Méthode GetGracePeriodDays de la \_ classe Win32 TerminalServiceSetting

Récupère le nombre de jours restants dans la période de grâce des licences Services Bureau à distance pour un serveur hôte de session Bureau à distance (hôte de session Bureau à distance). Une valeur zéro indique que la période de grâce est terminée.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetGracePeriodDays(
  [out] uint32 DaysLeft
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DaysLeft* \[ à\]
</dt> <dd>

Nombre de jours restants dans la période de grâce.

</dd> </dl>

## <a name="remarks"></a>Remarques

Pour se connecter à \\ l' \\ \\ espace de noms licences TS cimv2 racine, le niveau d’authentification doit inclure la confidentialité du paquet. Pour les appels C/C++, il s’agit d’un niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC c**. pour les Visual Basic et les appels de script, il s’agit d’un niveau d’authentification **WbemAuthenticationLevelPktPrivacy** ou « pktPrivacy », avec une valeur de 6. l’exemple VBScript (Visual Basic scripting Edition) suivant montre comment se connecter à un ordinateur distant avec la confidentialité du paquet.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Configuration requise



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

 

