---
description: Comment lire un fichier
ms.assetid: 3d8c5d06-8690-4298-a1d1-f21af35bcfd4
title: Comment lire un fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc84ef751db318354da36454e6a30fd2ce4bd8e7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392816"
---
# <a name="how-to-play-a-file"></a><span data-ttu-id="4a3ef-103">Comment lire un fichier</span><span class="sxs-lookup"><span data-stu-id="4a3ef-103">How To Play a File</span></span>

<span data-ttu-id="4a3ef-104">Cet article a pour but de vous offrir la version de la programmation DirectShow.</span><span class="sxs-lookup"><span data-stu-id="4a3ef-104">This article is intended to give you the flavor of DirectShow programming.</span></span> <span data-ttu-id="4a3ef-105">Il présente une application console simple qui lit un fichier audio ou vidéo.</span><span class="sxs-lookup"><span data-stu-id="4a3ef-105">It presents a simple console application that plays an audio or video file.</span></span> <span data-ttu-id="4a3ef-106">Le programme n’a que quelques lignes de long, mais il illustre une partie de la puissance de la programmation DirectShow.</span><span class="sxs-lookup"><span data-stu-id="4a3ef-106">The program is only a few lines long, but it demonstrates some of the power of DirectShow programming.</span></span>

<span data-ttu-id="4a3ef-107">Comme l’explique l’article [sur la programmation d’applications DirectShow](introduction-to-directshow-application-programming.md) , une application DirectShow effectue toujours les mêmes étapes de base :</span><span class="sxs-lookup"><span data-stu-id="4a3ef-107">As the article [Introduction to DirectShow Application Programming](introduction-to-directshow-application-programming.md) describes, a DirectShow application always performs the same basic steps:</span></span>

1.  <span data-ttu-id="4a3ef-108">Créez une instance du [Gestionnaire de graphes de filtre](filter-graph-manager.md).</span><span class="sxs-lookup"><span data-stu-id="4a3ef-108">Create an instance of the [Filter Graph Manager](filter-graph-manager.md).</span></span>
2.  <span data-ttu-id="4a3ef-109">Utilisez le gestionnaire de graphe de filtre pour générer un graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="4a3ef-109">Use the Filter Graph Manager to build a filter graph.</span></span>
3.  <span data-ttu-id="4a3ef-110">Exécuter le graphique, ce qui provoque le déplacement des données dans les filtres.</span><span class="sxs-lookup"><span data-stu-id="4a3ef-110">Run the graph, causing data to move through the filters.</span></span>

<span data-ttu-id="4a3ef-111">Pour compiler et lier le code dans cette rubrique, incluez le fichier d’en-tête DShow. h et un lien vers le fichier de bibliothèque statique strmiids. lib.</span><span class="sxs-lookup"><span data-stu-id="4a3ef-111">To compile and link the code in this topic, include the header file Dshow.h and link to the static library file strmiids.lib.</span></span> <span data-ttu-id="4a3ef-112">Pour plus d’informations, consultez [génération d’applications DirectShow](setting-up-the-build-environment.md).</span><span class="sxs-lookup"><span data-stu-id="4a3ef-112">For more information, see [Building DirectShow Applications](setting-up-the-build-environment.md).</span></span>

<span data-ttu-id="4a3ef-113">Commencez par appeler [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) ou [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) pour initialiser la bibliothèque com :</span><span class="sxs-lookup"><span data-stu-id="4a3ef-113">Start by calling [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) to initialize the COM library:</span></span>


```C++
HRESULT hr = CoInitialize(NULL);
if (FAILED(hr))
{
    // Add error-handling code here. (Omitted for clarity.)
}
```



<span data-ttu-id="4a3ef-114">Pour simplifier les choses, cet exemple ignore la valeur de retour, mais vous devez toujours vérifier la valeur **HRESULT** à partir de n’importe quel appel de méthode.</span><span class="sxs-lookup"><span data-stu-id="4a3ef-114">To keep things simple, this example ignores the return value, but you should always check the **HRESULT** value from any method call.</span></span>

