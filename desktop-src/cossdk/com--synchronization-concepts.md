---
description: En règle générale, la synchronisation n’est pas requise lorsque vous avez un thread cloisonné (STA, Single-Threaded Apartment) car le cloisonnement fournit la synchronisation pour vous.
ms.assetid: a05de040-0115-44aa-80e2-55eff2ec894d
title: Concepts de synchronisation COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eaca81050e67c76e3de6ad4845543b9230d2a24
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748877"
---
# <a name="com-synchronization-concepts"></a><span data-ttu-id="ced6e-103">Concepts de synchronisation COM+</span><span class="sxs-lookup"><span data-stu-id="ced6e-103">COM+ Synchronization Concepts</span></span>

<span data-ttu-id="ced6e-104">En règle générale, la synchronisation n’est pas requise lorsque vous avez un thread cloisonné (STA, Single-Threaded Apartment) car le cloisonnement fournit la synchronisation pour vous.</span><span class="sxs-lookup"><span data-stu-id="ced6e-104">Generally, synchronization is not required when you have a single-threaded apartment (STA) because the apartment provides the synchronization for you.</span></span> <span data-ttu-id="ced6e-105">La synchronisation devient importante lorsque vous avez un cloisonnement multithread (MTA) et un objet à thread libre.</span><span class="sxs-lookup"><span data-stu-id="ced6e-105">Synchronization becomes important when you have a multithreaded apartment (MTA) and a free-threaded object.</span></span> <span data-ttu-id="ced6e-106">Dans le passé, les objets à thread libre devaient gérer le verrouillage.</span><span class="sxs-lookup"><span data-stu-id="ced6e-106">In the past, free-threaded objects have had to handle locking.</span></span> <span data-ttu-id="ced6e-107">Vous pouvez éliminer la nécessité d’utiliser le verrouillage en définissant l’attribut de synchronisation d’un composant.</span><span class="sxs-lookup"><span data-stu-id="ced6e-107">You can eliminate the need to use locking by setting the synchronization attribute for a component.</span></span>

<span data-ttu-id="ced6e-108">La synchronisation a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="ced6e-108">Synchronization has the following properties:</span></span>

-   <span data-ttu-id="ced6e-109">Permet à un appelant d’entrer le composant à la fois.</span><span class="sxs-lookup"><span data-stu-id="ced6e-109">Allows one caller to enter the component at a time.</span></span>
-   <span data-ttu-id="ced6e-110">Interdit le passage d’un processus à un autre.</span><span class="sxs-lookup"><span data-stu-id="ced6e-110">Prohibits flow across process or across computer.</span></span>
-   <span data-ttu-id="ced6e-111">Passe du composant au composant au sein d’un processus.</span><span class="sxs-lookup"><span data-stu-id="ced6e-111">Flows from component to component within a process.</span></span>
-   <span data-ttu-id="ced6e-112">Autorise la réentrance à partir du même appelant.</span><span class="sxs-lookup"><span data-stu-id="ced6e-112">Allows reentrancy from the same caller.</span></span>

<span data-ttu-id="ced6e-113">Contrairement aux cloisonnements, les activités couvrent les contextes de plusieurs processus et hôtes.</span><span class="sxs-lookup"><span data-stu-id="ced6e-113">Unlike apartments, activities span contexts from multiple processes and hosts.</span></span> <span data-ttu-id="ced6e-114">La synchronisation détermine l’activité qui contiendra un objet.</span><span class="sxs-lookup"><span data-stu-id="ced6e-114">Synchronization determines which activity will contain an object.</span></span> <span data-ttu-id="ced6e-115">Les objets peuvent résider dans l’une des activités suivantes :</span><span class="sxs-lookup"><span data-stu-id="ced6e-115">Objects can reside in any of the following activities:</span></span>

-   <span data-ttu-id="ced6e-116">Activité du créateur</span><span class="sxs-lookup"><span data-stu-id="ced6e-116">Creator's activity</span></span>
-   <span data-ttu-id="ced6e-117">Nouvelle activité</span><span class="sxs-lookup"><span data-stu-id="ced6e-117">New activity</span></span>
-   <span data-ttu-id="ced6e-118">Aucune activité</span><span class="sxs-lookup"><span data-stu-id="ced6e-118">No activity</span></span>

