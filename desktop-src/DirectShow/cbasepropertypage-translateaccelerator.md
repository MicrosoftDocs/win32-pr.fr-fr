---
description: 'La méthode TranslateAccelerator demande à la page de propriétés de traiter une séquence de touches. Cette méthode implémente la méthode IPropertyPage :: TranslateAccelerator.'
ms.assetid: 2da214c9-35dc-470c-9b7f-2f4ef6bcd40a
title: CBasePropertyPage. TranslateAccelerator, méthode (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.TranslateAccelerator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc86d50c5692f48c7fb00b45228b13c88c96137473cee3609013f782a0a2d7ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502839"
---
# <a name="cbasepropertypagetranslateaccelerator-method"></a>CBasePropertyPage. TranslateAccelerator, méthode

La `TranslateAccelerator` méthode indique à la page de propriétés de traiter une séquence de touches. Cette méthode implémente la méthode **IPropertyPage :: TranslateAccelerator** .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT TranslateAccelerator(
   LPMSG lpMsg
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpMsg* 
</dt> <dd>

Pointeur vers une structure **MSG** décrivant la séquence de touches à traiter.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne E \_ NOTIMPL.

## <a name="remarks"></a>Remarques

Substituez cette méthode si vous souhaitez fournir des accélérateurs de clavier pour la page de propriétés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Cprop. h (inclure Flux. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePropertyPage, classe**](cbasepropertypage.md)
</dt> </dl>

 

 




