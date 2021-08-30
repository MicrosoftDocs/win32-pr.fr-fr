---
description: Acquiert un handle pour les informations d’identification préexistantes d’un principal de sécurité qui utilise Negotiate.
ms.assetid: ff372163-c73b-41bb-afcb-7d5de7720967
title: AcquireCredentialsHandle (Negotiate), fonction (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 887b821143616951a17816d5beb4f1fc2dec84e1ab176ad78a894e2cdc3f918c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101449"
---
# <a name="acquirecredentialshandle-negotiate-function"></a>AcquireCredentialsHandle (Negotiate) (fonction)

La fonction **AcquireCredentialsHandle (Negotiate)** acquiert un handle aux informations d’identification préexistantes d’un [*principal de sécurité*](../secgloss/s-gly.md). Ce handle est requis par les fonctions [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) et [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) . Il peut s’agir *d’informations d’identification* préexistantes, qui sont établies par le biais d’une ouverture de session système qui n’est pas décrite ici, ou l’appelant peut fournir d’autres informations d’identification.

> [!Note]  
> Ce n’est pas une « connexion au réseau » et n’implique pas la collecte des informations d’identification.

 

## <a name="syntax"></a>Syntaxe


```C++
SECURITY_STATUS SEC_Entry AcquireCredentialsHandle(
  _In_  SEC_CHAR       *pszPrincipal,
  _In_  SEC_CHAR       *pszPackage,
  _In_  ULONG          fCredentialUse,
  _In_  PLUID          pvLogonID,
  _In_  PVOID          pAuthData,
  _In_  SEC_GET_KEY_FN pGetKeyFn,
  _In_  PVOID          pvGetKeyArgument,
  _Out_ PCredHandle    phCredential,
  _Out_ PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pszPrincipal* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du principal dont les informations d’identification seront référencées par le handle.

> [!Note]  
> Si le processus qui demande le descripteur n’a pas accès aux informations d’identification, la fonction retourne une erreur. Une chaîne NULL indique que le processus requiert un handle vers les informations d’identification de l’utilisateur sous le [*contexte de sécurité*](../secgloss/s-gly.md) qu’il exécute.

 

</dd> <dt>

*pszPackage* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du [*package de sécurité*](../secgloss/s-gly.md) avec lequel ces informations d’identification seront utilisées. Il s’agit d’un nom de [*package de sécurité*](../secgloss/s-gly.md) renvoyé dans le membre **Name** d’une structure [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) retournée par la fonction [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) . Une fois qu’un contexte est établi, [**QueryContextAttributes (Negotiate)**](querycontextattributes--negotiate.md) peut être appelé avec *ULATTRIBUTE* défini sur SECPKG \_ attr \_ package \_ info pour retourner des informations sur le [*package de sécurité*](../secgloss/s-gly.md) en cours d’utilisation.

Pour appeler correctement cette fonction à l’aide du SSP Negotiate, définissez ce paramètre sur « Negotiate ».

</dd> <dt>

*fCredentialUse* \[ dans\]
</dt> <dd>

Indicateur qui spécifie la façon dont ces informations d’identification seront utilisées. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                                                    | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_AUTOLOGON_RESTRICTED"></span><span id="secpkg_cred_autologon_restricted"></span><dl> <dt>**SECPKG \_ \_ \_ Accès**</dt> automatique à cred-limité <dt>0x00000010</dt> </dl> | La sécurité n’utilise pas les informations d’identification d’ouverture de session par défaut ou les informations d’identification du [Gestionnaire d’informations d’identification](credential-manager.md).<br/> **Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Cette valeur n’est pas prise en charge.<br/>                                                                                                                                                                                                                    |
| <span id="SECPKG_CRED_BOTH"></span><span id="secpkg_cred_both"></span><dl> <dt>**SECPKG \_ cred \_**</dt> </dl>                                                                                                                  | Validez les informations d’identification entrantes ou utilisez des informations d’identification locales pour préparer un jeton sortant. Cet indicateur active à la fois d’autres indicateurs.<br/>                                                                                                                                                                                                                                                                                                                                  |
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <dt>**SECPKG \_ cred \_ entrant**</dt> </dl>                                                                                                         | Validez les informations d’identification du serveur entrant. Les informations d’identification entrantes peuvent être validées à l’aide d’une autorité d’authentification lorsque [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) ou [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) est appelé. Si une autorité de ce type n’est pas disponible, la fonction échoue et retourne SEC \_ E \_ no \_ Authority Authentication \_ . La validation est spécifique au package.<br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <dt>**SECPKG \_ cred \_ sortant**</dt> </dl>                                                                                                      | Autorisez les informations d’identification du client local à préparer un jeton sortant.<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="SECPKG_CRED_PROCESS_POLICY_ONLY"></span><span id="secpkg_cred_process_policy_only"></span><dl> <dt>**SECPKG \_ \_Stratégie de processus cred \_ \_ uniquement**</dt> <dt>0x00000020</dt> </dl>   | La fonction traite la stratégie de serveur et retourne **sec \_ E \_ sans \_ informations d’identification**, ce qui indique que l’application doit demander des informations d’identification.<br/> **Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Cette valeur n’est pas prise en charge.<br/>                                                                                                                                                                                             |



 

</dd> <dt>

*pvLogonID* \[ dans\]
</dt> <dd>

Pointeur vers un [*identificateur unique local*](../secgloss/l-gly.md) (LUID) qui identifie l’utilisateur. Ce paramètre est fourni pour les processus de système de fichiers tels que les redirecteurs réseau. Ce paramètre peut être **NULL**.

</dd> <dt>

*pAuthData* \[ dans\]
</dt> <dd>

Pointeur vers des données spécifiques au package. Ce paramètre peut avoir la **valeur null**, ce qui indique que les informations d’identification par défaut pour ce [*package de sécurité*](../secgloss/s-gly.md) doivent être utilisées. Pour utiliser les informations d’identification fournies, transmettez une structure **opaque d’identité d' \_ \_ authentification \_ \_ PSEC Winnt** retournée à partir d’un appel précédent à la fonction [**SspiPromptForCredentials**](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa) .

**Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Le **type \_ \_ opaque d' \_ identité \_ d’authentification PSEC Winnt** et la fonction [**SspiPromptForCredentials**](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa) ne sont pas pris en charge. Pour utiliser les informations d’identification fournies, transmettez un pointeur vers une [**\_ \_ \_ identité Winnt auth**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) ou une structure d' [**\_ \_ \_ identité \_ d’authentification winnt winnt**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2) qui comprend ces informations d’identification.

Le temps d’exécution RPC passe tout ce qui a été fourni dans [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).

Lorsque vous utilisez le package Negotiate, les longueurs maximales de caractères pour le nom d’utilisateur, le mot de passe et le domaine sont respectivement 256, 256 et 15.

</dd> <dt>

*pGetKeyFn* \[ dans\]
</dt> <dd>

Ce paramètre n’est pas utilisé et doit avoir la valeur **null**.

</dd> <dt>

*pvGetKeyArgument* \[ dans\]
</dt> <dd>

Ce paramètre n’est pas utilisé et doit avoir la valeur **null**.

</dd> <dt>

*phCredential* \[ à\]
</dt> <dd>

Pointeur vers une structure [CredHandle](sspi-handles.md) pour recevoir le handle d’informations d’identification.

</dd> <dt>

*ptsExpiry* \[ à\]
</dt> <dd>

Pointeur vers une structure d' [**horodatage**](timestamp.md) qui reçoit l’heure à laquelle les informations d’identification retournées expirent. La valeur retournée dans cette structure d' **horodatage** dépend de la [*délégation avec restriction*](../secgloss/s-gly.md). Le [*package de sécurité*](../secgloss/s-gly.md) doit retourner cette valeur en heure locale.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction s’exécute correctement, la fonction retourne SEC \_ E \_ OK.

Si la fonction échoue, elle retourne l’un des codes d’erreur suivants.



| Code de retour                                                                                                 | Description                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**s \_ E \_ mémoire insuffisante \_**</dt> </dl> | La mémoire disponible est insuffisante pour terminer l’action demandée.<br/>                                                                  |
| <dl> <dt>**SEC \_ E \_ \_ erreur interne**</dt> </dl>      | Une erreur qui n’a pas été mappée à un code d’erreur SSPI s’est produite.<br/>                                                                               |
| <dl> <dt>**s \_ E \_ aucune \_ information d’identification**</dt> </dl>      | Aucune information d’identification n’est disponible dans la [*délégation conpressionnelle*](../secgloss/s-gly.md).<br/> |
| <dl> <dt>**SEC \_ E \_ non \_ propriétaire**</dt> </dl>           | L’appelant de la fonction n’a pas les informations d’identification nécessaires.<br/>                                                                     |
| <dl> <dt>**SEC \_ E \_ SECPKG \_ \_ introuvable**</dt> </dl>   | Le [*package de sécurité*](../secgloss/s-gly.md) demandé n’existe pas.<br/>                                                                                          |
| <dl> <dt>**SEC \_ E \_ \_ informations d’identification inconnues**</dt> </dl> | Les informations d’identification fournies au package n’ont pas été reconnues.<br/>                                                                            |



 

## <a name="remarks"></a>Remarques

La fonction **AcquireCredentialsHandle (Negotiate)** retourne un handle vers les informations d’identification d’un principal, tel qu’un utilisateur ou un client, tel qu’il est utilisé par une [*délégation restreinte*](../secgloss/s-gly.md)spécifique. Il peut s’agir du descripteur des informations d’identification préexistantes, ou la fonction peut créer un nouvel ensemble d’informations d’identification et la retourner. Ce handle peut être utilisé dans les appels ultérieurs aux fonctions [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) et [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) .

En général, **AcquireCredentialsHandle (Negotiate)** ne permet pas à un processus d’obtenir un handle pour les informations d’identification d’autres utilisateurs ayant ouvert une session sur le même ordinateur. toutefois, un appelant avec SE \_ \_ [*privilège*](../secgloss/s-gly.md) nom TCB a la possibilité de spécifier l' [*identificateur de connexion*](../secgloss/l-gly.md) (LUID) d’un jeton de session de connexion existant pour obtenir un descripteur des informations d’identification de cette session. En général, il est utilisé par les modules en mode noyau qui doivent agir pour le compte d’un utilisateur connecté.

Un package peut appeler la fonction dans *pGetKeyFn* fournie par le transport d’exécution RPC. Si le transport ne prend pas en charge la notion de rappel pour récupérer les informations d’identification, ce paramètre doit avoir la **valeur null**.

Pour les appelants en mode noyau, les différences suivantes doivent être notées :

-   Les deux paramètres de chaîne doivent être des chaînes [*Unicode*](../secgloss/u-gly.md) .
-   Les valeurs de mémoire tampon doivent être allouées dans la mémoire virtuelle du processus, et non dans le pool.

Lorsque vous avez terminé d’utiliser les informations d’identification retournées, libérez la mémoire utilisée par les informations d’identification en appelant la fonction [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                   |
| En-tête<br/>                   | <dl> <dt>SSPI. h (include Security. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Secur32. lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |
| Noms Unicode et ANSI<br/>   | **AcquireCredentialsHandleW** (Unicode) et **AcquireCredentialsHandleA** (ANSI)<br/>            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md)
</dt> <dt>

[**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md)
</dt> <dt>

[**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 
