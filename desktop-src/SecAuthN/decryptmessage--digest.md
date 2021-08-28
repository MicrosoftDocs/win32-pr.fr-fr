---
description: Déchiffre un message à l’aide de Digest.
ms.assetid: 46d45f59-33fa-434a-b329-20b6257c9a19
title: DecryptMessage (Digest) (fonction)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: f87828263766643a10cf5400e38cabe9d3096403
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480865"
---
# <a name="decryptmessage-digest-function"></a>DecryptMessage (Digest) (fonction)

La fonction **DecryptMessage (Digest)** déchiffre un message. Certains packages ne chiffrent et ne déchiffrent pas les messages, mais effectuent et vérifient plutôt un [*hachage*](../secgloss/h-gly.md)d’intégrité.

Le fournisseur SSP ( [*Security Support Provider*](../secgloss/s-gly.md) ) de Digest fournit la confidentialité de chiffrement et de déchiffrement pour les messages échangés entre le client et le serveur en tant que mécanisme SASL uniquement.

> [!Note]  
> [**EncryptMessage (Digest)**](encryptmessage--digest.md) et **DecryptMessage (Digest)** peuvent être appelés en même temps à partir de deux threads différents dans un contexte SSPI ( [*Security Support Provider Interface*](../secgloss/s-gly.md) ) unique si un thread est en cours de chiffrement et que l’autre déchiffre. Si plusieurs threads chiffrent, ou si plusieurs threads déchiffrent, chaque thread doit obtenir un contexte unique.

## <a name="syntax"></a>Syntaxe

```C++
SECURITY_STATUS SEC_ENTRY DecryptMessage(
  PCtxtHandle    phContext,
  PSecBufferDesc pMessage,
  unsigned long  MessageSeqNo,
  unsigned long  *pfQOP
);
```

## <a name="parameters"></a>Paramètres

*phContext* \[ dans\]

Handle du contexte de [*sécurité*](../secgloss/s-gly.md) à utiliser pour déchiffrer le message.

*pMessage* \[ in, out\]

Pointeur vers une structure [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . En entrée, la structure fait référence à une ou plusieurs structures [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . Au moins une de ces données doit être de type SECBUFFER \_ . Cette mémoire tampon contient le message chiffré. Le message chiffré est déchiffré sur place, remplaçant le contenu d’origine de sa mémoire tampon.

Lors de l’utilisation du SSP Digest, en entrée, la structure fait référence à une ou plusieurs structures [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . L’un d’eux doit être de type SECBUFFER \_ Data ou SECBUFFER \_ Stream, et il doit contenir le message chiffré.

*MessageSeqNo* \[ dans\]

Numéro de séquence attendu par l’application de transport, le cas échéant. Si l’application de transport ne conserve pas les numéros séquentiels, ce paramètre doit avoir la valeur zéro.

Lorsque vous utilisez le SSP Digest, ce paramètre doit avoir la valeur zéro. Le SSP Digest gère la numérotation des séquences en interne.

*pfQOP* \[ à\]

Pointeur vers une variable de type **ULong** qui reçoit des indicateurs spécifiques au package qui indiquent la qualité de la protection.

Ce paramètre peut être l’un des indicateurs suivants.


| Valeur | Signification | 
|-------|---------|
| <span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt></dl> | Le message n’a pas été chiffré, mais un en-tête ou un code de fin a été créé.<br /><blockquote>[!Note]<br />KERB_WRAP_NO_ENCRYPT a la même valeur et la même signification.</blockquote><br /> | 
| <span id="SIGN_ONLY_"></span><span id="sign_only_"></span><dl><dt><strong>SIGN_ONLY</strong></dt></dl> | Lorsque vous utilisez le SSP Digest, utilisez cet indicateur lorsque le [*contexte de sécurité*](../secgloss/s-gly.md) est défini pour vérifier la [*signature*](../secgloss/s-gly.md) uniquement. Pour plus d’informations, consultez [Quality of protection](quality-of-protection.md).<br /> | 


## <a name="return-value"></a>Valeur de retour

Si la fonction vérifie que le message a été reçu dans l’ordre correct, la fonction retourne SEC \_ E \_ OK.

Si la fonction ne parvient pas à déchiffrer le message, elle retourne l’un des codes d’erreur suivants.

| Code de retour                         | Description                                                                                                                                                                  |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_tampon s \_ E \_ trop \_ petit**      | La mémoire tampon des messages est trop petite. Utilisé avec le SSP Digest.                                                                                                                   |
| **SEC \_ E \_ système de chiffrement \_ \_ non valide** | Le [*chiffrement*](../secgloss/c-gly.md) choisi pour le [*contexte de sécurité*](../secgloss/s-gly.md) n’est pas pris en charge. Utilisé avec le SSP Digest.                                                                                       |
| **s \_ E \_ message incomplet \_**     | Les données de la mémoire tampon d’entrée sont incomplètes. L’application doit lire plus de données à partir du serveur et appeler de nouveau [**DecryptMessage (Digest)**](decryptmessage--digest.md) . |
| **SEC \_ E \_ handle non valide \_**         | Un descripteur de contexte non valide a été spécifié dans le paramètre *phContext* . Utilisé avec le SSP Digest.                                                                     |
| **s \_ \_ message électronique \_ modifié**        | Le message a été modifié. Utilisé avec le SSP Digest.                                                                                                                      |
| **SEC \_ E \_ hors \_ \_ séquence**       | Le message n’a pas été reçu dans l’ordre correct.                                                                                                                        |
| **SEC \_ E \_ QoP \_ non \_ pris en charge**     | La confidentialité et l' [*intégrité*](../secgloss/i-gly.md) ne sont pas prises en charge par le [*contexte de sécurité*](../secgloss/s-gly.md). Utilisé avec le SSP Digest.                           |

## <a name="remarks"></a>Remarques

Parfois, une application lit les données du tiers distant, tente de les déchiffrer à l’aide de **DecryptMessage (Digest)** et découvre que **DecryptMessage (Digest)** a réussi, mais les tampons de sortie sont vides. Il s’agit d’un comportement normal, et les applications doivent être en mesure de les gérer.

**Windows XP :** Cette fonction était également connue sous le nom de **UnsealMessage**. Les applications doivent désormais utiliser **DecryptMessage (Digest)** uniquement.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|--------------------------|-------------------------------------------|
| Client minimal pris en charge | Windows \[Applications de bureau XP uniquement\]          |
| Serveur minimal pris en charge | Windows Serveur 2003 \[ applications de bureau uniquement\] |
| En-tête                   | SSPI. h (include Security. h)               |
| Bibliothèque                  | Secur32. lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Voir aussi

- [Fonctions SSPI](authentication-functions.md#sspi-functions)
- [**EncryptMessage (Digest)**](encryptmessage--digest.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
