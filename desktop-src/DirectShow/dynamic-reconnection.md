---
description: Reconnexion dynamique
ms.assetid: 5b777f64-6b62-48dd-8eae-6603582a452a
title: Reconnexion dynamique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704178a28b91c6f78bea20b9c73c9a61f80be881
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481849"
---
# <a name="dynamic-reconnection"></a><span data-ttu-id="f8b81-103">Reconnexion dynamique</span><span class="sxs-lookup"><span data-stu-id="f8b81-103">Dynamic Reconnection</span></span>

<span data-ttu-id="f8b81-104">Dans la plupart des filtres DirectShow, les codes confidentiels ne peuvent pas être reconnectés lorsque le graphique diffuse activement des données.</span><span class="sxs-lookup"><span data-stu-id="f8b81-104">In most DirectShow filters, pins cannot be reconnected while the graph is actively streaming data.</span></span> <span data-ttu-id="f8b81-105">L’application doit arrêter le graphique avant de reconnecter les broches.</span><span class="sxs-lookup"><span data-stu-id="f8b81-105">The application must stop the graph before reconnecting the pins.</span></span> <span data-ttu-id="f8b81-106">Toutefois, certains filtres prennent en charge les reconnexions de code confidentiel pendant que le graphique est en cours d’exécution, un processus appelé reconnexion dynamique.</span><span class="sxs-lookup"><span data-stu-id="f8b81-106">However, some filters do support pin reconnections while the graph is running, a process known as dynamic reconnection.</span></span> <span data-ttu-id="f8b81-107">Cela peut être effectué par l’application ou par un filtre dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="f8b81-107">This can be done either by the application, or by a filter in the graph.</span></span>

<span data-ttu-id="f8b81-108">À titre d’exemple, examinez le graphique dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="f8b81-108">As an example, consider the graph in the following illustration.</span></span>

![diagramme de création de graphique dynamique](images/dyngraph.png)

<span data-ttu-id="f8b81-110">Un scénario de reconnexion dynamique peut consister à supprimer le filtre 2 du graphique, tandis que le graphique est en cours d’exécution et à le remplacer par un autre filtre.</span><span class="sxs-lookup"><span data-stu-id="f8b81-110">One scenario for dynamic reconnection might be to remove Filter 2 from the graph, while the graph is running, and replace it with another filter.</span></span> <span data-ttu-id="f8b81-111">Pour que ce scénario fonctionne, les conditions suivantes doivent être remplies :</span><span class="sxs-lookup"><span data-stu-id="f8b81-111">For this scenario to work, the following must be true:</span></span>

-   <span data-ttu-id="f8b81-112">La broche d’entrée sur le filtre 3 (pin D) doit prendre en charge l’interface [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) .</span><span class="sxs-lookup"><span data-stu-id="f8b81-112">The input pin on Filter 3 (pin D) must support the [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) interface.</span></span> <span data-ttu-id="f8b81-113">Cette interface permet de reconnecter le code confidentiel sans arrêter le filtre.</span><span class="sxs-lookup"><span data-stu-id="f8b81-113">This interface enables the pin to be reconnected without stopping the filter.</span></span>
-   <span data-ttu-id="f8b81-114">La broche de sortie sur le filtre 1 (pin A) doit pouvoir bloquer le workflow des données multimédias pendant la reconnexion.</span><span class="sxs-lookup"><span data-stu-id="f8b81-114">The output pin on Filter 1 (pin A) must be able to block the flow of media data while the reconnection occurs.</span></span> <span data-ttu-id="f8b81-115">Aucune donnée ne peut voyager entre le code confidentiel A et le code pin D lors de la reconnexion.</span><span class="sxs-lookup"><span data-stu-id="f8b81-115">No data can travel between pin A and pin D during the reconnection.</span></span> <span data-ttu-id="f8b81-116">En général, cela signifie que la broche de sortie doit prendre en charge l’interface [**IPinFlowControl**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) .</span><span class="sxs-lookup"><span data-stu-id="f8b81-116">Generally, this means the output pin must support the [**IPinFlowControl**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) interface.</span></span> <span data-ttu-id="f8b81-117">Toutefois, si Filter 1 est le filtre qui initie la reconnexion, il peut avoir un mécanisme interne pour bloquer son propre workflow de données.</span><span class="sxs-lookup"><span data-stu-id="f8b81-117">However, if Filter 1 is the filter that initiates the reconnection, it might have some internal mechanism to block its own data flow.</span></span>

