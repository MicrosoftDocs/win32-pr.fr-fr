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
ms.openlocfilehash: b87c8ba76928fbf0e465a8b6a3a0aaf4730759f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526793"
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

## <a name="remarks"></a>Notes

Dans la classe de base, la méthode retourne toujours E \_ NOTIMPL. Lorsque la méthode échoue, le frame appelle **IPropertyPage :: GetPageInfo** pour obtenir le nom du fichier d’aide et de l’identificateur de contexte. Par défaut, il s’agit de la **valeur null**. Par conséquent, pour fournir de l’aide, la classe dérivée peut substituer la méthode `Help` ou la méthode [**CBasePropertyPage :: GetPageInfo**](cbasepropertypage-getpageinfo.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Cprop. h (include streams. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePropertyPage, classe**](cbasepropertypage.md)
</dt> </dl>

 

 




