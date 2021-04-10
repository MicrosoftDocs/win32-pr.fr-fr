---
title: Single-Threaded et communication multithread
description: Single-Threaded et communication multithread
ms.assetid: 8d3a855c-b52d-48bb-9fdf-efbf8005c374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6470ac398e6ae1c8a645fb076fbbf509d58b579
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309693"
---
# <a name="single-threaded-and-multithreaded-communication"></a><span data-ttu-id="97368-103">Single-Threaded et communication multithread</span><span class="sxs-lookup"><span data-stu-id="97368-103">Single-Threaded and Multithreaded Communication</span></span>

<span data-ttu-id="97368-104">Un client ou un serveur qui prend en charge les cloisonnements à thread unique et multithread aura un cloisonnement multithread, contenant tous les threads initialisés en tant que threads libres et un ou plusieurs Apartments (cloisonnés) à thread unique.</span><span class="sxs-lookup"><span data-stu-id="97368-104">A client or server that supports both single-threaded and multithreaded apartments will have one multithreaded apartment, containing all threads initialized as free-threaded, and one or more single-threaded apartments.</span></span> <span data-ttu-id="97368-105">Les pointeurs d’interface doivent être marshalés entre les Apartments, mais ils peuvent être utilisés sans marshaling dans un cloisonnement.</span><span class="sxs-lookup"><span data-stu-id="97368-105">Interface pointers must be marshaled between apartments but can be used without marshaling within an apartment.</span></span> <span data-ttu-id="97368-106">Les appels aux objets dans un cloisonnement à thread unique sont synchronisés par COM.</span><span class="sxs-lookup"><span data-stu-id="97368-106">Calls to objects in a single-threaded apartment will be synchronized by COM.</span></span> <span data-ttu-id="97368-107">Les appels aux objets dans le cloisonnement multithread ne sont pas synchronisés par COM.</span><span class="sxs-lookup"><span data-stu-id="97368-107">Calls to objects in the multithreaded apartment will not be synchronized by COM.</span></span>

<span data-ttu-id="97368-108">Toutes les informations sur les cloisonnements à thread unique s’appliquent aux threads marqués comme modèle cloisonné, et toutes les informations sur les Apartments (multithreads) s’appliquent à tous les threads marqués comme étant libres de threads.</span><span class="sxs-lookup"><span data-stu-id="97368-108">All of the information on single-threaded apartments applies to the threads marked as apartment model, and all of the information on multithreaded apartments applies to all of the threads marked as free-threaded.</span></span> <span data-ttu-id="97368-109">Les règles de thread cloisonné s’appliquent à la communication entre cloisonnements, ce qui nécessite que les pointeurs d’interface soient marshalés entre les cloisonnements avec des appels à [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) et [**CoGetInterfaceAndReleaseStream**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream), comme décrit dans les [cloisonnements à thread unique](single-threaded-apartments.md).</span><span class="sxs-lookup"><span data-stu-id="97368-109">Apartment threading rules apply to inter-apartment communication, requiring that interface pointers be marshaled between apartments with calls to [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) and [**CoGetInterfaceAndReleaseStream**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream), as described in [Single-Threaded Apartments](single-threaded-apartments.md).</span></span>

> [!Note]  
> <span data-ttu-id="97368-110">Certaines considérations spéciales s’appliquent lors du traitement des serveurs in-process.</span><span class="sxs-lookup"><span data-stu-id="97368-110">Some special considerations apply when dealing with in-process servers.</span></span> <span data-ttu-id="97368-111">Pour plus d’informations, consultez [problèmes de Threading du serveur in-process](in-process-server-threading-issues.md).</span><span class="sxs-lookup"><span data-stu-id="97368-111">For more information, see [In-Process Server Threading Issues](in-process-server-threading-issues.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="97368-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="97368-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97368-113">Accès aux interfaces à travers les Apartments</span><span class="sxs-lookup"><span data-stu-id="97368-113">Accessing Interfaces Across Apartments</span></span>](accessing-interfaces-across-apartments.md)
</dt> <dt>

[<span data-ttu-id="97368-114">Choix du modèle de thread</span><span class="sxs-lookup"><span data-stu-id="97368-114">Choosing the Threading Model</span></span>](choosing-the-threading-model.md)
</dt> <dt>

[<span data-ttu-id="97368-115">Apartments (cloisonnés) multithread</span><span class="sxs-lookup"><span data-stu-id="97368-115">Multithreaded Apartments</span></span>](multithreaded-apartments.md)
</dt> <dt>

[<span data-ttu-id="97368-116">Problèmes liés aux threads du serveur in-process</span><span class="sxs-lookup"><span data-stu-id="97368-116">In-Process Server Threading Issues</span></span>](in-process-server-threading-issues.md)
</dt> <dt>

[<span data-ttu-id="97368-117">Processus, threads et Apartments</span><span class="sxs-lookup"><span data-stu-id="97368-117">Processes, Threads, and Apartments</span></span>](processes--threads--and-apartments.md)
</dt> <dt>

[<span data-ttu-id="97368-118">Apartments (cloisonnés) à thread unique</span><span class="sxs-lookup"><span data-stu-id="97368-118">Single-Threaded Apartments</span></span>](single-threaded-apartments.md)
</dt> </dl>

 

 




