---
description: Les événements sont un élément essentiel de la gestion des appels sous TAPI 3. La gestion des événements comprend quatre étapes.
ms.assetid: db43f4e0-f2f5-49b1-a03d-3df3de0e5611
title: Événements (API de téléphonie)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a9a7d994c7bc9f8019224d826d586d698bc605
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529073"
---
# <a name="events-telephony-api"></a><span data-ttu-id="33125-104">Événements (API de téléphonie)</span><span class="sxs-lookup"><span data-stu-id="33125-104">Events (Telephony API)</span></span>

<span data-ttu-id="33125-105">Les événements sont un élément essentiel de la gestion des appels sous TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="33125-105">Events are a crucial part of call handling under TAPI 3.</span></span> <span data-ttu-id="33125-106">La gestion des événements comprend quatre étapes.</span><span class="sxs-lookup"><span data-stu-id="33125-106">Event handling includes four stages.</span></span>

<span data-ttu-id="33125-107">**Pour s’inscrire et activer la réception d’événements**</span><span class="sxs-lookup"><span data-stu-id="33125-107">**To register for and enable the reception of events**</span></span>

1.  <span data-ttu-id="33125-108">Implémentez la méthode [**ITTAPIEventNotification :: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) .</span><span class="sxs-lookup"><span data-stu-id="33125-108">Implement the [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) method.</span></span> <span data-ttu-id="33125-109">(L’interface TAPI appelle cette méthode lorsqu’un événement se produit.) En règle générale, cette implémentation ne fait pas plus que **AddRef** du pointeur d’interface **IDispatch** , puis publie sur la pompe de messages de l’application.</span><span class="sxs-lookup"><span data-stu-id="33125-109">(TAPI calls this method when an event occurs.) Typically, this implementation does no more than **AddRef** the **IDispatch** interface pointer, then post to the application's message pump.</span></span>
2.  <span data-ttu-id="33125-110">Inscrivez l’interface sortante [**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) à l’aide des interfaces COM [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) et [**IConnectionPoint**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint) , et transmettez à la méthode [**IConnectionPoint :: Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) un pointeur vers [**ITTAPIEventNotification :: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event).</span><span class="sxs-lookup"><span data-stu-id="33125-110">Register the [**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) outgoing interface using the COM standard [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) and [**IConnectionPoint**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint) interfaces, and pass the [**IConnectionPoint::Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) method a pointer to [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event).</span></span>
3.  <span data-ttu-id="33125-111">Appelez la méthode [**ITTAPI ::p ut \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) pour indiquer à l’interface TAPI les événements que l’application doit gérer.</span><span class="sxs-lookup"><span data-stu-id="33125-111">Call the [**ITTAPI::put\_EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) method to tell TAPI which events the application will handle.</span></span> <span data-ttu-id="33125-112">Le filtre d’événements se compose des membres **ou** Ed de l’énumération des [**\_ événements TAPI**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) .</span><span class="sxs-lookup"><span data-stu-id="33125-112">The event filter consists of **OR** ed members of the [**TAPI\_EVENT**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) enumeration.</span></span>
    > [!Note]  
    > <span data-ttu-id="33125-113">Vous devez appeler la méthode **ITTAPI ::p ut \_ EventFilter** pour définir le masque de filtre d’événement et activer la réception des événements.</span><span class="sxs-lookup"><span data-stu-id="33125-113">You must call the **ITTAPI::put\_EventFilter** method to set the event filter mask and enable reception of events.</span></span> <span data-ttu-id="33125-114">Si vous n’appelez pas **ITTAPI ::p ut \_ EventFilter**, votre application ne recevra aucun événement.</span><span class="sxs-lookup"><span data-stu-id="33125-114">If you do not call **ITTAPI::put\_EventFilter**, your application will not receive any events.</span></span>

     

<span data-ttu-id="33125-115">Vous devez également appeler la méthode [**ITTAPI :: RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) pour chaque objet d’adresse sur lequel l’application doit gérer les appels.</span><span class="sxs-lookup"><span data-stu-id="33125-115">You must also call the [**ITTAPI::RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) method for each address object on which the application will handle calls.</span></span>

<span data-ttu-id="33125-116">Pour obtenir la liste de toutes les interfaces d’événements, consultez [interfaces](./event-interfaces.md) d’événements.</span><span class="sxs-lookup"><span data-stu-id="33125-116">See [Event Interfaces](./event-interfaces.md) for a list of all event interfaces.</span></span> <span data-ttu-id="33125-117">Consultez [inscrire des événements](register-events.md) pour obtenir des exemples de code qui illustrent le processus d’inscription et [reçoivent un appel](receive-a-call.md) pour obtenir un exemple de code qui illustre une utilisation d’événements.</span><span class="sxs-lookup"><span data-stu-id="33125-117">See [Register Events](register-events.md) for code examples that illustrate the registration process and [Receive a Call](receive-a-call.md) for a code example that shows one use of events.</span></span>

 

 
