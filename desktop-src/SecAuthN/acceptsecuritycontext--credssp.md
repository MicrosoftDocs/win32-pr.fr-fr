---
description: Permet au composant serveur d’une application de transport d’établir un contexte de sécurité entre le serveur et un client distant.
ms.assetid: a53f733e-b646-4431-b021-a2c446308849
title: AcceptSecurityContext (CredSSP) (fonction)
ms.topic: article
ms.date: 07/25/2019
ms.openlocfilehash: 681e03ea15729cc8726d63551e8b7b0a2b39ecac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545823"
---
# <a name="acceptsecuritycontext-credssp-function"></a>AcceptSecurityContext (CredSSP) (fonction)

La fonction **AcceptSecurityContext (CredSSP)** permet au composant serveur d’une application de transport d’établir un contexte de sécurité entre le serveur et un client distant. Le client distant appelle la fonction [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md) pour démarrer le processus d’établissement d’un contexte de sécurité. Le serveur peut exiger un ou plusieurs jetons de réponse du client distant pour terminer l’établissement du contexte de sécurité.

## <a name="syntax"></a>Syntaxe

```C++
SECURITY_STATUS SEC_ENTRY AcceptSecurityContext(
  _In_opt_    PCredHandle    phCredential,
  _In_opt_    PCtxtHandle    phContext,
  _In_opt_    PSecBufferDesc pInput,
  _In_        unsigned long  fContextReq,
  _In_        unsigned long  TargetDataRep,
  _Inout_opt_ PCtxtHandle    phNewContext,
  _Inout_opt_ PSecBufferDesc pOutput,
  _Out_       unsigned long  *pfContextAttr,
  _Out_opt_   PTimeStamp     ptsExpiry
);
```

## <a name="parameters"></a>Paramètres

*phCredential* \[ dans, facultatif\]

Handle vers les informations d’identification du serveur. Pour récupérer ce handle, le serveur appelle la fonction [**CredSSP (AcquireCredentialsHandle)**](acquirecredentialshandle--credssp.md) avec l’indicateur SECPKG \_ cred \_ entrant ou SECPKG \_ cred \_ défini.

*phContext* \[ dans, facultatif\]

Pointeur vers une structure [CtxtHandle](sspi-handles.md) . Lors du premier appel à **AcceptSecurityContext (CredSSP)**, ce pointeur est **null**. Lors des appels suivants, *phContext* spécifie le contexte partiellement formé retourné dans le paramètre *phNewContext* par le premier appel.

*pInput* \[ dans, facultatif\]

Pointeur vers une structure [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) générée par un appel client à [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md). La structure contient le descripteur de mémoire tampon d’entrée.

La première mémoire tampon doit être de **type \_ jeton SECBUFFER** et contenir le jeton de sécurité reçu du client. La deuxième mémoire tampon doit être de type **SECBUFFER \_ vide**.

*fContextReq* \[ dans\]

Bits indicateurs qui spécifient les attributs requis par le serveur pour établir le contexte. **Les indicateurs de bits** peuvent être combinés à l’aide d’opérations or au niveau du bit. Ce paramètre peut être une ou plusieurs des valeurs suivantes.

| Valeur                          | Signification                                                                                                                                                                                                        |
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_demande ASC \_ allouer de la \_ mémoire** | CredSSP (Credential Security Support Provider) alloue des tampons de sortie. Lorsque vous avez fini d’utiliser les tampons de sortie, libérez-les en appelant la fonction [**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) . |
| **connexion à la \_ demande ASC \_**       | Le contexte de sécurité ne gère pas les messages de mise en forme.                                                                                                                                                      |
| **\_délégué req \_ ASC**         | Le serveur est autorisé à emprunter l’identité du client. Ignorez cet indicateur pour la délégation avec restriction.                                                         |
| **\_ \_ erreur étendue ASC \_ req**  | Lorsque des erreurs se produisent, le tiers distant est averti.                                                                                                                                                          |
| **détection de la \_ RElecture de la demande ASC \_ \_**   | Détecter les paquets relus.                                                                                                                                                                                       |
| **détection de la \_ séquence de demande ASC \_ \_** | Détecte les messages reçus en dehors de la séquence.                                                                                                                                                                      |
| **\_flux de demande ASC \_**           | Prend en charge une connexion orientée flux.                                                                                                                                                                          |

