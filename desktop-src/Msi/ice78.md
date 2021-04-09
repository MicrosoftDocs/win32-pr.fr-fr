---
description: ICE78 vérifie que la table AdvtUISequence n’existe pas ou est vide. Cela est nécessaire, car aucune interface utilisateur n’est autorisée pendant la publicité.
ms.assetid: 8ed1c68f-331d-42f9-80df-bdcb42962482
title: ICE78
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8993a0a03b0f70bf2d99511782bc9b7d259d4c9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113851"
---
# <a name="ice78"></a><span data-ttu-id="69152-104">ICE78</span><span class="sxs-lookup"><span data-stu-id="69152-104">ICE78</span></span>

<span data-ttu-id="69152-105">ICE78 vérifie que la [table AdvtUISequence](advtuisequence-table.md) n’existe pas ou est vide.</span><span class="sxs-lookup"><span data-stu-id="69152-105">ICE78 verifies that the [AdvtUISequence table](advtuisequence-table.md) either does not exist or is empty.</span></span> <span data-ttu-id="69152-106">Cela est nécessaire, car aucune interface utilisateur n’est autorisée pendant la publicité.</span><span class="sxs-lookup"><span data-stu-id="69152-106">This is required because no user interface is allowed during advertising.</span></span>

## <a name="result"></a><span data-ttu-id="69152-107">Résultats</span><span class="sxs-lookup"><span data-stu-id="69152-107">Result</span></span>

<span data-ttu-id="69152-108">ICE78 publie une erreur si la table AdvtUISequence existe et n’est pas vide.</span><span class="sxs-lookup"><span data-stu-id="69152-108">ICE78 posts an error if the AdvtUISequence table exists and is not empty.</span></span>

## <a name="example"></a><span data-ttu-id="69152-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="69152-109">Example</span></span>

<span data-ttu-id="69152-110">ICE78 signale l’erreur suivante pour l’exemple :</span><span class="sxs-lookup"><span data-stu-id="69152-110">ICE78 reports the following error for the example:</span></span>

<span data-ttu-id="69152-111">Action’action1 'trouvée dans la table AdvtUISequence.</span><span class="sxs-lookup"><span data-stu-id="69152-111">Action 'Action1' found in AdvtUISequence table.</span></span> <span data-ttu-id="69152-112">Aucune interface utilisateur n’est autorisée pendant la publicité.</span><span class="sxs-lookup"><span data-stu-id="69152-112">No UI is allowed during advertising.</span></span> <span data-ttu-id="69152-113">Par conséquent, la table AdvtUISequence doit être vide ou absente.</span><span class="sxs-lookup"><span data-stu-id="69152-113">Therefore AdvtUISequence table must be empty or not present.</span></span>

<span data-ttu-id="69152-114">[Table AdvtUISequence](advtuisequence-table.md)(partielle)</span><span class="sxs-lookup"><span data-stu-id="69152-114">[AdvtUISequence table](advtuisequence-table.md)(partial)</span></span>



| <span data-ttu-id="69152-115">Action</span><span class="sxs-lookup"><span data-stu-id="69152-115">Action</span></span>  | <span data-ttu-id="69152-116">Condition</span><span class="sxs-lookup"><span data-stu-id="69152-116">Condition</span></span> | <span data-ttu-id="69152-117">Séquence</span><span class="sxs-lookup"><span data-stu-id="69152-117">Sequence</span></span> |
|---------|-----------|----------|
| <span data-ttu-id="69152-118">Action1</span><span class="sxs-lookup"><span data-stu-id="69152-118">Action1</span></span> | <span data-ttu-id="69152-119">TRUE</span><span class="sxs-lookup"><span data-stu-id="69152-119">TRUE</span></span>      | <span data-ttu-id="69152-120">1</span><span class="sxs-lookup"><span data-stu-id="69152-120">1</span></span>        |



 

<span data-ttu-id="69152-121">Pour corriger l’erreur, supprimez « action1 » de la table ou supprimez la table.</span><span class="sxs-lookup"><span data-stu-id="69152-121">To fix the error, either remove "Action1" from the table, or remove the table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="69152-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="69152-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69152-123">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="69152-123">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



