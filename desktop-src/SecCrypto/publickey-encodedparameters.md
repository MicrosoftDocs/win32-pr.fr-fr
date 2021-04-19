---
description: Récupère les paramètres de l’algorithme de clé publique.
ms.assetid: 1d12f72e-0144-4b7b-b468-d2f35bf253d3
title: Propriété PublicKey. EncodedParameters
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.EncodedParameters
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 316e9737633bccea46cb644da24e4cc98fd118bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537751"
---
# <a name="publickeyencodedparameters-property"></a>Propriété PublicKey. EncodedParameters

\[La propriété **EncodedParameters** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**propriété X509Certificate2. PublicKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propriété **EncodedParameters** récupère les paramètres de l’algorithme de clé publique.

## <a name="syntax"></a>Syntaxe


```VB
PublicKey.EncodedParameters As EncodedData
```



## <a name="property-value"></a>Valeur de la propriété

Objet [**EncodedData**](encodeddata.md) qui fournit l’accès aux paramètres de l’algorithme de clé publique.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PublicKey**](publickey.md)
</dt> </dl>

 

 
