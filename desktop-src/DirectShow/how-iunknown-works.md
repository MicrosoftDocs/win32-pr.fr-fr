---
description: Fonctionnement de IUnknown
ms.assetid: 926778a5-e941-4424-8bc0-b50c925fd08b
title: Fonctionnement de IUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a7549ce892e9c0dd3c82f1229a2440f1b930190
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108471"
---
# <a name="how-iunknown-works"></a><span data-ttu-id="c2686-103">Fonctionnement de IUnknown</span><span class="sxs-lookup"><span data-stu-id="c2686-103">How IUnknown Works</span></span>

<span data-ttu-id="c2686-104">Les méthodes dans **IUnknown** permettent à une application d’interroger les interfaces sur le composant et de gérer le nombre de références du composant.</span><span class="sxs-lookup"><span data-stu-id="c2686-104">The methods in **IUnknown** enable an application to query for interfaces on the component and manage the component's reference count.</span></span>

<span data-ttu-id="c2686-105">**Nombre de références**</span><span class="sxs-lookup"><span data-stu-id="c2686-105">**Reference Count**</span></span>

<span data-ttu-id="c2686-106">Le décompte de références est une variable interne, incrémentée dans la méthode **AddRef** et décrémentée dans la méthode **Release** .</span><span class="sxs-lookup"><span data-stu-id="c2686-106">The reference count is an internal variable, incremented in the **AddRef** method and decremented in the **Release** method.</span></span> <span data-ttu-id="c2686-107">Les classes de base gèrent le décompte de références et synchronisent l’accès au décompte de références entre plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="c2686-107">The base classes manage the reference count and synchronize access to the reference count among multiple threads.</span></span>

<span data-ttu-id="c2686-108">**Requêtes d’interface**</span><span class="sxs-lookup"><span data-stu-id="c2686-108">**Interface Queries**</span></span>

<span data-ttu-id="c2686-109">L’interrogation d’une interface est également simple.</span><span class="sxs-lookup"><span data-stu-id="c2686-109">Querying for an interface is also straightforward.</span></span> <span data-ttu-id="c2686-110">L’appelant passe deux paramètres : un identificateur d’interface (IID) et l’adresse d’un pointeur.</span><span class="sxs-lookup"><span data-stu-id="c2686-110">The caller passes two parameters: an interface identifier (IID), and the address of a pointer.</span></span> <span data-ttu-id="c2686-111">Si le composant prend en charge l’interface demandée, il définit le pointeur sur l’interface, incrémente son propre nombre de références et retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c2686-111">If the component supports the requested interface, it sets the pointer to the interface, increments its own reference count, and returns S\_OK.</span></span> <span data-ttu-id="c2686-112">Dans le cas contraire, elle définit le pointeur sur la **valeur null** et retourne E \_ nointerface.</span><span class="sxs-lookup"><span data-stu-id="c2686-112">Otherwise, it sets the pointer to **NULL** and returns E\_NOINTERFACE.</span></span> <span data-ttu-id="c2686-113">Le pseudo-code suivant illustre la structure générale de la méthode **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="c2686-113">The following pseudocode shows the general outline of the **QueryInterface** method.</span></span> <span data-ttu-id="c2686-114">L’agrégation de composants, décrite dans la section suivante, présente une complexité supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="c2686-114">Component aggregation, described in the next section, introduces some additional complexity.</span></span>


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



<span data-ttu-id="c2686-115">La seule différence entre la méthode **QueryInterface** d’un composant et la méthode **QueryInterface** d’une autre est la liste des IID que chaque composant teste.</span><span class="sxs-lookup"><span data-stu-id="c2686-115">The only difference between the **QueryInterface** method of one component and the **QueryInterface** method of another is the list of IIDs that each component tests.</span></span> <span data-ttu-id="c2686-116">Pour chaque interface que le composant prend en charge, le composant doit tester l’IID de cette interface.</span><span class="sxs-lookup"><span data-stu-id="c2686-116">For every interface that the component supports, the component must test for the IID of that interface.</span></span>

<span data-ttu-id="c2686-117">**Agrégation et délégation**</span><span class="sxs-lookup"><span data-stu-id="c2686-117">**Aggregation and Delegation**</span></span>

