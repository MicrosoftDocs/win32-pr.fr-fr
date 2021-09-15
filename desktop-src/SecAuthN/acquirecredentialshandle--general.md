---
description: Acquiert un handle pour les informations d’identification préexistantes d’un principal de sécurité.
ms.assetid: acda4cf3-39a6-4bd2-91a0-db1f191b57b5
title: AcquireCredentialsHandle (général), fonction (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 9c1202d8b482eee45697cec35ff6a7e8ba6ef354
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522772"
---
# <a name="acquirecredentialshandle-general-function"></a>AcquireCredentialsHandle (général) (fonction)

La fonction **AcquireCredentialsHandle (général)** acquiert un handle aux informations d’identification préexistantes d’un [*principal de sécurité*](../secgloss/s-gly.md). Ce handle est requis par les fonctions [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) et [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) . Il peut s’agir d’informations d’identification préexistantes, qui sont établies par le biais d’une ouverture de session système qui n’est pas décrite ici, ou l’appelant peut fournir d’autres informations d’identification.

> [!Note]  
> Ce n’est pas une « connexion au réseau » et n’implique pas la collecte des informations d’identification.

 

Pour plus d’informations sur l’utilisation de cette fonction avec un fournisseur SSP ( [*Security Support Provider*](../secgloss/s-gly.md) ) spécifique, consultez les rubriques suivantes.



| Rubrique                                                                                           | Description                                                                                                                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md)<br/>     | Acquiert un handle aux informations d’identification préexistantes d’un principal de sécurité qui utilise le protocole CredSSP (Credential Security Support Provider).<br/> |
| [**AcquireCredentialsHandle (Digest)**](acquirecredentialshandle--digest.md)<br/>       | Acquiert un handle pour les informations d’identification préexistantes d’un principal de sécurité qui utilise Digest.<br/>                                         |
| [**AcquireCredentialsHandle (Kerberos)**](acquirecredentialshandle--kerberos.md)<br/>   | Acquiert un handle pour les informations d’identification préexistantes d’un principal de sécurité qui utilise Kerberos.<br/>                                       |
| [**AcquireCredentialsHandle (Negotiate)**](acquirecredentialshandle--negotiate.md)<br/> | Acquiert un handle pour les informations d’identification préexistantes d’un principal de sécurité qui utilise Negotiate.<br/>                                      |
| [**AcquireCredentialsHandle (NTLM)**](acquirecredentialshandle--ntlm.md)<br/>           | Acquiert un handle pour les informations d’identification préexistantes d’un principal de sécurité qui utilise NTLM.<br/>                                           |
| [**AcquireCredentialsHandle (SChannel)**](acquirecredentialshandle--schannel.md)<br/>   | Acquiert un handle pour les informations d’identification préexistantes d’un principal de sécurité qui utilise Schannel.<br/>                                       |



 

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

Lorsque vous utilisez le SSP Digest, ce paramètre est facultatif.

Lorsque vous utilisez le SSP Schannel, ce paramètre n’est pas utilisé et doit avoir la valeur **null**.

> [!Note]  
> Si le processus qui demande le descripteur n’a pas accès aux informations d’identification, la fonction retourne une erreur. Une chaîne NULL indique que le processus requiert un handle vers les informations d’identification de l’utilisateur sous le [*contexte de sécurité*](../secgloss/s-gly.md) qu’il exécute.

 

</dd> <dt>

*pszPackage* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du [*package de sécurité*](../secgloss/s-gly.md) avec lequel ces informations d’identification seront utilisées. Il s’agit d’un nom de [*package de sécurité*](../secgloss/s-gly.md) renvoyé dans le membre **Name** d’une structure [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) retournée par la fonction [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) . Une fois qu’un contexte est établi, [**QueryContextAttributes (général)**](querycontextattributes--general.md) peut être appelé avec *ULATTRIBUTE* défini sur SECPKG \_ attr \_ package \_ info pour retourner des informations sur le [*package de sécurité*](../secgloss/s-gly.md) en cours d’utilisation.

Lorsque vous utilisez le SSP Digest, définissez ce paramètre sur WDIGEST \_ SP \_ Name.

Lorsque vous utilisez le SSP Schannel, définissez ce paramètre sur UNISP \_ Name.

</dd> <dt>

*fCredentialUse* \[ dans\]
</dt> <dd>

Indicateur qui spécifie la façon dont ces informations d’identification seront utilisées. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                                                    | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_AUTOLOGON_RESTRICTED"></span><span id="secpkg_cred_autologon_restricted"></span><dl> <dt>**SECPKG \_ \_ \_ Accès**</dt> automatique à cred-limité <dt>0x00000010</dt> </dl> | La sécurité n’utilise pas les informations d’identification d’ouverture de session par défaut ou les informations d’identification du [Gestionnaire d’informations d’identification](credential-manager.md).<br/> Cette valeur est prise en charge uniquement par la [*délégation conpressionnelle*](../secgloss/s-gly.md)Negotiate.<br/> **Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Cette valeur n’est pas prise en charge.<br/>                                                                                                                                 |
| <span id="SECPKG_CRED_BOTH"></span><span id="secpkg_cred_both"></span><dl> <dt>**SECPKG \_ cred \_**</dt> </dl>                                                                                                                  | Validez les informations d’identification entrantes ou utilisez des informations d’identification locales pour préparer un jeton sortant. Cet indicateur active à la fois d’autres indicateurs. Cet indicateur n’est pas valide avec les SSP condensé et Schannel.<br/>                                                                                                                                                                                                                                                                |
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <dt>**SECPKG \_ cred \_ entrant**</dt> </dl>                                                                                                         | Validez les informations d’identification du serveur entrant. Les informations d’identification entrantes peuvent être validées à l’aide d’une autorité d’authentification lorsque [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) ou [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) est appelé. Si une autorité de ce type n’est pas disponible, la fonction échoue et retourne SEC \_ E \_ no \_ Authority Authentication \_ . La validation est spécifique au package.<br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <dt>**SECPKG \_ cred \_ sortant**</dt> </dl>                                                                                                      | Autorisez les informations d’identification du client local à préparer un jeton sortant.<br/>                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="SECPKG_CRED_PROCESS_POLICY_ONLY"></span><span id="secpkg_cred_process_policy_only"></span><dl> <dt>**SECPKG \_ \_Stratégie de processus cred \_ \_ uniquement**</dt> <dt>0x00000020</dt> </dl>   | La fonction traite la stratégie de serveur et retourne **sec \_ E \_ sans \_ informations d’identification**, ce qui indique que l’application doit demander des informations d’identification.<br/> Cette valeur est prise en charge uniquement par la [*délégation conpressionnelle*](../secgloss/s-gly.md)Negotiate.<br/> **Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Cette valeur n’est pas prise en charge.<br/>                                                                                                          |



 

