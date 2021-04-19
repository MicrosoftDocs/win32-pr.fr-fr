---
description: Pointeur vers une fonction qui crée une instance de l’objet.
ms.assetid: 86859bf9-e16a-4494-bf1b-1d8ddbc1c805
title: 'CFactoryTemplate :: m_lpfnNew, membre (ComBase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lpfnNew
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2299f7a87f348ac8a5fa6c6d83b6a17fbf97ca28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539234"
---
# <a name="cfactorytemplatem_lpfnnew-member"></a>CFactoryTemplate :: m \_ lpfnNew, membre

Pointeur vers une fonction qui crée une instance de l’objet.

## <a name="syntax"></a>Syntaxe


```C++
LPFNNewCOMObject m_lpfnNew;
```



## <a name="remarks"></a>Notes

Dans votre DLL, déclarez une fonction statique qui retourne un pointeur vers une nouvelle instance de l’objet. Dans le modèle Factory, définissez la variable de membre **m \_ lpfnNew** sur l’adresse de cette fonction statique.

Le type de pointeur de fonction est [**LPFNNewCOMObject**](lpfnnewcomobject.md).

L’exemple suivant montre une fonction classique pour **m \_ lpfnNew**:


```C++
CUnknown * WINAPI CMyComponent::CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr) 
{
    CMyComponent *pNewObject = 
        new CMyComponent(NAME("My Component"), pUnk, pHr );

    if (pNewObject == NULL)  
    {
        *phr = E_OUTOFMEMORY;
    }
    return pNewObject;
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>ComBase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CFactoryTemplate, classe**](cfactorytemplate.md)
</dt> </dl>

 

 




