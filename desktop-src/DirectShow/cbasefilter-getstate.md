---
description: 'La méthode GetState récupère l’état du filtre (en cours d’exécution, arrêté ou suspendu). Cette méthode implémente la méthode IMediaFilter :: GetState.'
ms.assetid: e32e3a1d-857f-4db3-b52c-5b6b802ded42
title: Méthode CBaseFilter. GetState (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9b6ed61b8b1e72652e9590d11827322256d4923bd92405206e5c5419cd5e7ae5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017167"
---
# <a name="cbasefiltergetstate-method"></a>Méthode CBaseFilter. GetState

La `GetState` méthode récupère l’état du filtre (en cours d’exécution, arrêté ou suspendu). Cette méthode implémente la méthode [**IMediaFilter :: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetState(
   DWORD        dwMilliSecsTimeout,
   FILTER_STATE *State
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwMilliSecsTimeout* 
</dt> <dd>

Intervalle de délai d’attente, en millisecondes.

</dd> <dt>

*State* 
</dt> <dd>

Pointeur vers une variable qui reçoit un membre du type énuméré d' [**\_ État de filtre**](/windows/win32/api/strmif/ne-strmif-filter_state) , indiquant l’état du filtre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le \_ pointeur S ou OK \_ .

## <a name="remarks"></a>Remarques

Dans la classe de base, toutes les transitions d’État sont synchrones et le paramètre *dwMilliSecsTimeout* est ignoré. Si une classe dérivée exécute des transitions d’État asynchrones, elle doit substituer cette méthode pour attendre pendant les transitions d’État, avec un délai d’attente de *dwMilliSecsTimeout* millisecondes.

Si votre filtre ne remet pas de données pendant la suspension, substituez la `GetState` méthode pour retourner la valeur de VFW \_ S \_ ne pas \_ signaler lorsque le filtre est suspendu (voir [remise d’exemples](delivering-samples.md)). Par exemple :


```C++
CMyFilter::GetState(DWORD dw, FILTER_STATE *pState)
{
    CheckPointer(pState, E_POINTER);
    *pState = m_State;
    if (m_State == State_Paused)
        return VFW_S_CANT_CUE;
    else
        return S_OK;
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseFilter, classe**](cbasefilter.md)
</dt> </dl>

 

 




