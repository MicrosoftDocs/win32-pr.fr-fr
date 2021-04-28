---
description: 'Méthode CBasePin. SetMediaType : la méthode SetMediaType définit le type de média pour la connexion.'
ms.assetid: db32b33b-df71-4f46-b53f-d7e647f5f559
title: Méthode CBasePin. SetMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b61b6179aa6364ebddd940b8853e22d628463e56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095985"
---
# <a name="cbasepinsetmediatype-method"></a>Méthode CBasePin. SetMediaType

La `SetMediaType` méthode définit le type de média pour la connexion.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*crédit* 
</dt> <dd>

Pointeur vers un objet [**CMediaType**](cmediatype.md) qui spécifie le type de média.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne S \_ OK.

## <a name="remarks"></a>Notes 

Cette méthode établit le format d’une connexion de code confidentiel. Avant d’appeler cette méthode, le code PIN appelle la méthode [**CBasePin :: CheckMediaType**](cbasepin-checkmediatype.md) pour déterminer si le type de média est acceptable. Par conséquent, le paramètre *VPM* est supposé être un type de média acceptable.

Dans la classe de base, cette méthode définit la variable de membre [**CBasePin :: m \_ MT**](cbasepin-m-mt.md) et retourne S \_ OK. Une classe dérivée peut substituer cette méthode si elle requiert une notification lorsque le type de média est défini.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




