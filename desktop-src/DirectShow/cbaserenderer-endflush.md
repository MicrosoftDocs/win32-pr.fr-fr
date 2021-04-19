---
description: La méthode EndFlush termine une opération de vidage.
ms.assetid: 4c30abbf-7351-4eee-af9a-9330f6d1aa08
title: Méthode CBaseRenderer. EndFlush (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bd565bfa21edb9945b901d8e315f3e1d1cd054f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106524064"
---
# <a name="cbaserendererendflush-method"></a>Méthode CBaseRenderer. EndFlush

La `EndFlush` méthode termine une opération de vidage.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT EndFlush();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Notes

La broche d’entrée du filtre appelle cette méthode lorsqu’elle reçoit un appel à la méthode [**IPIN :: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




