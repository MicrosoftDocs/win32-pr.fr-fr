---
description: Récupère la collection de certificats associée à l’objet SignedData. Une fois récupérés, les objets de certificat individuels de la collection peuvent être énumérés.
ms.assetid: 94741fee-2462-4a18-bc14-c52e9cac374b
title: SignedData. Certificates, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 55c0fe432794289fabe67b37deeedfac43f7a7d0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095865"
---
# <a name="signeddatacertificates-property"></a>SignedData. Certificates, propriété

\[La propriété **certificats** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La propriété **certificats** récupère la collection de [**certificats**](certificates.md) associée à l’objet [**SignedData**](signeddata.md) . Une fois récupérés, les objets de [**certificat**](certificate.md) individuels de la collection peuvent être énumérés.

## <a name="syntax"></a>Syntaxe


```VB
SignedData.Certificates As Certificates
```



## <a name="property-value"></a>Valeur de la propriété

Collection de [**certificats**](certificates.md) associée à l’objet [**SignedData**](signeddata.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 
