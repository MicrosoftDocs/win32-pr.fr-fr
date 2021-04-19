---
description: 'La méthode Run exécute l’objet. Cette méthode implémente la méthode IMediaFilter :: Run.'
ms.assetid: a59180df-46b4-4c23-973f-2931d95ace55
title: CBaseMediaFilter. Run, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c4023be7731f9bae60576bc7002010eb0b51823
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528634"
---
# <a name="cbasemediafilterrun-method"></a>CBaseMediaFilter. Run, méthode

La `Run` méthode exécute l’objet. Cette méthode implémente la méthode [**IMediaFilter :: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) .

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

Retourne S \_ OK.

## <a name="remarks"></a>Notes

Si l’objet est arrêté, cette méthode suspend l’objet en appelant la méthode [**CBaseMediaFilter ::P ause**](cbasemediafilter-pause.md) . Il définit ensuite la variable de membre d' [**\_ État CBaseMediaFilter :: m**](cbasemediafilter-m-state.md) sur State \_ Running.

Le temps de flux est calculé comme le temps de référence actuel moins *tStart*. Un échantillon de média avec un horodatage de zéro doit être affiché au moment du *tStart*.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseMediaFilter, classe**](cbasemediafilter.md)
</dt> </dl>

 

 




