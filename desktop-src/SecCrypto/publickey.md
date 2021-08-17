---
description: L’objet PublicKey représente une clé publique dans un objet de certificat.
title: PublicKey, objet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5d27a89d51840e70563854b3cc7f9084b6bd42cb5707630755e771d610c64a91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901346"
---
# <a name="publickey-object"></a>PublicKey, objet

\[L’objet **PublicKey** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. Utilisez plutôt la [**propriété X509Certificate2. PublicKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

L’objet **PublicKey** représente une clé publique dans un objet de [**certificat**](certificate.md) .

## <a name="when-to-use"></a>Quand l’utiliser

L’objet **PublicKey** est utilisé pour récupérer les données relatives à la clé publique.

## <a name="members"></a>Membres

L’objet **PublicKey** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **PublicKey** possède ces propriétés.



| Propriété                                                            | Type d’accès          | Description                                                                                                                            |
|:--------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**Algorithm**](publickey-algorithm.md)<br/>                 | Lecture seule<br/> | Récupère l’objet [**OID**](oid.md) qui identifie l’algorithme utilisé par la clé publique. Il s’agit de la propriété par défaut.<br/> |
| [**EncodedKey**](publickey-encodedkey.md)<br/>               | Lecture seule<br/> | Récupère un objet [**EncodedData**](encodeddata.md) qui fournit l’accès à la valeur de la clé publique.<br/>                 |
| [**EncodedParameters**](publickey-encodedparameters.md)<br/> | Lecture seule<br/> | Récupère un objet [**EncodedData**](encodeddata.md) qui fournit l’accès aux paramètres de l’algorithme de clé publique.<br/>  |
| [**Longueur**](publickey-length.md)<br/>                       | Lecture seule<br/> | Récupère la longueur de la clé publique en bits.<br/>                                                                             |



 

## <a name="remarks"></a>Remarques

Impossible de créer l’objet **PublicKey** .

L’objet **PublicKey** est utilisé par la méthode [**Certificate. PublicKey**](certificate-publickey.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
