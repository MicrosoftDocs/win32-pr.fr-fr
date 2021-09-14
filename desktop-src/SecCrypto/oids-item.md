---
description: Récupère un objet OID de la collection. Il s’agit de la propriété par défaut.
ms.assetid: af0de567-e520-411d-850d-fbdbcb2ace69
title: OID. Item, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: dfdf65f013c5e5e1a031c03c19af9d08b8fc72c1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123089"
---
# <a name="oidsitem-property"></a>OID. Item, propriété

\[La propriété **Item** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe OidCollection**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La propriété **Item** récupère un objet [**OID**](oid.md) de la collection. Il s’agit de la propriété par défaut.

## <a name="syntax"></a>Syntaxe


```VB
OIDs.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>Valeur de la propriété

Objet [**OID**](oid.md) à l’index spécifié, ou objet **OID** avec la valeur en pointillés spécifiée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**OID**](oids.md)
</dt> </dl>

 

 
