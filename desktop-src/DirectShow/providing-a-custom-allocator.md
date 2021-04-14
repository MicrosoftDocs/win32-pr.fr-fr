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
# <a name="providing-a-custom-allocator"></a>Fourniture d’un allocateur personnalisé

Cette section décrit comment fournir un allocateur personnalisé pour un filtre. Seules les connexions [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) sont décrites, mais les étapes pour une connexion [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) sont similaires.

Tout d’abord, définissez une classe C++ pour l’allocateur. Votre allocateur peut dériver de l’une des classes Allocator standard, [**CBaseAllocator**](cbaseallocator.md) ou [**CMemAllocator**](cmemallocator.md), ou vous pouvez créer une classe Allocator entièrement nouvelle. Si vous créez une nouvelle classe, elle doit exposer l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .

Les étapes restantes varient selon que votre allocateur appartient à une broche d’entrée ou à une broche de sortie sur votre filtre. Les broches d’entrée jouent un rôle différent de celui des broches de sortie lors de la phase de négociation allocateur, car la broche de sortie sélectionne finalement l’allocateur.

**Fourniture d’un allocateur personnalisé pour une broche d’entrée**

Pour fournir un allocateur pour une broche d’entrée, remplacez la méthode [**CBaseInputPin :: GetAllocator**](cbaseinputpin-getallocator.md) du code confidentiel d’entrée. Dans cette méthode, vérifiez la variable de membre **m \_ pAllocator** . Si cette variable est non **null**, cela signifie que l’allocateur a déjà été sélectionné pour cette connexion, de sorte que la méthode **GetAllocator** doit retourner un pointeur vers cet allocateur. Si **m \_ pAllocator** a la **valeur null**, cela signifie que l’allocateur n’a pas été sélectionné, de sorte que la méthode **GetAllocator** doit retourner un pointeur vers l’allocateur préféré de la broche d’entrée. Dans ce cas, créez une instance de votre allocateur personnalisé et retournez son pointeur [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) . Le code suivant montre comment implémenter la méthode **GetAllocator** :


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



Lorsque le filtre amont sélectionne un allocateur, il appelle la méthode [**IMemInputPin :: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) du code confidentiel d’entrée. Substituez la méthode [**CBaseInputPin :: NotifyAllocator**](cbaseinputpin-notifyallocator.md) pour vérifier les propriétés Allocator. Dans certains cas, la broche d’entrée peut rejeter l’allocateur s’il ne s’agit pas de votre allocateur personnalisé, même si cela peut entraîner l’échec de toute la connexion du pin.

**Fourniture d’un allocateur personnalisé pour une broche de sortie**

Pour fournir un allocateur pour une broche de sortie, substituez la méthode [**CBaseOutputPin :: InitAllocator**](cbaseoutputpin-initallocator.md) pour créer une instance de votre allocateur :


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



Par défaut, la classe [**CBaseOutputPin**](cbaseoutputpin.md) demande d’abord un allocateur à partir de la broche d’entrée. Si cet allocateur n’est pas approprié, la broche de sortie crée son propre allocateur. Pour forcer la connexion à utiliser votre allocateur personnalisé, remplacez la méthode [**CBaseOutputPin ::D ecideallocator**](cbaseoutputpin-decideallocator.md) . Toutefois, sachez que cela peut empêcher votre broche de sortie de se connecter à certains filtres, car l’autre filtre peut également nécessiter son propre allocateur personnalisé. Une troisième option consiste à basculer l’ordre : essayez d’abord votre allocateur personnalisé, puis revenez à l’allocateur de l’autre filtre.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Négociation des allocateurs](negotiating-allocators.md)
</dt> </dl>

 

 



