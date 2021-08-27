---
description: 'La méthode IsPageDirty indique si la page de propriétés a été modifiée depuis son activation ou depuis l’appel le plus récent à IPropertyPage :: apply. Cette méthode implémente la méthode IPropertyPage :: IsPageDirty.'
ms.assetid: 95eeec26-7dbb-4add-a827-6505b40afe48
title: Méthode CBasePropertyPage. IsPageDirty (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.IsPageDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72b818ce117990f6f91ee58b8605e9d8cff9734fa9114d7f6114ed11d53a9521
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108499"
---
# <a name="cbasepropertypageispagedirty-method"></a>Méthode CBasePropertyPage. IsPageDirty

La `IsPageDirty` méthode indique si la page de propriétés a été modifiée depuis son activation ou depuis l’appel le plus récent à **IPropertyPage :: apply**. Cette méthode implémente la méthode **IPropertyPage :: IsPageDirty** .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IsPageDirty();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK si [**CBasePropertyPage :: m \_ BDirty**](cbasepropertypage-m-bdirty.md) a la **valeur true**, ou la \_ valeur false dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Cprop. h (inclure Flux. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePropertyPage, classe**](cbasepropertypage.md)
</dt> </dl>

 

 




