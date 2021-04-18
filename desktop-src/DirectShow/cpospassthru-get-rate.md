---
description: 'La \_ méthode obtenir le taux récupère la vitesse de lecture. Cette méthode implémente la méthode IMediaPosition :: obten \_ rate.'
ms.assetid: 216cbcef-4874-4565-abb0-8c8bf67fe23c
title: Méthode CPosPassThru.get_Rate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_Rate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 46e565f51d7c549f524f9e478b2a8326daf690a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522799"
---
# <a name="cpospassthruget_rate-method"></a>CPosPassThru. obtient la \_ méthode rate

La `get_Rate` méthode récupère la vitesse de lecture. Cette méthode implémente la méthode [**IMediaPosition :: obten \_ rate**](/windows/desktop/api/Control/nf-control-imediaposition-get_rate) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Rate(
   double *pdRate
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pdRate* 
</dt> <dd>

Pointeur vers une variable qui reçoit la vitesse de lecture.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur **HRESULT** de la broche connectée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPosPassThru, classe**](cpospassthru.md)
</dt> </dl>

 

 




