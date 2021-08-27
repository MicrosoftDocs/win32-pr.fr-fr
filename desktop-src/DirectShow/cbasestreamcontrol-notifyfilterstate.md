---
description: La méthode NotifyFilterState avertit le pin lorsque l’état du filtre change.
ms.assetid: 0eb3b0e5-9c44-464e-b4ca-bcded731e813
title: Méthode CBaseStreamControl. NotifyFilterState (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.NotifyFilterState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3433e5c40f86a9e333696774fe671eb7bb90d9803cb9cd6501d7971111e5d36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131419"
---
# <a name="cbasestreamcontrolnotifyfilterstate-method"></a>Méthode CBaseStreamControl. NotifyFilterState

La `NotifyFilterState` méthode notifie le code confidentiel lorsque l’état du filtre change.

## <a name="syntax"></a>Syntaxe


```C++
void NotifyFilterState(
   FILTER_STATE   new_state,
   REFERENCE_TIME tStart = 0
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nouvel \_ État* 
</dt> <dd>

Spécifie le nouvel État, en tant que membre de l’énumération de l' [**\_ État du filtre**](/windows/win32/api/strmif/ne-strmif-filter_state) .

</dd> <dt>

*tStart* 
</dt> <dd>

Spécifie l’heure de début. Si le nouvel état de filtre est état \_ en cours d’exécution, transmettez la valeur à partir de la méthode [**IMediaFilter :: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) . Sinon, utilisez la valeur par défaut.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode provoque l’arrêt de l’attente de la méthode [**CBaseStreamControl :: CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) . Appelez cette méthode chaque fois que le filtre propriétaire change d’État.

## <a name="examples"></a>Exemples


```C++
STDMETHODIMP CMyFilter::Run(REFERENCE_TIME tStart)
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Running, tStart);
   return CBaseFilter::Run(tStart); // Call the filter base class.
}

STDMETHODIMP CMyFilter::Pause()
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Paused);
   return CBaseFilter::Pause();
}

STDMETHODIMP CMyFilter::Stop()
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Stopped);
   return CBaseFilter::Stop();
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Strmctl. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseStreamControl, classe**](cbasestreamcontrol.md)
</dt> </dl>

 

 




