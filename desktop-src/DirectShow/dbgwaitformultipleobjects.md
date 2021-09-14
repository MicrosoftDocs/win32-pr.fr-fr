---
description: Attend qu’un ou plusieurs des objets spécifiés soient signalés.
ms.assetid: e60c98b6-a4d2-40de-8297-727404e3c387
title: DbgWaitForMultipleObjects, fonction (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgWaitForMultipleObjects
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e555afb4e6a82500876f11e6d1275e7de027f7e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006662"
---
# <a name="dbgwaitformultipleobjects-function"></a>DbgWaitForMultipleObjects fonction)

Attend qu’un ou plusieurs des objets spécifiés soient signalés.

Dans une version Debug, cette fonction déclenche une assertion si l’intervalle de délai d’attente expire avant que les objets ne soient signalés. Pour définir l’intervalle de délai d’attente, appelez la fonction [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) .

Dans une version commerciale, cette fonction est équivalente à la fonction **WaitForMultipleObjects** avec un intervalle de délai d’attente infini.

## <a name="syntax"></a>Syntaxe


```C++
DWORD DbgWaitForMultipleObjects(
   DWORD         nCount,
   CONST HANDLE  *lpHandles,
   BOOL          bWaitAll
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nCount* 
</dt> <dd>

Nombre d’objets.

</dd> <dt>

*lpHandles* 
</dt> <dd>

Tableau de handles aux objets, de taille *nCount*.

</dd> <dt>

*bWaitAll* 
</dt> <dd>

Valeur booléenne qui spécifie s’il faut attendre tous les objets. Si la **valeur est true**, la fonction attend que tous les objets soient signalés. Sinon, elle attend qu’au moins un objet soit signalé.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxdebug. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de débogage d’attente](wait-debugging-functions.md)
</dt> </dl>

 

 