<span data-ttu-id="f8b81-118">La reconnexion dynamique implique les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="f8b81-118">The dynamic reconnection will involve the following steps:</span></span>

1.  <span data-ttu-id="f8b81-119">Bloque le flux de données du code confidentiel A.</span><span class="sxs-lookup"><span data-stu-id="f8b81-119">Block the data stream from pin A.</span></span>
2.  <span data-ttu-id="f8b81-120">Reconnectez le code confidentiel A à la broche D, éventuellement par le biais d’un nouveau filtre intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="f8b81-120">Reconnect pin A to pin D, possibly through a new intermediate filter.</span></span>
3.  <span data-ttu-id="f8b81-121">Débloquez le code confidentiel A afin que les données repassent à nouveau.</span><span class="sxs-lookup"><span data-stu-id="f8b81-121">Unblock pin A so that data starts to flow again.</span></span>

<span data-ttu-id="f8b81-122">**Étape 1. Bloquer le flux de données**</span><span class="sxs-lookup"><span data-stu-id="f8b81-122">**Step 1. Block the Data Stream**</span></span>

<span data-ttu-id="f8b81-123">Pour bloquer le flux de données, appelez [**IPinFlowControl :: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) sur le pin A. Cette méthode peut être appelée de façon asynchrone ou synchrone.</span><span class="sxs-lookup"><span data-stu-id="f8b81-123">To block the data stream, call [**IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) on pin A. This method can be called either asynchronously or synchronously.</span></span> <span data-ttu-id="f8b81-124">Pour appeler la méthode de *façon asynchrone*, créez un objet d’événement Win32 et transmettez le descripteur d’événement à la méthode de **bloc** .</span><span class="sxs-lookup"><span data-stu-id="f8b81-124">To call the method *asynchronously*, create a Win32 event object and pass the event handle to the **Block** method.</span></span> <span data-ttu-id="f8b81-125">La méthode est retournée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="f8b81-125">The method will return immediately.</span></span> <span data-ttu-id="f8b81-126">Attendez que l’événement soit signalé, à l’aide d’une fonction telle que **WaitForSingleObject**.</span><span class="sxs-lookup"><span data-stu-id="f8b81-126">Wait for the event to be signaled, using a function such as **WaitForSingleObject**.</span></span> <span data-ttu-id="f8b81-127">Le code confidentiel signale l’événement lorsqu’il a bloqué le Workflow.</span><span class="sxs-lookup"><span data-stu-id="f8b81-127">The pin signals the event when it has blocked the data flow.</span></span> <span data-ttu-id="f8b81-128">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="f8b81-128">For example:</span></span>


```C++
// Create an event
HANDLE hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
if (hEvent != NULL)
{
    // Block the data flow.
    hr = pFlowControl->Block(AM_PIN_FLOW_CONTROL_BLOCK, hEvent); 
    if (SUCCEEDED(hr))
    {
        // Wait for the pin to finish.
        DWORD dwRes = WaitForSingleObject(hEvent, dwMilliseconds);
    }
}
```



