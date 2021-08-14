---
description: La méthode EndRun bascule vers le mode arrêté ou suspendu.
ms.assetid: 2c41262c-a809-4f3b-898c-02c0891dc6f8
title: Méthode CCmdQueue. EndRun (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.EndRun
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2c5a20917c82ba26c941b063941e8667a3a30adce15176aed52362140a15ce90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757359"
---
# <a name="ccmdqueueendrun-method"></a>Méthode CCmdQueue. EndRun

La `EndRun` méthode bascule en mode arrêté ou suspendu.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT EndRun();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** qui dépend de l’implémentation.

## <a name="remarks"></a>Remarques

Le mappage de temps entre le temps de flux et l’heure de présentation n’est pas connu après l’appel de cette fonction membre. Appelez la fonction membre [**CCmdQueue :: Run**](ccmdqueue-run.md) pour effectuer ce mappage.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CCmdQueue, classe**](ccmdqueue.md)
</dt> </dl>

 

 




