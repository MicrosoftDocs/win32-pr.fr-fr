---
description: Contrôle d’un graphique de capture
ms.assetid: e7afafca-e993-4096-bad4-399ee6c67fe9
title: Contrôle d’un graphique de capture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0089fa11adbc0ac861fb9e8e30e2cd0f56b23680
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909047"
---
# <a name="controlling-a-capture-graph"></a><span data-ttu-id="da6af-103">Contrôle d’un graphique de capture</span><span class="sxs-lookup"><span data-stu-id="da6af-103">Controlling a Capture Graph</span></span>

<span data-ttu-id="da6af-104">L’interface [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) du gestionnaire de graphique de filtre a des méthodes pour l’exécution, l’arrêt et la suspension de l’ensemble du graphique.</span><span class="sxs-lookup"><span data-stu-id="da6af-104">The Filter Graph Manager's [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) interface has methods for running, stopping, and pausing the entire graph.</span></span> <span data-ttu-id="da6af-105">Toutefois, si le graphique de filtre a des flux de capture et d’aperçu, vous souhaiterez probablement contrôler les deux flux indépendamment.</span><span class="sxs-lookup"><span data-stu-id="da6af-105">If the filter graph has capture and preview streams, however, you probably want to control the two streams independently.</span></span> <span data-ttu-id="da6af-106">Par exemple, vous souhaiterez peut-être afficher un aperçu de la vidéo sans la capturer.</span><span class="sxs-lookup"><span data-stu-id="da6af-106">For example, you might want to preview the video without capturing it.</span></span> <span data-ttu-id="da6af-107">Pour ce faire, vous pouvez utiliser la méthode [**ICaptureGraphBuilder2 :: ControlStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-controlstream) .</span><span class="sxs-lookup"><span data-stu-id="da6af-107">You can do this through the [**ICaptureGraphBuilder2::ControlStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-controlstream) method.</span></span>

> [!Note]  
> <span data-ttu-id="da6af-108">Cette méthode ne fonctionne pas lors de la capture dans un fichier ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="da6af-108">This method does not work when capturing to an Advanced Systems Format (ASF) file.</span></span>

 

<span data-ttu-id="da6af-109">Contrôle du flux de capture</span><span class="sxs-lookup"><span data-stu-id="da6af-109">Controlling the Capture Stream</span></span>

<span data-ttu-id="da6af-110">Le code suivant définit le flux de capture vidéo à exécuter pendant quatre secondes, à partir d’une seconde après l’exécution du graphique :</span><span class="sxs-lookup"><span data-stu-id="da6af-110">The following code sets the video capture stream to run for four seconds, starting one second after the graph runs:</span></span>


```C++
// Control the video capture stream. 
REFERENCE_TIME rtStart = 10000000, rtStop = 50000000;
const WORD wStartCookie = 1, wStopCookie = 2;  // Arbitrary values.
hr = pBuild->ControlStream(
    &PIN_CATEGORY_CAPTURE, // Pin category.
    &MEDIATYPE_Video,      // Media type.
    pCap,                 // Capture filter.
    &rtStart, &rtStop,     // Start and stop times.
    wStartCookie, wStopCookie  // Values for the start and stop events.
);
pControl->Run();
```



<span data-ttu-id="da6af-111">Le premier paramètre spécifie le flux à contrôler, en tant que GUID de catégorie de code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="da6af-111">The first parameter specifies which stream to control, as a pin category GUID.</span></span> <span data-ttu-id="da6af-112">Le deuxième paramètre donne le type de média.</span><span class="sxs-lookup"><span data-stu-id="da6af-112">The second parameter gives the media type.</span></span> <span data-ttu-id="da6af-113">Le troisième paramètre est un pointeur vers le filtre de capture.</span><span class="sxs-lookup"><span data-stu-id="da6af-113">The third parameter is a pointer to the capture filter.</span></span> <span data-ttu-id="da6af-114">Pour contrôler tous les flux de capture dans le graphique, définissez les deuxième et troisième paramètres sur **null**.</span><span class="sxs-lookup"><span data-stu-id="da6af-114">To control all the capture streams in the graph, set the second and third parameters to **NULL**.</span></span>