Pour connaître les indicateurs d’attribut possibles et leurs significations, consultez [spécifications de contexte](context-requirements.md). Les indicateurs utilisés pour ce paramètre sont préfixés avec ASC \_ req, par exemple ASC \_ req \_ Delegate.

Les attributs demandés ne sont peut-être pas pris en charge par le client. Pour plus d’informations, consultez le paramètre *pfContextAttr* .

*TargetDataRep* \[ dans\]

Représentation des données, telle que l’ordonnancement des octets, sur la cible. Ce paramètre peut être **Security \_ native \_ DREP** ou **Security \_ Network \_ DREP**.

*phNewContext* \[ in, out, facultatif\]

Pointeur vers une structure [CtxtHandle](sspi-handles.md) . Lors du premier appel à **AcceptSecurityContext (CredSSP)**, ce pointeur reçoit le nouveau handle de contexte. Lors des appels suivants, *phNewContext* peut être le même que le handle spécifié dans le paramètre *phContext* .

*pOutput* \[ in, out, facultatif\]

Pointeur vers une structure [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) qui contient le descripteur de mémoire tampon de sortie. Cette mémoire tampon est envoyée au client pour l’entrée dans des appels supplémentaires à [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md). Une mémoire tampon de sortie peut être générée même si la fonction retourne SEC \_ E \_ OK. Toute mémoire tampon générée doit être renvoyée à l’application cliente.

Lors de la sortie, cette mémoire tampon reçoit un jeton pour le contexte de sécurité. Le jeton doit être envoyé au client. La fonction peut également retourner une mémoire tampon de type SECBUFFER \_ extra.

*pfContextAttr* \[ à\]

Pointeur vers un jeu d’indicateurs binaires qui indiquent les attributs du contexte établi. Pour obtenir une description des différents attributs, consultez [spécifications de contexte](context-requirements.md). Les indicateurs utilisés pour ce paramètre sont préfixés par ASC \_ RET, par exemple ASC \_ RET \_ Delegate.

Ne vérifiez pas les attributs liés à la sécurité jusqu’à ce que l’appel de fonction final soit retourné avec succès. Les indicateurs d’attribut non liés à la sécurité, tels que l' \_ indicateur ASC RET \_ allouée la \_ mémoire, peuvent être vérifiés avant le retour final.

*ptsExpiry* \[ out, facultatif\]

Pointeur vers une structure d' [**horodatage**](timestamp.md) qui reçoit l’heure d’expiration du contexte. Nous recommandons que le package de sécurité retourne toujours cette valeur en heure locale.

> [!Note]  
> Jusqu’au dernier appel du processus d’authentification, l’heure d’expiration du contexte peut être incorrecte, car des informations supplémentaires seront fournies lors des étapes ultérieures de la négociation. Par conséquent, *ptsTimeStamp* doit avoir la **valeur null** jusqu’au dernier appel à la fonction.

## <a name="return-value"></a>Valeur retournée

Cette fonction retourne l’une des valeurs suivantes.

