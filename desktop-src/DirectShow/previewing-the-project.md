---
description: Aperçu du projet
ms.assetid: 00d72a39-f848-47ea-8460-8b826684eeea
title: Aperçu du projet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bdf38fe19e500cfe9bd9a8dfb77f7ff56528a2f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103950267"
---
# <a name="previewing-the-project"></a><span data-ttu-id="62270-103">Aperçu du projet</span><span class="sxs-lookup"><span data-stu-id="62270-103">Previewing the Project</span></span>

<span data-ttu-id="62270-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="62270-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="62270-105">Pour afficher un aperçu du projet, vous avez besoin d’un composant appelé « *moteur de rendu*», qui génère un graphique de filtre DirectShow à partir d’une chronologie.</span><span class="sxs-lookup"><span data-stu-id="62270-105">To preview the project, you need a component called a *render engine*, which builds a DirectShow filter graph from a timeline.</span></span> <span data-ttu-id="62270-106">Le graphique de filtre est ce qui restitue réellement le projet.</span><span class="sxs-lookup"><span data-stu-id="62270-106">The filter graph is what actually renders the project.</span></span> <span data-ttu-id="62270-107">Vous pouvez utiliser le moteur de rendu pour afficher un aperçu d’un projet ou écrire le fichier de sortie final.</span><span class="sxs-lookup"><span data-stu-id="62270-107">You can use the render engine to preview a project or to write the final output file.</span></span>

