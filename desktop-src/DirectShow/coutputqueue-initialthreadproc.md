---
description: 'La méthode InitialThreadProc appelle la méthode COutputQueue :: ThreadProc lorsque le thread est créé.'
ms.assetid: 6093f0c3-ec58-418d-bb8c-618163c43ac7
title: COutputQueue.Iniméthode tialThreadProc (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.InitialThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a80561ae652df7168ad09c1cf6e9fde767154e6c72a8fe5360a5d09c784941f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813589"
---
# <a name="coutputqueueinitialthreadproc-method"></a>COutputQueue.Iniméthode tialThreadProc

La `InitialThreadProc` méthode appelle la méthode [**COutputQueue :: ThreadProc**](coutputqueue-threadproc.md) lorsque le thread est créé.

## <a name="syntax"></a>Syntaxe


```C++
static DWORD WINAPI InitialThreadProc(
   LPVOID pv
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*va* 
</dt> <dd>

`this` dirigé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur retournée par la méthode [**COutputQueue :: ThreadProc**](coutputqueue-threadproc.md) .

## <a name="remarks"></a>Remarques

Cette méthode est la procédure de thread pour le thread de travail de l’objet. Le pointeur de l’objet `this` est le paramètre de thread. La méthode déréférence ce pour appeler **ThreadProc**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Outputq. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COutputQueue, classe**](coutputqueue.md)
</dt> </dl>

 

 




