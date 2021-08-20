---
description: Définit ou récupère le nom complet de l’identificateur.
ms.assetid: 53f84d0d-c189-4fd2-a383-29fd0d22de08
title: OID. FriendlyName, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID.FriendlyName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4af16c5f143d44a743b4e8f327b7d89f616b833707e09dc365a087ef37243f40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117980065"
---
# <a name="oidfriendlyname-property"></a>OID. FriendlyName, propriété

\[La propriété **FriendlyName** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe OID**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La propriété **FriendlyName** définit ou récupère le nom complet de l’identificateur.

## <a name="syntax"></a>Syntaxe


```VB
OID.FriendlyName As String
```



## <a name="property-value"></a>Valeur de la propriété

Nom complet de l' [**OID**](oid.md).

## <a name="remarks"></a>Remarques

Si la propriété **FriendlyName** est définie, la propriété [**value**](oid-value.md) est définie sur la valeur en pointillé correspondante. Si la propriété **valeur** est définie, la propriété **FriendlyName** est définie sur le nom complet correspondant.

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**OID**](oid.md)
</dt> </dl>

 

 
