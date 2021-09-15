---
title: Agrégation
description: L’agrégation est le mécanisme de réutilisation d’objets dans lequel l’objet externe expose les interfaces de l’objet interne comme si elles étaient implémentées sur l’objet externe lui-même.
ms.assetid: 6845b114-8f43-47ad-acdf-b63d6008d221
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a4f11f69f5d7b14047a8138cba93bd503b645a3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525009"
---
# <a name="aggregation"></a>Agrégation

L’agrégation est le mécanisme de réutilisation d’objets dans lequel l’objet externe expose les interfaces de l’objet interne comme si elles étaient implémentées sur l’objet externe lui-même. Cela est utile lorsque l’objet externe délègue chaque appel à l’une de ses interfaces à la même interface dans l’objet interne. L’agrégation est disponible à des fins pratiques pour éviter une surcharge d’implémentation supplémentaire dans l’objet externe dans ce cas. L’agrégation est en fait un cas spécialisé de [relation contenant-contenu et de délégation](containment-delegation.md).

L’agrégation est presque aussi simple à implémenter que la relation contenant-contenu est, à l’exception des trois fonctions [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) : [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)et [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Le piège est que du point de vue du client, toute fonction **IUnknown** sur l’objet externe doit affecter l’objet externe. Autrement dit, **AddRef** et **Release** affectent l’objet externe et **QueryInterface** expose toutes les interfaces disponibles sur l’objet externe. Toutefois, si l’objet externe expose simplement l’interface d’un objet interne comme lui-même, les membres **IUnknown** de cet objet interne appelés par le biais de cette interface se comportent différemment des membres **IUnknown** sur les interfaces de l’objet externe, ce qui constitue une violation absolue des règles et des propriétés régissant **IUnknown**.

La solution est que l’agrégation requiert une implémentation explicite de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) sur l’objet interne et la délégation des méthodes **IUnknown** de toute autre interface aux méthodes **IUnknown** de l’objet externe.

## <a name="creating-aggregable-objects"></a>Création d’objets Aggregable

La création d’objets pouvant être agrégés est facultative ; Toutefois, il est simple de faire et fournit des avantages significatifs. Les règles suivantes s’appliquent à la création d’un objet aggregable :

-   L’implémentation d’un objet aggregable (ou interne) de [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)et [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) pour son interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) contrôle le décompte de références de l’objet interne, et cette implémentation ne doit pas déléguer à l’objet externe inconnu (contrôle **IUnknown**).
-   L’implémentation d’un objet aggregable (ou interne) de [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)et [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) pour ses autres interfaces doit déléguer au contrôle [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) et ne doit pas affecter directement le décompte de références de l’objet interne.
-   L’interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interne doit implémenter [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) uniquement pour l’objet interne.
-   L’objet aggregable ne doit pas appeler [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) lorsqu’il contient une référence au pointeur de contrôle [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) .
-   Lorsque l’objet est créé, si une interface autre que [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) est demandée, la création doit échouer avec E \_ nointerface.

Le fragment de code suivant illustre une implémentation correcte d’un objet aggregable à l’aide de la méthode de classe imbriquée d’implémentation d’interfaces :


