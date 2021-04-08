---
description: 'Les événements COM+ offrent deux moyens de contrôler les événements qui atteignent les abonnés : le filtrage du serveur de publication et le filtrage des paramètres.'
ms.assetid: dfc82a57-5587-462d-a43d-516b7d70e25e
title: Filtrage des événements dans COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d3a7d152813e4806a9cfb6a342255e0981ecf37
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748861"
---
# <a name="filtering-events-in-com"></a><span data-ttu-id="222ce-103">Filtrage des événements dans COM+</span><span class="sxs-lookup"><span data-stu-id="222ce-103">Filtering Events in COM+</span></span>

<span data-ttu-id="222ce-104">Les événements COM+ offrent deux moyens de contrôler les événements qui atteignent les abonnés : le filtrage du serveur de *publication* et le *filtrage des paramètres*.</span><span class="sxs-lookup"><span data-stu-id="222ce-104">COM+ Events provides two ways to control which events reach which subscribers: *publisher filtering* and *parameter filtering*.</span></span>

## <a name="publisher-filtering"></a><span data-ttu-id="222ce-105">Filtrage de l’éditeur</span><span class="sxs-lookup"><span data-stu-id="222ce-105">Publisher Filtering</span></span>

<span data-ttu-id="222ce-106">Le filtrage de l’éditeur contrôle l’ordre et le déclenchement d’une méthode d’événement par un objet de [classe d’événements](the-com--event-class-object.md) .</span><span class="sxs-lookup"><span data-stu-id="222ce-106">Publisher filtering controls the order and firing of an event method by an [event class](the-com--event-class-object.md) object.</span></span> <span data-ttu-id="222ce-107">Le filtrage de l’éditeur permet au serveur de publication de déterminer les abonnés qui reçoivent un événement particulier.</span><span class="sxs-lookup"><span data-stu-id="222ce-107">Publisher filtering allows the publisher to determine which subscribers receive a particular event.</span></span>

<span data-ttu-id="222ce-108">Un exemple d’utilisation efficace du filtrage de l’éditeur est celui d’une bourse.</span><span class="sxs-lookup"><span data-stu-id="222ce-108">An example of effective use of publisher filtering is that of a stock exchange.</span></span> <span data-ttu-id="222ce-109">La plupart des abonnés veulent savoir quand une nouvelle action est ajoutée.</span><span class="sxs-lookup"><span data-stu-id="222ce-109">Most subscribers want to know when a new stock is added.</span></span> <span data-ttu-id="222ce-110">Toutefois, un grand nombre de ces mêmes abonnés peuvent ne pas souhaiter savoir à quel moment chaque cours d’action change.</span><span class="sxs-lookup"><span data-stu-id="222ce-110">However, many of these same subscribers may not want to know whenever each stock price changes.</span></span> <span data-ttu-id="222ce-111">Le filtrage de l’éditeur fournit la granularité requise pour remettre efficacement les événements aux abonnés qui souhaitent ces informations.</span><span class="sxs-lookup"><span data-stu-id="222ce-111">Publisher filtering provides the granularity required to effectively deliver events to only the subscribers who want this information.</span></span>

<span data-ttu-id="222ce-112">Lorsqu’une méthode est appelée sur l’objet de classe d’événements instancié, elle collecte tous les filtres d’éditeur sur cette méthode.</span><span class="sxs-lookup"><span data-stu-id="222ce-112">When a method is invoked on the instantiated event class object, it collects any publisher filters on that method.</span></span> <span data-ttu-id="222ce-113">Le filtre force l’objet d’événement à déclencher la méthode d’événement sur un abonné spécifique.</span><span class="sxs-lookup"><span data-stu-id="222ce-113">The filter forces the event object to fire the event method to a specific subscriber.</span></span> <span data-ttu-id="222ce-114">Le filtre détermine les abonnements à activer et leur ordre de déclenchement.</span><span class="sxs-lookup"><span data-stu-id="222ce-114">The filter determines which subscriptions to fire and in which order to fire them.</span></span> <span data-ttu-id="222ce-115">Par exemple, le filtre peut lire la liste des abonnements et créer la commande en fonction de certains critères d’application, puis appeler les abonnés dans cet ordre.</span><span class="sxs-lookup"><span data-stu-id="222ce-115">For example, the filter could read the subscription list and create the order based on some application criteria and then call the subscribers in that order.</span></span>

