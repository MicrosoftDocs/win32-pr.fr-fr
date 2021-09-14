---
description: 'La méthode GetSyncSource récupère l’horloge de référence utilisée par l’objet. Cette méthode implémente la méthode IMediaFilter :: GetSyncSource.'
ms.assetid: 7e74d6ce-cd34-4345-8ff9-174e0acb243a
title: Méthode CBaseMediaFilter. GetSyncSource (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1e92c9d0fa5e486d7785ff8184ba4ce0dd42e5be
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127239309"
---
# <a name="cbasemediafiltergetsyncsource-method"></a>Méthode CBaseMediaFilter. GetSyncSource

La `GetSyncSource` méthode récupère l’horloge de référence utilisée par l’objet. Cette méthode implémente la méthode [**IMediaFilter :: GetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource) .

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

## <a name="return-value"></a>Valeur de retour

Retourne le \_ pointeur S ou OK \_ .

## <a name="remarks"></a>Notes

Si l’objet n’utilise pas une horloge de référence, *\* pClock* a la valeur **null**. Lorsque la méthode est retournée, si *\* pClock* est non **null**, l’interface **IReferenceClock** a un nombre de références en attente. Veillez à le libérer lorsque vous avez terminé.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseMediaFilter, classe**](cbasemediafilter.md)
</dt> </dl>

 

 




