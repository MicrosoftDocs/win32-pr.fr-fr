---
description: ICE68 vérifie que tous les types d’action personnalisés nécessaires pour une installation sont valides.
ms.assetid: a37d6d6c-3005-425b-883a-6fe074b9d708
title: ICE68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1392db6ec05085c672ed70c8f035ea8eed3015e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532160"
---
# <a name="ice68"></a><span data-ttu-id="36366-103">ICE68</span><span class="sxs-lookup"><span data-stu-id="36366-103">ICE68</span></span>

<span data-ttu-id="36366-104">ICE68 vérifie que tous les types d’action personnalisés nécessaires pour une installation sont valides.</span><span class="sxs-lookup"><span data-stu-id="36366-104">ICE68 checks that all custom action types needed for an installation are valid.</span></span> <span data-ttu-id="36366-105">L’échec de la résolution de l’erreur signalée par ICE68 provoque l’échec d’une installation qui tente d’exécuter l’action.</span><span class="sxs-lookup"><span data-stu-id="36366-105">Failure to fix the error reported by ICE68 causes an installation that attempts to execute the action to fail.</span></span> <span data-ttu-id="36366-106">ICE68 émet un avertissement si l’attribut **msidbCustomActionTypeNoImpersonate** est défini sans définir également l’attribut **msidbCustomActionTypeInScript** .</span><span class="sxs-lookup"><span data-stu-id="36366-106">ICE68 issues a warning if the **msidbCustomActionTypeNoImpersonate** attribute is set without also setting the **msidbCustomActionTypeInScript** attribute.</span></span>

## <a name="result"></a><span data-ttu-id="36366-107">Résultats</span><span class="sxs-lookup"><span data-stu-id="36366-107">Result</span></span>

<span data-ttu-id="36366-108">ICE68 retourne une erreur si un type d’action requis pour une installation n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="36366-108">ICE68 returns an error if an action type needed for an installation is invalid.</span></span>

## <a name="example"></a><span data-ttu-id="36366-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="36366-109">Example</span></span>

<span data-ttu-id="36366-110">ICE68 publie l’avertissement suivant si une action personnalisée a le bit **msidbCustomActionTypeNoImpersonate** défini dans le champ type de la table CustomAction sans que le **msidbCustomActionTypeInScript** soit également défini.</span><span class="sxs-lookup"><span data-stu-id="36366-110">ICE68 posts the following warning if a custom action has the **msidbCustomActionTypeNoImpersonate** bit set in the Type field of the CustomAction table without the **msidbCustomActionTypeInScript** also set.</span></span>

``` syntax
Even though custom action '[2]' is marked to be elevated (with 
attribute msidbCustomActionTypeNoImpersonate), it will not be run with elevated 
privileges because it's not deferred (with attribute msidbCustomActionTypeInScript).
```

<span data-ttu-id="36366-111">Pour résoudre cet avertissement, incluez **msidbCustomActionTypeInScript** (0x400) si l’action personnalisée inclut **msidbCustomActionTypeNoImpersonate** (0x800).</span><span class="sxs-lookup"><span data-stu-id="36366-111">To fix this warning, include **msidbCustomActionTypeInScript** (0x400) if the custom action includes **msidbCustomActionTypeNoImpersonate** (0x800).</span></span> <span data-ttu-id="36366-112">Dans le cas contraire, le programme d’installation ignore l’attribut **msidbCustomActionTypeNoImpersonate** .</span><span class="sxs-lookup"><span data-stu-id="36366-112">Otherwise the installer ignores the **msidbCustomActionTypeNoImpersonate** attribute.</span></span> <span data-ttu-id="36366-113">Pour plus d’informations, consultez [action personnalisée In-Script options d’exécution](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="36366-113">For more information, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

<span data-ttu-id="36366-114">ICE68 signale l’erreur suivante pour l’exemple ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="36366-114">ICE68 reports the following error for the example shown:</span></span>

``` syntax
Invalid custom action type for action 'Action1'.
```

<span data-ttu-id="36366-115">1027 n’est pas un type d’action valide.</span><span class="sxs-lookup"><span data-stu-id="36366-115">1027 is not a valid action type.</span></span>

<span data-ttu-id="36366-116">Pour corriger cette erreur, choisissez un type d’action personnalisé valide.</span><span class="sxs-lookup"><span data-stu-id="36366-116">To fix this error, choose a valid custom action type.</span></span>

<span data-ttu-id="36366-117">[Table CustomAction](customaction-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="36366-117">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="36366-118">Action</span><span class="sxs-lookup"><span data-stu-id="36366-118">Action</span></span>  | <span data-ttu-id="36366-119">Type</span><span class="sxs-lookup"><span data-stu-id="36366-119">Type</span></span> | <span data-ttu-id="36366-120">Source</span><span class="sxs-lookup"><span data-stu-id="36366-120">Source</span></span>   | <span data-ttu-id="36366-121">Cible</span><span class="sxs-lookup"><span data-stu-id="36366-121">Target</span></span>     |
|---------|------|----------|------------|
| <span data-ttu-id="36366-122">Action1</span><span class="sxs-lookup"><span data-stu-id="36366-122">Action1</span></span> | <span data-ttu-id="36366-123">1027</span><span class="sxs-lookup"><span data-stu-id="36366-123">1027</span></span> | <span data-ttu-id="36366-124">Argument</span><span class="sxs-lookup"><span data-stu-id="36366-124">Argument</span></span> | <span data-ttu-id="36366-125">Composant1</span><span class="sxs-lookup"><span data-stu-id="36366-125">Component1</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="36366-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="36366-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36366-127">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="36366-127">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



