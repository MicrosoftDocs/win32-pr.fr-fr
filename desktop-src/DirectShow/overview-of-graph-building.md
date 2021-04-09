---
description: Vue d’ensemble de la génération de graphiques
ms.assetid: 5753f06c-ecfd-48d7-a8e9-768b798e9279
title: Vue d’ensemble de la génération de graphiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69ef9ea0f4f9e21d33372ad2a37a59b512d5dcc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109078"
---
# <a name="overview-of-graph-building"></a><span data-ttu-id="19219-103">Vue d’ensemble de la génération de graphiques</span><span class="sxs-lookup"><span data-stu-id="19219-103">Overview of Graph Building</span></span>

<span data-ttu-id="19219-104">Pour créer un graphique de filtre, commencez par créer une instance du gestionnaire de graphes de filtre :</span><span class="sxs-lookup"><span data-stu-id="19219-104">To create a filter graph, begin by creating an instance of the Filter Graph Manager:</span></span>


```C++
IGraphBuilder* pIGB;
HRESULT hr = CoCreateInstance(CLSID_FilterGraph,
    NULL, CLSCTX_INPROC_SERVER, IID_IGraphBuilder,
    (void **)&pIGB);
```



<span data-ttu-id="19219-105">Le gestionnaire de graphes de filtre prend en charge les méthodes de création de graphiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="19219-105">The Filter Graph Manager supports the following graph-building methods:</span></span>

-   <span data-ttu-id="19219-106">[**IFilterGraph :: ConnectDirect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-connectdirect) essaie d’établir une connexion directe entre deux broches.</span><span class="sxs-lookup"><span data-stu-id="19219-106">[**IFilterGraph::ConnectDirect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-connectdirect) tries to make a direct connection between two pins.</span></span> <span data-ttu-id="19219-107">Si les codes confidentiels ne peuvent pas se connecter, la méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="19219-107">If the pins cannot connect, the method fails.</span></span>
-   <span data-ttu-id="19219-108">[**IGraphBuilder :: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) connecte deux broches.</span><span class="sxs-lookup"><span data-stu-id="19219-108">[**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) connects two pins.</span></span> <span data-ttu-id="19219-109">Si possible, il établit une connexion directe.</span><span class="sxs-lookup"><span data-stu-id="19219-109">If possible, it makes a direct connection.</span></span> <span data-ttu-id="19219-110">Dans le cas contraire, il utilise des filtres intermédiaires pour terminer la connexion.</span><span class="sxs-lookup"><span data-stu-id="19219-110">Otherwise, it uses intermediate filters to complete the connection.</span></span>
-   <span data-ttu-id="19219-111">[**IGraphBuilder :: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) commence à partir d’une broche de sortie et génère le reste du graphique.</span><span class="sxs-lookup"><span data-stu-id="19219-111">[**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) starts from an output pin and builds the rest of the graph.</span></span> <span data-ttu-id="19219-112">Cette méthode ajoute des filtres en fonction des besoins, en aval, jusqu’à ce qu’elle atteigne un filtre de convertisseur.</span><span class="sxs-lookup"><span data-stu-id="19219-112">This methods adds filters as needed, working downstream, until it reaches a renderer filter.</span></span>
-   <span data-ttu-id="19219-113">[**IGraphBuilder :: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) crée un graphique de lecture de fichier complet.</span><span class="sxs-lookup"><span data-stu-id="19219-113">[**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) builds a complete file-playback graph.</span></span>
-   <span data-ttu-id="19219-114">[**IFilterGraph :: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) ajoute un filtre au graphique.</span><span class="sxs-lookup"><span data-stu-id="19219-114">[**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) adds a filter to the graph.</span></span> <span data-ttu-id="19219-115">Il ne connecte pas le filtre.</span><span class="sxs-lookup"><span data-stu-id="19219-115">It does not connect the filter.</span></span> <span data-ttu-id="19219-116">Vous devez créer le filtre avant d’appeler cette méthode, soit en appelant **CoCreateInstance** , soit en utilisant le mappeur de filtre ou l’énumérateur de périphérique système.</span><span class="sxs-lookup"><span data-stu-id="19219-116">You must create the filter before calling this method, either by calling **CoCreateInstance** or by using the Filter Mapper or System Device Enumerator.</span></span>

<span data-ttu-id="19219-117">Ces méthodes fournissent trois approches de base pour générer le graphique :</span><span class="sxs-lookup"><span data-stu-id="19219-117">These methods provide three basic approaches to building the graph:</span></span>

1.  <span data-ttu-id="19219-118">Le gestionnaire de graphique de filtre crée le graphique entier.</span><span class="sxs-lookup"><span data-stu-id="19219-118">The Filter Graph Manager builds the entire graph.</span></span>
2.  <span data-ttu-id="19219-119">Le gestionnaire de graphique de filtre génère une partie du graphique.</span><span class="sxs-lookup"><span data-stu-id="19219-119">The Filter Graph Manager builds part of the graph.</span></span>
3.  <span data-ttu-id="19219-120">L’application génère le graphique entier.</span><span class="sxs-lookup"><span data-stu-id="19219-120">The application builds the entire graph.</span></span>

