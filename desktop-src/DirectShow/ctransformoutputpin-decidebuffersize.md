---
description: 'Méthode CTransformOutputPin. DecideBufferSize : la méthode DecideBufferSize définit les exigences de la mémoire tampon.'
ms.assetid: cdf9e384-623e-46a6-b123-d881fe21fb09
title: Méthode CTransformOutputPin. DecideBufferSize (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1bc84eaf5e95a19436de5429ce018352cdaa286e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084837"
---
# <a name="ctransformoutputpindecidebuffersize-method"></a>Méthode CTransformOutputPin. DecideBufferSize

La `DecideBufferSize` méthode définit les spécifications de la mémoire tampon.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pAlloc* 
</dt> <dd>

Pointeur vers l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) de l’allocateur.

</dd> <dt>

*ppropInputRequest* 
</dt> <dd>

Pointeur d’une structure de [**\_ Propriétés Allocator**](/windows/win32/api/strmif/ns-strmif-allocator_properties) qui contient les exigences de mémoire tampon du code confidentiel d’entrée.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Notes 

Cette méthode remplace la méthode [**CBaseOutputPin ::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) . Elle appelle la méthode virtuelle pure [**CTransformFilter ::D ecidebuffersize**](ctransformfilter-decidebuffersize.md) du filtre, que la classe dérivée du filtre doit implémenter.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




