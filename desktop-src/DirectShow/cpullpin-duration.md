---
description: La méthode Duration récupère la durée du flux.
ms.assetid: 82fbd7f5-36dc-4e81-9ce5-9ee28adf73ef
title: CPullPin. Duration, méthode (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Duration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ecd05478f67934368aa6d1de84ae32a209ddcad6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007604"
---
# <a name="cpullpinduration-method"></a>CPullPin. Duration, méthode

La `Duration` méthode récupère la durée du flux.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Duration(
   REFERENCE_TIME *ptDuration
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ptDuration* 
</dt> <dd>

Pointeur vers une variable qui reçoit la durée, en octets multiplié par 10 millions.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne S \_ OK.

## <a name="remarks"></a>Notes

la durée est indéterminée jusqu’à ce que la méthode [**CPullPin :: Connecter**](cpullpin-connect.md) soit appelée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPullPin, classe**](cpullpin.md)
</dt> </dl>

 

 




