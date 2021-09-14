---
description: La fonction GetPropertyInfo retourne un pointeur vers les informations de propriété d’un protocole donné.
ms.assetid: f65166ba-1d94-4d65-b9d7-edb84ada0826
title: GetPropertyInfo, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPropertyInfo
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 007332a85f170f865604526199681cad6d68cdcb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416743"
---
# <a name="getpropertyinfo-function"></a>GetPropertyInfo fonction)

La fonction **GetPropertyInfo** retourne un pointeur vers les informations de propriété d’un protocole donné.

## <a name="syntax"></a>Syntaxe


```C++
LPPROPERTYINFO WINAPI GetPropertyInfo(
  _In_ HPROPERTY hProperty
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hProperty* \[ dans\]
</dt> <dd>

Handle vers une propriété.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction réussit, la valeur de retour est un pointeur désignant la propriété.

Si la fonction échoue, la valeur de retour est **null**.

## <a name="remarks"></a>Notes

Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetPropertyInfo** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




