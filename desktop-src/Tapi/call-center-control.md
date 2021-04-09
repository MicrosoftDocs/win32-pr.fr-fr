---
description: L’interface TAPI 2,2 de base peut être utilisée pour gérer les centres d’appels et d’autres éléments de l’infrastructure réseau de téléphonie (tels que les serveurs de messagerie vocale et IVR) via un contrôle d’appel tiers.
ms.assetid: e920dc4a-adb4-4a36-ac04-f265538531eb
title: Contrôle du centre d’appels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4200ff434249856507109915f41f7f1479eddfd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866929"
---
# <a name="call-center-control"></a><span data-ttu-id="f0506-103">Contrôle du centre d’appels</span><span class="sxs-lookup"><span data-stu-id="f0506-103">Call Center Control</span></span>

<span data-ttu-id="f0506-104">L’interface TAPI 2,2 de base peut être utilisée pour gérer les centres d’appels et d’autres éléments de l’infrastructure réseau de téléphonie (tels que les serveurs de messagerie vocale et IVR) via un contrôle d’appel tiers.</span><span class="sxs-lookup"><span data-stu-id="f0506-104">Basic TAPI 2.2 can be used to manage call centers and other elements of Telephony network infrastructure (such as IVR and voice mail servers) through third-party call control.</span></span> <span data-ttu-id="f0506-105">Pour faciliter la création de proxys ACD qui s’exécuteront sur des serveurs, des fonctions ont été ajoutées à TAPI 2,2 pour fournir une assistance supplémentaire aux développeurs d’applications.</span><span class="sxs-lookup"><span data-stu-id="f0506-105">To help create ACD proxies that will run on servers, functions have been added to TAPI 2.2 to provide additional assistance to application developers.</span></span>

<span data-ttu-id="f0506-106">Les rubriques suivantes décrivent les fonctionnalités TAPI 2,2 que vous pouvez utiliser pour implémenter des contrôles de centre d’appels :</span><span class="sxs-lookup"><span data-stu-id="f0506-106">The following topics describe the TAPI 2.2 features that you can use to implement call center controls:</span></span>

-   [<span data-ttu-id="f0506-107">Modélisation d’un centre d’appels</span><span class="sxs-lookup"><span data-stu-id="f0506-107">Modeling of a Call Center</span></span>](modeling-of-a-call-center.md)
-   [<span data-ttu-id="f0506-108">Stations</span><span class="sxs-lookup"><span data-stu-id="f0506-108">Stations</span></span>](stations.md)
-   [<span data-ttu-id="f0506-109">Numérotation prédictive</span><span class="sxs-lookup"><span data-stu-id="f0506-109">Predictive Dialing</span></span>](predictive-dialing.md)
-   [<span data-ttu-id="f0506-110">Appels aux files d’attente et points de route</span><span class="sxs-lookup"><span data-stu-id="f0506-110">Call Queues and Route Points</span></span>](call-queues-and-route-points.md)
-   [<span data-ttu-id="f0506-111">Surveillance et contrôle de l’agent ACD</span><span class="sxs-lookup"><span data-stu-id="f0506-111">ACD Agent Monitoring and Control</span></span>](acd-agent-monitoring-and-control.md)
-   [<span data-ttu-id="f0506-112">Contrôle de l’état de la station</span><span class="sxs-lookup"><span data-stu-id="f0506-112">Station Status Control</span></span>](station-status-control.md)
-   [<span data-ttu-id="f0506-113">Contrôle de l’état de la station</span><span class="sxs-lookup"><span data-stu-id="f0506-113">Station Status Control</span></span>](station-status-control.md)
-   [<span data-ttu-id="f0506-114">Minuterie de l’état d’appel</span><span class="sxs-lookup"><span data-stu-id="f0506-114">Call State Timer</span></span>](call-state-timer.md)
-   [<span data-ttu-id="f0506-115">Minuteurs d’événements de média</span><span class="sxs-lookup"><span data-stu-id="f0506-115">Media Event Timers</span></span>](media-event-timers.md)

<span data-ttu-id="f0506-116">TAPI 3. x est l’API préférée de l’écriture d’applications de l’agent ACD.</span><span class="sxs-lookup"><span data-stu-id="f0506-116">TAPI 3.x is the preferred API of writing ACD Agent applications.</span></span> <span data-ttu-id="f0506-117">Pour plus d’informations sur l’utilisation de ces interfaces et méthodes, consultez la section [contrôles du centre d’appels](./about-call-center-controls.md) .</span><span class="sxs-lookup"><span data-stu-id="f0506-117">Please see the [Call Center Controls](./about-call-center-controls.md) section for information on using these interfaces and methods.</span></span> <span data-ttu-id="f0506-118">Toutefois, TAPI 2,2 reste utilisable pour les suites d’applications ACD complètes, si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="f0506-118">However, TAPI 2.2 remains usable for full ACD application suites if desired.</span></span>

 

 
