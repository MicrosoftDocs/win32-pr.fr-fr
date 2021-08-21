---
description: La méthode OnThreadDestroy est appelée lorsque le thread de streaming est sur le point de quitter.
ms.assetid: a484b6d2-bce6-4a42-9176-2a6ce374e28b
title: Méthode CSourceStream. OnThreadDestroy (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadDestroy
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b71bd7ff9da79ed42ad7d36ff176a60687ca5fd0edcd6003d77c20084adc1b84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953698"
---
# <a name="csourcestreamonthreaddestroy-method"></a>Méthode CSourceStream. OnThreadDestroy

La `OnThreadDestroy` méthode est appelée lorsque le thread de diffusion en continu est sur le point de quitter.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT OnThreadDestroy();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Remarques

La procédure de thread, [**CSourceStream :: ThreadProc**](csourcestream-threadproc.md), appelle cette méthode avant de quitter. La méthode n’a aucun effet dans la classe de base ; elle est disponible pour la substitution de la classe dérivée. Si la classe dérivée retourne un code d’erreur, le thread se termine avec une erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Source. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceStream, classe**](csourcestream.md)
</dt> </dl>

 

 




