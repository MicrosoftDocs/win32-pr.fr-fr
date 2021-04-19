---
description: L’interface INonDelegatingUnknown est une version de IUnknown qui est renommée pour permettre la prise en charge de nondelegating et de la délégation d’interfaces IUnknown dans le même objet COM.
ms.assetid: a2faf9d1-2130-4c6c-8fcd-3e118d592b7f
title: INonDelegatingUnknown (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INonDelegatingUnknown
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 13e93d5ba083706ee361addeb4db2157471cbe25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543898"
---
# <a name="inondelegatingunknown"></a>INonDelegatingUnknown

L' `INonDelegatingUnknown` interface est une version de **IUnknown** qui est renommée pour permettre la prise en charge de la nondelegating et de la délégation des interfaces **IUnknown** dans le même objet com.

## <a name="syntax"></a>Syntaxe


```C++
interface INonDelegatingUnknown
{
    virtual HRESULT NonDelegatingQueryInterface) (REFIID riid, LPVOID *ppv) PURE;
    virtual ULONG NonDelegatingAddRef)(void) PURE;
    virtual ULONG NonDelegatingRelease)(void) PURE;
};
```



## <a name="remarks"></a>Notes

Pour utiliser `INonDelegatingUnknown` pour l’héritage multiple, procédez comme suit.

1.  Dérivez votre classe d’une interface, par exemple IMyInterface.
2.  Incluez [**Declare \_ IUnknown**](declare-iunknown.md) dans votre définition de classe pour déclarer des implémentations de **QueryInterface**, **AddRef** et **Release** qui appellent l’externe Unknown.
3.  Remplacez **NonDelegatingQueryInterface** pour exposer IMyInterface à l’aide d’un code tel que le suivant :
    ```C++
         if (riid == IID_IMyInterface) {
             return GetInterface((IMyInterface *) this, ppv);
         } else {
             return CUnknown::NonDelegatingQueryInterface(riid, ppv);
         }
    ```

    

4.  Déclarez et implémentez les fonctions membres de IMyInterface.

Pour utiliser `INonDelegatingUnknown` pour les interfaces imbriquées, procédez comme suit :

1.  Déclarez une classe dérivée de [**CUnknown**](cunknown.md).
2.  Incluez [**Declare \_ IUnknown**](declare-iunknown.md) dans votre définition de classe.
3.  Remplacez **NonDelegatingQueryInterface** pour exposer IMyInterface avec le code suivant :
    ```C++
         if (riid == IID_IMyInterface) {
             return GetInterface((IMyInterface *) this, ppv);
         } else {
             return CUnknown::NonDelegatingQueryInterface(riid, ppv);
         }
    ```

    

4.  Implémentez les fonctions membres de IMyInterface. Utilisez [**CUnknown :: GetOwner**](cunknown-getowner.md) pour accéder à la classe d’objets com.
5.  Dans votre classe d’objets COM, faites de la classe imbriquée un Friend de la classe d’objet COM, puis déclarez une instance de la classe imbriquée en tant que membre de la classe d’objets COM.

Étant donné que vous devez toujours passer l’externe Unknown et un **HRESULT** au constructeur [**CUnknown**](cunknown.md) , vous ne pouvez pas utiliser un constructeur par défaut. Vous devez transformer la variable membre en pointeur vers la classe et en faire un nouvel appel dans votre constructeur pour la créer réellement.

Remplacez le **NonDelegatingQueryInterface** par un code tel que le suivant :


```C++
     if (riid == IID_IMyInterface) {
         return m_pImplFilter->
            NonDelegatingQueryInterface(IID_IMyInterface, ppv);
     } else {
         return CUnknown::NonDelegatingQueryInterface(riid, ppv);
     }
```



Vous pouvez avoir des classes mixtes qui prennent en charge certaines interfaces via un héritage multiple et certaines interfaces via des classes imbriquées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>ComBase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions d’assistance COM**](com-helper-functions.md)
</dt> </dl>

 

 




