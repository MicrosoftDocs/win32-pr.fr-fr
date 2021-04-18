---
description: Le tableau AdminExecuteSequence répertorie les actions que le programme d’installation appelle en séquence lorsque l’action d’administration de niveau supérieur est exécutée.
ms.assetid: 33a2ef50-519b-424e-b510-55c21c5706a3
title: Table AdminExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c62ae43f8436ab210765e5402751c5722b78b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519869"
---
# <a name="adminexecutesequence-table"></a><span data-ttu-id="4f5fc-103">Table AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="4f5fc-103">AdminExecuteSequence Table</span></span>

<span data-ttu-id="4f5fc-104">Le tableau AdminExecuteSequence répertorie les actions que le programme d’installation appelle en séquence lorsque l' [action d’administration](admin-action.md) de niveau supérieur est exécutée.</span><span class="sxs-lookup"><span data-stu-id="4f5fc-104">The AdminExecuteSequence table lists actions that the installer calls in sequence when the top-level [ADMIN action](admin-action.md) is executed.</span></span>

<span data-ttu-id="4f5fc-105">Les actions d’administration dans la séquence d’installation, jusqu’à l' [action InstallValidate](installvalidate-action.md) et toutes les boîtes de dialogue de sortie, se trouvent dans la [table AdminUISequence](adminuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="4f5fc-105">ADMIN actions in the install sequence, up to the [InstallValidate action](installvalidate-action.md) and any exit dialog boxes, are located in the [AdminUISequence table](adminuisequence-table.md).</span></span>

