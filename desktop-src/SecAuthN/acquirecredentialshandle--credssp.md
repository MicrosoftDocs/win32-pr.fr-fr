---
description: La fonction AcquireCredentialsHandle (CredSSP) acquiert un handle aux informations d’identification préexistantes d’un principal de sécurité.
ms.assetid: 3b73decf-75d4-4bc4-b7ca-5f16aaadff29
title: AcquireCredentialsHandle (CredSSP), fonction
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 0dbece18bc7a7de8ec35764c9879380e29292e92
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522773"
---
# <a name="acquirecredentialshandle-credssp-function"></a>AcquireCredentialsHandle (CredSSP), fonction

La fonction **AcquireCredentialsHandle (CredSSP)** acquiert un handle aux informations d’identification préexistantes d’un principal de sécurité. Ce handle est requis par les fonctions [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md) et [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md) . Il peut s’agir *d’informations d’identification* préexistantes, qui sont établies par le biais d’une ouverture de session système qui n’est pas décrite ici, ou l’appelant peut fournir d’autres informations d’identification.

> [!Note]  
> Ce n’est pas une « connexion au réseau » et n’implique pas la collecte des informations d’identification.

## <a name="syntax"></a>Syntaxe

```C++
SECURITY_STATUS SEC_ENTRY AcquireCredentialsHandle(
  _In_opt_   SEC_CHAR       *pszPrincipal,
  _In_       SEC_CHAR       *pszPackage,
  _In_       unsigned long  fCredentialUse,
  _In_opt_   void           *pvLogonID,
  _In_opt_   void           *pAuthData,
  _In_opt_   SEC_GET_KEY_FN pGetKeyFn,
  _Reserved_ void           *pvGetKeyArgument,
  _Out_      PCredHandle    phCredential,
  _Out_opt_  PTimeStamp     ptsExpiry
);
```

## <a name="parameters"></a>Paramètres

*pszPrincipal* \[ dans, facultatif\]

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du principal dont les informations d’identification seront référencées par le handle.

> [!Note]  
> Si le processus qui demande le descripteur n’a pas accès aux informations d’identification, la fonction retourne une erreur. Une chaîne NULL indique que le processus requiert un handle vers les informations d’identification de l’utilisateur sous le contexte de sécurité qu’il exécute.

*pszPackage* \[ dans\]

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du package de sécurité avec lequel ces informations d’identification seront utilisées. Il s’agit d’un nom de package de sécurité renvoyé dans le membre **Name** d’une structure [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) retournée par la fonction [**EnumerateSecurityPackages**](/windows/win32/api/sspi/nf-sspi-enumeratesecuritypackagesa) . Une fois qu’un contexte est établi, [**QueryContextAttributes (CredSSP)**](querycontextattributes--credssp.md) peut être appelé avec *UlAttribute* défini sur **SECPKG \_ attr \_ package \_ info** pour retourner des informations sur le package de sécurité en cours d’utilisation.

*fCredentialUse* \[ dans\]

Indicateur qui spécifie la façon dont ces informations d’identification seront utilisées. Ce paramètre peut prendre les valeurs suivantes.

| Valeur                                                                                                                                                                                                                                        | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SECPKG \_ cred \_ entrant**<br/>0x1  | Validez les informations d’identification du serveur entrant. Les informations d’identification entrantes peuvent être validées à l’aide d’une autorité d’authentification lorsque [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md) ou [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md) est appelé. Si une autorité de ce type n’est pas disponible, la fonction échoue et retourne **sec \_ E \_ no \_ \_ Authority Authentication**. La validation est spécifique au package |
| **SECPKG \_ cred \_ sortant**<br/>0x0 | Autorisez les informations d’identification du client local à préparer un jeton sortant. |

*pvLogonId* \[ dans, facultatif\]

