---
description: Dans le cas des pionniers du traitement des transactions, l’acronyme ACID est un acronyme atomique, cohérent, isolé et durable.
ms.assetid: 857d145c-710d-4097-8ed6-df11e8d52228
title: Propriétés ACID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2e725cae75b4aa80d25f2959d474e8baa05f70
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110567"
---
# <a name="acid-properties"></a><span data-ttu-id="efd8d-103">Propriétés ACID</span><span class="sxs-lookup"><span data-stu-id="efd8d-103">ACID Properties</span></span>

<span data-ttu-id="efd8d-104">Dans le cas des pionniers du traitement des transactions, l’acronyme ACID est un acronyme atomique, cohérent, isolé et durable.</span><span class="sxs-lookup"><span data-stu-id="efd8d-104">Coined by transaction processing pioneers, the acronym ACID stands for atomic, consistent, isolated, and durable.</span></span> <span data-ttu-id="efd8d-105">Pour garantir un comportement prévisible, toutes les transactions doivent posséder ces propriétés de base, ce qui renforce le rôle des transactions stratégiques en tant que propositions « tout ou rien ».</span><span class="sxs-lookup"><span data-stu-id="efd8d-105">To ensure predictable behavior, all transactions must possess these basic properties, reinforcing the role of mission-critical transactions as all-or-none propositions.</span></span>

<span data-ttu-id="efd8d-106">La liste suivante contient une définition et une description de chaque propriété ACID :</span><span class="sxs-lookup"><span data-stu-id="efd8d-106">The following list contains a definition and a description of each ACID property:</span></span>

<dl> <dt>

<span data-ttu-id="efd8d-107"><span id="Atomic"></span><span id="atomic"></span><span id="ATOMIC"></span>Atomique</span><span class="sxs-lookup"><span data-stu-id="efd8d-107"><span id="Atomic"></span><span id="atomic"></span><span id="ATOMIC"></span>Atomic</span></span>
</dt> <dd>

<span data-ttu-id="efd8d-108">Une transaction doit être exécutée une seule fois et doit être atomique : soit la totalité du travail est effectuée, soit aucune d’entre elles n’est.</span><span class="sxs-lookup"><span data-stu-id="efd8d-108">A transaction must execute exactly once and must be atomic—either all of the work is done or none of it is.</span></span> <span data-ttu-id="efd8d-109">Les opérations au sein d’une transaction partagent généralement une intention commune et sont interdépendantes.</span><span class="sxs-lookup"><span data-stu-id="efd8d-109">Operations within a transaction usually share a common intent and are interdependent.</span></span> <span data-ttu-id="efd8d-110">En effectuant uniquement un sous-ensemble de ces opérations, le système peut compromettre l’intention globale de la transaction.</span><span class="sxs-lookup"><span data-stu-id="efd8d-110">By performing only a subset of these operations, the system could compromise the overall intent of the transaction.</span></span> <span data-ttu-id="efd8d-111">L’atomicité élimine le risque de traiter uniquement un sous-ensemble d’opérations.</span><span class="sxs-lookup"><span data-stu-id="efd8d-111">Atomicity eliminates the chance of processing only a subset of operations.</span></span>

</dd> <dt>

<span data-ttu-id="efd8d-112"><span id="Consistent"></span><span id="consistent"></span><span id="CONSISTENT"></span>Conforme</span><span class="sxs-lookup"><span data-stu-id="efd8d-112"><span id="Consistent"></span><span id="consistent"></span><span id="CONSISTENT"></span>Consistent</span></span>
</dt> <dd>

<span data-ttu-id="efd8d-113">Une transaction doit préserver la cohérence des données, transformant un état cohérent des données en un autre État de données cohérent.</span><span class="sxs-lookup"><span data-stu-id="efd8d-113">A transaction must preserve the consistency of data, transforming one consistent state of data into another consistent state of data.</span></span> <span data-ttu-id="efd8d-114">Une grande partie de la responsabilité du maintien de la cohérence incombe au développeur de l’application.</span><span class="sxs-lookup"><span data-stu-id="efd8d-114">Much of the responsibility for maintaining consistency falls to the application developer.</span></span>

</dd> <dt>

<span data-ttu-id="efd8d-115"><span id="Isolated"></span><span id="isolated"></span><span id="ISOLATED"></span>Concerné</span><span class="sxs-lookup"><span data-stu-id="efd8d-115"><span id="Isolated"></span><span id="isolated"></span><span id="ISOLATED"></span>Isolated</span></span>
</dt> <dd>

<span data-ttu-id="efd8d-116">Une transaction doit être une unité d’isolation, ce qui signifie que les transactions simultanées doivent se comporter comme si chacune était la seule transaction en cours d’exécution dans le système.</span><span class="sxs-lookup"><span data-stu-id="efd8d-116">A transaction must be a unit of isolation, which means that concurrent transactions should behave as if each were the only transaction running in the system.</span></span> <span data-ttu-id="efd8d-117">Étant donné qu’un degré élevé d’isolation peut limiter le nombre de transactions simultanées, certaines applications réduisent le niveau d’isolation dans Exchange pour un meilleur débit.</span><span class="sxs-lookup"><span data-stu-id="efd8d-117">Because a high degree of isolation can limit the number of concurrent transactions, some applications reduce the isolation level in exchange for better throughput.</span></span> <span data-ttu-id="efd8d-118">Pour plus d’informations, consultez [Configuration des niveaux d’isolation des transactions](configuring-transaction-isolation-levels.md) .</span><span class="sxs-lookup"><span data-stu-id="efd8d-118">See [Configuring Transaction Isolation Levels](configuring-transaction-isolation-levels.md) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="efd8d-119"><span id="Durable"></span><span id="durable"></span><span id="DURABLE"></span>Durable</span><span class="sxs-lookup"><span data-stu-id="efd8d-119"><span id="Durable"></span><span id="durable"></span><span id="DURABLE"></span>Durable</span></span>
</dt> <dd>

<span data-ttu-id="efd8d-120">Une transaction doit être récupérable et doit donc avoir une durabilité.</span><span class="sxs-lookup"><span data-stu-id="efd8d-120">A transaction must be recoverable and therefore must have durability.</span></span> <span data-ttu-id="efd8d-121">Si une transaction est validée, le système garantit que ses mises à jour peuvent être conservées même si l’ordinateur se bloque immédiatement après la validation.</span><span class="sxs-lookup"><span data-stu-id="efd8d-121">If a transaction commits, the system guarantees that its updates can persist even if the computer crashes immediately after the commit.</span></span> <span data-ttu-id="efd8d-122">La journalisation spécialisée permet à la procédure de redémarrage du système d’effectuer les opérations non terminées requises par la transaction, ce qui rend la transaction durable.</span><span class="sxs-lookup"><span data-stu-id="efd8d-122">Specialized logging allows the system's restart procedure to complete unfinished operations required by the transaction, making the transaction durable.</span></span>

</dd> </dl>

 

 



