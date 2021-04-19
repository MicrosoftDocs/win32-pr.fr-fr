---
description: La méthode SetSyncSource notifie la classe de base de l’horloge de référence actuelle.
ms.assetid: 056385ac-682c-456e-9a5f-86490bd6e05f
title: Méthode CBaseStreamControl. SetSyncSource (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60832d1bf7ceca59089875f10579d52cf2cfec4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539491"
---
# <a name="cbasestreamcontrolsetsyncsource-method"></a>Méthode CBaseStreamControl. SetSyncSource

La `SetSyncSource` méthode notifie la classe de base de l’horloge de référence actuelle.

## <a name="syntax"></a>Syntaxe


```C++
void SetSyncSource(
   IReferenceClock *pRefClock
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pRefClock* 
</dt> <dd>

Pointeur vers l’interface [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) de l’horloge de référence.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Appelez cette méthode à l’intérieur de la méthode [**IMediaFilter :: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) du filtre. La classe **CBaseStreamControl** utilise l’interface **IReferenceClock** pour s’assurer qu’elle n’ignore pas les exemples trop rapidement.

## <a name="examples"></a>Exemples


```C++
STDMETHODIMP CMyFilter::SetSyncSource(IReferenceClock *pClock)
{
    // Note: It's OK if pClock is NULL.

    m_pMyPin->SetSyncSource(pClock);
    return CBaseFilter::SetSyncSource(pClock);
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Strmctl. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseStreamControl, classe**](cbasestreamcontrol.md)
</dt> </dl>

 

 




