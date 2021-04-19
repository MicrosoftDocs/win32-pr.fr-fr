---
description: À propos des exemples de supports et des allocators
ms.assetid: d6283bf0-0460-4519-9a56-fd4c78cfaabc
title: À propos des exemples de supports et des allocators
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9105228e70f82aaa7c36b7e7d28cf7e748e1e2f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106523748"
---
# <a name="about-media-samples-and-allocators"></a><span data-ttu-id="e1faa-103">À propos des exemples de supports et des allocators</span><span class="sxs-lookup"><span data-stu-id="e1faa-103">About Media Samples and Allocators</span></span>

<span data-ttu-id="e1faa-104">Les filtres fournissent des données sur les connexions de code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="e1faa-104">Filters deliver data across pin connections.</span></span> <span data-ttu-id="e1faa-105">Les données sont déplacées de la broche de sortie d’un filtre vers la broche d’entrée d’un autre filtre.</span><span class="sxs-lookup"><span data-stu-id="e1faa-105">Data moves from the output pin of one filter to the input pin of another filter.</span></span> <span data-ttu-id="e1faa-106">La méthode la plus courante pour que la broche de sortie remette les données consiste à appeler la méthode [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) sur l’entrée, bien qu’il existe également quelques autres mécanismes.</span><span class="sxs-lookup"><span data-stu-id="e1faa-106">The most common way for the output pin to deliver the data is by calling the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method on the input, although a few other mechanisms exist as well.</span></span>

<span data-ttu-id="e1faa-107">Selon le filtre, il est possible d’allouer de la mémoire pour les données multimédias de différentes façons : sur le tas, dans une surface DirectDraw, à l’aide de la mémoire GDI partagée ou à l’aide d’un autre mécanisme d’allocation.</span><span class="sxs-lookup"><span data-stu-id="e1faa-107">Depending on the filter, memory for the media data can be allocated in various ways: on the heap, in a DirectDraw surface, using shared GDI memory, or using some other allocation mechanism.</span></span> <span data-ttu-id="e1faa-108">L’objet chargé d’allouer la mémoire est appelé *Allocator*, qui est un objet com qui expose l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .</span><span class="sxs-lookup"><span data-stu-id="e1faa-108">The object responsible for allocating the memory is called an *allocator*, which is a COM object that exposes the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

<span data-ttu-id="e1faa-109">Lorsque deux codes confidentiels se connectent, l’un des codes confidentiels doit fournir un allocateur.</span><span class="sxs-lookup"><span data-stu-id="e1faa-109">When two pins connect, one of the pins must provide an allocator.</span></span> <span data-ttu-id="e1faa-110">DirectShow définit une séquence d’appels de méthode qui est utilisée pour déterminer quel pin fournit l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="e1faa-110">DirectShow defines a sequence of method calls that is used to establish which pin provides the allocator.</span></span> <span data-ttu-id="e1faa-111">Les codes confidentiels acceptent également le nombre de mémoires tampons que l’allocateur va créer et la taille des mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="e1faa-111">The pins also agree on the number of buffers that the allocator will create, and the size of the buffers.</span></span>

<span data-ttu-id="e1faa-112">Avant le début de la diffusion en continu, l’allocateur crée un pool de mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="e1faa-112">Before streaming begins, the allocator creates a pool of buffers.</span></span> <span data-ttu-id="e1faa-113">Pendant la diffusion en continu, le filtre amont remplit les tampons de données et les remet au filtre en aval.</span><span class="sxs-lookup"><span data-stu-id="e1faa-113">During streaming, the upstream filter fills buffers with data and delivers them to the downstream filter.</span></span> <span data-ttu-id="e1faa-114">Toutefois, le filtre amont n’attribue pas de pointeurs bruts de filtre en aval aux tampons.</span><span class="sxs-lookup"><span data-stu-id="e1faa-114">But the upstream filter does not give the downstream filter raw pointers to the buffers.</span></span> <span data-ttu-id="e1faa-115">Au lieu de cela, il utilise les objets COM appelés *exemples de médias*, que l’allocateur crée pour gérer les mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="e1faa-115">Instead, it uses COM objects called *media samples*, which the allocator creates to manage the buffers.</span></span> <span data-ttu-id="e1faa-116">Les exemples de supports exposent l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) .</span><span class="sxs-lookup"><span data-stu-id="e1faa-116">Media samples expose the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span> <span data-ttu-id="e1faa-117">Un exemple de support contient les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="e1faa-117">A media sample contains:</span></span>

