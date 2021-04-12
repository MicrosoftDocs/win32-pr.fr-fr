---
title: Agrégation
description: L’agrégation est le mécanisme de réutilisation d’objets dans lequel l’objet externe expose les interfaces de l’objet interne comme si elles étaient implémentées sur l’objet externe lui-même.
ms.assetid: 6845b114-8f43-47ad-acdf-b63d6008d221
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a4f11f69f5d7b14047a8138cba93bd503b645a3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316535"
---
# <a name="aggregation"></a><span data-ttu-id="cde06-103">Agrégation</span><span class="sxs-lookup"><span data-stu-id="cde06-103">Aggregation</span></span>

<span data-ttu-id="cde06-104">L’agrégation est le mécanisme de réutilisation d’objets dans lequel l’objet externe expose les interfaces de l’objet interne comme si elles étaient implémentées sur l’objet externe lui-même.</span><span class="sxs-lookup"><span data-stu-id="cde06-104">Aggregation is the object reuse mechanism in which the outer object exposes interfaces from the inner object as if they were implemented on the outer object itself.</span></span> <span data-ttu-id="cde06-105">Cela est utile lorsque l’objet externe délègue chaque appel à l’une de ses interfaces à la même interface dans l’objet interne.</span><span class="sxs-lookup"><span data-stu-id="cde06-105">This is useful when the outer object delegates every call to one of its interfaces to the same interface in the inner object.</span></span> <span data-ttu-id="cde06-106">L’agrégation est disponible à des fins pratiques pour éviter une surcharge d’implémentation supplémentaire dans l’objet externe dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="cde06-106">Aggregation is available as a convenience to avoid extra implementation overhead in the outer object in this case.</span></span> <span data-ttu-id="cde06-107">L’agrégation est en fait un cas spécialisé de [relation contenant-contenu et de délégation](containment-delegation.md).</span><span class="sxs-lookup"><span data-stu-id="cde06-107">Aggregation is actually a specialized case of [containment/delegation](containment-delegation.md).</span></span>

