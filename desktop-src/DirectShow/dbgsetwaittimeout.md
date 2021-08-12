---
description: Définit la valeur du délai d’attente du débogage. Ignoré dans les builds de vente au détail.
ms.assetid: d0f60d8b-34f2-44b2-bdd6-5e8e6f7806d8
title: DbgSetWaitTimeout, fonction (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgSetWaitTimeout
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67a5522184b9e88cd4b8ac9f23246f96c13ffad2175d625334de32d34c750e12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654021"
---
# <a name="dbgsetwaittimeout-function"></a>DbgSetWaitTimeout fonction)

Définit la valeur du délai d’attente du débogage. Ignoré dans les builds de vente au détail.

## <a name="syntax"></a>Syntaxe


```C++
void DbgSetWaitTimeout(
   DWORD dwTimeout
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwTimeout* 
</dt> <dd>

Valeur du délai d’attente en millisecondes, ou infinie pour attendre indéfiniment.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Dans les versions Debug, les fonctions [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) et [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) utilisent cette valeur comme intervalle de délai d’attente.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxdebug. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de débogage d’attente](wait-debugging-functions.md)
</dt> </dl>

 

 




