---
description: La méthode OnDisconnect est appelée lorsque la page de propriétés doit libérer l’objet associé.
ms.assetid: 55bab0ca-587e-405c-9025-f391cf08a620
title: CBasePropertyPage. OnDisconnect, méthode (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnDisconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abd251d20ca82ad0374a613d9ee73f0eaee21d31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540344"
---
# <a name="cbasepropertypageondisconnect-method"></a>CBasePropertyPage. OnDisconnect, méthode

La `OnDisconnect` méthode est appelée lorsque la page de propriétés doit libérer l’objet associé.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT OnDisconnect();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

L’implémentation de la classe de base retourne S \_ OK.

## <a name="remarks"></a>Notes

La méthode [**CBasePropertyPage :: SetObjects**](cbasepropertypage-setobjects.md) appelle la `OnDisconnect` méthode. Substituez `OnDisconnect` pour libérer tous les pointeurs obtenus dans la méthode [**CBasePropertyPage :: OnConnect**](cbasepropertypage-onconnect.md) .

## <a name="examples"></a>Exemples


```C++
HRESULT CMyProp::OnDisconnect(void)
{
    if (m_pOwningFilter)
    {
        m_pOwningFilter->Release();
        m_pOwningFilter = NULL;
    }
    return S_OK;
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

 

 




