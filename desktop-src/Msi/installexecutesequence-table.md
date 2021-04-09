---
description: Le tableau InstallExecuteSequence répertorie les actions qui sont exécutées lors de l’exécution de l’action d’installation de niveau supérieur.
ms.assetid: 995d4159-bfc9-48b2-8328-3ae8251d785d
title: Table InstallExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7d110debacab19739c3da69abf3948d11bb7aa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862342"
---
# <a name="installexecutesequence-table"></a><span data-ttu-id="f11f3-103">Table InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="f11f3-103">InstallExecuteSequence Table</span></span>

<span data-ttu-id="f11f3-104">Le tableau InstallExecuteSequence répertorie les actions qui sont exécutées lors de l’exécution de l' [action d’installation](install-action.md) de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="f11f3-104">The InstallExecuteSequence table lists actions that are executed when the top-level [INSTALL action](install-action.md) is executed.</span></span>

<span data-ttu-id="f11f3-105">Les actions de la séquence d’installation jusqu’à l' [action InstallValidate](installvalidate-action.md)et toutes les boîtes de dialogue de sortie sont situées dans la [table InstallUISequence](installuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="f11f3-105">Actions in the install sequence up to the [InstallValidate action](installvalidate-action.md), and any exit dialog boxes, are located in the [InstallUISequence table](installuisequence-table.md).</span></span> <span data-ttu-id="f11f3-106">Toutes les actions du InstallValidate jusqu’à la fin de la séquence d’installation se trouvent dans la table InstallExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="f11f3-106">All actions from the InstallValidate through the end of the install sequence are in the InstallExecuteSequence table.</span></span> <span data-ttu-id="f11f3-107">Étant donné que la table InstallExecuteSequence doit être autonome, elle comporte toutes les actions d’initialisation nécessaires, telles que les actions [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md)et [CostFinalize](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="f11f3-107">Because the InstallExecuteSequence table needs to stand alone, it has any necessary initialization actions such as the [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md), and [CostFinalize](costfinalize-action.md) actions.</span></span>

