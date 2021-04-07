---
title: Utilisation d’ADO pour la récupération de plages
description: Si un langage Automation est utilisé, les objets d’annuaire ActiveX (ADO) doivent être utilisés pour récupérer une plage de valeurs de propriété. Lorsque vous utilisez ADO pour la récupération de plages, il existe un problème qui doit être traité spécifiquement.
ms.assetid: ca06169d-7de7-4552-aa7d-e9427353e49e
ms.tgt_platform: multiple
keywords:
- Utilisation d’ADO pour l’ADSI de récupération de plages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb8950a71708bd9c824c90842f043808c897554
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671110"
---
# <a name="using-ado-for-range-retrieval"></a><span data-ttu-id="231ce-104">Utilisation d’ADO pour la récupération de plages</span><span class="sxs-lookup"><span data-stu-id="231ce-104">Using ADO for Range Retrieval</span></span>

<span data-ttu-id="231ce-105">Si un langage Automation est utilisé, les objets d’annuaire ActiveX (ADO) doivent être utilisés pour récupérer une plage de valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="231ce-105">If an automation language is used, the ActiveX Directory Objects (ADO) should be used to retrieve a range of property values.</span></span>

<span data-ttu-id="231ce-106">Lorsque vous utilisez ADO pour la récupération de plages, il existe un problème qui doit être traité spécifiquement.</span><span class="sxs-lookup"><span data-stu-id="231ce-106">When using ADO for range retrieval, there is one problem that must be specifically addressed.</span></span> <span data-ttu-id="231ce-107">Lors de l’interrogation du groupe final de valeurs de propriété, l’objet ADO récupère zéro objet, même s’il en reste.</span><span class="sxs-lookup"><span data-stu-id="231ce-107">When querying for the final group of property values, the ADO object will retrieve zero objects, even though more remain.</span></span> <span data-ttu-id="231ce-108">Pour récupérer les valeurs restantes, utilisez le caractère générique de plage « \* ».</span><span class="sxs-lookup"><span data-stu-id="231ce-108">To retrieve the remaining values, use the range wildcard '\*'.</span></span> <span data-ttu-id="231ce-109">Par exemple, si un groupe contient 150 membres, les valeurs de membre 0-100 peuvent être récupérées normalement à l’aide d’une récupération étendue.</span><span class="sxs-lookup"><span data-stu-id="231ce-109">For example, if a group contains 150 members, member values 0-100 can be retrieved normally using ranged retrieval.</span></span> <span data-ttu-id="231ce-110">Si la plage 101-200 est ensuite demandée, l’objet ADO ne retourne aucun objet.</span><span class="sxs-lookup"><span data-stu-id="231ce-110">If range 101-200 is then requested, the ADO object will return zero objects.</span></span> <span data-ttu-id="231ce-111">À ce stade, il est nécessaire de modifier la requête pour demander la plage 101- \* .</span><span class="sxs-lookup"><span data-stu-id="231ce-111">At this point, it is necessary to modify the query to request range 101-\*.</span></span> <span data-ttu-id="231ce-112">Cela permet de récupérer des valeurs comprises entre 101 et 150.</span><span class="sxs-lookup"><span data-stu-id="231ce-112">This will retrieve values from 101 to 150.</span></span> <span data-ttu-id="231ce-113">Pour plus d’informations et pour obtenir un exemple de code, consultez [exemple de code pour l’utilisation de pour récupérer des membres d’un groupe](example-code-for-using-ranging-to-retrieve-members-of-a-group.md).</span><span class="sxs-lookup"><span data-stu-id="231ce-113">For more information and a code example, see [Example Code for Using Ranging to Retrieve Members of a Group](example-code-for-using-ranging-to-retrieve-members-of-a-group.md).</span></span>

<span data-ttu-id="231ce-114">Pour plus d’informations sur l’utilisation d’ADO pour la récupération de plages, consultez :</span><span class="sxs-lookup"><span data-stu-id="231ce-114">For more information about using ADO for range retrieval, see:</span></span>

-   [<span data-ttu-id="231ce-115">Dialecte LDAP ADO</span><span class="sxs-lookup"><span data-stu-id="231ce-115">ADO LDAP Ranging Dialect</span></span>](ado-ldap-ranging-dialect.md)
-   [<span data-ttu-id="231ce-116">Dialecte SQL ADO</span><span class="sxs-lookup"><span data-stu-id="231ce-116">ADO SQL Ranging Dialect</span></span>](ado-sql-ranging-dialect.md)
-   [<span data-ttu-id="231ce-117">Exemple de code pour l’utilisation de permettant de récupérer des membres d’un groupe</span><span class="sxs-lookup"><span data-stu-id="231ce-117">Example Code for Using Ranging to Retrieve Members of a Group</span></span>](example-code-for-using-ranging-to-retrieve-members-of-a-group.md)

 

 




