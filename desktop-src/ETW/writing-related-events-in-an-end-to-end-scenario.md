---
description: ETW offre un moyen de regrouper les événements connexes à partir de plusieurs composants.
ms.assetid: 2a85e4af-a1fe-4c28-8ce2-14d15deaa820
title: Écriture d’événements connexes dans un scénario de bout en bout
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d27b3455ffe71c6d657e935e6f93dc2dc39392
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972255"
---
# <a name="writing-related-events-in-an-end-to-end-scenario"></a><span data-ttu-id="6a007-103">Écriture d’événements connexes dans un scénario de bout en bout</span><span class="sxs-lookup"><span data-stu-id="6a007-103">Writing Related Events in an End-to-End Scenario</span></span>

<span data-ttu-id="6a007-104">ETW offre un moyen de regrouper les événements connexes à partir de plusieurs composants.</span><span class="sxs-lookup"><span data-stu-id="6a007-104">ETW provides a way to group related events from more than one component.</span></span> <span data-ttu-id="6a007-105">Par exemple, si plusieurs composants (sur le même ordinateur ou sur des ordinateurs différents) sont impliqués dans le traitement des mêmes données, et que chaque composant consigne des événements pour leur partie de l’activité, vous pouvez regrouper tous les événements associés.</span><span class="sxs-lookup"><span data-stu-id="6a007-105">For example, if several components (either on the same computer or on different computers) are involved in processing the same data, and each component logs events for their portion of the activity, you can group all of the related events together.</span></span> <span data-ttu-id="6a007-106">Cela permettra à un consommateur d’utiliser tous les événements, du début du processus à la fin du processus.</span><span class="sxs-lookup"><span data-stu-id="6a007-106">This will allow a consumer to consume all of the events, from the beginning of the process to the end of the process.</span></span>

<span data-ttu-id="6a007-107">Pour écrire des événements connexes dans un fournisseur basé sur un [manifeste](about-event-tracing.md) , consultez [écriture d’événements connexes dans un fournisseur basé sur un manifeste](writing-related-events-in-a-manifest-base-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6a007-107">To write related events in a [manifest-based](about-event-tracing.md) provider, see [Writing Related Events in a Manifest-based Provider](writing-related-events-in-a-manifest-base-provider.md).</span></span>

<span data-ttu-id="6a007-108">Pour écrire des événements connexes dans un fournisseur [Classic](about-event-tracing.md) , consultez [écriture d’événements connexes dans un fournisseur classique](tracing-event-instances.md).</span><span class="sxs-lookup"><span data-stu-id="6a007-108">To write related events in a [classic](about-event-tracing.md) provider, see [Writing Related Events in a Classic Provider](tracing-event-instances.md).</span></span>

 

 



