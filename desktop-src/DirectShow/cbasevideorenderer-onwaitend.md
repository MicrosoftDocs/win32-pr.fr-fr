---
description: La méthode OnWaitEnd est appelée lorsqu’un délai d’attente se termine.
ms.assetid: 283627bb-599c-4711-abc4-b5f92dfd29a5
title: Méthode CBaseVideoRenderer. OnWaitEnd (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnWaitEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36377565556a759c9268ef1bf31ff7774933ccc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523903"
---
# <a name="cbasevideorendereronwaitend-method"></a>Méthode CBaseVideoRenderer. OnWaitEnd

La méthode OnWaitEnd est appelée lorsqu’un délai d’attente se termine.

## <a name="syntax"></a>Syntaxe


```C++
void OnWaitEnd();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette fonction membre effectue uniquement la journalisation des performances. Elle est appelée lorsque le thread est activé d’attendre dans la fenêtre, ou lorsque l’exemple suivant est dû à un rendu. Il peut ensuite être utilisé pour collecter des informations qui contrôlent la synchronisation.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseVideoRenderer, classe**](cbasevideorenderer.md)
</dt> </dl>

 

 




