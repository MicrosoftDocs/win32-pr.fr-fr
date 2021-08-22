---
description: La méthode de dévalidation annule l’allocation. Cette méthode implémente la méthode IMemAllocator ::D ecommit.
ms.assetid: 0c8d44e0-17ea-4f7f-be44-f9ae2e34fbef
title: CBaseAllocator. decommit, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Decommit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 614986a912f08d918d4fbbaf6b3eeeb0d3b2c3eabc47748351934a08b8280cca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017547"
---
# <a name="cbaseallocatordecommit-method"></a>CBaseAllocator. decommit, méthode

La `Decommit` méthode annule la validation de l’allocateur. Cette méthode implémente la méthode [**IMemAllocator ::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Decommit();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Remarques

Une fois cette méthode appelée, les appels à la méthode [**CBaseAllocator :: GetBuffer**](cbaseallocator-getbuffer.md) échouent. À mesure que des exemples sont publiés, ils sont retournés à la liste libre. Lorsque le dernier échantillon est retourné, l’allocateur appelle la méthode [**CBaseAllocator :: Free**](cbaseallocator-free.md) , qui libère la mémoire allouée. (Dans la classe de base, **Free** est une méthode virtuelle pure.)

De plus, cette méthode libère tous les threads qui sont bloqués sur les appels **GetBuffer** . Les appels à **GetBuffer** échouent.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseAllocator, classe**](cbaseallocator.md)
</dt> </dl>

 

 




