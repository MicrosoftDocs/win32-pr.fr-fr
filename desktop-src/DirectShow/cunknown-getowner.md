---
description: La méthode GetOwner récupère un pointeur vers l’interface IUnknown du composant propriétaire. Pour un composant agrégé, le propriétaire est le composant externe. Dans le cas contraire, le composant se trouve lui-même.
ms.assetid: 7d8af9d1-52c0-4f2b-9d05-6ddff85ab508
title: Méthode CUnknown. GetOwner (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.GetOwner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e3cb1cd1d5b183857b6d75db79ee0fcdc6cb2d30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540013"
---
# <a name="cunknowngetowner-method"></a>Méthode CUnknown. GetOwner

La `GetOwner` méthode récupère un pointeur vers l’interface **IUnknown** du composant propriétaire. Pour un composant agrégé, le propriétaire est le composant externe. Dans le cas contraire, le composant se trouve lui-même.

## <a name="syntax"></a>Syntaxe


```C++
LPUNKNOWN GetOwner();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne un pointeur vers l’interface de contrôle **IUnknown** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>ComBase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




