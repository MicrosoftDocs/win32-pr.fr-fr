---
description: Récupère le nom du magasin de certificats que cet objet représente.
ms.assetid: db61b464-0e8e-4b19-be12-04e00d6bba53
title: Propriété Store.Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 85679bb594bdb59c41773b7f956deea95021381f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541784"
---
# <a name="storename-property"></a>Propriété Store.Name

\[La propriété [**nom**](store-location.md) peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propriété [**Name**](store-location.md) récupère le nom du magasin de certificats que cet objet représente.

## <a name="syntax"></a>Syntaxe


```VB
Store.Name As String
```



## <a name="property-value"></a>Valeur de la propriété

Valeur de **chaîne** qui représente le nom du magasin de certificats.

## <a name="remarks"></a>Notes

Voici des exemples de noms de magasins de certificats : My et root.

La valeur de la propriété [**Name**](store-location.md) est la même que la valeur fournie pour le paramètre *StoreName* de la méthode [**Open**](store-open.md) lors de l’ouverture du magasin.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,1 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Magasin**](store.md)
</dt> </dl>

 

 
