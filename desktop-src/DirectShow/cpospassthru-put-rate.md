---
description: La méthode de taux de placement \_ définit la vitesse de lecture. Cette méthode implémente la méthode IMediaPosition ::p ut \_ rate.
ms.assetid: c077f344-de34-4f8a-8e08-6d7086a5a4f1
title: Méthode CPosPassThru.put_Rate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_Rate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21e7e654233f78adcda2addf73b87a178654872e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010061"
---
# <a name="cpospassthruput_rate-method"></a>Méthode de taux de CPosPassThru. put \_

La `put_Rate` méthode définit la vitesse de lecture. Cette méthode implémente la méthode [**IMediaPosition ::p ut \_ rate**](/windows/desktop/api/Control/nf-control-imediaposition-put_rate) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_Rate(
   double dRate
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dRate* 
</dt> <dd>

Vitesse de lecture. Ne doit pas être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne E \_ INVALIDARG si *dRate* est égal à zéro. Sinon, retourne la valeur **HRESULT** de la broche connectée.

## <a name="remarks"></a>Notes

Les taux négatifs indiquent une lecture inversée. Tous les supports ne prennent pas en charge la lecture inversée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPosPassThru, classe**](cpospassthru.md)
</dt> </dl>

 

 