| Code/valeur de retour                                   | Description                                                                                                                                                                 |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SEC_E_INCOMPLETE_MESSAGE <br/> 0x80090318L          | La fonction a réussi. Les données de la mémoire tampon d’entrée sont incomplètes. L’application doit lire à nouveau les données supplémentaires du client et appeler [<strong>AcceptSecurityContext (CredSSP)</strong>](acceptsecuritycontext--credssp.md) . |
| SEC_E_INSUFFICIENT_MEMORY <br/> 0x80090300L         | Échec de la fonction. La mémoire disponible est insuffisante pour terminer l’action demandée.                                                                                 |
| SEC_E_INTERNAL_ERROR <br/> 0x80090304L              | Échec de la fonction. Une erreur qui n’a pas été mappée à un code d’erreur SSPI s’est produite.                                                                                              |
| SEC_E_INVALID_HANDLE <br/> 0x80100003L              | Échec de la fonction. Le handle passé à la fonction n’est pas valide.                                                                                                        |
| SEC_E_INVALID_TOKEN <br/> 0x80090308L               | Échec de la fonction. Le jeton passé à la fonction n’est pas valide.                                                                                                         |
| SEC_E_LOGON_DENIED <br/> 0x8009030CL                | L’ouverture de session a échoué.                                                                                                                                                           |
| SEC_E_NO_AUTHENTICATING_AUTHORITY <br/> 0x80090311L | Échec de la fonction. Aucune autorité n’a pu être contactée pour l’authentification. Cela peut être dû aux conditions suivantes :<br/><ul><li>Le nom de domaine du tiers d’authentification est incorrect.</li><li>Le domaine n’est pas disponible.</li><li>La relation d’approbation a échoué. |
| SEC_E_NO_CREDENTIALS <br/>0x8009030EL               | Échec de la fonction. Le descripteur des informations d’identification spécifié dans le paramètre *phCredential* n’est pas valide.                            |
| SEC_E_OK <br/> 0x00000000L                          | La fonction a réussi. Le contexte de sécurité reçu du client a été accepté. Si la fonction a généré un jeton de sortie, le jeton doit être envoyé au processus client. |
| SEC_E_UNSUPPORTED_FUNCTION <br/> 0x80090302L        | Échec de la fonction. Le paramètre *fContextReq* a spécifié un indicateur d’attribut de contexte (ASC_REQ_DELEGATE ou ASC_REQ_PROMPT_FOR_CREDS) qui n’était pas valide.                       |
| SEC_I_COMPLETE_AND_CONTINUE <br/> 0x00090314L       | La fonction a réussi. Le serveur doit appeler [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) et transmettre le jeton de sortie au client. Le serveur doit ensuite attendre un jeton de retour du client avant d’effectuer un autre appel à [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md). |
| SEC_I_COMPLETE_NEEDED <br/> 0x00090313L             | La fonction a réussi. Le serveur doit terminer la génération du message à partir du client avant d’appeler [ **CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken)                             |
| SEC_I_CONTINUE_NEEDED <br/> 0x00090312L             | La fonction a réussi. Le serveur doit envoyer le jeton de sortie au client et attendre un jeton retourné. Le jeton retourné doit être passé dans *pInput* pour un autre appel à [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md).


## <a name="remarks"></a>Notes

La fonction **AcceptSecurityContext (CredSSP)** est l’équivalent serveur de la fonction [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md) .

Lorsque le serveur reçoit une demande d’un client, il utilise le paramètre *fContextReq* pour spécifier ce qu’il requiert de la session. De cette manière, un serveur peut exiger que les clients soient en mesure d’utiliser une session confidentielle ou contrôlée par [*l’intégrité*](../secgloss/i-gly.md); Il peut rejeter les clients qui ne peuvent pas répondre à cette demande. Une autre solution consiste à ne pas avoir besoin d’un serveur. ce que le client requiert ou peut fournir est retourné dans le paramètre *pfContextAttr* .

Les paramètres *fContextReq* et *pfContextAttr* sont des masques de masques qui représentent différents attributs de contexte. Pour obtenir une description des différents attributs, consultez [spécifications de contexte](context-requirements.md).

> [!Note]  
> Tandis que le paramètre *pfContextAttr* est valide en cas de retour correct, vous devez examiner les indicateurs relatifs aux aspects de sécurité du contexte uniquement lors du retour final réussi. Les retours intermédiaires peuvent définir, par exemple, \_ l' \_ indicateur ISC RET allouée \_ Memory.

L’appelant est chargé de déterminer si les attributs de contexte finaux sont suffisants. Par exemple, si la confidentialité (chiffrement) a été demandée mais n’a pas pu être établie, certaines applications peuvent choisir d’arrêter immédiatement la connexion. Si le contexte de sécurité ne peut pas être établi, le serveur doit libérer le contexte partiellement créé en appelant la fonction [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) . Pour plus d’informations sur l’appel de la fonction **DeleteSecurityContext** , consultez **DeleteSecurityContext**.

Une fois le contexte de sécurité établi, l’application serveur peut utiliser la fonction [**QuerySecurityContextToken**](/windows/win32/api/sspi/nf-sspi-querysecuritycontexttoken) pour récupérer un handle vers le compte d’utilisateur auquel le certificat client a été mappé. En outre, le serveur peut utiliser la fonction [**ImpersonateSecurityContext**](/windows/win32/api/sspi/nf-sspi-impersonatesecuritycontext) pour emprunter l’identité de l’utilisateur.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|--------------------------|-------------------------------------------|
| Client minimal pris en charge | Applications de \[ Bureau Windows Vista uniquement\]       |
| Serveur minimal pris en charge | Applications de bureau Windows Server 2008 \[ uniquement\] |
| En-tête                   | SSPI. h (include Security. h)               |
| Bibliothèque                  | Secur32. lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Voir aussi

- [Fonctions SSPI](authentication-functions.md#sspi-functions)
- [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
- [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md)
