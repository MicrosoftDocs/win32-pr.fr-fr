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
ms.openlocfilehash: c69c2e7d480f63542e146c73e56b9e692693f665
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540580"
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
| En-tête<br/>  | <dl> <dt>Cprop. h (include streams. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePropertyPage, classe**](cbasepropertypage.md)
</dt> </dl>

 

 




