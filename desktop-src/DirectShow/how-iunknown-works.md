---
description: Fonctionnement de IUnknown
ms.assetid: 926778a5-e941-4424-8bc0-b50c925fd08b
title: Fonctionnement de IUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a7549ce892e9c0dd3c82f1229a2440f1b930190
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119865"
---
# <a name="how-iunknown-works"></a>Fonctionnement de IUnknown

Les méthodes dans **IUnknown** permettent à une application d’interroger les interfaces sur le composant et de gérer le nombre de références du composant.

**Nombre de références**

Le décompte de références est une variable interne, incrémentée dans la méthode **AddRef** et décrémentée dans la méthode **Release** . Les classes de base gèrent le décompte de références et synchronisent l’accès au décompte de références entre plusieurs threads.

**Requêtes d’interface**

L’interrogation d’une interface est également simple. L’appelant passe deux paramètres : un identificateur d’interface (IID) et l’adresse d’un pointeur. Si le composant prend en charge l’interface demandée, il définit le pointeur sur l’interface, incrémente son propre nombre de références et retourne S \_ OK. Dans le cas contraire, elle définit le pointeur sur la **valeur null** et retourne E \_ nointerface. Le pseudo-code suivant illustre la structure générale de la méthode **QueryInterface** . L’agrégation de composants, décrite dans la section suivante, présente une complexité supplémentaire.


```C++
if (IID == IID_IUnknown)
    set pointer to (IUnknown *)this
    AddRef
    return S_OK

else if (IID == IID_ISomeInterface)
    set pointer to (ISomeInterface *)this
    AddRef
    return S_OK

else if ... 

else
    set pointer to NULL
    return E_NOINTERFACE
```



La seule différence entre la méthode **QueryInterface** d’un composant et la méthode **QueryInterface** d’une autre est la liste des IID que chaque composant teste. Pour chaque interface que le composant prend en charge, le composant doit tester l’IID de cette interface.

**Agrégation et délégation**

L’agrégation de composants doit être transparente pour l’appelant. Par conséquent, l’agrégat doit exposer une seule interface **IUnknown** , le composant agrégé reportant à l’implémentation du composant externe. Dans le cas contraire, l’appelant voit deux interfaces **IUnknown** différentes dans le même agrégat. Si le composant n’est pas agrégé, il utilise sa propre implémentation.

Pour prendre en charge ce comportement, le composant doit ajouter un niveau d’indirection. Une opération *IUnknown de délégation* délègue le travail à l’emplacement approprié : au composant externe, s’il y en a un, ou à la version interne du composant. Une *Nondelegating IUnknown* effectue le travail, comme décrit dans la section précédente.

La version de délégation est publique et conserve le nom **IUnknown**. La version nondelegating est renommée [**INonDelegatingUnknown**](inondelegatingunknown.md). Ce nom ne fait pas partie de la spécification COM, car il ne s’agit pas d’une interface publique.

Lorsque le client crée une instance du composant, il appelle la méthode **IClassFactory :: CreateInstance** . Un paramètre est un pointeur vers l’interface **IUnknown** du composant d’agrégation, ou **null** si la nouvelle instance n’est pas agrégée. Le composant utilise ce paramètre pour stocker une variable membre indiquant l’interface **IUnknown** à utiliser, comme illustré dans l’exemple suivant :


```C++
CMyComponent::CMyComponent(IUnknown *pOuterUnkown)
{
    if (pOuterUnknown == NULL)
        m_pUnknown = (IUnknown *)(INonDelegatingUnknown *)this;
    else
        m_pUnknown = pOuterUnknown;

    [ ... more constructor code ... ]
}
```



Chaque méthode dans la délégation **IUnknown** appelle son équivalent nondelegating, comme indiqué dans l’exemple suivant :


```C++
HRESULT QueryInterface(REFIID iid, void **ppv) 
{
    return m_pUnknown->QueryInterface(iid, ppv);
}
```



Par la nature de la délégation, les méthodes de délégation semblent identiques dans chaque composant. Seules les versions de nondelegating changent.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comment implémenter IUnknown](how-to-implement-iunknown.md)
</dt> </dl>

 

 



