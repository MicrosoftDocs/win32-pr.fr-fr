---
description: ICE63 vérifie le séquencement approprié de l’action RemoveExistingProducts.
ms.assetid: 4dd67bb0-c08a-4a44-b687-0394a3afc2c4
title: ICE63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5faa6f2ddbcb95cdf12966c2887fe9438a5d610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866718"
---
# <a name="ice63"></a><span data-ttu-id="f264b-103">ICE63</span><span class="sxs-lookup"><span data-stu-id="f264b-103">ICE63</span></span>

<span data-ttu-id="f264b-104">ICE63 vérifie le séquencement approprié de l' [action RemoveExistingProducts](removeexistingproducts-action.md).</span><span class="sxs-lookup"><span data-stu-id="f264b-104">ICE63 checks for proper sequencing of the [RemoveExistingProducts action](removeexistingproducts-action.md).</span></span> <span data-ttu-id="f264b-105">L’action RemoveExistingProducts peut être placée :</span><span class="sxs-lookup"><span data-stu-id="f264b-105">The RemoveExistingProducts action may be placed:</span></span>

1.  <span data-ttu-id="f264b-106">Entre InstallValidate et InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="f264b-106">Between InstallValidate and InstallInitialize</span></span>
2.  <span data-ttu-id="f264b-107">Immédiatement après InstallInitialize, ou après InstallInitialize si les actions entre InstallInitialize et RemoveExistingProducts ne génèrent pas d’actions de script.</span><span class="sxs-lookup"><span data-stu-id="f264b-107">Immediately after InstallInitialize, or after InstallInitialize if the actions between InstallInitialize and RemoveExistingProducts do not generate any script actions.</span></span>
3.  <span data-ttu-id="f264b-108">Immédiatement après InstallExecute ou InstallExecuteAgain et avant InstallFinalize (la même restriction que ci-dessus s’applique).</span><span class="sxs-lookup"><span data-stu-id="f264b-108">Immediately after InstallExecute or InstallExecuteAgain and before InstallFinalize (the same restriction as above applies).</span></span>
4.  <span data-ttu-id="f264b-109">Après InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="f264b-109">After InstallFinalize.</span></span>

<span data-ttu-id="f264b-110">L’échec de la résolution d’un avertissement ou d’une erreur signalée par ICE63 provoque l’échec de la mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="f264b-110">Failure to fix a warning or error reported by ICE63 leads to failure of the upgrade.</span></span>

## <a name="result"></a><span data-ttu-id="f264b-111">Résultats</span><span class="sxs-lookup"><span data-stu-id="f264b-111">Result</span></span>

<span data-ttu-id="f264b-112">ICE63 publie un avertissement ou une erreur si le séquencement de l’action RemoveExistingProducts n’est pas correct.</span><span class="sxs-lookup"><span data-stu-id="f264b-112">ICE63 posts a warning or error if the sequencing of the RemoveExistingProducts action is not correct.</span></span>

## <a name="example"></a><span data-ttu-id="f264b-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="f264b-113">Example</span></span>

<span data-ttu-id="f264b-114">ICE63 signale l’erreur suivante pour l’exemple indiqué.</span><span class="sxs-lookup"><span data-stu-id="f264b-114">ICE63 reports the following error for the example shown.</span></span>

``` syntax
WARNING: Some action falls between InstallInitialize and RemoveExistingProducts.
```

<span data-ttu-id="f264b-115">L’action « MyCustomAction » se produit entre InstallInitialize et RemoveExistingProducts.</span><span class="sxs-lookup"><span data-stu-id="f264b-115">The action 'MyCustomAction' occurs between InstallInitialize and RemoveExistingProducts.</span></span> <span data-ttu-id="f264b-116">Si MyCustomAction génère des actions dans le script, cela provoque des problèmes lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="f264b-116">If MyCustomAction generates any actions in the script, this causes problems in the installation.</span></span>

<span data-ttu-id="f264b-117">Pour corriger cette erreur, vérifiez que MyCustomAction ne génère pas d’actions de script ou reséquencez les actions.</span><span class="sxs-lookup"><span data-stu-id="f264b-117">To fix this error, verify that MyCustomAction does not generate any script actions or resequence the actions.</span></span>

[<span data-ttu-id="f264b-118">Table InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="f264b-118">InstallExecuteSequence Table</span></span>](installexecutesequence-table.md)



| <span data-ttu-id="f264b-119">Action</span><span class="sxs-lookup"><span data-stu-id="f264b-119">Action</span></span>                 | <span data-ttu-id="f264b-120">Condition</span><span class="sxs-lookup"><span data-stu-id="f264b-120">Condition</span></span> | <span data-ttu-id="f264b-121">Séquence</span><span class="sxs-lookup"><span data-stu-id="f264b-121">Sequence</span></span> |
|------------------------|-----------|----------|
| <span data-ttu-id="f264b-122">InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="f264b-122">InstallInitialize</span></span>      |           | <span data-ttu-id="f264b-123">1 000</span><span class="sxs-lookup"><span data-stu-id="f264b-123">1000</span></span>     |
| <span data-ttu-id="f264b-124">MyCustomAction</span><span class="sxs-lookup"><span data-stu-id="f264b-124">MyCustomAction</span></span>         |           | <span data-ttu-id="f264b-125">1010</span><span class="sxs-lookup"><span data-stu-id="f264b-125">1010</span></span>     |
| <span data-ttu-id="f264b-126">RemoveExistingProducts</span><span class="sxs-lookup"><span data-stu-id="f264b-126">RemoveExistingProducts</span></span> |           | <span data-ttu-id="f264b-127">1020</span><span class="sxs-lookup"><span data-stu-id="f264b-127">1020</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="f264b-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f264b-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f264b-129">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="f264b-129">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