<span data-ttu-id="c2686-118">L’agrégation de composants doit être transparente pour l’appelant.</span><span class="sxs-lookup"><span data-stu-id="c2686-118">Component aggregation must be transparent to the caller.</span></span> <span data-ttu-id="c2686-119">Par conséquent, l’agrégat doit exposer une seule interface **IUnknown** , le composant agrégé reportant à l’implémentation du composant externe.</span><span class="sxs-lookup"><span data-stu-id="c2686-119">Therefore, the aggregate must expose a single **IUnknown** interface, with the aggregated component deferring to the outer component's implementation.</span></span> <span data-ttu-id="c2686-120">Dans le cas contraire, l’appelant voit deux interfaces **IUnknown** différentes dans le même agrégat.</span><span class="sxs-lookup"><span data-stu-id="c2686-120">Otherwise, the caller would see two different **IUnknown** interfaces in the same aggregate.</span></span> <span data-ttu-id="c2686-121">Si le composant n’est pas agrégé, il utilise sa propre implémentation.</span><span class="sxs-lookup"><span data-stu-id="c2686-121">If the component is not aggregated, it uses its own implementation.</span></span>

<span data-ttu-id="c2686-122">Pour prendre en charge ce comportement, le composant doit ajouter un niveau d’indirection.</span><span class="sxs-lookup"><span data-stu-id="c2686-122">To support this behavior, the component must add a level of indirection.</span></span> <span data-ttu-id="c2686-123">Une opération *IUnknown de délégation* délègue le travail à l’emplacement approprié : au composant externe, s’il y en a un, ou à la version interne du composant.</span><span class="sxs-lookup"><span data-stu-id="c2686-123">A *delegating IUnknown* delegates the work to the appropriate place: to the outer component, if there is one, or to the component's internal version.</span></span> <span data-ttu-id="c2686-124">Une *Nondelegating IUnknown* effectue le travail, comme décrit dans la section précédente.</span><span class="sxs-lookup"><span data-stu-id="c2686-124">A *nondelegating IUnknown* does the work, as described in the previous section.</span></span>

<span data-ttu-id="c2686-125">La version de délégation est publique et conserve le nom **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="c2686-125">The delegating version is public and keeps the name **IUnknown**.</span></span> <span data-ttu-id="c2686-126">La version nondelegating est renommée [**INonDelegatingUnknown**](inondelegatingunknown.md).</span><span class="sxs-lookup"><span data-stu-id="c2686-126">The nondelegating version is renamed [**INonDelegatingUnknown**](inondelegatingunknown.md).</span></span> <span data-ttu-id="c2686-127">Ce nom ne fait pas partie de la spécification COM, car il ne s’agit pas d’une interface publique.</span><span class="sxs-lookup"><span data-stu-id="c2686-127">This name is not part of the COM specification, because it is not a public interface.</span></span>

<span data-ttu-id="c2686-128">Lorsque le client crée une instance du composant, il appelle la méthode **IClassFactory :: CreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="c2686-128">When the client creates an instance of the component, it calls the **IClassFactory::CreateInstance** method.</span></span> <span data-ttu-id="c2686-129">Un paramètre est un pointeur vers l’interface **IUnknown** du composant d’agrégation, ou **null** si la nouvelle instance n’est pas agrégée.</span><span class="sxs-lookup"><span data-stu-id="c2686-129">One parameter is a pointer to the aggregating component's **IUnknown** interface, or **NULL** if the new instance is not aggregated.</span></span> <span data-ttu-id="c2686-130">Le composant utilise ce paramètre pour stocker une variable membre indiquant l’interface **IUnknown** à utiliser, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="c2686-130">The component uses this parameter to store a member variable indicating which **IUnknown** interface to use, as shown in the following example:</span></span>


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



<span data-ttu-id="c2686-131">Chaque méthode dans la délégation **IUnknown** appelle son équivalent nondelegating, comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="c2686-131">Each method in the delegating **IUnknown** calls its nondelegating counterpart, as shown in the following example:</span></span>


```C++
HRESULT QueryInterface(REFIID iid, void **ppv) 
{
    return m_pUnknown->QueryInterface(iid, ppv);
}
```



<span data-ttu-id="c2686-132">Par la nature de la délégation, les méthodes de délégation semblent identiques dans chaque composant.</span><span class="sxs-lookup"><span data-stu-id="c2686-132">By the nature of delegation, the delegating methods look identical in every component.</span></span> <span data-ttu-id="c2686-133">Seules les versions de nondelegating changent.</span><span class="sxs-lookup"><span data-stu-id="c2686-133">Only the nondelegating versions change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2686-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c2686-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2686-135">Comment implémenter IUnknown</span><span class="sxs-lookup"><span data-stu-id="c2686-135">How to Implement IUnknown</span></span>](how-to-implement-iunknown.md)
</dt> </dl>

 

 



