---
description: Isolation des erreurs et stratégie FailFast
ms.assetid: 219c417c-a8a1-49eb-bc5a-702a16994d66
title: Isolation des erreurs et stratégie FailFast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc097a6d45f10d4ef8a8d059b1376862edd785ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523431"
---
# <a name="fault-isolation-and-failfast-policy"></a><span data-ttu-id="b88c5-103">Isolation des erreurs et stratégie FailFast</span><span class="sxs-lookup"><span data-stu-id="b88c5-103">Fault Isolation and Failfast Policy</span></span>

<span data-ttu-id="b88c5-104">COM+ effectue une intégrité interne et des vérifications de cohérence étendues.</span><span class="sxs-lookup"><span data-stu-id="b88c5-104">COM+ performs extensive internal integrity and consistency checks.</span></span> <span data-ttu-id="b88c5-105">Si COM+ rencontre une condition d’erreur interne inattendue, il met immédiatement fin au processus.</span><span class="sxs-lookup"><span data-stu-id="b88c5-105">If COM+ encounters an unexpected internal error condition, it immediately terminates the process.</span></span> <span data-ttu-id="b88c5-106">Cette stratégie, appelée *FailFast*, facilite la contention des erreurs et aboutit à des systèmes plus fiables et fiables.</span><span class="sxs-lookup"><span data-stu-id="b88c5-106">This policy, called *failfast*, facilitates fault containment and results in more reliable and robust systems.</span></span>

<span data-ttu-id="b88c5-107">Prenons l’exemple d’un cas dans lequel COM+ détecte qu’une de ses structures de données est dans un état endommagé.</span><span class="sxs-lookup"><span data-stu-id="b88c5-107">Consider a case in which COM+ detects that one of its data structures is in a corrupted state.</span></span> <span data-ttu-id="b88c5-108">À ce stade, la cause et l’ampleur de l’endommagement sont inconnues et, malheureusement, COM+ ne peut pas indiquer le degré de propagation des dégâts.</span><span class="sxs-lookup"><span data-stu-id="b88c5-108">At this point, both the cause and the magnitude of the corruption are unknown and, unfortunately, COM+ cannot tell how far the damage has spread.</span></span> <span data-ttu-id="b88c5-109">Toutefois, même si COM+ est dans un état indéterminé, il ne s’exécute pas de manière isolée.</span><span class="sxs-lookup"><span data-stu-id="b88c5-109">However, even though COM+ is in an indeterminate state, it does not run in isolation.</span></span> <span data-ttu-id="b88c5-110">Comme les autres dll, il est hébergé dans un environnement de processus et partage un espace d’adressage unique avec l’exécutable principal du programme et de nombreuses autres dll.</span><span class="sxs-lookup"><span data-stu-id="b88c5-110">Like other DLLs, it is hosted in a process environment and shares a single address space with the main program executable and many other DLLs.</span></span> <span data-ttu-id="b88c5-111">Par conséquent, COM+ suppose que l’intégralité du processus a été endommagé et que le processus est immédiatement interrompu pour l’empêcher de diffuser des informations potentiellement endommagées vers d’autres processus ou, pire encore, d’autoriser la validation et la durabilité des données endommagées.</span><span class="sxs-lookup"><span data-stu-id="b88c5-111">Therefore, COM+ assumes that the entire process has been corrupted, and the process is immediately terminated to prevent it from spreading potentially corrupted information to other processes or, worse yet, from allowing corrupted data to be committed and made durable.</span></span>

<span data-ttu-id="b88c5-112">COM+ n’autorise pas les exceptions à se propager en dehors d’un contexte.</span><span class="sxs-lookup"><span data-stu-id="b88c5-112">COM+ does not allow exceptions to propagate outside of a context.</span></span> <span data-ttu-id="b88c5-113">Si une exception se produit lors de l’exécution dans un contexte COM+ et que l’application n’intercepte pas l’exception avant de retourner à partir du contexte, COM+ intercepte l’exception et met fin au processus.</span><span class="sxs-lookup"><span data-stu-id="b88c5-113">If an exception occurs while executing within a COM+ context and the application doesn't catch the exception before returning from the context, COM+ catches the exception and terminates the process.</span></span> <span data-ttu-id="b88c5-114">Dans ce cas, l’utilisation de la stratégie FailFast est basée sur l’hypothèse que l’exception a placé le processus dans un état indéterminé ; Il n’est pas possible de continuer le traitement.</span><span class="sxs-lookup"><span data-stu-id="b88c5-114">Using the failfast policy in this case is based on the assumption that the exception has put the process into an indeterminate state; it is not safe to continue processing.</span></span>

<span data-ttu-id="b88c5-115">En tant que développeur ou administrateur, vous devez examiner le journal des applications observateur d’événements pour plus d’informations sur les actions FailFast ou les erreurs d’application graves.</span><span class="sxs-lookup"><span data-stu-id="b88c5-115">As a developer or administrator, you should inspect the Event Viewer application log for details on any failfast action or serious application errors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b88c5-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b88c5-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b88c5-117">Recherche de la source d’une erreur</span><span class="sxs-lookup"><span data-stu-id="b88c5-117">Finding the Source of an Error</span></span>](finding-the-source-of-an-error.md)
</dt> <dt>

[<span data-ttu-id="b88c5-118">Modification des valeurs de retour par COM+</span><span class="sxs-lookup"><span data-stu-id="b88c5-118">How COM+ Modifies Return Values</span></span>](how-com--modifies-return-values.md)
</dt> <dt>

[<span data-ttu-id="b88c5-119">Interprétation des codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="b88c5-119">Interpreting Error Codes</span></span>](interpreting-error-codes.md)
</dt> <dt>

[<span data-ttu-id="b88c5-120">Stratégies de gestion des erreurs dans COM+</span><span class="sxs-lookup"><span data-stu-id="b88c5-120">Strategies for Handling Errors in COM+</span></span>](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[<span data-ttu-id="b88c5-121">Dépannage</span><span class="sxs-lookup"><span data-stu-id="b88c5-121">Troubleshooting</span></span>](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



