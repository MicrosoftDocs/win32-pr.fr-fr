---
description: 'La méthode AlterQuality avertit le filtre qu’une modification de qualité est demandée. Cette méthode remplace la méthode CTransformFilter :: AlterQuality.'
ms.assetid: 9a1d1379-8557-4b33-ab49-b5c6a684f685
title: Méthode CVideoTransformFilter. AlterQuality (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.AlterQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6cd2568bfc9518e2eeaf0399fa53796e305d246c511e5ee5bea1d3a1cacf7712
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998619"
---
# <a name="cvideotransformfilteralterquality-method"></a>Méthode CVideoTransformFilter. AlterQuality

La `AlterQuality` méthode notifie le filtre qu’une modification de qualité est demandée. Cette méthode remplace la méthode [**CTransformFilter :: AlterQuality**](ctransformfilter-alterquality.md) .

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT AlterQuality(
   Quality q
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*question* 
</dt> <dd>

Structure de [**qualité**](/windows/win32/api/strmif/ns-strmif-quality) qui contient le message de contrôle qualité.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne E \_ Fail.

## <a name="remarks"></a>Remarques

Cette méthode est appelée lorsque la broche de sortie reçoit un message de qualité (par le biais de la méthode [**IQualityControl :: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) ).

La valeur de fin de *q* est stockée dans la variable de membre **m \_ itrLate** . La valeur de retour de E \_ Fail indique que le convertisseur doit rattraper le problème en supprimant des frames, bien que la classe **CVideoTransformFilter** dépose également des frames dans les conditions appropriées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Vtrans. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CVideoTransformFilter, classe**](cvideotransformfilter.md)
</dt> <dt>

[**CVideoTransformFilter::ShouldSkipFrame**](cvideotransformfilter-shouldskipframe.md)
</dt> </dl>

 

 




