---
description: L' \_ \_ énumération de l’algorithme de hachage CAPICOM définit un algorithme de hachage.
ms.assetid: 5373b6cc-944a-4d83-ac71-59edcb2af94e
title: Énumération CAPICOM_HASH_ALGORITHM (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_HASH_ALGORITHM
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 14ee06437f7b6e32c58415e5b9d77a75929250a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534980"
---
# <a name="capicom_hash_algorithm-enumeration"></a>\_Énumération de l' \_ algorithme de hachage CAPICOM

L’énumération de l' **\_ \_ algorithme de hachage CAPICOM** définit un algorithme de hachage.

## <a name="members"></a>Membres



| Membre                                 | Description                                                                                                                                                                 | Valeur |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **\_Algorithme de hachage \_ CAPICOM \_ SHA1**     | [*Algorithme de hachage sécurisé*](../secgloss/s-gly.md) (SHA) qui génère un résumé de message 160 bits.<br/> | 0     |
| **MD2 de l' \_ algorithme de hachage CAPICOM \_ \_**      | Algorithme de hachage MD2.<br/>                                                                                                                                           | 1     |
| **\_Algorithme de hachage \_ CAPICOM \_ MD4**      | Algorithme de hachage MD4.<br/>                                                                                                                                           | 2     |
| **\_Algorithme de hachage \_ CAPICOM \_ MD5**      | Algorithme de hachage MD5.<br/>                                                                                                                                           | 3     |
| **\_Algorithme de hachage \_ capicom \_ SHA \_ 256** | Algorithme de hachage SHA-256.<br/> **CAPICOM 2.0.0.3 et versions antérieures :** Cette valeur n’est pas prise en charge.<br/>                                                                 | 4     |
| **\_Algorithme de hachage \_ capicom \_ SHA \_ 384** | Algorithme de hachage SHA-384.<br/> **CAPICOM 2.0.0.3 et versions antérieures :** Cette valeur n’est pas prise en charge.<br/>                                                                 | 5     |
| **\_Algorithme de hachage \_ capicom \_ SHA \_ 512** | Algorithme de hachage SHA-512.<br/> **CAPICOM 2.0.0.3 et versions antérieures :** Cette valeur n’est pas prise en charge.<br/>                                                                 | 6     |



## <a name="remarks"></a>Notes

L’énumération de l' **\_ \_ algorithme de hachage CAPICOM** est utilisée par la propriété [**HashedData. Algorithm**](hasheddata-algorithm.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|--------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                |
| En-tête<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
