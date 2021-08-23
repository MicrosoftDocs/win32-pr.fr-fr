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
ms.openlocfilehash: b130bf38833951cad4f82fd559c0299d2aea86854ca0ab5545f3f2794ab9b4b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432469"
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

## <a name="remarks"></a>Remarques

Cette fonction membre effectue uniquement la journalisation des performances. Elle est appelée lorsque le thread est activé d’attendre dans la fenêtre, ou lorsque l’exemple suivant est dû à un rendu. Il peut ensuite être utilisé pour collecter des informations qui contrôlent la synchronisation.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseVideoRenderer, classe**](cbasevideorenderer.md)
</dt> </dl>

 

 




