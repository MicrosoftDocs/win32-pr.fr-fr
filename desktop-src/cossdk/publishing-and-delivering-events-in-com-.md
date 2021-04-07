---
description: Pour publier un événement, il vous suffit d’instancier un objet de classe d’événements et d’appeler la méthode souhaitée. pour obtenir des instructions détaillées sur la façon de procéder dans le code, consultez publication d’un événement.
ms.assetid: 835c3753-fdcc-4afe-94c3-c954aaf1c832
title: Publication et diffusion d’événements dans COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47a444b64501156191590c115d6000f4c0bda153
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748853"
---
# <a name="publishing-and-delivering-events-in-com"></a><span data-ttu-id="fe669-103">Publication et diffusion d’événements dans COM+</span><span class="sxs-lookup"><span data-stu-id="fe669-103">Publishing and Delivering Events in COM+</span></span>

<span data-ttu-id="fe669-104">Pour publier un événement, il vous suffit d’instancier un objet de [classe d’événements](the-com--event-class-object.md) et d’appeler la méthode souhaitée. pour obtenir des instructions détaillées sur la façon de procéder dans le code, consultez [publication d’un événement](publishing-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="fe669-104">To publish an event, simply instantiate an [event class](the-com--event-class-object.md) object and invoke the desired method; for detailed instructions on how to do this in code, see [Publishing an Event](publishing-an-event.md).</span></span>

<span data-ttu-id="fe669-105">Lorsqu’un serveur de publication déclenche un événement, le service d’événements COM+ recherche la base de données d’abonnement pour trouver tous les abonnés qui ont inscrit des abonnements à la classe d’événements instanciée.</span><span class="sxs-lookup"><span data-stu-id="fe669-105">When a publisher fires an event, the COM+ Events service searches the subscription database to find all the subscribers who have registered subscriptions to the instantiated event class.</span></span> <span data-ttu-id="fe669-106">Il se connecte à ces abonnés (par la création directe, les monikers ou les composants mis en file d’attente) et appelle la méthode.</span><span class="sxs-lookup"><span data-stu-id="fe669-106">It connects to those subscribers (by direct creation, monikers, or queued components) and calls the method.</span></span> <span data-ttu-id="fe669-107">Pour prendre en charge plusieurs notifications de l’abonné pour un événement, les méthodes peuvent contenir uniquement des paramètres in et doivent retourner uniquement des valeurs **HRESULT** de réussite ou d’échec.</span><span class="sxs-lookup"><span data-stu-id="fe669-107">To support more than one subscriber notification for an event, methods can contain only in parameters and must return only success or failure **HRESULT** values.</span></span>

> [!Note]  
> <span data-ttu-id="fe669-108">Cette version des événements COM+ ne prend pas en charge un magasin d’événements distribué.</span><span class="sxs-lookup"><span data-stu-id="fe669-108">This version of COM+ events does not support a distributed event store.</span></span> <span data-ttu-id="fe669-109">Un abonné doit s’abonner à un événement sur chaque ordinateur à partir duquel il souhaite recevoir une notification.</span><span class="sxs-lookup"><span data-stu-id="fe669-109">A subscriber must subscribe to an event on each computer from which it wants to receive notification.</span></span> <span data-ttu-id="fe669-110">Vous pouvez également enregistrer l’objet de classe d’événements et les abonnements sur un ordinateur central et instancier cet objet de classe d’événements à partir des ordinateurs distants sur lesquels vous publiez des événements.</span><span class="sxs-lookup"><span data-stu-id="fe669-110">As an alternative, you can register the event class object and subscriptions on a central computer and instantiate this event class object from the remote computers on which you publish events.</span></span> <span data-ttu-id="fe669-111">La remise des événements est fournie par DCOM ou par le service de composants en file d’attente COM+.</span><span class="sxs-lookup"><span data-stu-id="fe669-111">Delivery of events is provided either by DCOM or by the COM+ queued components service.</span></span> <span data-ttu-id="fe669-112">Pour plus d’informations sur l’utilisation du service COM+ Queued Components, consultez [utilisation d’événements com+ avec des composants en file d’attente com+](using-com--events-with-com--queued-components.md).</span><span class="sxs-lookup"><span data-stu-id="fe669-112">For more information about using the COM+ queued components service, see [Using COM+ Events with COM+ Queued Components](using-com--events-with-com--queued-components.md).</span></span>

 

<span data-ttu-id="fe669-113">Par défaut, le service événements COM+ déclenche un événement à la fois, sans ordre déterminé ou reproductible.</span><span class="sxs-lookup"><span data-stu-id="fe669-113">By default, the COM+ events service fires events one at a time, in no determined or repeatable order.</span></span> <span data-ttu-id="fe669-114">Les serveurs de publication qui ont besoin de contrôler l’ordre dans lequel les abonnés reçoivent un événement peuvent implémenter un filtre de l’éditeur.</span><span class="sxs-lookup"><span data-stu-id="fe669-114">Publishers that need to control the order in which subscribers receive an event can implement a publisher filter.</span></span> <span data-ttu-id="fe669-115">(Pour plus d’informations, consultez [filtrage des événements dans com+](filtering-events-in-com-.md).)</span><span class="sxs-lookup"><span data-stu-id="fe669-115">(For more information, see [Filtering Events in COM+](filtering-events-in-com-.md).)</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe669-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fe669-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe669-117">Filtrage des événements dans COM+</span><span class="sxs-lookup"><span data-stu-id="fe669-117">Filtering Events in COM+</span></span>](filtering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="fe669-118">Abonnements</span><span class="sxs-lookup"><span data-stu-id="fe669-118">Subscriptions</span></span>](subscriptions.md)
</dt> <dt>

[<span data-ttu-id="fe669-119">Objet de classe d’événements COM+</span><span class="sxs-lookup"><span data-stu-id="fe669-119">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
</dt> <dt>

[<span data-ttu-id="fe669-120">Utilisation d’événements COM+ avec des composants en file d’attente COM+</span><span class="sxs-lookup"><span data-stu-id="fe669-120">Using COM+ Events with COM+ Queued Components</span></span>](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 



