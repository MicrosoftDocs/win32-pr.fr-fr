---
description: La méthode IsActive détermine si l’objet est actif (en cours d’exécution ou en pause).
ms.assetid: 6531cf1f-e057-4094-9354-d5a32371c83c
title: CBaseMediaFilter. IsActive, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.IsActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6438850b90309b47fbe1fb76b1fd4f7baea8f48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542475"
---
# <a name="cbasemediafilterisactive-method"></a>CBaseMediaFilter. IsActive, méthode

La `IsActive` méthode détermine si l’objet est actif (en cours d’exécution ou en pause).

## <a name="syntax"></a>Syntaxe


```C++
BOOL IsActive();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si l’objet est en pause ou en cours d’exécution, ou **false** s’il est arrêté.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseMediaFilter, classe**](cbasemediafilter.md)
</dt> </dl>

 

 




