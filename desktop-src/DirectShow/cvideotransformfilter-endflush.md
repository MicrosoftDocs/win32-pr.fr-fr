---
description: 'La méthode EndFlush termine une opération de vidage. Cette méthode remplace la méthode CTransformFilter :: EndFlush.'
ms.assetid: e7dfc6f9-1630-426b-95b2-9814331b5e61
title: Méthode CVideoTransformFilter. EndFlush (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 359229e690715667d7bbfbe3d3a9134f41f5af9febc185885e08cde7d986896e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118155873"
---
# <a name="cvideotransformfilterendflush-method"></a>Méthode CVideoTransformFilter. EndFlush

La `EndFlush` méthode termine une opération de vidage. Cette méthode remplace la méthode [**CTransformFilter :: EndFlush**](ctransformfilter-endflush.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK en cas de réussite, ou un code d’erreur.

## <a name="remarks"></a>Remarques

Cette méthode réinitialise toutes les mesures de performances internes du filtre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Vtrans. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CVideoTransformFilter, classe**](cvideotransformfilter.md)
</dt> </dl>

 

 




