---
description: 'CBaseOutputPin. inactive, méthode : la méthode inactive indique au code confidentiel que le filtre n’est plus actif.'
ms.assetid: 14a020de-2102-4d49-8a34-d59abe6698d1
title: CBaseOutputPin. inactive, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc4901bba7f1e34d49ff5bafb7b291544157bd9c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096137"
---
# <a name="cbaseoutputpininactive-method"></a>CBaseOutputPin. inactive, méthode

La `Inactive` méthode notifie le code confidentiel que le filtre n’est plus actif.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Inactive();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                          | Description                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                 | Réussite.<br/>                          |
| <dl> <dt>**VFW \_ E \_ aucun \_ allocateur**</dt> </dl> | Aucun allocateur de mémoire n’est disponible.<br/> |



 

## <a name="remarks"></a>Notes 

Cette méthode remplace la méthode [**CBasePin :: inactive**](cbasepin-inactive.md) . Elle appelle la méthode [**IMemAllocator ::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) pour désallouer l’allocateur de mémoire.

Si vous substituez cette méthode, appelez la méthode de la classe de base à partir de votre méthode de substitution.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseOutputPin, classe**](cbaseoutputpin.md)
</dt> </dl>

 

 




