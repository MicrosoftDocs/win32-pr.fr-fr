---
description: 'Méthode CRenderedInputPin. EndFlush : la méthode EndFlush termine une opération de vidage. Cette méthode implémente la méthode IPin :: EndFlush.'
ms.assetid: 5c27bf76-6886-431d-9958-5064c53909ec
title: Méthode CRenderedInputPin. EndFlush (Amextra. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 723ba917d7fc9c0a1d7ac0bb0c2e8dcaf1510212b0811d6e608d10f3a0a88224
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108019"
---
# <a name="crenderedinputpinendflush-method"></a>Méthode CRenderedInputPin. EndFlush

La `EndFlush` méthode termine une opération de vidage. Cette méthode implémente la méthode [**IPIN :: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK en cas de réussite, ou un code d’erreur dans le cas contraire.

## <a name="remarks"></a>Remarques

Cette méthode efface tous les événements d' [**\_ achèvement EC**](ec-complete.md) en attente.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amextra. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CRenderedInputPin, classe**](crenderedinputpin.md)
</dt> </dl>

 

 