<span data-ttu-id="62270-108">Cet article ne décrit pas en détail le moteur de rendu.</span><span class="sxs-lookup"><span data-stu-id="62270-108">This article does not go into detail about the render engine.</span></span> <span data-ttu-id="62270-109">Pour la version préliminaire, vous n’avez besoin que de quelques appels de méthode.</span><span class="sxs-lookup"><span data-stu-id="62270-109">For preview, you only need a few method calls.</span></span> <span data-ttu-id="62270-110">Vous pouvez trouver une discussion plus approfondie, y compris comment écrire des fichiers de sortie, dans le [rendu d’un projet](rendering-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="62270-110">You can find a more thorough discussion, including how to write output files, in [Rendering a Project](rendering-a-project.md).</span></span> <span data-ttu-id="62270-111">L’exemple de code suivant montre comment construire un graphique d’aperçu.</span><span class="sxs-lookup"><span data-stu-id="62270-111">The following code example shows how to construct a preview graph.</span></span>


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC_SERVER,
            IID_IRenderEngine, (void**) &pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd( );
hr = pRender->RenderOutputPins( );
```



<span data-ttu-id="62270-112">Créez le moteur de rendu à l’aide de la fonction **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="62270-112">Create the render engine using the **CoCreateInstance** function.</span></span> <span data-ttu-id="62270-113">Appelez ensuite les méthodes suivantes sur l’interface [**IRenderEngine**](irenderengine.md) du moteur de rendu :</span><span class="sxs-lookup"><span data-stu-id="62270-113">Then call the following methods on the render engine's [**IRenderEngine**](irenderengine.md) interface:</span></span>

-   <span data-ttu-id="62270-114">[**SetTimelineObject**](irenderengine-settimelineobject.md).</span><span class="sxs-lookup"><span data-stu-id="62270-114">[**SetTimelineObject**](irenderengine-settimelineobject.md).</span></span> <span data-ttu-id="62270-115">Spécifie la chronologie à utiliser.</span><span class="sxs-lookup"><span data-stu-id="62270-115">Specifies the timeline to use.</span></span>
-   <span data-ttu-id="62270-116">[**ConnectFrontEnd**](irenderengine-connectfrontend.md).</span><span class="sxs-lookup"><span data-stu-id="62270-116">[**ConnectFrontEnd**](irenderengine-connectfrontend.md).</span></span> <span data-ttu-id="62270-117">Génère un graphique de filtre partiel, avec une broche de sortie pour chaque groupe dans la chronologie.</span><span class="sxs-lookup"><span data-stu-id="62270-117">Builds a partial filter graph, with one output pin for each group in the timeline.</span></span>
-   <span data-ttu-id="62270-118">[**RenderOutputPins**](irenderengine-renderoutputpins.md).</span><span class="sxs-lookup"><span data-stu-id="62270-118">[**RenderOutputPins**](irenderengine-renderoutputpins.md).</span></span> <span data-ttu-id="62270-119">Termine le graphique d’aperçu en connectant chaque broche de sortie à un convertisseur audio ou vidéo.</span><span class="sxs-lookup"><span data-stu-id="62270-119">Completes the preview graph by connecting each output pin to a video or audio renderer.</span></span>

<span data-ttu-id="62270-120">Une fois le graphique créé, vous pouvez afficher un aperçu du projet en exécutant le graphique, comme vous le feriez avec n’importe quel graphique de filtre DirectShow.</span><span class="sxs-lookup"><span data-stu-id="62270-120">Once the graph is built, you can preview the project by running the graph, as you would with any DirectShow filter graph.</span></span> <span data-ttu-id="62270-121">Tout d’abord, obtenez un pointeur vers le graphique de filtre en appelant la méthode [**IRenderEngine :: GetFilterGraph**](irenderengine-getfiltergraph.md) .</span><span class="sxs-lookup"><span data-stu-id="62270-121">First, obtain a pointer to the filter graph by calling the [**IRenderEngine::GetFilterGraph**](irenderengine-getfiltergraph.md) method.</span></span>


```C++
IGraphBuilder   *pGraph = NULL;
hr = pRender->GetFilterGraph(&pGraph);
```



<span data-ttu-id="62270-122">Interrogez le graphique de filtre pour les interfaces [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) et [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) .</span><span class="sxs-lookup"><span data-stu-id="62270-122">Query the filter graph for the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) and [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) interfaces.</span></span> <span data-ttu-id="62270-123">Utilisez ces deux interfaces pour exécuter le graphique et attendre la fin de la lecture.</span><span class="sxs-lookup"><span data-stu-id="62270-123">Use these two interfaces to run the graph and wait for playback to complete.</span></span> <span data-ttu-id="62270-124">Pour obtenir une explication de l’utilisation de ces interfaces, consultez [Comment lire un fichier](how-to-play-a-file.md) et [répondre à des événements](responding-to-events.md).</span><span class="sxs-lookup"><span data-stu-id="62270-124">For an explanation of how to use these interfaces, see [How To Play a File](how-to-play-a-file.md) and [Responding to Events](responding-to-events.md).</span></span> <span data-ttu-id="62270-125">Le code suivant illustre une façon d’utiliser ces interfaces.</span><span class="sxs-lookup"><span data-stu-id="62270-125">The following code shows one way to use these interfaces.</span></span>


```C++
IMediaControl   *pControl = NULL;
IMediaEvent     *pEvent = NULL;
long evCode;
pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
hr = pControl->Run();
hr = pEvent->WaitForCompletion(INFINITE, &evCode);
pControl->Stop();
```



<span data-ttu-id="62270-126">Le code de cet exemple bloque l’exécution du programme jusqu’à la fin de la lecture, en raison du paramètre infini dans l’appel de la méthode [**IMediaEvent :: WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) .</span><span class="sxs-lookup"><span data-stu-id="62270-126">The code in this example blocks program execution until playback completes, because of the INFINITE parameter in the [**IMediaEvent::WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) method call.</span></span> <span data-ttu-id="62270-127">En cas de problème lors de la lecture, toutefois, cela peut entraîner le blocage du programme.</span><span class="sxs-lookup"><span data-stu-id="62270-127">If something goes wrong during playback, however, it could cause the program to stop responding.</span></span> <span data-ttu-id="62270-128">Dans une application réelle, utilisez une boucle de messages pour attendre la fin de la lecture.</span><span class="sxs-lookup"><span data-stu-id="62270-128">In a real application, use a message loop to wait for playback to complete.</span></span> <span data-ttu-id="62270-129">Il est également recommandé de fournir à l’utilisateur un moyen d’interrompre la lecture.</span><span class="sxs-lookup"><span data-stu-id="62270-129">It's also recommended that you provide the user with a way to interrupt playback.</span></span>

<span data-ttu-id="62270-130">Lorsque vous avez terminé d’utiliser le moteur de rendu, appelez toujours la méthode [**IRenderEngine :: ScrapIt**](irenderengine-scrapit.md) .</span><span class="sxs-lookup"><span data-stu-id="62270-130">When you finish using the render engine, always call the [**IRenderEngine::ScrapIt**](irenderengine-scrapit.md) method.</span></span> <span data-ttu-id="62270-131">Cette méthode supprime le graphique de filtre et libère toutes les ressources détenues par le moteur de rendu.</span><span class="sxs-lookup"><span data-stu-id="62270-131">This method deletes the filter graph and releases any resources held by the render engine.</span></span>


```C++
pRender->ScrapIt();
```



## <a name="related-topics"></a><span data-ttu-id="62270-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="62270-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62270-133">Chargement et affichage de l’aperçu d’un projet</span><span class="sxs-lookup"><span data-stu-id="62270-133">Loading and Previewing a Project</span></span>](loading-and-previewing-a-project.md)
</dt> </dl>

 

 



