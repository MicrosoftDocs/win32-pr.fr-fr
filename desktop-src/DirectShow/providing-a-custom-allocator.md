---
description: Fourniture d’un allocateur personnalisé
ms.assetid: 4ce2db4b-c901-43a5-b905-7d6d923c940b
title: Fourniture d’un allocateur personnalisé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e85a8d133ee5b686e25bc0d7d4a3e2444cb2791
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392520"
---
# <a name="providing-a-custom-allocator"></a><span data-ttu-id="55f67-103">Fourniture d’un allocateur personnalisé</span><span class="sxs-lookup"><span data-stu-id="55f67-103">Providing a Custom Allocator</span></span>

<span data-ttu-id="55f67-104">Cette section décrit comment fournir un allocateur personnalisé pour un filtre.</span><span class="sxs-lookup"><span data-stu-id="55f67-104">This section describes how to provide a custom allocator for a filter.</span></span> <span data-ttu-id="55f67-105">Seules les connexions [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) sont décrites, mais les étapes pour une connexion [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) sont similaires.</span><span class="sxs-lookup"><span data-stu-id="55f67-105">Only [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) connections are described, but the steps for an [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) connection are similar.</span></span>

<span data-ttu-id="55f67-106">Tout d’abord, définissez une classe C++ pour l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="55f67-106">First, define a C++ class for the allocator.</span></span> <span data-ttu-id="55f67-107">Votre allocateur peut dériver de l’une des classes Allocator standard, [**CBaseAllocator**](cbaseallocator.md) ou [**CMemAllocator**](cmemallocator.md), ou vous pouvez créer une classe Allocator entièrement nouvelle.</span><span class="sxs-lookup"><span data-stu-id="55f67-107">Your allocator can derive from one of the standard allocator classes, [**CBaseAllocator**](cbaseallocator.md) or [**CMemAllocator**](cmemallocator.md), or you can create an entirely new allocator class.</span></span> <span data-ttu-id="55f67-108">Si vous créez une nouvelle classe, elle doit exposer l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .</span><span class="sxs-lookup"><span data-stu-id="55f67-108">If you create a new class, it must expose the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

<span data-ttu-id="55f67-109">Les étapes restantes varient selon que votre allocateur appartient à une broche d’entrée ou à une broche de sortie sur votre filtre.</span><span class="sxs-lookup"><span data-stu-id="55f67-109">The remaining steps depend on whether your allocator belongs to an input pin or an output pin on your filter.</span></span> <span data-ttu-id="55f67-110">Les broches d’entrée jouent un rôle différent de celui des broches de sortie lors de la phase de négociation allocateur, car la broche de sortie sélectionne finalement l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="55f67-110">Input pins play a different role than output pins during the allocator negotiation phase, because the output pin ultimately selects the allocator.</span></span>

<span data-ttu-id="55f67-111">**Fourniture d’un allocateur personnalisé pour une broche d’entrée**</span><span class="sxs-lookup"><span data-stu-id="55f67-111">**Providing a Custom Allocator for an Input Pin**</span></span>

