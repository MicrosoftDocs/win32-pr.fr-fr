---
description: Définit ou récupère le type d’algorithme de hachage utilisé.
ms.assetid: 3f8e83f2-0e46-494b-ac63-658e663680ea
title: HashedData. algorithme, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 16562f3b954c9968899b7af63729a105956c7f809d094bdfa6c508a160a6d51d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006647"
---
# <a name="hasheddataalgorithm-property"></a>HashedData. algorithme, propriété

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe HashAlgorithm**](/previous-versions/windows/) dans l’espace de noms [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La propriété de l' **algorithme** définit ou récupère le type d’algorithme de hachage utilisé.

## <a name="syntax"></a>Syntaxe


```VB
HashedData.Algorithm As CAPICOM_HASH_ALGORITHM
```



## <a name="property-value"></a>Valeur de la propriété

Valeur de l’énumération de l' [**\_ \_ algorithme de hachage CAPICOM**](capicom-hash-algorithm.md) qui définit un algorithme de hachage. La valeur par défaut est CAPICOM \_ hash \_ Algorithm \_ SHA1. Le tableau suivant répertorie les valeurs possibles.



| Value                                                                                                                                                                                                               | Signification                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_HASH_ALGORITHM_SHA1"></span><span id="capicom_hash_algorithm_sha1"></span><dl> <dt>**\_Algorithme de hachage \_ CAPICOM \_ SHA1**</dt> </dl>           | Algorithme de hachage SHA1.<br/>                                                                          |
| <span id="CAPICOM_HASH_ALGORITHM_MD2"></span><span id="capicom_hash_algorithm_md2"></span><dl> <dt>**MD2 de l' \_ algorithme de hachage CAPICOM \_ \_**</dt> </dl>              | Algorithme de hachage MD2.<br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_MD4"></span><span id="capicom_hash_algorithm_md4"></span><dl> <dt>**\_Algorithme de hachage \_ CAPICOM \_ MD4**</dt> </dl>              | Algorithme de hachage MD4.<br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_MD5"></span><span id="capicom_hash_algorithm_md5"></span><dl> <dt>**\_Algorithme de hachage \_ CAPICOM \_ MD5**</dt> </dl>              | Algorithme de hachage MD5.<br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_256"></span><span id="capicom_hash_algorithm_sha_256"></span><dl> <dt>**\_Algorithme de hachage \_ capicom \_ SHA \_ 256**</dt> </dl> | Algorithme de hachage SHA-256.<br/> **CAPICOM 2.0.0.3 et versions antérieures :** Cette valeur n’est pas prise en charge.<br/> |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_384"></span><span id="capicom_hash_algorithm_sha_384"></span><dl> <dt>**\_Algorithme de hachage \_ capicom \_ SHA \_ 384**</dt> </dl> | Algorithme de hachage SHA-384.<br/> **CAPICOM 2.0.0.3 et versions antérieures :** Cette valeur n’est pas prise en charge.<br/> |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_512"></span><span id="capicom_hash_algorithm_sha_512"></span><dl> <dt>**\_Algorithme de hachage \_ capicom \_ SHA \_ 512**</dt> </dl> | Algorithme de hachage SHA-512.<br/> **CAPICOM 2.0.0.3 et versions antérieures :** Cette valeur n’est pas prise en charge.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**HashedData**](hasheddata.md)
</dt> </dl>

 

 
