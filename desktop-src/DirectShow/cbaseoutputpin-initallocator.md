---
description: La méthode InitAllocator crée un allocateur de mémoire.
ms.assetid: a1fa0ffb-ed43-446d-811e-6c3594743592
title: CBaseOutputPin.Iniméthode tAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.InitAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ce1e8f8097ca88d0434f79c20e855d8b61798b5a1b0e32b6a38077e4c7aa1271
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652459"
---
# <a name="cbaseoutputpininitallocator-method"></a>CBaseOutputPin.Iniméthode tAllocator

La `InitAllocator` méthode crée un allocateur de mémoire.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT InitAllocator(
   IMemAllocator **ppAlloc
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppAlloc* 
</dt> <dd>

Adresse d’une variable qui reçoit un pointeur vers l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) de l’allocateur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK en cas de réussite, ou un code d’erreur de la fonction **CoCreateInstance** .

## <a name="remarks"></a>Remarques

Si la broche d’entrée ne fournit pas d’allocateur de mémoire, la méthode [**CBaseOutputPin ::D ecideallocator**](cbaseoutputpin-decideallocator.md) appelle cette méthode pour créer un allocateur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseOutputPin, classe**](cbaseoutputpin.md)
</dt> </dl>

 

 