<span data-ttu-id="222ce-116">Pour obtenir des instructions détaillées sur la création d’un filtre de serveur de publication, consultez [création d’un filtre](creating-a-publisher-filter.md)de serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="222ce-116">For detailed instructions on creating a publisher filter, see [Creating a Publisher Filter](creating-a-publisher-filter.md).</span></span>

## <a name="parameter-filtering"></a><span data-ttu-id="222ce-117">Filtrage des paramètres</span><span class="sxs-lookup"><span data-stu-id="222ce-117">Parameter Filtering</span></span>

<span data-ttu-id="222ce-118">Contrairement au filtrage de l’éditeur, le service d’événements COM+ fournit un filtrage facultatif des paramètres de l’abonné pour chaque abonnement et chaque appel de méthode d’événement.</span><span class="sxs-lookup"><span data-stu-id="222ce-118">In contrast to publisher filtering, the COM+ Events service provides an optional subscriber parameter filtering for each subscription and each event method invocation.</span></span> <span data-ttu-id="222ce-119">Le filtrage des paramètres évalue la propriété de l’abonnement de l’abonnement par rapport aux paramètres de la méthode d’événement.</span><span class="sxs-lookup"><span data-stu-id="222ce-119">Parameter filtering evaluates the subscription FilterCriteria property against the parameters of the event method.</span></span> <span data-ttu-id="222ce-120">Ce type de filtrage est utilisé sur la base de la méthode par abonnement et fournit un niveau de filtrage des abonnés au niveau de la source de l’événement.</span><span class="sxs-lookup"><span data-stu-id="222ce-120">This type of filtering is used on a per-method, per-subscription basis and provides a level of subscriber filtering at the event source.</span></span> <span data-ttu-id="222ce-121">La chaîne des critères de filtre reconnaît les opérateurs relationnels pour la vérification de l’égalité (=, = =, !, ! =, ~, ~ =,  <>), les parenthèses imbriquées et les mots clés logiques **and**, **or** ou **not**.</span><span class="sxs-lookup"><span data-stu-id="222ce-121">The filter criteria string recognizes relational operators for checking equality (=, ==, !, !=, ~, ~=, <>), nested parentheses, and logical keywords **AND**, **OR**, or **NOT**.</span></span>

<span data-ttu-id="222ce-122">Le filtrage des paramètres se produit après tout filtrage de l’éditeur et lorsque l’objet d’événement standard est déclenché pour un abonnement donné.</span><span class="sxs-lookup"><span data-stu-id="222ce-122">Parameter filtering occurs after any publisher filtering and when the standard event object is fired for a given subscription.</span></span> <span data-ttu-id="222ce-123">Si le filtrage de l’éditeur est utilisé, le filtrage des paramètres se produit uniquement lorsque le filtre de l’éditeur appelle [**IFiringControl :: FireSubscription**](/windows/desktop/api/EventSys/nf-eventsys-ifiringcontrol-firesubscription).</span><span class="sxs-lookup"><span data-stu-id="222ce-123">If publisher filtering is used, parameter filtering occurs only when the publisher filter invokes [**IFiringControl::FireSubscription**](/windows/desktop/api/EventSys/nf-eventsys-ifiringcontrol-firesubscription).</span></span> <span data-ttu-id="222ce-124">Pour cette raison, le filtrage de l’éditeur et le filtrage des paramètres peuvent se composer ensemble, mais le filtrage de l’éditeur est prioritaire.</span><span class="sxs-lookup"><span data-stu-id="222ce-124">Because of this, publisher filtering and parameter filtering can compose together but publisher filtering takes precedence.</span></span>

## <a name="related-topics"></a><span data-ttu-id="222ce-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="222ce-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="222ce-126">Publication et diffusion d’événements dans COM+</span><span class="sxs-lookup"><span data-stu-id="222ce-126">Publishing and Delivering Events in COM+</span></span>](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="222ce-127">Abonnements</span><span class="sxs-lookup"><span data-stu-id="222ce-127">Subscriptions</span></span>](subscriptions.md)
</dt> <dt>

[<span data-ttu-id="222ce-128">Objet de classe d’événements COM+</span><span class="sxs-lookup"><span data-stu-id="222ce-128">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
</dt> <dt>

[<span data-ttu-id="222ce-129">Utilisation d’événements COM+ avec des composants en file d’attente COM+</span><span class="sxs-lookup"><span data-stu-id="222ce-129">Using COM+ Events with COM+ Queued Components</span></span>](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 



