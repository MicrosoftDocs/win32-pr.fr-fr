---
description: Chiffre un message pour fournir la confidentialité à l’aide de Schannel.
ms.assetid: b02b38bd-f3dd-4bf8-a36e-44ff9fbbe550
title: EncryptMessage (SChannel) (fonction)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: de792e543a8cb67bd6b608d79832fd31a68267fc297a85e0e178d268bbc069d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008287"
---
# <a name="encryptmessage-schannel-function"></a>EncryptMessage (SChannel) (fonction)

La fonction **EncryptMessage (SChannel)** chiffre un message pour fournir la [*confidentialité*](../secgloss/p-gly.md). **EncryptMessage (SChannel)** permet à une application de choisir parmi les [*algorithmes de chiffrement*](../secgloss/c-gly.md) pris en charge par le mécanisme choisi. La fonction **EncryptMessage (SChannel)** utilise le [*contexte de sécurité*](../secgloss/s-gly.md) référencé par le handle de contexte. Certains packages n’ont pas de messages à chiffrer ou à déchiffrer, mais fournissent plutôt un [*hachage*](../secgloss/h-gly.md) d’intégrité qui peut être vérifié.

Lorsque vous utilisez le SSP Schannel, cette fonction chiffre les messages à l’aide d’une [*clé de session*](../secgloss/s-gly.md) négociée avec le tiers distant qui recevra le message. L’algorithme de chiffrement est déterminé par la suite de [ [*chiffrement*](../secgloss/c-gly.md)]([*cipher*](../secgloss/c-gly.md)-suites-in-schannel.md) en cours d’utilisation.

> [!Note]  
> **EncryptMessage (SChannel)** et [**DecryptMessage (SChannel)**](decryptmessage--schannel.md) peuvent être appelés en même temps à partir de deux threads différents dans un contexte SSPI ( [*Security Support Provider Interface*](../secgloss/s-gly.md) ) unique si un thread est en cours de chiffrement et que l’autre déchiffre. Si plusieurs threads chiffrent, ou si plusieurs threads déchiffrent, chaque thread doit obtenir un contexte unique.

## <a name="syntax"></a>Syntaxe

```C++
SECURITY_STATUS SEC_Entry EncryptMessage(
  _In_    PCtxtHandle    phContext,
  _In_    ULONG          fQOP,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo
);
```

## <a name="parameters"></a>Paramètres

*phContext* \[ dans\]

Handle du contexte de [*sécurité*](../secgloss/s-gly.md) à utiliser pour chiffrer le message.

*fQOP* \[ dans\]

Indicateurs spécifiques au package qui indiquent la qualité de la protection. Un [*package de sécurité*](../secgloss/s-gly.md) peut utiliser ce paramètre pour activer la sélection d' [*algorithmes de chiffrement*](../secgloss/c-gly.md).

Ce paramètre peut être l’indicateur suivant.

| Valeur                                                                                                                                                                                | Signification                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECQOP_WRAP_OOB_DATA"></span><span id="secqop_wrap_oob_data"></span><dl> <dt>**SECQOP \_ encapsuler les \_ \_ données OOB**</dt> </dl> | Envoyer un message d’alerte Schannel. Dans ce cas, le paramètre *pMessage* doit contenir un code d’événement SSL/TLS à deux octets standard. Cette valeur est prise en charge uniquement par le SSP Schannel.<br/> par exemple, à partir de Windows Vista, le message « server hello » envoyé par le serveur pendant le protocole de réauthentification doit être chiffré en tant qu’alerte TLS.<br/> |

*pMessage* \[ in, out\]

