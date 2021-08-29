---
description: 'La méthode GetSyncSource récupère l’horloge de référence utilisée par le filtre. Cette méthode implémente la méthode IMediaFilter :: GetSyncSource.'
ms.assetid: b8c95838-bd6e-41c5-b3ab-71ebb33136f0
title: Méthode CBaseFilter. GetSyncSource (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 632350f925f843f05bdf7820bc8c14a4570f152afc741d5ed58f1827ad205251
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056549"
---
# <a name="cbasefiltergetsyncsource-method"></a>Méthode CBaseFilter. GetSyncSource

La `GetSyncSource` méthode récupère l’horloge de référence utilisée par le filtre. Cette méthode implémente la méthode [**IMediaFilter :: GetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSyncSource(
   IReferenceClock **pClock
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pClock* 
</dt> <dd>

Adresse d’une variable qui reçoit un pointeur vers l’interface [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) de l’horloge.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le \_ pointeur S ou OK \_ .

## <a name="remarks"></a>Remarques

Si le filtre n’utilise pas une horloge de référence, *\* pClock* a la valeur **null**. Lorsque la méthode est retournée, si *\* pClock* est non **null**, l’interface **IReferenceClock** a un nombre de références en attente. Veillez à le libérer lorsque vous avez terminé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseFilter, classe**](cbasefilter.md)
</dt> </dl>

 

 




