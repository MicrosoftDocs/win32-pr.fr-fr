---
description: En savoir plus sur la prise en charge des deltas PrintTicket. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 80fdc8f1-4fda-4102-9b27-16d9acb4d077
title: Prise en charge des deltas PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f72f82875d0207ed232f4db897c78295ce2ee0
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548777"
---
# <a name="supporting-printticket-deltas"></a><span data-ttu-id="dd753-105">Prise en charge des deltas PrintTicket</span><span class="sxs-lookup"><span data-stu-id="dd753-105">Supporting PrintTicket Deltas</span></span>

<span data-ttu-id="dd753-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="dd753-106">This topic is not current.</span></span> <span data-ttu-id="dd753-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="dd753-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="dd753-108">L’interface du fournisseur PrintTicket a des méthodes qui peuvent être utilisées pour apporter des modifications incrémentielles à un PrintTicket existant.</span><span class="sxs-lookup"><span data-stu-id="dd753-108">The PrintTicket Provider Interface has methods that can be used to make incremental changes to an existing PrintTicket.</span></span> <span data-ttu-id="dd753-109">Les modifications Incremental PrintTicket peuvent être spécifiées dans un PrintTicket partiel appelé « un Delta PrintTicket ».</span><span class="sxs-lookup"><span data-stu-id="dd753-109">The incremental PrintTicket changes can be specified in a partial PrintTicket that is known as a PrintTicket delta.</span></span> <span data-ttu-id="dd753-110">Un PrintTicket révisé est créé en fusionnant un Delta PrintTicket avec un PrintTicket existant.</span><span class="sxs-lookup"><span data-stu-id="dd753-110">A revised PrintTicket is created by merging a PrintTicket delta with an existing PrintTicket.</span></span> <span data-ttu-id="dd753-111">Pour plus d’informations sur les méthodes impliquant des deltas PrintTicket, consultez le document de l’interface de fournisseur PrintTicket à venir.</span><span class="sxs-lookup"><span data-stu-id="dd753-111">See the forthcoming PrintTicket Provider Interface document for more information about methods involving PrintTicket deltas.</span></span>

<span data-ttu-id="dd753-112">Lors du traitement d’un Delta PrintTicket, les étapes suivantes doivent être effectuées.</span><span class="sxs-lookup"><span data-stu-id="dd753-112">When a PrintTicket delta is processed, the following steps must be performed.</span></span>

1.  <span data-ttu-id="dd753-113">Identifiez les instances de fonctionnalité ou de ParameterInit qui sont communes à la fois à l’instance PrintTicket existante (le PrintTicket cible) et à l’écart PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="dd753-113">Identify Feature or ParameterInit instances that are common to both the existing PrintTicket (the target PrintTicket) and the PrintTicket delta.</span></span>

    -   <span data-ttu-id="dd753-114">Pour chaque fonctionnalité commune à la fois à la cible PrintTicket et au Delta PrintTicket, remplacez la fonctionnalité dans le PrintTicket cible par la fonctionnalité correspondante dans le delta PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="dd753-114">For each Feature common to both the target PrintTicket and the PrintTicket delta, replace the Feature in the target PrintTicket by the corresponding Feature in the PrintTicket delta.</span></span>

    -   <span data-ttu-id="dd753-115">Pour chaque ParameterInit commun à la fois à la cible PrintTicket et à l’écart PrintTicket, remplacez le ParameterInit dans le PrintTicket cible par le ParameterInit correspondant dans le delta PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="dd753-115">For each ParameterInit common to both the target PrintTicket and the PrintTicket delta, replace the ParameterInit in the target PrintTicket by the corresponding ParameterInit in the PrintTicket delta.</span></span>

2.  <span data-ttu-id="dd753-116">Copiez toutes les instances de fonctionnalité et ParameterInit restantes dans le delta PrintTicket dans le PrintTicket cible.</span><span class="sxs-lookup"><span data-stu-id="dd753-116">Copy all remaining Feature and ParameterInit instances in the PrintTicket delta to the target PrintTicket.</span></span>

3.  <span data-ttu-id="dd753-117">Si votre algorithme de résolution des conflits permet de spécifier des priorités dans le PrintTicket lui-même, vous pouvez choisir d’élever les priorités de la fonctionnalité et les instances ParameterInit nommées dans le delta PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="dd753-117">If your conflict resolution algorithm allows priorities to be specified in the PrintTicket itself, you may choose to elevate the priorities of the Feature and ParameterInit instances named in the PrintTicket delta.</span></span>

4.  <span data-ttu-id="dd753-118">Exécutez la validation PrintTicket comme décrit dans la liste de contrôle de [validation PrintTicket](printticket-validation-checklist.md).</span><span class="sxs-lookup"><span data-stu-id="dd753-118">Perform PrintTicket validation as described in [PrintTicket Validation Checklist](printticket-validation-checklist.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd753-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dd753-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd753-120">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="dd753-120">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



