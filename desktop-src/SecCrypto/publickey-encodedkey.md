---
description: Récupère la valeur de la clé publique.
ms.assetid: d9846ebe-44df-4ee0-8f15-cc96883d9d53
title: Propriété PublicKey. EncodedKey
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.EncodedKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0d4708461f5ff51d5f86170ba0f1df35669859149b4882f8fb86aafdbed5e436
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901461"
---
# <a name="publickeyencodedkey-property"></a>Propriété PublicKey. EncodedKey

\[La propriété **EncodedKey** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**propriété X509Certificate2. PublicKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propriété **EncodedKey** récupère la valeur de la clé publique.

## <a name="syntax"></a>Syntaxe


```VB
PublicKey.EncodedKey As EncodedData
```



## <a name="property-value"></a>Valeur de la propriété

Objet [**EncodedData**](encodeddata.md) qui fournit l’accès à la valeur de la clé publique.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PublicKey**](publickey.md)
</dt> </dl>

 

 
