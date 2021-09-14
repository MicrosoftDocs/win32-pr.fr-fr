---
description: 'Méthode CBaseInputPin. NotifyAllocator : la méthode NotifyAllocator spécifie un allocateur pour la connexion. Cette méthode implémente la méthode IMemInputPin :: NotifyAllocator.'
ms.assetid: 16167bd5-2d33-4329-87ec-6a6c578e0060
title: Méthode CBaseInputPin. NotifyAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c63e448d0cf2d287a441a4983f6a2e06bd9b8151
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127223561"
---
# <a name="cbaseinputpinnotifyallocator-method"></a>Méthode CBaseInputPin. NotifyAllocator

La `NotifyAllocator` méthode spécifie un allocateur pour la connexion. Cette méthode implémente la méthode [**IMemInputPin :: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT NotifyAllocator(
   IMemAllocator *pAllocator,
   BOOL          bReadOnly
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pAllocator* 
</dt> <dd>

Pointeur vers l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) de l’allocateur.

</dd> <dt>

*bReadOnly* 
</dt> <dd>

Indicateur qui spécifie si les exemples de cet allocateur sont en lecture seule. Si la **valeur est true**, les exemples sont en lecture seule.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne S \_ OK.

## <a name="remarks"></a>Notes

Au cours de la connexion de code confidentiel, la broche de sortie choisit un allocateur et appelle cette méthode pour notifier la broche d’entrée. La broche de sortie peut utiliser l’allocateur que la broche d’entrée a proposée dans la méthode [**IMemInputPin :: GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) , ou elle peut fournir son propre allocateur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseInputPin, classe**](cbaseinputpin.md)
</dt> </dl>

 

 