<span data-ttu-id="4f5fc-106">Les actions d’administration à partir de l’action InstallValidate jusqu’à la fin de la séquence d’installation se trouvent dans la table AdminExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="4f5fc-106">ADMIN actions from the InstallValidate action through the end of the install sequence are in the AdminExecuteSequence table.</span></span> <span data-ttu-id="4f5fc-107">Étant donné que la table AdminExecuteSequence doit être autonome, elle contient également toutes les actions d’initialisation nécessaires, telles que [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md)et [CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="4f5fc-107">Because the AdminExecuteSequence table needs to stand alone, it also contains any necessary initialization actions such as [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md), and [CostFinalize](costfinalize-action.md).</span></span>

<span data-ttu-id="4f5fc-108">Les [actions personnalisées](custom-actions.md) nécessitant une interface utilisateur doivent utiliser [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) au lieu de boîtes de dialogue créées créées à l’aide de la table de [boîtes de dialogue](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="4f5fc-108">[Custom actions](custom-actions.md) requiring a user interface should use [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) instead of authored dialog boxes created using the [Dialog table](dialog-table.md).</span></span>

<span data-ttu-id="4f5fc-109">Les colonnes sont identiques à celles de la [table InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="4f5fc-109">The columns are identical to those of the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="4f5fc-110">La table AdminExecuteSequence contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="4f5fc-110">The AdminExecuteSequence table has the following columns.</span></span>



| <span data-ttu-id="4f5fc-111">Colonne</span><span class="sxs-lookup"><span data-stu-id="4f5fc-111">Column</span></span>    | <span data-ttu-id="4f5fc-112">Type</span><span class="sxs-lookup"><span data-stu-id="4f5fc-112">Type</span></span>                         | <span data-ttu-id="4f5fc-113">Clé</span><span class="sxs-lookup"><span data-stu-id="4f5fc-113">Key</span></span> | <span data-ttu-id="4f5fc-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="4f5fc-114">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="4f5fc-115">Action</span><span class="sxs-lookup"><span data-stu-id="4f5fc-115">Action</span></span>    | [<span data-ttu-id="4f5fc-116">Identificateur</span><span class="sxs-lookup"><span data-stu-id="4f5fc-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="4f5fc-117">O</span><span class="sxs-lookup"><span data-stu-id="4f5fc-117">Y</span></span>   | <span data-ttu-id="4f5fc-118">N</span><span class="sxs-lookup"><span data-stu-id="4f5fc-118">N</span></span>        |
| <span data-ttu-id="4f5fc-119">Condition</span><span class="sxs-lookup"><span data-stu-id="4f5fc-119">Condition</span></span> | [<span data-ttu-id="4f5fc-120">Condition</span><span class="sxs-lookup"><span data-stu-id="4f5fc-120">Condition</span></span>](condition.md)   | <span data-ttu-id="4f5fc-121">N</span><span class="sxs-lookup"><span data-stu-id="4f5fc-121">N</span></span>   | <span data-ttu-id="4f5fc-122">O</span><span class="sxs-lookup"><span data-stu-id="4f5fc-122">Y</span></span>        |
| <span data-ttu-id="4f5fc-123">Séquence</span><span class="sxs-lookup"><span data-stu-id="4f5fc-123">Sequence</span></span>  | [<span data-ttu-id="4f5fc-124">Integer</span><span class="sxs-lookup"><span data-stu-id="4f5fc-124">Integer</span></span>](integer.md)       | <span data-ttu-id="4f5fc-125">N</span><span class="sxs-lookup"><span data-stu-id="4f5fc-125">N</span></span>   | <span data-ttu-id="4f5fc-126">O</span><span class="sxs-lookup"><span data-stu-id="4f5fc-126">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="4f5fc-127">Colonnes</span><span class="sxs-lookup"><span data-stu-id="4f5fc-127">Columns</span></span>

<dl> <dt>

<span data-ttu-id="4f5fc-128"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Transactionnel</span><span class="sxs-lookup"><span data-stu-id="4f5fc-128"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="4f5fc-129">Nom de l’action à exécuter.</span><span class="sxs-lookup"><span data-stu-id="4f5fc-129">Name of the action to execute.</span></span> <span data-ttu-id="4f5fc-130">Il s’agit d’une action standard ou d’une action personnalisée figurant dans la [table CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="4f5fc-130">This is either a standard action or a custom action listed in the [CustomAction table](customaction-table.md).</span></span>

<span data-ttu-id="4f5fc-131">Clé de table primaire.</span><span class="sxs-lookup"><span data-stu-id="4f5fc-131">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="4f5fc-132"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Etat</span><span class="sxs-lookup"><span data-stu-id="4f5fc-132"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="4f5fc-133">Expression logique.</span><span class="sxs-lookup"><span data-stu-id="4f5fc-133">Logical expression.</span></span> <span data-ttu-id="4f5fc-134">Si l’expression prend la valeur false, l’action est ignorée.</span><span class="sxs-lookup"><span data-stu-id="4f5fc-134">If the expression evaluates to false, the action is skipped.</span></span> <span data-ttu-id="4f5fc-135">Si la syntaxe de l’expression n’est pas valide, la séquence se termine et retourne iesBadActionData.</span><span class="sxs-lookup"><span data-stu-id="4f5fc-135">If the expression syntax is invalid, the sequence terminates, returning iesBadActionData.</span></span> <span data-ttu-id="4f5fc-136">Pour plus d’informations sur la syntaxe des instructions conditionnelles, consultez Syntaxe des instructions [conditionnelles](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="4f5fc-136">For information on the syntax of conditional statements see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f5fc-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Séquence</span><span class="sxs-lookup"><span data-stu-id="4f5fc-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="4f5fc-138">Une valeur positive indique la position de séquence de l’action.</span><span class="sxs-lookup"><span data-stu-id="4f5fc-138">A positive value indicates the sequence position of the action.</span></span> <span data-ttu-id="4f5fc-139">Les valeurs négatives suivantes indiquent que l’action est appelée si le programme d’installation retourne l’indicateur d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="4f5fc-139">The following negative values indicate that the action is called if the installer returns the termination flag.</span></span> <span data-ttu-id="4f5fc-140">Chaque indicateur de fin (valeur négative) peut être utilisé avec une seule action.</span><span class="sxs-lookup"><span data-stu-id="4f5fc-140">Each termination flag (negative value) can be used with no more than one action.</span></span> <span data-ttu-id="4f5fc-141">Plusieurs actions peuvent avoir des indicateurs d’arrêt, mais elles doivent être des indicateurs différents.</span><span class="sxs-lookup"><span data-stu-id="4f5fc-141">Multiple actions can have termination flags, but they must be different flags.</span></span> <span data-ttu-id="4f5fc-142">Les indicateurs de fin (valeurs négatives) sont généralement utilisés avec les [boîtes de dialogue](dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="4f5fc-142">Termination flags (negative values) are typically used with [Dialog Boxes](dialog-boxes.md).</span></span>



| <span data-ttu-id="4f5fc-143">Indicateur de fin</span><span class="sxs-lookup"><span data-stu-id="4f5fc-143">Termination flag</span></span>          | <span data-ttu-id="4f5fc-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f5fc-144">Value</span></span> | <span data-ttu-id="4f5fc-145">Description</span><span class="sxs-lookup"><span data-stu-id="4f5fc-145">Description</span></span>                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4f5fc-146">msiDoActionStatusSuccess</span><span class="sxs-lookup"><span data-stu-id="4f5fc-146">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="4f5fc-147">-1</span><span class="sxs-lookup"><span data-stu-id="4f5fc-147">-1</span></span>    | <span data-ttu-id="4f5fc-148">Achèvement réussi.</span><span class="sxs-lookup"><span data-stu-id="4f5fc-148">Successful completion.</span></span> <span data-ttu-id="4f5fc-149">Utilisé avec les boîtes de dialogue [quitter](exit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="4f5fc-149">Used with [Exit](exit-dialog.md) dialog boxes.</span></span>               |
| <span data-ttu-id="4f5fc-150">msiDoActionStatusUserExit</span><span class="sxs-lookup"><span data-stu-id="4f5fc-150">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="4f5fc-151">-2</span><span class="sxs-lookup"><span data-stu-id="4f5fc-151">-2</span></span>    | <span data-ttu-id="4f5fc-152">L’utilisateur termine l’installation.</span><span class="sxs-lookup"><span data-stu-id="4f5fc-152">User terminates install.</span></span> <span data-ttu-id="4f5fc-153">Utilisé avec les boîtes de dialogue [UserExit](userexit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="4f5fc-153">Used with [UserExit](userexit-dialog.md) dialog boxes.</span></span>     |
| <span data-ttu-id="4f5fc-154">msiDoActionStatusFailure</span><span class="sxs-lookup"><span data-stu-id="4f5fc-154">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="4f5fc-155">-3</span><span class="sxs-lookup"><span data-stu-id="4f5fc-155">-3</span></span>    | <span data-ttu-id="4f5fc-156">La sortie irrécupérable s’arrête.</span><span class="sxs-lookup"><span data-stu-id="4f5fc-156">Fatal exit terminates.</span></span> <span data-ttu-id="4f5fc-157">Utilisé avec les boîtes de dialogue [FatalError](fatalerror-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="4f5fc-157">Used with a [FatalError](fatalerror-dialog.md) dialog boxes.</span></span> |
| <span data-ttu-id="4f5fc-158">msiDoActionStatusSuspend</span><span class="sxs-lookup"><span data-stu-id="4f5fc-158">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="4f5fc-159">-4</span><span class="sxs-lookup"><span data-stu-id="4f5fc-159">-4</span></span>    | <span data-ttu-id="4f5fc-160">L’installation est suspendue.</span><span class="sxs-lookup"><span data-stu-id="4f5fc-160">Install is suspended.</span></span>                                                                |



 

<span data-ttu-id="4f5fc-161">Zéro, tous les autres nombres négatifs ou une valeur null indique que l’action n’est jamais appelée.</span><span class="sxs-lookup"><span data-stu-id="4f5fc-161">Zero, all other negative numbers, or a null value indicate that the action is never called.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="4f5fc-162">Validation</span><span class="sxs-lookup"><span data-stu-id="4f5fc-162">Validation</span></span>

<dl>

[<span data-ttu-id="4f5fc-163">ICE03</span><span class="sxs-lookup"><span data-stu-id="4f5fc-163">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="4f5fc-164">ICE06</span><span class="sxs-lookup"><span data-stu-id="4f5fc-164">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="4f5fc-165">ICE12</span><span class="sxs-lookup"><span data-stu-id="4f5fc-165">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="4f5fc-166">ICE13</span><span class="sxs-lookup"><span data-stu-id="4f5fc-166">ICE13</span></span>](ice13.md)  
[<span data-ttu-id="4f5fc-167">ICE26</span><span class="sxs-lookup"><span data-stu-id="4f5fc-167">ICE26</span></span>](ice26.md)  
[<span data-ttu-id="4f5fc-168">ICE27</span><span class="sxs-lookup"><span data-stu-id="4f5fc-168">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="4f5fc-169">ICE28</span><span class="sxs-lookup"><span data-stu-id="4f5fc-169">ICE28</span></span>](ice28.md)  
[<span data-ttu-id="4f5fc-170">ICE75</span><span class="sxs-lookup"><span data-stu-id="4f5fc-170">ICE75</span></span>](ice75.md)  
[<span data-ttu-id="4f5fc-171">ICE77</span><span class="sxs-lookup"><span data-stu-id="4f5fc-171">ICE77</span></span>](ice77.md)  
[<span data-ttu-id="4f5fc-172">ICE79</span><span class="sxs-lookup"><span data-stu-id="4f5fc-172">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="4f5fc-173">ICE82</span><span class="sxs-lookup"><span data-stu-id="4f5fc-173">ICE82</span></span>](ice82.md)  
[<span data-ttu-id="4f5fc-174">ICE84</span><span class="sxs-lookup"><span data-stu-id="4f5fc-174">ICE84</span></span>](ice84.md)  
[<span data-ttu-id="4f5fc-175">ICE86</span><span class="sxs-lookup"><span data-stu-id="4f5fc-175">ICE86</span></span>](ice86.md)  
[<span data-ttu-id="4f5fc-176">ICEM04</span><span class="sxs-lookup"><span data-stu-id="4f5fc-176">ICEM04</span></span>](icem04.md)  
</dl>

 

 



