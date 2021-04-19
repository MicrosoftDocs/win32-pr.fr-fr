---
description: À propos du gestionnaire de graphique de filtre
ms.assetid: a227539a-7f9a-4f8d-99fe-f9ab67df9ef4
title: À propos du gestionnaire de graphique de filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dedf716b84ee62818e323bfaa082b6252e5faad0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522239"
---
# <a name="about-the-filter-graph-manager"></a><span data-ttu-id="7bc08-103">À propos du gestionnaire de graphique de filtre</span><span class="sxs-lookup"><span data-stu-id="7bc08-103">About the Filter Graph Manager</span></span>

<span data-ttu-id="7bc08-104">Le [Gestionnaire de graphes de filtres](filter-graph-manager.md) est un objet com qui contrôle les filtres dans un graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="7bc08-104">The [Filter Graph Manager](filter-graph-manager.md) is a COM object that controls the filters in a filter graph.</span></span> <span data-ttu-id="7bc08-105">Il effectue de nombreuses fonctions, y compris les suivantes :</span><span class="sxs-lookup"><span data-stu-id="7bc08-105">It performs many functions, including the following:</span></span>

-   <span data-ttu-id="7bc08-106">Coordination des changements d’état parmi les filtres.</span><span class="sxs-lookup"><span data-stu-id="7bc08-106">Coordinating state changes among the filters.</span></span>
-   <span data-ttu-id="7bc08-107">Établissement d’une horloge de référence.</span><span class="sxs-lookup"><span data-stu-id="7bc08-107">Establishing a reference clock.</span></span>
-   <span data-ttu-id="7bc08-108">Communication des événements à l’application.</span><span class="sxs-lookup"><span data-stu-id="7bc08-108">Communicating events back to the application.</span></span>
-   <span data-ttu-id="7bc08-109">Fournir des méthodes pour que les applications génèrent le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="7bc08-109">Providing methods for applications to build the filter graph.</span></span>

<span data-ttu-id="7bc08-110">Chacune de ces fonctions est décrite brièvement ici.</span><span class="sxs-lookup"><span data-stu-id="7bc08-110">Each of these functions is described briefly here.</span></span> <span data-ttu-id="7bc08-111">Vous trouverez des détails ailleurs dans la documentation.</span><span class="sxs-lookup"><span data-stu-id="7bc08-111">Details can be found elsewhere in the documentation.</span></span>

<span data-ttu-id="7bc08-112">**Modifications d’État**.</span><span class="sxs-lookup"><span data-stu-id="7bc08-112">**State changes**.</span></span> <span data-ttu-id="7bc08-113">Les changements d’État dans les filtres doivent se produire dans un ordre particulier.</span><span class="sxs-lookup"><span data-stu-id="7bc08-113">State changes within filters must occur in a particular order.</span></span> <span data-ttu-id="7bc08-114">Par conséquent, l’application n’émet pas de commandes de modification d’État directement aux filtres.</span><span class="sxs-lookup"><span data-stu-id="7bc08-114">Therefore, the application does not issue state-change commands directly to the filters.</span></span> <span data-ttu-id="7bc08-115">Au lieu de cela, il fournit une seule commande au gestionnaire de graphique de filtre, qui distribue la commande à chacun des filtres.</span><span class="sxs-lookup"><span data-stu-id="7bc08-115">Instead, it gives a single command to the Filter Graph Manager, which distributes the command to each of the filters.</span></span> <span data-ttu-id="7bc08-116">La recherche fonctionne de la même manière : l’application fournit une commande Seek au gestionnaire de graphique de filtre, qui le distribue aux filtres.</span><span class="sxs-lookup"><span data-stu-id="7bc08-116">Seeking works in a similar fashion: The application gives a seek command to the Filter Graph Manager, which distributes it to the filters.</span></span>