<span data-ttu-id="da6af-115">Les deux paramètres suivants définissent les heures de démarrage et d’arrêt du flux, par rapport à l’heure de début de l’exécution du graphique.</span><span class="sxs-lookup"><span data-stu-id="da6af-115">The next two parameters define the times when the stream will start and stop, relative to the time when the graph starts running.</span></span> <span data-ttu-id="da6af-116">Appelez [**IMediaControl :: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) pour exécuter le graphique.</span><span class="sxs-lookup"><span data-stu-id="da6af-116">Call [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) to run the graph.</span></span> <span data-ttu-id="da6af-117">Tant que vous n’avez pas exécuté le graphique, la méthode **ControlStream** n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="da6af-117">Until you run the graph, the **ControlStream** method has no effect.</span></span> <span data-ttu-id="da6af-118">Si le graphique est déjà en cours d’exécution, les paramètres prennent effet immédiatement.</span><span class="sxs-lookup"><span data-stu-id="da6af-118">If the graph is already running, the settings take effect immediately.</span></span>

<span data-ttu-id="da6af-119">Les deux derniers paramètres sont utilisés pour obtenir des notifications d’événements lorsque le flux démarre et s’arrête.</span><span class="sxs-lookup"><span data-stu-id="da6af-119">The last two parameters are used for getting event notifications when the stream starts and stops.</span></span> <span data-ttu-id="da6af-120">Pour chaque flux que vous contrôlez à l’aide de cette méthode, le graphique de filtre envoie une paire d’événements : le contrôle de flux de la [**ce \_ \_ \_ a démarré**](ec-stream-control-started.md) au démarrage du flux et le [**contrôle de \_ flux ce \_ \_ est arrêté**](ec-stream-control-stopped.md) lorsque le flux s’arrête.</span><span class="sxs-lookup"><span data-stu-id="da6af-120">For each stream that you control using this method, the filter graph sends a pair of events: [**EC\_STREAM\_CONTROL\_STARTED**](ec-stream-control-started.md) when the stream starts, and [**EC\_STREAM\_CONTROL\_STOPPED**](ec-stream-control-stopped.md) when the stream stops.</span></span> <span data-ttu-id="da6af-121">Les valeurs de **wStartCookie** et **wStopCookie** sont utilisées comme deuxième paramètre d’événement.</span><span class="sxs-lookup"><span data-stu-id="da6af-121">The values of **wStartCookie** and **wStopCookie** are used as the second event parameter.</span></span> <span data-ttu-id="da6af-122">Ainsi, *lParam2* dans l’événement de début est égal à **wStartCookie** et *lParam2* dans l’événement d’arrêt est égal à **wStopCookie**.</span><span class="sxs-lookup"><span data-stu-id="da6af-122">Thus, *lParam2* in the start event equals **wStartCookie**, and *lParam2* in the stop event equals **wStopCookie**.</span></span> <span data-ttu-id="da6af-123">Le code suivant illustre l’obtention de ces événements :</span><span class="sxs-lookup"><span data-stu-id="da6af-123">The following code shows how to get these events:</span></span>


```C++
while (hr = pEvent->GetEvent(&evCode, &param1, &param2, 0), SUCCEEDED(hr))
{
    switch (evCode)
    {
    case EC_STREAM_CONTROL_STARTED: 
    // param2 == wStartCookie
    break;

    case EC_STREAM_CONTROL_STOPPED: 
    // param2 == wStopCookie
    break;
    
    } 
    pEvent->FreeEventParams(evCode, param1, param2);
}
```



<span data-ttu-id="da6af-124">La méthode **ControlStream** définit des valeurs spéciales pour les heures de début et de fin.</span><span class="sxs-lookup"><span data-stu-id="da6af-124">The **ControlStream** method defines some special values for the start and stop times.</span></span>



| <span data-ttu-id="da6af-125">Étiquette</span><span class="sxs-lookup"><span data-stu-id="da6af-125">Label</span></span> | <span data-ttu-id="da6af-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="da6af-126">Value</span></span> |
|-------------|----------------------------------------|------------------------------------|
|             | <span data-ttu-id="da6af-127">Démarrer</span><span class="sxs-lookup"><span data-stu-id="da6af-127">Start</span></span>                                  | <span data-ttu-id="da6af-128">Stop</span><span class="sxs-lookup"><span data-stu-id="da6af-128">Stop</span></span>                               |
| <span data-ttu-id="da6af-129">MAXLONGLONG</span><span class="sxs-lookup"><span data-stu-id="da6af-129">MAXLONGLONG</span></span> | <span data-ttu-id="da6af-130">Ne jamais démarrer ce flux.</span><span class="sxs-lookup"><span data-stu-id="da6af-130">Never start this stream.</span></span>               | <span data-ttu-id="da6af-131">Ne s’arrête pas tant que le graphique n’est pas arrêté.</span><span class="sxs-lookup"><span data-stu-id="da6af-131">Do not stop until the graph stops.</span></span> |
| <span data-ttu-id="da6af-132">**NULL**</span><span class="sxs-lookup"><span data-stu-id="da6af-132">**NULL**</span></span>    | <span data-ttu-id="da6af-133">Démarrer immédiatement lorsque le graphique s’exécute.</span><span class="sxs-lookup"><span data-stu-id="da6af-133">Start immediately when the graph runs.</span></span> | <span data-ttu-id="da6af-134">Arrêter immédiatement.</span><span class="sxs-lookup"><span data-stu-id="da6af-134">Stop immediately.</span></span>                  |



 

