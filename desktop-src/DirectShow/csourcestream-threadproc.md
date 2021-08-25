---
description: 'La méthode ThreadProc est la procédure de thread pour le thread de travail. Cette méthode implémente la méthode CAMThread :: ThreadProc virtuelle pure.'
ms.assetid: 8e66b609-d795-45a8-8fe5-774c659ee350
title: Méthode CSourceStream. ThreadProc (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10ef0d29ab46ada118dc97c2d767b8377556086b949b6b9969cf5671b51e5359
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915269"
---
# <a name="csourcestreamthreadproc-method"></a>CSourceStream. ThreadProc, méthode

La `ThreadProc` méthode est la procédure de thread pour le thread de travail. Cette méthode implémente la méthode [**CAMThread :: ThreadProc**](camthread-threadproc.md) virtuelle pure.

## <a name="syntax"></a>Syntaxe


```C++
virtual DWORD ThreadProc();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne 0 si le thread s’est terminé correctement ou 1 dans le cas contraire. Si la valeur de retour est 1, il est possible que les ressources du thread soient encore allouées.

## <a name="remarks"></a>Remarques

Cette méthode attend indéfiniment les demandes de thread, en appelant la méthode [**CAMThread :: GetRequest**](camthread-getrequest.md) . Si elle reçoit une demande [**CSourceStream :: Run**](csourcestream-run.md) ou [**CSourceStream ::P ause**](csourcestream-pause.md) , elle appelle la méthode [**CSourceStream ::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) . La méthode **DoBufferProcessingLoop** transmet les données jusqu’à ce qu’elles reçoivent une demande [**CSourceStream :: Stop**](csourcestream-stop.md) . La procédure de thread s’arrête lorsqu’elle reçoit une demande [**CSourceStream :: Exit**](csourcestream-exit.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Source. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceStream, classe**](csourcestream.md)
</dt> </dl>

 

 




