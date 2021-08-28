---
description: La méthode Create crée le thread.
ms.assetid: 453972eb-7cf6-43c6-820e-c1992675260e
title: CAMThread. Create, méthode (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Create
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 135af6dd12bb53a2fa1e7ec14425c12e1c0bcc99bf9c82ce7aeaccb72df544f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103319"
---
# <a name="camthreadcreate-method"></a>CAMThread. Create, méthode

La `Create` méthode crée le thread.

## <a name="syntax"></a>Syntaxe


```C++
BOOL Create();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

Cette méthode crée le thread, à l’aide de la méthode [**CAMThread :: InitialThreadProc**](camthread-initialthreadproc.md) pour la procédure de thread et `this` pour l’argument de thread.

La méthode échoue si le thread existe déjà.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAMThread, classe**](camthread.md)
</dt> </dl>

 

 




