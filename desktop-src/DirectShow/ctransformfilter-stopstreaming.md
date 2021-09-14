---
description: La méthode StopStreaming est appelée lorsque le filtre bascule à l’état arrêté.
ms.assetid: cfebfed2-4105-4dea-8d47-60d6160ee337
title: Méthode CTransformFilter. StopStreaming (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.StopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4990b55ad87a4eb754af7101e762ce227a090993
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127234209"
---
# <a name="ctransformfilterstopstreaming-method"></a>Méthode CTransformFilter. StopStreaming

La `StopStreaming` méthode est appelée lorsque le filtre bascule à l’état arrêté.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT StopStreaming();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne S \_ OK.

## <a name="remarks"></a>Notes

Cette méthode n’a aucun effet dans la classe de base, mais la classe dérivée peut la substituer.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransformFilter, classe**](ctransformfilter.md)
</dt> </dl>

 

 




