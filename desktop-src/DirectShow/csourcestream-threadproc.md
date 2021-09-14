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
ms.openlocfilehash: 6dc7d08643cc0ca76d3d05f0b9090f30200eb181
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010023"
---
# <a name="csourcestreamthreadproc-method"></a>CSourceStream. ThreadProc, méthode

La `ThreadProc` méthode est la procédure de thread pour le thread de travail. Cette méthode implémente la méthode [**CAMThread :: ThreadProc**](camthread-threadproc.md) virtuelle pure.

## <a name="syntax"></a>Syntaxe


```C++
virtual DWORD ThreadProc();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne 0 si le thread s’est terminé correctement ou 1 dans le cas contraire. Si la valeur de retour est 1, il est possible que les ressources du thread soient encore allouées.

## <a name="remarks"></a>Notes

Cette méthode attend indéfiniment les demandes de thread, en appelant la méthode [**CAMThread :: GetRequest**](camthread-getrequest.md) . Si elle reçoit une demande [**CSourceStream :: Run**](csourcestream-run.md) ou [**CSourceStream ::P ause**](csourcestream-pause.md) , elle appelle la méthode [**CSourceStream ::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) . La méthode **DoBufferProcessingLoop** transmet les données jusqu’à ce qu’elles reçoivent une demande [**CSourceStream :: Stop**](csourcestream-stop.md) . La procédure de thread s’arrête lorsqu’elle reçoit une demande [**CSourceStream :: Exit**](csourcestream-exit.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Source. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceStream, classe**](csourcestream.md)
</dt> </dl>

 

 




