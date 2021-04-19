---
description: Le service événements COM+ est utilisé pour gérer la remise des événements des serveurs de publication aux abonnés.
ms.assetid: 0945163b-1276-47f6-ae7f-9d932a1b586d
title: Utilisation d’événements COM+ avec des composants en file d’attente COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be31dd1088b720902295738c23173c28145cef2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515173"
---
# <a name="using-com-events-with-com-queued-components"></a><span data-ttu-id="a08a3-103">Utilisation d’événements COM+ avec des composants en file d’attente COM+</span><span class="sxs-lookup"><span data-stu-id="a08a3-103">Using COM+ Events with COM+ Queued Components</span></span>

<span data-ttu-id="a08a3-104">Le service événements COM+ est utilisé pour gérer la remise des événements des serveurs de publication aux abonnés.</span><span class="sxs-lookup"><span data-stu-id="a08a3-104">The COM+ events service is used to manage the delivery of events from publishers to subscribers.</span></span> <span data-ttu-id="a08a3-105">Le service composants en file d’attente COM+ peut être utilisé pour rendre le serveur de publication et le temps de traitement de l’abonné indépendant en mettant en file d’attente le message de l’éditeur et en le relisant ultérieurement sur l’abonné.</span><span class="sxs-lookup"><span data-stu-id="a08a3-105">The COM+ queued components service can be used to make the publisher and subscriber processing time independent by queuing the publisher's message and later replaying it to the subscriber.</span></span> <span data-ttu-id="a08a3-106">La nécessité ou non d’utiliser le service Queued Components dépend de la logique métier sous-jacente de votre application.</span><span class="sxs-lookup"><span data-stu-id="a08a3-106">Whether or not you need to use the queued components service depends on the underlying business logic of your application.</span></span> <span data-ttu-id="a08a3-107">Si vous avez besoin d’événements qui sont indépendants de l’heure, vous pouvez les créer à l’aide du service événements COM+ avec les composants en file d’attente COM+.</span><span class="sxs-lookup"><span data-stu-id="a08a3-107">If you need to have events that are time independent, you can create them by using the COM+ events service with COM+ queued components service.</span></span>

> [!Note]  
> <span data-ttu-id="a08a3-108">Pour plus d’informations sur l’utilisation du service COM+ Queued Components, consultez [composants en file d’attente com+](com--queued-components.md).</span><span class="sxs-lookup"><span data-stu-id="a08a3-108">For additional information about using the COM+ queued components service, see [COM+ Queued Components](com--queued-components.md).</span></span>

 

<span data-ttu-id="a08a3-109">Le service Queued Components gère l’appel de méthode de méthode dans un message unique.</span><span class="sxs-lookup"><span data-stu-id="a08a3-109">The queued components service maintains order-of-method invocation within a single message.</span></span> <span data-ttu-id="a08a3-110">L’enregistreur effectue un traitement par lots de tous les appels de méthode dans un message, puis le lecteur appelle ces méthodes dans l’ordre où le message est traité.</span><span class="sxs-lookup"><span data-stu-id="a08a3-110">The recorder batches all method invocations into a message, and then the player invokes those methods in order when the message is processed.</span></span>

<span data-ttu-id="a08a3-111">Un enregistreur et un lecteur de composants en file d’attente peuvent être positionnés dans l’un des deux emplacements suivants :</span><span class="sxs-lookup"><span data-stu-id="a08a3-111">A queued components recorder and player can be positioned in either of the following two places:</span></span>

-   <span data-ttu-id="a08a3-112">Entre le serveur de publication et l’objet d’événement</span><span class="sxs-lookup"><span data-stu-id="a08a3-112">Between the publisher and event object</span></span>
-   <span data-ttu-id="a08a3-113">Entre l’objet d’événement et l’abonné</span><span class="sxs-lookup"><span data-stu-id="a08a3-113">Between the event object and subscriber</span></span>

<span data-ttu-id="a08a3-114">Si vous placez l’enregistreur et le lecteur entre le serveur de publication et l’objet d’événement, vous rendez la [classe d’événements](the-com--event-class-object.md) en tant que composant.</span><span class="sxs-lookup"><span data-stu-id="a08a3-114">If you position the recorder and player between the publisher and event object, you are making the [event class](the-com--event-class-object.md) component queuable.</span></span> <span data-ttu-id="a08a3-115">Le composant de la classe d’événements doit être marqué pour la mise en file d’attente et être activé par le joueur dans un processus distinct du serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="a08a3-115">The event class component must be marked for queuing and be activated by the player in a process that is separate from the publisher.</span></span>

<span data-ttu-id="a08a3-116">Pour remettre des événements de manière asynchrone, composez l’enregistreur et le lecteur entre l’objet d’événement et l’abonné, puis définissez l’attribut de mise en file d’attente de l’objet d’abonnement.</span><span class="sxs-lookup"><span data-stu-id="a08a3-116">To deliver events asynchronously, compose the recorder and player between the event object and subscriber and set the Queued attribute of the subscription object.</span></span> <span data-ttu-id="a08a3-117">Cela définit SubscriberMoniker comme suit : « queue:/New:/ {12345678-1234-1234-1234-123456789012} ».</span><span class="sxs-lookup"><span data-stu-id="a08a3-117">This sets SubscriberMoniker as follows: "queue:/new:/{12345678-1234-1234-1234-123456789012}".</span></span>

<span data-ttu-id="a08a3-118">Il y a un ordre de implication de livraison à prendre en compte lors de l’utilisation de composants en file d’attente dans une situation d’événement.</span><span class="sxs-lookup"><span data-stu-id="a08a3-118">There is an order of delivery implication to consider when using queued components in an event situation.</span></span> <span data-ttu-id="a08a3-119">Étant donné que les composants en file d’attente de service enregistrent et lisent tous les appels au cours de la durée de vie d’un objet unique dans un message, tous les appels sont relus dans l’ordre dans lequel ils ont été créés.</span><span class="sxs-lookup"><span data-stu-id="a08a3-119">Because the queued components service records and plays back all calls within the lifetime of a single object in one message, all calls are replayed in the order in which they were made.</span></span> <span data-ttu-id="a08a3-120">Toutefois, s’il existe plusieurs sessions avec plusieurs objets, l’ordre ne peut pas être garanti.</span><span class="sxs-lookup"><span data-stu-id="a08a3-120">However, if there is more than one session with more than one object, order cannot be guaranteed.</span></span> <span data-ttu-id="a08a3-121">Si l’ordre est important, assurez-vous que les appels qui doivent être lus dans l’ordre résident sur la même instance d’objet.</span><span class="sxs-lookup"><span data-stu-id="a08a3-121">If order is important, make sure that calls that need to be played back in order reside on the same object instance.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a08a3-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a08a3-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a08a3-123">Filtrage des événements dans COM+</span><span class="sxs-lookup"><span data-stu-id="a08a3-123">Filtering Events in COM+</span></span>](filtering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="a08a3-124">Publication et diffusion d’événements dans COM+</span><span class="sxs-lookup"><span data-stu-id="a08a3-124">Publishing and Delivering Events in COM+</span></span>](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="a08a3-125">Abonnements</span><span class="sxs-lookup"><span data-stu-id="a08a3-125">Subscriptions</span></span>](subscriptions.md)
</dt> <dt>

[<span data-ttu-id="a08a3-126">Objet de classe d’événements COM+</span><span class="sxs-lookup"><span data-stu-id="a08a3-126">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
</dt> </dl>

 

 