<span data-ttu-id="da6af-135">Par exemple, le code suivant arrête immédiatement le flux de capture :</span><span class="sxs-lookup"><span data-stu-id="da6af-135">For example, the following code stops the capture stream immediately:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap,
    0, 0,     // Start and stop times.
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="da6af-136">Bien que vous puissiez arrêter le flux de capture et le redémarrer ultérieurement, cela crée un intervalle dans les horodatages.</span><span class="sxs-lookup"><span data-stu-id="da6af-136">Although you can stop the capture stream and restart it later, this will create a gap in the time stamps.</span></span> <span data-ttu-id="da6af-137">Lors de la lecture, la vidéo semble bloquée pendant l’intervalle (selon le format de fichier).</span><span class="sxs-lookup"><span data-stu-id="da6af-137">On playback, the video will appear to stall during the gap (depending on the file format).</span></span>

<span data-ttu-id="da6af-138">Contrôle du flux de la version préliminaire</span><span class="sxs-lookup"><span data-stu-id="da6af-138">Controlling the Preview Stream</span></span>

<span data-ttu-id="da6af-139">Pour contrôler la broche d’aperçu, appelez **ControlStream** , mais définissez le premier paramètre sur épingler la \_ catégorie \_ aperçu.</span><span class="sxs-lookup"><span data-stu-id="da6af-139">To control the preview pin, call **ControlStream** but set the first parameter to PIN\_CATEGORY\_PREVIEW.</span></span> <span data-ttu-id="da6af-140">Cela fonctionne comme pour la capture de catégorie de code confidentiel \_ \_ , sauf que vous ne pouvez pas utiliser les temps de référence pour spécifier le démarrage et l’arrêt, car les images d’aperçu n’ont pas de datage.</span><span class="sxs-lookup"><span data-stu-id="da6af-140">This works just like it does for PIN\_CATEGORY\_CAPTURE, except that you cannot use reference times to specify the start and stop, because the preview frames do not have time stamps.</span></span> <span data-ttu-id="da6af-141">Par conséquent, vous devez utiliser la **valeur null** ou MAXLONGLONG.</span><span class="sxs-lookup"><span data-stu-id="da6af-141">Therefore, you must use **NULL** or MAXLONGLONG.</span></span> <span data-ttu-id="da6af-142">Utilisez la **valeur null** pour démarrer le flux de préversion :</span><span class="sxs-lookup"><span data-stu-id="da6af-142">Use **NULL** to start the preview stream:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    NULL,    // Start now.
    0,       // (Don't care.)
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="da6af-143">Utilisez MAXLONGLONG pour arrêter le flux de la version préliminaire :</span><span class="sxs-lookup"><span data-stu-id="da6af-143">Use MAXLONGLONG to stop the preview stream:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    0,               // (Don't care.)
    MAXLONGLONG,     // Stop now.
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="da6af-144">Peu importe si le flux de préversion provient d’une épingle d’aperçu sur le filtre de capture ou du filtre des tees intelligents.</span><span class="sxs-lookup"><span data-stu-id="da6af-144">It does not matter whether the preview stream comes from a preview pin on the capture filter, or from the Smart Tee filter.</span></span> <span data-ttu-id="da6af-145">La méthode **ControlStream** fonctionne dans les deux sens.</span><span class="sxs-lookup"><span data-stu-id="da6af-145">The **ControlStream** method works either way.</span></span>

<span data-ttu-id="da6af-146">Toutefois, pour les broches de port vidéo, la méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="da6af-146">For video port pins, however, the method will fail.</span></span> <span data-ttu-id="da6af-147">Dans ce cas, une autre approche consiste à masquer la fenêtre vidéo.</span><span class="sxs-lookup"><span data-stu-id="da6af-147">In that case, another approach is to hide the video window.</span></span> <span data-ttu-id="da6af-148">Interrogez le graphique pour **IVideoWindow** et utilisez la méthode [**IVideoWindow ::p ut \_ visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) pour afficher ou masquer la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="da6af-148">Query the graph for **IVideoWindow**, and use the [**IVideoWindow::put\_Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) method to show or hide the window.</span></span>


