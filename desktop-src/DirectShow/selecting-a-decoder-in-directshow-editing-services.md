---
description: Sélection d’un décodeur dans les services de modification DirectShow
ms.assetid: dc6b0445-7fc1-4331-9000-a652b44a8364
title: Sélection d’un décodeur dans les services de modification DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 956ad0284722eb394590b1b0065f167c55b3cf51
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481512"
---
# <a name="selecting-a-decoder-in-directshow-editing-services"></a><span data-ttu-id="dea46-103">Sélection d’un décodeur dans les services de modification DirectShow</span><span class="sxs-lookup"><span data-stu-id="dea46-103">Selecting a Decoder in DirectShow Editing Services</span></span>

<span data-ttu-id="dea46-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="dea46-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="dea46-105">Lorsque les [services d’édition DirectShow](directshow-editing-services.md) affichent un projet de montage vidéo, le moteur de rendu sélectionne automatiquement les décodeurs nécessaires.</span><span class="sxs-lookup"><span data-stu-id="dea46-105">When [DirectShow Editing Services](directshow-editing-services.md) (DES) renders a video editing project, the Rendering Engine automatically selects the necessary decoders.</span></span> <span data-ttu-id="dea46-106">Cela peut se produire à l’intérieur de la méthode [**IRenderEngine :: ConnectFrontEnd**](irenderengine-connectfrontend.md) , ou de manière dynamique pendant le rendu.</span><span class="sxs-lookup"><span data-stu-id="dea46-106">This may happen inside the [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) method, or else dynamically during rendering.</span></span>

<span data-ttu-id="dea46-107">Un utilisateur peut installer plusieurs décodeurs capable de décoder un fichier particulier.</span><span class="sxs-lookup"><span data-stu-id="dea46-107">A user might install several decoders that are capable of decoding a particular file.</span></span> <span data-ttu-id="dea46-108">Quand plusieurs décodeurs sont disponibles, l’algorithme DES utilise l’algorithme de [connexion intelligente](intelligent-connect.md) pour sélectionner le décodeur.</span><span class="sxs-lookup"><span data-stu-id="dea46-108">When multiple decoders are available, DES uses the [Intelligent Connect](intelligent-connect.md) algorithm to select the decoder.</span></span>

<span data-ttu-id="dea46-109">Il n’existe aucun moyen pour l’application de spécifier directement le décodeur à utiliser.</span><span class="sxs-lookup"><span data-stu-id="dea46-109">There is no way for the application to specify directly which decoder to use.</span></span> <span data-ttu-id="dea46-110">Toutefois, vous pouvez choisir le décodeur indirectement par le biais de l’interface de rappel [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) .</span><span class="sxs-lookup"><span data-stu-id="dea46-110">However, you can choose the decoder indirectly through the [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) callback interface.</span></span> <span data-ttu-id="dea46-111">En implémentant cette interface dans votre application, vous pouvez recevoir des notifications pendant le processus de création de graphiques et rejeter certains filtres du graphique.</span><span class="sxs-lookup"><span data-stu-id="dea46-111">By implementing this interface in your application, you can receive notifications during the graph-building process and reject certain filters from the graph.</span></span>

<span data-ttu-id="dea46-112">Commencez par implémenter une classe qui expose l’interface [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) :</span><span class="sxs-lookup"><span data-stu-id="dea46-112">Start by implementing a class that exposes the [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) interface:</span></span>


```C++
class GraphBuilderCB : public IAMGraphBuilderCallback
{
public:
     // Method declarations (not shown).
};
```



<span data-ttu-id="dea46-113">Créez ensuite une instance du gestionnaire de graphes de filtres et enregistrez votre classe pour recevoir des notifications de rappel :</span><span class="sxs-lookup"><span data-stu-id="dea46-113">Then create an instance of the Filter Graph Manager and register your class to receive callback notifications:</span></span>


```C++
// Declare an instance of the callback object.
GraphBuilderCB GraphCB; 

// Create the Filter Graph Manager.
CComPtr<IGraphBuilder> pGraph;
hr = pGraph.CoCreateInstance(CLSID_FilterGraph);
if (FAILED(hr))
{
    // Handle error (not shown).
}
// Register to receive the callbacks.
CComQIPtr<IObjectWithSite> pSite(pGraph);
if (pSite)
{
    hr = pSite->SetSite((IUnknown*)&GraphCB);
}
```



<span data-ttu-id="dea46-114">Ensuite, créez le moteur de rendu et appelez la méthode [**IRenderEngine :: SetFilterGraph**](irenderengine-setfiltergraph.md) avec un pointeur vers le gestionnaire de graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="dea46-114">Next, create the Render Engine and call the [**IRenderEngine::SetFilterGraph**](irenderengine-setfiltergraph.md) method with a pointer to the Filter Graph Manager.</span></span> <span data-ttu-id="dea46-115">Cela garantit que le moteur de rendu ne crée pas son propre gestionnaire de graphes de filtre, mais utilise à la place l’instance que vous avez configurée pour les rappels.</span><span class="sxs-lookup"><span data-stu-id="dea46-115">This ensures that the Render Engine does not create its own Filter Graph Manager, but instead uses the instance that you have configured for callbacks.</span></span>


```C++
CComPtr<IRenderEngine> pRender;
hr = pRender.CoCreateInstance(CLSID_RenderEngine);
if (FAILED(hr))
{
    // Handle error (not shown).
}

hr = pRender->SetFilterGraph(pGraph);
```



