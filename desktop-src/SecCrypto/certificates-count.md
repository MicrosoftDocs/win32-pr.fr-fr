---
description: Récupère le nombre d’objets de certificat dans la collection.
ms.assetid: 95931721-3b0c-4915-805f-039d1d5510fa
title: Propriété Certificates. Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 703b929ee4b9cbe69a0f2ff37ad7e1d0c2c0005c0aa461fc38a14baa8a8ab443
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770548"
---
# <a name="certificatescount-property"></a>Propriété Certificates. Count

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propriété **Count** récupère le nombre d’objets de [**certificat**](certificate.md) dans la collection.

## <a name="syntax"></a>Syntaxe


```VB
Certificates.Count As Long
```



## <a name="property-value"></a>Valeur de la propriété

Nombre d’objets de [**certificat**](certificate.md) dans la collection. Chaque objet de **certificat** représente un certificat unique dans la collection.

## <a name="remarks"></a>Remarques

CAPICOM ne prend en charge qu’un seul certificat pour le magasin de [*cartes à puce*](../secgloss/s-gly.md) . Même si le magasin de cartes à puce contient plus d’un certificat, cette propriété contient 1. Pour plus d’informations sur le magasin de cartes à puce, consultez le membre du **\_ \_ \_ \_ magasin utilisateur de la carte à puce** CAPICOM de l’énumération [**\_ \_ emplacement du magasin CAPICOM**](capicom-store-location.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Certificates**](certificates.md)
</dt> </dl>

 

 
