---
description: La méthode DecideAllocator sélectionne un allocateur de mémoire.
ms.assetid: cdc15b0e-ea1b-43aa-9267-95fa9db56ed5
title: Méthode CBaseOutputPin. DecideAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DecideAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 73d822450d635fe5f7620d59f39fcc7ed85fe1e2465f34af3ef561dfc2f3828f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814209"
---
# <a name="cbaseoutputpindecideallocator-method"></a>Méthode CBaseOutputPin. DecideAllocator

La `DecideAllocator` méthode sélectionne un allocateur de mémoire.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT DecideAllocator(
   IMemInputPin  *pPin,
   IMemAllocator **pAlloc
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pPin* 
</dt> <dd>

Pointeur vers l’interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) du code confidentiel d’entrée.

</dd> <dt>

*pAlloc* 
</dt> <dd>

Adresse d’une variable qui reçoit un pointeur vers l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) de l’allocateur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’erreur.

## <a name="remarks"></a>Remarques

Cette méthode est appelée à la fin du processus de connexion du code confidentiel. Il permet d'effectuer les opérations suivantes :

1.  Appelle la méthode [**IMemInputPin :: GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) pour récupérer les exigences en matière de mémoire tampon du code confidentiel d’entrée, le cas échéant.
2.  Appelle la méthode [**IMemInputPin :: GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) pour demander un allocateur à partir de la broche d’entrée. Si la broche d’entrée ne fournit pas d’allocateur, la broche de sortie en crée une en appelant la méthode de la classe [**CBaseOutputPin :: InitAllocator**](cbaseoutputpin-initallocator.md) .
3.  Appelle la méthode de la classe [**CBaseOutputPin ::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) , qui définit les propriétés Allocator. Il s’agit d’une méthode virtuelle pure ; la classe dérivée doit l’implémenter.
4.  Appelle la méthode [**IMemInputPin :: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) , qui avertit la broche d’entrée de l’allocateur utilisé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseOutputPin, classe**](cbaseoutputpin.md)
</dt> </dl>

 

 




