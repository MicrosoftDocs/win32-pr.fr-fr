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
ms.openlocfilehash: 99d0058a60b5cf5b362adb80855a788d9a597af6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521762"
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
| En-tête<br/>  | <dl> <dt>Wxdebug. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de débogage d’attente](wait-debugging-functions.md)
</dt> </dl>

 

 




