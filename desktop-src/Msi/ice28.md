---
description: ICE28 est couramment utilisé pour confirmer que l’action ForceReboot est placée avant ou après, et jamais dans, un groupe spécifique d’actions dans les tables de séquences d’actions. Consultez la rubrique d’action ForceReboot pour déterminer les actions qui composent ce groupe.
ms.assetid: 746d907a-33e1-479a-bcb0-93e7fd5dd975
title: ICE28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc65878bdc3db4f9b79ba95b4a170b694a4728ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750132"
---
# <a name="ice28"></a><span data-ttu-id="051e7-104">ICE28</span><span class="sxs-lookup"><span data-stu-id="051e7-104">ICE28</span></span>

<span data-ttu-id="051e7-105">ICE28 est couramment utilisé pour confirmer que l’action ForceReboot est placée avant ou après, et jamais dans, un groupe spécifique d’actions dans les tables de séquences d’actions.</span><span class="sxs-lookup"><span data-stu-id="051e7-105">ICE28 is commonly used to validate that the ForceReboot action is placed before or after, and never within, a specific group of actions in the action sequence tables.</span></span> <span data-ttu-id="051e7-106">Consultez la rubrique d' [action ForceReboot](forcereboot-action.md) pour déterminer les actions qui composent ce groupe.</span><span class="sxs-lookup"><span data-stu-id="051e7-106">See the [ForceReboot action](forcereboot-action.md) topic to determine the actions that comprise this group.</span></span>

<span data-ttu-id="051e7-107">ICE28 valide les actions dans les tableaux de séquence suivants :</span><span class="sxs-lookup"><span data-stu-id="051e7-107">ICE28 validates actions in the following sequence tables:</span></span>

[<span data-ttu-id="051e7-108">Table AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="051e7-108">AdminUISequence table</span></span>](adminuisequence-table.md)

[<span data-ttu-id="051e7-109">Table AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="051e7-109">AdminExecuteSequence table</span></span>](adminexecutesequence-table.md)

[<span data-ttu-id="051e7-110">Table InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="051e7-110">InstallUISequence table</span></span>](installuisequence-table.md)

[<span data-ttu-id="051e7-111">Table InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="051e7-111">InstallExecuteSequence table</span></span>](installexecutesequence-table.md)

## <a name="result"></a><span data-ttu-id="051e7-112">Résultats</span><span class="sxs-lookup"><span data-stu-id="051e7-112">Result</span></span>

<span data-ttu-id="051e7-113">ICE28 publie un message d’erreur si ForceReboot est séquencé dans le groupe d’actions spécifié.</span><span class="sxs-lookup"><span data-stu-id="051e7-113">ICE28 posts an error message if ForceReboot is sequenced within the specified action group.</span></span>

## <a name="example"></a><span data-ttu-id="051e7-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="051e7-114">Example</span></span>

<span data-ttu-id="051e7-115">Pour l’exemple illustré, ICE28 publie le message d’erreur suivant :</span><span class="sxs-lookup"><span data-stu-id="051e7-115">For the example shown, ICE28 posts the following error message:</span></span>

``` syntax
Action: 'ForceReboot' of table InstallExecuteSequence is not permitted in the range 5 to 15 because it cannot separate a set of actions contained in this range.
```

[<span data-ttu-id="051e7-116">Table InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="051e7-116">InstallExecuteSequence Table</span></span>](installexecutesequence-table.md)



| <span data-ttu-id="051e7-117">Action</span><span class="sxs-lookup"><span data-stu-id="051e7-117">Action</span></span>             | <span data-ttu-id="051e7-118">Séquence</span><span class="sxs-lookup"><span data-stu-id="051e7-118">Sequence</span></span> |
|--------------------|----------|
| <span data-ttu-id="051e7-119">ForceReboot</span><span class="sxs-lookup"><span data-stu-id="051e7-119">ForceReboot</span></span>        | <span data-ttu-id="051e7-120">10</span><span class="sxs-lookup"><span data-stu-id="051e7-120">10</span></span>       |
| <span data-ttu-id="051e7-121">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="051e7-121">RegisterMIMEInfo</span></span>   |   <span data-ttu-id="051e7-122">5</span><span class="sxs-lookup"><span data-stu-id="051e7-122">5</span></span>      |
| <span data-ttu-id="051e7-123">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="051e7-123">RegisterProgIdInfo</span></span> | <span data-ttu-id="051e7-124">15</span><span class="sxs-lookup"><span data-stu-id="051e7-124">15</span></span>       |



 

<span data-ttu-id="051e7-125">Le numéro de séquence 10 donné aux arrêts ForceReboot génère l’erreur, car il est compris entre les numéros de séquence de RegisterMIMEInfo et de RegisterProgIdInfo.</span><span class="sxs-lookup"><span data-stu-id="051e7-125">The sequence number of 10 given to ForceReboot breaks generates the error, because it comes between the sequence numbers of RegisterMIMEInfo and RegisterProgIdInfo.</span></span>

## <a name="related-topics"></a><span data-ttu-id="051e7-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="051e7-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="051e7-127">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="051e7-127">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



