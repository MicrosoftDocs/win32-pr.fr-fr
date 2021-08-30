---
description: Déchiffre un message à l’aide de Negotiate.
ms.assetid: 188341ff-4e67-481e-af30-7f9913b1d24e
title: DecryptMessage (Negotiate) (fonction)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 5587b9faef4cbb44cfe8d30841de31ef1147e7ea
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468146"
---
# <a name="decryptmessage-negotiate-function"></a>DecryptMessage (Negotiate) (fonction)

La fonction **DecryptMessage (Negotiate)** déchiffre un message. Certains packages ne chiffrent et ne déchiffrent pas les messages, mais effectuent et vérifient plutôt un [*hachage*](../secgloss/h-gly.md)d’intégrité.

> [!Note]  
> [**EncryptMessage (Negotiate)**](encryptmessage--negotiate.md) et **DecryptMessage (Negotiate)** peuvent être appelés en même temps à partir de deux threads différents dans un contexte SSPI ( [*Security Support Provider Interface*](../secgloss/s-gly.md) ) unique si un thread chiffre et que l’autre déchiffre. Si plusieurs threads chiffrent, ou si plusieurs threads déchiffrent, chaque thread doit obtenir un contexte unique.

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

Pointeur vers une structure [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . En entrée, la structure fait référence à une ou plusieurs structures [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . Au moins une de ces données doit être de type SECBUFFER \_ . Cette mémoire tampon contient le message chiffré. Le message chiffré est déchiffré sur place, remplaçant le contenu d’origine de sa mémoire tampon.

*MessageSeqNo* \[ dans\]

Numéro de séquence attendu par l’application de transport, le cas échéant. Si l’application de transport ne conserve pas les numéros séquentiels, ce paramètre doit avoir la valeur zéro.

*pfQOP* \[ à\]

Pointeur vers une variable de type **ULong** qui reçoit des indicateurs spécifiques au package qui indiquent la qualité de la protection.

Ce paramètre peut être l’indicateur suivant.


| Valeur | Signification | 
|-------|---------|
| <span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt></dl> | Le message n’a pas été chiffré, mais un en-tête ou un code de fin a été créé.<br /><blockquote>[!Note]<br />KERB_WRAP_NO_ENCRYPT a la même valeur et la même signification.</blockquote><br /> | 


## <a name="return-value"></a>Valeur de retour

Si la fonction vérifie que le message a été reçu dans l’ordre correct, la fonction retourne SEC \_ E \_ OK.

Si la fonction ne parvient pas à déchiffrer le message, elle retourne l’un des codes d’erreur suivants.

| Code de retour                     | Description                                                                                                                                                                        |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **s \_ E \_ message incomplet \_** | Les données de la mémoire tampon d’entrée sont incomplètes. L’application doit lire plus de données à partir du serveur et appeler à nouveau [**DecryptMessage (Negotiate)**](decryptmessage--negotiate.md) . |
| **SEC \_ E \_ hors \_ \_ séquence**   | Le message n’a pas été reçu dans l’ordre correct.                                                                                                                              |

## <a name="remarks"></a>Remarques

Parfois, une application lit les données du tiers distant, tente de les déchiffrer à l’aide de **DecryptMessage (Negotiate)** et découvre que **DecryptMessage (Negotiate)** a réussi, mais les mémoires tampons de sortie sont vides. Il s’agit d’un comportement normal, et les applications doivent être en mesure de les gérer.

**Windows XP :** Cette fonction était également connue sous le nom de **UnsealMessage**. Les applications doivent désormais utiliser **DecryptMessage (Negotiate)** uniquement.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge | Windows \[Applications de bureau XP uniquement\]          |
| Serveur minimal pris en charge | Windows Serveur 2003 \[ applications de bureau uniquement\] |
| En-tête                   | SSPI. h (include Security. h)               |
| Bibliothèque                  | Secur32. lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Voir aussi

- [Fonctions SSPI](authentication-functions.md#sspi-functions)
- [**EncryptMessage (Negotiate)**](encryptmessage--negotiate.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