Pointeur vers une structure [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . En entrée, la structure fait référence à une ou plusieurs structures [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . L’une d’entre elles peut être de type SECBUFFER \_ Data. Cette mémoire tampon contient le message à chiffrer. Le message est chiffré sur place, remplaçant le contenu d’origine de la structure.

La fonction ne traite pas les tampons avec l' \_ attribut SECBUFFER ReadOnly.

La longueur de la structure [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) qui contient le message ne doit pas être supérieure à **cbMaximumMessage**, qui est obtenue à partir de la fonction [**QueryContextAttributes (SChannel)**](querycontextattributes--schannel.md) (SECPKG \_ attr \_ Stream \_ sizes).

*MessageSeqNo* \[ dans\]

Numéro de séquence que l’application de transport a affecté au message. Si l’application de transport ne conserve pas les numéros séquentiels, ce paramètre doit être égal à zéro.

Lorsque vous utilisez le SSP Schannel, ce paramètre doit avoir la valeur zéro. Le SSP Schannel n’utilise pas de numéros de séquence.

## <a name="return-value"></a>Valeur retournée

Si la fonction s’exécute correctement, la fonction retourne SEC \_ E \_ OK.

Si la fonction échoue, elle retourne l’un des codes d’erreur suivants.

| Code de retour                                                                                                    | Description                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_tampon s \_ E \_ trop \_ petit**</dt> </dl>      | La mémoire tampon de sortie est trop petite. Pour plus d'informations, consultez la section Notes.<br/>                                                                               |
| <dl> <dt>**\_contexte E/s \_ \_ expiré**</dt> </dl>        | L’application fait référence à un contexte qui a déjà été fermé. Une application correctement écrite ne doit pas recevoir cette erreur.<br/>             |
| <dl> <dt>**SEC \_ E \_ système de chiffrement \_ \_ non valide**</dt> </dl> | Le [*chiffrement*](../secgloss/c-gly.md) choisi pour le [*contexte de sécurité*](../secgloss/s-gly.md) n’est pas pris en charge.<br/>                       |
| <dl> <dt>**s \_ E \_ mémoire insuffisante \_**</dt> </dl>    | La mémoire disponible est insuffisante pour terminer l’action demandée.<br/>                                                                           |
| <dl> <dt>**SEC \_ E \_ handle non valide \_**</dt> </dl>         | Un descripteur de contexte non valide a été spécifié dans le paramètre *phContext* .<br/>                                                                   |
| <dl> <dt>**s \_ E \_ jeton non valide \_**</dt> </dl>          | Aucune \_ mémoire tampon de type de données SECBUFFER n’a été trouvée.<br/>                                                                                                        |
| <dl> <dt>**SEC \_ E \_ QoP \_ non \_ pris en charge**</dt> </dl>     | La confidentialité et l' [*intégrité*](../secgloss/i-gly.md) ne sont pas prises en charge par le [*contexte de sécurité*](../secgloss/s-gly.md).<br/> |

## <a name="remarks"></a>Remarques

La fonction **EncryptMessage (SChannel)** chiffre un message basé sur le message et la [*clé de session*](../secgloss/s-gly.md) à partir d’un contexte de [*sécurité*](../secgloss/s-gly.md).

Si l’application de transport a créé le [*contexte de sécurité*](../secgloss/s-gly.md) pour prendre en charge la détection de séquence et que l’appelant fournit un numéro de séquence, la fonction inclut ces informations avec le message chiffré. L’inclusion de ces informations protège la relecture, l’insertion et la suppression des messages. Le [*package de sécurité*](../secgloss/s-gly.md) intègre le numéro de séquence passé à partir de l’application de transport.

Lorsqu’il est utilisé avec le SSP Schannel, le paramètre *pMessage* doit contenir une structure [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) avec les mémoires tampons suivantes.

> [!Note]  
> Ces mémoires tampons doivent être fournies dans l’ordre indiqué.

| Type de mémoire tampon                | Description                                                                                                         |
|----------------------------|---------------------------------------------------------------------------------------------------------------------|
| \_ \_ en-tête de flux SECBUFFER  | Utilisé en interne. Aucune initialisation n’est requise.                                                                        |
| \_données SECBUFFER            | Contient le message de [*texte en clair*](../secgloss/s-gly.md) à chiffrer. |
| Code de fin de \_ flux SECBUFFER \_ | Utilisé en interne. Aucune initialisation n’est requise.                                                                        |
| SECBUFFER \_ vide           | Utilisé en interne. Aucune initialisation n’est requise. La taille peut être égale à zéro.                                                      |

Lorsque vous utilisez le SSP Schannel, déterminez la taille maximale de chacune des mémoires tampons en appelant la fonction [**QueryContextAttributes (SChannel)**](querycontextattributes--schannel.md) et en spécifiant l’attribut de tailles de flux de SECPKG \_ attr \_ \_ . Cette fonction retourne une [**structure \_ SecPkgContext StreamSizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_streamsizes) dont les membres contiennent les tailles maximales pour les mémoires tampons d’en-tête (membre **cbHeader** ), de message (membre **cbMaximumMessage** ) et de code de fin (membre **cbTrailer** ).

Pour des performances optimales, les structures *pMessage* doivent être allouées à partir de la mémoire contiguë.

**Windows XP/2000 :** Cette fonction était également connue sous le nom de **SealMessage**. Les applications doivent désormais utiliser **EncryptMessage (SChannel)** uniquement.

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
- [**AcceptSecurityContext (SChannel)**](acceptsecuritycontext--schannel.md)
- [**DecryptMessage (SChannel)**](decryptmessage--schannel.md)
- [**InitializeSecurityContext (SChannel)**](initializesecuritycontext--schannel.md)
- [**QueryContextAttributes (SChannel)**](querycontextattributes--schannel.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
