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
ms.openlocfilehash: c741a6820d414d7a00ad0a9fef768d982f2335c9cb9d8417e42376ea243cc58b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076039"
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
| En-tête<br/>  | <dl> <dt>combase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