<span data-ttu-id="dea46-116">Lorsque le projet est rendu, la méthode [**IAMGraphBuilderCallback :: SelectedFilter**](/windows/desktop/api/Strmif/nf-strmif-iamgraphbuildercallback-selectedfilter) de l’application est appelée immédiatement avant que le gestionnaire de graphique de filtre crée un nouveau filtre.</span><span class="sxs-lookup"><span data-stu-id="dea46-116">When the project is rendered, the application's [**IAMGraphBuilderCallback::SelectedFilter**](/windows/desktop/api/Strmif/nf-strmif-iamgraphbuildercallback-selectedfilter) method is called immediately before the Filter Graph Manager creates a new filter.</span></span> <span data-ttu-id="dea46-117">La méthode **SelectedFilter** reçoit un pointeur vers une interface **IMoniker** qui représente un moniker pour le filtre.</span><span class="sxs-lookup"><span data-stu-id="dea46-117">The **SelectedFilter** method receives a pointer to an **IMoniker** interface that represents a moniker for the filter.</span></span> <span data-ttu-id="dea46-118">Examinez le moniker et, si vous décidez de rejeter le filtre, retournez un code d’erreur à partir de la méthode **SelectedFilter** .</span><span class="sxs-lookup"><span data-stu-id="dea46-118">Examine the moniker, and if you decide to reject the filter, return a failure code from the **SelectedFilter** method.</span></span>

<span data-ttu-id="dea46-119">La partie difficile consiste à identifier les monikers qui représentent des décodeurs, et en particulier les monikers qui représentent des décodeurs que vous souhaitez rejeter.</span><span class="sxs-lookup"><span data-stu-id="dea46-119">The difficult part is to identify which monikers represent decoders — and in particular, which monikers represent decoders that you want to reject.</span></span> <span data-ttu-id="dea46-120">Une solution est la suivante :</span><span class="sxs-lookup"><span data-stu-id="dea46-120">One solution is the following:</span></span>

-   <span data-ttu-id="dea46-121">Avant de restituer le projet, utilisez la méthode [**IFilterMapper2 :: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) pour créer une liste de filtres inscrits comme acceptant le type d’entrée souhaité.</span><span class="sxs-lookup"><span data-stu-id="dea46-121">Before rendering the project, use the [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) method to create a list of filters that are registered as accepting the desired input type.</span></span> <span data-ttu-id="dea46-122">Pour les types de compression vidéo ou audio, cette liste doit être mappée à un ensemble de décodeurs.</span><span class="sxs-lookup"><span data-stu-id="dea46-122">For video or audio compression types, this list should map to a set of decoders.</span></span>
-   <span data-ttu-id="dea46-123">La méthode **EnumMatchingFilters** retourne une collection de monikers.</span><span class="sxs-lookup"><span data-stu-id="dea46-123">The **EnumMatchingFilters** method returns a collection of monikers.</span></span> <span data-ttu-id="dea46-124">Pour chaque moniker de la collection, récupérez la propriété **DisplayName** , comme décrit dans [utilisation du mappeur de filtre](using-the-filter-mapper.md).</span><span class="sxs-lookup"><span data-stu-id="dea46-124">For each moniker in the collection, get the **DisplayName** property, as described in [Using the Filter Mapper](using-the-filter-mapper.md).</span></span>
-   <span data-ttu-id="dea46-125">Stockez une liste des noms complets, mais omettez le nom complet qui correspond au filtre que vous souhaitez utiliser pour le décodage.</span><span class="sxs-lookup"><span data-stu-id="dea46-125">Store a list of the display names, but omit the display name that matches the filter you want to use for decoding.</span></span> <span data-ttu-id="dea46-126">Les noms d’affichage des filtres logiciels se présentent sous la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="dea46-126">Display names for software filters have the following form:</span></span>

    ```C++
    OLESTR("@device:sw:{CategoryGUID}\{FilterCLSID}");
    ```

    

    <span data-ttu-id="dea46-127">where</span><span class="sxs-lookup"><span data-stu-id="dea46-127">where</span></span>

    ```C++
    CategoryGUID
    ```

    

    <span data-ttu-id="dea46-128">est le GUID de la catégorie de filtre, et</span><span class="sxs-lookup"><span data-stu-id="dea46-128">is the GUID of the filter category, and</span></span>

    ```C++
    FilterCLSID
    ```

    

    <span data-ttu-id="dea46-129">est le CLSID du filtre.</span><span class="sxs-lookup"><span data-stu-id="dea46-129">is the filter's CLSID.</span></span> <span data-ttu-id="dea46-130">Pour DMOs, le format est le même, mais il prend la `sw` valeur `dmo` .</span><span class="sxs-lookup"><span data-stu-id="dea46-130">For DMOs, the format is the same, but change `sw` to `dmo`.</span></span>

    <span data-ttu-id="dea46-131">La liste contient maintenant des noms complets pour chaque filtre qui génère le type de média souhaité, mais n’est pas votre filtre préféré.</span><span class="sxs-lookup"><span data-stu-id="dea46-131">The list now contains display names for every filter that outputs the desired media type but is not your preferred filter.</span></span>

-   <span data-ttu-id="dea46-132">Dans la méthode **SelectedFilter** , récupérez la propriété **DisplayName** sur le moniker proposé et vérifiez-le par rapport à la liste stockée.</span><span class="sxs-lookup"><span data-stu-id="dea46-132">In the **SelectedFilter** method, get the **DisplayName** property on the proposed moniker and check it against the stored list.</span></span> <span data-ttu-id="dea46-133">Si le nom complet correspond à une entrée de la liste, rejeter ce filtre.</span><span class="sxs-lookup"><span data-stu-id="dea46-133">If the display name matches an entry in the list, reject that filter.</span></span> <span data-ttu-id="dea46-134">Dans le cas contraire, acceptez-le en renvoyant S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dea46-134">Otherwise, accept it by returning S\_OK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dea46-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dea46-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dea46-136">Rendu d’un projet</span><span class="sxs-lookup"><span data-stu-id="dea46-136">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 