```C++
// Hide the video window.
IVideoWindow *pVidWin = 0;
hr = pGraph->QueryInterface(IID_IVideoWindow, (void**)&pVidWin);
if (SUCCEEDED(hr))
{
    pVidWin->put_Visible(OAFALSE);
    pVidWin->Release();
}
```



<span data-ttu-id="da6af-149">En outre, si vous appelez [**IVideoWindow ::p ut \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) avec la valeur OAFALSE avant d’exécuter le graphique, le filtre de convertisseur vidéo masque la fenêtre jusqu’à ce que vous spécifiiez autrement.</span><span class="sxs-lookup"><span data-stu-id="da6af-149">Also, if you call [**IVideoWindow::put\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) with the value OAFALSE before you run the graph, the Video Renderer filter hides the window until you specify otherwise.</span></span> <span data-ttu-id="da6af-150">Par défaut, le convertisseur vidéo affiche la fenêtre lorsque vous exécutez le graphique.</span><span class="sxs-lookup"><span data-stu-id="da6af-150">By default, the Video Renderer shows the window when you run the graph.</span></span>

<span data-ttu-id="da6af-151">Remarques sur le contrôle Stream</span><span class="sxs-lookup"><span data-stu-id="da6af-151">Remarks about Stream Control</span></span>

<span data-ttu-id="da6af-152">Le comportement par défaut d’un code confidentiel est de fournir des exemples lorsque le graphique s’exécute.</span><span class="sxs-lookup"><span data-stu-id="da6af-152">The default behavior for a pin is to deliver samples when the graph runs.</span></span> <span data-ttu-id="da6af-153">Supposons, par exemple, que vous appelez **ControlStream** avec la \_ capture de catégorie pin \_ mais pas avec l' \_ aperçu de catégorie pin \_ .</span><span class="sxs-lookup"><span data-stu-id="da6af-153">For example, suppose that you call **ControlStream** with PIN\_CATEGORY\_CAPTURE but not with PIN\_CATEGORY\_PREVIEW.</span></span> <span data-ttu-id="da6af-154">Lorsque vous exécutez le graphique, le flux de préversion s’exécute immédiatement, tandis que le flux de capture est exécuté à l’heure que vous avez spécifiée dans **ControlStream**.</span><span class="sxs-lookup"><span data-stu-id="da6af-154">When you run the graph, the preview stream will run immediately, while the capture stream will run at whatever time you specified in **ControlStream**.</span></span>

<span data-ttu-id="da6af-155">Si vous capturez plusieurs flux et les envoyez à un filtre Mux (par exemple, si vous capturez des données audio et vidéo dans un fichier AVI), vous devez contrôler les deux flux en tandem.</span><span class="sxs-lookup"><span data-stu-id="da6af-155">If you are capturing more than one stream and sending them to a mux filter — for example, if you are capturing audio and video to an AVI file — you should control both streams in tandem.</span></span> <span data-ttu-id="da6af-156">Dans le cas contraire, le filtre MUX peut bloquer l’attente d’un flux, car il tente d’entrelacer les deux flux.</span><span class="sxs-lookup"><span data-stu-id="da6af-156">Otherwise, the mux filter might block waiting for one stream, as it tries to interleave the two streams.</span></span> <span data-ttu-id="da6af-157">Définissez les mêmes heures de démarrage et d’arrêt sur tous les flux de capture avant d’exécuter le graphique :</span><span class="sxs-lookup"><span data-stu-id="da6af-157">Set the same start and stop times on all capture streams before running the graph:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, 
    
NULL, NULL,       // All capture streams.
    &rtStart, rtStop, 
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="da6af-158">En interne, la méthode **ControlStream** utilise l’interface [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) , qui est exposée sur les broches du filtre de capture, le filtre tee intelligent (le cas échéant) et éventuellement le filtre Mux.</span><span class="sxs-lookup"><span data-stu-id="da6af-158">Internally, the **ControlStream** method uses the [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) interface, which is exposed on the pins of the capture filter, the Smart Tee filter (if present), and possibly the mux filter.</span></span> <span data-ttu-id="da6af-159">Vous pouvez utiliser cette interface directement, au lieu d’appeler **ControlStream**, bien qu’il n’y ait aucun avantage particulier à le faire.</span><span class="sxs-lookup"><span data-stu-id="da6af-159">You can use this interface directly, instead of calling **ControlStream**, although there is no particular advantage to doing so.</span></span>

## <a name="related-topics"></a><span data-ttu-id="da6af-160">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="da6af-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da6af-161">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="da6af-161">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