<span data-ttu-id="f8b81-129">Pour appeler la méthode de *façon synchrone*, il vous suffit de passer la valeur **null** au lieu du descripteur d’événement.</span><span class="sxs-lookup"><span data-stu-id="f8b81-129">To call the method *synchronously*, simply pass the value **NULL** instead of the event handle.</span></span> <span data-ttu-id="f8b81-130">À présent, la méthode est bloquée jusqu’à ce que l’opération se termine.</span><span class="sxs-lookup"><span data-stu-id="f8b81-130">Now the method will block until the operation completes.</span></span> <span data-ttu-id="f8b81-131">Cela peut ne pas se produire tant que le code confidentiel n’est pas prêt à remettre un nouvel échantillon.</span><span class="sxs-lookup"><span data-stu-id="f8b81-131">This may not happen until the pin is ready to deliver a new sample.</span></span> <span data-ttu-id="f8b81-132">Si le filtre est suspendu, cela peut prendre une durée arbitraire.</span><span class="sxs-lookup"><span data-stu-id="f8b81-132">If the filter is paused, this can take an arbitrary length of time.</span></span> <span data-ttu-id="f8b81-133">Par conséquent, n’effectuez pas l’appel synchrone à partir de votre thread d’application principal.</span><span class="sxs-lookup"><span data-stu-id="f8b81-133">Therefore, do not make the synchronous call from your main application thread.</span></span> <span data-ttu-id="f8b81-134">Utilisez un thread de travail ou appelez la méthode de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="f8b81-134">Use a worker thread, or else call the method asynchronously.</span></span>

<span data-ttu-id="f8b81-135">**Étape 2. Reconnecter les broches**</span><span class="sxs-lookup"><span data-stu-id="f8b81-135">**Step 2. Reconnect the Pins**</span></span>

<span data-ttu-id="f8b81-136">Pour reconnecter les codes confidentiels, interrogez le gestionnaire du graphique de filtre pour l’interface **IGraphConfig** et appelez [**IGraphConfig :: reconnect**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconnect) ou [**IGraphConfig :: reconfigure**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconfigure).</span><span class="sxs-lookup"><span data-stu-id="f8b81-136">To reconnect the pins, query the Filter Graph Manager for the **IGraphConfig** interface and call either [**IGraphConfig::Reconnect**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconnect) or [**IGraphConfig::Reconfigure**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconfigure).</span></span> <span data-ttu-id="f8b81-137">La méthode **reconnect** est plus simple à utiliser ; elle effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="f8b81-137">The **Reconnect** method is simpler to use; it does the following:</span></span>

-   <span data-ttu-id="f8b81-138">Arrête les filtres intermédiaires (filtre 2 dans l’exemple) et les supprime du graphique.</span><span class="sxs-lookup"><span data-stu-id="f8b81-138">Stops the intermediate filters (Filter 2 in the example) and removes them from the graph.</span></span>
-   <span data-ttu-id="f8b81-139">Ajoute de nouveaux filtres intermédiaires, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="f8b81-139">Adds new intermediate filters, if needed.</span></span>
-   <span data-ttu-id="f8b81-140">Connecte toutes les broches.</span><span class="sxs-lookup"><span data-stu-id="f8b81-140">Connects all the pins.</span></span>
-   <span data-ttu-id="f8b81-141">Met en pause ou exécute tout nouveau filtre pour qu’il corresponde à l’état du graphique.</span><span class="sxs-lookup"><span data-stu-id="f8b81-141">Pauses or runs any new filters, to match the state of the graph.</span></span>

<span data-ttu-id="f8b81-142">La méthode **reconnect** comporte plusieurs paramètres facultatifs qui peuvent être utilisés pour spécifier le type de support de la connexion de code confidentiel et le filtre intermédiaire à utiliser.</span><span class="sxs-lookup"><span data-stu-id="f8b81-142">The **Reconnect** method has several optional parameters that can be used to specify the media type for the pin connection and the intermediate filter to use.</span></span> <span data-ttu-id="f8b81-143">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="f8b81-143">For example:</span></span>


```C++
pGraph->AddFilter(pNewFilter, L"New Filter for the Graph");
pConfig->Reconnect(
    pPinA,      // Reconnect this output pin...
    pPinD,      // ... to this input pin.
    pMediaType, // Use this media type.
    pNewFilter, // Connect them through this filter.
    NULL, 
    0);     
```



