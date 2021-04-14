---
title: Méthode WSMan. CreateSession (WSManDisp. h)
description: Crée un objet de session qui peut ensuite être utilisé pour les opérations réseau ultérieures.
ms.assetid: 299d9a95-bd30-414c-996d-6633e8b7ce52
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode CreateSession
- Méthode CreateSession Windows Remote Management, objet WSMan
- Objet WSMan Windows Remote Management, méthode CreateSession
topic_type:
- apiref
api_name:
- WSMan.CreateSession
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 966fd1f43db7114d3a4c0cf4cddaa4428fcb41c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508818"
---
# <a name="wsmancreatesession-method"></a>Méthode WSMan. CreateSession

Crée un objet de [**session**](session.md) qui peut ensuite être utilisé pour les opérations réseau ultérieures.

## <a name="syntax"></a>Syntaxe


```VB
WSMan.CreateSession( _
  [ ByVal connection ], _
  [ ByVal flags ], _
  [ ByVal connectionOptions ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*connexion* \[ dans, facultatif\]
</dt> <dd>

Protocole et service auquel se connecter, y compris IPv4 ou IPv6. Le format des informations de connexion est le suivant : < ><  >< *suffixe* d’adresse de transport>. Pour obtenir des exemples, consultez la section Notes. Si aucune information de connexion n’est fournie, l’ordinateur local est utilisé.

</dd> <dt>

*indicateurs* \[ dans, facultatif\]
</dt> <dd>

Indicateurs de session qui spécifient la méthode d’authentification, telle que [*Negotiate Authentication*](windows-remote-management-glossary.md) ou [*Digest Authentication*](windows-remote-management-glossary.md), pour la connexion à un ordinateur distant. Ces indicateurs spécifient également d’autres informations de connexion de session, telles que l’encodage ou le chiffrement. Ce paramètre doit contenir un ou plusieurs indicateurs dans **\_ \_ WSManSessionFlags** pour une connexion à distance. Pour plus d’informations, consultez [sessions, constantes](session-constants.md). Aucun paramètre d’indicateur n’est requis pour une connexion à WinRM sur l’ordinateur local. La valeur par défaut est **WSManFlagUseNegotiate**.

Pour plus d’informations, consultez [authentification pour les connexions à distance](authentication-for-remote-connections.md) et le paramètre *connectionOptions* .

</dd> <dt>

*connectionOptions* \[ dans, facultatif\]
</dt> <dd>

Pointeur vers un objet [**ConnectionOptions**](connectionoptions.md) qui contient un nom d’utilisateur et un mot de passe. La valeur par défaut est **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Objet de [**session**](session.md) qui peut ensuite être utilisé pour effectuer des opérations WinRM locales ou distantes.

## <a name="remarks"></a>Notes

La méthode **CreateSession** Initialise l’objet de [**session**](session.md) en rassemblant des paramètres, tels que des indicateurs, des informations d’identification et une chaîne de connexion pour le paramètre de *connexion* . **CreateSession** ne se connecte pas réellement à l’ordinateur local ou distant. Si la connexion ne peut pas être établie, un échec se produit lors de la première opération de **session** , telle qu’une opération d' [**extraction**](session-get.md) ou d' [**énumération**](session-enumerate.md), après l’appel à **CreateSession**. Ce comportement diffère d’une connexion [*WMI*](windows-remote-management-glossary.md) à un [*espace de noms*](windows-remote-management-glossary.md) sur un ordinateur distant. Pour plus d’informations, consultez [Windows Remote Management et WMI](windows-remote-management-and-wmi.md).

L’exemple de code VBScript suivant est utilisé pour appeler cette méthode.


```VB
Set session = _
    wsman.CreateSession("<Transport><Address><Suffix>")
```



Les exemples suivants illustrent les différents formats utilisés pour spécifier les informations de connexion dans le paramètre de *connexion* (lors de la création d’une session HTTPS, le champ *adresse*> <doit correspondre au nom du certificat de l’ordinateur serveur, sinon une défaillance se produit) :

-   "https://service"

    Utilise le protocole HTTPs pour se connecter à l’emplacement du service Web par défaut.

-   "https://service.corp.com/websvcs/wsman"

    Utilise le protocole HTTPs pour se connecter à l’emplacement du service Web spécifique.

-   "https:// \[ E3D7:0000:0000:0000:51F4:9BC8 : c0a8:6420 \] "

    Utilise HTTPs et IPv6 avec le port par défaut.

-   « https:// \[ E3D7:0000:0000:0000:51F4:9BC8 : c0a8:6420 \] : 9999/WSMan »

    Utilise HTTPs et IPv6 avec le port donné.

## <a name="examples"></a>Exemples

L’exemple de code VBScript suivant crée une session sur l’ordinateur local.


```VB
 Set NewSession = Wsman.CreateSession   
   
```



L’exemple de code VBScript suivant crée une session sur un ordinateur distant qui est identifié par une adresse IP. Le script fournit un nom d’utilisateur et un mot de passe pour un compte. Les indicateurs **WSManFlagCredUserNamePassword** et **WSManFlagUseBasic** sont combinés pour indiquer que le compte est un compte local sur l’ordinateur distant. Si la création de la session échoue, le script se termine. Le script utilise les méthodes qui retournent la constante, telles que [**WSMan. SessionFlagUseBasic**](wsman-sessionflagusebasic.md).

Pour exécuter ce script, sachez que vous devez configurer les paramètres de configuration par défaut pour le client et le serveur afin d’autoriser le trafic non chiffré et l’authentification de base (**AllowUnencrypted** a la valeur **true** et Basic défini sur **true**). Pour plus d’informations, consultez [installation et configuration de Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).


```VB
iFlags = WSMan.SessionFlagUseBasic Or WSMan.SessionFlagCredUsernamePassword
Set Options = Wsman.CreateConnectionOptions
Options.Username = "MyUserName"
Options.Password = "MyPassword"
Set NewSession = WSMan.CreateSession("127.0.51.1", iFlags, _
    Options) 
```



Dans l’exemple de code VBScript suivant, le compte est un compte de domaine et l’authentification par négociation est utilisée. Avec l’authentification Negotiate, vous devez spécifier le nom d’utilisateur en tant que `computername\username` ou `ipaddress\username` .


```VB
iFlags = WSMan.SessionFlagUseNegotiate Or WSMan.SessionFlagCredUsernamePassword
Set Options = Wsman.CreateConnectionOptions
Options.Username = "MyComputer\MyUserName"
Options.Password = "MyPassword"
Set NewSession = WSMan.CreateSession("127.0.51.1", iFlags, _
    Options) 
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

[**WSMan**](wsman.md)
</dt> <dt>

[**ConnectionOptions**](connectionoptions.md)
</dt> <dt>

[**session**](session.md)
</dt> <dt>

[Authentification des connexions à distance](authentication-for-remote-connections.md)
</dt> <dt>

[Installation et configuration de Windows Remote Management](installation-and-configuration-for-windows-remote-management.md)
</dt> </dl>

 

 





