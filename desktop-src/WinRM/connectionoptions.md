---
title: Objet ConnectionOptions (WSManDisp. h)
description: L’objet ConnectionOptions est passé à la méthode CreateSession pour fournir le nom d’utilisateur et le mot de passe associés au compte local sur l’ordinateur distant.
ms.assetid: 7a87a5f7-78ed-452c-9b9f-ad48811a3339
ms.tgt_platform: multiple
keywords:
- objet ConnectionOptions Windows Remote Management
- Windows Remote Management d’objets ConnectionOptions, description
topic_type:
- apiref
api_name:
- ConnectionOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8665dc3a5be91fddb4332be3512ec9eec5c483495a21b95b641ec26e4e9e111
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119734089"
---
# <a name="connectionoptions-object"></a>Objet ConnectionOptions

L’objet **ConnectionOptions** est passé à la méthode [**CreateSession**](wsman-createsession.md) pour fournir le nom d’utilisateur et le mot de passe associés au compte local sur l’ordinateur distant. Si aucun paramètre n’est fourni, les informations d’identification du compte qui exécute le script sont définies sur les valeurs par défaut.

## <a name="members"></a>Membres

L’objet **ConnectionOptions** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **ConnectionOptions** a ces propriétés.



| Propriété                                                  | Type d’accès           | Description                                                                                 |
|:----------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------|
| [**Mot de passe**](connectionoptions-password.md)<br/> | Écriture seule<br/> | Définit le mot de passe d’un compte local ou de domaine sur l’ordinateur distant.<br/>           |
| [**Nom d’utilisateur**](connectionoptions-username.md)<br/> | Lecture/écriture<br/> | Définit et obtient le nom d’utilisateur d’un compte local ou de domaine sur l’ordinateur distant.<br/> |



 

## <a name="remarks"></a>Remarques

L’objet **ConnectionOptions** correspond à l’interface [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions) .

si une application cliente Windows Remote Management s’exécute avec l’emprunt d’identité, un échec se produit si vous définissez la propriété [**de mot de passe**](connectionoptions-password.md) . Une application cliente est un script ou tout autre programme qui envoie une demande à WinRM sur l’ordinateur local ou distant. L’application cliente peut s’exécuter sous emprunt d’identité, car elle a appelé une fonction telle que [**ImpersonateClient**](/previous-versions/windows/desktop/legacy/aa375494(v=vs.85)). Une page de Active Server (ASP) ou un service ne peut pas demander un nom d’utilisateur et un mot de passe si le processus ASP s’exécute sous un compte qui emprunte l’identité d’un client.

L’indicateur **WSManFlagCredUserNamePassword** doit être défini sur l’appel de [**WSman. CreateSession**](wsman-createsession.md) lors de l’utilisation du [**nom d’utilisateur**](connectionoptions-username.md) et du [**mot de passe**](connectionoptions-password.md) pour l’authentification.

## <a name="examples"></a>Exemples

L’exemple de code VBScript suivant montre comment créer un objet **ConnectionOptions** , définir les propriétés du compte sur l’ordinateur distant et l’utiliser pour créer un objet de [**session**](session.md) .


```VB
Set objWsman = CreateObject( "Wsman.Automation" )
'Create ConnectionOptions object.
Set objConnectionOptions = objWsman.CreateConnectionOptions
objConnectionOptions.UserName = "johns "
objConnectionOptions.Password = "Dtf#4542?98"
iFlags = objWsman.SessionFlagUseBasic Or _
  objWsman.SessionFlagCredUserNamePassword
Set objSession = objWsman.CreateSession _
  ("https://172.30.168.2", iFlags, objConnectionOptions)
strResource = objSession.Get("winrm/config")
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Authentification des connexions à distance](authentication-for-remote-connections.md)
</dt> <dt>

[API de script WinRM](winrm-scripting-api.md)
</dt> <dt>

[à propos de Windows Remote Management](about-windows-remote-management.md)
</dt> <dt>

[utilisation de Windows Remote Management](using-windows-remote-management.md)
</dt> <dt>

[scripts dans Windows Remote Management](scripting-in-windows-remote-management.md)
</dt> <dt>

[Obtention de données à partir de l’ordinateur local](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[Obtention de données à partir d’un ordinateur distant](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

