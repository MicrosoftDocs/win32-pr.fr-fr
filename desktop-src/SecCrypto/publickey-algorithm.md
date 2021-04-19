---
description: La propriété algorithme récupère l’objet OID qui identifie l’algorithme utilisé par la clé publique. Il s’agit de la propriété par défaut.
ms.assetid: f804ac4b-6a33-4f25-950b-6b6838bcc638
title: PublicKey. Algorithm, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 98e955279646306b1484dcd0674cf735680d44e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528854"
---
# <a name="publickeyalgorithm-property"></a>PublicKey. Algorithm, propriété

\[La propriété **algorithme** est disponible pour une utilisation dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**propriété X509Certificate2. PublicKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propriété **algorithme** récupère l’objet [**OID**](oid.md) qui identifie l’algorithme utilisé par la clé publique. Il s’agit de la propriété par défaut.

## <a name="syntax"></a>Syntaxe


```VB
PublicKey.Algorithm As OID
```



## <a name="property-value"></a>Valeur de la propriété

Objet [**OID**](oid.md) qui identifie l’algorithme utilisé par la clé publique.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PublicKey**](publickey.md)
</dt> </dl>

 

 
