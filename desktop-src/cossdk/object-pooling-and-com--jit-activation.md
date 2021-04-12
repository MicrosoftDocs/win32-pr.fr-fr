---
description: L’activation JIT COM+ fait essentiellement un compromis entre les clients gourmands et les serveurs gourmands afin d’obtenir des performances optimales. Les clients sont en mesure de conserver les références d’objets, tandis que les serveurs peuvent mieux gérer l’utilisation de la mémoire.
ms.assetid: 125d39f5-af38-4a87-a649-2f77a3e77c27
title: Mise en pool d’objets et activation JIT COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8042d838aaaae62eace6f61a8fe1aa820e17d079
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393223"
---
# <a name="object-pooling-and-com-jit-activation"></a><span data-ttu-id="97120-104">Mise en pool d’objets et activation JIT COM+</span><span class="sxs-lookup"><span data-stu-id="97120-104">Object Pooling and COM+ JIT Activation</span></span>

<span data-ttu-id="97120-105">L’activation JIT COM+ fait essentiellement un compromis entre les clients gourmands et les serveurs gourmands afin d’obtenir des performances optimales.</span><span class="sxs-lookup"><span data-stu-id="97120-105">COM+ JIT activation essentially strikes a compromise between greedy clients and greedy servers for the sake of getting optimal performance.</span></span> <span data-ttu-id="97120-106">Les clients sont en mesure de conserver les références d’objets, tandis que les serveurs peuvent mieux gérer l’utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="97120-106">Clients get to keep object references, while servers can more closely manage memory utilization.</span></span>

<span data-ttu-id="97120-107">Vous pouvez affiner cette amélioration en utilisant le [regroupement d’objets com+](com--object-pooling.md).</span><span class="sxs-lookup"><span data-stu-id="97120-107">You can refine this further by using [COM+ Object Pooling](com--object-pooling.md).</span></span> <span data-ttu-id="97120-108">En regroupant les objets qui sont activés juste-à-temps, vous pouvez dédier une certaine quantité de mémoire pour contenir un certain nombre d’objets actifs en mémoire, prêts à être réutilisés immédiatement.</span><span class="sxs-lookup"><span data-stu-id="97120-108">By pooling objects that are JIT activated, you can dedicate a certain amount of memory to hold a certain number of objects active in memory, ready for immediate reuse.</span></span> <span data-ttu-id="97120-109">Cela est plus clair lorsque les objets sont coûteux à créer, comme dans le cas où ils détiennent plusieurs ressources.</span><span class="sxs-lookup"><span data-stu-id="97120-109">This makes the most sense when objects are expensive to create, as in the case where they hold multiple resources.</span></span>

<span data-ttu-id="97120-110">En regroupant les objets activés juste-à-temps de cette manière, vous pouvez bénéficier des avantages suivants :</span><span class="sxs-lookup"><span data-stu-id="97120-110">Pooling JIT-activated objects in this manner, you can achieve the following benefits:</span></span>

-   <span data-ttu-id="97120-111">Délais de réactivation d’objets accélérés.</span><span class="sxs-lookup"><span data-stu-id="97120-111">Greatly accelerated object reactivation times.</span></span>
-   <span data-ttu-id="97120-112">Réutilisation des ressources coûteuses que les objets détiennent.</span><span class="sxs-lookup"><span data-stu-id="97120-112">Reuse of any expensive resources the objects are holding.</span></span>
-   <span data-ttu-id="97120-113">Administration plus précise de la mémoire et de l’utilisation des ressources pour les objets regroupés.</span><span class="sxs-lookup"><span data-stu-id="97120-113">More precise governing of memory and resource use for the pooled objects.</span></span>
-   <span data-ttu-id="97120-114">Rétention de la flexibilité administrative afin que votre application puisse être mise à l’échelle pour utiliser les ressources disponibles et s’adapter à l’évolution des besoins en performances.</span><span class="sxs-lookup"><span data-stu-id="97120-114">Retention of administrative flexibility so that your application can scale to use available resources and adapt to changing performance requirements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97120-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="97120-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97120-116">Concepts d’activation juste-à-temps de COM+</span><span class="sxs-lookup"><span data-stu-id="97120-116">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="97120-117">Mise en pool d’objets COM+</span><span class="sxs-lookup"><span data-stu-id="97120-117">COM+ Object Pooling</span></span>](com--object-pooling.md)
</dt> <dt>

[<span data-ttu-id="97120-118">Activation de l’activation JIT pour un composant</span><span class="sxs-lookup"><span data-stu-id="97120-118">Enabling JIT Activation for a Component</span></span>](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[<span data-ttu-id="97120-119">Transactions et activation JIT COM+</span><span class="sxs-lookup"><span data-stu-id="97120-119">Transactions and COM+ JIT Activation</span></span>](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



