---
description: Apprentissage du moment où un événement se produit
ms.assetid: 4e44089b-676b-4220-9721-54ddf56bf760
title: Apprentissage du moment où un événement se produit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19ed537430fd66818687b142f059399292c923e1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522068"
---
# <a name="learning-when-an-event-occurs"></a><span data-ttu-id="f89f4-103">Apprentissage du moment où un événement se produit</span><span class="sxs-lookup"><span data-stu-id="f89f4-103">Learning When an Event Occurs</span></span>

<span data-ttu-id="f89f4-104">Pour traiter les événements DirectShow, une application a besoin d’un moyen de savoir quand les événements sont en attente dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="f89f4-104">To process DirectShow events, an application needs a way to find out when events are waiting in the queue.</span></span> <span data-ttu-id="f89f4-105">Le gestionnaire de graphes de filtre propose deux méthodes pour effectuer cette opération :</span><span class="sxs-lookup"><span data-stu-id="f89f4-105">The Filter Graph Manager provides two ways to do this:</span></span>

-   <span data-ttu-id="f89f4-106">**Notification de fenêtre :** Le gestionnaire de graphes de filtres envoie un message Windows défini par l’utilisateur à une fenêtre d’application à chaque fois qu’il y a un nouvel événement.</span><span class="sxs-lookup"><span data-stu-id="f89f4-106">**Window notification:** The Filter Graph Manager sends a user-defined Windows message to an application window whenever there is a new event.</span></span>
-   <span data-ttu-id="f89f4-107">**Signalement des événements :** Le gestionnaire de graphique de filtre signale un événement Windows s’il y a des événements DirectShow dans la file d’attente et réinitialise l’événement si la file d’attente est vide.</span><span class="sxs-lookup"><span data-stu-id="f89f4-107">**Event signaling:** The Filter Graph Manager signals a Windows event if there are DirectShow events in the queue, and reset the event if the queue is empty.</span></span>

<span data-ttu-id="f89f4-108">Une application peut utiliser l’une ou l’autre technique.</span><span class="sxs-lookup"><span data-stu-id="f89f4-108">An application can use either technique.</span></span> <span data-ttu-id="f89f4-109">La notification de fenêtre est généralement plus simple.</span><span class="sxs-lookup"><span data-stu-id="f89f4-109">Window notification is usually simpler.</span></span>

<span data-ttu-id="f89f4-110">**Notification de fenêtre**</span><span class="sxs-lookup"><span data-stu-id="f89f4-110">**Window Notification**</span></span>

<span data-ttu-id="f89f4-111">Pour configurer la notification de fenêtre, appelez la méthode [**IMediaEventEx :: SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) et spécifiez un message privé.</span><span class="sxs-lookup"><span data-stu-id="f89f4-111">To set up window notification, call the [**IMediaEventEx::SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) method and specify a private message.</span></span> <span data-ttu-id="f89f4-112">Les applications peuvent utiliser des numéros de message dans la plage de l' \_ application WM via 0xBFFF en tant que messages privés.</span><span class="sxs-lookup"><span data-stu-id="f89f4-112">Applications can use message numbers in the range from WM\_APP through 0xBFFF as private messages.</span></span> <span data-ttu-id="f89f4-113">Chaque fois que le gestionnaire de graphique de filtre place une nouvelle notification d’événement dans la file d’attente, il publie ce message dans la fenêtre désignée.</span><span class="sxs-lookup"><span data-stu-id="f89f4-113">Whenever the Filter Graph Manager places a new event notification in the queue, it posts this message to the designated window.</span></span> <span data-ttu-id="f89f4-114">L’application répond au message dans la boucle de messages de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f89f4-114">The application responds to the message from within the window's message loop.</span></span>

<span data-ttu-id="f89f4-115">L’exemple de code suivant montre comment définir la fenêtre de notification.</span><span class="sxs-lookup"><span data-stu-id="f89f4-115">The following code example shows how to set the notification window.</span></span>


```C++
#define WM_GRAPHNOTIFY WM_APP + 1   // Private message.
pEvent->SetNotifyWindow((OAHWND)g_hwnd, WM_GRAPHNOTIFY, 0);
```



<span data-ttu-id="f89f4-116">Le message est un message Windows ordinaire et est publié séparément de la file d’attente des notifications d’événements DirectShow.</span><span class="sxs-lookup"><span data-stu-id="f89f4-116">The message is an ordinary Windows message, and is posted separately from the DirectShow event notification queue.</span></span> <span data-ttu-id="f89f4-117">L’avantage de cette approche est que la plupart des applications implémentent déjà une boucle de message.</span><span class="sxs-lookup"><span data-stu-id="f89f4-117">The advantage of this approach is that most applications already implement a message loop.</span></span> <span data-ttu-id="f89f4-118">Par conséquent, vous pouvez incorporer la gestion des événements DirectShow sans aucun travail supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="f89f4-118">Therefore, you can incorporate DirectShow event handling without much additional work.</span></span>

