---
description: 'La méthode SetPageSite initialise la page de propriétés et fournit un pointeur vers l’interface IPropertyPageSite du frame de propriété. Cette méthode implémente la méthode IPropertyPage :: SetPageSite.'
ms.assetid: 16c4633f-2f91-4b1b-a47c-4ef945c3af00
title: Méthode CBasePropertyPage. SetPageSite (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.SetPageSite
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a165ff60971cef3d2373e0f07b2abee554308279
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542474"
---
# <a name="cbasepropertypagesetpagesite-method"></a>Méthode CBasePropertyPage. SetPageSite

La `SetPageSite` méthode initialise la page de propriétés et fournit un pointeur vers l’interface **IPropertyPageSite** du frame de propriété. Cette méthode implémente la méthode **IPropertyPage :: SetPageSite** .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetPageSite(
   IPropertyPageSite *pPageSite
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pPageSite* 
</dt> <dd>

Pointeur vers l’interface **IPropertyPageSite** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes.



| Code de retour                                                                                  | Description                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Opération réussie.<br/>            |
| <dl> <dt>**E \_ inattendu**</dt> </dl> | Erreur inattendue.<br/> |



 

## <a name="remarks"></a>Notes

La méthode stocke le pointeur *pPageSite* dans la variable membre [**CBasePropertyPage :: m \_ pPageSite**](cbasepropertypage-m-ppagesite.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Cprop. h (include streams. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePropertyPage, classe**](cbasepropertypage.md)
</dt> </dl>

 

 




