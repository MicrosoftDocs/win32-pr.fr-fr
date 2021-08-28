---
description: Fournit l’initialisation sur un thread.
ms.assetid: a9c330bb-0a2b-45bf-9b24-d03dd61d7dbf
title: Méthode CMsgThread. OnThreadInit (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.OnThreadInit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b9105bf8399b036421c5360c62a63d8c3fac44471adc13b9e8c224fb0eb84e8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831839"
---
# <a name="cmsgthreadonthreadinit-method"></a>Méthode CMsgThread. OnThreadInit

Fournit l’initialisation sur un thread.

## <a name="syntax"></a>Syntaxe


```C++
virtual void OnThreadInit();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Substituez cette fonction si vous souhaitez effectuer votre propre initialisation spécifique au démarrage du thread.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Msgthrd. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMsgThread, classe**](cmsgthread.md)
</dt> </dl>

 

 




