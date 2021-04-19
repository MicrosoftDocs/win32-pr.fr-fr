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
ms.openlocfilehash: cfa59ca6bed0539caa7eb650458c168999b0de5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541750"
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

## <a name="remarks"></a>Notes

La méthode [**CBaseRenderer :: SendEndOfStream**](cbaserenderer-sendendofstream.md) utilise un événement de minuteur pour planifier \_ des notifications complètes ec. La méthode **CBaseRenderer :: TimerCallback** est la fonction de rappel pour l’événement du minuteur. La `TimerCallback` méthode appelle à nouveau **SendEndOfStream** , et **SendEndOfStream** détermine s’il faut envoyer la \_ notification complète ce ou définir une autre minuterie.

La méthode [**CBaseRenderer :: ResetEndOfStreamTimer**](cbaserenderer-resetendofstreamtimer.md) annule l’événement du minuteur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




