---
description: 'Méthode CBaseRenderer. GetPin : la méthode GetPin récupère un code confidentiel.'
ms.assetid: 665e1aaf-4491-4241-94c6-6ea356d7a665
title: Méthode CBaseRenderer. GetPin (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b7c30767b7cba68931bc1ddde4905c9b7bc2bc29
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999314"
---
# <a name="cbaserenderergetpin-method"></a>Méthode CBaseRenderer. GetPin

La `GetPin` méthode récupère un code confidentiel.

## <a name="syntax"></a>Syntaxe


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*n* 
</dt> <dd>

Numéro du code confidentiel spécifié. Doit être zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne le pointeur [**CBaseRenderer :: m \_ pInputPin**](cbaserenderer-m-pinputpin.md) .

## <a name="remarks"></a>Notes

Cette méthode implémente la méthode [**CBaseFilter :: GetPin**](cbasefilter-getpin.md) , qui est virtuelle pure dans la classe **CBaseFilter** . Le filtre prend en charge exactement un pin (la broche d’entrée). La première fois que cette méthode est appelée, elle crée le code confidentiel en tant que nouvel objet [**CRendererInputPin**](crendererinputpin.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




