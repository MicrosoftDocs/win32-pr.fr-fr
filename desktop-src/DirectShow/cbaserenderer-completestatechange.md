---
description: La méthode CompleteStateChange détermine si une transition vers l’état suspendu est terminée.
ms.assetid: 505a0b31-deaa-46be-91e6-f9bc8e47dd3a
title: Méthode CBaseRenderer. CompleteStateChange (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CompleteStateChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 260cd5692e10fb6e6adaa3ed715944eb773064afaea68f5e0909fa08f45adfb9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872359"
---
# <a name="cbaserenderercompletestatechange-method"></a>Méthode CBaseRenderer. CompleteStateChange

La `CompleteStateChange` méthode détermine si une transition vers l’état suspendu est terminée.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT CompleteStateChange(
   FILTER_STATE OldState
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*OldState* 
</dt> <dd>

État avant la transition.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK si la transition est terminée. Sinon, retourne S \_ false.

## <a name="remarks"></a>Remarques

La méthode [**CBaseRenderer ::P ause**](cbaserenderer-pause.md) appelle cette méthode pour mettre à jour l’état de la transition d’État. En général, la transition vers suspendue ne se termine pas tant que le filtre n’a pas reçu d’exemple. Toutefois, dans certaines situations, la transition se termine immédiatement : par exemple, si le filtre n’est pas connecté ou si la fin du flux a été atteinte. Cette méthode vérifie les différents critères, puis appelle la méthode [**CBaseRenderer :: Ready**](cbaserenderer-ready.md) ou la méthode [**CBaseRenderer :: nochapy**](cbaserenderer-notready.md) pour mettre à jour l’état de transition.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




