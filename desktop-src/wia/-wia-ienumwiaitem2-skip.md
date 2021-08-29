---
description: Ignore le nombre spécifié d’éléments au cours d’une énumération des objets IWiaItem2 disponibles.
ms.assetid: 7a5e9e1c-1e6e-4de0-9499-bf89e35c19aa
title: 'IEnumWiaItem2 :: Skip, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Skip
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: e8676f997ea509bc6a6632a38230b16cf5477ef807f0de25d1505afd462fe834
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814249"
---
# <a name="ienumwiaitem2skip-method"></a>IEnumWiaItem2 :: Skip, méthode

Ignore le nombre spécifié d’éléments au cours d’une énumération des objets [**IWiaItem2**](-wia-iwiaitem2.md) disponibles.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Skip(
  [in] ULONG cElt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cElt* \[ dans\]
</dt> <dd>

Type : **ULong**

Spécifie le nombre d’éléments à ignorer.

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



 

 




