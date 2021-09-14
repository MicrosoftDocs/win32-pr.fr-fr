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
ms.openlocfilehash: f20802836adb665614e2bbfb8cb79bdccd5a36ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127224641"
---
# <a name="ctransinplacefilterusingdifferentallocators-method"></a>Méthode CTransInPlaceFilter. UsingDifferentAllocators

La `UsingDifferentAllocators` méthode détermine si les broches d’entrée et de sortie utilisent des allocateurs différents.

## <a name="syntax"></a>Syntaxe


```C++
BOOL UsingDifferentAllocators() const;
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** si les broches d’entrée et de sortie utilisent différents allocators, ou **false** dans le cas contraire.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transip. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransInPlaceFilter, classe**](ctransinplacefilter.md)
</dt> </dl>

 

 




