---
description: 'La méthode QueryAccept détermine si le code PIN accepte un type de média spécifié. Cette méthode implémente la méthode IPin :: QueryAccept.'
ms.assetid: 7aa25b45-5116-474b-afee-1eddc8b7fd2a
title: Méthode CBasePin. QueryAccept (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryAccept
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2c4a982f583d1780dbab37d982fd9a54601e141
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533269"
---
# <a name="cbasepinqueryaccept-method"></a>Méthode CBasePin. QueryAccept

La `QueryAccept` méthode détermine si le pin accepte un type de média spécifié. Cette méthode implémente la méthode [**IPIN :: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT QueryAccept(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*crédit* 
</dt> <dd>

Pointeur vers une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) qui spécifie le type de média.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK si le type de média est acceptable. Sinon, retourne S \_ false.

## <a name="remarks"></a>Notes

Dans la classe de base, cette méthode délègue à la méthode [**CBasePin :: CheckMediaType**](cbasepin-checkmediatype.md) . Si **CheckMediaType** échoue, `QueryAccept` retourne la \_ valeur false.

Cette méthode ne contient pas la section critique du pin ([**CBasePin :: m \_ pLock**](cbasepin-m-plock.md)). Si votre classe dérivée modifie dynamiquement l’ensemble des types de médias acceptables, vous devez substituer cette méthode pour contenir la section critique.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