<span data-ttu-id="4a3ef-115">Ensuite, appelez [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer le gestionnaire de graphique de filtre :</span><span class="sxs-lookup"><span data-stu-id="4a3ef-115">Next, call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the Filter Graph Manager:</span></span>


```C++
IGraphBuilder *pGraph;
HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
    CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void **)&pGraph);
```



<span data-ttu-id="4a3ef-116">Comme indiqué, l’identificateur de classe (CLSID) est CLSID \_ FilterGraph.</span><span class="sxs-lookup"><span data-stu-id="4a3ef-116">As shown, the class identifier (CLSID) is CLSID\_FilterGraph.</span></span> <span data-ttu-id="4a3ef-117">Le gestionnaire de graphes de filtres étant fourni par une DLL in-process, le contexte d’exécution est **CLSCTX \_ InProc \_ Server**.</span><span class="sxs-lookup"><span data-stu-id="4a3ef-117">The Filter Graph Manager is provided by an in-process DLL, so the execution context is **CLSCTX\_INPROC\_SERVER**.</span></span> <span data-ttu-id="4a3ef-118">DirectShow prend en charge le modèle de thread libre. vous pouvez donc également appeler [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) avec l’indicateur **coinit \_ multithread** .</span><span class="sxs-lookup"><span data-stu-id="4a3ef-118">DirectShow supports the free-threading model, so you can also call [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) with the **COINIT\_MULTITHREADED** flag.</span></span>

<span data-ttu-id="4a3ef-119">L’appel à [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) retourne l’interface [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) , qui contient principalement des méthodes pour générer le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="4a3ef-119">The call to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) returns the [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface, which mostly contains methods for building the filter graph.</span></span> <span data-ttu-id="4a3ef-120">Deux autres interfaces sont nécessaires pour cet exemple :</span><span class="sxs-lookup"><span data-stu-id="4a3ef-120">Two other interfaces are needed for this example:</span></span>

-   <span data-ttu-id="4a3ef-121">L' [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) contrôle la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="4a3ef-121">[**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) controls streaming.</span></span> <span data-ttu-id="4a3ef-122">Elle contient des méthodes pour l’arrêt et le démarrage du graphique.</span><span class="sxs-lookup"><span data-stu-id="4a3ef-122">It contains methods for stopping and starting the graph.</span></span>
-   <span data-ttu-id="4a3ef-123">[**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) a des méthodes permettant d’obtenir des événements à partir du gestionnaire de graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="4a3ef-123">[**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) has methods for getting events from the Filter Graph Manager.</span></span> <span data-ttu-id="4a3ef-124">Dans cet exemple, l’interface est utilisée pour attendre la fin de la lecture.</span><span class="sxs-lookup"><span data-stu-id="4a3ef-124">In this example, the interface is used to wait for playback to complete.</span></span>

<span data-ttu-id="4a3ef-125">Ces deux interfaces sont exposées par le gestionnaire de graphe de filtre.</span><span class="sxs-lookup"><span data-stu-id="4a3ef-125">Both of these interfaces are exposed by the Filter Graph Manager.</span></span> <span data-ttu-id="4a3ef-126">Utilisez le pointeur [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) retourné pour effectuer une requête :</span><span class="sxs-lookup"><span data-stu-id="4a3ef-126">Use the returned [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) pointer to query for them:</span></span>


```C++
IMediaControl *pControl;
IMediaEvent   *pEvent;
hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



<span data-ttu-id="4a3ef-127">Vous pouvez maintenant générer le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="4a3ef-127">Now you can build the filter graph.</span></span> <span data-ttu-id="4a3ef-128">Pour la lecture de fichiers, cette opération est effectuée par un appel de méthode unique :</span><span class="sxs-lookup"><span data-stu-id="4a3ef-128">For file playback, this is done by a single method call:</span></span>


```C++
hr = pGraph->RenderFile(L"C:\\Example.avi", NULL);
```



<span data-ttu-id="4a3ef-129">La méthode [**IGraphBuilder :: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) crée un graphique de filtre qui peut lire le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="4a3ef-129">The [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) method builds a filter graph that can play the specified file.</span></span> <span data-ttu-id="4a3ef-130">Le premier paramètre est le nom de fichier, représenté sous la forme d’une chaîne de caractères larges (2 octets).</span><span class="sxs-lookup"><span data-stu-id="4a3ef-130">The first parameter is the file name, represented as a wide character (2-byte) string.</span></span> <span data-ttu-id="4a3ef-131">Le deuxième paramètre est réservé et doit être égal à **null**.</span><span class="sxs-lookup"><span data-stu-id="4a3ef-131">The second parameter is reserved and must equal **NULL**.</span></span>

<span data-ttu-id="4a3ef-132">Cette méthode peut échouer si le fichier spécifié n’existe pas ou si le format de fichier n’est pas reconnu.</span><span class="sxs-lookup"><span data-stu-id="4a3ef-132">This method can fail if the specified file does not exist, or the file format is not recognized.</span></span> <span data-ttu-id="4a3ef-133">En supposant que la méthode aboutisse, toutefois, le graphique de filtre est maintenant prêt pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="4a3ef-133">Assuming that the method succeeds, however, the filter graph is now ready for playback.</span></span> <span data-ttu-id="4a3ef-134">Pour exécuter le graphique, appelez la méthode [**IMediaControl :: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) :</span><span class="sxs-lookup"><span data-stu-id="4a3ef-134">To run the graph, call the [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) method:</span></span>


```C++
hr = pControl->Run();
```



<span data-ttu-id="4a3ef-135">Lorsque le graphique de filtre s’exécute, les données se déplacent dans les filtres et sont rendues en tant que vidéo et audio.</span><span class="sxs-lookup"><span data-stu-id="4a3ef-135">When the filter graph runs, data moves through the filters and is rendered as video and audio.</span></span> <span data-ttu-id="4a3ef-136">La lecture se produit sur un thread séparé.</span><span class="sxs-lookup"><span data-stu-id="4a3ef-136">Playback occurs on a separate thread.</span></span> <span data-ttu-id="4a3ef-137">Vous pouvez attendre la fin de la lecture en appelant la méthode [**IMediaEvent :: WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) :</span><span class="sxs-lookup"><span data-stu-id="4a3ef-137">You can wait for playback to complete by calling the [**IMediaEvent::WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) method:</span></span>


```C++
long evCode = 0;
pEvent->WaitForCompletion(INFINITE, &evCode);
```



<span data-ttu-id="4a3ef-138">Cette méthode bloque jusqu’à ce que le fichier soit terminé, ou jusqu’à ce que l’intervalle de délai d’attente spécifié se soit écoulé.</span><span class="sxs-lookup"><span data-stu-id="4a3ef-138">This method blocks until the file is done playing, or until the specified time-out interval elapses.</span></span> <span data-ttu-id="4a3ef-139">La valeur infinie signifie que l’application se bloque indéfiniment jusqu’à ce que le fichier soit terminé.</span><span class="sxs-lookup"><span data-stu-id="4a3ef-139">The value INFINITE means the application blocks indefinitely until the file is done playing.</span></span> <span data-ttu-id="4a3ef-140">Pour obtenir un exemple plus réaliste de gestion des événements, consultez [réponse aux événements](responding-to-events.md).</span><span class="sxs-lookup"><span data-stu-id="4a3ef-140">For a more realistic example of event handling, see [Responding to Events](responding-to-events.md).</span></span>

<span data-ttu-id="4a3ef-141">Lorsque l’application est terminée, libérez les pointeurs d’interface et fermez la bibliothèque COM :</span><span class="sxs-lookup"><span data-stu-id="4a3ef-141">When the application is finished, release the interface pointers and close the COM library:</span></span>


```C++
pControl->Release();
pEvent->Release();
pGraph->Release();
CoUninitialize();
```



## <a name="example-code"></a><span data-ttu-id="4a3ef-142">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="4a3ef-142">Example Code</span></span>

<span data-ttu-id="4a3ef-143">Voici le code complet de l’exemple décrit dans cet article :</span><span class="sxs-lookup"><span data-stu-id="4a3ef-143">Here is the complete code for the example described in this article:</span></span>


```C++
#include <dshow.h>
void main(void)
{
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEvent   *pEvent = NULL;

    // Initialize the COM library.
    HRESULT hr = CoInitialize(NULL);
    if (FAILED(hr))
    {
        printf("ERROR - Could not initialize COM library");
        return;
    }

    // Create the filter graph manager and query for interfaces.
    hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
                        IID_IGraphBuilder, (void **)&pGraph);
    if (FAILED(hr))
    {
        printf("ERROR - Could not create the Filter Graph Manager.");
        return;
    }

    hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
    hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);

    // Build the graph. IMPORTANT: Change this string to a file on your system.
    hr = pGraph->RenderFile(L"C:\\Example.avi", NULL);
    if (SUCCEEDED(hr))
    {
        // Run the graph.
        hr = pControl->Run();
        if (SUCCEEDED(hr))
        {
            // Wait for completion.
            long evCode;
            pEvent->WaitForCompletion(INFINITE, &evCode);

            // Note: Do not use INFINITE in a real application, because it
            // can block indefinitely.
        }
    }
    pControl->Release();
    pEvent->Release();
    pGraph->Release();
    CoUninitialize();
}
```



## <a name="related-topics"></a><span data-ttu-id="4a3ef-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4a3ef-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a3ef-145">Tâches de base de DirectShow</span><span class="sxs-lookup"><span data-stu-id="4a3ef-145">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> </dl>

 

 
