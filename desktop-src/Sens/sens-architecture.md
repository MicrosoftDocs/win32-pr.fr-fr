---
description: Le service de notification d’événements système fonctionne avec le système d’événements COM+.
ms.assetid: c51d1f61-6087-4480-b989-31241829781b
title: Architecture SENSe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32976a716ab0ba5651ce6605fe524d639820696
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520106"
---
# <a name="sens-architecture"></a><span data-ttu-id="f8000-103">Architecture SENSe</span><span class="sxs-lookup"><span data-stu-id="f8000-103">SENS Architecture</span></span>

<span data-ttu-id="f8000-104">Le service de notification d’événements système fonctionne avec le système d’événements COM+.</span><span class="sxs-lookup"><span data-stu-id="f8000-104">The System Event Notification Service works with the COM+ Event System.</span></span> <span data-ttu-id="f8000-105">SENS est un éditeur d’événements pour les classes d’événements qu’il surveille : le réseau, l’ouverture de session et les événements d’alimentation/batterie.</span><span class="sxs-lookup"><span data-stu-id="f8000-105">SENS is an event publisher for the classes of events that it monitors: network, logon, and power/battery events.</span></span> <span data-ttu-id="f8000-106">L’application recevant une notification est appelée abonné aux événements.</span><span class="sxs-lookup"><span data-stu-id="f8000-106">The application receiving a notification is called an event subscriber.</span></span>

<span data-ttu-id="f8000-107">Lorsqu’une application s’abonne pour recevoir des notifications, elle peut également spécifier des filtres associés aux événements souscrits.</span><span class="sxs-lookup"><span data-stu-id="f8000-107">When an application subscribes to receive notifications, it can also specify filters associated with the subscribed events.</span></span> <span data-ttu-id="f8000-108">Les événements SENS et COM+ utilisent les filtres pour déterminer plus en détail quand l’application doit être notifiée.</span><span class="sxs-lookup"><span data-stu-id="f8000-108">SENS and COM+ Events use the filters to further determine when the application should be notified.</span></span>

<span data-ttu-id="f8000-109">Les notifications étant asynchrones, l’application qui reçoit la notification n’a pas besoin d’être active lorsque la notification est envoyée.</span><span class="sxs-lookup"><span data-stu-id="f8000-109">Notifications are asynchronous, so the application receiving the notification does not have to be active when the notification is sent.</span></span> <span data-ttu-id="f8000-110">Lorsqu’une application s’abonne pour recevoir des notifications, elle peut spécifier si elle doit être activée lorsque l’événement se produit ou être notifié plus tard quand elle est active.</span><span class="sxs-lookup"><span data-stu-id="f8000-110">When an application subscribes to receive notifications, it can specify whether it should be activated when the event occurs or notified later when it is active.</span></span>

<span data-ttu-id="f8000-111">L’abonnement peut être temporaire et valide uniquement jusqu’à ce que l’application cesse de s’exécuter, ou il peut être persistant et valide jusqu’à ce que l’application soit supprimée du système.</span><span class="sxs-lookup"><span data-stu-id="f8000-111">The subscription can be transient and valid only until the application stops running, or it can be persistent and valid until the application is removed from the system.</span></span>

<span data-ttu-id="f8000-112">Un magasin de données d’événements COM+ contient des informations sur l’éditeur d’événements (SENS), les abonnés aux événements et les filtres.</span><span class="sxs-lookup"><span data-stu-id="f8000-112">A COM+ Events data store contains information about the event publisher (SENS), event subscribers, and filters.</span></span> <span data-ttu-id="f8000-113">SENS prédéfinit également une interface sortante pour chaque classe d’événements dans une bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="f8000-113">SENS also predefines an outgoing interface for each event class in a type library.</span></span>



