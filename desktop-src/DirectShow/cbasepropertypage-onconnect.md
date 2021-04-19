---
description: La méthode OnConnect fournit un pointeur IUnknown vers l’objet associé à la page de propriétés.
ms.assetid: 74cae8e1-5347-4e3d-ba5f-6a4efec2ddae
title: CBasePropertyPage. OnConnect, méthode (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 38f83a7c491f1591cece8d5d85eb4525a1059d2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523451"
---
# <a name="cbasepropertypageonconnect-method"></a>CBasePropertyPage. OnConnect, méthode

La `OnConnect` méthode fournit un pointeur **IUnknown** vers l’objet associé à la page de propriétés.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT OnConnect(
   IUnknown *pUnknown
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pUnknown* 
</dt> <dd>

Pointeur vers l’interface **IUnknown** de l’objet.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

L’implémentation de la classe de base retourne S \_ OK.

## <a name="remarks"></a>Notes

La méthode [**CBasePropertyPage :: SetObjects**](cbasepropertypage-setobjects.md) appelle la `OnConnect` méthode. Substituez cette méthode pour stocker un pointeur vers l’objet spécifié par *pUnknown*. Vous pouvez soit stocker le pointeur *pUnknown* lui-même, soit demander ce pointeur pour d’autres interfaces. Si vous stockez le pointeur *pUnknown* , appelez **AddRef** avant `OnConnect` returns.

Dans la méthode [**CBasePropertyPage :: OnActivate**](cbasepropertypage-onactivate.md) , utilisez le pointeur stocké (ou les pointeurs) pour récupérer les valeurs initiales des propriétés de la boîte de dialogue. Dans la méthode [**CBasePropertyPage :: OnApplyChanges**](cbasepropertypage-onapplychanges.md) , appliquez toutes les modifications à l’objet. Libérez tous les pointeurs dans la méthode [**CBasePropertyPage :: OnDisconnect**](cbasepropertypage-ondisconnect.md) .

## <a name="examples"></a>Exemples


```C++
HRESULT CMyProp::OnConnect(IUnknown *pUnk)
{
    ASSERT(m_pOwningFilter == NULL);
    HRESULT hr;
    // Query pUnk for the filter's custom interface.
    hr = pUnk->QueryInterface(IID_ISomeCustomInterface,
             reinterpret_cast<void**>(&m_pOwningFilter));
    return hr;
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

 

 




