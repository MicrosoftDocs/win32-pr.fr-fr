---
description: Implémentez le multitâche, planifiez les priorités et travaillez avec les processus, les threads, les pools de threads, les objets de travail et les fibres. Utilisez la planification en mode utilisateur pour planifier les threads.
ms.assetid: 6bff848c-0c55-41e7-aff1-84c6b21a1b8d
title: Processus et threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f469806a5f803910a773c78c9847d0f7b0ecc7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519700"
---
# <a name="processes-and-threads"></a><span data-ttu-id="10452-104">Processus et threads</span><span class="sxs-lookup"><span data-stu-id="10452-104">Processes and Threads</span></span>

<span data-ttu-id="10452-105">Une application se compose d’un ou plusieurs processus.</span><span class="sxs-lookup"><span data-stu-id="10452-105">An application consists of one or more processes.</span></span> <span data-ttu-id="10452-106">Un *processus*, en termes simples, est un programme en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="10452-106">A *process*, in the simplest terms, is an executing program.</span></span> <span data-ttu-id="10452-107">Un ou plusieurs threads s’exécutent dans le contexte du processus.</span><span class="sxs-lookup"><span data-stu-id="10452-107">One or more threads run in the context of the process.</span></span> <span data-ttu-id="10452-108">Un *thread* est l’unité de base à laquelle le système d’exploitation alloue du temps processeur.</span><span class="sxs-lookup"><span data-stu-id="10452-108">A *thread* is the basic unit to which the operating system allocates processor time.</span></span> <span data-ttu-id="10452-109">Un thread peut exécuter n’importe quelle partie du code de processus, y compris les composants en cours d’exécution par un autre thread.</span><span class="sxs-lookup"><span data-stu-id="10452-109">A thread can execute any part of the process code, including parts currently being executed by another thread.</span></span>

<span data-ttu-id="10452-110">Un *objet de traitement* permet de gérer des groupes de processus en tant qu’unité.</span><span class="sxs-lookup"><span data-stu-id="10452-110">A *job object* allows groups of processes to be managed as a unit.</span></span> <span data-ttu-id="10452-111">Les objets de traitement sont des objets namable, sécurisables et partageables qui contrôlent les attributs des processus qui leur sont associés.</span><span class="sxs-lookup"><span data-stu-id="10452-111">Job objects are namable, securable, sharable objects that control attributes of the processes associated with them.</span></span> <span data-ttu-id="10452-112">Les opérations effectuées sur l’objet de traitement affectent tous les processus associés à l’objet de traitement.</span><span class="sxs-lookup"><span data-stu-id="10452-112">Operations performed on the job object affect all processes associated with the job object.</span></span>

<span data-ttu-id="10452-113">Un *pool de threads* est une collection de threads de travail qui exécutent efficacement des rappels asynchrones pour le compte de l’application.</span><span class="sxs-lookup"><span data-stu-id="10452-113">A *thread pool* is a collection of worker threads that efficiently execute asynchronous callbacks on behalf of the application.</span></span> <span data-ttu-id="10452-114">Le pool de threads est principalement utilisé pour réduire le nombre de threads d’application et assurer la gestion des threads de travail.</span><span class="sxs-lookup"><span data-stu-id="10452-114">The thread pool is primarily used to reduce the number of application threads and provide management of the worker threads.</span></span>

<span data-ttu-id="10452-115">Une *fibre* est une unité d’exécution qui doit être planifiée manuellement par l’application.</span><span class="sxs-lookup"><span data-stu-id="10452-115">A *fiber* is a unit of execution that must be manually scheduled by the application.</span></span> <span data-ttu-id="10452-116">Les fibres s’exécutent dans le contexte des threads qui les planifient.</span><span class="sxs-lookup"><span data-stu-id="10452-116">Fibers run in the context of the threads that schedule them.</span></span>

<span data-ttu-id="10452-117">La *planification en mode utilisateur* (UMS) est un mécanisme léger que les applications peuvent utiliser pour planifier leurs propres threads.</span><span class="sxs-lookup"><span data-stu-id="10452-117">*User-mode scheduling* (UMS) is a lightweight mechanism that applications can use to schedule their own threads.</span></span> <span data-ttu-id="10452-118">Les threads UMS diffèrent des [fibres](fibers.md) en ce que chaque thread UMS a son propre contexte de thread au lieu de partager le contexte de thread d’un thread unique.</span><span class="sxs-lookup"><span data-stu-id="10452-118">UMS threads differ from [fibers](fibers.md) in that each UMS thread has its own thread context instead of sharing the thread context of a single thread.</span></span>

-   [<span data-ttu-id="10452-119">Nouveautés des processus et des threads</span><span class="sxs-lookup"><span data-stu-id="10452-119">What's New in Processes and Threads</span></span>](what-s-new-in-processes-and-threads.md)
-   [<span data-ttu-id="10452-120">À propos des processus et des threads</span><span class="sxs-lookup"><span data-stu-id="10452-120">About Processes and Threads</span></span>](about-processes-and-threads.md)
-   [<span data-ttu-id="10452-121">Utilisation des processus et des threads</span><span class="sxs-lookup"><span data-stu-id="10452-121">Using Processes and Threads</span></span>](using-processes-and-threads.md)
-   [<span data-ttu-id="10452-122">Référence des processus et des threads</span><span class="sxs-lookup"><span data-stu-id="10452-122">Process and Thread Reference</span></span>](process-and-thread-reference.md)

 

 



