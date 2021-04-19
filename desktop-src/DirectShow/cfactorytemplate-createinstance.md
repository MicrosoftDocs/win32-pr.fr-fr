---
description: La méthode CreateInstance appelle la fonction de création d’objet pour la classe.
ms.assetid: 8a7d5c56-867d-432d-a0c2-97b8e3cf8a69
title: CFactoryTemplate. CreateInstance, méthode (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0f67ba528943bc2a468419fc84db44359745d4a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540545"
---
# <a name="cfactorytemplatecreateinstance-method"></a>CFactoryTemplate. CreateInstance, méthode

La `CreateInstance` méthode appelle la fonction de création d’objet pour la classe.

## <a name="syntax"></a>Syntaxe


```C++
CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pUnk* 
</dt> <dd>

Pointeur vers l’interface **IUnknown** d’agrégation.

</dd> <dt>

*phr* 
</dt> <dd>

Pointeur vers une variable qui reçoit une valeur **HRESULT** indiquant la réussite ou l’échec de la méthode.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une instance de l’objet de classe.

## <a name="remarks"></a>Notes

La méthode **IClassFactory :: CreateInstance** appelle cette méthode de classe. Cette méthode appelle la fonction vers laquelle pointe la variable membre [**CFactoryTemplate :: m \_ lpfnNew**](cfactorytemplate-m-lpfnnew.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>ComBase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CFactoryTemplate, classe**](cfactorytemplate.md)
</dt> </dl>

 

 