<span data-ttu-id="55f67-112">Pour fournir un allocateur pour une broche d’entrée, remplacez la méthode [**CBaseInputPin :: GetAllocator**](cbaseinputpin-getallocator.md) du code confidentiel d’entrée.</span><span class="sxs-lookup"><span data-stu-id="55f67-112">To provide an allocator for an input pin, override the input pin's [**CBaseInputPin::GetAllocator**](cbaseinputpin-getallocator.md) method.</span></span> <span data-ttu-id="55f67-113">Dans cette méthode, vérifiez la variable de membre **m \_ pAllocator** .</span><span class="sxs-lookup"><span data-stu-id="55f67-113">Within this method, check the **m\_pAllocator** member variable.</span></span> <span data-ttu-id="55f67-114">Si cette variable est non **null**, cela signifie que l’allocateur a déjà été sélectionné pour cette connexion, de sorte que la méthode **GetAllocator** doit retourner un pointeur vers cet allocateur.</span><span class="sxs-lookup"><span data-stu-id="55f67-114">If this variable is non-**NULL**, it means the allocator has already been selected for this connection, so the **GetAllocator** method must return a pointer to that allocator.</span></span> <span data-ttu-id="55f67-115">Si **m \_ pAllocator** a la **valeur null**, cela signifie que l’allocateur n’a pas été sélectionné, de sorte que la méthode **GetAllocator** doit retourner un pointeur vers l’allocateur préféré de la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="55f67-115">If **m\_pAllocator** is **NULL**, it means the allocator has not been selected, so the **GetAllocator** method should return a pointer to the input pin's preferred allocator.</span></span> <span data-ttu-id="55f67-116">Dans ce cas, créez une instance de votre allocateur personnalisé et retournez son pointeur [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .</span><span class="sxs-lookup"><span data-stu-id="55f67-116">In that case, create an instance of your custom allocator and return its [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) pointer.</span></span> <span data-ttu-id="55f67-117">Le code suivant montre comment implémenter la méthode **GetAllocator** :</span><span class="sxs-lookup"><span data-stu-id="55f67-117">The following code shows how to implement the **GetAllocator** method:</span></span>


```C++
STDMETHODIMP CMyInputPin::GetAllocator(IMemAllocator **ppAllocator)
{
    CheckPointer(ppAllocator, E_POINTER);
    if (m_pAllocator)  
    {
        // We already have an allocator, so return that one.
        *ppAllocator = m_pAllocator;
        (*ppAllocator)->AddRef();
        return S_OK;
    }

    // No allocator yet, so propose our custom allocator. The exact code
    // here will depend on your custom allocator class definition.
    HRESULT hr = S_OK;
    CMyAllocator *pAlloc = new CMyAllocator(&hr);
    if (!pAlloc)
    {
        return E_OUTOFMEMORY;
    }
    if (FAILED(hr))
    {
        delete pAlloc;
        return hr;
    }

    // Return the IMemAllocator interface to the caller.
    return pAlloc->QueryInterface(IID_IMemAllocator, (void**)ppAllocator);
}
```



<span data-ttu-id="55f67-118">Lorsque le filtre amont sélectionne un allocateur, il appelle la méthode [**IMemInputPin :: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) du code confidentiel d’entrée.</span><span class="sxs-lookup"><span data-stu-id="55f67-118">When the upstream filter selects an allocator, it calls the input pin's [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) method.</span></span> <span data-ttu-id="55f67-119">Substituez la méthode [**CBaseInputPin :: NotifyAllocator**](cbaseinputpin-notifyallocator.md) pour vérifier les propriétés Allocator.</span><span class="sxs-lookup"><span data-stu-id="55f67-119">Override the [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md) method to check the allocator properties.</span></span> <span data-ttu-id="55f67-120">Dans certains cas, la broche d’entrée peut rejeter l’allocateur s’il ne s’agit pas de votre allocateur personnalisé, même si cela peut entraîner l’échec de toute la connexion du pin.</span><span class="sxs-lookup"><span data-stu-id="55f67-120">In some cases, the input pin might reject the allocator if it is not your custom allocator, although this may cause the entire pin connection to fail.</span></span>

<span data-ttu-id="55f67-121">**Fourniture d’un allocateur personnalisé pour une broche de sortie**</span><span class="sxs-lookup"><span data-stu-id="55f67-121">**Providing a Custom Allocator for an Output Pin**</span></span>

<span data-ttu-id="55f67-122">Pour fournir un allocateur pour une broche de sortie, substituez la méthode [**CBaseOutputPin :: InitAllocator**](cbaseoutputpin-initallocator.md) pour créer une instance de votre allocateur :</span><span class="sxs-lookup"><span data-stu-id="55f67-122">To provide an allocator for an output pin, override the [**CBaseOutputPin::InitAllocator**](cbaseoutputpin-initallocator.md) method to create an instance of your allocator:</span></span>


```C++
HRESULT MyOutputPin::InitAllocator(IMemAllocator **ppAllocator)
{
    HRESULT hr = S_OK;
    CMyAllocator *pAlloc = new CMyAllocator(&hr);
    if (!pAlloc)
    {
        return E_OUTOFMEMORY;
    }

    if (FAILED(hr))
    {
        delete pAlloc;
        return hr;
    }

    // Return the IMemAllocator interface.
    return pAlloc->QueryInterface(IID_IMemAllocator, (void**)ppAllocator);
}
```



<span data-ttu-id="55f67-123">Par défaut, la classe [**CBaseOutputPin**](cbaseoutputpin.md) demande d’abord un allocateur à partir de la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="55f67-123">By default, the [**CBaseOutputPin**](cbaseoutputpin.md) class requests an allocator from the input pin first.</span></span> <span data-ttu-id="55f67-124">Si cet allocateur n’est pas approprié, la broche de sortie crée son propre allocateur.</span><span class="sxs-lookup"><span data-stu-id="55f67-124">If that allocator is not suitable, the output pin creates its own allocator.</span></span> <span data-ttu-id="55f67-125">Pour forcer la connexion à utiliser votre allocateur personnalisé, remplacez la méthode [**CBaseOutputPin ::D ecideallocator**](cbaseoutputpin-decideallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="55f67-125">To force the connection to use your custom allocator, override the [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md) method.</span></span> <span data-ttu-id="55f67-126">Toutefois, sachez que cela peut empêcher votre broche de sortie de se connecter à certains filtres, car l’autre filtre peut également nécessiter son propre allocateur personnalisé.</span><span class="sxs-lookup"><span data-stu-id="55f67-126">However, be aware that this can prevent your output pin from connecting with certain filters, because the other filter may also require its own custom allocator.</span></span> <span data-ttu-id="55f67-127">Une troisième option consiste à basculer l’ordre : essayez d’abord votre allocateur personnalisé, puis revenez à l’allocateur de l’autre filtre.</span><span class="sxs-lookup"><span data-stu-id="55f67-127">A third option is to switch the order: Try your custom allocator first, and then fall back to the other filter's allocator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="55f67-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="55f67-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55f67-129">Négociation des allocateurs</span><span class="sxs-lookup"><span data-stu-id="55f67-129">Negotiating Allocators</span></span>](negotiating-allocators.md)
</dt> </dl>

 

 



