---
description: Récupération des événements
ms.assetid: 18c5892d-7e33-497c-ab7d-d17fea5df17e
title: Récupération des événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78d23cf4f8060c15db564e718ba3a2fa4a660022
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385504"
---
# <a name="retrieving-events"></a><span data-ttu-id="81265-103">Récupération des événements</span><span class="sxs-lookup"><span data-stu-id="81265-103">Retrieving Events</span></span>

<span data-ttu-id="81265-104">Le gestionnaire de graphique de filtre expose trois interfaces qui prennent en charge la notification d’événements.</span><span class="sxs-lookup"><span data-stu-id="81265-104">The Filter Graph Manager exposes three interfaces that support event notification.</span></span>

-   <span data-ttu-id="81265-105">[**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) contient la méthode pour les filtres pour la publication des événements.</span><span class="sxs-lookup"><span data-stu-id="81265-105">[**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) contains the method for filters to post events.</span></span>
-   <span data-ttu-id="81265-106">[**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) contient des méthodes permettant aux applications de récupérer des événements.</span><span class="sxs-lookup"><span data-stu-id="81265-106">[**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) contains methods for applications to retrieve events.</span></span>
-   <span data-ttu-id="81265-107">[**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) hérite de et étend l’interface [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) .</span><span class="sxs-lookup"><span data-stu-id="81265-107">[**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) inherits from and extends the [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) interface.</span></span>

<span data-ttu-id="81265-108">Les filtres publient les notifications d’événements en appelant la méthode [**IMediaEventSink :: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) sur le gestionnaire de graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="81265-108">Filters post event notifications by calling the [**IMediaEventSink::Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) method on the Filter Graph Manager.</span></span> <span data-ttu-id="81265-109">Une notification d’événement se compose d’un code d’événement qui définit le type d’événement, et de deux paramètres qui fournissent des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="81265-109">An event notification consists of an event code, which defines the type of event, and two parameters that give additional information.</span></span> <span data-ttu-id="81265-110">En fonction du code d’événement, les paramètres peuvent contenir des pointeurs, des codes de retour, des temps de référence ou d’autres informations.</span><span class="sxs-lookup"><span data-stu-id="81265-110">Depending on the event code, the parameters might contain pointers, return codes, reference times, or other information.</span></span> <span data-ttu-id="81265-111">Pour obtenir la liste complète des codes et paramètres d’événement, consultez [codes de notification d’événement](event-notification-codes.md).</span><span class="sxs-lookup"><span data-stu-id="81265-111">For a complete list of event codes and parameters, see [Event Notification Codes](event-notification-codes.md).</span></span>

<span data-ttu-id="81265-112">Pour récupérer un événement à partir de la file d’attente, l’application appelle la méthode [**IMediaEvent :: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) sur le gestionnaire de graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="81265-112">To retrieve an event from the queue, the application calls the [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) method on the Filter Graph Manager.</span></span> <span data-ttu-id="81265-113">Cette méthode bloque jusqu’à ce qu’il y ait un événement à retourner ou jusqu’à ce qu’un délai spécifié se soit écoulé.</span><span class="sxs-lookup"><span data-stu-id="81265-113">This method blocks until there is an event to return or until a specified time elapses.</span></span> <span data-ttu-id="81265-114">En supposant qu’il existe un événement de mise en file d’attente, la méthode retourne avec le code d’événement et les deux paramètres d’événement.</span><span class="sxs-lookup"><span data-stu-id="81265-114">Assuming there is a queued event, the method returns with the event code and the two event parameters.</span></span> <span data-ttu-id="81265-115">Après l’appel de **GetEvent**, une application doit toujours appeler la méthode [**IMediaEvent :: FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) pour libérer toutes les ressources associées aux paramètres de l’événement.</span><span class="sxs-lookup"><span data-stu-id="81265-115">After calling **GetEvent**, an application should always call the [**IMediaEvent::FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) method to release any resources associated with the event parameters.</span></span> <span data-ttu-id="81265-116">Par exemple, un paramètre peut être une valeur **BSTR** qui a été allouée par le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="81265-116">For example, a parameter might be a **BSTR** value that was allocated by the filter graph.</span></span>

<span data-ttu-id="81265-117">L’exemple de code suivant montre comment récupérer des événements de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="81265-117">The following code example provides an outline of how to retrieve events from the queue.</span></span>


```C++
long evCode;
LONG_PTR param1, param2;
HRESULT hr;
while (hr = pEvent->GetEvent(&evCode, &param1, &param2, 0), SUCCEEDED(hr))
{
    switch(evCode) 
    { 
        // Call application-defined functions for each 
        // type of event that you want to handle.
    } 
    hr = pEvent->FreeEventParams(evCode, param1, param2);
}
```



<span data-ttu-id="81265-118">Pour remplacer la gestion par défaut du gestionnaire de graphique de filtre pour un événement, appelez la méthode [**IMediaEvent :: CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) avec le code d’événement en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="81265-118">To override the Filter Graph Manager's default handling for an event, call the [**IMediaEvent::CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) method with the event code as a parameter.</span></span> <span data-ttu-id="81265-119">Vous pouvez rétablir la gestion par défaut en appelant la méthode [**IMediaEvent :: RestoreDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-restoredefaulthandling) .</span><span class="sxs-lookup"><span data-stu-id="81265-119">You can reinstate the default handling by calling the [**IMediaEvent::RestoreDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-restoredefaulthandling) method.</span></span> <span data-ttu-id="81265-120">Si le graphique de filtre n’effectue aucune gestion par défaut pour le code d’événement spécifié, l’appel de ces méthodes n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="81265-120">If the filter graph performs no default handling for the specified event code, calling these methods has no effect.</span></span>

## <a name="related-topics"></a><span data-ttu-id="81265-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="81265-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81265-122">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="81265-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 