</dd> <dt>

*pvLogonID* \[ dans\]
</dt> <dd>

Pointeur vers un [*identificateur unique local*](../secgloss/l-gly.md) (LUID) qui identifie l’utilisateur. Ce paramètre est fourni pour les processus de système de fichiers tels que les redirecteurs réseau. Ce paramètre peut être **NULL**.

Lorsque vous utilisez le SSP Schannel, ce paramètre n’est pas utilisé et doit avoir la valeur **null**.

</dd> <dt>

*pAuthData* \[ dans\]
</dt> <dd>

Pointeur vers des données spécifiques au package. Ce paramètre peut avoir la **valeur null**, ce qui indique que les informations d’identification par défaut pour ce [*package de sécurité*](../secgloss/s-gly.md) doivent être utilisées. Pour utiliser les informations d’identification fournies, transmettez une structure d' [**\_ \_ \_ identité Winnt auth s**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) qui comprend ces informations d’identification dans ce paramètre. Le temps d’exécution RPC passe tout ce qui a été fourni dans [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).

Lorsque vous utilisez le SSP Digest, ce paramètre est un pointeur vers une structure d’identité d’authentification [**\_ winnt \_ \_ s**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) qui contient les informations d’authentification à utiliser pour localiser les informations d’identification.

Quand vous utilisez le SSP Schannel, spécifiez une structure [**Schannel \_ cred**](/windows/win32/api/schannel/ns-schannel-schannel_cred) qui indique le protocole à utiliser et les paramètres des différentes fonctionnalités de canal personnalisables.

Lors de l’utilisation des packages NTLM ou Negotiate, les longueurs maximales de caractères pour le nom d’utilisateur, le mot de passe et le domaine sont respectivement 256, 256 et 15.

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

Ce paramètre est défini sur une durée maximale constante. Il n’y a pas de délai d’expiration pour les informations d’identification ou les informations d’identification du [*contexte de sécurité*](../secgloss/s-gly.md)Digest ou lors de l’utilisation du SSP Digest.

Lorsque vous utilisez le SSP Schannel, ce paramètre est facultatif. Lorsque les informations d’identification à utiliser pour l’authentification sont un certificat, ce paramètre reçoit l’heure d’expiration de ce certificat. Si aucun certificat n’a été fourni, une valeur de temps maximale est retournée.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

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



 

## <a name="remarks"></a>Notes

La fonction **AcquireCredentialsHandle (General)** retourne un handle vers les informations d’identification d’un principal, tel qu’un utilisateur ou un client, tel qu’il est utilisé par une [*délégation restreinte*](../secgloss/s-gly.md)spécifique. Il peut s’agir du descripteur des informations d’identification préexistantes, ou la fonction peut créer un nouvel ensemble d’informations d’identification et la retourner. Ce handle peut être utilisé dans les appels ultérieurs aux fonctions [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) et [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) .

En général, **AcquireCredentialsHandle (général)** ne permet pas à un processus d’obtenir un handle pour les informations d’identification d’autres utilisateurs ayant ouvert une session sur le même ordinateur. toutefois, un appelant avec SE \_ \_ [*privilège*](../secgloss/s-gly.md) nom TCB a la possibilité de spécifier l' [*identificateur de connexion*](../secgloss/l-gly.md) (LUID) d’un jeton de session de connexion existant pour obtenir un descripteur des informations d’identification de cette session. En général, il est utilisé par les modules en mode noyau qui doivent agir pour le compte d’un utilisateur connecté.

Un package peut appeler la fonction dans *pGetKeyFn* fournie par le transport d’exécution RPC. Si le transport ne prend pas en charge la notion de rappel pour récupérer les informations d’identification, ce paramètre doit avoir la **valeur null**.

Pour les appelants en mode noyau, les différences suivantes doivent être notées :

-   Les deux paramètres de chaîne doivent être des chaînes [*Unicode*](../secgloss/u-gly.md) .
-   Les valeurs de mémoire tampon doivent être allouées dans la mémoire virtuelle du processus, et non dans le pool.

Lorsque vous avez terminé d’utiliser les informations d’identification retournées, libérez la mémoire utilisée par les informations d’identification en appelant la fonction [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) .

## <a name="requirements"></a>Spécifications



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

[**AcceptSecurityContext (général)**](acceptsecuritycontext--general.md)
</dt> <dt>

[**InitializeSecurityContext (général)**](initializesecuritycontext--general.md)
</dt> <dt>

[**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 
