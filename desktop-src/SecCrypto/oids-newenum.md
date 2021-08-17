---
description: La \_ propriété NewEnum des OID récupère une interface IEnumVARIANT sur un objet qui peut être utilisé pour énumérer la collection. cette propriété est masquée dans Visual Basic scripting Edition (VBScript).
ms.assetid: 7c09fd11-064b-451e-bd6b-e6c13ab228a0
title: OIDs._NewEnum, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9d7841f2b041a9e48f9954b1f81d68828e1bef17f16d7f54e470ab2ecb904916
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117979488"
---
# <a name="oids_newenum-property"></a>OID. \_ NewEnum, propriété

\[La propriété **\_ NewEnum** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe OidCollection**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La propriété **\_ NewEnum** récupère une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection. cette propriété est masquée dans Visual Basic scripting Edition (VBScript).

## <a name="syntax"></a>Syntaxe


```VB
OIDs._NewEnum As IUnknown
```



## <a name="property-value"></a>Valeur de la propriété

Une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection.

## <a name="remarks"></a>Remarques

cette propriété est automatiquement utilisée en interne lorsque vous utilisez la `For Each In` construction dans Visual Basic scripting Edition (VBScript).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**OID**](oids.md)
</dt> </dl>

 

 
