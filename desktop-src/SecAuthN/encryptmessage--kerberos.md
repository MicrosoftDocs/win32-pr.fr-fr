---
description: Chiffre un message pour fournir la confidentialité à l’aide de Kerberos.
ms.assetid: b9b6ca95-b986-4de7-bd28-994a5125ad05
title: EncryptMessage (Kerberos) (fonction)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 89c6504fe8518e1c43d155ebce638dec1acfeb80
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476215"
---
# <a name="encryptmessage-kerberos-function"></a>EncryptMessage (Kerberos) (fonction)

La fonction **EncryptMessage (Kerberos)** chiffre un message pour fournir la [*confidentialité*](../secgloss/p-gly.md). **EncryptMessage (Kerberos)** permet à une application de choisir parmi les [*algorithmes de chiffrement*](../secgloss/c-gly.md) pris en charge par le mécanisme choisi. La fonction **EncryptMessage (Kerberos)** utilise le [*contexte de sécurité*](../secgloss/s-gly.md) référencé par le handle de contexte. Certains packages n’ont pas de messages à chiffrer ou à déchiffrer, mais fournissent plutôt un [*hachage*](../secgloss/h-gly.md) d’intégrité qui peut être vérifié.

> [!Note]  
> **EncryptMessage (Kerberos)** et [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md) peuvent être appelés en même temps à partir de deux threads différents dans un contexte SSPI ( [*Security Support Provider Interface*](../secgloss/s-gly.md) ) unique si un thread est en cours de chiffrement et que l’autre déchiffre. Si plusieurs threads chiffrent, ou si plusieurs threads déchiffrent, chaque thread doit obtenir un contexte unique.

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

<dl> <dt>

*phContext* \[ dans\]
</dt> <dd>

Handle du contexte de [*sécurité*](../secgloss/s-gly.md) à utiliser pour chiffrer le message.

</dd> <dt>

*fQOP* \[ dans\]
</dt> <dd>

Indicateurs spécifiques au package qui indiquent la qualité de la protection. Un [*package de sécurité*](../secgloss/s-gly.md) peut utiliser ce paramètre pour activer la sélection d' [*algorithmes de chiffrement*](../secgloss/c-gly.md).

Ce paramètre peut être l’indicateur suivant.


| Valeur | Signification | 
|-------|---------|
| <span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt></dl> | Générez un en-tête ou un code de fin, mais ne chiffrez pas le message.<br /><blockquote>[!Note]<br />KERB_WRAP_NO_ENCRYPT a la même valeur et la même signification.</blockquote><br /> | 


</dd> <dt>

*pMessage* \[ in, out\]
</dt> <dd>

