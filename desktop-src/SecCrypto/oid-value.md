---
description: Définit ou récupère la valeur du numéro d’OID en pointillés de l’identificateur.
ms.assetid: bb960e65-776e-4ae8-a557-62254dc10558
title: OID. Propriété Value
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: edaca987dbba57127c922161fbc6c6cd9473732ba1b7d1339618009335c904cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117979731"
---
# <a name="oidvalue-property"></a>OID. Propriété Value

\[La propriété **valeur** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe OID**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La propriété **value** définit ou récupère la valeur du numéro d’OID en pointillés de l’identificateur.

## <a name="syntax"></a>Syntaxe


```VB
OID.Value As String
```



## <a name="property-value"></a>Valeur de la propriété

Valeur du numéro d’OID en pointillés de l’identificateur. Pour connaître les valeurs possibles, consultez Wincrypt. h.

## <a name="remarks"></a>Remarques

Si la propriété **valeur** est définie, la propriété [**FriendlyName**](oid-friendlyname.md) est définie sur le nom complet correspondant. Si la propriété **FriendlyName** est définie, la propriété **value** est définie sur la valeur en pointillé correspondante.

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**OID**](oid.md)
</dt> </dl>

 

 
