---
description: Définition de l’horloge du graphique
ms.assetid: 23deab26-6c9a-4f94-b750-11c9b1a14ce3
title: Définition de l’horloge du graphique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe98c8dce1ab5f94664fbe1406c682e5d4e50b8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106516537"
---
# <a name="setting-the-graph-clock"></a><span data-ttu-id="57e55-103">Définition de l’horloge du graphique</span><span class="sxs-lookup"><span data-stu-id="57e55-103">Setting the Graph Clock</span></span>

<span data-ttu-id="57e55-104">Quand vous générez un graphique de filtre, le gestionnaire de graphes de filtres choisit automatiquement une horloge de référence pour le graphique.</span><span class="sxs-lookup"><span data-stu-id="57e55-104">When you build a filter graph, the Filter Graph Manager automatically chooses a reference clock for the graph.</span></span> <span data-ttu-id="57e55-105">Tous les filtres du graphique sont synchronisés avec l’horloge de référence.</span><span class="sxs-lookup"><span data-stu-id="57e55-105">All filters in the graph are synchronized to the reference clock.</span></span> <span data-ttu-id="57e55-106">En particulier, les filtres de convertisseur utilisent l’horloge de référence pour déterminer l’heure de présentation de chaque échantillon.</span><span class="sxs-lookup"><span data-stu-id="57e55-106">In particular, renderer filters use the reference clock to determine the presentation time of each sample.</span></span>

<span data-ttu-id="57e55-107">Il n’y a généralement aucune raison pour qu’une application remplace le choix de l’horloge de référence du gestionnaire de graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="57e55-107">There is usually no reason for an application to override the Filter Graph Manager's choice of reference clock.</span></span> <span data-ttu-id="57e55-108">Toutefois, vous pouvez le faire en appelant la méthode [**IMediaFilter :: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) sur le gestionnaire de graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="57e55-108">However, you can do so by calling the [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method on the Filter Graph Manager.</span></span> <span data-ttu-id="57e55-109">Cette méthode prend un pointeur vers l’interface **IReferenceClock** de l’horloge.</span><span class="sxs-lookup"><span data-stu-id="57e55-109">This method takes a pointer to the clock's **IReferenceClock** interface.</span></span> <span data-ttu-id="57e55-110">Appelez la méthode pendant que le graphique est arrêté.</span><span class="sxs-lookup"><span data-stu-id="57e55-110">Call the method while the graph is stopped.</span></span>

<span data-ttu-id="57e55-111">Si un filtre fournit une horloge, vous pouvez obtenir le pointeur **IReferenceClock** en appelant **QueryInterface** sur le filtre.</span><span class="sxs-lookup"><span data-stu-id="57e55-111">If a filter provides a clock, you can get the **IReferenceClock** pointer by calling **QueryInterface** on the filter.</span></span> <span data-ttu-id="57e55-112">Vous pouvez également implémenter une horloge de référence externe qui n’est pas fournie par un filtre, à condition que votre horloge externe implémente **IReferenceClock**.</span><span class="sxs-lookup"><span data-stu-id="57e55-112">Alternatively, you can implement an external reference clock that is not provided by a filter, as long as your external clock implements **IReferenceClock**.</span></span> <span data-ttu-id="57e55-113">L’exemple suivant montre comment spécifier une horloge :</span><span class="sxs-lookup"><span data-stu-id="57e55-113">The following example shows how to specify a clock:</span></span>


```C++
IGraphBuilder *pGraph = 0;
IReferenceClock *pClock = 0;

CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
    IID_IGraphBuilder, (void **)&pGraph);

// Build the graph.
pGraph->RenderFile(L"C:\\Example.avi", 0);

// Create your clock.
hr = CreateMyPrivateClock(&pClock);
if (SUCCEEDED(hr))
{
    // Set the graph clock.
    IMediaFilter *pMediaFilter = 0;
    pGraph->QueryInterface(IID_IMediaFilter, (void**)&pMediaFilter);
    pMediaFilter->SetSyncSource(pClock);
    pClock->Release();
    pMediaFilter->Release();
}
```



<span data-ttu-id="57e55-114">Cet exemple suppose que CreateMyPrivateClock est une fonction définie par l’application qui crée une horloge et retourne un pointeur **IReferenceClock** .</span><span class="sxs-lookup"><span data-stu-id="57e55-114">This example assumes that CreateMyPrivateClock is an application-defined function that creates a clock and returns an **IReferenceClock** pointer.</span></span>

<span data-ttu-id="57e55-115">Vous pouvez également définir le graphique de filtre pour qu’il s’exécute sans horloge, en appelant **SetSyncSource** avec la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="57e55-115">You can also set the filter graph to run with no clock, by calling **SetSyncSource** with the value **NULL**.</span></span> <span data-ttu-id="57e55-116">S’il n’y a pas d’horloge, le graphique s’exécute aussi rapidement que possible.</span><span class="sxs-lookup"><span data-stu-id="57e55-116">If there is no clock, the graph runs as quickly as possible.</span></span> <span data-ttu-id="57e55-117">Sans horloge, les filtres de convertisseur n’attendent pas l’heure de la présentation d’un exemple.</span><span class="sxs-lookup"><span data-stu-id="57e55-117">With no clock, renderer filters do not wait for a sample's presentation time.</span></span> <span data-ttu-id="57e55-118">Au lieu de cela, ils affichent chaque échantillon dès qu’il arrive.</span><span class="sxs-lookup"><span data-stu-id="57e55-118">Instead, they render each sample as soon as it arrives.</span></span> <span data-ttu-id="57e55-119">La définition du graphique pour qu’il s’exécute sans horloge est utile si vous souhaitez traiter les données rapidement, plutôt que de les afficher en temps réel.</span><span class="sxs-lookup"><span data-stu-id="57e55-119">Setting the graph to run without a clock is useful if you want to process data quickly, rather than previewing it in real time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57e55-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="57e55-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57e55-121">Tâches de base de DirectShow</span><span class="sxs-lookup"><span data-stu-id="57e55-121">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> <dt>

[<span data-ttu-id="57e55-122">**CBaseReferenceClock, classe**</span><span class="sxs-lookup"><span data-stu-id="57e55-122">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> <dt>

[<span data-ttu-id="57e55-123">Temps et horloges dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="57e55-123">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



