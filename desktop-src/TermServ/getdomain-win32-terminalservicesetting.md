---
title: Méthode GetDomain de la classe Win32_TerminalServiceSetting
description: Récupère le nom du domaine auquel le serveur hôte de session Bureau à distance (hôte de session Bureau à distance) est membre.
ms.assetid: 11d58068-56df-4040-b7ba-afdd55bd417a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetDomain
- Services Bureau à distance de la méthode GetDomain, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode GetDomain
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetDomain
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 613c3758d605727b50e8fb1bfbeebd1e475b00eb6673196c22be068bafd86499
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001557"
---
# <a name="getdomain-method-of-the-win32_terminalservicesetting-class"></a>Méthode GetDomain de la \_ classe Win32 TerminalServiceSetting

Récupère le nom du domaine auquel le serveur hôte de session Bureau à distance (hôte de session Bureau à distance) est membre.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetDomain(
  [out] string Domain
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Domaine* \[ à\]
</dt> <dd>

Nom de domaine du serveur hôte de session Bureau à distance.

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

 

