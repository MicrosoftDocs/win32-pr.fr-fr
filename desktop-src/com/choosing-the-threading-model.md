---
title: Choix du modèle de thread
description: Choix du modèle de thread
ms.assetid: e8a0286d-1831-454f-8549-1957fd794809
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2f0fdcd327bf05c0019a03ad171d41c1f1d95a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380341"
---
# <a name="choosing-the-threading-model"></a><span data-ttu-id="90f2b-103">Choix du modèle de thread</span><span class="sxs-lookup"><span data-stu-id="90f2b-103">Choosing the Threading Model</span></span>

<span data-ttu-id="90f2b-104">Le choix du modèle de thread pour un objet dépend de la fonction de l’objet.</span><span class="sxs-lookup"><span data-stu-id="90f2b-104">Choosing the threading model for an object depends on the object's function.</span></span> <span data-ttu-id="90f2b-105">Un objet qui effectue des e/s étendues peut prendre en charge le thread libre pour fournir une réponse maximale aux clients en autorisant les appels d’interface pendant la latence d’e/s.</span><span class="sxs-lookup"><span data-stu-id="90f2b-105">An object that does extensive I/O might support free-threading to provide maximum response to clients by allowing interface calls during I/O latency.</span></span> <span data-ttu-id="90f2b-106">En revanche, un objet qui interagit avec l’utilisateur peut prendre en charge le thread cloisonné pour synchroniser les appels COM entrants avec ses opérations de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="90f2b-106">On the other hand, an object that interacts with the user might support apartment threading to synchronize incoming COM calls with its window operations.</span></span>

<span data-ttu-id="90f2b-107">Il est plus facile de prendre en charge le thread cloisonné dans des Apartments à thread unique, car COM assure la synchronisation par appel.</span><span class="sxs-lookup"><span data-stu-id="90f2b-107">It is easier to support apartment threading in single-threaded apartments because COM provides synchronization on a per-call basis.</span></span> <span data-ttu-id="90f2b-108">La prise en charge des threads libres est plus difficile, car l’objet doit implémenter la synchronisation. Toutefois, la réponse aux clients peut être meilleure car la synchronisation peut être implémentée pour des sections de code plus petites.</span><span class="sxs-lookup"><span data-stu-id="90f2b-108">Supporting free-threading is more difficult because the object must implement synchronization; however, response to clients may be better because synchronization can be implemented for smaller sections of code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90f2b-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="90f2b-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90f2b-110">Accès aux interfaces à travers les Apartments</span><span class="sxs-lookup"><span data-stu-id="90f2b-110">Accessing Interfaces Across Apartments</span></span>](accessing-interfaces-across-apartments.md)
</dt> <dt>

[<span data-ttu-id="90f2b-111">Apartments (cloisonnés) multithread</span><span class="sxs-lookup"><span data-stu-id="90f2b-111">Multithreaded Apartments</span></span>](multithreaded-apartments.md)
</dt> <dt>

[<span data-ttu-id="90f2b-112">Problèmes liés aux threads du serveur in-process</span><span class="sxs-lookup"><span data-stu-id="90f2b-112">In-Process Server Threading Issues</span></span>](in-process-server-threading-issues.md)
</dt> <dt>

[<span data-ttu-id="90f2b-113">Processus, threads et Apartments</span><span class="sxs-lookup"><span data-stu-id="90f2b-113">Processes, Threads, and Apartments</span></span>](processes--threads--and-apartments.md)
</dt> <dt>

[<span data-ttu-id="90f2b-114">Communication monothread et multithread</span><span class="sxs-lookup"><span data-stu-id="90f2b-114">Single-Threaded and Multithreaded Communication</span></span>](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[<span data-ttu-id="90f2b-115">Apartments (cloisonnés) à thread unique</span><span class="sxs-lookup"><span data-stu-id="90f2b-115">Single-Threaded Apartments</span></span>](single-threaded-apartments.md)
</dt> </dl>

 

 




