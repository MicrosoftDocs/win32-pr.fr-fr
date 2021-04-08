---
description: La fonction LogonUserExExW tente de connecter un utilisateur à l’ordinateur local.
ms.assetid: d90db4c6-a711-4519-8b91-5069cee07738
title: LogonUserExExW, fonction (Winbasep. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LogonUserExExW
api_type:
- DllExport
api_location:
- Advapi32.dll
ms.openlocfilehash: 35ec65e7899f45a5222ae12b08992e77ea67f306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035017"
---
# <a name="logonuserexexw-function"></a>LogonUserExExW fonction)

La fonction **LogonUserExExW** tente de connecter un utilisateur à l’ordinateur local. L’ordinateur local est l’ordinateur à partir duquel **LogonUserExExW** a été appelé. Vous ne pouvez pas utiliser **LogonUserExExW** pour vous connecter à un ordinateur distant. Spécifiez l’utilisateur à l’aide d’un nom d’utilisateur et d’un domaine et [*authentifiez*](../secgloss/a-gly.md) l’utilisateur à l’aide d’un mot de passe en texte clair. Si la fonction est réussie, elle reçoit un handle vers un jeton qui représente l’utilisateur connecté. Vous pouvez ensuite utiliser ce handle de jeton pour emprunter l’identité de l’utilisateur spécifié ou, dans la plupart des cas, pour créer un [*processus*](../secgloss/p-gly.md) qui s’exécute dans le contexte de l’utilisateur spécifié.

Cette fonction est similaire à la fonction [**LogonUserEx**](/windows/desktop/api/Winbase/nf-winbase-logonuserexa) , à ceci près qu’elle prend le paramètre supplémentaire, *pTokenGroups*, qui est un ensemble d’un ou plusieurs [*identificateurs de sécurité*](../secgloss/s-gly.md) (SID) qui sont ajoutés au jeton renvoyé à l’appelant lorsque l’ouverture de session est réussie.

Cette fonction n’est pas déclarée dans un en-tête public et n’a pas de bibliothèque d’importation associée. Vous devez utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Advapi32.dll.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI LogonUserExExW(
  _In_      LPTSTR        lpszUsername,
  _In_opt_  LPTSTR        lpszDomain,
  _In_opt_  LPTSTR        lpszPassword,
  _In_      DWORD         dwLogonType,
  _In_      DWORD         dwLogonProvider,
  _In_opt_  PTOKEN_GROUPS pTokenGroups,
  _Out_opt_ PHANDLE       phToken,
  _Out_opt_ PSID          *ppLogonSid,
  _Out_opt_ PVOID         *ppProfileBuffer,
  _Out_opt_ LPDWORD       pdwProfileLength,
  _Out_opt_ PQUOTA_LIMITS pQuotaLimits
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpszUsername* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’utilisateur. Il s’agit du nom du compte d’utilisateur auquel se connecter. Si vous utilisez le format UPN ( [*user principal name*](../secgloss/u-gly.md) ), le paramètre *lpszDomain* doit avoir la **valeur null**.

</dd> <dt>

*lpszDomain* \[ dans, facultatif\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du domaine ou du serveur dont la base de données du compte contient le compte *lpszUsername* . Si ce paramètre a la **valeur null**, le nom d’utilisateur doit être spécifié au format UPN. Si ce paramètre est « . », la fonction valide le compte à l’aide de la base de données de comptes locale uniquement.

</dd> <dt>

*lpszPassword* \[ dans, facultatif\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le mot de passe en texte clair pour le compte d’utilisateur spécifié par *lpszUsername*. Lorsque vous avez fini d’utiliser le mot de passe, effacez le mot de passe de la mémoire en appelant la fonction [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) . Pour plus d’informations sur la protection des mots de passe, consultez [gestion des mots de passe](../secbp/handling-passwords.md).

</dd> <dt>

*dwLogonType* \[ dans\]
</dt> <dd>

Type d’opération d’ouverture de session à effectuer. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                                        | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOGON32_LOGON_INTERACTIVE"></span><span id="logon32_logon_interactive"></span><dl> <dt>**LOGON32 \_ Ouverture de session \_ interactive**</dt> <dt>2</dt> </dl>                    | Ce type d’ouverture de session est destiné aux utilisateurs qui se connectent de manière interactive à l’ordinateur, comme un utilisateur connecté par un serveur [*Terminal*](../secgloss/t-gly.md) Server, un interpréteur de commandes à distance ou un processus similaire. Ce type d’ouverture de session a des frais supplémentaires pour la mise en cache des informations de connexion pour les opérations déconnectées. par conséquent, il est inapproprié pour certaines applications client/serveur, telles qu’un serveur de messagerie.<br/>                                  |
| <span id="LOGON32_LOGON_NETWORK"></span><span id="logon32_logon_network"></span><dl> <dt>**LOGON32 \_ CONNEXION \_ réseau**</dt> <dt>3</dt> </dl>                                | Ce type d’ouverture de session est destiné aux serveurs à hautes performances pour authentifier les mots de passe en texte clair. La fonction **LogonUserExExW** ne met pas en cache les informations d’identification pour ce type de connexion.<br/>                                                                                                                                                                                                                                                                                                 |
| <span id="LOGON32_LOGON_BATCH"></span><span id="logon32_logon_batch"></span><dl> <dt>**LOGON32 \_ \_Lot d’ouverture de session**</dt> <dt>4</dt> </dl>                                      | Ce type de connexion est destiné aux serveurs batch, où les processus peuvent s’exécuter pour le compte d’un utilisateur sans leur intervention directe. Ce type est également destiné aux serveurs de performances plus importants qui traitent de nombreuses tentatives d’authentification en texte clair à la fois, comme les serveurs de messagerie ou les serveurs Web. La fonction **LogonUserExExW** ne met pas en cache les informations d’identification pour ce type de connexion.<br/>                                                                                                           |
| <span id="LOGON32_LOGON_SERVICE"></span><span id="logon32_logon_service"></span><dl> <dt>**LOGON32 \_ \_Service d’ouverture de session**</dt> <dt>5</dt> </dl>                                | Indique une ouverture de session de type service. Le compte fourni doit avoir le privilège de service activé.<br/>                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="LOGON32_LOGON_UNLOCK"></span><span id="logon32_logon_unlock"></span><dl> <dt>**LOGON32 \_ Ouverture de session \_ déverrouillage**</dt> <dt>7</dt> </dl>                                   | Ce type de connexion concerne les dll [*Gina*](../secgloss/g-gly.md) qui se connectent aux utilisateurs qui se connectent de manière interactive à l’ordinateur. Ce type d’ouverture de session peut générer un enregistrement d’audit unique qui indique le moment où la station de travail a été déverrouillée.<br/>                                                                                                                                                                                                                   |
| <span id="LOGON32_LOGON_NETWORK_CLEARTEXT"></span><span id="logon32_logon_network_cleartext"></span><dl> <dt>**LOGON32 \_ \_Texte en \_ clair du réseau de connexion**</dt> <dt>8</dt> </dl> | Ce type d’ouverture de session conserve le nom et le mot de passe dans le [*package d’authentification*](../secgloss/a-gly.md), ce qui permet au serveur d’établir des connexions à d’autres serveurs réseau tout en usurpant l’identité du client. Un serveur peut accepter des informations d’identification en texte clair d’un client, appeler **LogonUserExExW**, vérifier que l’utilisateur peut accéder au système sur le réseau et toujours communiquer avec d’autres serveurs. <br/> |
| <span id="LOGON32_LOGON_NEW_CREDENTIALS"></span><span id="logon32_logon_new_credentials"></span><dl> <dt>**LOGON32 \_ Ouvrir une session- \_ nouvelles \_ informations d’identification**</dt> <dt>9</dt> </dl>       | Ce type d’ouverture de session permet à l’appelant de cloner son jeton actuel et de spécifier de nouvelles informations d’identification pour les connexions sortantes. La nouvelle session d’ouverture de session a le même identificateur local, mais elle utilise des informations d’identification différentes pour d’autres connexions réseau.<br/> Ce type d’ouverture de session est pris en charge uniquement par le fournisseur **LOGON32 \_ \_ WINNT50** Logon Provider.<br/>                                                                                                                                       |



 

</dd> <dt>

*dwLogonProvider* \[ dans\]
</dt> <dd>

Fournisseur d’ouverture de session. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                           | Signification                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOGON32_PROVIDER_DEFAULT"></span><span id="logon32_provider_default"></span><dl> <dt>**\_Fournisseur LOGON32 \_ par défaut**</dt> </dl> | Utilisez le fournisseur d’ouverture de session standard pour le système. Le [*fournisseur de sécurité*](../secgloss/s-gly.md) par défaut est NTLM.<br/> |
| <span id="LOGON32_PROVIDER_WINNT50"></span><span id="logon32_provider_winnt50"></span><dl> <dt>**\_Fournisseur LOGON32 \_ WINNT50**</dt> </dl> | Utilisez le fournisseur Negotiate Logon. <br/>                                                                                                                                                         |
| <span id="LOGON32_PROVIDER_WINNT40"></span><span id="logon32_provider_winnt40"></span><dl> <dt>**\_Fournisseur LOGON32 \_ WINNT40**</dt> </dl> | Utilisez le fournisseur d’ouverture de session NTLM.<br/>                                                                                                                                                               |



 

</dd> <dt>

*pTokenGroups* \[ dans, facultatif\]
</dt> <dd>

Pointeur vers une structure [**de \_ groupes de jetons**](/windows/win32/api/winnt/ns-winnt-token_groups) qui spécifie une liste de SID de groupe ajoutée au jeton que cette fonction reçoit lorsque la connexion réussit. Les SID ajoutés au jeton affectent également l’expansion de groupe. Par exemple, si les SID ajoutés sont membres de groupes locaux, ces groupes sont également ajoutés au jeton d’accès reçu.

Si ce paramètre n’est pas **null**, l’appelant de cette fonction doit avoir le privilège de **privilège de se \_ TCB \_** accordé et activé.

</dd> <dt>

*phToken* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une variable de handle qui reçoit un handle vers un jeton qui représente l’utilisateur spécifié.

Vous pouvez utiliser le handle retourné dans les appels à la fonction [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) .

Dans la plupart des cas, le handle retourné est un [*jeton principal*](../secgloss/p-gly.md) que vous pouvez utiliser dans les appels à la fonction [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) . Toutefois, si vous spécifiez l' \_ indicateur de réseau de connexion LOGON32 \_ , **LogonUserExExW** retourne un [*jeton d’emprunt d’identité*](../secgloss/i-gly.md) que vous ne pouvez pas utiliser dans **CreateProcessAsUser** , sauf si vous appelez [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) pour convertir le jeton d’emprunt d’identité en jeton principal.

Lorsque vous n’avez plus besoin de ce handle, fermez-le en appelant la fonction [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) .

</dd> <dt>

*ppLogonSid* \[ out, facultatif\]
</dt> <dd>

Pointeur vers un pointeur vers un SID qui reçoit le SID de l’utilisateur connecté.

Lorsque vous avez fini d’utiliser le SID, libérez-le en appelant la fonction [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) .

</dd> <dt>

*ppProfileBuffer* \[ out, facultatif\]
</dt> <dd>

Pointeur vers un pointeur qui reçoit l’adresse d’une mémoire tampon qui contient le profil de l’utilisateur connecté.

</dd> <dt>

*pdwProfileLength* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une **valeur DWORD** qui reçoit la longueur de la mémoire tampon du profil.

</dd> <dt>

*pQuotaLimits* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une structure [**de \_ limites de quota**](/windows/desktop/api/Winnt/ns-winnt-quota_limits) qui reçoit des informations sur les quotas pour l’utilisateur connecté.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la fonction retourne une valeur différente de zéro.

Si la fonction échoue, elle retourne zéro. Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Remarques

Le type de connexion **\_ \_ réseau LOGON32 Logon** est plus rapide, mais il présente les limitations suivantes :

-   La fonction retourne un [*jeton d’emprunt d’identité*](../secgloss/i-gly.md), et non un jeton principal. Vous ne pouvez pas utiliser ce jeton directement dans la fonction [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) . Toutefois, vous pouvez appeler la fonction [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) pour convertir le jeton en jeton principal, puis l’utiliser dans **CreateProcessAsUser**.
-   Si vous convertissez le jeton en jeton principal et que vous l’utilisez dans [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) pour démarrer un processus, le nouveau processus ne peut pas accéder à d’autres ressources réseau, telles que des serveurs distants ou des imprimantes, par le biais du redirecteur. Une exception est que, si la ressource réseau n’est pas contrôlée par l’accès, le nouveau processus peut y accéder.

Le compte spécifié par *lpszUsername* doit disposer des droits de compte nécessaires. Par exemple, pour ouvrir une session sur un utilisateur avec l’indicateur **\_ \_ interactif d’ouverture de session LOGON32** , l’utilisateur (ou un groupe auquel l’utilisateur appartient) doit avoir le droit de compte de **\_ \_ \_ nom d’ouverture de session interactive se** . Pour obtenir la liste des droits de compte qui affectent les différentes opérations d’ouverture de session, consultez [droits d’accès à un objet de compte](../secmgmt/account-object-access-rights.md).

Un utilisateur est considéré comme connecté s’il existe au moins un jeton. Si vous appelez [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) , puis que vous fermez le jeton, l’utilisateur est toujours connecté jusqu’à ce que le processus (et tous les processus enfants) se termine.

Si le paramètre facultatif *pTokenGroups* est fourni, LSA n’ajoutera pas automatiquement le SID local ou le SID d’ouverture de session.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                                  |
| Version<br/>                  | LogonUserExExW est également disponible onWindows Server 2003 ou Windows XPwith la version de distribution générale.<br/> |
| En-tête<br/>                   | <dl> <dt>Winbasep. h</dt> </dl>                                 |
| DLL<br/>                      | <dl> <dt>Advapi32.dll</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Access Control client/serveur](../secauthz/client-server-access-control.md)
</dt> <dt>

[Fonctions de Access Control client/serveur](../secauthz/authorization-functions.md)
</dt> <dt>

[**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle)
</dt> <dt>

[**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)
</dt> <dt>

[**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex)
</dt> <dt>

[**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser)
</dt> <dt>

[**LogonUserEx**](/windows/desktop/api/Winbase/nf-winbase-logonuserexa)
</dt> <dt>

[**limites de QUOTA \_**](/windows/desktop/api/Winnt/ns-winnt-quota_limits)
</dt> </dl>

 

 
