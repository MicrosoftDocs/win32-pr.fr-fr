---
title: Utilisation du collecteur d’événements Windows
description: Cette section répertorie les rubriques qui expliquent les tâches réalisables à l’aide du kit de développement logiciel (SDK) du collecteur d’événements Windows. Des exemples de code et des explications sur toutes les tâches sont inclus dans chacune des rubriques suivantes.
ms.assetid: 3396454a-4f43-45d0-951e-3096b9a4a077
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc618ced4cefc7f17fb63b27bb1e097e65b3adac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106525704"
---
# <a name="using-windows-event-collector"></a><span data-ttu-id="349a9-104">Utilisation du collecteur d’événements Windows</span><span class="sxs-lookup"><span data-stu-id="349a9-104">Using Windows Event Collector</span></span>

<span data-ttu-id="349a9-105">Cette section répertorie les rubriques qui expliquent les tâches réalisables à l’aide du kit de développement logiciel (SDK) du collecteur d’événements Windows.</span><span class="sxs-lookup"><span data-stu-id="349a9-105">This section lists the topics that explain the tasks that can be accomplished using the Windows Event Collector SDK.</span></span> <span data-ttu-id="349a9-106">Des exemples de code et des explications sur toutes les tâches sont inclus dans chacune des rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="349a9-106">Code examples and explanations for all the tasks are included in each of the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="349a9-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="349a9-107">In This Section</span></span>

-   [<span data-ttu-id="349a9-108">Création d’un abonnement initié par le collecteur</span><span class="sxs-lookup"><span data-stu-id="349a9-108">Creating a Collector Initiated Subscription</span></span>](creating-an-event-collector-subscription.md)

    <span data-ttu-id="349a9-109">Fournit des informations et un exemple de code C++ pour créer un abonnement initié par le collecteur.</span><span class="sxs-lookup"><span data-stu-id="349a9-109">Provides information and a C++ code example for creating a collector-initiated subscription.</span></span> <span data-ttu-id="349a9-110">Un abonnement initié par le collecteur vous permet de recevoir des événements sur un ordinateur local (le collecteur d’événements) qui sont transférés à partir d’un ordinateur distant (une source d’événement).</span><span class="sxs-lookup"><span data-stu-id="349a9-110">A collector-initiated subscription enables you to receive events on a local computer (the event collector) that are forwarded from a remote computer (an event source).</span></span>

-   [<span data-ttu-id="349a9-111">Configuration d’un abonnement initié par la source</span><span class="sxs-lookup"><span data-stu-id="349a9-111">Setting up a Source Initiated Subscription</span></span>](setting-up-a-source-initiated-subscription.md)

    <span data-ttu-id="349a9-112">Fournit des informations et un exemple de code C++ pour la création d’un abonnement initié par la source.</span><span class="sxs-lookup"><span data-stu-id="349a9-112">Provides information and a C++ code example for creating a source-initiated subscription.</span></span> <span data-ttu-id="349a9-113">Un abonnement initié par la source vous permet de recevoir des événements sur un ordinateur local (le collecteur d’événements) qui sont transférés à partir d’un ordinateur distant (une source d’événement) sans spécifier les sources d’événements dans l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="349a9-113">A source-initiated subscription enables you to receive events on a local computer (the event collector) that are forwarded from a remote computer (an event source) without specifying the event sources in the subscription.</span></span>

-   [<span data-ttu-id="349a9-114">Ajout d’une source d’événement à un abonnement initié par le collecteur</span><span class="sxs-lookup"><span data-stu-id="349a9-114">Adding an Event Source to a Collector Initiated Subscription</span></span>](adding-an-event-source-to-an-event-collector-subscription.md)

    <span data-ttu-id="349a9-115">Fournit des informations et un exemple de code C++ pour l’ajout d’une source d’événement (ordinateur local ou ordinateur distant) à un abonnement initié par le collecteur.</span><span class="sxs-lookup"><span data-stu-id="349a9-115">Provides information and a C++ code example for adding an event source (local computer or remote computer) to a collector-initiated subscription.</span></span> <span data-ttu-id="349a9-116">Un abonnement initié par le collecteur ne peut pas commencer à collecter des événements tant qu’une source d’événement n’a pas été ajoutée à l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="349a9-116">A collector initiated subscription cannot start collecting events until an event source is added to the subscription.</span></span>

-   [<span data-ttu-id="349a9-117">Création d’abonnements aux événements matériels</span><span class="sxs-lookup"><span data-stu-id="349a9-117">Creating Hardware Event Subscriptions</span></span>](creating-hardware-event-subscriptions.md)

    <span data-ttu-id="349a9-118">Contient des informations sur la création d’un abonnement aux événements pour recevoir des événements matériels d’un ordinateur sur lequel est installé un contrôleur BMC (Baseboard Management Controller).</span><span class="sxs-lookup"><span data-stu-id="349a9-118">Provides information about how to create an event subscription in order to receive hardware events from a computer that has a Baseboard Management Controller (BMC) installed.</span></span>

