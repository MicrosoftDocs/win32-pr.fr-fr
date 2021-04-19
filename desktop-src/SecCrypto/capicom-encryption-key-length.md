---
description: Définit la longueur de clé à utiliser dans le chiffrement.
ms.assetid: a91e75db-f81e-4908-b795-34be7a1c242d
title: Énumération CAPICOM_ENCRYPTION_KEY_LENGTH (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCRYPTION_KEY_LENGTH
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 4f3e64df1e706ef20a83f4da5c81cda2a08ed331
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537127"
---
# <a name="capicom_encryption_key_length-enumeration"></a>\_Énumération de la \_ longueur de clé de CHIFFREment CAPICOM \_

Le type d’énumération de la **longueur de \_ \_ clé \_ de chiffrement CAPICOM** définit la [*longueur de clé*](../secgloss/k-gly.md) à utiliser dans le chiffrement.

## <a name="members"></a>Membres



| Membre                                          | Description                                                                               | Valeur     |
|-------------------------------------------------|-------------------------------------------------------------------------------------------|-----------|
| **\_ \_ \_ longueur maximale de la clé de chiffrement CAPICOM \_**   | Utilise la longueur de clé maximale disponible avec l’algorithme de chiffrement indiqué.<br/> | 0         |
| **\_Longueur de clé de chiffrement capicom \_ \_ \_ 40 \_ bits**  | Utilise des clés 40 bits.<br/>                                                              | 1         |
| **\_Longueur de clé de chiffrement capicom \_ \_ \_ 56 \_ bits**  | Utilise des clés 56 bits si elles sont disponibles.<br/>                                                 | 2         |
| **\_Longueur de clé de chiffrement capicom \_ \_ \_ 128 \_ bits** | Utilise des clés 128 bits si elles sont disponibles.<br/>                                                | 3         |
| **\_Longueur de clé de chiffrement capicom \_ \_ \_ 192 \_ bits** | Utilise des clés 192 bits. Cette longueur de clé n’est disponible que pour AES.<br/>                  | 4//v 2.0 |
| **\_Longueur de clé de chiffrement capicom \_ \_ \_ 256 \_ bits** | Utilise des clés 256 bits. Cette longueur de clé n’est disponible que pour AES.<br/>                  | 5//v 2.0 |



## <a name="remarks"></a>Notes

Le type d’énumération de la **\_ longueur de \_ clé \_ de chiffrement CAPICOM** est utilisé par la propriété [**Algorithm. KeyLength**](algorithm-keylength.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|--------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                |
| En-tête<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
