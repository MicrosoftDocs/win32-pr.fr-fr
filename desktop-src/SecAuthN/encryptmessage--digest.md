---
description: Chiffre un message pour fournir la confidentialité à l’aide de Digest.
ms.assetid: 0045e931-929b-40c4-a524-5664d2fc5170
title: EncryptMessage (Digest), fonction (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: af16238ca58449c286edd9eabb88d7bc9a3f7fa781fac360863fdd52f7296833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008427"
---
# <a name="encryptmessage-digest-function"></a>EncryptMessage (Digest) (fonction)

La fonction **EncryptMessage (Digest)** chiffre un message pour fournir la [*confidentialité*](../secgloss/p-gly.md). **EncryptMessage (Digest)** permet à l’application de choisir parmi les [*algorithmes de chiffrement*](../secgloss/c-gly.md) pris en charge par le mécanisme choisi. La fonction **EncryptMessage (Digest)** utilise le [*contexte de sécurité*](../secgloss/s-gly.md) référencé par le handle de contexte. Certains packages n’ont pas de messages à chiffrer ou à déchiffrer, mais fournissent plutôt un [*hachage*](../secgloss/h-gly.md) d’intégrité qui peut être vérifié.

Cette fonction est uniquement disponible en tant que mécanisme SASL.

> [!Note]  
> **EncryptMessage (Digest)** et [**DecryptMessage (Digest)**](decryptmessage--digest.md) peuvent être appelés en même temps à partir de deux threads différents dans un contexte SSPI ( [*Security Support Provider Interface*](../secgloss/s-gly.md) ) unique si un thread est en cours de chiffrement et que l’autre déchiffre. Si plusieurs threads chiffrent, ou si plusieurs threads déchiffrent, chaque thread doit obtenir un contexte unique.

 

## <a name="syntax"></a>Syntaxe


```C++
SECURITY_STATUS SEC_ENTRY EncryptMessage(
  PCtxtHandle    phContext,
  unsigned long  fQOP,
  PSecBufferDesc pMessage,
  unsigned long  MessageSeqNo
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

Lorsque vous utilisez le SSP Digest, ce paramètre doit avoir la valeur zéro.

</dd> <dt>

*pMessage* \[ in, out\]
</dt> <dd>

Pointeur vers une structure [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . En entrée, la structure fait référence à une ou plusieurs structures [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) qui peuvent être de type SecBuffer \_ . Cette mémoire tampon contient le message à chiffrer. Le message est chiffré sur place, remplaçant le contenu d’origine de la structure.

La fonction ne traite pas les tampons avec l' \_ attribut SECBUFFER ReadOnly.

La longueur de la structure [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) qui contient le message ne doit pas être supérieure à **cbMaximumMessage**, qui est obtenue à partir de la fonction [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) (SECPKG \_ attr \_ Stream \_ sizes).

Lorsque vous utilisez le SSP Digest, il doit exister une deuxième mémoire tampon de type SECBUFFER \_ padding ou \_ sec \_ Data buffer pour contenir les informations de [*signature*](../secgloss/d-gly.md#_security_digital_signature_gly) . Pour connaître la taille de la mémoire tampon de sortie, appelez la fonction [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) et spécifiez des \_ tailles d’attr SECPKG \_ . La fonction retourne une structure [**de \_ tailles SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) . La taille de la mémoire tampon de sortie est la somme des valeurs des membres **cbMaxSignature** et **cbBlockSize** .

Les applications qui n’utilisent pas SSL doivent fournir un [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) de type SecBuffer \_ Padding.

</dd> <dt>

*MessageSeqNo* \[ dans\]
</dt> <dd>

Numéro de séquence que l’application de transport a affecté au message. Si l’application de transport ne conserve pas les numéros séquentiels, ce paramètre doit être égal à zéro.

Lorsque vous utilisez le SSP Digest, ce paramètre doit avoir la valeur zéro. Le SSP Digest gère la numérotation des séquences en interne.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction s’exécute correctement, la fonction retourne SEC \_ E \_ OK.

Si la fonction échoue, elle retourne l’un des codes d’erreur suivants.



| Code de retour                                                                                                    | Description                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_tampon s \_ E \_ trop \_ petit**</dt> </dl>      | La mémoire tampon de sortie est trop petite. Pour plus d'informations, consultez la section Notes.<br/>                                                                                                                                                                 |
| <dl> <dt>**\_contexte E/s \_ \_ expiré**</dt> </dl>        | L’application fait référence à un contexte qui a déjà été fermé. Une application correctement écrite ne doit pas recevoir cette erreur.<br/>                                                                                               |
| <dl> <dt>**SEC \_ E \_ système de chiffrement \_ \_ non valide**</dt> </dl> | Le [*chiffrement*](../secgloss/c-gly.md) choisi pour le [*contexte de sécurité*](../secgloss/s-gly.md) n’est pas pris en charge.<br/>                                                                                                         |
| <dl> <dt>**s \_ E \_ mémoire insuffisante \_**</dt> </dl>    | La mémoire disponible est insuffisante pour terminer l’action demandée.<br/>                                                                                                                                                             |
| <dl> <dt>**SEC \_ E \_ handle non valide \_**</dt> </dl>         | Un descripteur de contexte non valide a été spécifié dans le paramètre *phContext* .<br/>                                                                                                                                                     |
| <dl> <dt>**s \_ E \_ jeton non valide \_**</dt> </dl>          | Aucune \_ mémoire tampon de type de données SECBUFFER n’a été trouvée.<br/>                                                                                                                                                                                          |
| <dl> <dt>**SEC \_ E \_ QoP \_ non \_ pris en charge**</dt> </dl>     | La confidentialité et l' [*intégrité*](../secgloss/i-gly.md) ne sont pas prises en charge par le [*contexte de sécurité*](../secgloss/s-gly.md).<br/> |



 

## <a name="remarks"></a>Remarques

La fonction **EncryptMessage (Digest)** chiffre un message basé sur le message et la [*clé de session*](../secgloss/s-gly.md) à partir d’un contexte de [*sécurité*](../secgloss/s-gly.md).

Si l’application de transport a créé le [*contexte de sécurité*](../secgloss/s-gly.md) pour prendre en charge la détection de séquence et que l’appelant fournit un numéro de séquence, la fonction inclut ces informations avec le message chiffré. L’inclusion de ces informations protège la relecture, l’insertion et la suppression des messages. Le [*package de sécurité*](../secgloss/s-gly.md) intègre le numéro de séquence passé à partir de l’application de transport.

Lorsque vous utilisez le SSP Digest, récupérez la taille de la mémoire tampon de sortie en appelant la fonction [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) et en spécifiant des \_ tailles d’attr SECPKG \_ . La fonction retourne une structure [**de \_ tailles SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) . La taille de la mémoire tampon de sortie est la somme des valeurs des membres **cbMaxSignature** et **cbBlockSize** .

> [!Note]  
> Ces mémoires tampons doivent être fournies dans l’ordre indiqué.

 



| Type de mémoire tampon                           | Description                                                                                                                    |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ en-tête de flux SECBUFFER<br/>  | Utilisé en interne. Aucune initialisation n’est requise.<br/>                                                                        |
| \_données SECBUFFER<br/>            | Contient le message de [*texte en clair*](../secgloss/s-gly.md) à chiffrer.<br/> |
| Code de fin de \_ flux SECBUFFER \_<br/> | Utilisé en interne. Aucune initialisation n’est requise.<br/>                                                                        |
| SECBUFFER \_ vide<br/>           | Utilisé en interne. Aucune initialisation n’est requise. La taille peut être égale à zéro.<br/>                                                      |



 

Pour des performances optimales, les structures *pMessage* doivent être allouées à partir de la mémoire contiguë.

**Windows XP :** Cette fonction était également connue sous le nom de **SealMessage**. Les applications doivent désormais utiliser **EncryptMessage (Digest)** uniquement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                   |
| En-tête<br/>                   | <dl> <dt>SSPI. h (include Security. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Secur32. lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md)
</dt> <dt>

[**DecryptMessage (Digest)**](decryptmessage--digest.md)
</dt> <dt>

[**InitializeSecurityContext (condensé)**](initializesecuritycontext--digest.md)
</dt> <dt>

[**QueryContextAttributes (Digest)**](querycontextattributes--digest.md)
</dt> <dt>

[**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

 

 
