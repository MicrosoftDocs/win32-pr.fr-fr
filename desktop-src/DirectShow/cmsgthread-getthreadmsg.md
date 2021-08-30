---
description: Récupère un objet CMsg mis en file d’attente contenant une requête.
ms.assetid: 65b76121-c21c-4525-8dde-138783a4964e
title: Méthode CMsgThread. GetThreadMsg (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5badc43e2bcdebd5d251ce657f2ec61ae90ec9ea53f372634a4edeaf5cfc4db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831859"
---
# <a name="cmsgthreadgetthreadmsg-method"></a>Méthode CMsgThread. GetThreadMsg

Récupère un objet [**CMsg**](cmsg.md) mis en file d’attente contenant une requête.

## <a name="syntax"></a>Syntaxe


```C++
virtual void GetThreadMsg(
   CMsg *msg
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*msg* 
</dt> <dd>

Pointeur vers un objet [**CMsg**](cmsg.md) alloué.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette fonction membre est appelée à partir de la fonction [**ThreadProc**](camthread-threadproc.md) privée du thread de travail pour récupérer la fonction membre suivante. Le paramètre *MSG* doit pointer vers un objet [**CMsg**](cmsg.md) alloué qui sera rempli avec les paramètres de la requête suivante dans la file d’attente. S’il n’y a aucune demande en file d’attente, cette fonction membre se bloque jusqu’à ce que la requête suivante soit mise en file d’attente (par un appel à la fonction membre [**CMsgThread ::P utthreadmsg**](cmsgthread-putthreadmsg.md) ).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Msgthrd. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMsgThread, classe**](cmsgthread.md)
</dt> </dl>

 

 