Pointeur vers une structure [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . En entrée, la structure fait référence à une ou plusieurs structures [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) qui peuvent être de type SecBuffer \_ . Cette mémoire tampon contient le message à chiffrer. Le message est chiffré sur place, remplaçant le contenu d’origine de la structure.

La fonction ne traite pas les tampons avec l' \_ attribut SECBUFFER ReadOnly.

La longueur de la structure [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) qui contient le message ne doit pas être supérieure à **cbMaximumMessage**, qui est obtenue à partir de la fonction [**QueryContextAttributes (Kerberos)**](querycontextattributes--kerberos.md) (SECPKG \_ attr \_ Stream \_ sizes).

Les applications qui n’utilisent pas SSL doivent fournir un [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) de type SecBuffer \_ Padding.

</dd> <dt>

*MessageSeqNo* \[ dans\]
</dt> <dd>

Numéro de séquence que l’application de transport a affecté au message. Si l’application de transport ne conserve pas les numéros séquentiels, ce paramètre doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction s’exécute correctement, la fonction retourne SEC \_ E \_ OK.

Si la fonction échoue, elle retourne l’un des codes d’erreur suivants.

| Code de retour                                                                                                    | Description                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_tampon s \_ E \_ trop \_ petit**</dt> </dl>      | La mémoire tampon de sortie est trop petite. Pour plus d'informations, consultez la section Notes.                                                                                                                                                                 |
| <dl> <dt>**\_contexte E/s \_ \_ expiré**</dt> </dl>        | L’application fait référence à un contexte qui a déjà été fermé. Une application correctement écrite ne doit pas recevoir cette erreur.                                                                                               |
| <dl> <dt>**SEC \_ E \_ système de chiffrement \_ \_ non valide**</dt> </dl> | Le [*chiffrement*](../secgloss/c-gly.md) choisi pour le [*contexte de sécurité*](../secgloss/s-gly.md) n’est pas pris en charge.                                                                                                         |
| <dl> <dt>**s \_ E \_ mémoire insuffisante \_**</dt> </dl>    | La mémoire disponible est insuffisante pour terminer l’action demandée.                                                                                                                                                             |
| <dl> <dt>**SEC \_ E \_ handle non valide \_**</dt> </dl>         | Un descripteur de contexte non valide a été spécifié dans le paramètre *phContext* .                                                                                                                                                     |
| <dl> <dt>**s \_ E \_ jeton non valide \_**</dt> </dl>          | Aucune \_ mémoire tampon de type de données SECBUFFER n’a été trouvée.                                                                                                                                                                                          |
| <dl> <dt>**SEC \_ E \_ QoP \_ non \_ pris en charge**</dt> </dl>     | La confidentialité et l' [*intégrité*](../secgloss/i-gly.md) ne sont pas prises en charge par le [*contexte de sécurité*](../secgloss/s-gly.md). |

## <a name="remarks"></a>Remarques

La fonction **EncryptMessage (Kerberos)** chiffre un message basé sur le message et la [*clé de session*](../secgloss/s-gly.md) à partir d’un contexte de [*sécurité*](../secgloss/s-gly.md).

Si l’application de transport a créé le [*contexte de sécurité*](../secgloss/s-gly.md) pour prendre en charge la détection de séquence et que l’appelant fournit un numéro de séquence, la fonction inclut ces informations avec le message chiffré. L’inclusion de ces informations protège la relecture, l’insertion et la suppression des messages. Le [*package de sécurité*](../secgloss/s-gly.md) intègre le numéro de séquence passé à partir de l’application de transport.

> [!Note]  
> Ces mémoires tampons doivent être fournies dans l’ordre indiqué.

| Type de mémoire tampon                           | Description                                                                                                                    |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| \_ \_< en-tête de flux SECBUFFER  | Utilisé en interne. Aucune initialisation n’est requise.                                                                       |
| \_données SECBUFFER            | Contient le message de [*texte en clair*](../secgloss/s-gly.md) à chiffrer. |
| Code de fin de \_ flux SECBUFFER \_ | Utilisé en interne. Aucune initialisation n’est requise.                                                                        |
| SECBUFFER \_ vide           | Utilisé en interne. Aucune initialisation n’est requise. La taille peut être égale à zéro.                                                      |

Pour des performances optimales, les structures *pMessage* doivent être allouées à partir de la mémoire contiguë.

**Windows XP :** Cette fonction était également connue sous le nom de **SealMessage**. Les applications doivent désormais utiliser **EncryptMessage (Kerberos)** uniquement.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|--------------------------|-------------------------------------------|
| Client minimal pris en charge | Windows \[Applications de bureau XP uniquement\]          |
| Serveur minimal pris en charge | Windows Serveur 2003 \[ applications de bureau uniquement\] |
| En-tête                   | SSPI. h (include Security. h)               |
| Bibliothèque                  | Secur32. lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md)
</dt> <dt>

[**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md)
</dt> <dt>

[**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md)
</dt> <dt>

[**QueryContextAttributes (Kerberos)**](querycontextattributes--kerberos.md)
</dt> <dt>

[**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>
