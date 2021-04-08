---
title: Pourquoi Active Directory Domain Services utilise ce modèle de réplication
description: Cette rubrique explique les raisons du système de forme libre utilisé par Active Directory Domain Services pour un modèle de réplication.
ms.assetid: 202df900-6d03-4aa8-9099-016238059ef4
ms.tgt_platform: multiple
keywords:
- Active Directory du modèle de réplication, avantages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538fe291a04953d373ff3cd45cbd4693d3dafab4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839257"
---
# <a name="why-active-directory-domain-services-uses-this-replication-model"></a><span data-ttu-id="c8775-104">Pourquoi Active Directory Domain Services utilise ce modèle de réplication</span><span class="sxs-lookup"><span data-stu-id="c8775-104">Why Active Directory Domain Services Uses This Replication Model</span></span>

<span data-ttu-id="c8775-105">Cette rubrique explique les raisons du système de forme libre utilisé par Active Directory Domain Services pour un modèle de réplication.</span><span class="sxs-lookup"><span data-stu-id="c8775-105">This topic explains the reasons for the free-form system used by Active Directory Domain Services for a replication model.</span></span>

<span data-ttu-id="c8775-106">Les Active Directory Domain Services sont un système de forme libre pour les raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="c8775-106">Active Directory Domain Services are a free-form system for the following reasons:</span></span>

-   <span data-ttu-id="c8775-107">Les clients ont besoin d’une solution hautement distribuée dans laquelle des parties de l’annuaire peuvent être réparties sur leurs réseaux et administrées localement.</span><span class="sxs-lookup"><span data-stu-id="c8775-107">Customers require a highly distributed solution in which parts of the directory can be spread across their networks and administered locally.</span></span>
-   <span data-ttu-id="c8775-108">Les clients de grande taille se développent souvent en millions d’objets, de centaines ou de milliers de réplicas, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="c8775-108">Large customers often grow to millions of objects, hundreds or thousands of replicas, or both.</span></span>
-   <span data-ttu-id="c8775-109">De nombreux réseaux clients fournissent uniquement une connectivité intermittente à certains emplacements. par exemple, les plates-formes de forages pétroliers distantes et les navires en mer, le système doit être tolérant aux opérations partiellement connectées ou déconnectées.</span><span class="sxs-lookup"><span data-stu-id="c8775-109">Many customer networks provide only intermittent connectivity to some locations; for example, remote oil drilling platforms and ships at sea, so the system must be tolerant of partly connected or disconnected operations.</span></span>

<span data-ttu-id="c8775-110">Il n’existe aucun moyen de garantir la connaissance complète de l’état actuel ou futur d’un système distribué, car la connaissance des changements d’État doit être propagée et la propagation prend du temps, au cours de laquelle des modifications d’État supplémentaires peuvent se produire.</span><span class="sxs-lookup"><span data-stu-id="c8775-110">There is no way to guarantee complete awareness of the current or future state of a distributed system because knowledge of state changes must be propagated and propagation takes time, during which more state changes may occur.</span></span>

<span data-ttu-id="c8775-111">Les systèmes étroitement couplés gèrent l’incertitude en tentant de l’éliminer.</span><span class="sxs-lookup"><span data-stu-id="c8775-111">Tightly coupled systems handle uncertainty by attempting to eliminate it.</span></span> <span data-ttu-id="c8775-112">Cela s’effectue par le biais de contraintes sur les mises à jour, nécessitant la disponibilité de tous les nœuds ou de la majorité des nœuds avant que les mises à jour puissent être effectuées, en utilisant des schémas de verrouillage distribués ou une simple maîtrise pour les ressources critiques, en limitant la connexion de tous les nœuds, ou une combinaison de ces techniques.</span><span class="sxs-lookup"><span data-stu-id="c8775-112">This is accomplished through constraints on updates, requiring all nodes or some majority of nodes to be available before updates can be performed, using distributed locking schemes or single-mastering for critical resources, constraining all nodes to be well-connected, or some combination of these techniques.</span></span> <span data-ttu-id="c8775-113">Plus les nœuds informatiques sont étroitement couplés dans un système distribué, plus la limite de mise à l’échelle est faible.</span><span class="sxs-lookup"><span data-stu-id="c8775-113">The more tightly coupled the computing nodes in a distributed system are, the lower the scaling limit.</span></span>

<span data-ttu-id="c8775-114">Les systèmes de forme libre gèrent l’incertitude en le tolérant.</span><span class="sxs-lookup"><span data-stu-id="c8775-114">Free-form systems handle uncertainty by tolerating it.</span></span> <span data-ttu-id="c8775-115">Un système de forme libre permet aux nœuds d’avoir des vues différentes de l’état général du système et fournit des algorithmes pour la résolution des conflits.</span><span class="sxs-lookup"><span data-stu-id="c8775-115">A free-form system enables the nodes to have differing views of the overall system state and provides algorithms for resolving conflicts.</span></span>

<span data-ttu-id="c8775-116">Les solutions fortement couplées ont été rejetées comme inappropriées pour les Active Directory Domain Services en raison des exigences liées à l’administration locale, au fonctionnement déconnecté et à l’évolutivité vers un très grand nombre de nœuds.</span><span class="sxs-lookup"><span data-stu-id="c8775-116">Tightly coupled solutions were rejected as unsuitable for Active Directory Domain Services because of the requirements for local administration, disconnected operation, and scalability to very large numbers of nodes.</span></span> <span data-ttu-id="c8775-117">Le modèle faiblement couplé choisi, à compatibilité avec la cohérence multimaître avec la convergence, satisfait à toutes les exigences.</span><span class="sxs-lookup"><span data-stu-id="c8775-117">The loosely coupled model chosen, multi-master loose consistency with convergence, satisfies all requirements.</span></span>

 

 




