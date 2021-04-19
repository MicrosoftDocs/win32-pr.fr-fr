---
description: Chiffre un message pour fournir la confidentialité.
ms.assetid: 2e09f262-9c3e-4db2-9285-017f5e1810c7
title: EncryptMessage (général), fonction (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 3c661f5f529700db19683966783c1aa0793e376b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514784"
---
# <a name="encryptmessage-general-function"></a>EncryptMessage (général) (fonction)

La fonction **EncryptMessage (général)** chiffre un message pour fournir la [*confidentialité*](../secgloss/p-gly.md). **EncryptMessage (général)** permet à une application de choisir parmi les [*algorithmes de chiffrement*](../secgloss/c-gly.md) pris en charge par le mécanisme choisi. La fonction **EncryptMessage (General)** utilise le [*contexte de sécurité*](../secgloss/s-gly.md) référencé par le handle de contexte. Certains packages n’ont pas de messages à chiffrer ou à déchiffrer, mais fournissent plutôt un [*hachage*](../secgloss/h-gly.md) d’intégrité qui peut être vérifié.

Lorsque vous utilisez le [*fournisseur SSP (Security Support Provider*](../secgloss/s-gly.md) ) Digest, cette fonction est uniquement disponible en tant que mécanisme SASL.

Lorsque vous utilisez le SSP Schannel, cette fonction chiffre les messages à l’aide d’une [*clé de session*](../secgloss/s-gly.md) négociée avec le tiers distant qui recevra le message. L’algorithme de chiffrement est déterminé par la suite de [ [*chiffrement*](../secgloss/c-gly.md)]([*cipher*](../secgloss/c-gly.md)-suites-in-schannel.md) en cours d’utilisation.

> [!Note]  
> **EncryptMessage (General)** et [**DecryptMessage (General)**](decryptmessage--general.md) peuvent être appelés en même temps à partir de deux threads différents dans un contexte SSPI ( [*Security Support Provider Interface*](../secgloss/s-gly.md) ) unique si un thread est en cours de chiffrement et que l’autre déchiffre. Si plusieurs threads chiffrent, ou si plusieurs threads déchiffrent, chaque thread doit obtenir un contexte unique.

Pour plus d’informations sur l’utilisation de cette fonction avec un fournisseur de services partagés spécifique, consultez les rubriques suivantes.

| Rubrique                                                            | Description                                               |
|------------------------------------------------------------------|-----------------------------------------------------------|
| [**EncryptMessage (Digest)**](encryptmessage--digest.md)       | Chiffre un message pour fournir la confidentialité à l’aide de Digest.    |
| [**EncryptMessage (Kerberos)**](encryptmessage--kerberos.md)   | Chiffre un message pour fournir la confidentialité à l’aide de Kerberos.  |
| [**EncryptMessage (Negotiate)**](encryptmessage--negotiate.md) | Chiffre un message pour fournir la confidentialité en utilisant Negotiate. |
| [**EncryptMessage (NTLM)**](encryptmessage--ntlm.md)           | Chiffre un message pour fournir la confidentialité à l’aide de NTLM.      |
| [**EncryptMessage (SChannel)**](encryptmessage--schannel.md)   | Chiffre un message pour fournir la confidentialité à l’aide de Schannel.  |

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

Lorsque vous utilisez le SSP Digest, ce paramètre doit avoir la valeur zéro.

Ce paramètre peut être l’un des indicateurs suivants.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Valeur</th><th>Signification</th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </dl></td><td>Générez un en-tête ou un code de fin, mais ne chiffrez pas le message.<br/><blockquote>[!Note]<br />
KERB_WRAP_NO_ENCRYPT a la même valeur et la même signification.</blockquote><br/></td></tr><tr class="even"><td><span id="SECQOP_WRAP_OOB_DATA"></span><span id="secqop_wrap_oob_data"></span><dl> <dt><strong>SECQOP_WRAP_OOB_DATA</strong></dt> </dl></td><td>Envoyer un message d’alerte Schannel. Dans ce cas, le paramètre <em>pMessage</em> doit contenir un code d’événement SSL/TLS à deux octets standard. Cette valeur est prise en charge uniquement par le SSP Schannel.<br/></td></tr></tbody></table>

*pMessage* \[ in, out\]

Pointeur vers une structure [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . En entrée, la structure fait référence à une ou plusieurs structures [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . L’une d’entre elles peut être de type SECBUFFER \_ Data. Cette mémoire tampon contient le message à chiffrer. Le message est chiffré sur place, remplaçant le contenu d’origine de la structure.

La fonction ne traite pas les tampons avec l' \_ attribut SECBUFFER ReadOnly.

La longueur de la structure [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) qui contient le message ne doit pas être supérieure à **cbMaximumMessage**, qui est obtenue à partir de la fonction [**QueryContextAttributes (général)**](querycontextattributes--general.md) (SECPKG \_ attr \_ Stream \_ sizes).

Lorsque vous utilisez le SSP Digest, il doit exister une deuxième mémoire tampon de type SECBUFFER \_ padding ou \_ sec \_ Data buffer pour contenir les informations de [*signature*](../secgloss/d-gly.md#_security_digital_signature_gly) . Pour obtenir la taille de la mémoire tampon de sortie, appelez la fonction [**QueryContextAttributes (General)**](querycontextattributes--general.md) et spécifiez des \_ tailles d’attr SECPKG \_ . La fonction retourne une structure [**de \_ tailles SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) . La taille de la mémoire tampon de sortie est la somme des valeurs des membres **cbMaxSignature** et **cbBlockSize** .

Les applications qui n’utilisent pas SSL doivent fournir un [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) de type SecBuffer \_ Padding.

*MessageSeqNo* \[ dans\]

Numéro de séquence que l’application de transport a affecté au message. Si l’application de transport ne conserve pas les numéros séquentiels, ce paramètre doit être égal à zéro.

Lorsque vous utilisez le SSP Digest, ce paramètre doit avoir la valeur zéro. Le SSP Digest gère la numérotation des séquences en interne.

Lorsque vous utilisez le SSP Schannel, ce paramètre doit avoir la valeur zéro. Le SSP Schannel n’utilise pas de numéros de séquence.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction s’exécute correctement, la fonction retourne SEC \_ E \_ OK.

Si la fonction échoue, elle retourne l’un des codes d’erreur suivants.

| Code de retour                         | Description                                                                                                                                                                 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_tampon s \_ E \_ trop \_ petit**      | La mémoire tampon de sortie est trop petite. Pour plus d'informations, consultez la section Notes.                                                                                                          |
| **\_contexte E/s \_ \_ expiré**        | L’application fait référence à un contexte qui a déjà été fermé. Une application correctement écrite ne doit pas recevoir cette erreur.                                        |
| **SEC \_ E \_ système de chiffrement \_ \_ non valide** | Le [*chiffrement*](../secgloss/c-gly.md) choisi pour le [*contexte de sécurité*](../secgloss/s-gly.md) n’est pas pris en charge.                                                                       |
| **s \_ E \_ mémoire insuffisante \_**    | La mémoire disponible est insuffisante pour terminer l’action demandée.                                                                                                      |
| **SEC \_ E \_ handle non valide \_**         | Un descripteur de contexte non valide a été spécifié dans le paramètre *phContext* .                                                                                              |
| **s \_ E \_ jeton non valide \_**          | Aucune \_ mémoire tampon de type de données SECBUFFER n’a été trouvée.                                                                                                                                   |
| **SEC \_ E \_ QoP \_ non \_ pris en charge**     | La confidentialité et l' [*intégrité*](../secgloss/i-gly.md) ne sont pas prises en charge par le [*contexte de sécurité*](../secgloss/s-gly.md). |

## <a name="remarks"></a>Notes

La fonction **EncryptMessage (général)** chiffre un message basé sur le message et la [*clé de session*](../secgloss/s-gly.md) à partir d’un contexte de [*sécurité*](../secgloss/s-gly.md).

Si l’application de transport a créé le [*contexte de sécurité*](../secgloss/s-gly.md) pour prendre en charge la détection de séquence et que l’appelant fournit un numéro de séquence, la fonction inclut ces informations avec le message chiffré. L’inclusion de ces informations protège la relecture, l’insertion et la suppression des messages. Le [*package de sécurité*](../secgloss/s-gly.md) intègre le numéro de séquence passé à partir de l’application de transport.

Lorsque vous utilisez le SSP Digest, récupérez la taille de la mémoire tampon de sortie en appelant la fonction [**QueryContextAttributes (General)**](querycontextattributes--general.md) et en spécifiant des \_ tailles d’attr SECPKG \_ . La fonction retourne une structure [**de \_ tailles SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) . La taille de la mémoire tampon de sortie est la somme des valeurs des membres **cbMaxSignature** et **cbBlockSize** .

Lorsqu’il est utilisé avec le SSP Schannel, le paramètre *pMessage* doit contenir une structure [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) avec les mémoires tampons suivantes.

> [!Note]  
> Ces mémoires tampons doivent être fournies dans l’ordre indiqué.

| Type de mémoire tampon                | Description                                                                                 |
|----------------------------|---------------------------------------------------------------------------------------------|
| \_ \_ en-tête de flux SECBUFFER  | Utilisé en interne. Aucune initialisation n’est requise.                                                |
| \_données SECBUFFER            | Contient le message de [*texte en clair*](../secgloss/s-gly.md) à chiffrer. |
| Code de fin de \_ flux SECBUFFER \_ | Utilisé en interne. Aucune initialisation n’est requise.                                                |
| SECBUFFER \_ vide           | Utilisé en interne. Aucune initialisation n’est requise. La taille peut être égale à zéro.                              |

Lorsque vous utilisez le SSP Schannel, déterminez la taille maximale de chacune des mémoires tampons en appelant la fonction [**QueryContextAttributes (General)**](querycontextattributes--general.md) et en spécifiant l' \_ attribut de tailles de flux attr SECPKG \_ \_ . Cette fonction retourne une [**structure \_ SecPkgContext StreamSizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_streamsizes) dont les membres contiennent les tailles maximales pour les mémoires tampons d’en-tête (membre **cbHeader** ), de message (membre **cbMaximumMessage** ) et de code de fin (membre **cbTrailer** ).

Pour des performances optimales, les structures *pMessage* doivent être allouées à partir de la mémoire contiguë.

**Windows XP/2000 :** Cette fonction était également connue sous le nom de **SealMessage**. Les applications doivent désormais utiliser **EncryptMessage (général)** uniquement.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge | Applications de \[ Bureau Windows XP uniquement\]                                                            |
| Serveur minimal pris en charge | Applications de bureau Windows Server 2003 \[ uniquement\]                                                   |
| En-tête                   | <dl> <dt>SSPI. h (include Security. h)</dt> </dl> |
| Bibliothèque                  | <dl> <dt>Secur32. lib</dt> </dl>                 |
| DLL                      | <dl> <dt>Secur32.dll</dt> </dl>                 |

## <a name="see-also"></a>Voir aussi

- [Fonctions SSPI](authentication-functions.md#sspi-functions)
- [**AcceptSecurityContext (général)**](acceptsecuritycontext--general.md)
- [**DecryptMessage (général)**](decryptmessage--general.md)
- [**InitializeSecurityContext (général)**](initializesecuritycontext--general.md)
- [**QueryContextAttributes (général)**](querycontextattributes--general.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
