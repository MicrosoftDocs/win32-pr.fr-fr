---
description: Définit ou récupère la longueur de la clé.
ms.assetid: c0176d2d-c000-4529-af45-1cc9060ca56a
title: Propriété d’algorithme. KeyLength
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm.KeyLength
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c5ce8f906628df06ef506a0f57c33db4bed7c5980bb78ab2e0094d0443b5646b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773663"
---
# <a name="algorithmkeylength-property"></a>Propriété d’algorithme. KeyLength

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista, Windows XP. Utilisez plutôt la [**classe AlgorithmIdentifier**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La propriété **KeyLength** définit ou récupère la longueur de la clé.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
Algorithm.KeyLength As CAPICOM_ENCRYPTION_KEY_LENGTH
```



## <a name="property-value"></a>Valeur de la propriété

Valeur de l’énumération de la [**longueur de \_ \_ clé \_ de chiffrement CAPICOM**](capicom-encryption-key-length.md) qui spécifie la longueur de clé. Le tableau suivant répertorie les valeurs possibles.



| Value                                                                                                                                                                                                                                        | Signification                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM"></span><span id="capicom_encryption_key_length_maximum"></span><dl> <dt>**\_ \_ \_ longueur maximale de la clé de chiffrement CAPICOM \_**</dt> </dl>     | Utilisez la longueur de clé maximale disponible avec l’algorithme de chiffrement indiqué.<br/> |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS"></span><span id="capicom_encryption_key_length_40_bits"></span><dl> <dt>**\_Longueur de clé de chiffrement capicom \_ \_ \_ 40 \_ bits**</dt> </dl>    | Utilisez des clés 40 bits.<br/>                                                              |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS"></span><span id="capicom_encryption_key_length_56_bits"></span><dl> <dt>**\_Longueur de clé de chiffrement capicom \_ \_ \_ 56 \_ bits**</dt> </dl>    | Utilisez des clés 56 bits si elles sont disponibles.<br/>                                                 |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS"></span><span id="capicom_encryption_key_length_128_bits"></span><dl> <dt>**\_Longueur de clé de chiffrement capicom \_ \_ \_ 128 \_ bits**</dt> </dl> | Utilisez des clés 128 bits si elles sont disponibles.<br/>                                                |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_192_BITS"></span><span id="capicom_encryption_key_length_192_bits"></span><dl> <dt>**\_Longueur de clé de chiffrement capicom \_ \_ \_ 192 \_ bits**</dt> </dl> | Utilisez des clés 192 bits. Cette longueur de clé n’est disponible que pour AES.<br/>                  |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_256_BITS"></span><span id="capicom_encryption_key_length_256_bits"></span><dl> <dt>**\_Longueur de clé de chiffrement capicom \_ \_ \_ 256 \_ bits**</dt> </dl> | Utilisez des clés 256 bits. Cette longueur de clé n’est disponible que pour AES.<br/>                  |



 

## <a name="remarks"></a>Remarques

Lorsque des algorithmes de chiffrement DES et 3DES sont utilisés, les longueurs de clé sont standard et la propriété **KeyLength** est ignorée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Algorithm**](algorithm.md)
</dt> </dl>

 

 
