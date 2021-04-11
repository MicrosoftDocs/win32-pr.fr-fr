---
description: Aperçu d’un projet
ms.assetid: 2efa3f25-a93f-4362-b461-b67475e5d78c
title: Aperçu d’un projet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cd9d299a99a0a7315cec986fbc044d427385647
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317669"
---
# <a name="previewing-a-project"></a><span data-ttu-id="4cc83-103">Aperçu d’un projet</span><span class="sxs-lookup"><span data-stu-id="4cc83-103">Previewing a Project</span></span>

<span data-ttu-id="4cc83-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="4cc83-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="4cc83-105">Pour afficher un aperçu d’un projet, appelez d’abord **CoCreateInstance** pour créer une instance du moteur de rendu de base.</span><span class="sxs-lookup"><span data-stu-id="4cc83-105">To preview a project, first call **CoCreateInstance** to create an instance of the Basic Render Engine.</span></span> <span data-ttu-id="4cc83-106">L’identificateur de classe est CLSID \_ RenderEngine.</span><span class="sxs-lookup"><span data-stu-id="4cc83-106">The class identifier is CLSID\_RenderEngine.</span></span> <span data-ttu-id="4cc83-107">Appelez ensuite la méthode [**IRenderEngine :: SetTimelineObject**](irenderengine-settimelineobject.md) pour spécifier la chronologie que vous rendez.</span><span class="sxs-lookup"><span data-stu-id="4cc83-107">Then call the [**IRenderEngine::SetTimelineObject**](irenderengine-settimelineobject.md) method to specify the timeline that you are rendering.</span></span>

<span data-ttu-id="4cc83-108">La première fois que vous affichez un aperçu de la chronologie, effectuez les appels suivants dans l’ordre indiqué :</span><span class="sxs-lookup"><span data-stu-id="4cc83-108">The first time that you preview the timeline, perform the following calls in the order listed:</span></span>

1.  <span data-ttu-id="4cc83-109">Appelez [**IRenderEngine :: SetRenderRange**](irenderengine-setrenderrange.md) pour spécifier la partie de la chronologie à afficher.</span><span class="sxs-lookup"><span data-stu-id="4cc83-109">Call [**IRenderEngine::SetRenderRange**](irenderengine-setrenderrange.md) to specify which portion of the timeline to preview.</span></span> <span data-ttu-id="4cc83-110">(facultatif)</span><span class="sxs-lookup"><span data-stu-id="4cc83-110">(Optional)</span></span>
2.  <span data-ttu-id="4cc83-111">Appelez [**IRenderEngine :: ConnectFrontEnd**](irenderengine-connectfrontend.md) pour créer le composant frontal du graphique.</span><span class="sxs-lookup"><span data-stu-id="4cc83-111">Call [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) to build the front end of the graph.</span></span>
3.  <span data-ttu-id="4cc83-112">Appelez [**IRenderEngine :: RenderOutputPins**](irenderengine-renderoutputpins.md).</span><span class="sxs-lookup"><span data-stu-id="4cc83-112">Call [**IRenderEngine::RenderOutputPins**](irenderengine-renderoutputpins.md).</span></span> <span data-ttu-id="4cc83-113">Cette méthode connecte chaque broche de sortie à un convertisseur vidéo ou audio, en terminant le graphique.</span><span class="sxs-lookup"><span data-stu-id="4cc83-113">This method connects each output pin to a video renderer or audio renderer, completing the graph.</span></span>

<span data-ttu-id="4cc83-114">L’exemple de code suivant illustre ces étapes :</span><span class="sxs-lookup"><span data-stu-id="4cc83-114">The following code example shows these steps:</span></span>


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, 
    CLSCTX_INPROC_SERVER, IID_IRenderEngine, (void**)&pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd();
