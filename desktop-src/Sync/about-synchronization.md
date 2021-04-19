---
description: Pour synchroniser l’accès à une ressource, utilisez l’un des objets de synchronisation dans l’une des fonctions Wait.
ms.assetid: 0930bf12-6d5f-4f2c-914d-53e6e862d3bd
title: À propos de la synchronisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ad53dc8c309d8ec55f37cef5f78839348071477
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106537045"
---
# <a name="about-synchronization"></a><span data-ttu-id="5b675-103">À propos de la synchronisation</span><span class="sxs-lookup"><span data-stu-id="5b675-103">About Synchronization</span></span>

<span data-ttu-id="5b675-104">Pour synchroniser l’accès à une ressource, utilisez l’un des [objets de synchronisation](synchronization-objects.md) dans l’une des [fonctions Wait](wait-functions.md).</span><span class="sxs-lookup"><span data-stu-id="5b675-104">To synchronize access to a resource, use one of the [synchronization objects](synchronization-objects.md) in one of the [wait functions](wait-functions.md).</span></span> <span data-ttu-id="5b675-105">L’état d’un objet de synchronisation est *signalé* ou non *signalé*.</span><span class="sxs-lookup"><span data-stu-id="5b675-105">The state of a synchronization object is either *signaled* or *nonsignaled*.</span></span> <span data-ttu-id="5b675-106">Les fonctions Wait permettent à un thread de bloquer sa propre exécution jusqu’à ce qu’un objet non signalé spécifié soit défini sur l’état signalé.</span><span class="sxs-lookup"><span data-stu-id="5b675-106">The wait functions allow a thread to block its own execution until a specified nonsignaled object is set to the signaled state.</span></span> <span data-ttu-id="5b675-107">Pour plus d’informations, consultez [synchronisation entre processus](interprocess-synchronization.md).</span><span class="sxs-lookup"><span data-stu-id="5b675-107">For more information, see [Interprocess Synchronization](interprocess-synchronization.md).</span></span>

<span data-ttu-id="5b675-108">Les autres mécanismes de synchronisation sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="5b675-108">The following are other synchronization mechanisms:</span></span>

-   [<span data-ttu-id="5b675-109">entrée et sortie avec chevauchement</span><span class="sxs-lookup"><span data-stu-id="5b675-109">overlapped input and output</span></span>](synchronization-and-overlapped-input-and-output.md)
-   [<span data-ttu-id="5b675-110">appels de procédure asynchrone</span><span class="sxs-lookup"><span data-stu-id="5b675-110">asynchronous procedure calls</span></span>](asynchronous-procedure-calls.md)
-   [<span data-ttu-id="5b675-111">objets de section critique</span><span class="sxs-lookup"><span data-stu-id="5b675-111">critical section objects</span></span>](critical-section-objects.md)
-   [<span data-ttu-id="5b675-112">variables de condition</span><span class="sxs-lookup"><span data-stu-id="5b675-112">condition variables</span></span>](condition-variables.md)
-   [<span data-ttu-id="5b675-113">verrous de lecture/écriture Slim</span><span class="sxs-lookup"><span data-stu-id="5b675-113">slim reader/writer locks</span></span>](slim-reader-writer--srw--locks.md)
-   [<span data-ttu-id="5b675-114">initialisation unique</span><span class="sxs-lookup"><span data-stu-id="5b675-114">one-time initialization</span></span>](one-time-initialization.md)
-   [<span data-ttu-id="5b675-115">accès aux variables verrouillées</span><span class="sxs-lookup"><span data-stu-id="5b675-115">interlocked variable access</span></span>](interlocked-variable-access.md)
-   [<span data-ttu-id="5b675-116">listes liées de façon isolée</span><span class="sxs-lookup"><span data-stu-id="5b675-116">interlocked singly linked lists</span></span>](interlocked-singly-linked-lists.md)
-   [<span data-ttu-id="5b675-117">files d’attente du minuteur</span><span class="sxs-lookup"><span data-stu-id="5b675-117">timer queues</span></span>](timer-queues.md)
-   <span data-ttu-id="5b675-118">la macro [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier)</span><span class="sxs-lookup"><span data-stu-id="5b675-118">the [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) macro</span></span>

<span data-ttu-id="5b675-119">Pour plus d’informations sur la synchronisation, consultez [problèmes liés à la synchronisation et aux multiprocesseurs](synchronization-and-multiprocessor-issues.md).</span><span class="sxs-lookup"><span data-stu-id="5b675-119">For additional information on synchronization, see [Synchronization and Multiprocessor Issues](synchronization-and-multiprocessor-issues.md).</span></span>

 

 
