---
description: Cet article explique comment répondre aux événements qui se produisent dans un graphique de filtre.
ms.assetid: 1c09149b-7f34-4296-bd32-dbbae5e1d62b
title: Réponse aux événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a51481371501c05733e5f637885a71001c1f996
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521399"
---
# <a name="responding-to-events"></a><span data-ttu-id="e1597-103">Réponse aux événements</span><span class="sxs-lookup"><span data-stu-id="e1597-103">Responding to Events</span></span>

<span data-ttu-id="e1597-104">Cet article explique comment répondre aux événements qui se produisent dans un graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="e1597-104">This article describes how to respond to events that occur in a filter graph.</span></span>

## <a name="how-event-notification-works"></a><span data-ttu-id="e1597-105">Fonctionnement de la notification d’événement</span><span class="sxs-lookup"><span data-stu-id="e1597-105">How Event Notification Works</span></span>

<span data-ttu-id="e1597-106">Pendant l’exécution d’une application DirectShow, les événements peuvent se produire dans le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="e1597-106">While a DirectShow application is running, events can occur within the filter graph.</span></span> <span data-ttu-id="e1597-107">Par exemple, un filtre peut rencontrer une erreur de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="e1597-107">For example, a filter might encounter a streaming error.</span></span> <span data-ttu-id="e1597-108">Les filtres alertent le gestionnaire du graphique de filtre en envoyant des événements, qui consistent en un code d’événement et deux paramètres d’événement.</span><span class="sxs-lookup"><span data-stu-id="e1597-108">Filters alert the Filter Graph Manager by sending events, which consist of an event code and two event parameters.</span></span> <span data-ttu-id="e1597-109">Le code d’événement indique le type d’événement et les paramètres d’événement fournissent des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="e1597-109">The event code indicates the type of event, and the event parameters supply additional information.</span></span> <span data-ttu-id="e1597-110">La signification des paramètres dépend du code de l’événement.</span><span class="sxs-lookup"><span data-stu-id="e1597-110">The meaning of the parameters depends on the event code.</span></span> <span data-ttu-id="e1597-111">Pour obtenir la liste complète des codes d’événement, consultez [codes de notification d’événement](event-notification-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e1597-111">For a complete list of event codes, see [Event Notification Codes](event-notification-codes.md).</span></span>

<span data-ttu-id="e1597-112">Certains événements sont gérés en mode silencieux par le gestionnaire de graphique de filtre, sans que l’application soit notifiée.</span><span class="sxs-lookup"><span data-stu-id="e1597-112">Some events are handled silently by the Filter Graph Manager, without the application being notified.</span></span> <span data-ttu-id="e1597-113">D’autres événements sont placés dans une file d’attente pour l’application.</span><span class="sxs-lookup"><span data-stu-id="e1597-113">Other events are placed on a queue for the application.</span></span> <span data-ttu-id="e1597-114">Selon l’application, vous devrez peut-être gérer différents événements.</span><span class="sxs-lookup"><span data-stu-id="e1597-114">Depending on the application, there are various events that you might need to handle.</span></span> <span data-ttu-id="e1597-115">Cet article se concentre sur trois événements très courants :</span><span class="sxs-lookup"><span data-stu-id="e1597-115">This article focuses on three events that are very common:</span></span>

-   <span data-ttu-id="e1597-116">L’événement [**EC \_ Complete**](ec-complete.md) indique que la lecture s’est terminée normalement.</span><span class="sxs-lookup"><span data-stu-id="e1597-116">The [**EC\_COMPLETE**](ec-complete.md) event indicates that playback has completed normally.</span></span>
-   <span data-ttu-id="e1597-117">L’événement [**EC \_ USERABORT**](ec-userabort.md) indique que l’utilisateur a interrompu la lecture.</span><span class="sxs-lookup"><span data-stu-id="e1597-117">The [**EC\_USERABORT**](ec-userabort.md) event indicates that the user has interrupted playback.</span></span> <span data-ttu-id="e1597-118">Les convertisseurs vidéo envoient cet événement si l’utilisateur ferme la fenêtre vidéo.</span><span class="sxs-lookup"><span data-stu-id="e1597-118">Video renderers send this event if the user closes the video window.</span></span>
-   <span data-ttu-id="e1597-119">L’événement [**EC \_ ERRORABORT**](ec-errorabort.md) indique qu’une erreur a provoqué l’arrêt de la lecture.</span><span class="sxs-lookup"><span data-stu-id="e1597-119">The [**EC\_ERRORABORT**](ec-errorabort.md) event indicates that an error has caused playback to halt.</span></span>

## <a name="using-event-notification"></a><span data-ttu-id="e1597-120">Utilisation de la notification d’événement</span><span class="sxs-lookup"><span data-stu-id="e1597-120">Using Event Notification</span></span>

<span data-ttu-id="e1597-121">Une application peut demander au gestionnaire de graphique de filtre d’envoyer un message Windows à une fenêtre désignée à chaque fois qu’un nouvel événement se produit.</span><span class="sxs-lookup"><span data-stu-id="e1597-121">An application can instruct the Filter Graph Manager to send a Windows message to a designated window whenever a new event occurs.</span></span> <span data-ttu-id="e1597-122">Cela permet à l’application de répondre à l’intérieur de la boucle de message de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e1597-122">This enables the application to respond inside the window's message loop.</span></span> <span data-ttu-id="e1597-123">Tout d’abord, définissez le message qui sera envoyé à la fenêtre d’application.</span><span class="sxs-lookup"><span data-stu-id="e1597-123">First, define the message that will be sent to the application window.</span></span> <span data-ttu-id="e1597-124">Les applications peuvent utiliser des numéros de message dans la plage de l' \_ application WM via 0xBFFF en tant que messages privés :</span><span class="sxs-lookup"><span data-stu-id="e1597-124">Applications can use message numbers in the range from WM\_APP through 0xBFFF as private messages:</span></span>


```C++
#define WM_GRAPHNOTIFY  WM_APP + 1
```



<span data-ttu-id="e1597-125">Ensuite, interrogez le gestionnaire du graphique de filtre pour l’interface [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) et appelez la méthode [**IMediaEventEx :: SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) :</span><span class="sxs-lookup"><span data-stu-id="e1597-125">Next, query the Filter Graph Manager for the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interface and call the [**IMediaEventEx::SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) method:</span></span>


```C++
IMediaEventEx *g_pEvent = NULL;
g_pGraph->QueryInterface(IID_IMediaEventEx, (void **)&g_pEvent);
g_pEvent->SetNotifyWindow((OAHWND)g_hwnd, WM_GRAPHNOTIFY, 0);
```



<span data-ttu-id="e1597-126">Cette méthode désigne la fenêtre spécifiée (g \_ HWND) comme destinataire du message.</span><span class="sxs-lookup"><span data-stu-id="e1597-126">This method designates the specified window (g\_hwnd) as the recipient of the message.</span></span> <span data-ttu-id="e1597-127">Appelez la méthode après avoir créé le graphique de filtre, mais avant d’exécuter le graphique.</span><span class="sxs-lookup"><span data-stu-id="e1597-127">Call the method after you create the filter graph, but before running the graph.</span></span>

<span data-ttu-id="e1597-128">WM \_ GRAPHNOTIFY est un message Windows ordinaire.</span><span class="sxs-lookup"><span data-stu-id="e1597-128">WM\_GRAPHNOTIFY is an ordinary Windows message.</span></span> <span data-ttu-id="e1597-129">Chaque fois que le gestionnaire de graphique de filtre place un nouvel événement dans la file d’attente d’événements, il publie un \_ message WM GRAPHNOTIFY dans la fenêtre d’application désignée.</span><span class="sxs-lookup"><span data-stu-id="e1597-129">Whenever the Filter Graph Manager puts a new event on the event queue, it posts a WM\_GRAPHNOTIFY message to the designated application window.</span></span> <span data-ttu-id="e1597-130">Le paramètre *lParam* du message est égal au troisième paramètre dans [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow).</span><span class="sxs-lookup"><span data-stu-id="e1597-130">The message's *lParam* parameter is equal to the third parameter in [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow).</span></span> <span data-ttu-id="e1597-131">Ce paramètre vous permet d’envoyer des données d’instance avec le message.</span><span class="sxs-lookup"><span data-stu-id="e1597-131">This parameter enables you to send instance data with the message.</span></span> <span data-ttu-id="e1597-132">Le paramètre *wParam* du message de fenêtre est toujours égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="e1597-132">The window message's *wParam* parameter is always zero.</span></span>

<span data-ttu-id="e1597-133">Dans la fonction **WindowProc** de votre application, ajoutez une instruction case pour le \_ message WM GRAPHNOTIFY :</span><span class="sxs-lookup"><span data-stu-id="e1597-133">In your application's **WindowProc** function, add a case statement for the WM\_GRAPHNOTIFY message:</span></span>


```C++
case WM_GRAPHNOTIFY:
    HandleGraphEvent();
    break;
```



<span data-ttu-id="e1597-134">Dans la fonction de gestionnaire d’événements, appelez la méthode [**IMediaEvent :: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) pour récupérer les événements de la file d’attente :</span><span class="sxs-lookup"><span data-stu-id="e1597-134">In the event handler function, call the [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) method to retrieve events from the queue:</span></span>


```C++
void HandleGraphEvent()
{
    // Disregard if we don't have an IMediaEventEx pointer.
    if (g_pEvent == NULL)
    {
        return;
    }
    // Get all the events
    long evCode;
    LONG_PTR param1, param2;
    HRESULT hr;
    while (SUCCEEDED(g_pEvent->GetEvent(&evCode, &param1, &param2, 0)))
    {
        g_pEvent->FreeEventParams(evCode, param1, param2);
        switch (evCode)
        {
        case EC_COMPLETE:  // Fall through.
        case EC_USERABORT: // Fall through.
        case EC_ERRORABORT:
            CleanUp();
            PostQuitMessage(0);
            return;
        }
    } 
}
```



<span data-ttu-id="e1597-135">La méthode [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) récupère le code d’événement et les deux paramètres d’événement.</span><span class="sxs-lookup"><span data-stu-id="e1597-135">The [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) method retrieves the event code and the two event parameters.</span></span> <span data-ttu-id="e1597-136">Le quatrième paramètre **GetEvent** spécifie la durée d’attente d’un événement, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="e1597-136">The fourth **GetEvent** parameter specifies the length of time to wait for an event, in milliseconds.</span></span> <span data-ttu-id="e1597-137">Étant donné que l’application appelle cette méthode en réponse à un \_ message WM GRAPHNOTIFY, l’événement est déjà mis en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="e1597-137">Because the application calls this method in response to a WM\_GRAPHNOTIFY message, the event is already queued.</span></span> <span data-ttu-id="e1597-138">Par conséquent, nous définissons la valeur du délai d’attente sur zéro.</span><span class="sxs-lookup"><span data-stu-id="e1597-138">Therefore, we set the time-out value to zero.</span></span>

<span data-ttu-id="e1597-139">La notification d’événement et la boucle de message sont toutes deux asynchrones, donc la file d’attente peut contenir plusieurs événements au moment où votre application répond au message.</span><span class="sxs-lookup"><span data-stu-id="e1597-139">Event notification and the message loop are both asynchronous, so the queue might hold more than one event by the time your application responds to the message.</span></span> <span data-ttu-id="e1597-140">En outre, le gestionnaire de graphes de filtre peut supprimer certains événements de la file d’attente, s’ils deviennent non valides.</span><span class="sxs-lookup"><span data-stu-id="e1597-140">Also, the Filter Graph Manager can remove certain events from the queue, if they become invalid.</span></span> <span data-ttu-id="e1597-141">Par conséquent, vous devez appeler [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) jusqu’à ce qu’il retourne un code d’échec, indiquant que la file d’attente est vide.</span><span class="sxs-lookup"><span data-stu-id="e1597-141">Therefore, you should call [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) until it returns a failure code, indicating the queue is empty.</span></span>

<span data-ttu-id="e1597-142">Dans cet exemple, l’application répond à la valeur [**EC \_ Complete**](ec-complete.md), [**EC \_ USERABORT**](ec-userabort.md)et [**EC \_ ERRORABORT**](ec-errorabort.md) en appelant la fonction de nettoyage définie par l’application, ce qui entraîne la fermeture normale de l’application.</span><span class="sxs-lookup"><span data-stu-id="e1597-142">In this example, the application responds to [**EC\_COMPLETE**](ec-complete.md), [**EC\_USERABORT**](ec-userabort.md), and [**EC\_ERRORABORT**](ec-errorabort.md) by invoking the application-defined CleanUp function, which causes the application to quit gracefully.</span></span> <span data-ttu-id="e1597-143">L’exemple ignore les deux paramètres d’événement.</span><span class="sxs-lookup"><span data-stu-id="e1597-143">The example ignores the two event parameters.</span></span> <span data-ttu-id="e1597-144">Après avoir récupéré un événement, appelez [**IMediaEvent :: FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) pour accéder à toutes les ressources gratuites associées aux paramètres de l’événement.</span><span class="sxs-lookup"><span data-stu-id="e1597-144">After you retrieve an event, call [**IMediaEvent::FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) to any free resources associated with the event parameters.</span></span>

<span data-ttu-id="e1597-145">Notez qu’un événement [**EC \_ Complete**](ec-complete.md) ne provoque pas l’arrêt du graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="e1597-145">Note that an [**EC\_COMPLETE**](ec-complete.md) event does not cause the filter graph to stop.</span></span> <span data-ttu-id="e1597-146">L’application peut arrêter ou suspendre le graphique.</span><span class="sxs-lookup"><span data-stu-id="e1597-146">The application can either stop or pause the graph.</span></span> <span data-ttu-id="e1597-147">Si vous arrêtez le graphique, les filtres libèrent toutes les ressources qu’ils détiennent.</span><span class="sxs-lookup"><span data-stu-id="e1597-147">If you stop the graph, filters release any resources they are holding.</span></span> <span data-ttu-id="e1597-148">Si vous suspendez le graphique, les filtres continuent à contenir des ressources.</span><span class="sxs-lookup"><span data-stu-id="e1597-148">If you pause the graph, filters continue to hold resources.</span></span> <span data-ttu-id="e1597-149">En outre, lorsqu’un convertisseur vidéo est suspendu, il affiche une image statique du frame le plus récent.</span><span class="sxs-lookup"><span data-stu-id="e1597-149">Also, when a video renderer pauses, it displays a static image of the most recent frame.</span></span>

<span data-ttu-id="e1597-150">Avant de libérer le pointeur [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) , annulez la notification d’événement en appelant [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) avec un handle de fenêtre **null** :</span><span class="sxs-lookup"><span data-stu-id="e1597-150">Before you release the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) pointer, cancel event notification by calling [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) with a **NULL** window handle:</span></span>


```C++
// Disable event notification before releasing the graph.
g_pEvent->SetNotifyWindow(NULL, 0, 0);
g_pEvent->Release();
g_pEvent = NULL;
```



<span data-ttu-id="e1597-151">Dans le \_ Gestionnaire de messages WM GRAPHNOTIFY, vérifiez le pointeur [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) avant d’appeler [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent):</span><span class="sxs-lookup"><span data-stu-id="e1597-151">In the WM\_GRAPHNOTIFY message handler, check the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) pointer before calling [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent):</span></span>


```C++
if (g_pEvent == NULL) return;
```



<span data-ttu-id="e1597-152">Cela empêche une erreur possible qui peut se produire si l’application reçoit la notification d’événement après avoir relâché le pointeur.</span><span class="sxs-lookup"><span data-stu-id="e1597-152">This prevents a possible error that can occur if the application receives the event notification after releasing the pointer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1597-153">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e1597-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1597-154">Tâches de base de DirectShow</span><span class="sxs-lookup"><span data-stu-id="e1597-154">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> <dt>

[<span data-ttu-id="e1597-155">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="e1597-155">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 