<span data-ttu-id="f89f4-119">L’exemple de code suivant montre comment répondre au message de notification.</span><span class="sxs-lookup"><span data-stu-id="f89f4-119">The following code example shows an outline of how to respond to the notification message.</span></span> <span data-ttu-id="f89f4-120">Pour obtenir un exemple complet, consultez [réponse aux événements](responding-to-events.md).</span><span class="sxs-lookup"><span data-stu-id="f89f4-120">For a complete example, see [Responding to Events](responding-to-events.md).</span></span>


```C++
LRESULT CALLBACK WindowProc( HWND hwnd, UINT msg, UINT wParam, LONG lParam)
{
    switch (msg)
    {
        case WM_GRAPHNOTIFY:
            HandleEvent();  // Application-defined function.
            break;
        // Handle other Windows messages here too.
    }
    return (DefWindowProc(hwnd, msg, wParam, lParam));
}
```



<span data-ttu-id="f89f4-121">Étant donné que la notification d’événements et la boucle de message sont toutes deux asynchrones, la file d’attente peut contenir plusieurs événements au moment où votre application répond au message.</span><span class="sxs-lookup"><span data-stu-id="f89f4-121">Because event notification and the message loop are both asynchronous, the queue might contain more than one event by the time your application responds to the message.</span></span> <span data-ttu-id="f89f4-122">En outre, les événements peuvent parfois être effacés de la file d’attente s’ils deviennent non valides.</span><span class="sxs-lookup"><span data-stu-id="f89f4-122">Also, events can sometimes be cleared from the queue if they become invalid.</span></span> <span data-ttu-id="f89f4-123">Par conséquent, dans votre code de gestion des événements, appelez [**IAMMediaEvent :: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) jusqu’à ce qu’il retourne un code d’échec, ce qui indique que la file d’attente est vide.</span><span class="sxs-lookup"><span data-stu-id="f89f4-123">Therefore, in your event handling code, call [**IAMMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) until it returns a failure code, indicating that the queue is empty.</span></span>

<span data-ttu-id="f89f4-124">Avant de libérer le pointeur [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) , annulez la notification d’événement en appelant [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) avec un pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="f89f4-124">Before you release the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) pointer, cancel event notification by calling [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) with a **NULL** pointer.</span></span> <span data-ttu-id="f89f4-125">Dans votre code de traitement des événements, vérifiez si votre pointeur **IMediaEventEx** est valide avant d’appeler [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent).</span><span class="sxs-lookup"><span data-stu-id="f89f4-125">In your event processing code, check whether your **IMediaEventEx** pointer is valid before calling [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent).</span></span> <span data-ttu-id="f89f4-126">Ces étapes empêchent une erreur possible, dans laquelle l’application reçoit la notification d’événement après la libération du pointeur **IMediaEventEx** .</span><span class="sxs-lookup"><span data-stu-id="f89f4-126">These steps prevent a possible error, in which the application receives the event notification after it has released the **IMediaEventEx** pointer.</span></span>

<span data-ttu-id="f89f4-127">**Signalisation d’événements**</span><span class="sxs-lookup"><span data-stu-id="f89f4-127">**Event Signaling**</span></span>

<span data-ttu-id="f89f4-128">Le gestionnaire de graphes de filtre conserve un événement de réinitialisation manuelle qui reflète l’état de la file d’attente d’événements.</span><span class="sxs-lookup"><span data-stu-id="f89f4-128">The Filter Graph Manager keeps a manual-reset event that reflects the state of the event queue.</span></span> <span data-ttu-id="f89f4-129">Si la file d’attente contient des notifications d’événements en attente, le gestionnaire du graphique de filtres signale l’événement de réinitialisation manuelle.</span><span class="sxs-lookup"><span data-stu-id="f89f4-129">If the queue contains pending event notifications, the Filter Graph Manager signals the manual-reset event.</span></span> <span data-ttu-id="f89f4-130">Si la file d’attente est vide, un appel à la méthode [**IMediaEvent :: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) réinitialise l’événement.</span><span class="sxs-lookup"><span data-stu-id="f89f4-130">If the queue is empty, a call to the [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) method resets the event.</span></span> <span data-ttu-id="f89f4-131">Une application peut utiliser cet événement pour déterminer l’état de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="f89f4-131">An application can use this event to determine the state of the queue.</span></span>

