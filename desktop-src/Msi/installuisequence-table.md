---
description: La table InstallUISequence répertorie les actions qui sont exécutées lorsque l’action d’installation de niveau supérieur est exécutée et que le niveau d’interface utilisateur interne est défini sur interface utilisateur complète ou réduite.
ms.assetid: 076d7c14-e302-4465-aed5-27a4b1f70ac8
title: Table InstallUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19a4d8d3033645ac1f414e3aff67be2a26d7a6ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536596"
---
# <a name="installuisequence-table"></a><span data-ttu-id="cb67e-103">Table InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="cb67e-103">InstallUISequence Table</span></span>

<span data-ttu-id="cb67e-104">La table InstallUISequence répertorie les actions qui sont exécutées lorsque l' [action d’installation](install-action.md) de niveau supérieur est exécutée et que le niveau d’interface utilisateur interne est défini sur interface utilisateur complète ou réduite.</span><span class="sxs-lookup"><span data-stu-id="cb67e-104">The InstallUISequence table lists actions that are executed when the top-level [INSTALL action](install-action.md) is executed and the internal user interface level is set to full UI or reduced UI.</span></span> <span data-ttu-id="cb67e-105">Le programme d’installation ignore les actions dans ce tableau si le niveau de l’interface utilisateur est défini sur interface utilisateur de base ou aucune interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cb67e-105">The installer skips the actions in this table if the user interface level is set to basic UI or no UI.</span></span> <span data-ttu-id="cb67e-106">Consultez [à propos de l’interface utilisateur](about-the-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="cb67e-106">See [About the User Interface](about-the-user-interface.md).</span></span>

<span data-ttu-id="cb67e-107">Les actions de la séquence d’installation jusqu’à l' [action InstallValidate](installvalidate-action.md)et les boîtes de dialogue quitter sont situées dans la table InstallUISequence.</span><span class="sxs-lookup"><span data-stu-id="cb67e-107">Actions in the install sequence up to the [InstallValidate action](installvalidate-action.md), and the exit dialog boxes, are located in the InstallUISequence table.</span></span> <span data-ttu-id="cb67e-108">Toutes les actions du InstallValidate jusqu’à la fin de la séquence d’installation se trouvent dans la [table InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="cb67e-108">All actions from the InstallValidate through the end of the install sequence are in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="cb67e-109">Étant donné que la table InstallExecuteSequence doit être autonome, elle comporte toutes les actions d’initialisation nécessaires, telles que les actions [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md), [CostFinalize](costfinalize-action.md)et [ExecuteAction](executeaction-action.md).</span><span class="sxs-lookup"><span data-stu-id="cb67e-109">Because the InstallExecuteSequence table needs to stand alone, it has any necessary initialization actions such as the [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md), and the [CostFinalize](costfinalize-action.md), and [ExecuteAction action](executeaction-action.md).</span></span>

<span data-ttu-id="cb67e-110">La table InstallUISequence contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="cb67e-110">The InstallUISequence table has the following columns.</span></span>



| <span data-ttu-id="cb67e-111">Colonne</span><span class="sxs-lookup"><span data-stu-id="cb67e-111">Column</span></span>    | <span data-ttu-id="cb67e-112">Type</span><span class="sxs-lookup"><span data-stu-id="cb67e-112">Type</span></span>                         | <span data-ttu-id="cb67e-113">Clé</span><span class="sxs-lookup"><span data-stu-id="cb67e-113">Key</span></span> | <span data-ttu-id="cb67e-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="cb67e-114">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="cb67e-115">Action</span><span class="sxs-lookup"><span data-stu-id="cb67e-115">Action</span></span>    | [<span data-ttu-id="cb67e-116">Identificateur</span><span class="sxs-lookup"><span data-stu-id="cb67e-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="cb67e-117">O</span><span class="sxs-lookup"><span data-stu-id="cb67e-117">Y</span></span>   | <span data-ttu-id="cb67e-118">N</span><span class="sxs-lookup"><span data-stu-id="cb67e-118">N</span></span>        |
| <span data-ttu-id="cb67e-119">Condition</span><span class="sxs-lookup"><span data-stu-id="cb67e-119">Condition</span></span> | [<span data-ttu-id="cb67e-120">Condition</span><span class="sxs-lookup"><span data-stu-id="cb67e-120">Condition</span></span>](condition.md)   | <span data-ttu-id="cb67e-121">N</span><span class="sxs-lookup"><span data-stu-id="cb67e-121">N</span></span>   | <span data-ttu-id="cb67e-122">O</span><span class="sxs-lookup"><span data-stu-id="cb67e-122">Y</span></span>        |
| <span data-ttu-id="cb67e-123">Séquence</span><span class="sxs-lookup"><span data-stu-id="cb67e-123">Sequence</span></span>  | [<span data-ttu-id="cb67e-124">Integer</span><span class="sxs-lookup"><span data-stu-id="cb67e-124">Integer</span></span>](integer.md)       | <span data-ttu-id="cb67e-125">N</span><span class="sxs-lookup"><span data-stu-id="cb67e-125">N</span></span>   | <span data-ttu-id="cb67e-126">O</span><span class="sxs-lookup"><span data-stu-id="cb67e-126">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="cb67e-127">Colonnes</span><span class="sxs-lookup"><span data-stu-id="cb67e-127">Columns</span></span>

