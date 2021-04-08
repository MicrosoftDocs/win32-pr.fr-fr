---
description: Déchiffre un message à l’aide de Schannel.
ms.assetid: 5d7c8598-2d6b-4839-ae98-dff964bc962c
title: DecryptMessage (SChannel) (fonction)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 6bfbb354be9f3553e5369b8ce1f8b4260eab8ee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750044"
---
# <a name="decryptmessage-schannel-function"></a>DecryptMessage (SChannel) (fonction)

La fonction **DecryptMessage (SChannel)** déchiffre un message. Certains packages ne chiffrent et ne déchiffrent pas les messages, mais effectuent et vérifient plutôt un [*hachage*](../secgloss/h-gly.md)d’intégrité.


Cette fonction est également utilisée avec le fournisseur SSP ( [*Security Support Provider*](../secgloss/s-gly.md#_SECURITY_SECURITY_SUPPORT_PROVIDER_GLY) ) Schannel pour signaler une demande de la part d’un expéditeur de message pour une renégociation (rétablissement) des attributs de connexion ou pour l’arrêt de la connexion.

> [!Note]  
> [**EncryptMessage (SChannel)**](encryptmessage--schannel.md) et **DecryptMessage (SChannel)** peuvent être appelés en même temps à partir de deux threads différents dans un contexte SSPI ( [*Security Support Provider Interface*](../secgloss/s-gly.md#_SECURITY_SECURITY_SUPPORT_PROVIDER_INTERFACE_GLY) ) unique si un thread est en cours de chiffrement et que l’autre déchiffre. Si plusieurs threads chiffrent, ou si plusieurs threads déchiffrent, chaque thread doit obtenir un contexte unique.


## <a name="syntax"></a>Syntaxe

```C++
SECURITY_STATUS SEC_Entry DecryptMessage(
  _In_    PCtxtHandle    phContext,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo,
  _Out_   PULONG         pfQOP
);
```

## <a name="parameters"></a>Paramètres

*phContext* \[ dans\]


Handle du contexte de [*sécurité*](../secgloss/s-gly.md#_SECURITY_SECURITY_CONTEXT_GLY) à utiliser pour déchiffrer le message.

*pMessage* \[ in, out\]

Pointeur vers une structure [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . En entrée, la structure fait référence à une ou plusieurs structures [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . L’une d’entre elles peut être de type SECBUFFER \_ Data. Cette mémoire tampon contient le message chiffré. Le message chiffré est déchiffré sur place, remplaçant le contenu d’origine de sa mémoire tampon.

Lorsque vous utilisez le SSP Schannel avec des contextes qui ne sont pas orientés connexion, la structure doit contenir quatre structures [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . Une seule mémoire tampon doit être de type SECBUFFER \_ Data et contenir un message chiffré, qui est déchiffré sur place. Les mémoires tampons restantes sont utilisées pour la sortie et doivent être de type SECBUFFER \_ vide. Pour les contextes orientés connexion, un \_ tampon de type de données SECBUFFER doit être fourni, comme indiqué pour les contextes non orientés connexion. En outre, un deuxième tampon de type de jeton SECBUFFER contenant \_ un jeton de sécurité doit également être fourni.

*MessageSeqNo* \[ dans\]

Numéro de séquence attendu par l’application de transport, le cas échéant. Si l’application de transport ne conserve pas les numéros séquentiels, ce paramètre doit avoir la valeur zéro.

Lorsque vous utilisez le SSP Schannel, ce paramètre doit avoir la valeur zéro. Le SSP Schannel n’utilise pas de numéros de séquence.

*pfQOP* \[ à\]

Pointeur vers une variable de type **ULong** qui reçoit des indicateurs spécifiques au package qui indiquent la qualité de la protection.

Lorsque vous utilisez le SSP Schannel, ce paramètre n’est pas utilisé et doit avoir la valeur **null**.

Ce paramètre peut être l’indicateur suivant.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Valeur</th><th>Signification</th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </dl></td><td>Le message n’a pas été chiffré, mais un en-tête ou un code de fin a été créé.<br/><blockquote>[!Note]<br />
KERB_WRAP_NO_ENCRYPT a la même valeur et la même signification.</blockquote><br/></td></tr></tbody></table>

## <a name="return-value"></a>Valeur retournée

Si la fonction vérifie que le message a été reçu dans l’ordre correct, la fonction retourne SEC \_ E \_ OK.

Si la fonction ne parvient pas à déchiffrer le message, elle retourne l’un des codes d’erreur suivants.

| Code de retour                     | Description                                                                                                    |
|---------------------------------|----------------------------------------------------------------------------------------------------------------|
| **SEC \_ E \_ handle non valide \_**     | Un descripteur de contexte non valide a été spécifié dans le paramètre *phContext* . Utilisé avec le SSP Schannel.     |
| **s \_ E \_ jeton non valide \_**      | Les mémoires tampons sont de type incorrect ou aucune mémoire tampon de type SECBUFFER \_ Data n’a été trouvée. Utilisé avec le SSP Schannel.  |
| **s \_ \_ message électronique \_ modifié**    | Le message a été modifié. Utilisé avec le SSP Schannel.                                                      |
| **SEC \_ E \_ hors \_ \_ séquence**   | Le message n’a pas été reçu dans l’ordre correct.                                                          |
| **le \_ contexte sec I \_ \_ a expiré**    | L’expéditeur du message a fini d’utiliser la connexion et a lancé un arrêt. Pour plus d’informations sur l’initialisation ou la reconnaissance d’un arrêt, consultez [arrêt d’une connexion Schannel](shutting-down-an-schannel-connection.md). Utilisé avec le SSP Schannel. |
| **s \_ je \_ renégocie**         | Le tiers distant requiert une nouvelle séquence de négociation ou l’application vient d’initier un arrêt. Revenez à la boucle de négociation et appelez [**AcceptSecurityContext (SChannel)**](acceptsecuritycontext--schannel.md) ou [**InitializeSecurityContext (schannel)**](initializesecuritycontext--schannel.md), SECBUFFER_EXTRA retournée à partir de DecryptMessage (). La renégociation n’est pas prise en charge pour le mode noyau Schannel. L’appelant doit soit ignorer cette valeur de retour, soit arrêter la connexion. Si la valeur est ignorée, le client ou le serveur peut arrêter la connexion en conséquence. |


## <a name="remarks"></a>Notes

Parfois, une application lit les données du tiers distant, tente de les déchiffrer à l’aide de **DecryptMessage (SChannel)** et découvre que **DecryptMessage (SChannel)** a réussi, mais les mémoires tampons de sortie sont vides. Il s’agit d’un comportement normal, et les applications doivent être en mesure de les gérer.

Lorsque vous utilisez le SSP Schannel, la fonction [**DecryptMessage (General)**](decryptmessage--general.md) retourne le \_ contexte sec I \_ \_ expiré lorsque l’expéditeur du message a arrêté la connexion. Pour plus d’informations sur l’initialisation ou la reconnaissance d’un arrêt, consultez [arrêt d’une connexion Schannel](shutting-down-an-schannel-connection.md).

Si vous utilisez TLS 1,0, vous devrez peut-être appeler cette fonction plusieurs fois, en ajustant la mémoire tampon d’entrée sur chaque appel, afin de déchiffrer l’intégralité d’un message.


La fonction **DecryptMessage (SChannel)** renvoie sec \_ I \_ renégociée lorsque l’expéditeur du message souhaite renégocier la connexion ([*contexte de sécurité*](../secgloss/s-gly.md)). Une application gère une renégociation demandée en appelant [**AcceptSecurityContext (SChannel)**](acceptsecuritycontext--schannel.md) (côté serveur) ou [**InitializeSecurityContext (SChannel)**](initializesecuritycontext--schannel.md) (côté client) et passe SECBUFFER_EXTRA retournée à partir de DecryptMessage (). Après que cet appel initial a retourné une valeur, procédez comme si votre application était en train de créer une nouvelle connexion. Pour plus d’informations, consultez [création d’un contexte de sécurité Schannel](creating-an-schannel-security-context.md).


## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|--------------------------|-------------------------------------------|
| Client minimal pris en charge | Applications de \[ Bureau Windows XP uniquement\]          |
| Serveur minimal pris en charge | Applications de bureau Windows Server 2003 \[ uniquement\] |
| En-tête                   | SSPI. h (include Security. h)               |
| Bibliothèque                  | Secur32. lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Voir aussi

- [Fonctions SSPI](authentication-functions.md#sspi-functions)
- [**EncryptMessage (SChannel)**](encryptmessage--schannel.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
