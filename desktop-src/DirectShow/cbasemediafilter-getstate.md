---
description: 'La méthode GetState récupère l’état de l’objet (en cours d’exécution, arrêté ou suspendu). Cette méthode implémente la méthode IMediaFilter :: GetState.'
ms.assetid: d4cc7e2b-5ea5-4165-842f-becc3a81cbce
title: Méthode CBaseMediaFilter. GetState (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2a4c70412311be5ea4843a823e961fae34de2974f7365f51286ff6da36e41dcb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966699"
---
# <a name="cbasemediafiltergetstate-method"></a>Méthode CBaseMediaFilter. GetState

La `GetState` méthode récupère l’état de l’objet (en cours d’exécution, arrêté ou suspendu). Cette méthode implémente la méthode [**IMediaFilter :: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) .

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

Pointeur vers une variable qui reçoit un membre du type énuméré d' [**\_ État de filtre**](/windows/win32/api/strmif/ne-strmif-filter_state) , indiquant l’état de l’objet.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le \_ pointeur S ou OK \_ .

## <a name="remarks"></a>Remarques

Dans la classe de base, toutes les transitions d’État sont synchrones et le paramètre *dwMilliSecsTimeout* est ignoré. Si une classe dérivée exécute des transitions d’État asynchrones, elle doit substituer cette méthode pour attendre pendant les transitions d’État, avec un délai d’attente de *dwMilliSecsTimeout* millisecondes.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseMediaFilter, classe**](cbasemediafilter.md)
</dt> </dl>

 

 




