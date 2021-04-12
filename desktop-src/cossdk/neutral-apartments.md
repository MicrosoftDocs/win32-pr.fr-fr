---
description: COM+ introduit des cloisonnements neutres pour simplifier la programmation dans les environnements multithread. Le cloisonnement neutre est le modèle préféré pour COM+ pour les composants sans interface utilisateur.
ms.assetid: 679742af-7c04-4b0e-822a-a43e1aafa936
title: Cloisonnements neutres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ac3bdff2670e4f99ad94af20278eaca6a38861e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393068"
---
# <a name="neutral-apartments"></a><span data-ttu-id="9760d-104">Cloisonnements neutres</span><span class="sxs-lookup"><span data-stu-id="9760d-104">Neutral Apartments</span></span>

<span data-ttu-id="9760d-105">COM+ introduit des cloisonnements neutres pour simplifier la programmation dans les environnements multithread.</span><span class="sxs-lookup"><span data-stu-id="9760d-105">COM+ introduces neutral apartments to simplify programming in multithreaded environments.</span></span> <span data-ttu-id="9760d-106">Le cloisonnement neutre est le modèle préféré pour COM+ pour les composants sans interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9760d-106">The neutral apartment is the preferred model for COM+ for components with no user interface.</span></span>

<span data-ttu-id="9760d-107">Par le passé, pour éviter les goulots d’étranglement, les développeurs COM+ nécessitant une évolutivité du serveur devaient implémenter des composants à threads libres. Toutefois, les modèles de threads libres sont difficiles à implémenter, car ils doivent gérer l’accès au verrouillage.</span><span class="sxs-lookup"><span data-stu-id="9760d-107">In the past, to prevent bottlenecks, COM+ developers requiring server scalability had to implement free-threaded components; however, free-threading models are complicated to implement because they must deal with interlocking access.</span></span> <span data-ttu-id="9760d-108">Dans les cloisonnements neutres, les objets suivent les instructions pour les cloisonnements multithread, mais peuvent s’exécuter sur n’importe quel type de thread.</span><span class="sxs-lookup"><span data-stu-id="9760d-108">In neutral apartments, objects follow the guidelines for multithreaded apartments but can execute on any kind of thread.</span></span> <span data-ttu-id="9760d-109">Quand un thread s’exécute dans un cloisonnement neutre, le contexte de l’objet est reçu sans provoquer de changement de thread.</span><span class="sxs-lookup"><span data-stu-id="9760d-109">When a thread is running in a neutral apartment, the object's context is received without causing a thread switch.</span></span>

<span data-ttu-id="9760d-110">Chaque processus ne peut avoir qu’un seul cloisonnement neutre.</span><span class="sxs-lookup"><span data-stu-id="9760d-110">Each process can have only one neutral apartment.</span></span> <span data-ttu-id="9760d-111">Pour sélectionner un cloisonnement neutre, utilisez le paramètre de Registre suivant :</span><span class="sxs-lookup"><span data-stu-id="9760d-111">To select a neutral apartment, use the following registry setting:</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer32
         ThreadingModel = Neutral
```

<span data-ttu-id="9760d-112">Les composants qui ont des interfaces utilisateur doivent continuer à utiliser des Apartments à thread unique comme modèle préféré.</span><span class="sxs-lookup"><span data-stu-id="9760d-112">Components that have user interfaces should continue to use single-threaded apartments as the preferred model.</span></span> <span data-ttu-id="9760d-113">Pour sélectionner un cloisonnement à thread unique, utilisez le paramètre de Registre suivant :</span><span class="sxs-lookup"><span data-stu-id="9760d-113">To select a single-threaded apartment, use the following registry setting:</span></span>

<span data-ttu-id="9760d-114">**ThreadingModel** = cloisonnement</span><span class="sxs-lookup"><span data-stu-id="9760d-114">**ThreadingModel** = Apartment</span></span>

 

 



