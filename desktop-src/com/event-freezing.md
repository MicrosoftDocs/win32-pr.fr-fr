---
title: Gel des événements
description: Gel des événements
ms.assetid: 1e537503-f7e7-42f4-aa3c-3c71715b84fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e403448d53949c263b8e146961690de1200436c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839929"
---
# <a name="event-freezing"></a><span data-ttu-id="af733-103">Gel des événements</span><span class="sxs-lookup"><span data-stu-id="af733-103">Event Freezing</span></span>

<span data-ttu-id="af733-104">Un conteneur peut notifier un contrôle qu’il n’est pas prêt à répondre aux événements en appelant [**IOleControl :: FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) avec **true**.</span><span class="sxs-lookup"><span data-stu-id="af733-104">A container can notify a control that it is not ready to respond to events by calling [**IOleControl::FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) with **TRUE**.</span></span> <span data-ttu-id="af733-105">Il peut libérer les événements en appelant **FreezeEvents** avec **false**.</span><span class="sxs-lookup"><span data-stu-id="af733-105">It can unfreeze the events by calling **FreezeEvents** with **FALSE**.</span></span> <span data-ttu-id="af733-106">Lorsqu’un conteneur gèle des événements, il fige le traitement des événements, pas la réception d’événements ; autrement dit, un conteneur peut toujours recevoir des événements tandis que les événements sont figés.</span><span class="sxs-lookup"><span data-stu-id="af733-106">When a container freezes events, it is freezing event processing, not event receiving; that is, a container can still receive events while events are frozen.</span></span> <span data-ttu-id="af733-107">Si un conteneur reçoit une notification d’événement alors que ses événements sont figés, le conteneur doit ignorer l’événement.</span><span class="sxs-lookup"><span data-stu-id="af733-107">If a container receives an event notification while its events are frozen, the container should ignore the event.</span></span> <span data-ttu-id="af733-108">Aucune autre action n’est appropriée.</span><span class="sxs-lookup"><span data-stu-id="af733-108">No other action is appropriate.</span></span>

<span data-ttu-id="af733-109">Un contrôle doit prendre note de l’appel d’un conteneur à [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) avec **true** s’il est important pour le contrôle qu’un événement ne soit pas manqué.</span><span class="sxs-lookup"><span data-stu-id="af733-109">A control should take note of a container's call to [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) with **TRUE** if it is important to the control that an event is not missed.</span></span> <span data-ttu-id="af733-110">Tandis que le traitement des événements d’un conteneur est figé, un contrôle doit implémenter l’une des techniques suivantes :</span><span class="sxs-lookup"><span data-stu-id="af733-110">While a container's event processing is frozen, a control should implement one of the following techniques:</span></span>

-   <span data-ttu-id="af733-111">Déclenchez les événements dans la connaissance totale selon laquelle le conteneur n’effectuera aucune action.</span><span class="sxs-lookup"><span data-stu-id="af733-111">Fire the events in the full knowledge that the container will take no action.</span></span>
-   <span data-ttu-id="af733-112">Ignorer tous les événements que le contrôle aurait déclenchés.</span><span class="sxs-lookup"><span data-stu-id="af733-112">Discard all events that the control would have fired.</span></span>
-   <span data-ttu-id="af733-113">Met en file d’attente tous les événements en attente et les déclenche après que le conteneur a appelé [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) avec la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="af733-113">Queue up all pending events and fire them after the container has called [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) with **FALSE**.</span></span>
-   <span data-ttu-id="af733-114">Met en file d’attente uniquement les événements pertinents ou importants et les déclenche après que le conteneur a appelé [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) avec la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="af733-114">Queue up only relevant or important events and fire them after the container has called [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) with **FALSE**.</span></span>

<span data-ttu-id="af733-115">Chaque technique est acceptable et appropriée dans différentes circonstances.</span><span class="sxs-lookup"><span data-stu-id="af733-115">Each technique is acceptable and appropriate in different circumstances.</span></span> <span data-ttu-id="af733-116">Le développeur de contrôle est responsable de la détermination et de l’implémentation de la technique appropriée pour les fonctionnalités du contrôle.</span><span class="sxs-lookup"><span data-stu-id="af733-116">The control developer is responsible for determining and implementing the appropriate technique for the control's functionality.</span></span>

 

 




