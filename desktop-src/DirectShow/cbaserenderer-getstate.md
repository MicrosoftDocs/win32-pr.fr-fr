---
description: La méthode GetState récupère l’état du filtre (en cours d’exécution, arrêté ou suspendu).
ms.assetid: 5d35824c-2509-499a-bbb1-1fb916b51808
title: Méthode CBaseRenderer. GetState (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 532a41bb9e39f844b3a485fc236ae8d03450d45cdcb45d92c8cfa94d9af4a4bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118403408"
---
# <a name="cbaserenderergetstate-method"></a>Méthode CBaseRenderer. GetState

La `GetState` méthode récupère l’état du filtre (en cours d’exécution, arrêté ou suspendu).

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

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                                                | Description                                                    |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                       | Réussite.<br/>                                            |
| <dl> <dt>**\_ \_ état \_ intermédiaire de VFW S**</dt> </dl> | Le filtre passe à l’état indiqué.<br/> |
| <dl> <dt>**\_pointeur E**</dt> </dl>                  | Argument de pointeur **null** .<br/>                          |



 

## <a name="remarks"></a>Remarques

Cette méthode remplace la méthode [**CBaseFilter :: GetState**](cbasefilter-getstate.md) . Quand le convertisseur est suspendu, il ne termine pas la transition d’État tant qu’il n’a pas reçu d’exemple à restituer. Si le délai d’attente expire avant la fin de la transition d’État, la méthode retourne le niveau intermédiaire de l' \_ État VFW S \_ \_ .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




