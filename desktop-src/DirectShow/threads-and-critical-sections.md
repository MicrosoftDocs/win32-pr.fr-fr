---
description: Threads et sections critiques
ms.assetid: e55acb06-03f4-4191-bffe-3196f41ef2c7
title: Threads et sections critiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 576cb28e7e382db92328adf09980a825e71b5a3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321110"
---
# <a name="threads-and-critical-sections"></a><span data-ttu-id="c4203-103">Threads et sections critiques</span><span class="sxs-lookup"><span data-stu-id="c4203-103">Threads and Critical Sections</span></span>

<span data-ttu-id="c4203-104">Cette section décrit les threads dans les filtres DirectShow et les étapes à suivre pour éviter les blocages ou les blocages dans un filtre personnalisé.</span><span class="sxs-lookup"><span data-stu-id="c4203-104">This section describes threading in DirectShow filters, and the steps you should take to avoid crashes or deadlocks in a custom filter.</span></span>

<span data-ttu-id="c4203-105">Les exemples de cette section utilisent un pseudocode pour illustrer le code que vous devrez écrire.</span><span class="sxs-lookup"><span data-stu-id="c4203-105">The examples in this section use pseudocode to illustrate the code you will need to write.</span></span> <span data-ttu-id="c4203-106">Ils partent du principe qu’un filtre personnalisé utilise des classes dérivées des classes de base DirectShow, comme suit :</span><span class="sxs-lookup"><span data-stu-id="c4203-106">They assume that a custom filter is using classes derived from the DirectShow base classes, as follows:</span></span>

-   <span data-ttu-id="c4203-107">CMyInputPin : dérivée de [**CBaseInputPin**](cbaseinputpin.md).</span><span class="sxs-lookup"><span data-stu-id="c4203-107">CMyInputPin: Derived from [**CBaseInputPin**](cbaseinputpin.md).</span></span>
-   <span data-ttu-id="c4203-108">CMyOutputPin : dérivée de [**CBaseOutputPin**](cbaseoutputpin.md).</span><span class="sxs-lookup"><span data-stu-id="c4203-108">CMyOutputPin: Derived from [**CBaseOutputPin**](cbaseoutputpin.md).</span></span>
-   <span data-ttu-id="c4203-109">CMyFilter : dérivée de [**CBaseFilter**](cbasefilter.md).</span><span class="sxs-lookup"><span data-stu-id="c4203-109">CMyFilter: Derived from [**CBaseFilter**](cbasefilter.md).</span></span>
-   <span data-ttu-id="c4203-110">CMyInputAllocator : Allocator du code confidentiel d’entrée, dérivé de [**CMemAllocator**](cmemallocator.md).</span><span class="sxs-lookup"><span data-stu-id="c4203-110">CMyInputAllocator: The input pin's allocator, derived from [**CMemAllocator**](cmemallocator.md).</span></span> <span data-ttu-id="c4203-111">Tous les filtres n’ont pas besoin d’un allocateur personnalisé.</span><span class="sxs-lookup"><span data-stu-id="c4203-111">Not every filter needs a custom allocator.</span></span> <span data-ttu-id="c4203-112">Pour de nombreux filtres, la classe **CMemAllocator** est suffisante.</span><span class="sxs-lookup"><span data-stu-id="c4203-112">For many filters, the **CMemAllocator** class is sufficient.</span></span>

<span data-ttu-id="c4203-113">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="c4203-113">This section contains the following topics.</span></span>

-   [<span data-ttu-id="c4203-114">Threads de diffusion en continu et d’application</span><span class="sxs-lookup"><span data-stu-id="c4203-114">The Streaming and Application Threads</span></span>](the-streaming-and-application-threads.md)
-   [<span data-ttu-id="c4203-115">Suspension</span><span class="sxs-lookup"><span data-stu-id="c4203-115">Pausing</span></span>](pausing.md)
-   [<span data-ttu-id="c4203-116">Réception et envoi d’exemples</span><span class="sxs-lookup"><span data-stu-id="c4203-116">Receiving and Delivering Samples</span></span>](receiving-and-delivering-samples.md)
-   [<span data-ttu-id="c4203-117">Transmission de la fin du flux</span><span class="sxs-lookup"><span data-stu-id="c4203-117">Delivering the End of Stream</span></span>](delivering-the-end-of-stream.md)
-   [<span data-ttu-id="c4203-118">Vidage des données</span><span class="sxs-lookup"><span data-stu-id="c4203-118">Flushing Data</span></span>](flushing-data.md)
-   [<span data-ttu-id="c4203-119">En cours d’arrêt</span><span class="sxs-lookup"><span data-stu-id="c4203-119">Stopping</span></span>](stopping.md)
-   [<span data-ttu-id="c4203-120">Obtention de mémoires tampons</span><span class="sxs-lookup"><span data-stu-id="c4203-120">Getting Buffers</span></span>](getting-buffers.md)
-   [<span data-ttu-id="c4203-121">Streaming threads et le gestionnaire de graphique de filtre</span><span class="sxs-lookup"><span data-stu-id="c4203-121">Streaming Threads and the Filter Graph Manager</span></span>](streaming-threads-and-the-filter-graph-manager.md)
-   [<span data-ttu-id="c4203-122">Résumé du thread de filtre</span><span class="sxs-lookup"><span data-stu-id="c4203-122">Summary of Filter Threading</span></span>](summary-of-filter-threading.md)

## <a name="related-topics"></a><span data-ttu-id="c4203-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c4203-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4203-124">Transmission de données pour les développeurs de filtres</span><span class="sxs-lookup"><span data-stu-id="c4203-124">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
</dt> <dt>

[<span data-ttu-id="c4203-125">Écriture de filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="c4203-125">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



