---
description: La méthode Allocator récupère un pointeur vers l’allocateur de mémoire.
ms.assetid: ac262502-eadc-482c-bc58-1e942889f0a7
title: CRendererInputPin. Allocator, méthode (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.Allocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9bf30b9d2aaad9f879baf5b0122589150ebff814a73f2f3c85c2ca72c6886308
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908469"
---
# <a name="crendererinputpinallocator-method"></a>CRendererInputPin. Allocator, méthode

La `Allocator` méthode récupère un pointeur vers l’allocateur de mémoire.

## <a name="syntax"></a>Syntaxe


```C++
IMemAllocator* Allocator() const;
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne un pointeur vers l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) de l’allocateur, ou **null**.

## <a name="remarks"></a>Remarques

Cette méthode retourne la variable de membre [**CBaseInputPin :: m \_ pAllocator**](cbaseinputpin-m-pallocator.md) . La méthode n’incrémente pas le nombre de références sur l’interface. Cette méthode est strictement une méthode d’accesseur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CRendererInputPin, classe**](crendererinputpin.md)
</dt> </dl>

 

 