<dl> <dt>

<span data-ttu-id="cb67e-128"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Transactionnel</span><span class="sxs-lookup"><span data-stu-id="cb67e-128"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="cb67e-129">Nom de l’action à exécuter.</span><span class="sxs-lookup"><span data-stu-id="cb67e-129">Name of the action to execute.</span></span> <span data-ttu-id="cb67e-130">Il s’agit d’une action intégrée, d’une action personnalisée ou d’un assistant de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cb67e-130">This is either a built-in action, a custom action, or a user interface wizard.</span></span>

<span data-ttu-id="cb67e-131">Clé de table primaire.</span><span class="sxs-lookup"><span data-stu-id="cb67e-131">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="cb67e-132"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Etat</span><span class="sxs-lookup"><span data-stu-id="cb67e-132"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="cb67e-133">Ce champ contient une expression conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="cb67e-133">This field contains a conditional expression.</span></span> <span data-ttu-id="cb67e-134">Si l’expression prend la valeur false, l’action est ignorée.</span><span class="sxs-lookup"><span data-stu-id="cb67e-134">If the expression evaluates to False, then the action is skipped.</span></span> <span data-ttu-id="cb67e-135">Si la syntaxe de l’expression n’est pas valide, la séquence se termine et retourne iesBadActionData.</span><span class="sxs-lookup"><span data-stu-id="cb67e-135">If the expression syntax is invalid, then the sequence terminates, returning iesBadActionData.</span></span> <span data-ttu-id="cb67e-136">Pour plus d’informations sur la syntaxe des instructions conditionnelles, consultez [syntaxe d’instruction conditionnelle](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="cb67e-136">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="cb67e-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Séquence</span><span class="sxs-lookup"><span data-stu-id="cb67e-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="cb67e-138">Le nombre dans cette colonne détermine la position de la séquence dans laquelle cette action est exécutée.</span><span class="sxs-lookup"><span data-stu-id="cb67e-138">The number in this column determines the sequence position in which this action is run.</span></span>

<span data-ttu-id="cb67e-139">Une valeur positive représente la position de la séquence.</span><span class="sxs-lookup"><span data-stu-id="cb67e-139">A positive value represents the sequence position.</span></span> <span data-ttu-id="cb67e-140">Une valeur null indique que l’action n’est jamais exécutée.</span><span class="sxs-lookup"><span data-stu-id="cb67e-140">A Null value indicates that the action is never run.</span></span> <span data-ttu-id="cb67e-141">Les valeurs négatives suivantes indiquent que cette action est exécutée si le programme d’installation retourne l’indicateur de fin associé.</span><span class="sxs-lookup"><span data-stu-id="cb67e-141">The following negative values indicate that this action is executed if the installer returns the associated termination flag.</span></span> <span data-ttu-id="cb67e-142">Chaque indicateur de fin (valeur négative) peut être utilisé avec une seule action.</span><span class="sxs-lookup"><span data-stu-id="cb67e-142">Each termination flag (negative value) can be used with no more than one action.</span></span> <span data-ttu-id="cb67e-143">Plusieurs actions peuvent avoir des indicateurs d’arrêt, mais elles doivent être des indicateurs différents.</span><span class="sxs-lookup"><span data-stu-id="cb67e-143">Multiple actions can have termination flags, but they must be different flags.</span></span> <span data-ttu-id="cb67e-144">Les indicateurs de fin (valeurs négatives) sont généralement utilisés avec les [boîtes de dialogue](dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="cb67e-144">Termination flags (negative values) are typically used with [Dialog Boxes](dialog-boxes.md).</span></span>



| <span data-ttu-id="cb67e-145">Indicateur de fin</span><span class="sxs-lookup"><span data-stu-id="cb67e-145">Termination flag</span></span>          | <span data-ttu-id="cb67e-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb67e-146">Value</span></span> | <span data-ttu-id="cb67e-147">Description</span><span class="sxs-lookup"><span data-stu-id="cb67e-147">Description</span></span>                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cb67e-148">msiDoActionStatusSuccess</span><span class="sxs-lookup"><span data-stu-id="cb67e-148">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="cb67e-149">-1</span><span class="sxs-lookup"><span data-stu-id="cb67e-149">-1</span></span>    | <span data-ttu-id="cb67e-150">Achèvement réussi.</span><span class="sxs-lookup"><span data-stu-id="cb67e-150">Successful completion.</span></span> <span data-ttu-id="cb67e-151">Utilisé avec les boîtes de dialogue [quitter](exit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="cb67e-151">Used with [Exit](exit-dialog.md) dialog boxes.</span></span>               |
| <span data-ttu-id="cb67e-152">msiDoActionStatusUserExit</span><span class="sxs-lookup"><span data-stu-id="cb67e-152">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="cb67e-153">-2</span><span class="sxs-lookup"><span data-stu-id="cb67e-153">-2</span></span>    | <span data-ttu-id="cb67e-154">L’utilisateur termine l’installation.</span><span class="sxs-lookup"><span data-stu-id="cb67e-154">User terminates install.</span></span> <span data-ttu-id="cb67e-155">Utilisé avec les boîtes de dialogue [UserExit](userexit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="cb67e-155">Used with [UserExit](userexit-dialog.md) dialog boxes.</span></span>     |
| <span data-ttu-id="cb67e-156">msiDoActionStatusFailure</span><span class="sxs-lookup"><span data-stu-id="cb67e-156">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="cb67e-157">-3</span><span class="sxs-lookup"><span data-stu-id="cb67e-157">-3</span></span>    | <span data-ttu-id="cb67e-158">La sortie irrécupérable s’arrête.</span><span class="sxs-lookup"><span data-stu-id="cb67e-158">Fatal exit terminates.</span></span> <span data-ttu-id="cb67e-159">Utilisé avec les boîtes de dialogue [FatalError](fatalerror-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="cb67e-159">Used with a [FatalError](fatalerror-dialog.md) dialog boxes.</span></span> |
| <span data-ttu-id="cb67e-160">msiDoActionStatusSuspend</span><span class="sxs-lookup"><span data-stu-id="cb67e-160">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="cb67e-161">-4</span><span class="sxs-lookup"><span data-stu-id="cb67e-161">-4</span></span>    | <span data-ttu-id="cb67e-162">L’installation est suspendue.</span><span class="sxs-lookup"><span data-stu-id="cb67e-162">Install is suspended.</span></span>                                                                |



 

<span data-ttu-id="cb67e-163">Zéro, tous les autres nombres négatifs ou une valeur null indique que l’action n’est jamais exécutée.</span><span class="sxs-lookup"><span data-stu-id="cb67e-163">Zero, all other negative numbers, or a Null value indicate that the action is never run.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cb67e-164">Notes</span><span class="sxs-lookup"><span data-stu-id="cb67e-164">Remarks</span></span>

<span data-ttu-id="cb67e-165">Le texte localisé associé à l’affichage de progression ou à la journalisation est spécifié dans la [table ActionText](actiontext-table.md).</span><span class="sxs-lookup"><span data-stu-id="cb67e-165">Associated localized text for progress display or logging is specified in the [ActionText table](actiontext-table.md).</span></span>

<span data-ttu-id="cb67e-166">Pour obtenir un exemple de table de séquences, consultez [utilisation d’une table de séquences](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="cb67e-166">For an example of a sequence table, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="cb67e-167">Validation</span><span class="sxs-lookup"><span data-stu-id="cb67e-167">Validation</span></span>

<dl>

[<span data-ttu-id="cb67e-168">ICE03</span><span class="sxs-lookup"><span data-stu-id="cb67e-168">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="cb67e-169">ICE06</span><span class="sxs-lookup"><span data-stu-id="cb67e-169">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="cb67e-170">ICE12</span><span class="sxs-lookup"><span data-stu-id="cb67e-170">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="cb67e-171">ICE13</span><span class="sxs-lookup"><span data-stu-id="cb67e-171">ICE13</span></span>](ice13.md)  
[<span data-ttu-id="cb67e-172">ICE20</span><span class="sxs-lookup"><span data-stu-id="cb67e-172">ICE20</span></span>](ice20.md)  
[<span data-ttu-id="cb67e-173">ICE26</span><span class="sxs-lookup"><span data-stu-id="cb67e-173">ICE26</span></span>](ice26.md)  
[<span data-ttu-id="cb67e-174">ICE27</span><span class="sxs-lookup"><span data-stu-id="cb67e-174">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="cb67e-175">ICE28</span><span class="sxs-lookup"><span data-stu-id="cb67e-175">ICE28</span></span>](ice28.md)  
[<span data-ttu-id="cb67e-176">ICE46</span><span class="sxs-lookup"><span data-stu-id="cb67e-176">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="cb67e-177">ICE75</span><span class="sxs-lookup"><span data-stu-id="cb67e-177">ICE75</span></span>](ice75.md)  
[<span data-ttu-id="cb67e-178">ICE79</span><span class="sxs-lookup"><span data-stu-id="cb67e-178">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="cb67e-179">ICE82</span><span class="sxs-lookup"><span data-stu-id="cb67e-179">ICE82</span></span>](ice82.md)  
[<span data-ttu-id="cb67e-180">ICE86</span><span class="sxs-lookup"><span data-stu-id="cb67e-180">ICE86</span></span>](ice86.md)  
</dl>

 

 



