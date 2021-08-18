---
description: 'La méthode Help appelle l’aide de la page de propriétés. Cette méthode implémente la méthode IPropertyPage :: help.'
ms.assetid: 8fe72b2e-a9f1-435d-8eda-27056f112c6d
title: CBasePropertyPage. Help, méthode (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Help
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e2f97f7edd1e719eb44ff1d41929d7cb3864d8117eabb383b4318688adfa537f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955088"
---
# <a name="cbasepropertypagehelp-method"></a>CBasePropertyPage. Help, méthode

La `Help` méthode appelle l’aide de la page de propriétés. Cette méthode implémente la méthode **IPropertyPage :: help** .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Help(
   LPCWSTR lpszHelpDir
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpszHelpDir* 
</dt> <dd>

Pointeur vers la chaîne sous la clé **helpDir** dans les informations de CLSID de la page de propriétés dans le registre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne E \_ NOTIMPL.

## <a name="remarks"></a>Remarques

Dans la classe de base, la méthode retourne toujours E \_ NOTIMPL. Lorsque la méthode échoue, le frame appelle **IPropertyPage :: GetPageInfo** pour obtenir le nom du fichier d’aide et de l’identificateur de contexte. Par défaut, il s’agit de la **valeur null**. Par conséquent, pour fournir de l’aide, la classe dérivée peut substituer la méthode `Help` ou la méthode [**CBasePropertyPage :: GetPageInfo**](cbasepropertypage-getpageinfo.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Cprop. h (inclure Flux. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePropertyPage, classe**](cbasepropertypage.md)
</dt> </dl>

 

 