-   <span data-ttu-id="e1faa-118">pointeur vers la mémoire tampon sous-jacente</span><span class="sxs-lookup"><span data-stu-id="e1faa-118">a pointer to the underlying buffer</span></span>
-   <span data-ttu-id="e1faa-119">un horodatage</span><span class="sxs-lookup"><span data-stu-id="e1faa-119">a time stamp</span></span>
-   <span data-ttu-id="e1faa-120">différents indicateurs</span><span class="sxs-lookup"><span data-stu-id="e1faa-120">various flags</span></span>
-   <span data-ttu-id="e1faa-121">éventuellement, un type de média</span><span class="sxs-lookup"><span data-stu-id="e1faa-121">optionally, a media type</span></span>

<span data-ttu-id="e1faa-122">L’horodatage définit l’heure de présentation, que le filtre de convertisseur utilise pour planifier le rendu.</span><span class="sxs-lookup"><span data-stu-id="e1faa-122">The time stamp defines the presentation time, which the renderer filter uses to schedule rendering.</span></span> <span data-ttu-id="e1faa-123">Les indicateurs indiquent notamment s’il y a eu une rupture dans les données depuis l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="e1faa-123">The flags indicate things like whether there was a break in the data since the previous sample.</span></span> <span data-ttu-id="e1faa-124">Le type de média offre un moyen pour les filtres de modifier les formats mi-flux.</span><span class="sxs-lookup"><span data-stu-id="e1faa-124">The media type provides a way for filters to change formats mid-stream.</span></span> <span data-ttu-id="e1faa-125">En règle générale, l’exemple n’a aucun type de média, ce qui indique que le format n’a pas changé depuis l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="e1faa-125">Usually, the sample has no media type, which indicates that the format has not changed since the previous sample.</span></span>

<span data-ttu-id="e1faa-126">Lorsqu’un filtre utilise une mémoire tampon, il contient le nombre de références sur l’exemple.</span><span class="sxs-lookup"><span data-stu-id="e1faa-126">While a filter is using a buffer, it holds reference count on the sample.</span></span> <span data-ttu-id="e1faa-127">L’allocateur utilise le décompte de références pour déterminer quand il peut réutiliser la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="e1faa-127">The allocator uses the reference count to determine when it can re-use the buffer.</span></span> <span data-ttu-id="e1faa-128">Cela empêche un filtre de remplacer une mémoire tampon qu’un autre filtre utilise encore.</span><span class="sxs-lookup"><span data-stu-id="e1faa-128">This prevents a filter from overwriting a buffer that another filter is still using.</span></span> <span data-ttu-id="e1faa-129">Un exemple ne retourne pas au pool d’exemples disponibles de l’allocateur tant que chaque filtre ne l’a pas libéré.</span><span class="sxs-lookup"><span data-stu-id="e1faa-129">A sample does not return to the allocator's pool of available samples until every filter has released it.</span></span>

<span data-ttu-id="e1faa-130">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="e1faa-130">For more information, see the following topics:</span></span>

-   <span data-ttu-id="e1faa-131">La rubrique [exemples et allocators](samples-and-allocators.md) fournit une description plus détaillée du fonctionnement des allocateurs.</span><span class="sxs-lookup"><span data-stu-id="e1faa-131">The topic [Samples and Allocators](samples-and-allocators.md) provides a more detailed description of how allocators work.</span></span>
-   <span data-ttu-id="e1faa-132">Le [Data Flow dans le graphique de filtre](data-flow-in-the-filter-graph.md) donne une vue d’ensemble du workflow de données dans DirectShow.</span><span class="sxs-lookup"><span data-stu-id="e1faa-132">The topic [Data Flow in the Filter Graph](data-flow-in-the-filter-graph.md) gives a general overview of data flow in DirectShow.</span></span>

<span data-ttu-id="e1faa-133">Les rubriques suivantes sont destinées aux développeurs qui écrivent leurs propres filtres personnalisés :</span><span class="sxs-lookup"><span data-stu-id="e1faa-133">The following topics are intended for developers who are writing their own custom filters:</span></span>

-   [<span data-ttu-id="e1faa-134">Transmission de données pour les développeurs de filtres</span><span class="sxs-lookup"><span data-stu-id="e1faa-134">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
-   [<span data-ttu-id="e1faa-135">Threads et sections critiques</span><span class="sxs-lookup"><span data-stu-id="e1faa-135">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)

## <a name="related-topics"></a><span data-ttu-id="e1faa-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e1faa-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1faa-137">Le graphique de filtre et ses composants</span><span class="sxs-lookup"><span data-stu-id="e1faa-137">The Filter Graph and Its Components</span></span>](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 