<span data-ttu-id="f8b81-144">Pour plus d’informations, consultez la page de référence.</span><span class="sxs-lookup"><span data-stu-id="f8b81-144">For details, consult the reference page.</span></span> <span data-ttu-id="f8b81-145">Si la méthode **reconnect** n’est pas suffisamment flexible, vous pouvez utiliser la méthode **reconfigure** , qui appelle une méthode de rappel définie par l’application pour reconnecter les broches.</span><span class="sxs-lookup"><span data-stu-id="f8b81-145">If the **Reconnect** method is not flexible enough, you can use the **Reconfigure** method, which calls an application-defined callback method to reconnect the pins.</span></span> <span data-ttu-id="f8b81-146">Pour utiliser cette méthode, implémentez l’interface [**IGraphConfigCallback**](/windows/desktop/api/Strmif/nn-strmif-igraphconfigcallback) dans votre application.</span><span class="sxs-lookup"><span data-stu-id="f8b81-146">To use this method, implement the [**IGraphConfigCallback**](/windows/desktop/api/Strmif/nn-strmif-igraphconfigcallback) interface in your application.</span></span>

<span data-ttu-id="f8b81-147">Avant d’appeler **reconfigure**, bloquez le workflow à partir de la broche de sortie, comme décrit précédemment.</span><span class="sxs-lookup"><span data-stu-id="f8b81-147">Before calling **Reconfigure**, block the data flow from the output pin, as described previously.</span></span> <span data-ttu-id="f8b81-148">Envoyez ensuite les données qui sont toujours en attente dans la section du graphique que vous reconnectez, comme suit :</span><span class="sxs-lookup"><span data-stu-id="f8b81-148">Then push any data that is still pending in the section of the graph that you are reconnecting, as follows:</span></span>

1.  <span data-ttu-id="f8b81-149">Appelez [**IPinConnection :: NotifyEndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-notifyendofstream) sur la broche d’entrée la plus en aval dans la chaîne de reconnexion (pin D dans l’exemple).</span><span class="sxs-lookup"><span data-stu-id="f8b81-149">Call [**IPinConnection::NotifyEndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-notifyendofstream) on the input pin furthest downstream in the reconnection chain (pin D in the example).</span></span> <span data-ttu-id="f8b81-150">Transmettez un handle à un événement Win32.</span><span class="sxs-lookup"><span data-stu-id="f8b81-150">Pass in a handle to a Win32 event.</span></span>
2.  <span data-ttu-id="f8b81-151">Appelez [**IPIN :: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) sur la broche d’entrée qui est immédiatement en aval de la broche de sortie où vous avez bloqué le Workflow.</span><span class="sxs-lookup"><span data-stu-id="f8b81-151">Call [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) on the input pin that is immediately downstream from the output pin where you blocked the data flow.</span></span> <span data-ttu-id="f8b81-152">(Dans cet exemple, le workflow a été bloqué au niveau du code confidentiel A. vous devez donc appeler **EndOfStream** sur pin B.)</span><span class="sxs-lookup"><span data-stu-id="f8b81-152">(In this example, the data flow was blocked at pin A, so you would call **EndOfStream** on pin B.)</span></span>
3.  <span data-ttu-id="f8b81-153">Attendez que l’événement soit signalé.</span><span class="sxs-lookup"><span data-stu-id="f8b81-153">Wait for the event to be signaled.</span></span> <span data-ttu-id="f8b81-154">La broche d’entrée (pin D) signale l’événement lorsqu’il reçoit la notification de fin de flux.</span><span class="sxs-lookup"><span data-stu-id="f8b81-154">The input pin (pin D) signals the event when it receives the end-of-stream notification.</span></span> <span data-ttu-id="f8b81-155">Cela indique qu’aucune donnée n’est en déplacement entre les broches et que l’appelant peut reconnecter en toute sécurité les broches.</span><span class="sxs-lookup"><span data-stu-id="f8b81-155">This indicates that no data is traveling between the pins, and that the caller can safely reconnect the pins.</span></span>

