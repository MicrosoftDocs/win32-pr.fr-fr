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
ms.openlocfilehash: dfc7b8660d838b6ad31dd298c509b6282ab61810
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543883"
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

## <a name="remarks"></a>Notes

Cette méthode est la procédure de thread pour le thread de travail de l’objet. Le pointeur de l’objet `this` est le paramètre de thread. La méthode déréférence ce pour appeler **ThreadProc**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Outputq. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COutputQueue, classe**](coutputqueue.md)
</dt> </dl>

 

 




