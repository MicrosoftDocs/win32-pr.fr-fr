---
title: Propriété ConnectionOptions. UserName (WSManDisp. h)
description: Définit et obtient le nom d’utilisateur d’un compte local ou d’un compte de domaine sur l’ordinateur distant. Cette propriété détermine le nom d’utilisateur pour l’authentification.
ms.assetid: e8f70143-f002-4b39-97a3-006b9713262d
ms.tgt_platform: multiple
keywords:
- Propriété UserName Windows Remote Management
- Propriété UserName Windows Remote Management, objet ConnectionOptions
- Objet ConnectionOptions Windows Remote Management, propriété UserName
topic_type:
- apiref
api_name:
- ConnectionOptions.UserName
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4d6c751dbe579372b863566412e740c2a646a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104584"
---
# <a name="connectionoptionsusername-property"></a>ConnectionOptions. UserName, propriété

Définit et obtient le nom d’utilisateur d’un compte local ou d’un compte de domaine sur l’ordinateur distant. Cette propriété détermine le nom d’utilisateur pour l’authentification. Pour plus d’informations, consultez [authentification pour les connexions à distance](authentication-for-remote-connections.md).

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
ConnectionOptions.UserName As String
```



## <a name="property-value"></a>Valeur de la propriété

Chaîne qui contient le nom d’utilisateur d’un compte local ou d’un compte de domaine sur l’ordinateur distant.

Si aucune valeur n’est fournie et que l’indicateur **WSManFlagCredUsernamePassword** n’est pas défini, le nom d’utilisateur du compte qui exécute le script est utilisé.

Si aucune valeur n’est fournie et que l’indicateur **WSManFlagCredUsernamePassword** est défini, le script invite l’utilisateur à entrer le nom d’utilisateur et le mot de passe. Si un nom d’utilisateur et un mot de passe valides ne sont pas entrés, une erreur d’accès refusé est retournée.

## <a name="remarks"></a>Notes

La syntaxe suivante est utilisée pour spécifier cette propriété.


```VB
Set ConnectionOptions = wsman.CreateConnectionOptions
ConnectionOptions.UserName = "<UserName>"
```



Vous pouvez fournir le **nom d’utilisateur** et le [**mot de passe**](connectionoptions-password.md) d’un compte de domaine lors de l’utilisation de l’authentification [*Negotiate*](windows-remote-management-glossary.md) ou *Kerberos* , ou pour un compte local avec l’authentification de [*base*](windows-remote-management-glossary.md) . Pour se connecter à un compte local, les indicateurs [**WSMan. CreateSession**](wsman-createsession.md) doivent contenir la combinaison de l’indicateur **WSManFlagUseBasic** et de l’indicateur **WsmanFlagCredUserNamePassword** . Pour vous connecter à un compte de domaine, les indicateurs **WSMan. CreateSession** doivent contenir la combinaison de l’indicateur **WSManFlagUseNegotiate** et de l’indicateur **WsmanFlagCredUserNamePassword** , ou bien la combinaison de l’indicateur **WSManFlagUseKerberos** et de l’indicateur **WsmanFlagCredUserNamePassword** . Pour un compte de domaine, le nom **d’utilisateur** doit être spécifié sous la forme « nom \\ d’utilisateur de l’ordinateur », où la partie « ordinateur » de la chaîne peut être le nom ou l’adresse IP. Pour plus d’informations, consultez [authentification pour les connexions à distance](authentication-for-remote-connections.md).


```VB
Set ConnectionOptions = Wsman.CreateConnectionOptions
ConnectionOptions.Username = "MyUserName"
ConnectionOptions.Password = "MyPassword"
Set NewSession = Wsman.CreateSession("127.0.51.1", _
  (WSMan.SessionFlagUseBasic Or _
  WSMan.SessionFlagCredUsernamePassword), ConnectionOptions)
```



Pour la connexion à un compte de domaine, les indicateurs [**WSMan. CreateSession**](wsman-createsession.md) doivent contenir la combinaison de l’indicateur **WSManFlagUseNegotiate** et de l’indicateur **WsmanFlagCredUserNamePassword** pour la connexion à un compte de domaine, qui requiert l’authentification par négociation.


```VB
Set ConnectionOptions = Wsman.CreateConnectionOptions
ConnectionOptions.Username = "MyUserName"
ConnectionOptions.Password = "MyPassword"
Set NewSession = Wsman.CreateSession("127.0.51.1", _
  (WSMan.SessionFlagUseNegotiate Or _
  WSMan.SessionFlagCredUsernamePassword), ConnectionOptions)
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

[**ConnectionOptions**](connectionoptions.md)
</dt> </dl>

 

 





