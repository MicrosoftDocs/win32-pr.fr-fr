---
description: 'Méthode CBaseOutputPin. CheckConnect : la méthode CheckConnect détermine si une connexion de code confidentiel est appropriée.'
ms.assetid: 50ab59ad-8ff7-4d7b-add3-b59203d93307
title: Méthode CBaseOutputPin. CheckConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca35cb98f279674285610fbd06b0399e93a68d59749fe4129475ab8bd970824a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658862"
---
# <a name="cbaseoutputpincheckconnect-method"></a>Méthode CBaseOutputPin. CheckConnect

La `CheckConnect` méthode détermine si une connexion de code confidentiel est appropriée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pPin* 
</dt> <dd>

Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) du code confidentiel d’entrée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** suivantes.



| Code de retour                                                                                               | Description                                                                 |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                      | Réussite.<br/>                                                         |
| <dl> <dt>**E \_ NOinterface**</dt> </dl>             | La broche d’entrée ne prend pas en charge [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin).<br/> |
| <dl> <dt>**VFW \_ E \_ sens non valide \_**</dt> </dl> | Les directions de code confidentiel ne sont pas compatibles.<br/>                               |



 

## <a name="remarks"></a>Remarques

Cette méthode appelle la méthode de classe de base [**CBasePin :: CheckConnect**](cbasepin-checkconnect.md) , puis interroge la broche d’entrée pour son interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseOutputPin, classe**](cbaseoutputpin.md)
</dt> </dl>

 

 




