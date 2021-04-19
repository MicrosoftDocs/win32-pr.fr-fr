---
description: Ajoute l’objet OID spécifié à la collection.
ms.assetid: 0ae087d6-768a-4538-b834-0f936680de05
title: Méthode OID. Add
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d2fa007798a0657991ec8e37a7dddc9fb4c95b2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106536054"
---
# <a name="oidsadd-method"></a>Méthode OID. Add

\[La méthode **Add** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. Utilisez plutôt la [**classe OidCollection**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La méthode **Add** ajoute l’objet [**OID**](oid.md) spécifié à la collection.

## <a name="syntax"></a>Syntaxe


```VB
OIDs.Add( _
  ByVal OID _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*OID* \[ dans\]
</dt> <dd>

Objet [**OID**](oid.md) à ajouter à la collection. L’objet **OID** est ajouté dans l’ordre trié en fonction de sa valeur en pointillés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