<span data-ttu-id="19219-121">**Le gestionnaire de graphique de filtre crée le graphique entier**</span><span class="sxs-lookup"><span data-stu-id="19219-121">**The Filter Graph Manager Builds the Entire Graph**</span></span>

<span data-ttu-id="19219-122">Si vous souhaitez simplement lire un fichier créé dans un format reconnu, par exemple AVI, MPEG, WAV ou MP3, utilisez la méthode **RenderFile** .</span><span class="sxs-lookup"><span data-stu-id="19219-122">If you simply want to play a file that is authored in a recognized format, such as AVI, MPEG, WAV, or MP3, use the **RenderFile** method.</span></span> <span data-ttu-id="19219-123">L’article [Comment lire un fichier](how-to-play-a-file.md) montre comment procéder.</span><span class="sxs-lookup"><span data-stu-id="19219-123">The article [How To Play a File](how-to-play-a-file.md) shows how to do this.</span></span>

<span data-ttu-id="19219-124">La méthode **RenderFile** commence par Rechercher dans le registre un filtre source qui peut analyser le fichier.</span><span class="sxs-lookup"><span data-stu-id="19219-124">The **RenderFile** method starts by looking in the registry for a source filter that can parse the file.</span></span> <span data-ttu-id="19219-125">Elle utilise le protocole (par exemple, « `https://` » dans l’URL), l’extension de fichier ou des modèles d’octets prédéfinis dans le fichier pour déterminer le filtre source.</span><span class="sxs-lookup"><span data-stu-id="19219-125">It uses the protocol (such as " `https://` " in the URL), the file extension, or pre-defined byte patterns in the file to determine the source filter.</span></span> <span data-ttu-id="19219-126">Pour plus d’informations, consultez [inscription d’un type de fichier personnalisé](registering-a-custom-file-type.md).</span><span class="sxs-lookup"><span data-stu-id="19219-126">For details, see [Registering a Custom File Type](registering-a-custom-file-type.md).</span></span>

<span data-ttu-id="19219-127">Pour créer le reste du graphique, le gestionnaire de graphes de filtre utilise un processus itératif dans lequel il prend les types de média qu’un filtre prend en charge sur ses broches de sortie, et recherche dans le registre les filtres qui acceptent ce type de média comme entrée.</span><span class="sxs-lookup"><span data-stu-id="19219-127">To build the rest of the graph, the Filter Graph Manager uses an iterative process wherein it takes the media types that a filter supports on its output pins, and searches the registry for filters that will accept that media type as input.</span></span> <span data-ttu-id="19219-128">Il utilise plusieurs critères pour affiner la recherche et définir la priorité des filtres :</span><span class="sxs-lookup"><span data-stu-id="19219-128">It uses several criteria to narrow the search and prioritize filters:</span></span>

-   <span data-ttu-id="19219-129">La *catégorie de filtre* identifie les fonctionnalités générales du filtre.</span><span class="sxs-lookup"><span data-stu-id="19219-129">The *filter category* identifies the general functionality of the filter.</span></span>
-   <span data-ttu-id="19219-130">Le type de média décrit le type de données que le filtre peut accepter comme entrée ou remettre en sortie.</span><span class="sxs-lookup"><span data-stu-id="19219-130">The media type describes what kind of data the filter can accept as input or deliver as output.</span></span>
-   <span data-ttu-id="19219-131">La *mérite* détermine l’ordre dans lequel les filtres sont essayés.</span><span class="sxs-lookup"><span data-stu-id="19219-131">The *merit* determines the order in which filters are tried.</span></span> <span data-ttu-id="19219-132">Si deux filtres de la même catégorie de filtre prennent tous deux en charge les mêmes types d’entrée, le gestionnaire de graphes de filtre sélectionne celui dont la valeur mérite la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="19219-132">If two filters in the same filter category both support the same input types, the Filter Graph Manager selects the one with the highest merit value.</span></span> <span data-ttu-id="19219-133">Certains filtres reçoivent intentionnellement une valeur de faible valeur, car ils sont conçus à des fins spécialisées et doivent être ajoutés uniquement au graphique par l’application.</span><span class="sxs-lookup"><span data-stu-id="19219-133">Some filters are purposely given a low merit value because they are designed for specialized purposes and should only be added to the graph by the application.</span></span>

<span data-ttu-id="19219-134">Le gestionnaire de graphique de filtre utilise l’objet [Mappeur de filtre](filter-mapper.md) pour rechercher dans le registre.</span><span class="sxs-lookup"><span data-stu-id="19219-134">The Filter Graph Manager uses the [Filter Mapper](filter-mapper.md) object to search the registry.</span></span>

