---
description: 'La méthode Run exécute le filtre. Cette méthode implémente la méthode IMediaFilter :: Run.'
ms.assetid: fab2cef7-cad1-4933-92a4-5f41cd947c2f
title: CBaseFilter. Run, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6259e6ce00b0a2f93e0b71d6b44d1c6ed4aa65eaadca21ed0a78f1d16d98a42b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793279"
---
# <a name="cbasefilterrun-method"></a>CBaseFilter. Run, méthode

La `Run` méthode exécute le filtre. Cette méthode implémente la méthode [**IMediaFilter :: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*tStart* 
</dt> <dd>

Temps de référence correspondant au temps de flux 0.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’erreur.

## <a name="remarks"></a>Remarques

Si le filtre est arrêté, cette méthode suspend le filtre en appelant la méthode [**CBaseFilter ::P ause**](cbasefilter-pause.md) . Il appelle ensuite la méthode [**CBasePin :: Run**](cbasepin-run.md) sur chacune des broches connectées du filtre. Enfin, il définit la variable de membre d' [**\_ État CBaseFilter :: m**](cbasefilter-m-state.md) sur State \_ Running.

Le temps de flux est calculé comme le temps de référence actuel moins *tStart*. Un échantillon de média avec un horodatage de zéro doit être affiché au moment du *tStart*.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseFilter, classe**](cbasefilter.md)
</dt> </dl>

 

 




