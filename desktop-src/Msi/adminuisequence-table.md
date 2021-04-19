---
description: La table AdminUISequence répertorie les actions que le programme d’installation appelle en séquence lorsque l’action d’administration de niveau supérieur est exécutée et que le niveau de l’interface utilisateur interne est défini sur interface utilisateur complète ou interface utilisateur réduite.
ms.assetid: 7227846d-b755-4af9-acc3-e27742a5097a
title: Table AdminUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8fb460f65d223e75ebd50a7587f5b3f4adeced8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534222"
---
# <a name="adminuisequence-table"></a><span data-ttu-id="a35d3-103">Table AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="a35d3-103">AdminUISequence Table</span></span>

<span data-ttu-id="a35d3-104">La table AdminUISequence répertorie les actions que le programme d’installation appelle en séquence lorsque l' [action d’administration](admin-action.md) de niveau supérieur est exécutée et que le niveau de l’interface utilisateur interne est défini sur interface utilisateur complète ou interface utilisateur réduite.</span><span class="sxs-lookup"><span data-stu-id="a35d3-104">The AdminUISequence table lists actions that the installer calls in sequence when the top-level [ADMIN action](admin-action.md) is executed and the internal user interface level is set to full UI or reduced UI.</span></span> <span data-ttu-id="a35d3-105">Le programme d’installation ignore les actions dans ce tableau si le niveau de l’interface utilisateur est défini sur interface utilisateur de base ou aucune interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a35d3-105">The installer skips the actions in this table if the user interface level is set to basic UI or no UI.</span></span> <span data-ttu-id="a35d3-106">Consultez [à propos de l’interface utilisateur](about-the-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="a35d3-106">See [About the User Interface](about-the-user-interface.md).</span></span>

<span data-ttu-id="a35d3-107">Les actions d’administration dans la séquence d’installation jusqu’à l' [action InstallValidate](installvalidate-action.md)et toutes les boîtes de dialogue de sortie sont situées dans la table AdminUISequence.</span><span class="sxs-lookup"><span data-stu-id="a35d3-107">ADMIN actions in the install sequence up to the [InstallValidate action](installvalidate-action.md), and any exit dialog boxes, are located in the AdminUISequence table.</span></span> <span data-ttu-id="a35d3-108">Toutes les actions du InstallValidate jusqu’à la fin de la séquence d’installation se trouvent dans la [table AdminExecuteSequence](adminexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="a35d3-108">All actions from the InstallValidate through the end of the install sequence are in the [AdminExecuteSequence table](adminexecutesequence-table.md).</span></span> <span data-ttu-id="a35d3-109">Étant donné que la table AdminExecuteSequence doit être autonome, elle contient également toutes les actions d’initialisation nécessaires, telles que [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md)et [CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="a35d3-109">Because the AdminExecuteSequence table needs to stand alone, it also contains any necessary initialization actions such as [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md), and [CostFinalize](costfinalize-action.md).</span></span> <span data-ttu-id="a35d3-110">Elle a également l' [action ExecuteAction](executeaction-action.md).</span><span class="sxs-lookup"><span data-stu-id="a35d3-110">It also has the [ExecuteAction action](executeaction-action.md).</span></span>

