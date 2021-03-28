---
title: Comment énumérer des adaptateurs
description: Cette rubrique montre comment utiliser Microsoft DirectX Graphics infrastructure (DXGI) pour énumérer les cartes graphiques disponibles sur un ordinateur.
ms.assetid: f8ef981c-363e-4ac8-8734-69c68f346950
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af16aba0131d93a5f72732931a68f132126b5d48
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990964"
---
# <a name="how-to-enumerate-adapters"></a><span data-ttu-id="22319-103">Comment : énumérer des adaptateurs</span><span class="sxs-lookup"><span data-stu-id="22319-103">How To: Enumerate Adapters</span></span>

<span data-ttu-id="22319-104">Cette rubrique montre comment utiliser Microsoft DirectX Graphics infrastructure (DXGI) pour énumérer les cartes graphiques disponibles sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="22319-104">This topic shows how to use Microsoft DirectX Graphics Infrastructure (DXGI) to enumerate the available graphics adapters on a computer.</span></span> <span data-ttu-id="22319-105">Direct3D 10 et 11 peuvent utiliser DXGI pour énumérer les adaptateurs.</span><span class="sxs-lookup"><span data-stu-id="22319-105">Direct3D 10 and 11 can use DXGI to enumerate adapters.</span></span>

<span data-ttu-id="22319-106">En général, vous devez énumérer les adaptateurs pour les raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="22319-106">You generally need to enumerate adapters for these reasons:</span></span>

-   <span data-ttu-id="22319-107">Pour déterminer le nombre de cartes graphiques installées sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="22319-107">To determine how many graphics adapters are installed on a computer.</span></span>
-   <span data-ttu-id="22319-108">Pour vous aider à choisir la carte à utiliser pour créer un appareil Direct3D.</span><span class="sxs-lookup"><span data-stu-id="22319-108">To help you choose which adapter to use to create a Direct3D device.</span></span>
-   <span data-ttu-id="22319-109">Pour récupérer un objet [**IDXGIAdapter**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) que vous pouvez utiliser pour récupérer les fonctionnalités de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="22319-109">To retrieve an [**IDXGIAdapter**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) object that you can use to retrieve device capabilities.</span></span>

<span data-ttu-id="22319-110">**Pour énumérer des adaptateurs**</span><span class="sxs-lookup"><span data-stu-id="22319-110">**To enumerate adapters**</span></span>

1.  <span data-ttu-id="22319-111">Créez un objet [**IDXGIFactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) en appelant la fonction [**CreateDXGIFactory**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory) .</span><span class="sxs-lookup"><span data-stu-id="22319-111">Create an [**IDXGIFactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) object by calling the [**CreateDXGIFactory**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory) function.</span></span> <span data-ttu-id="22319-112">L’exemple de code suivant montre comment initialiser un objet **IDXGIFactory** .</span><span class="sxs-lookup"><span data-stu-id="22319-112">The following code example demonstrates how to initialize an **IDXGIFactory** object.</span></span>
    ```
    IDXGIFactory * pFactory = NULL;

    CreateDXGIFactory(__uuidof(IDXGIFactory) ,(void**)&pFactory)
    ```

    

2.  <span data-ttu-id="22319-113">Énumérez chaque adaptateur en appelant la méthode [**IDXGIFactory :: EnumAdapters**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-enumadapters) .</span><span class="sxs-lookup"><span data-stu-id="22319-113">Enumerate through each adapter by calling the [**IDXGIFactory::EnumAdapters**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-enumadapters) method.</span></span> <span data-ttu-id="22319-114">Le paramètre *adapter* vous permet de spécifier un numéro d’index de base zéro de l’adaptateur à énumérer.</span><span class="sxs-lookup"><span data-stu-id="22319-114">The *Adapter* parameter allows you to specify a zero-based index number of the adapter to enumerate.</span></span> <span data-ttu-id="22319-115">Si aucun adaptateur n’est disponible à l’index spécifié, la méthode retourne l' [**\_ erreur dxgi \_ \_ introuvable**](/windows/desktop/direct3ddxgi/dxgi-error).</span><span class="sxs-lookup"><span data-stu-id="22319-115">If no adapter is available at the specified index, the method returns [**DXGI\_ERROR\_NOT\_FOUND**](/windows/desktop/direct3ddxgi/dxgi-error).</span></span>

    <span data-ttu-id="22319-116">L’exemple de code suivant montre comment énumérer les adaptateurs sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="22319-116">The following code example demonstrates how to enumerate through the adapters on a computer.</span></span>

    ```
    for (UINT i = 0; 
         pFactory->EnumAdapters(i, &pAdapter) != DXGI_ERROR_NOT_FOUND; 
         ++i) 
    { ... }
    ```

    

<span data-ttu-id="22319-117">L’exemple de code suivant montre comment énumérer tous les adaptateurs d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="22319-117">The following code example demonstrates how to enumerate all adapters on a computer.</span></span>

> [!Note]  
> <span data-ttu-id="22319-118">Pour Direct3D 11,0 et versions ultérieures, nous recommandons que les applications utilisent toujours [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1) et [**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1) à la place.</span><span class="sxs-lookup"><span data-stu-id="22319-118">For Direct3D 11.0 and later, we recommend that apps always use [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1) and [**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1) instead.</span></span>

 


```C++
std::vector <IDXGIAdapter*> EnumerateAdapters(void)
{
    IDXGIAdapter * pAdapter; 
    std::vector <IDXGIAdapter*> vAdapters; 
    IDXGIFactory* pFactory = NULL; 
    

    // Create a DXGIFactory object.
    if(FAILED(CreateDXGIFactory(__uuidof(IDXGIFactory) ,(void**)&pFactory)))
    {
        return vAdapters;
    }


    for ( UINT i = 0;
          pFactory->EnumAdapters(i, &pAdapter) != DXGI_ERROR_NOT_FOUND;
          ++i )
    {
        vAdapters.push_back(pAdapter); 
    } 


    if(pFactory)
    {
        pFactory->Release();
    }

    return vAdapters;

}
```



## <a name="related-topics"></a><span data-ttu-id="22319-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="22319-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22319-120">Comment utiliser Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="22319-120">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 