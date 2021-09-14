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
ms.openlocfilehash: 451078a6167ff7ca89ad4153c416826af8ac6d05
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111317"
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

## <a name="return-value"></a>Valeur de retour

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                                                | Description                                                    |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                       | Réussite.<br/>                                            |
| <dl> <dt>**\_ \_ état \_ intermédiaire de VFW S**</dt> </dl> | Le filtre passe à l’état indiqué.<br/> |
| <dl> <dt>**\_pointeur E**</dt> </dl>                  | Argument de pointeur **null** .<br/>                          |



 

## <a name="remarks"></a>Notes

Cette méthode remplace la méthode [**CBaseFilter :: GetState**](cbasefilter-getstate.md) . Quand le convertisseur est suspendu, il ne termine pas la transition d’État tant qu’il n’a pas reçu d’exemple à restituer. Si le délai d’attente expire avant la fin de la transition d’État, la méthode retourne le niveau intermédiaire de l' \_ État VFW S \_ \_ .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




