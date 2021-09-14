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
ms.openlocfilehash: 64f2d46ded16384e53e5281632bc0a064021f673
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007646"
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

## <a name="return-value"></a>Valeur de retour

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

 

 




