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
ms.openlocfilehash: 57b085cd82c45fd78ddaa4794084cba775e1c80cd8b9e3b8df4c9680379ba462
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586369"
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

## <a name="return-value"></a>Valeur retournée

Retourne E \_ NOTIMPL.

## <a name="remarks"></a>Remarques

Lorsqu’une broche de sortie Initialise un allocateur de mémoire, elle peut appeler cette méthode pour déterminer si la broche d’entrée a des exigences de mémoire tampon. Pour plus d’informations, consultez [**CBaseOutputPin ::D ecideallocator**](cbaseoutputpin-decideallocator.md).

L’implémentation de cette méthode est facultative. Si le filtre a des exigences spécifiques en matière d’alignement ou de préfixe, substituez cette méthode.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseInputPin, classe**](cbaseinputpin.md)
</dt> </dl>

 

 




