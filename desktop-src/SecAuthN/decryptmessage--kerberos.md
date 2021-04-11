---
description: Déchiffre un message à l’aide de Kerberos.
ms.assetid: 9e699f7c-f738-4702-bdef-fb2c276c38fc
title: DecryptMessage (Kerberos) (fonction)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: b32968ea83ca0403a5d8dd1579c4e03f30776c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113810"
---
# <a name="decryptmessage-kerberos-function"></a>DecryptMessage (Kerberos) (fonction)

La fonction **DecryptMessage (Kerberos)** déchiffre un message. Certains packages ne chiffrent et ne déchiffrent pas les messages, mais effectuent et vérifient plutôt un [*hachage*](../secgloss/h-gly.md)d’intégrité.

> [!Note]  
> [**EncryptMessage (Kerberos)**](encryptmessage--kerberos.md) et **DecryptMessage (Kerberos)** peuvent être appelés en même temps à partir de deux threads différents dans un contexte SSPI ( [*Security Support Provider Interface*](../secgloss/s-gly.md) ) unique si un thread est en cours de chiffrement et que l’autre déchiffre. Si plusieurs threads chiffrent, ou si plusieurs threads déchiffrent, chaque thread doit obtenir un contexte unique.

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

Handle du contexte de [*sécurité*](../secgloss/s-gly.md) à utiliser pour déchiffrer le message.

*pMessage* \[ in, out\]

Pointeur vers une structure [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . En entrée, la structure fait référence à une ou plusieurs structures [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) qui peuvent être de type SecBuffer \_ Data. La mémoire tampon contient le message chiffré. Le message chiffré est déchiffré sur place, remplaçant le contenu d’origine de sa mémoire tampon.

*MessageSeqNo* \[ dans\]

Numéro de séquence attendu par l’application de transport, le cas échéant. Si l’application de transport ne conserve pas les numéros séquentiels, ce paramètre doit avoir la valeur zéro.

*pfQOP* \[ à\]

Pointeur vers une variable de type **ULong** qui reçoit des indicateurs spécifiques au package qui indiquent la qualité de la protection.

Ce paramètre peut être l’indicateur suivant.

| Valeur                  | Signification                                                             |
|------------------------|---------------------------------------------------------------------|
| SECQOP_WRAP_NO_ENCRYPT | le message n’a pas été chiffré, mais un en-tête ou un code de fin a été créé. |

> [!NOTE]
> KERB_WRAP_NO_ENCRYPT a la même valeur et la même signification.

## <a name="return-value"></a>Valeur retournée

Si la fonction vérifie que le message a été reçu dans l’ordre correct, la fonction retourne SEC \_ E \_ OK.

Si la fonction ne parvient pas à déchiffrer le message, elle retourne l’un des codes d’erreur suivants.

| Code de retour                     | Description                                                                                                                                                                      |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **s \_ E \_ message incomplet \_** | Les données de la mémoire tampon d’entrée sont incomplètes. L’application doit lire plus de données à partir du serveur et appeler à nouveau [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md) . |
| **SEC \_ E \_ hors \_ \_ séquence**   | Le message n’a pas été reçu dans l’ordre correct.                                                                                                                            |

## <a name="remarks"></a>Notes

Parfois, une application lit les données du tiers distant, tente de les déchiffrer à l’aide de **DecryptMessage (Kerberos)** et découvre que **DecryptMessage (Kerberos)** a réussi, mais les tampons de sortie sont vides. Il s’agit d’un comportement normal, et les applications doivent être en mesure de les gérer.

Pour plus d’informations sur l’interopérabilité avec GSSAPI, consultez [interopérabilité SSPI/Kerberos avec GSSAPI](sspi-kerberos-interoperability-with-gssapi.md).

**Windows XP :** Cette fonction était également connue sous le nom de **UnsealMessage**. Les applications doivent désormais utiliser **DecryptMessage (Kerberos)** uniquement.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge | Applications de \[ Bureau Windows XP uniquement\]          |
| Serveur minimal pris en charge | Applications de bureau Windows Server 2003 \[ uniquement\] |
| En-tête                   | SSPI. h (include Security. h)               |
| Bibliothèque                  | Secur32. lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Voir aussi

- [Fonctions SSPI](authentication-functions.md#sspi-functions)
- [**EncryptMessage (Kerberos)**](encryptmessage--kerberos.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