<span data-ttu-id="cde06-108">L’agrégation est presque aussi simple à implémenter que la relation contenant-contenu est, à l’exception des trois fonctions [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) : [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)et [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="cde06-108">Aggregation is almost as simple to implement as containment is, except for the three [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) functions: [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref), and [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="cde06-109">Le piège est que du point de vue du client, toute fonction **IUnknown** sur l’objet externe doit affecter l’objet externe.</span><span class="sxs-lookup"><span data-stu-id="cde06-109">The catch is that from the client's perspective, any **IUnknown** function on the outer object must affect the outer object.</span></span> <span data-ttu-id="cde06-110">Autrement dit, **AddRef** et **Release** affectent l’objet externe et **QueryInterface** expose toutes les interfaces disponibles sur l’objet externe.</span><span class="sxs-lookup"><span data-stu-id="cde06-110">That is, **AddRef** and **Release** affect the outer object and **QueryInterface** exposes all the interfaces available on the outer object.</span></span> <span data-ttu-id="cde06-111">Toutefois, si l’objet externe expose simplement l’interface d’un objet interne comme lui-même, les membres **IUnknown** de cet objet interne appelés par le biais de cette interface se comportent différemment des membres **IUnknown** sur les interfaces de l’objet externe, ce qui constitue une violation absolue des règles et des propriétés régissant **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="cde06-111">However, if the outer object simply exposes an inner object's interface as its own, that inner object's **IUnknown** members called through that interface will behave differently than those **IUnknown** members on the outer object's interfaces, an absolute violation of the rules and properties governing **IUnknown**.</span></span>

<span data-ttu-id="cde06-112">La solution est que l’agrégation requiert une implémentation explicite de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) sur l’objet interne et la délégation des méthodes **IUnknown** de toute autre interface aux méthodes **IUnknown** de l’objet externe.</span><span class="sxs-lookup"><span data-stu-id="cde06-112">The solution is that aggregation requires an explicit implementation of [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) on the inner object and delegation of the **IUnknown** methods of any other interface to the outer object's **IUnknown** methods.</span></span>

## <a name="creating-aggregable-objects"></a><span data-ttu-id="cde06-113">Création d’objets Aggregable</span><span class="sxs-lookup"><span data-stu-id="cde06-113">Creating Aggregable Objects</span></span>

<span data-ttu-id="cde06-114">La création d’objets pouvant être agrégés est facultative ; Toutefois, il est simple de faire et fournit des avantages significatifs.</span><span class="sxs-lookup"><span data-stu-id="cde06-114">Creating objects that can be aggregated is optional; however, it is simple to do and provides significant benefits.</span></span> <span data-ttu-id="cde06-115">Les règles suivantes s’appliquent à la création d’un objet aggregable :</span><span class="sxs-lookup"><span data-stu-id="cde06-115">The following rules apply to creating an aggregable object:</span></span>

-   <span data-ttu-id="cde06-116">L’implémentation d’un objet aggregable (ou interne) de [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)et [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) pour son interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) contrôle le décompte de références de l’objet interne, et cette implémentation ne doit pas déléguer à l’objet externe inconnu (contrôle **IUnknown**).</span><span class="sxs-lookup"><span data-stu-id="cde06-116">The aggregable (or inner) object's implementation of [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref), and [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) for its [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface controls the inner object's reference count, and this implementation must not delegate to the outer object's unknown (the controlling **IUnknown**).</span></span>
-   <span data-ttu-id="cde06-117">L’implémentation d’un objet aggregable (ou interne) de [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)et [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) pour ses autres interfaces doit déléguer au contrôle [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) et ne doit pas affecter directement le décompte de références de l’objet interne.</span><span class="sxs-lookup"><span data-stu-id="cde06-117">The aggregable (or inner) object's implementation of [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref), and [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) for its other interfaces must delegate to the controlling [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) and must not directly affect the inner object's reference count.</span></span>
-   <span data-ttu-id="cde06-118">L’interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interne doit implémenter [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) uniquement pour l’objet interne.</span><span class="sxs-lookup"><span data-stu-id="cde06-118">The inner [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) must implement [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) only for the inner object.</span></span>
-   <span data-ttu-id="cde06-119">L’objet aggregable ne doit pas appeler [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) lorsqu’il contient une référence au pointeur de contrôle [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="cde06-119">The aggregable object must not call [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) when holding a reference to the controlling [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) pointer.</span></span>
-   <span data-ttu-id="cde06-120">Lorsque l’objet est créé, si une interface autre que [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) est demandée, la création doit échouer avec E \_ nointerface.</span><span class="sxs-lookup"><span data-stu-id="cde06-120">When the object is created, if any interface other than [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) is requested, the creation must fail with E\_NOINTERFACE.</span></span>

<span data-ttu-id="cde06-121">Le fragment de code suivant illustre une implémentation correcte d’un objet aggregable à l’aide de la méthode de classe imbriquée d’implémentation d’interfaces :</span><span class="sxs-lookup"><span data-stu-id="cde06-121">The following code fragment illustrates a correct implementation of an aggregable object by using the nested class method of implementing interfaces:</span></span>


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



## <a name="aggregating-objects"></a><span data-ttu-id="cde06-122">Agrégation d’objets</span><span class="sxs-lookup"><span data-stu-id="cde06-122">Aggregating Objects</span></span>

<span data-ttu-id="cde06-123">Lors du développement d’un objet aggregable, les règles suivantes s’appliquent :</span><span class="sxs-lookup"><span data-stu-id="cde06-123">When developing an aggregable object, the following rules apply:</span></span>

-   <span data-ttu-id="cde06-124">Lors de la création de l’objet interne, l’objet externe doit demander explicitement son [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="cde06-124">When creating the inner object, the outer object must explicitly ask for its [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown).</span></span>
-   <span data-ttu-id="cde06-125">L’objet externe doit protéger son implémentation de [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) de la réentrance avec un décompte de références artificielles autour de son code de destruction.</span><span class="sxs-lookup"><span data-stu-id="cde06-125">The outer object must protect its implementation of [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) from reentrancy with an artificial reference count around its destruction code.</span></span>
-   <span data-ttu-id="cde06-126">L’objet externe doit appeler sa méthode de  [**mise à jour**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) **IUnknown** de contrôle s’il interroge un pointeur vers l’une des interfaces de l’objet interne.</span><span class="sxs-lookup"><span data-stu-id="cde06-126">The outer object must call its controlling **IUnknown** [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method if it queries for a pointer to any of the inner object's interfaces.</span></span> <span data-ttu-id="cde06-127">Pour libérer ce pointeur, l’objet externe appelle sa méthode de contrôle **IUnknown** [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) , suivie de **Release** sur le pointeur de l’objet interne.</span><span class="sxs-lookup"><span data-stu-id="cde06-127">To free this pointer, the outer object calls its controlling **IUnknown** [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) method, followed by **Release** on the inner object's pointer.</span></span>
    ```C++
    // Obtaining inner object interface pointer 
    pUnkInner->QueryInterface(IID_ISomeInterface, &pISomeInterface); 
    pUnkOuter->Release(); 
     
    // Releasing inner object interface pointer 
    pUnkOuter->AddRef(); 
    pISomeInterface->Release(); 
     
    ```

    

-   <span data-ttu-id="cde06-128">L’objet externe ne doit pas déléguer en aveugle une requête pour toute interface non reconnue à l’objet interne, à moins que ce comportement soit spécifiquement l’intention de l’objet externe.</span><span class="sxs-lookup"><span data-stu-id="cde06-128">The outer object must not blindly delegate a query for any unrecognized interface to the inner object, unless that behavior is specifically the intention of the outer object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cde06-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cde06-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cde06-130">Imbrication/délégation</span><span class="sxs-lookup"><span data-stu-id="cde06-130">Containment/Delegation</span></span>](containment-delegation.md)
</dt> </dl>

 

 