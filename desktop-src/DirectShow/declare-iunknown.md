---
description: La \_ macro DECLARE IUnknown déclare les trois méthodes de l’interface de base pour une nouvelle interface.
ms.assetid: 3bf8e830-c923-4c31-8855-88fa08f80422
title: DECLARE_IUNKNOWN (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DECLARE_IUNKNOWN
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4823c1b4bd4832b1047a732bc503f04b4da65483
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006656"
---
# <a name="declare_iunknown"></a>DÉCLARER \_ IUnknown

La macro **Declare \_ IUnknown** déclare les trois méthodes de l’interface de base pour une nouvelle interface.

**Syntaxe**

``` syntax
#define DECLARE_IUNKNOWN                                        \
    STDMETHODIMP QueryInterface(REFIID riid, void **ppv) {      \
        return GetOwner()->QueryInterface(riid,ppv);            \
    };                                                          \
    STDMETHODIMP_(ULONG) AddRef() {                             \
        return GetOwner()->AddRef();                            \
    };                                                          \
    STDMETHODIMP_(ULONG) Release() {                            \
        return GetOwner()->Release();                           \
    };
```

## <a name="remarks"></a>Notes

Quand vous créez une interface, elle doit dériver de **IUnknown**, qui a trois méthodes : **QueryInterface**, **AddRef** et **Release**. Cette macro simplifie le processus de déclaration en déclarant chacune de ces méthodes pour la nouvelle interface.

Cette macro fonctionne uniquement avec les classes qui dérivent, directement ou indirectement, de la classe [**CUnknown**](cunknown.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>combase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions d’assistance COM**](com-helper-functions.md)
</dt> <dt>

[**CUnknown :: GetOwner**](cunknown-getowner.md)
</dt> <dt>

[Comment implémenter IUnknown](how-to-implement-iunknown.md)
</dt> </dl>

 

 




