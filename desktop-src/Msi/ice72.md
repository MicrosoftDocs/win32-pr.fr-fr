---
description: ICE72 vérifie que les actions personnalisées non intégrées ne sont pas utilisées dans la table AdvtExecuteSequence.
ms.assetid: b04227d5-5bd6-434a-860c-498d787a1f0a
title: ICE72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d9d8e1859ffd8123cc7aa3dc801c5484d28ccb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529378"
---
# <a name="ice72"></a><span data-ttu-id="24ce8-103">ICE72</span><span class="sxs-lookup"><span data-stu-id="24ce8-103">ICE72</span></span>

<span data-ttu-id="24ce8-104">ICE72 vérifie que les actions personnalisées non intégrées ne sont pas utilisées dans la [table AdvtExecuteSequence](advtexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="24ce8-104">ICE72 verifies that non-built-in custom actions are not used in the [AdvtExecuteSequence table](advtexecutesequence-table.md).</span></span> <span data-ttu-id="24ce8-105">Plus précisément, seules les actions personnalisées de type 19, de type 35 et de type 51 sont autorisées dans la table AdvtExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="24ce8-105">Specifically, only type 19, type 35, and type 51 custom actions are allowed in the AdvtExecuteSequence table.</span></span> <span data-ttu-id="24ce8-106">Si d’autres actions personnalisées sont utilisées, la publication peut ne pas se comporter comme prévu.</span><span class="sxs-lookup"><span data-stu-id="24ce8-106">If other custom actions are used, advertisement may not behave as expected.</span></span>

## <a name="result"></a><span data-ttu-id="24ce8-107">Résultats</span><span class="sxs-lookup"><span data-stu-id="24ce8-107">Result</span></span>

<span data-ttu-id="24ce8-108">ICE72 retourne une erreur si la table AdvExecuteSequence utilise des actions personnalisées autres que le type 35, le type 51 et le type 19.</span><span class="sxs-lookup"><span data-stu-id="24ce8-108">ICE72 returns an error if the AdvExecuteSequence table uses custom actions other than type 35, type 51, and type 19.</span></span>

## <a name="example"></a><span data-ttu-id="24ce8-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="24ce8-109">Example</span></span>

<span data-ttu-id="24ce8-110">ICE72 signale l’erreur suivante pour l’exemple ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="24ce8-110">ICE72 reports the following error for the example shown:</span></span>

``` syntax
Custom Action 'CA1' in the AdvtExecuteSequence table is not allowed. Only built-in custom actions are allowed.
```

<span data-ttu-id="24ce8-111">Pour corriger l’erreur, supprimez « CA1 » de la table AdvtExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="24ce8-111">To fix the error, remove 'CA1' from the AdvtExecuteSequence table.</span></span>

<span data-ttu-id="24ce8-112">[Table AdvtExecuteSequence](advtexecutesequence-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="24ce8-112">[AdvtExecuteSequence Table](advtexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="24ce8-113">Action</span><span class="sxs-lookup"><span data-stu-id="24ce8-113">Action</span></span> |
|--------|
| <span data-ttu-id="24ce8-114">AC1</span><span class="sxs-lookup"><span data-stu-id="24ce8-114">CA1</span></span>    |
| <span data-ttu-id="24ce8-115">CA35</span><span class="sxs-lookup"><span data-stu-id="24ce8-115">CA35</span></span>   |



 

<span data-ttu-id="24ce8-116">[Table CustomAction](customaction-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="24ce8-116">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="24ce8-117">Action</span><span class="sxs-lookup"><span data-stu-id="24ce8-117">Action</span></span> | <span data-ttu-id="24ce8-118">Type</span><span class="sxs-lookup"><span data-stu-id="24ce8-118">Type</span></span> |
|--------|------|
| <span data-ttu-id="24ce8-119">AC1</span><span class="sxs-lookup"><span data-stu-id="24ce8-119">CA1</span></span>    | <span data-ttu-id="24ce8-120">1</span><span class="sxs-lookup"><span data-stu-id="24ce8-120">1</span></span>    |
| <span data-ttu-id="24ce8-121">CA35</span><span class="sxs-lookup"><span data-stu-id="24ce8-121">CA35</span></span>   | <span data-ttu-id="24ce8-122">35</span><span class="sxs-lookup"><span data-stu-id="24ce8-122">35</span></span>   |



 

## <a name="tables-used-during-execution"></a><span data-ttu-id="24ce8-123">Tables utilisées lors de l’exécution</span><span class="sxs-lookup"><span data-stu-id="24ce8-123">Tables used during execution</span></span>

[<span data-ttu-id="24ce8-124">Table AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="24ce8-124">AdvtExecuteSequence Table</span></span>](advtexecutesequence-table.md)

[<span data-ttu-id="24ce8-125">Table CustomAction</span><span class="sxs-lookup"><span data-stu-id="24ce8-125">CustomAction Table</span></span>](customaction-table.md)

## <a name="related-topics"></a><span data-ttu-id="24ce8-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="24ce8-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24ce8-127">Type d’action personnalisée 19</span><span class="sxs-lookup"><span data-stu-id="24ce8-127">Custom Action Type 19</span></span>](custom-action-type-19.md)
</dt> <dt>

[<span data-ttu-id="24ce8-128">Type d’action personnalisé 35</span><span class="sxs-lookup"><span data-stu-id="24ce8-128">Custom Action Type 35</span></span>](custom-action-type-35.md)
</dt> <dt>

[<span data-ttu-id="24ce8-129">Type d’action personnalisé 51</span><span class="sxs-lookup"><span data-stu-id="24ce8-129">Custom Action Type 51</span></span>](custom-action-type-51.md)
</dt> <dt>

[<span data-ttu-id="24ce8-130">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="24ce8-130">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