<span data-ttu-id="f11f3-108">Les [actions personnalisées](custom-actions.md) nécessitant une interface utilisateur doivent utiliser [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) au lieu de boîtes de dialogue créées créées à l’aide de la table de [boîtes de dialogue](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="f11f3-108">[Custom actions](custom-actions.md) requiring a user interface should use [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) instead of authored dialog boxes created using the [Dialog table](dialog-table.md).</span></span>

<span data-ttu-id="f11f3-109">La table InstallExecuteSequence contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="f11f3-109">The InstallExecuteSequence table has the following columns.</span></span>



| <span data-ttu-id="f11f3-110">Colonne</span><span class="sxs-lookup"><span data-stu-id="f11f3-110">Column</span></span>    | <span data-ttu-id="f11f3-111">Type</span><span class="sxs-lookup"><span data-stu-id="f11f3-111">Type</span></span>                         | <span data-ttu-id="f11f3-112">Clé</span><span class="sxs-lookup"><span data-stu-id="f11f3-112">Key</span></span> | <span data-ttu-id="f11f3-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="f11f3-113">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="f11f3-114">Action</span><span class="sxs-lookup"><span data-stu-id="f11f3-114">Action</span></span>    | [<span data-ttu-id="f11f3-115">Identificateur</span><span class="sxs-lookup"><span data-stu-id="f11f3-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="f11f3-116">O</span><span class="sxs-lookup"><span data-stu-id="f11f3-116">Y</span></span>   | <span data-ttu-id="f11f3-117">N</span><span class="sxs-lookup"><span data-stu-id="f11f3-117">N</span></span>        |
| <span data-ttu-id="f11f3-118">Condition</span><span class="sxs-lookup"><span data-stu-id="f11f3-118">Condition</span></span> | [<span data-ttu-id="f11f3-119">Condition</span><span class="sxs-lookup"><span data-stu-id="f11f3-119">Condition</span></span>](condition.md)   | <span data-ttu-id="f11f3-120">N</span><span class="sxs-lookup"><span data-stu-id="f11f3-120">N</span></span>   | <span data-ttu-id="f11f3-121">O</span><span class="sxs-lookup"><span data-stu-id="f11f3-121">Y</span></span>        |
| <span data-ttu-id="f11f3-122">Séquence</span><span class="sxs-lookup"><span data-stu-id="f11f3-122">Sequence</span></span>  | [<span data-ttu-id="f11f3-123">Integer</span><span class="sxs-lookup"><span data-stu-id="f11f3-123">Integer</span></span>](integer.md)       | <span data-ttu-id="f11f3-124">N</span><span class="sxs-lookup"><span data-stu-id="f11f3-124">N</span></span>   | <span data-ttu-id="f11f3-125">O</span><span class="sxs-lookup"><span data-stu-id="f11f3-125">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="f11f3-126">Colonnes</span><span class="sxs-lookup"><span data-stu-id="f11f3-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="f11f3-127"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Transactionnel</span><span class="sxs-lookup"><span data-stu-id="f11f3-127"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="f11f3-128">Nom de l’action à exécuter.</span><span class="sxs-lookup"><span data-stu-id="f11f3-128">Name of the action to execute.</span></span> <span data-ttu-id="f11f3-129">Il s’agit d’une action intégrée ou d’une action personnalisée.</span><span class="sxs-lookup"><span data-stu-id="f11f3-129">This is either a built-in action or a custom action.</span></span>

<span data-ttu-id="f11f3-130">Clé de table primaire.</span><span class="sxs-lookup"><span data-stu-id="f11f3-130">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="f11f3-131"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Etat</span><span class="sxs-lookup"><span data-stu-id="f11f3-131"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="f11f3-132">Ce champ contient une expression conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="f11f3-132">This field contains a conditional expression.</span></span> <span data-ttu-id="f11f3-133">Si l’expression prend la valeur false, l’action est ignorée.</span><span class="sxs-lookup"><span data-stu-id="f11f3-133">If the expression evaluates to False, then the action is skipped.</span></span> <span data-ttu-id="f11f3-134">Si la syntaxe de l’expression n’est pas valide, la séquence se termine et retourne iesBadActionData.</span><span class="sxs-lookup"><span data-stu-id="f11f3-134">If the expression syntax is invalid, then the sequence terminates, returning iesBadActionData.</span></span> <span data-ttu-id="f11f3-135">Pour plus d’informations sur la syntaxe des instructions conditionnelles, consultez [syntaxe d’instruction conditionnelle](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="f11f3-135">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="f11f3-136"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Séquence</span><span class="sxs-lookup"><span data-stu-id="f11f3-136"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="f11f3-137">Nombre qui détermine la position de la séquence dans laquelle cette action doit être exécutée.</span><span class="sxs-lookup"><span data-stu-id="f11f3-137">Number that determines the sequence position in which this action is to be executed.</span></span>

<span data-ttu-id="f11f3-138">Une valeur positive représente la position de la séquence.</span><span class="sxs-lookup"><span data-stu-id="f11f3-138">A positive value represents the sequence position.</span></span> <span data-ttu-id="f11f3-139">Une valeur null indique que l’action n’est pas exécutée.</span><span class="sxs-lookup"><span data-stu-id="f11f3-139">A Null value indicates that the action is not executed.</span></span> <span data-ttu-id="f11f3-140">Les valeurs négatives suivantes indiquent que cette action doit être exécutée si le programme d’installation retourne l’indicateur d’arrêt associé.</span><span class="sxs-lookup"><span data-stu-id="f11f3-140">The following negative values indicate that this action is to be executed if the installer returns the associated termination flag.</span></span> <span data-ttu-id="f11f3-141">Chaque indicateur de fin (valeur négative) peut être utilisé avec une seule action.</span><span class="sxs-lookup"><span data-stu-id="f11f3-141">Each termination flag (negative value) can be used with no more than one action.</span></span> <span data-ttu-id="f11f3-142">Plusieurs actions peuvent avoir des indicateurs d’arrêt, mais elles doivent être des indicateurs différents.</span><span class="sxs-lookup"><span data-stu-id="f11f3-142">Multiple actions can have termination flags, but they must be different flags.</span></span> <span data-ttu-id="f11f3-143">Les indicateurs de fin (valeurs négatives) sont généralement utilisés avec les [boîtes de dialogue](dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="f11f3-143">Termination flags (negative values) are typically used with [Dialog Boxes](dialog-boxes.md).</span></span>



| <span data-ttu-id="f11f3-144">Indicateur de fin</span><span class="sxs-lookup"><span data-stu-id="f11f3-144">Termination flag</span></span>          | <span data-ttu-id="f11f3-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="f11f3-145">Value</span></span> | <span data-ttu-id="f11f3-146">Description</span><span class="sxs-lookup"><span data-stu-id="f11f3-146">Description</span></span>                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f11f3-147">msiDoActionStatusSuccess</span><span class="sxs-lookup"><span data-stu-id="f11f3-147">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="f11f3-148">-1</span><span class="sxs-lookup"><span data-stu-id="f11f3-148">-1</span></span>    | <span data-ttu-id="f11f3-149">Achèvement réussi.</span><span class="sxs-lookup"><span data-stu-id="f11f3-149">Successful completion.</span></span> <span data-ttu-id="f11f3-150">Utilisé avec les boîtes de dialogue [quitter](exit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="f11f3-150">Used with [Exit](exit-dialog.md) dialog boxes.</span></span>               |
| <span data-ttu-id="f11f3-151">msiDoActionStatusUserExit</span><span class="sxs-lookup"><span data-stu-id="f11f3-151">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="f11f3-152">-2</span><span class="sxs-lookup"><span data-stu-id="f11f3-152">-2</span></span>    | <span data-ttu-id="f11f3-153">L’utilisateur termine l’installation.</span><span class="sxs-lookup"><span data-stu-id="f11f3-153">User terminates install.</span></span> <span data-ttu-id="f11f3-154">Utilisé avec les boîtes de dialogue [UserExit](userexit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="f11f3-154">Used with [UserExit](userexit-dialog.md) dialog boxes.</span></span>     |
| <span data-ttu-id="f11f3-155">msiDoActionStatusFailure</span><span class="sxs-lookup"><span data-stu-id="f11f3-155">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="f11f3-156">-3</span><span class="sxs-lookup"><span data-stu-id="f11f3-156">-3</span></span>    | <span data-ttu-id="f11f3-157">La sortie irrécupérable s’arrête.</span><span class="sxs-lookup"><span data-stu-id="f11f3-157">Fatal exit terminates.</span></span> <span data-ttu-id="f11f3-158">Utilisé avec les boîtes de dialogue [FatalError](fatalerror-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="f11f3-158">Used with a [FatalError](fatalerror-dialog.md) dialog boxes.</span></span> |
| <span data-ttu-id="f11f3-159">msiDoActionStatusSuspend</span><span class="sxs-lookup"><span data-stu-id="f11f3-159">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="f11f3-160">-4</span><span class="sxs-lookup"><span data-stu-id="f11f3-160">-4</span></span>    | <span data-ttu-id="f11f3-161">L’installation est suspendue.</span><span class="sxs-lookup"><span data-stu-id="f11f3-161">Install is suspended.</span></span>                                                                |



 

<span data-ttu-id="f11f3-162">Zéro, tous les autres nombres négatifs ou une valeur null indique que l’action n’est jamais exécutée.</span><span class="sxs-lookup"><span data-stu-id="f11f3-162">Zero, all other negative numbers, or a Null value indicate that the action is never run.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f11f3-163">Notes</span><span class="sxs-lookup"><span data-stu-id="f11f3-163">Remarks</span></span>

<span data-ttu-id="f11f3-164">Le texte localisé pour l’affichage ou la journalisation de la progression est spécifié dans la [table ActionText](actiontext-table.md).</span><span class="sxs-lookup"><span data-stu-id="f11f3-164">Localized text for progress display or logging is specified in the [ActionText table](actiontext-table.md).</span></span>

<span data-ttu-id="f11f3-165">Pour obtenir un exemple de table de séquences, consultez [utilisation d’une table de séquences](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="f11f3-165">For an example of a sequence table, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="f11f3-166">Validation</span><span class="sxs-lookup"><span data-stu-id="f11f3-166">Validation</span></span>

<dl>

[<span data-ttu-id="f11f3-167">ICE03</span><span class="sxs-lookup"><span data-stu-id="f11f3-167">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="f11f3-168">ICE06</span><span class="sxs-lookup"><span data-stu-id="f11f3-168">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="f11f3-169">ICE12</span><span class="sxs-lookup"><span data-stu-id="f11f3-169">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="f11f3-170">ICE13</span><span class="sxs-lookup"><span data-stu-id="f11f3-170">ICE13</span></span>](ice13.md)  
[<span data-ttu-id="f11f3-171">ICE26</span><span class="sxs-lookup"><span data-stu-id="f11f3-171">ICE26</span></span>](ice26.md)  
[<span data-ttu-id="f11f3-172">ICE27</span><span class="sxs-lookup"><span data-stu-id="f11f3-172">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="f11f3-173">ICE28</span><span class="sxs-lookup"><span data-stu-id="f11f3-173">ICE28</span></span>](ice28.md)  
[<span data-ttu-id="f11f3-174">ICE46</span><span class="sxs-lookup"><span data-stu-id="f11f3-174">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="f11f3-175">ICE63</span><span class="sxs-lookup"><span data-stu-id="f11f3-175">ICE63</span></span>](ice63.md)  
[<span data-ttu-id="f11f3-176">ICE75</span><span class="sxs-lookup"><span data-stu-id="f11f3-176">ICE75</span></span>](ice75.md)  
[<span data-ttu-id="f11f3-177">ICE77</span><span class="sxs-lookup"><span data-stu-id="f11f3-177">ICE77</span></span>](ice77.md)  
[<span data-ttu-id="f11f3-178">ICE79</span><span class="sxs-lookup"><span data-stu-id="f11f3-178">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="f11f3-179">ICE82</span><span class="sxs-lookup"><span data-stu-id="f11f3-179">ICE82</span></span>](ice82.md)  
[<span data-ttu-id="f11f3-180">ICE83</span><span class="sxs-lookup"><span data-stu-id="f11f3-180">ICE83</span></span>](ice83.md)  
[<span data-ttu-id="f11f3-181">ICE84</span><span class="sxs-lookup"><span data-stu-id="f11f3-181">ICE84</span></span>](ice84.md)  
[<span data-ttu-id="f11f3-182">ICE86</span><span class="sxs-lookup"><span data-stu-id="f11f3-182">ICE86</span></span>](ice86.md)  
</dl>

 

 



