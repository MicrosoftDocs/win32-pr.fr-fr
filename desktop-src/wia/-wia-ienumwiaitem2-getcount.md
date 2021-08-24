---
description: Retourne le nombre d’éléments stockés par cet énumérateur.
ms.assetid: d374ec81-0bd5-4b5d-8002-e3b53476421a
title: 'IEnumWiaItem2 :: GetCount, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.GetCount
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 0a64a7c015f7c21ff19a736570aa104f0b229bc1b6561001b612045824f9a31d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882419"
---
# <a name="ienumwiaitem2getcount-method"></a>IEnumWiaItem2 :: GetCount, méthode

Retourne le nombre d’éléments stockés par cet énumérateur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetCount(
  [out] ULONG *cElt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cElt* \[ à\]
</dt> <dd>

Type : **ULong \***

Reçoit un pointeur vers un **ULong** qui reçoit le nombre d’éléments dans l’énumération.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




