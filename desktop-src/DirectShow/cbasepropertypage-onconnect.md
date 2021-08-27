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
ms.openlocfilehash: edc5448a20320e9bf74da7511bf6ae9fb9d95facc9b7973bbcd688127b495fe8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056099"
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

## <a name="remarks"></a>Remarques

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
| En-tête<br/>  | <dl> <dt>Cprop. h (inclure Flux. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePropertyPage, classe**](cbasepropertypage.md)
</dt> </dl>

 

 




