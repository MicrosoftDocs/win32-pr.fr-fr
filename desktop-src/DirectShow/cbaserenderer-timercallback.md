---
description: La méthode TimerCallback est une méthode de rappel pour l’événement de minuterie de fin de flux.
ms.assetid: ed43d07a-1ece-43ab-8753-ab14fa388946
title: Méthode CBaseRenderer. TimerCallback (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.TimerCallback
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3d3164959ecaa701397b5550c43449884208df1110300b6a042879ac4f146584
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537429"
---
# <a name="cbaserenderertimercallback-method"></a>Méthode CBaseRenderer. TimerCallback

La `TimerCallback` méthode est une méthode de rappel pour l’événement de minuterie de fin de flux.

## <a name="syntax"></a>Syntaxe


```C++
void TimerCallback();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

La méthode [**CBaseRenderer :: SendEndOfStream**](cbaserenderer-sendendofstream.md) utilise un événement de minuteur pour planifier \_ des notifications complètes ec. La méthode **CBaseRenderer :: TimerCallback** est la fonction de rappel pour l’événement du minuteur. La `TimerCallback` méthode appelle à nouveau **SendEndOfStream** , et **SendEndOfStream** détermine s’il faut envoyer la \_ notification complète ce ou définir une autre minuterie.

La méthode [**CBaseRenderer :: ResetEndOfStreamTimer**](cbaserenderer-resetendofstreamtimer.md) annule l’événement du minuteur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