<span data-ttu-id="7bc08-117">**Horloge de référence**.</span><span class="sxs-lookup"><span data-stu-id="7bc08-117">**Reference clock**.</span></span> <span data-ttu-id="7bc08-118">Tous les filtres du graphique utilisent la même horloge, appelée *horloge de référence*.</span><span class="sxs-lookup"><span data-stu-id="7bc08-118">All of the filters in the graph use the same clock, called a *reference clock*.</span></span> <span data-ttu-id="7bc08-119">L’horloge de référence garantit que tous les flux sont synchronisés.</span><span class="sxs-lookup"><span data-stu-id="7bc08-119">The reference clock ensures that all the streams are synchronized.</span></span> <span data-ttu-id="7bc08-120">L’heure à laquelle un échantillon vidéo ou audio doit être rendu est l’heure de la *Présentation*.</span><span class="sxs-lookup"><span data-stu-id="7bc08-120">The time at which a video frame or audio sample should be rendered is called the *presentation time*.</span></span> <span data-ttu-id="7bc08-121">L’heure de la présentation est mesurée par rapport à l’horloge de référence.</span><span class="sxs-lookup"><span data-stu-id="7bc08-121">The presentation time is measured relative to the reference clock.</span></span> <span data-ttu-id="7bc08-122">Le gestionnaire de graphe de filtre choisit une horloge de référence, généralement l’horloge de la carte son ou l’horloge système.</span><span class="sxs-lookup"><span data-stu-id="7bc08-122">The Filter Graph Manager chooses a reference clock, usually either the clock on the sound card, or the system clock.</span></span>

<span data-ttu-id="7bc08-123">**Événements de graphique**.</span><span class="sxs-lookup"><span data-stu-id="7bc08-123">**Graph events**.</span></span> <span data-ttu-id="7bc08-124">Le gestionnaire de graphique de filtre utilise une file d’attente d’événements pour informer l’application des événements qui se produisent dans le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="7bc08-124">The Filter Graph Manager uses an event queue to inform the application of events that occur in the filter graph.</span></span> <span data-ttu-id="7bc08-125">Ce mécanisme est similaire à une boucle de messages Windows.</span><span class="sxs-lookup"><span data-stu-id="7bc08-125">This mechanism is similar to a Windows message loop.</span></span>

<span data-ttu-id="7bc08-126">**Méthodes de création de graphiques**.</span><span class="sxs-lookup"><span data-stu-id="7bc08-126">**Graph-building methods**.</span></span> <span data-ttu-id="7bc08-127">Le gestionnaire de graphes de filtre fournit des méthodes pour que l’application ajoute des filtres au graphique, connecte des filtres à d’autres filtres et déconnecte des filtres.</span><span class="sxs-lookup"><span data-stu-id="7bc08-127">The Filter Graph Manager provides methods for the application to add filters to the graph, connect filters to other filters, and disconnect filters.</span></span>

<span data-ttu-id="7bc08-128">Une fonction que le gestionnaire de graphes de filtre ne gère pas consiste à déplacer les données d’un filtre à l’autre.</span><span class="sxs-lookup"><span data-stu-id="7bc08-128">One function the Filter Graph Manager does not handle is moving data from one filter to the next.</span></span> <span data-ttu-id="7bc08-129">Cela est effectué par les filtres eux-mêmes, par le biais de leurs connexions de code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="7bc08-129">This is done by the filters themselves, through their pin connections.</span></span> <span data-ttu-id="7bc08-130">Le traitement se produit toujours sur un thread séparé.</span><span class="sxs-lookup"><span data-stu-id="7bc08-130">Processing always happens on a separate thread.</span></span>

> [!Note]  
> <span data-ttu-id="7bc08-131">Les filtres sont toujours libres de thread, résident dans le même processus que le gestionnaire de graphes de filtre et sont chargés à partir de serveurs in-process.</span><span class="sxs-lookup"><span data-stu-id="7bc08-131">Filters are always free-threaded, reside in the same process as the Filter Graph Manager, and are loaded from in-process servers.</span></span> <span data-ttu-id="7bc08-132">Par conséquent, les appels de méthode ne sont pas marshalés entre les filtres, ni entre les filtres et le gestionnaire de graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="7bc08-132">Therefore, method calls are not marshaled between filters, or between filters and the Filter Graph Manager.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="7bc08-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7bc08-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bc08-134">Data Flow dans le graphique de filtre</span><span class="sxs-lookup"><span data-stu-id="7bc08-134">Data Flow in the Filter Graph</span></span>](data-flow-in-the-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="7bc08-135">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="7bc08-135">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="7bc08-136">Définition de l’horloge du graphique</span><span class="sxs-lookup"><span data-stu-id="7bc08-136">Setting the Graph Clock</span></span>](setting-the-graph-clock.md)
</dt> <dt>

[<span data-ttu-id="7bc08-137">Temps et horloges dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="7bc08-137">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



