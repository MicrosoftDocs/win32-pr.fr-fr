---
description: La méthode OnApplyChanges est appelée lorsque l’utilisateur applique des modifications à la page de propriétés.
ms.assetid: 15a55644-b7bf-4c72-8e26-18fc4fb714b9
title: Méthode CBasePropertyPage. OnApplyChanges (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnApplyChanges
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cbcea308a8daaa8b9fdf15be765dc5d3a0df182c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525632"
---
# <a name="cbasepropertypageonapplychanges-method"></a>Méthode CBasePropertyPage. OnApplyChanges

La `OnApplyChanges` méthode est appelée lorsque l’utilisateur applique des modifications à la page de propriétés.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT OnApplyChanges();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

L’implémentation de la classe de base retourne S \_ OK.

## <a name="remarks"></a>Notes

La méthode [**CBasePropertyPage :: apply**](cbasepropertypage-apply.md) appelle `OnApplyChanges` si l’indicateur [**CBasePropertyPage :: m \_ bDirty**](cbasepropertypage-m-bdirty.md) a la **valeur true**. Remplacez `OnApplyChanges` pour traiter les modifications et réinitialisez **m \_ bDirty** sur **false**.

## <a name="examples"></a>Exemples


```C++
HRESULT CMyProp::OnApplyChanges(void)
{
    ASSERT(m_pOwningFilter != NULL);
    return m_pOwningFilter->SetSomeProperty(&m_lNewVal);
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Cprop. h (include streams. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePropertyPage, classe**](cbasepropertypage.md)
</dt> </dl>

 

 




