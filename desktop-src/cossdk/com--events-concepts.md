---
description: Concepts des événements COM+
ms.assetid: 6bfe4852-4029-4dd4-92ad-3061618b1b23
title: Concepts des événements COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811dbca17c4e90ba5e8c2bcb8c918ce6634487e5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749085"
---
# <a name="com-events-concepts"></a><span data-ttu-id="49c4e-103">Concepts des événements COM+</span><span class="sxs-lookup"><span data-stu-id="49c4e-103">COM+ Events Concepts</span></span>

<span data-ttu-id="49c4e-104">Le service d’événements COM+ est un système d’événements automatisé et *faiblement couplé* qui stocke les informations d’événements provenant de différents serveurs de publication dans le catalogue com+.</span><span class="sxs-lookup"><span data-stu-id="49c4e-104">The COM+ events service is an automated, *loosely coupled event* system that stores event information from different publishers in the COM+ catalog.</span></span> <span data-ttu-id="49c4e-105">Les abonnés peuvent interroger ce magasin d’événements et sélectionner les événements qu’ils souhaitent connaître.</span><span class="sxs-lookup"><span data-stu-id="49c4e-105">Subscribers can query this event store and select the events that they want to hear about.</span></span>

> [!Note]  
> <span data-ttu-id="49c4e-106">Un *événement* est identifié par une méthode dans une interface com+, appelée méthode d' *événement*, et provient d’un serveur de publication et distribué à l’abonné ou aux abonnés appropriés par le biais du service d’événements com+.</span><span class="sxs-lookup"><span data-stu-id="49c4e-106">An *event* is identified by a method in a COM+ interface, known as an *event method*, and is originated by a publisher and dispatched to the correct subscriber or subscribers through the COM+ events service.</span></span> <span data-ttu-id="49c4e-107">Les méthodes d’événement doivent être nommées de manière unique et ne peuvent contenir que des paramètres d’entrée (pas de paramètres de sortie ou d’entrée/sortie).</span><span class="sxs-lookup"><span data-stu-id="49c4e-107">Event methods must be uniquely named and can contain only input parameters (no output or input/output parameters).</span></span> <span data-ttu-id="49c4e-108">La valeur de retour doit être un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="49c4e-108">The return value must be an **HRESULT**.</span></span>

 

<span data-ttu-id="49c4e-109">Le service événements COM+ gère la plupart des sémantiques d’événements pour le serveur de publication et l’abonné.</span><span class="sxs-lookup"><span data-stu-id="49c4e-109">The COM+ events service handles most of the event semantics for the publisher and subscriber.</span></span> <span data-ttu-id="49c4e-110">Les éditeurs offrent la publication de types d’événements, et les abonnés demandent des types d’événements à partir des serveurs de publication.</span><span class="sxs-lookup"><span data-stu-id="49c4e-110">Publishers offer to publish event types, and subscribers request event types from publishers.</span></span> <span data-ttu-id="49c4e-111">Contrairement à un système d' *événements étroitement couplé* , où les éditeurs doivent gérer directement la surcharge liée à l’appel d’abonnés, le service d’événements com+ gère les données d’abonnement dans le catalogue com+, indépendamment du serveur de publication et de l’abonné.</span><span class="sxs-lookup"><span data-stu-id="49c4e-111">Unlike a *tightly coupled event* system, where publishers must handle the overhead of calling subscribers directly, the COM+ events service maintains subscription data in the COM+ catalog, independent of the publisher and subscriber.</span></span> <span data-ttu-id="49c4e-112">Cela simplifie le modèle de programmation pour le serveur de publication et l’abonné, car le composant d’abonné COM+ n’a pas besoin de contenir la logique de création d’abonnements.</span><span class="sxs-lookup"><span data-stu-id="49c4e-112">This simplifies the programming model for the publisher and subscriber because the COM+ subscriber component does not need to contain the logic for building subscriptions.</span></span>

<span data-ttu-id="49c4e-113">Étant donné que le cycle de vie des données d’abonnement aux événements COM+ est distinct de celui du serveur de publication ou de l’abonné, les abonnements peuvent être générés avant que l’abonné ou les applications du serveur de publication soient actifs.</span><span class="sxs-lookup"><span data-stu-id="49c4e-113">Because the life cycle of the COM+ events subscription data is separate from that of either the publisher or the subscriber, subscriptions can be built prior to either the subscriber or the publisher applications being active.</span></span> <span data-ttu-id="49c4e-114">Cela signifie également que les serveurs de publication et les abonnés peuvent être développés et déployés séparément.</span><span class="sxs-lookup"><span data-stu-id="49c4e-114">This also means that publishers and subscribers can be developed and deployed separately.</span></span> <span data-ttu-id="49c4e-115">Le serveur de publication peut être écrit sans connaître le nombre et l’emplacement des abonnés.</span><span class="sxs-lookup"><span data-stu-id="49c4e-115">The publisher can be written without knowledge of the number and location of the subscribers.</span></span> <span data-ttu-id="49c4e-116">Les abonnés utilisent le service événements COM+ pour rechercher le serveur de publication et gérer leurs abonnements.</span><span class="sxs-lookup"><span data-stu-id="49c4e-116">The subscribers use the COM+ Events service to find the publisher and manage their subscriptions.</span></span>

<span data-ttu-id="49c4e-117">Les rubriques suivantes de cette section fournissent des informations détaillées sur les éléments de base du service d’événements COM+ et expliquent comment les utiliser.</span><span class="sxs-lookup"><span data-stu-id="49c4e-117">The following topics in this section provide detailed information about the core elements of the COM+ events service and how to use them.</span></span>

-   [<span data-ttu-id="49c4e-118">Objet de classe d’événements COM+</span><span class="sxs-lookup"><span data-stu-id="49c4e-118">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
-   [<span data-ttu-id="49c4e-119">Abonnements</span><span class="sxs-lookup"><span data-stu-id="49c4e-119">Subscriptions</span></span>](subscriptions.md)
-   [<span data-ttu-id="49c4e-120">Publication et diffusion d’événements dans COM+</span><span class="sxs-lookup"><span data-stu-id="49c4e-120">Publishing and Delivering Events in COM+</span></span>](publishing-and-delivering-events-in-com-.md)
-   [<span data-ttu-id="49c4e-121">Filtrage des événements dans COM+</span><span class="sxs-lookup"><span data-stu-id="49c4e-121">Filtering Events in COM+</span></span>](filtering-events-in-com-.md)
-   [<span data-ttu-id="49c4e-122">Utilisation d’événements COM+ avec des composants en file d’attente COM+</span><span class="sxs-lookup"><span data-stu-id="49c4e-122">Using COM+ Events with COM+ Queued Components</span></span>](using-com--events-with-com--queued-components.md)

## <a name="related-topics"></a><span data-ttu-id="49c4e-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="49c4e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49c4e-124">Considérations sur la sécurité des événements COM+</span><span class="sxs-lookup"><span data-stu-id="49c4e-124">COM+ Events Security Considerations</span></span>](com--events-security-considerations.md)
</dt> <dt>

[<span data-ttu-id="49c4e-125">Tâches des événements COM+</span><span class="sxs-lookup"><span data-stu-id="49c4e-125">COM+ Events Tasks</span></span>](com--events-tasks.md)
</dt> </dl>

 

 



