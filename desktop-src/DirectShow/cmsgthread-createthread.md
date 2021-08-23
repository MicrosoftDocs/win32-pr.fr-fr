---
description: Crée un thread.
ms.assetid: 40785522-dc6e-41af-8b27-9e8875a0dd84
title: CMsgThread. CreateThread, méthode (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.CreateThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3681716af79d0c47ae08371caa2d03d236b9748d98b08098d7a6834a93ed9b2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831869"
---
# <a name="cmsgthreadcreatethread-method"></a>CMsgThread. CreateThread, méthode

Crée un thread.

## <a name="syntax"></a>Syntaxe


```C++
BOOL CreateThread();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs suivantes.



| Code de retour                                                                              | Description                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>VRAI * * * * *</dt> </dl>  | Le thread a été créé avec succès.<br/>     |
| <dl> <dt>FALSe * * * * *</dt> </dl> | Le thread n’a pas été créé avec succès.<br/> |



 

## <a name="remarks"></a>Remarques

Le thread se bloque jusqu’à ce qu’une demande soit mise en file d’attente (via la fonction membre [**CMsgThread ::P utthreadmsg**](cmsgthread-putthreadmsg.md) ), puis appelle la fonction membre [**CMsgThread :: ThreadMessageProc**](cmsgthread-threadmessageproc.md) avec chaque message.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Msgthrd. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMsgThread, classe**](cmsgthread.md)
</dt> </dl>

 

 




