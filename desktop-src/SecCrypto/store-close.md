---
description: Ferme un magasin de certificats ouvert.
ms.assetid: 14db819a-b220-47d4-9030-72157e0e5019
title: Store. Close, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Close
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e0310db88b29fea18756ecaf7a2dc142097c3a6e53dfff5892acdaf4030b9b00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897924"
---
# <a name="storeclose-method"></a>Store. Close, méthode

\[La méthode **Close** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La méthode **Close** ferme un [*magasin de certificats*](../secgloss/c-gly.md)ouvert.

## <a name="syntax"></a>Syntaxe


```VB
Store.Close()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Une fois la méthode **Close** appelée, l’objet [**Store**](store.md) est détruit.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,1 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Magasin**](store.md)
</dt> <dt>

[**Objets de chiffrement**](cryptography-objects.md)
</dt> <dt>

[**Afficher**](store-open.md)
</dt> </dl>

 

 