Pointeur vers un [*identificateur unique local*](../secgloss/l-gly.md#_security_locally_unique_identifier_gly) (LUID) qui identifie l’utilisateur. Ce paramètre est fourni pour les processus de système de fichiers tels que les redirecteurs réseau. Ce paramètre peut être **NULL**.

*pAuthData* \[ dans, facultatif\]

Pointeur vers une structure [**de \_ références CREDSSP**](/windows/win32/api/credssp/ns-credssp-credssp_cred) qui spécifie les données d’authentification pour les packages Schannel et Negotiate.

*pGetKeyFn* \[ dans, facultatif\]

Réservé. Ce paramètre n’est pas utilisé et doit avoir la valeur **null**.

*pvGetKeyArgument* \[ dans, facultatif\]

Réservé. Ce paramètre doit avoir la valeur **null**.

*phCredential* \[ à\]

Pointeur vers la structure [CredHandle](sspi-handles.md) qui recevra le handle d’informations d’identification.

*ptsExpiry* \[ out, facultatif\]

Pointeur vers une structure d' [**horodatage**](timestamp.md) qui reçoit l’heure à laquelle les informations d’identification retournées expirent. La valeur de structure reçue dépend du package de sécurité, qui doit spécifier la valeur en heure locale.

## <a name="return-value"></a>Valeur de retour

Si la fonction est réussie, elle retourne **sec \_ E \_ OK**.

Si la fonction échoue, elle retourne l’un des codes d’erreur suivants.

| Code de retour                      | Description                                                              |
|----------------------------------|--------------------------------------------------------------------------|
| **s \_ E \_ mémoire insuffisante \_** | La mémoire disponible est insuffisante pour terminer l’action demandée. |
| **SEC \_ E \_ \_ erreur interne**      | Une erreur qui n’a pas été mappée à un code d’erreur SSPI s’est produite.                |
| **s \_ E \_ aucune \_ information d’identification**      | Aucune information d’identification n’est disponible dans le package de sécurité.                    |
| **SEC \_ E \_ non \_ propriétaire**           | L’appelant de la fonction n’a pas les informations d’identification nécessaires.      |
| **SEC \_ E \_ SECPKG \_ \_ introuvable**   | Le package de sécurité demandé n’existe pas.                           |
| **SEC \_ E \_ \_ informations d’identification inconnues** | Les informations d’identification fournies au package n’ont pas été reconnues.             |

## <a name="remarks"></a>Notes

La fonction **AcquireCredentialsHandle (CredSSP)** retourne un handle vers les informations d’identification d’un principal, tel qu’un utilisateur ou un client, tel qu’il est utilisé par un package de sécurité spécifique. La fonction peut retourner le handle à des informations d’identification préexistantes ou à des informations d’identification nouvellement créées et la retourner. Ce handle peut être utilisé dans les appels ultérieurs aux fonctions [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md) et [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md) .

En général, **AcquireCredentialsHandle (CredSSP)** ne fournit pas les informations d’identification d’autres utilisateurs ayant ouvert une session sur le même ordinateur. toutefois, un appelant avec SE \_ \_ [*privilège*](../secgloss/p-gly.md#_security_privilege_gly) nom TCB peut obtenir les informations d’identification d’une session de connexion existante en spécifiant l' [*identificateur de connexion*](../secgloss/l-gly.md#_security_logon_identifier_gly) (LUID) de cette session. En général, il est utilisé par les modules en mode noyau qui doivent agir pour le compte d’un utilisateur connecté.

Un package peut appeler la fonction dans *pGetKeyFn* fournie par le transport d’exécution RPC. Si le transport ne prend pas en charge la notion de rappel pour récupérer les informations d’identification, ce paramètre doit avoir la **valeur null**.

Pour les appelants en mode noyau, les différences suivantes doivent être notées :

- Les deux paramètres de chaîne doivent être des chaînes [*Unicode*](../secgloss/u-gly.md#_security_unicode_gly) .
- Les valeurs de mémoire tampon doivent être allouées dans la mémoire virtuelle du processus, et non dans le pool.

Lorsque vous avez terminé d’utiliser les informations d’identification retournées, libérez la mémoire utilisée par les informations d’identification en appelant la fonction [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) .

## <a name="requirements"></a>Spécifications

| Condition requise | Valeur |
|--------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge | Windows \[Applications de bureau Vista uniquement\]                                              |
| Serveur minimal pris en charge | Windows Serveur 2008 \[ applications de bureau uniquement\]                                        |
| En-tête                   | SSPI. h (include Security. h)                                                      |
| Bibliothèque                  | Secur32. lib                                                                      |
| DLL                      | Secur32.dll                                                                      |
| Noms Unicode et ANSI   | **AcquireCredentialsHandleW** (Unicode) et **AcquireCredentialsHandleA** (ANSI) |

## <a name="see-also"></a>Voir aussi

- [Fonctions SSPI](authentication-functions.md#sspi-functions)
- [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md)
- [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md)
- [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
