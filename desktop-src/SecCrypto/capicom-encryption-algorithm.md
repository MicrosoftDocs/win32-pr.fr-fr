---
description: Définit les algorithmes à utiliser dans le chiffrement et le déchiffrement.
ms.assetid: c7aacd1c-02f6-4cf5-9305-50e2330f243c
title: Énumération CAPICOM_ENCRYPTION_ALGORITHM (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCRYPTION_ALGORITHM
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 19626ba560ead406005612db3ed90cabc61d98ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121129"
---
# <a name="capicom_encryption_algorithm-enumeration"></a>\_Énumération de l’algorithme de chiffrement CAPICOM \_

Le type d’énumération de l' **\_ \_ algorithme de chiffrement CAPICOM** définit les algorithmes à utiliser dans le chiffrement et le déchiffrement.

## <a name="members"></a>Membres



| Membre                                   | Description                                                                                                                                                                                              | Valeur     |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| **\_Algorithme de chiffrement CAPICOM \_ \_ RC2**  | Utilisez le chiffrement RSA RC2.<br/>                                                                                                                                                                       | 0         |
| **\_Algorithme de chiffrement CAPICOM \_ \_ RC4**  | Utilisez le chiffrement RSA RC4.<br/>                                                                                                                                                                       | 1         |
| **\_algorithme de chiffrement CAPICOM \_ \_ des**  | Utilisez le chiffrement DES.<br/>                                                                                                                                                                           | 2         |
| **\_Algorithme de chiffrement CAPICOM \_ \_ 3DES** | Utilisez le chiffrement triple DES.<br/>                                                                                                                                                                    | 3         |
| **\_algorithme de chiffrement CAPICOM \_ \_ AES**  | Utilisez l’algorithme [*Advanced Encryption Standard*](../secgloss/a-gly.md) (AES). Cette valeur est valide pour l’objet [**EncryptedData**](encrypteddata.md) uniquement.<br/> | 4//v 2.0 |



## <a name="remarks"></a>Notes

Le type d’énumération de l' **\_ \_ algorithme de chiffrement CAPICOM** est utilisé par la propriété [**Algorithm.Name**](algorithm-name.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------|--------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                |
| En-tête<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
