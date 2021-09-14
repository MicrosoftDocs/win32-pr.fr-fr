---
description: Supprime le magasin de certificats représenté par l’objet de magasin actuel.
ms.assetid: 274914ee-27a0-4bd6-8510-af897aab3a2d
title: Store. Delete, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Delete
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41c6417dae5006eb2ecaf64660fd0007cdf37fd2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120809"
---
# <a name="storedelete-method"></a>Store. Delete, méthode

\[La méthode de **suppression** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La méthode **Delete** supprime le [*magasin de certificats*](../secgloss/c-gly.md) représenté par l’objet [**Store**](certificate.md) actuel. Cette méthode supprime uniquement les magasins qui ne sont pas du système.

## <a name="syntax"></a>Syntaxe


```VB
Store.Delete()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Les magasins suivants sont des magasins système qui ne peuvent pas être supprimés :

-   My
-   Root
-   Confiance
-   CA
-   UserDS
-   TrustedPublisher
-   Interdit
-   AuthRoot
-   TrustedPeople

La méthode **Delete** retourne une erreur si elle est appelée à partir d’un script Web.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,1 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Magasin**](store.md)
</dt> <dt>

[**Objets de chiffrement**](cryptography-objects.md)
</dt> </dl>

 

 
