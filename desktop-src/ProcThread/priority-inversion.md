---
description: Une inversion de priorité se produit lorsque deux threads ou plus avec des priorités différentes sont en conflit pour être planifiés.
ms.assetid: 1cb2f3c9-4641-40d8-892c-768abaf6affb
title: Inversion de priorité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79a0f4c9d57000e9e81429ee882e70dc14f63ae4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319158"
---
# <a name="priority-inversion"></a><span data-ttu-id="fe59d-103">Inversion de priorité</span><span class="sxs-lookup"><span data-stu-id="fe59d-103">Priority Inversion</span></span>

<span data-ttu-id="fe59d-104">Une inversion de priorité se produit lorsque deux threads ou plus avec des priorités différentes sont en conflit pour être planifiés.</span><span class="sxs-lookup"><span data-stu-id="fe59d-104">Priority inversion occurs when two or more threads with different priorities are in contention to be scheduled.</span></span> <span data-ttu-id="fe59d-105">Prenons un cas simple avec trois threads : thread 1, thread 2 et thread 3.</span><span class="sxs-lookup"><span data-stu-id="fe59d-105">Consider a simple case with three threads: thread 1, thread 2, and thread 3.</span></span> <span data-ttu-id="fe59d-106">Le thread 1 est prioritaire et est prêt à être planifié.</span><span class="sxs-lookup"><span data-stu-id="fe59d-106">Thread 1 is high priority and becomes ready to be scheduled.</span></span> <span data-ttu-id="fe59d-107">Thread 2, un thread de faible priorité, exécute du code dans une section critique.</span><span class="sxs-lookup"><span data-stu-id="fe59d-107">Thread 2, a low-priority thread, is executing code in a critical section.</span></span> <span data-ttu-id="fe59d-108">Thread 1, le thread de priorité élevée, commence à attendre une ressource partagée du thread 2.</span><span class="sxs-lookup"><span data-stu-id="fe59d-108">Thread 1, the high-priority thread, begins waiting for a shared resource from thread 2.</span></span> <span data-ttu-id="fe59d-109">Le thread 3 a une priorité moyenne.</span><span class="sxs-lookup"><span data-stu-id="fe59d-109">Thread 3 has medium priority.</span></span> <span data-ttu-id="fe59d-110">Le thread 3 reçoit tout le temps processeur, car le thread de priorité élevée (thread 1) attend des ressources partagées du thread de faible priorité (thread 2).</span><span class="sxs-lookup"><span data-stu-id="fe59d-110">Thread 3 receives all the processor time, because the high-priority thread (thread 1) is waiting for shared resources from the low-priority thread (thread 2).</span></span> <span data-ttu-id="fe59d-111">Le thread 2 ne laisse pas la section critique, car il n’a pas la priorité la plus élevée et n’est pas planifié.</span><span class="sxs-lookup"><span data-stu-id="fe59d-111">Thread 2 will not leave the critical section, because it does not have the highest priority and will not be scheduled.</span></span>

<span data-ttu-id="fe59d-112">Le planificateur résout ce problème en renforçant de façon aléatoire la priorité des threads prêts (dans ce cas, les détenteurs de verrou basse priorité).</span><span class="sxs-lookup"><span data-stu-id="fe59d-112">The scheduler solves this problem by randomly boosting the priority of the ready threads (in this case, the low priority lock-holders).</span></span> <span data-ttu-id="fe59d-113">Les threads de faible priorité s’exécutent suffisamment longtemps pour quitter la section critique et le thread de priorité élevée peut entrer dans la section critique.</span><span class="sxs-lookup"><span data-stu-id="fe59d-113">The low priority threads run long enough to exit the critical section, and the high-priority thread can enter the critical section.</span></span> <span data-ttu-id="fe59d-114">Si le thread de faible priorité ne dispose pas de suffisamment de temps processeur pour quitter la section critique la première fois, il obtiendra une autre chance au cours de la prochaine période de planification.</span><span class="sxs-lookup"><span data-stu-id="fe59d-114">If the low-priority thread does not get enough CPU time to exit the critical section the first time, it will get another chance during the next round of scheduling.</span></span>

 

 



