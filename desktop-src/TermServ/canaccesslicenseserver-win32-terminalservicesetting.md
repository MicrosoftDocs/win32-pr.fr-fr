---
title: Méthode CanAccessLicenseServer de la classe Win32_TerminalServiceSetting
description: CanAccessLicenseServer n’est plus disponible.
ms.assetid: b09fa901-8ae1-431e-8d97-27ee84a84779
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode CanAccessLicenseServer
- Services Bureau à distance de la méthode CanAccessLicenseServer, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode CanAccessLicenseServer
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.CanAccessLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ffa5bd0e108c0ccceed6890adedea7901834804
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103173"
---
# <a name="canaccesslicenseserver-method-of-the-win32_terminalservicesetting-class"></a>Méthode CanAccessLicenseServer de la \_ classe Win32 TerminalServiceSetting

\[**CanAccessLicenseServer** ne peut plus être utilisé à partir de Windows Server 2008 R2.\]

* * Windows Server 2008 : * *

Détermine si le Bureau à distance serveur hôte de session Bureau à distance (hôte de session Bureau à distance) est autorisé à demander Services Bureau à distance des licences d’accès client (CAL RDS) à partir d’un serveur de licences Bureau à distance en fonction des éléments suivants :

-   Paramètre de stratégie de groupe « Groupe de sécurité du serveur de licences » sur le serveur de licences Bureau à distance.
-   Appartenance au groupe local ordinateurs Terminal Server sur le serveur de licences.

## <a name="syntax"></a>Syntaxe


```mof
uint32 CanAccessLicenseServer(
  [in]  string ServerName,
  [out] uint32 AccessAllowed
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom du serveur* \[ dans\]
</dt> <dd>

Nom du serveur de licences Bureau à distance.

</dd> <dt>

*AccessAllowed* \[ à\]
</dt> <dd>

Si le serveur hôte de session Bureau à distance est autorisé à demander des licences d’accès client aux services Bureau à distance à partir du serveur de licences.

<dt>

0
</dt> <dd>

La demande est autorisée.

</dd> <dt>

1
</dt> <dd>

La demande n’est pas autorisée.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur **\_ OK** si le serveur hôte de session Bureau à distance a accès au serveur de licences. Retourne **la \_ valeur S false** si le serveur hôte de session Bureau à distance n’a pas accès au serveur de licences.

## <a name="remarks"></a>Notes

Le paramètre de stratégie « Groupe de sécurité du serveur de licences » vous permet de spécifier les serveurs hôtes de session Bureau à distance qui sont autorisés à contacter le serveur de licences pour obtenir des licences d’accès client aux services Bureau à distance. Si le paramètre de stratégie est activé sur le serveur de licences, le serveur de licences répond uniquement aux demandes de licences d’accès client aux services Bureau à distance des serveurs hôtes de session Bureau à distance dont les comptes d’ordinateur sont membres du groupe local ordinateurs Terminal Server sur le serveur de licences.

Pour se connecter à \\ l' \\ \\ espace de noms licences TS cimv2 racine, le niveau d’authentification doit inclure la confidentialité du paquet. Pour les appels C/C++, il s’agit d’un niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC c**. Pour les Visual Basic et les appels de script, il s’agit d’un niveau d’authentification **WbemAuthenticationLevelPktPrivacy** ou « PktPrivacy », avec une valeur de 6. L’exemple de Visual Basic Scripting Edition suivant (VBScript) montre comment se connecter à un ordinateur distant avec la confidentialité du paquet.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



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

 

