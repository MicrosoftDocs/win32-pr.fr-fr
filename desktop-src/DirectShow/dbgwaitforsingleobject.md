---
description: Attend qu’un objet soit signalé.
ms.assetid: 5fbcccd9-9db7-4834-852a-86f28218e92e
title: DbgWaitForSingleObject, fonction (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgWaitForSingleObject
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f5e8180c905cdb7d8d1024f22a85984c17c0e12e18971499d29ed1479a79498f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749349"
---
# <a name="dbgwaitforsingleobject-function"></a>DbgWaitForSingleObject fonction)

Attend qu’un objet soit signalé.

Dans une version Debug, cette fonction déclenche une assertion si l’intervalle de délai d’attente expire avant que l’objet soit signalé. Pour définir l’intervalle de délai d’attente, appelez la fonction [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) .

Dans une version commerciale, cette fonction est équivalente à la fonction **WaitForSingleObject** avec un intervalle de délai d’attente infini.

## <a name="syntax"></a>Syntaxe


```C++
DWORD DbgWaitForSingleObject(
   HANDLE h
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*h* 
</dt> <dd>

Handle de l’objet.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxdebug. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de débogage d’attente](wait-debugging-functions.md)
</dt> </dl>

 

 




