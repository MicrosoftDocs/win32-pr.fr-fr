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
ms.openlocfilehash: 5805112b19132045e0245ef7baf29cb5c844e290
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539617"
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

## <a name="remarks"></a>Notes

Dans les versions Debug, les fonctions [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) et [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) utilisent cette valeur comme intervalle de délai d’attente.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxdebug. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de débogage d’attente](wait-debugging-functions.md)
</dt> </dl>

 

 




