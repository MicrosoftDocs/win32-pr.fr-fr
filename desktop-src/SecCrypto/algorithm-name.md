---
description: Définit ou récupère l’algorithme utilisé pour la signature, l’enveloppe et le chiffrement des opérations. Il s’agit de la propriété par défaut.
ms.assetid: e1144a9c-a352-4f73-a91c-ea66f3d61608
title: Propriété Algorithm.Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 35ff147d8db7fb409787fa938a951dfc0a2320e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523871"
---
# <a name="algorithmname-property"></a>Propriété Algorithm.Name

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista, Windows XP. Utilisez plutôt la [**classe AlgorithmIdentifier**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La propriété **Name** définit ou récupère l’algorithme utilisé pour la signature, l’enveloppe et le chiffrement des opérations. Il s’agit de la propriété par défaut.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
Algorithm.Name As CAPICOM_ENCRYPTION_ALGORITHM
```



## <a name="property-value"></a>Valeur de la propriété

Valeur de l’énumération de l' [**\_ \_ algorithme de chiffrement CAPICOM**](capicom-encryption-algorithm.md) qui spécifie l’algorithme à utiliser. Le tableau suivant répertorie les valeurs possibles.



| Value                                                                                                                                                                                                                       | Signification                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_RC2"></span><span id="capicom_encryption_algorithm_rc2"></span><dl> <dt>**\_Algorithme de chiffrement CAPICOM \_ \_ RC2**</dt> </dl>    | Utilisez le chiffrement RC2.<br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_RC4"></span><span id="capicom_encryption_algorithm_rc4"></span><dl> <dt>**\_Algorithme de chiffrement CAPICOM \_ \_ RC4**</dt> </dl>    | Utilisez le chiffrement RC4.<br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_DES"></span><span id="capicom_encryption_algorithm_des"></span><dl> <dt>**\_algorithme de chiffrement CAPICOM \_ \_ des**</dt> </dl>    | Utilisez le chiffrement DES.<br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_3DES"></span><span id="capicom_encryption_algorithm_3des"></span><dl> <dt>**\_Algorithme de chiffrement CAPICOM \_ \_ 3DES**</dt> </dl> | Utilisez le chiffrement triple DES.<br/> |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_AES"></span><span id="capicom_encryption_algorithm_aes"></span><dl> <dt>**\_algorithme de chiffrement CAPICOM \_ \_ AES**</dt> </dl>    | Utilisez l’algorithme AES.<br/>     |



 

## <a name="remarks"></a>Notes

Lorsque la valeur de cette propriété est réinitialisée, directement ou indirectement, l’intégralité de l’état de l’objet est réinitialisée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
