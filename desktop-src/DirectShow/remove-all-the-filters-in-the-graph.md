---
description: Supprimer tous les filtres dans le graphique
ms.assetid: a11af581-c331-4607-be8b-5f65961bd422
title: Supprimer tous les filtres dans le graphique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d414ef7e532eaf5df9143a6b601a57e4a8bd45
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746301"
---
# <a name="remove-all-the-filters-in-the-graph"></a><span data-ttu-id="5c993-103">Supprimer tous les filtres dans le graphique</span><span class="sxs-lookup"><span data-stu-id="5c993-103">Remove All the Filters in the Graph</span></span>

<span data-ttu-id="5c993-104">Le moyen le plus simple de supprimer tous les filtres dans un graphique de filtre consiste simplement à libérer le gestionnaire du graphique de filtres et à en créer un nouveau.</span><span class="sxs-lookup"><span data-stu-id="5c993-104">The easiest way to remove all of the filters in a filter graph is simply to release the Filter Graph Manager and create a new one.</span></span> <span data-ttu-id="5c993-105">Veillez à libérer chaque pointeur de votre application sur les interfaces des gestionnaires de graphique de filtre, ainsi que les pointeurs vers des objets dans le graphique, y compris des filtres, des codes confidentiels, l’horloge de référence, etc.</span><span class="sxs-lookup"><span data-stu-id="5c993-105">Make sure to release every pointer that your application has to any interfaces on the Filter Graph Managers, as well as pointers to objects in the graph, including filters, pins, the reference clock, and so forth.</span></span>

<span data-ttu-id="5c993-106">Vous pouvez également supprimer les filtres un par un, à l’aide de la méthode [**IFilterGraph :: removeFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-removefilter) :</span><span class="sxs-lookup"><span data-stu-id="5c993-106">Alternatively, you can remove the filters one at a time, using the [**IFilterGraph::RemoveFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-removefilter) method:</span></span>


```C++
// Stop the graph.
pControl->Stop();

// Enumerate the filters in the graph.
IEnumFilters *pEnum = NULL;
HRESULT hr = pGraph->EnumFilters(&pEnum);
if (SUCCEEDED(hr))
{
    IBaseFilter *pFilter = NULL;
    while (S_OK == pEnum->Next(1, &pFilter, NULL))
     {
         // Remove the filter.
         pGraph->RemoveFilter(pFilter);
         // Reset the enumerator.
         pEnum->Reset();
         pFilter->Release();
    }
    pEnum->Release();
}
```



<span data-ttu-id="5c993-107">Cet exemple utilise la méthode [**IFilterGraph :: EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) pour énumérer les filtres dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="5c993-107">This example uses the [**IFilterGraph::EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) method to enumerate the filters in the graph.</span></span> <span data-ttu-id="5c993-108">La suppression d’un filtre entraîne le désynchronisation de l’objet énumérateur avec le graphique.</span><span class="sxs-lookup"><span data-stu-id="5c993-108">Removing a filter causes the enumerator object to become out of sync with the graph.</span></span> <span data-ttu-id="5c993-109">Utilisez la méthode [**IEnumFilters :: Reset**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-reset) pour réinitialiser l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="5c993-109">Use the [**IEnumFilters::Reset**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-reset) method to reset the enumerator.</span></span> <span data-ttu-id="5c993-110">Dans le cas contraire, tout appel ultérieur à [**IEnumFilters :: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-next) échoue.</span><span class="sxs-lookup"><span data-stu-id="5c993-110">Otherwise, any subsequent call to [**IEnumFilters::Next**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-next) will fail.</span></span>

 

 