<span data-ttu-id="19219-135">À mesure que chaque filtre est ajouté, le gestionnaire de graphes de filtre tente de le connecter à la broche de sortie du filtre précédent.</span><span class="sxs-lookup"><span data-stu-id="19219-135">As each filter is added, the Filter Graph Manager tries to connect it to the previous filter's output pin.</span></span> <span data-ttu-id="19219-136">Les filtres négocient pour déterminer s’ils peuvent se connecter et, le cas échéant, le type de média à utiliser pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="19219-136">The filters negotiate to determine whether they can connect, and if so, what media type to use for the connection.</span></span> <span data-ttu-id="19219-137">Si le nouveau filtre ne peut pas se connecter, le gestionnaire de graphes de filtres l’ignore et tente un autre filtre.</span><span class="sxs-lookup"><span data-stu-id="19219-137">If the new filter cannot connect, the Filter Graph Manager discards it and tries another filter.</span></span> <span data-ttu-id="19219-138">Ce processus se poursuit jusqu’à ce que chaque flux soit rendu.</span><span class="sxs-lookup"><span data-stu-id="19219-138">This process continues until every stream is rendered.</span></span>

<span data-ttu-id="19219-139">**Le gestionnaire de graphes de filtres génère une partie du graphique**</span><span class="sxs-lookup"><span data-stu-id="19219-139">**The Filter Graph Manager Builds Part of the Graph**</span></span>

<span data-ttu-id="19219-140">Pour effectuer une tâche allant au-delà de la simple exécution d’un fichier, votre application doit effectuer au moins une partie du travail de génération du graphique.</span><span class="sxs-lookup"><span data-stu-id="19219-140">To do something beyond simply playing a file, your application must perform at least some of the graph building work.</span></span> <span data-ttu-id="19219-141">Par exemple, une application de capture vidéo doit sélectionner un filtre de source de capture et l’ajouter au graphique.</span><span class="sxs-lookup"><span data-stu-id="19219-141">For example, a video capture application must select a capture source filter and add it to the graph.</span></span> <span data-ttu-id="19219-142">Si vous écrivez des données dans un fichier AVI, vous devez ajouter les filtres AVI MUX et writer de fichier au graphique.</span><span class="sxs-lookup"><span data-stu-id="19219-142">If you are writing data to an AVI file, you must add the AVI Mux and File Writer filters to the graph.</span></span> <span data-ttu-id="19219-143">Toutefois, il est souvent possible de laisser le gestionnaire de graphes de filtres compléter le graphique.</span><span class="sxs-lookup"><span data-stu-id="19219-143">However, it is often possible to let the Filter Graph Manager complete the graph.</span></span> <span data-ttu-id="19219-144">Par exemple, vous pouvez afficher un code confidentiel pour l’aperçu en appelant la méthode **Render** .</span><span class="sxs-lookup"><span data-stu-id="19219-144">For example, you can render a pin for preview by calling the **Render** method.</span></span>

<span data-ttu-id="19219-145">**L’application génère le graphique entier**</span><span class="sxs-lookup"><span data-stu-id="19219-145">**The Application Builds the Entire Graph**</span></span>

<span data-ttu-id="19219-146">Dans certains scénarios, votre application peut avoir besoin de générer le graphique en ajoutant et en connectant chaque filtre.</span><span class="sxs-lookup"><span data-stu-id="19219-146">In some scenarios, your application may need to build the graph by adding and connecting each filter.</span></span> <span data-ttu-id="19219-147">Dans ce cas, vous connaissez probablement spécifiquement les filtres qui doivent être ajoutés au graphique.</span><span class="sxs-lookup"><span data-stu-id="19219-147">In this case, you probably know specifically which filters should be added to the graph.</span></span> <span data-ttu-id="19219-148">Avec cette approche, l’application ajoute chaque filtre en appelant **AddFilter**, énumère les broches sur les filtres et les connecte en appelant **Connect** ou **ConnectDirect**.</span><span class="sxs-lookup"><span data-stu-id="19219-148">With this approach, the application adds each filter by calling **AddFilter**, enumerates the pins on the filters, and connects them by calling either **Connect** or **ConnectDirect**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19219-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="19219-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19219-150">Création de graphiques à l’aide du générateur de graphiques de capture</span><span class="sxs-lookup"><span data-stu-id="19219-150">Building Graphs with the Capture Graph Builder</span></span>](building-graphs-with-the-capture-graph-builder.md)
</dt> <dt>

[<span data-ttu-id="19219-151">Énumération des appareils et des filtres</span><span class="sxs-lookup"><span data-stu-id="19219-151">Enumerating Devices and Filters</span></span>](enumerating-devices-and-filters.md)
</dt> <dt>

[<span data-ttu-id="19219-152">Énumération d’objets dans un graphique de filtre</span><span class="sxs-lookup"><span data-stu-id="19219-152">Enumerating Objects in a Filter Graph</span></span>](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="19219-153">Techniques d' Graph-Building générales</span><span class="sxs-lookup"><span data-stu-id="19219-153">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> <dt>

[<span data-ttu-id="19219-154">Génération du graphique de filtre</span><span class="sxs-lookup"><span data-stu-id="19219-154">Building the Filter Graph</span></span>](building-the-filter-graph.md)
</dt> </dl>

 

 