<span data-ttu-id="a35d3-111">Les colonnes sont identiques à celles de la [table InstallUISequence](installuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="a35d3-111">The columns are identical to those of the [InstallUISequence table](installuisequence-table.md).</span></span> <span data-ttu-id="a35d3-112">La table AdminUISequence contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="a35d3-112">The AdminUISequence table has the following columns.</span></span>



| <span data-ttu-id="a35d3-113">Colonne</span><span class="sxs-lookup"><span data-stu-id="a35d3-113">Column</span></span>    | <span data-ttu-id="a35d3-114">Type</span><span class="sxs-lookup"><span data-stu-id="a35d3-114">Type</span></span>                         | <span data-ttu-id="a35d3-115">Clé</span><span class="sxs-lookup"><span data-stu-id="a35d3-115">Key</span></span> | <span data-ttu-id="a35d3-116">Nullable</span><span class="sxs-lookup"><span data-stu-id="a35d3-116">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="a35d3-117">Action</span><span class="sxs-lookup"><span data-stu-id="a35d3-117">Action</span></span>    | [<span data-ttu-id="a35d3-118">Identificateur</span><span class="sxs-lookup"><span data-stu-id="a35d3-118">Identifier</span></span>](identifier.md) | <span data-ttu-id="a35d3-119">O</span><span class="sxs-lookup"><span data-stu-id="a35d3-119">Y</span></span>   | <span data-ttu-id="a35d3-120">N</span><span class="sxs-lookup"><span data-stu-id="a35d3-120">N</span></span>        |
| <span data-ttu-id="a35d3-121">Condition</span><span class="sxs-lookup"><span data-stu-id="a35d3-121">Condition</span></span> | [<span data-ttu-id="a35d3-122">Condition</span><span class="sxs-lookup"><span data-stu-id="a35d3-122">Condition</span></span>](condition.md)   | <span data-ttu-id="a35d3-123">N</span><span class="sxs-lookup"><span data-stu-id="a35d3-123">N</span></span>   | <span data-ttu-id="a35d3-124">O</span><span class="sxs-lookup"><span data-stu-id="a35d3-124">Y</span></span>        |
| <span data-ttu-id="a35d3-125">Séquence</span><span class="sxs-lookup"><span data-stu-id="a35d3-125">Sequence</span></span>  | [<span data-ttu-id="a35d3-126">Integer</span><span class="sxs-lookup"><span data-stu-id="a35d3-126">Integer</span></span>](integer.md)       | <span data-ttu-id="a35d3-127">N</span><span class="sxs-lookup"><span data-stu-id="a35d3-127">N</span></span>   | <span data-ttu-id="a35d3-128">O</span><span class="sxs-lookup"><span data-stu-id="a35d3-128">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="a35d3-129">Colonnes</span><span class="sxs-lookup"><span data-stu-id="a35d3-129">Columns</span></span>

<dl> <dt>

<span data-ttu-id="a35d3-130"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Transactionnel</span><span class="sxs-lookup"><span data-stu-id="a35d3-130"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="a35d3-131">Nom de l’action à exécuter.</span><span class="sxs-lookup"><span data-stu-id="a35d3-131">Name of the action to execute.</span></span> <span data-ttu-id="a35d3-132">Il s’agit d’une action standard, d’un assistant d’interface utilisateur ou d’une action personnalisée indiquée dans la [table CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="a35d3-132">This is either a standard action, a user interface wizard, or a custom action listed in the [CustomAction table](customaction-table.md).</span></span>

<span data-ttu-id="a35d3-133">Clé de table primaire.</span><span class="sxs-lookup"><span data-stu-id="a35d3-133">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="a35d3-134"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Etat</span><span class="sxs-lookup"><span data-stu-id="a35d3-134"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="a35d3-135">Expression logique.</span><span class="sxs-lookup"><span data-stu-id="a35d3-135">Logical expression.</span></span> <span data-ttu-id="a35d3-136">Si l’expression prend la valeur false, l’action est ignorée.</span><span class="sxs-lookup"><span data-stu-id="a35d3-136">If the expression evaluates to false, the action is skipped.</span></span> <span data-ttu-id="a35d3-137">Si la syntaxe de l’expression n’est pas valide, la séquence se termine et retourne iesBadActionData.</span><span class="sxs-lookup"><span data-stu-id="a35d3-137">If the expression syntax is invalid, the sequence terminates, returning iesBadActionData.</span></span> <span data-ttu-id="a35d3-138">Pour plus d’informations sur la syntaxe des instructions conditionnelles, consultez [syntaxe d’instruction conditionnelle](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="a35d3-138">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="a35d3-139"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Séquence</span><span class="sxs-lookup"><span data-stu-id="a35d3-139"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="a35d3-140">Une valeur positive indique la position de séquence de l’action.</span><span class="sxs-lookup"><span data-stu-id="a35d3-140">A positive value indicates the sequence position of the action.</span></span> <span data-ttu-id="a35d3-141">Les valeurs négatives suivantes indiquent que l’action est appelée si le programme d’installation retourne l’indicateur d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="a35d3-141">The following negative values indicate that the action is called if the installer returns the termination flag.</span></span> <span data-ttu-id="a35d3-142">Chaque indicateur de fin (valeur négative) peut être utilisé avec une seule action.</span><span class="sxs-lookup"><span data-stu-id="a35d3-142">Each termination flag (negative value) can be used with no more than one action.</span></span> <span data-ttu-id="a35d3-143">Plusieurs actions peuvent avoir des indicateurs d’arrêt, mais elles doivent être des indicateurs différents.</span><span class="sxs-lookup"><span data-stu-id="a35d3-143">Multiple actions can have termination flags, but they must be different flags.</span></span> <span data-ttu-id="a35d3-144">Les indicateurs de fin (valeurs négatives) sont généralement utilisés avec les [boîtes de dialogue](dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="a35d3-144">Termination flags (negative values) are typically used with [Dialog Boxes](dialog-boxes.md).</span></span>



| <span data-ttu-id="a35d3-145">Indicateur de fin</span><span class="sxs-lookup"><span data-stu-id="a35d3-145">Termination flag</span></span>          | <span data-ttu-id="a35d3-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="a35d3-146">Value</span></span> | <span data-ttu-id="a35d3-147">Description</span><span class="sxs-lookup"><span data-stu-id="a35d3-147">Description</span></span>                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a35d3-148">msiDoActionStatusSuccess</span><span class="sxs-lookup"><span data-stu-id="a35d3-148">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="a35d3-149">-1</span><span class="sxs-lookup"><span data-stu-id="a35d3-149">-1</span></span>    | <span data-ttu-id="a35d3-150">Achèvement réussi.</span><span class="sxs-lookup"><span data-stu-id="a35d3-150">Successful completion.</span></span> <span data-ttu-id="a35d3-151">Utilisé avec les boîtes de dialogue [quitter](exit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="a35d3-151">Used with [Exit](exit-dialog.md) dialog boxes.</span></span>               |
| <span data-ttu-id="a35d3-152">msiDoActionStatusUserExit</span><span class="sxs-lookup"><span data-stu-id="a35d3-152">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="a35d3-153">-2</span><span class="sxs-lookup"><span data-stu-id="a35d3-153">-2</span></span>    | <span data-ttu-id="a35d3-154">L’utilisateur termine l’installation.</span><span class="sxs-lookup"><span data-stu-id="a35d3-154">User terminates install.</span></span> <span data-ttu-id="a35d3-155">Utilisé avec les boîtes de dialogue [UserExit](userexit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="a35d3-155">Used with [UserExit](userexit-dialog.md) dialog boxes.</span></span>     |
| <span data-ttu-id="a35d3-156">msiDoActionStatusFailure</span><span class="sxs-lookup"><span data-stu-id="a35d3-156">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="a35d3-157">-3</span><span class="sxs-lookup"><span data-stu-id="a35d3-157">-3</span></span>    | <span data-ttu-id="a35d3-158">La sortie irrécupérable s’arrête.</span><span class="sxs-lookup"><span data-stu-id="a35d3-158">Fatal exit terminates.</span></span> <span data-ttu-id="a35d3-159">Utilisé avec les boîtes de dialogue [FatalError](fatalerror-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="a35d3-159">Used with a [FatalError](fatalerror-dialog.md) dialog boxes.</span></span> |
| <span data-ttu-id="a35d3-160">msiDoActionStatusSuspend</span><span class="sxs-lookup"><span data-stu-id="a35d3-160">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="a35d3-161">-4</span><span class="sxs-lookup"><span data-stu-id="a35d3-161">-4</span></span>    | <span data-ttu-id="a35d3-162">L’installation est suspendue.</span><span class="sxs-lookup"><span data-stu-id="a35d3-162">Install is suspended.</span></span>                                                                |



 

<span data-ttu-id="a35d3-163">Zéro, tous les autres nombres négatifs ou une valeur null indique que l’action n’est jamais appelée.</span><span class="sxs-lookup"><span data-stu-id="a35d3-163">Zero, all other negative numbers, or a null value indicate that the action is never called.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="a35d3-164">Validation</span><span class="sxs-lookup"><span data-stu-id="a35d3-164">Validation</span></span>

<dl>

[<span data-ttu-id="a35d3-165">ICE03</span><span class="sxs-lookup"><span data-stu-id="a35d3-165">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="a35d3-166">ICE06</span><span class="sxs-lookup"><span data-stu-id="a35d3-166">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="a35d3-167">ICE12</span><span class="sxs-lookup"><span data-stu-id="a35d3-167">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="a35d3-168">ICE13</span><span class="sxs-lookup"><span data-stu-id="a35d3-168">ICE13</span></span>](ice13.md)  
[<span data-ttu-id="a35d3-169">ICE20</span><span class="sxs-lookup"><span data-stu-id="a35d3-169">ICE20</span></span>](ice20.md)  
[<span data-ttu-id="a35d3-170">ICE26</span><span class="sxs-lookup"><span data-stu-id="a35d3-170">ICE26</span></span>](ice26.md)  
[<span data-ttu-id="a35d3-171">ICE27</span><span class="sxs-lookup"><span data-stu-id="a35d3-171">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="a35d3-172">ICE28</span><span class="sxs-lookup"><span data-stu-id="a35d3-172">ICE28</span></span>](ice28.md)  
[<span data-ttu-id="a35d3-173">ICE46</span><span class="sxs-lookup"><span data-stu-id="a35d3-173">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="a35d3-174">ICE75</span><span class="sxs-lookup"><span data-stu-id="a35d3-174">ICE75</span></span>](ice75.md)  
[<span data-ttu-id="a35d3-175">ICE79</span><span class="sxs-lookup"><span data-stu-id="a35d3-175">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="a35d3-176">ICE82</span><span class="sxs-lookup"><span data-stu-id="a35d3-176">ICE82</span></span>](ice82.md)  
[<span data-ttu-id="a35d3-177">ICE84</span><span class="sxs-lookup"><span data-stu-id="a35d3-177">ICE84</span></span>](ice84.md)  
[<span data-ttu-id="a35d3-178">ICE86</span><span class="sxs-lookup"><span data-stu-id="a35d3-178">ICE86</span></span>](ice86.md)  
[<span data-ttu-id="a35d3-179">ICE96</span><span class="sxs-lookup"><span data-stu-id="a35d3-179">ICE96</span></span>](ice96.md)  
[<span data-ttu-id="a35d3-180">ICEM04</span><span class="sxs-lookup"><span data-stu-id="a35d3-180">ICEM04</span></span>](icem04.md)  
</dl>

 

 



