---
description: Un système d’exploitation multitâche divise le temps processeur disponible entre les processus ou les threads qui en ont besoin.
ms.assetid: ac45bef6-f078-40ac-95f4-06bd61ff46c4
title: Multitâche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d06c1d8d44f397f06923c793971bcb20f35b2b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319162"
---
# <a name="multitasking"></a><span data-ttu-id="cbecf-103">Multitâche</span><span class="sxs-lookup"><span data-stu-id="cbecf-103">Multitasking</span></span>

<span data-ttu-id="cbecf-104">Un système d’exploitation multitâche divise le temps processeur disponible entre les processus ou les threads qui en ont besoin.</span><span class="sxs-lookup"><span data-stu-id="cbecf-104">A multitasking operating system divides the available processor time among the processes or threads that need it.</span></span> <span data-ttu-id="cbecf-105">Le système est conçu pour le multitâche préemptif. il alloue une tranche de *temps* processeur à chaque thread qu’il exécute.</span><span class="sxs-lookup"><span data-stu-id="cbecf-105">The system is designed for preemptive multitasking; it allocates a processor *time slice* to each thread it executes.</span></span> <span data-ttu-id="cbecf-106">Le thread en cours d’exécution est suspendu lorsque sa tranche de temps est écoulée, ce qui permet l’exécution d’un autre thread.</span><span class="sxs-lookup"><span data-stu-id="cbecf-106">The currently executing thread is suspended when its time slice elapses, allowing another thread to run.</span></span> <span data-ttu-id="cbecf-107">Lorsque le système passe d’un thread à un autre, il enregistre le contexte du thread préempté et restaure le contexte enregistré du thread suivant dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="cbecf-107">When the system switches from one thread to another, it saves the context of the preempted thread and restores the saved context of the next thread in the queue.</span></span>

<span data-ttu-id="cbecf-108">La longueur de chaque tranche de temps dépend du système d’exploitation et du processeur.</span><span class="sxs-lookup"><span data-stu-id="cbecf-108">The length of the time slice depends on the operating system and the processor.</span></span> <span data-ttu-id="cbecf-109">Étant donné que chaque tranche de temps est petite (environ 20 millisecondes), plusieurs threads semblent s’exécuter en même temps.</span><span class="sxs-lookup"><span data-stu-id="cbecf-109">Because each time slice is small (approximately 20 milliseconds), multiple threads appear to be executing at the same time.</span></span> <span data-ttu-id="cbecf-110">C’est le cas sur les systèmes multiprocesseurs, où les threads exécutables sont distribués entre les processeurs disponibles.</span><span class="sxs-lookup"><span data-stu-id="cbecf-110">This is actually the case on multiprocessor systems, where the executable threads are distributed among the available processors.</span></span> <span data-ttu-id="cbecf-111">Toutefois, vous devez faire attention lorsque vous utilisez plusieurs threads dans une application, car les performances du système peuvent diminuer si le nombre de threads est trop important.</span><span class="sxs-lookup"><span data-stu-id="cbecf-111">However, you must use caution when using multiple threads in an application, because system performance can decrease if there are too many threads.</span></span>

<span data-ttu-id="cbecf-112">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="cbecf-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="cbecf-113">Avantages de la multitâche</span><span class="sxs-lookup"><span data-stu-id="cbecf-113">Advantages of Multitasking</span></span>](advantages-of-multitasking.md)
-   [<span data-ttu-id="cbecf-114">Quand utiliser le multitâche</span><span class="sxs-lookup"><span data-stu-id="cbecf-114">When to Use Multitasking</span></span>](when-to-use-multitasking.md)
-   [<span data-ttu-id="cbecf-115">Considérations relatives au multitâche</span><span class="sxs-lookup"><span data-stu-id="cbecf-115">Multitasking Considerations</span></span>](multitasking-considerations.md)

 

 



