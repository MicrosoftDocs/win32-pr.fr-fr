---
description: 'La méthode QueryId récupère l’identificateur de code confidentiel. Cette méthode implémente la méthode IPin :: QueryId.'
ms.assetid: b365a574-61b4-454c-b062-8826cbe10f03
title: CBasePin. QueryId, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa14fb933c89da0b0b6d2eebfab480b5508a3666
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127223537"
---
# <a name="cbasepinqueryid-method"></a>CBasePin. QueryId, méthode

La `QueryId` méthode récupère l’identificateur de code confidentiel. Cette méthode implémente la méthode [**IPIN :: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Id* 
</dt> <dd>

Pointeur vers l’identificateur de code confidentiel.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                   | Description                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Réussite.<br/>                   |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>       |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Argument de pointeur **null** .<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode retourne une copie de la variable membre [**CBasePin :: m \_ pname**](cbasepin-m-pname.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




