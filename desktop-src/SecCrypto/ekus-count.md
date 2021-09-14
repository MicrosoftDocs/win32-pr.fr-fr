---
description: Récupère le nombre d’objets EKU dans la collection.
ms.assetid: a38ac480-4f9b-4d69-a7e6-fae4993fe2cf
title: EKU. Count, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKUs.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41e77f3803fa65db1573c6619ebf1265b7418924
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416468"
---
# <a name="ekuscount-property"></a>EKU. Count, propriété

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propriété **Count** récupère le nombre d’objets [**EKU**](eku.md) dans la collection.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
EKUs.Count As Long
```



## <a name="property-value"></a>Valeur de la propriété

Nombre d’objets [**EKU**](eku.md) dans la collection. Chaque objet **EKU** représente une propriété d’utilisation améliorée de la clé (EKU) d’un certificat.

## <a name="remarks"></a>Notes

La propriété **Count** peut être utilisée pour spécifier le dernier objet [**EKU**](eku.md) d’une collection lors de l’extraction d’un objet **EKU** spécifique à l’aide de la propriété [**EKU. Item**](ekus-item.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