-   [<span data-ttu-id="349a9-119">Suppression d’un abonnement à un collecteur d’événements</span><span class="sxs-lookup"><span data-stu-id="349a9-119">Deleting an Event Collector Subscription</span></span>](deleting-an-event-collector-subscription.md)

    <span data-ttu-id="349a9-120">Fournit des informations et un exemple de code C++ pour la suppression d’un abonnement d’un collecteur d’événements à partir d’un ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="349a9-120">Provides information and a C++ code example for deleting an Event Collector subscription from a local computer.</span></span>

-   [<span data-ttu-id="349a9-121">Affichage des propriétés d’un abonnement à un collecteur d’événements</span><span class="sxs-lookup"><span data-stu-id="349a9-121">Displaying the Properties of an Event Collector Subscription</span></span>](displaying-the-properties-of-an-event-collector-subscription.md)

    <span data-ttu-id="349a9-122">Fournit des informations et un exemple de code C++ permettant d’afficher les valeurs de propriété d’un abonnement au collecteur d’événements.</span><span class="sxs-lookup"><span data-stu-id="349a9-122">Provides information and a C++ code example for displaying the property values of an Event Collector subscription.</span></span> <span data-ttu-id="349a9-123">Les valeurs de propriété peuvent fournir des informations utiles, telles que les adresses des sources d’événements, l’état de l’abonnement et des sources d’événements, ainsi que des informations sur la façon dont les événements sont remis.</span><span class="sxs-lookup"><span data-stu-id="349a9-123">Property values can provide useful information, such as the addresses of event sources, the status of the subscription and event sources, and information about how events are delivered.</span></span>

-   [<span data-ttu-id="349a9-124">Affichage de l’état d’un abonnement au collecteur d’événements</span><span class="sxs-lookup"><span data-stu-id="349a9-124">Displaying the Status of an Event Collector Subscription</span></span>](displaying-the-status-of-an-event-collector-subscription.md)

    <span data-ttu-id="349a9-125">Fournit des informations et un exemple de code C++ permettant d’afficher l’état d’exécution des sources d’événements associées à un abonnement à un collecteur d’événements.</span><span class="sxs-lookup"><span data-stu-id="349a9-125">Provides information and a C++ code example for displaying the run time status of events sources that are associated to an Event Collector subscription.</span></span> <span data-ttu-id="349a9-126">Cela vous permet d’afficher les messages d’erreur qui peuvent aider à résoudre les problèmes, ce qui empêche une source d’événements de transférer des événements.</span><span class="sxs-lookup"><span data-stu-id="349a9-126">This enables you to view error messages that can help solve problems, which prevent an event source from forwarding events.</span></span>

-   [<span data-ttu-id="349a9-127">Liste des abonnements du collecteur d’événements</span><span class="sxs-lookup"><span data-stu-id="349a9-127">Listing Event Collector Subscriptions</span></span>](listing-event-collector-subscriptions.md)

    <span data-ttu-id="349a9-128">Fournit des informations et un exemple de code C++ pour répertorier les abonnements qui existent sur un ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="349a9-128">Provides information and a C++ code example for listing the subscriptions that exist on a local computer.</span></span> <span data-ttu-id="349a9-129">Vous pouvez utiliser les noms d’abonnements obtenus avec cet exemple pour supprimer un abonnement, ajouter une source d’événement à un abonnement, récupérer les propriétés d’un abonnement ou afficher l’état d’un abonnement.</span><span class="sxs-lookup"><span data-stu-id="349a9-129">You can use the subscription names that are obtained with this example to delete a subscription, add an event source to a subscription, retrieve the properties of a subscription, or view the status of a subscription.</span></span>

-   [<span data-ttu-id="349a9-130">Suppression d’une source d’événement d’un abonnement initié par le collecteur</span><span class="sxs-lookup"><span data-stu-id="349a9-130">Removing an Event Source from a Collector Initiated Subscription</span></span>](removing-an-event-source-from-an-event-collector-subscription.md)

    <span data-ttu-id="349a9-131">Fournit des informations et un exemple de code C++ pour supprimer une source d’événement d’un abonnement initié par le collecteur.</span><span class="sxs-lookup"><span data-stu-id="349a9-131">Provides information and a C++ code example for removing an event source from a collector-initiated subscription.</span></span> <span data-ttu-id="349a9-132">Vous pouvez supprimer une source d’événement d’un abonnement initié par le collecteur sans désactiver l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="349a9-132">You can remove an event source from a collector-initiated subscription without disabling the subscription.</span></span>

-   [<span data-ttu-id="349a9-133">Nouvelle tentative d’abonnement au collecteur d’événements</span><span class="sxs-lookup"><span data-stu-id="349a9-133">Retrying an Event Collector Subscription</span></span>](retrying-an-event-collector-subscription.md)

    <span data-ttu-id="349a9-134">Fournit des informations et un exemple de code C++ pour la nouvelle tentative d’abonnement d’un collecteur d’événements lorsqu’une ou plusieurs sources d’événements ont échoué.</span><span class="sxs-lookup"><span data-stu-id="349a9-134">Provides information and a C++ code example for retrying an Event Collector subscription when one or more event sources have failed.</span></span> <span data-ttu-id="349a9-135">Vous pouvez réessayer une seule source d’événements ou vous pouvez réessayer l’intégralité de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="349a9-135">You can retry a single event source or you can retry the entire subscription.</span></span>

 

 




