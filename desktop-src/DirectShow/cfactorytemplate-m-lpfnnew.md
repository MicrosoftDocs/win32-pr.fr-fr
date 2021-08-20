---
description: 'CFactoryTemplate :: m_lpfnNew pointeur membre vers une fonction qui crée une instance de l’objet.'
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
ms.openlocfilehash: 5a08b0f1b3dc28b70e62866b58a952b12959f0a7f753d5e6b4c847489b52bfd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317719"
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
| En-tête<br/>  | <dl> <dt>combase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CFactoryTemplate, classe**](cfactorytemplate.md)
</dt> </dl>

 

 