```C++
// CSomeObject is an aggregable object that implements 
// IUnknown and ISomeInterface 
class CSomeObject : public IUnknown 
{ 
    private: 
        DWORD        m_cRef;         // Object reference count 
        IUnknown*    m_pUnkOuter;    // Controlling IUnknown, no AddRef 
 
        // Nested class to implement the ISomeInterface interface 
        class CImpSomeInterface : public ISomeInterface 
        { 
            friend class CSomeObject ; 
            private: 
                DWORD    m_cRef;    // Interface ref-count, for debugging 
                IUnknown*    m_pUnkOuter;    // Controlling IUnknown 
            public: 
                CImpSomeInterface() { m_cRef = 0;   }; 
                ~ CImpSomeInterface(void) {}; 
 
                // IUnknown members delegate to the outer unknown 
                // IUnknown members do not control lifetime of object 
                STDMETHODIMP     QueryInterface(REFIID riid, void** ppv) 
                {    return m_pUnkOuter->QueryInterface(riid,ppv);   }; 
 
                STDMETHODIMP_(DWORD) AddRef(void) 
                {    return m_pUnkOuter->AddRef();   }; 
 
                STDMETHODIMP_(DWORD) Release(void) 
                {    return m_pUnkOuter->Release();   }; 
 
                // ISomeInterface members 
                STDMETHODIMP SomeMethod(void) 
                {    return S_OK;   }; 
        } ; 
        CImpSomeInterface m_ImpSomeInterface ; 
    public: 
        CSomeObject(IUnknown * pUnkOuter) 
        { 
            m_cRef=0; 
            // No AddRef necessary if non-NULL as we're aggregated. 
            m_pUnkOuter=pUnkOuter; 
            m_ImpSomeInterface.m_pUnkOuter=pUnkOuter; 
        } ; 
        ~CSomeObject(void) {} ; 
 
        // Static member function for creating new instances (don't use 
        // new directly). Protects against outer objects asking for 
        // interfaces other than Iunknown. 
        static HRESULT Create(IUnknown* pUnkOuter, REFIID riid, void **ppv) 
        { 
            CSomeObject*        pObj; 
            if (pUnkOuter != NULL && riid != IID_IUnknown) 
                return CLASS_E_NOAGGREGATION; 
            pObj = new CSomeObject(pUnkOuter); 
            if (pObj == NULL) 
                return E_OUTOFMEMORY; 
            // Set up the right unknown for delegation (the non-
            // aggregation case) 
            if (pUnkOuter == NULL) 
            {
                pObj->m_pUnkOuter = (IUnknown*)pObj ; 
                pObj->m_ImpSomeInterface.m_pUnkOuter = (IUnknown*)pObj;
            }
            HRESULT hr; 
            if (FAILED(hr = pObj->QueryInterface(riid, (void**)ppv))) 
                delete pObj ; 
            return hr; 
        } 
 
        // Inner IUnknown members, non-delegating 
        // Inner QueryInterface only controls inner object 
        STDMETHODIMP QueryInterface(REFIID riid, void** ppv) 
        { 
            *ppv=NULL; 
            if (riid == IID_IUnknown) 
                *ppv=this; 
            if (riid == IID_ISomeInterface) 
                *ppv=&m_ImpSomeInterface; 
            if (NULL==*ppv) 
                return ResultFromScode(E_NOINTERFACE); 
            ((IUnknown*)*ppv)->AddRef(); 
            return NOERROR; 
        } ; 
        STDMETHODIMP_(DWORD) AddRef(void) 
        {    return ++m_cRef; }; 
        STDMETHODIMP_(DWORD) Release(void) 
        { 
            if (--m_cRef != 0) 
                return m_cRef; 
            delete this; 
            return 0; 
        }; 
}; 
 
```



## <a name="aggregating-objects"></a>Agrégation d’objets

Lors du développement d’un objet aggregable, les règles suivantes s’appliquent :

-   Lors de la création de l’objet interne, l’objet externe doit demander explicitement son [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown).
-   L’objet externe doit protéger son implémentation de [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) de la réentrance avec un décompte de références artificielles autour de son code de destruction.
-   L’objet externe doit appeler sa méthode de [**mise à jour**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) **IUnknown** de contrôle s’il interroge un pointeur vers l’une des interfaces de l’objet interne. Pour libérer ce pointeur, l’objet externe appelle sa méthode de contrôle **IUnknown** [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) , suivie de **Release** sur le pointeur de l’objet interne.
    ```C++
    // Obtaining inner object interface pointer 
    pUnkInner->QueryInterface(IID_ISomeInterface, &pISomeInterface); 
    pUnkOuter->Release(); 
     
    // Releasing inner object interface pointer 
    pUnkOuter->AddRef(); 
    pISomeInterface->Release(); 
     
    ```

    

-   L’objet externe ne doit pas déléguer en aveugle une requête pour toute interface non reconnue à l’objet interne, à moins que ce comportement soit spécifiquement l’intention de l’objet externe.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Imbrication/délégation](containment-delegation.md)
</dt> </dl>

 

 