> [!Note]  
> <span data-ttu-id="f89f4-132">La terminologie peut prêter à confusion ici.</span><span class="sxs-lookup"><span data-stu-id="f89f4-132">The terminology can be confusing here.</span></span> <span data-ttu-id="f89f4-133">L’événement de réinitialisation manuelle est le type d’événement créé par la fonction [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) de Windows ; Il n’a rien à faire avec les événements définis par DirectShow.</span><span class="sxs-lookup"><span data-stu-id="f89f4-133">The manual-reset event is the type of event created by the Windows [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) function; it has nothing to do with the events defined by DirectShow.</span></span>

 

<span data-ttu-id="f89f4-134">Appelez la méthode [**IMediaEvent :: GetEventHandle**](/windows/desktop/api/Control/nf-control-imediaevent-geteventhandle) pour obtenir un descripteur de l’événement de réinitialisation manuelle.</span><span class="sxs-lookup"><span data-stu-id="f89f4-134">Call the [**IMediaEvent::GetEventHandle**](/windows/desktop/api/Control/nf-control-imediaevent-geteventhandle) method to get a handle to the manual-reset event.</span></span> <span data-ttu-id="f89f4-135">Attendez que l’événement soit signalé en appelant une fonction telle que [**WaitForMultipleObjects**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjects).</span><span class="sxs-lookup"><span data-stu-id="f89f4-135">Wait for the event to be signaled by calling a function such as [**WaitForMultipleObjects**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjects).</span></span> <span data-ttu-id="f89f4-136">Une fois que l’événement est signalé, appelez [**IMediaEvent :: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) pour accéder à l’événement DirectShow.</span><span class="sxs-lookup"><span data-stu-id="f89f4-136">Once the event is signaled, call [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) to get the DirectShow event.</span></span>

<span data-ttu-id="f89f4-137">L'exemple de code suivant illustre cette approche.</span><span class="sxs-lookup"><span data-stu-id="f89f4-137">The following code example illustrates this approach.</span></span> <span data-ttu-id="f89f4-138">Elle obtient le handle d’événement, puis attend dans les intervalles de 100 millisecondes que l’événement soit signalé.</span><span class="sxs-lookup"><span data-stu-id="f89f4-138">It gets the event handle, then waits in 100-millisecond intervals for the event to be signaled.</span></span> <span data-ttu-id="f89f4-139">Si l’événement est signalé, il appelle **GetEvent** et imprime le code d’événement et les paramètres d’événement dans la fenêtre de console.</span><span class="sxs-lookup"><span data-stu-id="f89f4-139">If the event is signaled, it calls **GetEvent** and prints the event code and event parameters to the console window.</span></span> <span data-ttu-id="f89f4-140">La boucle se termine lorsque l’événement [**EC \_ Complete**](ec-complete.md) se produit, indiquant que la lecture est terminée.</span><span class="sxs-lookup"><span data-stu-id="f89f4-140">The loop terminates when the [**EC\_COMPLETE**](ec-complete.md) event occurs, indicating that playback has completed.</span></span>


```C++
HANDLE  hEvent; 
long    evCode, param1, param2;
BOOLEAN bDone = FALSE;
HRESULT hr = S_OK;
hr = pEvent->GetEventHandle((OAEVENT*)&hEvent);
if (FAILED(hr))
{
    /* Insert failure-handling code here. */
}

while(!bDone) 
{
    if (WAIT_OBJECT_0 == WaitForSingleObject(hEvent, 100))
    { 
        while (S_OK == pEvent->GetEvent(&evCode, &param1, &param2, 0)) 
        {
            printf("Event code: %#04x\n Params: %d, %d\n", evCode, param1, param2);
            pEvent->FreeEventParams(evCode, param1, param2);
            bDone = (EC_COMPLETE == evCode);
        }
    }
} 
```



<span data-ttu-id="f89f4-141">Étant donné que le graphique de filtre définit ou réinitialise automatiquement l’événement, le cas échéant, votre application ne doit pas le faire.</span><span class="sxs-lookup"><span data-stu-id="f89f4-141">Because the filter graph automatically sets or resets the event when appropriate, your application should not do so.</span></span> <span data-ttu-id="f89f4-142">En outre, lorsque vous relâchez le graphique de filtre, le graphique de filtre ferme le descripteur d’événement. n’utilisez donc pas le descripteur d’événement après ce point.</span><span class="sxs-lookup"><span data-stu-id="f89f4-142">Also, when you release the filter graph, the filter graph closes the event handle, so do not use the event handle after that point.</span></span>

 

 