<span data-ttu-id="f8b81-156">Notez que la méthode **IGraphConfig :: reconnect** gère automatiquement les étapes précédentes.</span><span class="sxs-lookup"><span data-stu-id="f8b81-156">Note that the **IGraphConfig::Reconnect** method automatically handles the previous steps.</span></span> <span data-ttu-id="f8b81-157">Vous devez effectuer ces étapes uniquement si vous utilisez la méthode **reconfigure** .</span><span class="sxs-lookup"><span data-stu-id="f8b81-157">You only need to perform these steps if you are using the **Reconfigure** method.</span></span>

<span data-ttu-id="f8b81-158">Une fois que les données ont fait l’objet d’un push dans le graphique, appelez **reconfigure** et transmettez un pointeur à votre interface de rappel **IGraphConfigCallback** .</span><span class="sxs-lookup"><span data-stu-id="f8b81-158">After the data is pushed through the graph, call **Reconfigure** and pass a pointer to your **IGraphConfigCallback** callback interface.</span></span> <span data-ttu-id="f8b81-159">Le gestionnaire de graphes de filtre appellera la méthode [**IGraphConfigCallback :: reconfigure**](/windows/desktop/api/Strmif/nf-strmif-igraphconfigcallback-reconfigure) que vous avez fournie.</span><span class="sxs-lookup"><span data-stu-id="f8b81-159">The Filter Graph Manager will call the [**IGraphConfigCallback::Reconfigure**](/windows/desktop/api/Strmif/nf-strmif-igraphconfigcallback-reconfigure) method that you have provided.</span></span>

<span data-ttu-id="f8b81-160">**Étape 3. Débloquer le workflow**</span><span class="sxs-lookup"><span data-stu-id="f8b81-160">**Step 3. Unblock the Data Flow**</span></span>

<span data-ttu-id="f8b81-161">Une fois que vous avez reconnecté les codes confidentiels, débloquez le workflow en appelant **IPinFlowControl :: Block** avec une valeur de zéro pour le premier paramètre.</span><span class="sxs-lookup"><span data-stu-id="f8b81-161">After you have reconnected the pins, unblock the data flow by calling **IPinFlowControl::Block** with a value of zero for the first parameter.</span></span>

> [!Note]  
> <span data-ttu-id="f8b81-162">Si une reconnexion dynamique est effectuée par un filtre, vous devez être conscient de certains problèmes de thread.</span><span class="sxs-lookup"><span data-stu-id="f8b81-162">If a dynamic reconnection is performed by a filter, there are some threading issues that you must be aware of.</span></span> <span data-ttu-id="f8b81-163">Si le gestionnaire de graphes de filtre tente d’arrêter le filtre, il peut se bloquer, car le graphique attend que le filtre s’arrête, alors que le filtre peut attendre que les données soient transmises par le biais du graphique.</span><span class="sxs-lookup"><span data-stu-id="f8b81-163">If the Filter Graph Manager tries to stop the filter, it can deadlock, because the graph waits for the filter to stop, while at the same time the filter may be waiting for data to be pushed through the graph.</span></span> <span data-ttu-id="f8b81-164">Pour éviter le blocage possible, certaines des méthodes décrites dans cette section prennent un handle vers un événement Win32.</span><span class="sxs-lookup"><span data-stu-id="f8b81-164">To prevent the possible deadlock, some of the methods described in this section take a handle to a Win32 event.</span></span> <span data-ttu-id="f8b81-165">Le filtre doit signaler l’événement si le gestionnaire du graphique de filtre tente d’arrêter le filtre.</span><span class="sxs-lookup"><span data-stu-id="f8b81-165">The filter should signal the event if the Filter Graph Manager attempts to stop the filter.</span></span> <span data-ttu-id="f8b81-166">Pour plus d’informations, consultez [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) et [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection).</span><span class="sxs-lookup"><span data-stu-id="f8b81-166">For more information, see [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) and [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f8b81-167">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f8b81-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8b81-168">Génération de graphiques dynamiques</span><span class="sxs-lookup"><span data-stu-id="f8b81-168">Dynamic Graph Building</span></span>](dynamic-graph-building.md)
</dt> </dl>

 

 