hr = pRender->RenderOutputPins();
```



<span data-ttu-id="4cc83-115">Exécutez maintenant le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="4cc83-115">Now run the filter graph.</span></span> <span data-ttu-id="4cc83-116">Tout d’abord, appelez la méthode [**IRenderEngine :: GetFilterGraph**](irenderengine-getfiltergraph.md) pour récupérer un pointeur vers l’interface [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) du gestionnaire de graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="4cc83-116">First, call the [**IRenderEngine::GetFilterGraph**](irenderengine-getfiltergraph.md) method to retrieve a pointer to the Filter Graph Manager's [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface.</span></span> <span data-ttu-id="4cc83-117">Interrogez ensuite le gestionnaire de graphe de filtre pour l’interface [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) et appelez [**IMediaControl :: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), comme indiqué dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="4cc83-117">Then query the Filter Graph Manager for the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) interface and call [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), as shown in the following code:</span></span>


```C++
IGraphBuilder   *pGraph = NULL;
IMediaControl   *pControl = NULL;
hr = pRender->GetFilterGraph(&pGraph);
hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
hr = pControl->Run();
```



<span data-ttu-id="4cc83-118">Utilisez l’interface [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) du gestionnaire de graphique de filtre pour attendre la fin de l’aperçu.</span><span class="sxs-lookup"><span data-stu-id="4cc83-118">Use the Filter Graph Manager's [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interface to wait for the preview to complete.</span></span> <span data-ttu-id="4cc83-119">Vous pouvez également rechercher le graphique à l’aide de l’interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) du gestionnaire de graphique de filtre, comme vous le feriez avec un graphique de lecture de fichier.</span><span class="sxs-lookup"><span data-stu-id="4cc83-119">You can also seek the graph using the Filter Graph Manager's [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface, just as you would with a file playback graph.</span></span>

<span data-ttu-id="4cc83-120">Pour réafficher un aperçu du projet, recherchez à nouveau le graphique sur l’heure zéro et rappelez l' **exécution** .</span><span class="sxs-lookup"><span data-stu-id="4cc83-120">To preview the project again, seek the graph back to time zero and call **Run** again.</span></span> <span data-ttu-id="4cc83-121">Si vous modifiez le contenu de la chronologie, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="4cc83-121">If you change the contents of the timeline, do the following:</span></span>

1.  <span data-ttu-id="4cc83-122">Appelez **SetRenderRange**.</span><span class="sxs-lookup"><span data-stu-id="4cc83-122">Call **SetRenderRange**.</span></span> <span data-ttu-id="4cc83-123">(facultatif)</span><span class="sxs-lookup"><span data-stu-id="4cc83-123">(Optional)</span></span>
2.  <span data-ttu-id="4cc83-124">Appelez **ConnectFrontEnd**.</span><span class="sxs-lookup"><span data-stu-id="4cc83-124">Call **ConnectFrontEnd**.</span></span>
3.  <span data-ttu-id="4cc83-125">Si la méthode **ConnectFrontEnd** retourne S \_ WARN \_ OUTPUTRESET, appelez **RenderOutputPins**.</span><span class="sxs-lookup"><span data-stu-id="4cc83-125">If the **ConnectFrontEnd** method returns S\_WARN\_OUTPUTRESET, call **RenderOutputPins**.</span></span> <span data-ttu-id="4cc83-126">(Si **ConnectFrontEnd** retourne S \_ OK, vous pouvez ignorer cette étape.)</span><span class="sxs-lookup"><span data-stu-id="4cc83-126">(If **ConnectFrontEnd** returns S\_OK, you can skip this step.)</span></span>
4.  <span data-ttu-id="4cc83-127">Recherche le graphique sur l’heure zéro.</span><span class="sxs-lookup"><span data-stu-id="4cc83-127">Seek the graph back to time zero.</span></span>
5.  <span data-ttu-id="4cc83-128">Exécutez le graphique.</span><span class="sxs-lookup"><span data-stu-id="4cc83-128">Run the graph.</span></span>

<span data-ttu-id="4cc83-129">L’exemple suivant illustre ces étapes :</span><span class="sxs-lookup"><span data-stu-id="4cc83-129">The following example shows these steps:</span></span>


```C++
hr = pRender->ConnectFrontEnd();
if (hr == S_WARN_OUTPUTRESET)
{
    hr = pRender->RenderOutputPins();
}
LONGLONG llStart = 0; 
hr = pSeek->SetPositions(&llStart, AM_SEEKING_AbsolutePositioning, 0, 0); 
hr = pControl->Run();
```



<span data-ttu-id="4cc83-130">Pour obtenir un exemple complet qui charge et affiche un aperçu d’un fichier projet, consultez [chargement et affichage de l’aperçu d’un projet](loading-and-previewing-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="4cc83-130">For a complete example that loads and previews a project file, see [Loading and Previewing a Project](loading-and-previewing-a-project.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4cc83-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4cc83-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4cc83-132">Gestion des projets de montage vidéo</span><span class="sxs-lookup"><span data-stu-id="4cc83-132">Managing Video Editing Projects</span></span>](managing-video-editing-projects.md)
</dt> <dt>

[<span data-ttu-id="4cc83-133">Rendu d’un projet</span><span class="sxs-lookup"><span data-stu-id="4cc83-133">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 



