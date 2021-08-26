---
description: La méthode SetAllocator spécifie un allocateur pour la connexion.
ms.assetid: 6b8e80f9-3b0d-498f-b1b0-bae491c25e81
title: Méthode CTransInPlaceOutputPin. SetAllocator (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.SetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 568a95df0d0cee39245c268fa1c49505531ddc84e1fd1542a1eae170e5c7d0da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053179"
---
# <a name="ctransinplaceoutputpinsetallocator-method"></a>Méthode CTransInPlaceOutputPin. SetAllocator

La `SetAllocator` méthode spécifie un allocateur pour la connexion.

## <a name="syntax"></a>Syntaxe


```C++
void SetAllocator(
   IMemAllocator *pAllocator
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pAllocator* 
</dt> <dd>

Pointeur vers l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) de l’allocateur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

La broche de sortie pour ce filtre ne fournit jamais d’allocateur. Cette méthode spécifie l’allocateur pour la broche de sortie. Elle définit la valeur de la variable membre [**CBaseOutputPin :: m \_ pAllocator**](cbaseoutputpin-m-pallocator.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transip. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransInPlaceOutputPin, classe**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




