---
description: 'CBaseFilter. pause, méthode : la méthode pause interrompt le filtre. Cette méthode implémente la méthode IMediaFilter ::P ause.'
ms.assetid: cfb7d532-6c00-49a1-a48d-4dadaca39a0f
title: CBaseFilter. pause, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee91393a574d0135e66e5a9c1e1e6b0325a0b4de
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120087"
---
# <a name="cbasefilterpause-method"></a>CBaseFilter. pause, méthode

La `Pause` méthode suspend le filtre. Cette méthode implémente la méthode [**IMediaFilter ::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Pause();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur renvoyée

Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’erreur.

## <a name="remarks"></a>Notes 

Cette méthode appelle la méthode [**CBasePin :: active**](cbasepin-active.md) sur chacune des broches connectées du filtre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseFilter, classe**](cbasefilter.md)
</dt> </dl>

 

 




