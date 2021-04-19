---
description: 'La méthode GetAllocatorRequirements récupère les propriétés Allocator demandées par le code confidentiel. Cette méthode implémente la méthode IMemInputPin :: GetAllocatorRequirements.'
ms.assetid: 1355facc-f863-44b2-9284-8f06f62d39a2
title: Méthode CTransInPlaceInputPin. GetAllocatorRequirements (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.GetAllocatorRequirements
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfa176cd5da0317821996593e19bb90396e82224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543271"
---
# <a name="ctransinplaceinputpingetallocatorrequirements-method"></a>Méthode CTransInPlaceInputPin. GetAllocatorRequirements

La `GetAllocatorRequirements` méthode récupère les propriétés Allocator demandées par le code confidentiel. Cette méthode implémente la méthode [**IMemInputPin :: GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) .

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

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                               | Description                                                                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | Succès<br/>                                                                                   |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl> | La broche de sortie n’est pas connectée ou la broche d’entrée en aval ne prend pas en charge la méthode.<br/> |
| <dl> <dt>**\_pointeur E**</dt> </dl> | Argument de pointeur **null**<br/>                                                                 |



 

## <a name="remarks"></a>Notes

Si la broche de sortie est connectée, cette méthode passe l’appel à la broche d’entrée en aval. Dans le cas contraire, elle retourne E \_ NOTIMPL.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transip. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransInPlaceInputPin, classe**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