| <span data-ttu-id="f8000-114">Classe d'événements</span><span class="sxs-lookup"><span data-stu-id="f8000-114">Event class</span></span>    | <span data-ttu-id="f8000-115">GUID</span><span class="sxs-lookup"><span data-stu-id="f8000-115">GUID</span></span>                          | <span data-ttu-id="f8000-116">Interface</span><span class="sxs-lookup"><span data-stu-id="f8000-116">Interface</span></span>    |
|----------------|-------------------------------|--------------|
| <span data-ttu-id="f8000-117">Événements réseau</span><span class="sxs-lookup"><span data-stu-id="f8000-117">Network events</span></span> | <span data-ttu-id="f8000-118">\_réseau SENSGUID EVENTCLASS \_</span><span class="sxs-lookup"><span data-stu-id="f8000-118">SENSGUID\_EVENTCLASS\_NETWORK</span></span> | <span data-ttu-id="f8000-119">ISensNetwork</span><span class="sxs-lookup"><span data-stu-id="f8000-119">ISensNetwork</span></span> |
| <span data-ttu-id="f8000-120">Événements de connexion</span><span class="sxs-lookup"><span data-stu-id="f8000-120">Logon events</span></span>   | <span data-ttu-id="f8000-121">\_ouverture de \_ session SENSGUID EVENTCLASS</span><span class="sxs-lookup"><span data-stu-id="f8000-121">SENSGUID\_EVENTCLASS\_LOGON</span></span>   | <span data-ttu-id="f8000-122">ISensLogon</span><span class="sxs-lookup"><span data-stu-id="f8000-122">ISensLogon</span></span>   |
| <span data-ttu-id="f8000-123">Événements d’alimentation</span><span class="sxs-lookup"><span data-stu-id="f8000-123">Power events</span></span>   | <span data-ttu-id="f8000-124">SENSGUID \_ EVENTCLASS \_ ONNOW</span><span class="sxs-lookup"><span data-stu-id="f8000-124">SENSGUID\_EVENTCLASS\_ONNOW</span></span>   | <span data-ttu-id="f8000-125">ISensOnNow</span><span class="sxs-lookup"><span data-stu-id="f8000-125">ISensOnNow</span></span>   |



 

<span data-ttu-id="f8000-126">Pour recevoir des notifications pour l’un de ces événements, votre application doit effectuer deux opérations :</span><span class="sxs-lookup"><span data-stu-id="f8000-126">To receive notifications for any of these events, your application must do two things:</span></span>

-   <span data-ttu-id="f8000-127">Abonnez-vous aux événements SENS qui vous intéressent.</span><span class="sxs-lookup"><span data-stu-id="f8000-127">Subscribe to the SENS events that interest you.</span></span> <span data-ttu-id="f8000-128">Pour vous abonner à un événement, utilisez les interfaces **IEventSubscription** et **IEventSystem** dans les événements com+.</span><span class="sxs-lookup"><span data-stu-id="f8000-128">To subscribe to an event, use the **IEventSubscription** and **IEventSystem** interfaces in COM+ Events.</span></span> <span data-ttu-id="f8000-129">Vous devez fournir un identificateur pour les classes d’événements et l’identificateur d’éditeur SENSe, SENSGUID \_ Publisher.</span><span class="sxs-lookup"><span data-stu-id="f8000-129">You need to supply an identifier for the event classes and the SENS publisher identifier, SENSGUID\_PUBLISHER.</span></span> <span data-ttu-id="f8000-130">Les abonnements sont au niveau de chaque événement, de sorte que l’application d’abonnement doit également spécifier les événements de la classe qui sont intéressants.</span><span class="sxs-lookup"><span data-stu-id="f8000-130">Subscriptions are on a per event level so the subscribing application must also specify which events within the class are of interest.</span></span> <span data-ttu-id="f8000-131">Chaque événement correspond à une méthode dans l’interface correspondant à sa classe d’événements.</span><span class="sxs-lookup"><span data-stu-id="f8000-131">Each event corresponds to a method in the interface corresponding to its event class.</span></span>
-   <span data-ttu-id="f8000-132">Créez un objet récepteur avec une implémentation pour chaque interface que vous gérez.</span><span class="sxs-lookup"><span data-stu-id="f8000-132">Create a sink object with an implementation for each interface that you handle.</span></span> <span data-ttu-id="f8000-133">Pour plus d’informations sur ces interfaces et les événements pris en charge dans chacun d’eux, consultez [**ISensNetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork), [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)et [**ISensOnNow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow) .</span><span class="sxs-lookup"><span data-stu-id="f8000-133">See [**ISensNetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork), [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon), and [**ISensOnNow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow) for more information about these interfaces and the events supported in each one.</span></span>

<span data-ttu-id="f8000-134">Lorsque l’un des événements contrôlés se produit, SENS traite chaque abonnement avec les filtres associés et notifie les abonnés via le système d’événement COM+.</span><span class="sxs-lookup"><span data-stu-id="f8000-134">When one of the monitored events occurs, SENS processes each subscription with any associated filters and notifies the subscribers through the COM+ Event system.</span></span>

 

 



