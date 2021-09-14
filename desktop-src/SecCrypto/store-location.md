---
description: Récupère l’emplacement du magasin de certificats que cet objet représente.
ms.assetid: 756ee7cb-5f9f-4fb2-bf10-79b543895189
title: Store. Location, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Location
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 42afe40dffde5a0375928d355508ec75a4076f17
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011144"
---
# <a name="storelocation-property"></a>Store. Location, propriété

\[La propriété **emplacement** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propriété **location** récupère l’emplacement du magasin de certificats que cet objet représente.

## <a name="syntax"></a>Syntaxe


```VB
Store.Location As CAPICOM_STORE_LOCATION
```



## <a name="property-value"></a>Valeur de la propriété

Valeur d' [**emplacement du \_ magasin \_ CAPICOM**](capicom-store-location.md) qui représente l’emplacement du magasin de certificats.

## <a name="remarks"></a>Notes

La valeur de la propriété **location** est identique à la valeur fournie pour le paramètre *StoreLocation* de la méthode [**Open**](store-open.md) lors de l’ouverture du magasin.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,1 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Magasin**](store.md)
</dt> </dl>

 

 
