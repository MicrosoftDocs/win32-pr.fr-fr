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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006697"
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

## <a name="return-value"></a>Valeur de retour

Retourne la valeur **HRESULT** de la broche connectée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPosPassThru, classe**](cpospassthru.md)
</dt> </dl>

 

 




