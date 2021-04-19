---
title: Utilisation de la mise en cache
description: Cette rubrique contient un exemple de code qui montre comment utiliser les fonctionnalités de mise en cache (ou d’extraction en bloc) de l’arborescence Microsoft UI Automation.
ms.assetid: d72fa637-35ca-4c28-922d-263f469cb1c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8758621a8499202b820a6ffc3459fade57c2a485
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510002"
---
# <a name="how-to-use-caching"></a><span data-ttu-id="15f11-103">Utilisation de la mise en cache</span><span class="sxs-lookup"><span data-stu-id="15f11-103">How to Use Caching</span></span>

<span data-ttu-id="15f11-104">Cette rubrique contient un exemple de code qui montre comment utiliser les fonctionnalités de mise en cache (ou d’extraction en bloc) de l’arborescence Microsoft UI Automation.</span><span class="sxs-lookup"><span data-stu-id="15f11-104">This topic contains example code that shows how to use the caching (or bulk fetching) capabilities of Microsoft UI Automation tree.</span></span> <span data-ttu-id="15f11-105">Il aborde les sujets suivants :</span><span class="sxs-lookup"><span data-stu-id="15f11-105">It discusses the following topics:</span></span>

-   [<span data-ttu-id="15f11-106">Récupération des propriétés et des modèles de contrôle dans le cache</span><span class="sxs-lookup"><span data-stu-id="15f11-106">Fetching Properties and Control Patterns into the Cache</span></span>](#fetching-properties-and-control-patterns-into-the-cache)
-   [<span data-ttu-id="15f11-107">Récupération des propriétés et des modèles de contrôle à partir du cache</span><span class="sxs-lookup"><span data-stu-id="15f11-107">Retrieving Properties and Control Patterns from the Cache</span></span>](#retrieving-properties-and-control-patterns-from-the-cache)
-   [<span data-ttu-id="15f11-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="15f11-108">Related topics</span></span>](#related-topics)

## <a name="fetching-properties-and-control-patterns-into-the-cache"></a><span data-ttu-id="15f11-109">Récupération des propriétés et des modèles de contrôle dans le cache</span><span class="sxs-lookup"><span data-stu-id="15f11-109">Fetching Properties and Control Patterns into the Cache</span></span>

<span data-ttu-id="15f11-110">L’exemple de code suivant montre une fonction qui récupère des éléments d’un contrôle de liste et met en cache le modèle de contrôle SelectionItem et la propriété de nom pour chaque élément.</span><span class="sxs-lookup"><span data-stu-id="15f11-110">The following code example shows a function that retrieves items from a list control and caches the SelectionItem control pattern and Name property for each item.</span></span> <span data-ttu-id="15f11-111">Par défaut, les éléments de liste sont retournés avec une référence complète, afin que toutes les propriétés actuelles soient toujours disponibles.</span><span class="sxs-lookup"><span data-stu-id="15f11-111">By default, the list items are returned with a full reference, so that all current properties are still available.</span></span>


```C++
// Given a list element, caches a control pattern and a property for
// all the list items.
IUIAutomationElementArray* FindAndCacheListItems(IUIAutomationElement* pList)
{
    if (pList == NULL)
        return NULL;
    
    IUIAutomationCondition* pCondition = NULL;
    IUIAutomationCacheRequest* pCacheRequest = NULL;
    IUIAutomationElementArray* pFound = NULL;

    HRESULT hr = g_pAutomation->CreateTrueCondition(&pCondition);
    if (FAILED(hr))
        goto cleanup;

    hr = g_pAutomation->CreateCacheRequest(&pCacheRequest);
    if (FAILED(hr))
        goto cleanup;

    hr = pCacheRequest->AddPattern(UIA_SelectionItemPatternId);
    if (FAILED(hr))
        goto cleanup;

    hr = pCacheRequest->AddProperty(UIA_NamePropertyId);
    if (FAILED(hr))
        goto cleanup;

    pList->FindAllBuildCache(TreeScope_Children, pCondition, pCacheRequest, &pFound);
    
cleanup:
    if (pCondition != NULL)
        pCondition->Release();

    if (pCacheRequest != NULL)
        pCacheRequest->Release();

    return pFound;
}
```



## <a name="retrieving-properties-and-control-patterns-from-the-cache"></a><span data-ttu-id="15f11-112">Récupération des propriétés et des modèles de contrôle à partir du cache</span><span class="sxs-lookup"><span data-stu-id="15f11-112">Retrieving Properties and Control Patterns from the Cache</span></span>

<span data-ttu-id="15f11-113">Le code suivant montre comment récupérer des propriétés et des modèles de contrôle à partir du cache.</span><span class="sxs-lookup"><span data-stu-id="15f11-113">The following code demonstrates how to retrieve properties and control patterns from the cache.</span></span> <span data-ttu-id="15f11-114">Il récupère le modèle de contrôle SelectionItem et la propriété de nom pour un élément de liste.</span><span class="sxs-lookup"><span data-stu-id="15f11-114">It retrieves the SelectionItem control pattern and Name property for a list item.</span></span>


```C++
// Demonstrates retrieval of cached properties from a list item
// obtained in FindAndCacheListItems.
HRESULT GetCachedListItem(IUIAutomationElement* pItem)
{           
    if (pItem == NULL)
    {
        return E_INVALIDARG;
    }

    IUIAutomationSelectionItemPattern* pSelectionItemPattern;
    HRESULT hr = pItem->GetCachedPatternAs(UIA_SelectionItemPatternId, 
        IID_IUIAutomationSelectionItemPattern, (void**)&pSelectionItemPattern);
    if (pSelectionItemPattern != NULL)
    {
        // ... To do: Do something with the pattern.

        pSelectionItemPattern->Release();
    }

    // Retrieve a cached property.
    BSTR bstrName;
    hr = pItem->get_CachedName(&bstrName);
    if (SUCCEEDED(hr))
    {
        // ... To do: Do something with the property.

        // Clean up when done with name.
        SysFreeString(bstrName);
        bstrName = NULL;
    }

    BOOL isControl;

    // The following returns E_INVALIDARG because the property was not cached.
    // hr = pItem->get_CachedIsControlElement(&isControl);

    // The following is valid because we have a full reference to the object, therefore
    // we can get current properties. If the cache request had been made with 
    // AutomationElementMode_None, no current properties would be available from
    // this IUIAutomationElement.
    hr = pItem->get_CurrentIsControlElement(&isControl);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="15f11-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="15f11-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="15f11-116">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="15f11-116">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="15f11-117">Mise en cache des propriétés UI Automation et des modèles de contrôle</span><span class="sxs-lookup"><span data-stu-id="15f11-117">Caching UI Automation Properties and Control Patterns</span></span>](uiauto-cachingforclients.md)
</dt> <dt>

[<span data-ttu-id="15f11-118">Rubriques de procédures pour les clients UI Automation</span><span class="sxs-lookup"><span data-stu-id="15f11-118">How-To Topics for UI Automation Clients</span></span>](uiauto-howto-topics-for-uiautomation-clients.md)
</dt> </dl>

 

 




