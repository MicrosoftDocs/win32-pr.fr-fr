---
description: La méthode GetAllocatorRequirements récupère les propriétés Allocator demandées par la broche d’entrée.
ms.assetid: 81564924-6d5b-4b2a-b549-e3f358f18371
title: Méthode CBaseInputPin. GetAllocatorRequirements (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.GetAllocatorRequirements
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0239d226ea57ed5953fa65b925eeffaa0b13df1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123774"
---
# <a name="cbaseinputpingetallocatorrequirements-method"></a>Méthode CBaseInputPin. GetAllocatorRequirements

La `GetAllocatorRequirements` méthode récupère les propriétés Allocator demandées par la broche d’entrée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetAllocatorRequirements(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pProps* 
</dt> <dd>

Pointeur vers une structure de [**\_ Propriétés Allocator**](/windows/win32/api/strmif/ns-strmif-allocator_properties) , qui est remplie avec les spécifications.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne E \_ NOTIMPL.

## <a name="remarks"></a>Notes

Lorsqu’une broche de sortie Initialise un allocateur de mémoire, elle peut appeler cette méthode pour déterminer si la broche d’entrée a des exigences de mémoire tampon. Pour plus d’informations, consultez [**CBaseOutputPin ::D ecideallocator**](cbaseoutputpin-decideallocator.md).

L’implémentation de cette méthode est facultative. Si le filtre a des exigences spécifiques en matière d’alignement ou de préfixe, substituez cette méthode.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseInputPin, classe**](cbaseinputpin.md)
</dt> </dl>

 

 




