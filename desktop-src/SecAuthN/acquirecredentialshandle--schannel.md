---
description: Acquiert un handle pour les informations d’identification préexistantes d’un principal de sécurité qui utilise Schannel.
ms.assetid: 0f006670-a1e5-47ed-baf5-ed55bd42b468
title: AcquireCredentialsHandle (SChannel), fonction (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: d2fb9812817e27576667f7fa0ff5312eea8cea41743cbfc9e5b03267f837011f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101439"
---
# <a name="acquirecredentialshandle-schannel-function"></a>AcquireCredentialsHandle (SChannel) (fonction)

La fonction **AcquireCredentialsHandle (SChannel)** acquiert un handle aux informations d’identification préexistantes d’un [*principal de sécurité*](../secgloss/s-gly.md). Ce descripteur est requis par les fonctions [**InitializeSecurityContext (SChannel)**](initializesecuritycontext--schannel.md) et [**AcceptSecurityContext (SChannel)**](acceptsecuritycontext--schannel.md) . Il peut s’agir *d’informations d’identification* préexistantes, qui sont établies par le biais d’une ouverture de session système qui n’est pas décrite ici, ou l’appelant peut fournir d’autres informations d’identification.

> [!Note]  
> Ce n’est pas une « connexion au réseau » et n’implique pas la collecte des informations d’identification.

 

## <a name="syntax"></a>Syntaxe


```C++
SECURITY_STATUS SEC_Entry AcquireCredentialsHandle(
  _In_opt_  SEC_CHAR       *pszPrincipal,
  _In_      SEC_CHAR       *pszPackage,
  _In_      ULONG          fCredentialUse,
  _In_opt_  PLUID          pvLogonID,
  _In_opt_  PVOID          pAuthData,
  _In_opt_  SEC_GET_KEY_FN pGetKeyFn,
  _In_opt_  PVOID          pvGetKeyArgument,
  _Out_     PCredHandle    phCredential,
  _Out_opt_ PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pszPrincipal* \[ dans, facultatif\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du principal dont les informations d’identification seront référencées par le handle.

Lorsque vous utilisez le SSP Schannel, ce paramètre n’est pas utilisé et doit avoir la valeur **null**.

> [!Note]  
> Si le processus qui demande le descripteur n’a pas accès aux informations d’identification, la fonction retourne une erreur. Une chaîne NULL indique que le processus requiert un handle vers les informations d’identification de l’utilisateur sous le [*contexte de sécurité*](../secgloss/s-gly.md) qu’il exécute.

 

</dd> <dt>

*pszPackage* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du [*package de sécurité*](../secgloss/s-gly.md) avec lequel ces informations d’identification seront utilisées. Il s’agit d’un nom de [*package de sécurité*](../secgloss/s-gly.md) renvoyé dans le membre **Name** d’une structure [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) retournée par la fonction [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) . Une fois qu’un contexte est établi, [**QueryContextAttributes (SChannel)**](querycontextattributes--schannel.md) peut être appelé avec *ULATTRIBUTE* défini sur SECPKG \_ attr \_ package \_ info pour retourner des informations sur le [*package de sécurité*](../secgloss/s-gly.md) en cours d’utilisation.

Lorsque vous utilisez le SSP Schannel, définissez ce paramètre sur UNISP \_ Name.

</dd> <dt>

*fCredentialUse* \[ dans\]
</dt> <dd>

Indicateur qui spécifie la façon dont ces informations d’identification seront utilisées. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                               | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <dt>**SECPKG \_ cred \_ entrant**</dt> </dl>    | Validez les informations d’identification du serveur entrant. Les informations d’identification entrantes peuvent être validées à l’aide d’une autorité d’authentification lorsque [**InitializeSecurityContext (SChannel)**](initializesecuritycontext--schannel.md) ou [**AcceptSecurityContext (SChannel)**](acceptsecuritycontext--schannel.md) est appelé. Si une autorité de ce type n’est pas disponible, la fonction échoue et retourne SEC \_ E \_ no \_ Authority Authentication \_ . La validation est spécifique au package.<br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <dt>**SECPKG \_ cred \_ sortant**</dt> </dl> | Autorisez les informations d’identification du client local à préparer un jeton sortant.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

*pvLogonID* \[ dans, facultatif\]
</dt> <dd>

Pointeur vers un [*identificateur unique local*](../secgloss/l-gly.md) (LUID) qui identifie l’utilisateur. Ce paramètre est fourni pour les processus de système de fichiers tels que les redirecteurs réseau. Ce paramètre peut être **NULL**.

Lorsque vous utilisez le SSP Schannel, ce paramètre n’est pas utilisé et doit avoir la valeur **null**.

</dd> <dt>

*pAuthData* \[ dans, facultatif\]
</dt> <dd>

Pointeur vers des données spécifiques au package. Ce paramètre peut avoir la **valeur null**, ce qui indique que les informations d’identification par défaut pour ce [*package de sécurité*](../secgloss/s-gly.md) doivent être utilisées. Pour utiliser les informations d’identification fournies, transmettez une structure d' [**\_ \_ \_ identité Winnt auth s**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) qui comprend ces informations d’identification dans ce paramètre. Le temps d’exécution RPC passe tout ce qui a été fourni dans [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).

Lorsque vous utilisez le SSP Schannel, spécifiez une structure [**SCH_CREDENTIALS**](/windows/win32/api/schannel/ns-schannel-sch_credentials) qui indique le protocole à utiliser, ainsi que les paramètres des différentes fonctionnalités de canal personnalisables.

</dd> <dt>

*pGetKeyFn* \[ dans, facultatif\]
</dt> <dd>

Ce paramètre n’est pas utilisé et doit avoir la valeur **null**.

</dd> <dt>

*pvGetKeyArgument* \[ dans, facultatif\]
</dt> <dd>

Ce paramètre n’est pas utilisé et doit avoir la valeur **null**.

</dd> <dt>

*phCredential* \[ à\]
</dt> <dd>

Pointeur vers une structure [CredHandle](sspi-handles.md) pour recevoir le handle d’informations d’identification.

</dd> <dt>

*ptsExpiry* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une structure d' [**horodatage**](timestamp.md) qui reçoit l’heure à laquelle les informations d’identification retournées expirent. La valeur retournée dans cette structure d' **horodatage** dépend de la [*délégation avec restriction*](../secgloss/s-gly.md). Le [*package de sécurité*](../secgloss/s-gly.md) doit retourner cette valeur en heure locale.

Lorsque vous utilisez le SSP Schannel, ce paramètre est facultatif. Lorsque les informations d’identification à utiliser pour l’authentification sont un certificat, ce paramètre reçoit l’heure d’expiration de ce certificat. Si aucun certificat n’a été fourni, une valeur de temps maximale est retournée.

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

La fonction **AcquireCredentialsHandle (SChannel)** retourne un handle vers les informations d’identification d’un principal, tel qu’un utilisateur ou un client, tel qu’il est utilisé par une [*délégation restreinte*](../secgloss/s-gly.md)spécifique. Il peut s’agir du descripteur des informations d’identification préexistantes, ou la fonction peut créer un nouvel ensemble d’informations d’identification et la retourner. Ce handle peut être utilisé dans les appels ultérieurs aux fonctions [**AcceptSecurityContext (SChannel)**](acceptsecuritycontext--schannel.md) et [**InitializeSecurityContext (SChannel)**](initializesecuritycontext--schannel.md) .

En général, **AcquireCredentialsHandle (SChannel)** ne permet pas à un processus d’obtenir un descripteur des informations d’identification d’autres utilisateurs ayant ouvert une session sur le même ordinateur. toutefois, un appelant avec SE \_ \_ [*privilège*](../secgloss/s-gly.md) nom TCB a la possibilité de spécifier l' [*identificateur de connexion*](../secgloss/l-gly.md) (LUID) d’un jeton de session de connexion existant pour obtenir un descripteur des informations d’identification de cette session. En général, il est utilisé par les modules en mode noyau qui doivent agir pour le compte d’un utilisateur connecté.

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

[**AcceptSecurityContext (SChannel)**](acceptsecuritycontext--schannel.md)
</dt> <dt>

[**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

[**InitializeSecurityContext (SChannel)**](initializesecuritycontext--schannel.md)
</dt> <dt>

[**SCH_CREDENTIALS**](/windows/win32/api/schannel/ns-schannel-sch_credentials)
</dt> <dt>

[**Fonctions SSPI**](authentication-functions.md#sspi-functions)
</dt> <dt>
 

 