<span data-ttu-id="ced6e-119">COM+ garantit la concurrence par une série de verrous pour chaque activité.</span><span class="sxs-lookup"><span data-stu-id="ced6e-119">COM+ ensures concurrency by a series of locks for each activity.</span></span> <span data-ttu-id="ced6e-120">Si un appelant tente d’entrer dans un composant COM+ synchronisé qui est déjà utilisé par un autre appelant, l’appel est bloqué jusqu’à ce que le verrou soit libéré.</span><span class="sxs-lookup"><span data-stu-id="ced6e-120">If a caller tries to enter a COM+ synchronized component that is already being used by another caller, the call is blocked until the lock is released.</span></span> <span data-ttu-id="ced6e-121">Ce comportement de blocage n’expire pas et ne peut pas être configuré pour expirer. Si le verrou n’est pas utilisé, le verrou est acquis et l’appel est traité.</span><span class="sxs-lookup"><span data-stu-id="ced6e-121">This blocking behavior will not time out and cannot be configured to time out. If the lock is not in use, the lock is acquired and the call is processed.</span></span> <span data-ttu-id="ced6e-122">Une fois l’exécution terminée, le verrou est libéré pour l’appelant suivant.</span><span class="sxs-lookup"><span data-stu-id="ced6e-122">After completing, the lock is released for the next caller.</span></span> <span data-ttu-id="ced6e-123">Pour éviter les verrous mortels, COM+ gère l’accès à tous les objets entre les activités par une série imbriquée d’appels chaînés sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="ced6e-123">To prevent deadlock, COM+ manages access to all objects across activities by a nested series of calls chained throughout the network.</span></span>

<span data-ttu-id="ced6e-124">COM+ fournit les paramètres de synchronisation suivants :</span><span class="sxs-lookup"><span data-stu-id="ced6e-124">COM+ provides the following synchronization settings:</span></span>

-   <span data-ttu-id="ced6e-125">Désactivé</span><span class="sxs-lookup"><span data-stu-id="ced6e-125">Disabled</span></span>
-   <span data-ttu-id="ced6e-126">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="ced6e-126">Not Supported</span></span>
-   <span data-ttu-id="ced6e-127">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="ced6e-127">Supported</span></span>
-   <span data-ttu-id="ced6e-128">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ced6e-128">Required</span></span>
-   <span data-ttu-id="ced6e-129">Nouveau requis</span><span class="sxs-lookup"><span data-stu-id="ced6e-129">Requires New</span></span>

> [!Note]  
> <span data-ttu-id="ced6e-130">Certains paramètres de synchronisation fonctionnent conjointement avec d’autres paramètres de composant COM+.</span><span class="sxs-lookup"><span data-stu-id="ced6e-130">Some synchronization settings work in conjunction with other COM+ component settings.</span></span> <span data-ttu-id="ced6e-131">Par exemple, la synchronisation est requise si le service [d’activation juste-à-temps (JIT) com+](com--just-in-time-activation.md) est activé.</span><span class="sxs-lookup"><span data-stu-id="ced6e-131">For example, synchronization is required if the [COM+ just-in-time (JIT) activation](com--just-in-time-activation.md) service is enabled.</span></span> <span data-ttu-id="ced6e-132">JIT est requis si vous activez des transactions ; par conséquent, le [traitement des transactions](com--transactions.md) com+ requiert également une synchronisation.</span><span class="sxs-lookup"><span data-stu-id="ced6e-132">JIT is required if you enable transactions; therefore, COM+ [transaction processing](com--transactions.md) requires synchronization as well.</span></span> <span data-ttu-id="ced6e-133">Ainsi, les classes avec le paramètre de JIT = true doivent également avoir la valeur Synchronization = Required ou Synchronization = RequiresNew.</span><span class="sxs-lookup"><span data-stu-id="ced6e-133">So, classes with the setting of JIT=True must also have the setting of either Synchronization=Required or Synchronization=RequiresNew.</span></span>

 

<span data-ttu-id="ced6e-134">Pour obtenir des instructions sur la définition des options de synchronisation à l’aide de l’outil d’administration Services de composants, consultez [définition de l’attribut de synchronisation](setting-the-synchronization-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="ced6e-134">For instructions about setting synchronization options by using the Component Services administrative tool, see [Setting the Synchronization Attribute](setting-the-synchronization-attribute.md).</span></span>

<span data-ttu-id="ced6e-135">Pour obtenir plus d’informations sur l’utilisation de la bibliothèque d’administration COM+ pour définir les options de synchronisation, consultez automatisation de l' [administration com+](automating-com--administration.md).</span><span class="sxs-lookup"><span data-stu-id="ced6e-135">To obtain more information on using the COM+ Administration Library to set synchronization options, see [Automating COM+ Administration](automating-com--administration.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ced6e-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ced6e-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ced6e-137">Tâches de synchronisation COM+</span><span class="sxs-lookup"><span data-stu-id="ced6e-137">COM+ Synchronization Tasks</span></span>](com--synchronization-tasks.md)
</dt> </dl>

 

 



