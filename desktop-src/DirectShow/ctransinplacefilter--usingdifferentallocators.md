---
description: La méthode UsingDifferentAllocators détermine si les broches d’entrée et de sortie utilisent des allocateurs différents.
ms.assetid: 75feaa6e-6395-4d47-ae92-10a857f8764b
title: Méthode CTransInPlaceFilter. UsingDifferentAllocators (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.UsingDifferentAllocators
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0033c0f5ded1fe741d27397078367049d72061c40a993833f714686d9f8a96fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953418"
---
# <a name="ctransinplacefilterusingdifferentallocators-method"></a>Méthode CTransInPlaceFilter. UsingDifferentAllocators

La `UsingDifferentAllocators` méthode détermine si les broches d’entrée et de sortie utilisent des allocateurs différents.

## <a name="syntax"></a>Syntaxe


```C++
BOOL UsingDifferentAllocators() const;
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si les broches d’entrée et de sortie utilisent différents allocators, ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transip. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransInPlaceFilter, classe**](ctransinplacefilter.md)
</dt> </dl>

 

 




