---
description: Un programme de service contient du code exécutable pour un ou plusieurs services.
ms.assetid: 697db543-6149-46ac-add3-c8c6ca3aadbe
title: Programmes de service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b5e78574f46549956325bc19ffb6d51f4a114ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868186"
---
# <a name="service-programs"></a><span data-ttu-id="42e81-103">Programmes de service</span><span class="sxs-lookup"><span data-stu-id="42e81-103">Service Programs</span></span>

<span data-ttu-id="42e81-104">Un *programme de service* contient du code exécutable pour un ou plusieurs services.</span><span class="sxs-lookup"><span data-stu-id="42e81-104">A *service program* contains executable code for one or more services.</span></span> <span data-ttu-id="42e81-105">Un programme de service créé avec le processus de type SERVICE Win32 de type SERVICE \_ \_ \_ contient le code pour un seul service.</span><span class="sxs-lookup"><span data-stu-id="42e81-105">A service program created with the type SERVICE\_WIN32\_OWN\_PROCESS contains the code for only one service.</span></span> <span data-ttu-id="42e81-106">Un programme de service créé avec le \_ \_ processus de partage de type service Win32 \_ contient du code pour plusieurs services, ce qui leur permet de partager du code.</span><span class="sxs-lookup"><span data-stu-id="42e81-106">A service program created with the type SERVICE\_WIN32\_SHARE\_PROCESS contains code for more than one service, enabling them to share code.</span></span> <span data-ttu-id="42e81-107">Un exemple de programme de service qui effectue cette opération est le processus hôte de service générique, Svchost.exe, qui héberge des services Windows internes.</span><span class="sxs-lookup"><span data-stu-id="42e81-107">An example of a service program that does this is the generic service host process, Svchost.exe, which hosts internal Windows services.</span></span> <span data-ttu-id="42e81-108">Notez que Svchost.exe est réservée à une utilisation par le système d’exploitation et qu’il ne doit pas être utilisé par des services non-Windows.</span><span class="sxs-lookup"><span data-stu-id="42e81-108">Note that Svchost.exe is reserved for use by the operating system and should not be used by non-Windows services.</span></span> <span data-ttu-id="42e81-109">Au lieu de cela, les développeurs doivent implémenter leurs propres programmes d’hébergement de service.</span><span class="sxs-lookup"><span data-stu-id="42e81-109">Instead, developers should implement their own service hosting programs.</span></span>

<span data-ttu-id="42e81-110">Un programme de service peut être configuré pour s’exécuter dans le contexte d’un compte d’utilisateur à partir du domaine intégré (local), principal ou approuvé.</span><span class="sxs-lookup"><span data-stu-id="42e81-110">A service program can be configured to execute in the context of a user account from either the built-in (local), primary, or trusted domain.</span></span> <span data-ttu-id="42e81-111">Il peut également être configuré pour s’exécuter dans un [compte d’utilisateur de service](service-user-accounts.md)spécial.</span><span class="sxs-lookup"><span data-stu-id="42e81-111">It can also be configured to run in a special [service user account](service-user-accounts.md).</span></span>

<span data-ttu-id="42e81-112">Les rubriques suivantes décrivent les exigences d’interface du [Gestionnaire de contrôle des services](service-control-manager.md) (SCM) qu’un programme de service doit inclure :</span><span class="sxs-lookup"><span data-stu-id="42e81-112">The following topics describe the interface requirements of the [service control manager](service-control-manager.md) (SCM) that a service program must include:</span></span>

-   [<span data-ttu-id="42e81-113">Point d’entrée de service</span><span class="sxs-lookup"><span data-stu-id="42e81-113">Service Entry Point</span></span>](service-entry-point.md)
-   [<span data-ttu-id="42e81-114">Fonction de service ServiceMain</span><span class="sxs-lookup"><span data-stu-id="42e81-114">Service ServiceMain Function</span></span>](service-servicemain-function.md)
-   [<span data-ttu-id="42e81-115">Fonction du gestionnaire de contrôle des services</span><span class="sxs-lookup"><span data-stu-id="42e81-115">Service Control Handler Function</span></span>](service-control-handler-function.md)

<span data-ttu-id="42e81-116">Ces rubriques ne s’appliquent pas aux services de pilote.</span><span class="sxs-lookup"><span data-stu-id="42e81-116">These topics do not apply to driver services.</span></span> <span data-ttu-id="42e81-117">Pour connaître les exigences en matière d’interface des services de pilote, consultez le kit de pilotes Windows (WDK).</span><span class="sxs-lookup"><span data-stu-id="42e81-117">For interface requirements of driver services, see the Windows Driver Kit (WDK).</span></span>

<span data-ttu-id="42e81-118">Un service s’exécute en tant que processus en arrière-plan qui peut affecter les performances du système, la réactivité, l’efficacité énergétique et la sécurité.</span><span class="sxs-lookup"><span data-stu-id="42e81-118">A service runs as a background process that can affect system performance, responsiveness, energy efficiency, and security.</span></span> <span data-ttu-id="42e81-119">Pour obtenir des instructions sur l’optimisation des services, consultez [développement de processus d’arrière-plan efficaces pour Windows](/windows-hardware/drivers/kernel/implementing-power-management).</span><span class="sxs-lookup"><span data-stu-id="42e81-119">For service optimization guidelines, see [Developing Efficient Background Processes for Windows](/windows-hardware/drivers/kernel/implementing-power-management).</span></span> <span data-ttu-id="42e81-120">Les rubriques suivantes décrivent d’autres considérations relatives à la programmation :</span><span class="sxs-lookup"><span data-stu-id="42e81-120">The following topics describe additional programming considerations:</span></span>

-   [<span data-ttu-id="42e81-121">Transitions d’état de service</span><span class="sxs-lookup"><span data-stu-id="42e81-121">Service State Transitions</span></span>](service-status-transitions.md)
-   [<span data-ttu-id="42e81-122">Réception d’événements dans un service</span><span class="sxs-lookup"><span data-stu-id="42e81-122">Receiving Events in a Service</span></span>](receiving-events-in-a-service.md)
-   [<span data-ttu-id="42e81-123">Services multithread</span><span class="sxs-lookup"><span data-stu-id="42e81-123">Multithreaded Services</span></span>](multithreaded-services.md)
-   [<span data-ttu-id="42e81-124">Services et Registre</span><span class="sxs-lookup"><span data-stu-id="42e81-124">Services and the Registry</span></span>](services-and-the-registry.md)
-   [<span data-ttu-id="42e81-125">Services et lecteurs redirigés</span><span class="sxs-lookup"><span data-stu-id="42e81-125">Services and Redirected Drives</span></span>](services-and-redirected-drives.md)
-   [<span data-ttu-id="42e81-126">Événements de déclencheur de service</span><span class="sxs-lookup"><span data-stu-id="42e81-126">Service Trigger Events</span></span>](service-trigger-events.md)

<span data-ttu-id="42e81-127">Notez que si le programme de service fonctionne comme un serveur RPC, il doit utiliser des points de terminaison dynamiques et une authentification mutuelle.</span><span class="sxs-lookup"><span data-stu-id="42e81-127">Note that if the service program functions as an RPC server, it should use dynamic endpoints and mutual authentication.</span></span>

 

 
