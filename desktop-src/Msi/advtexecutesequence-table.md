---
description: Le tableau AdvtExecuteSequence répertorie les actions que le programme d’installation appelle lorsque l’action de publication de niveau supérieur est exécutée.
ms.assetid: 8873c161-a709-48b8-a66f-fe2ee9be859f
title: Table AdvtExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b68a3f69cc7473b2364f169545743941d752f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864505"
---
# <a name="advtexecutesequence-table"></a><span data-ttu-id="7ffa9-103">Table AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="7ffa9-103">AdvtExecuteSequence Table</span></span>

<span data-ttu-id="7ffa9-104">Le tableau AdvtExecuteSequence répertorie les actions que le programme d’installation appelle lorsque l' [action de publication](advertise-action.md) de niveau supérieur est exécutée.</span><span class="sxs-lookup"><span data-stu-id="7ffa9-104">The AdvtExecuteSequence table lists actions the installer calls when the top-level [ADVERTISE action](advertise-action.md) is executed.</span></span>

<span data-ttu-id="7ffa9-105">Seules les actions suivantes peuvent être utilisées dans la table AdvtExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="7ffa9-105">Only the following actions can be used in the AdvtExecuteSequence table.</span></span> <span data-ttu-id="7ffa9-106">Les actions personnalisées ne peuvent pas être utilisées dans cette table.</span><span class="sxs-lookup"><span data-stu-id="7ffa9-106">Custom actions cannot be used in this table.</span></span>

[<span data-ttu-id="7ffa9-107">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="7ffa9-107">CostFinalize</span></span>](costfinalize-action.md)

[<span data-ttu-id="7ffa9-108">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="7ffa9-108">CostInitialize</span></span>](costinitialize-action.md)

[<span data-ttu-id="7ffa9-109">CreateShortcuts</span><span class="sxs-lookup"><span data-stu-id="7ffa9-109">CreateShortcuts</span></span>](createshortcuts-action.md)

[<span data-ttu-id="7ffa9-110">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="7ffa9-110">InstallFinalize</span></span>](installfinalize-action.md)

[<span data-ttu-id="7ffa9-111">InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="7ffa9-111">InstallInitialize</span></span>](installinitialize-action.md)

[<span data-ttu-id="7ffa9-112">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="7ffa9-112">InstallValidate</span></span>](installvalidate-action.md)

[<span data-ttu-id="7ffa9-113">MsiPublishAssemblies</span><span class="sxs-lookup"><span data-stu-id="7ffa9-113">MsiPublishAssemblies</span></span>](msipublishassemblies-action.md)

[<span data-ttu-id="7ffa9-114">PublishComponents</span><span class="sxs-lookup"><span data-stu-id="7ffa9-114">PublishComponents</span></span>](publishcomponents-action.md)

[<span data-ttu-id="7ffa9-115">PublishFeatures</span><span class="sxs-lookup"><span data-stu-id="7ffa9-115">PublishFeatures</span></span>](publishfeatures-action.md)

[<span data-ttu-id="7ffa9-116">PublishProduct</span><span class="sxs-lookup"><span data-stu-id="7ffa9-116">PublishProduct</span></span>](publishproduct-action.md)

[<span data-ttu-id="7ffa9-117">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="7ffa9-117">RegisterClassInfo</span></span>](registerclassinfo-action.md)

[<span data-ttu-id="7ffa9-118">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="7ffa9-118">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)

[<span data-ttu-id="7ffa9-119">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="7ffa9-119">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

[<span data-ttu-id="7ffa9-120">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="7ffa9-120">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)

<span data-ttu-id="7ffa9-121">Les colonnes sont identiques à celles de la [table InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="7ffa9-121">The columns are identical to those of the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="7ffa9-122">La table AdvtExecuteSequence contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="7ffa9-122">The AdvtExecuteSequence table has the following columns.</span></span>



| <span data-ttu-id="7ffa9-123">Colonne</span><span class="sxs-lookup"><span data-stu-id="7ffa9-123">Column</span></span>    | <span data-ttu-id="7ffa9-124">Type</span><span class="sxs-lookup"><span data-stu-id="7ffa9-124">Type</span></span>                         | <span data-ttu-id="7ffa9-125">Clé</span><span class="sxs-lookup"><span data-stu-id="7ffa9-125">Key</span></span> | <span data-ttu-id="7ffa9-126">Nullable</span><span class="sxs-lookup"><span data-stu-id="7ffa9-126">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="7ffa9-127">Action</span><span class="sxs-lookup"><span data-stu-id="7ffa9-127">Action</span></span>    | [<span data-ttu-id="7ffa9-128">Identificateur</span><span class="sxs-lookup"><span data-stu-id="7ffa9-128">Identifier</span></span>](identifier.md) | <span data-ttu-id="7ffa9-129">O</span><span class="sxs-lookup"><span data-stu-id="7ffa9-129">Y</span></span>   | <span data-ttu-id="7ffa9-130">N</span><span class="sxs-lookup"><span data-stu-id="7ffa9-130">N</span></span>        |
| <span data-ttu-id="7ffa9-131">Condition</span><span class="sxs-lookup"><span data-stu-id="7ffa9-131">Condition</span></span> | [<span data-ttu-id="7ffa9-132">Condition</span><span class="sxs-lookup"><span data-stu-id="7ffa9-132">Condition</span></span>](condition.md)   | <span data-ttu-id="7ffa9-133">N</span><span class="sxs-lookup"><span data-stu-id="7ffa9-133">N</span></span>   | <span data-ttu-id="7ffa9-134">O</span><span class="sxs-lookup"><span data-stu-id="7ffa9-134">Y</span></span>        |
| <span data-ttu-id="7ffa9-135">Séquence</span><span class="sxs-lookup"><span data-stu-id="7ffa9-135">Sequence</span></span>  | [<span data-ttu-id="7ffa9-136">Integer</span><span class="sxs-lookup"><span data-stu-id="7ffa9-136">Integer</span></span>](integer.md)       | <span data-ttu-id="7ffa9-137">N</span><span class="sxs-lookup"><span data-stu-id="7ffa9-137">N</span></span>   | <span data-ttu-id="7ffa9-138">O</span><span class="sxs-lookup"><span data-stu-id="7ffa9-138">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="7ffa9-139">Colonnes</span><span class="sxs-lookup"><span data-stu-id="7ffa9-139">Columns</span></span>

<dl> <dt>

<span data-ttu-id="7ffa9-140"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Transactionnel</span><span class="sxs-lookup"><span data-stu-id="7ffa9-140"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="7ffa9-141">Nom de l' [action standard](standard-actions.md) que le programme d’installation doit exécuter.</span><span class="sxs-lookup"><span data-stu-id="7ffa9-141">Name of the [standard action](standard-actions.md) the installer is to execute.</span></span> <span data-ttu-id="7ffa9-142">Il s’agit de la clé primaire de la table.</span><span class="sxs-lookup"><span data-stu-id="7ffa9-142">This is the primary key of the table.</span></span>

</dd> <dt>

<span data-ttu-id="7ffa9-143"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Etat</span><span class="sxs-lookup"><span data-stu-id="7ffa9-143"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="7ffa9-144">Expression logique.</span><span class="sxs-lookup"><span data-stu-id="7ffa9-144">Logical expression.</span></span> <span data-ttu-id="7ffa9-145">Si l’expression prend la valeur false, l’action est ignorée.</span><span class="sxs-lookup"><span data-stu-id="7ffa9-145">If the expression evaluates to false, the action is skipped.</span></span> <span data-ttu-id="7ffa9-146">Si la syntaxe de l’expression n’est pas valide, la séquence se termine et retourne iesBadActionData.</span><span class="sxs-lookup"><span data-stu-id="7ffa9-146">If the expression syntax is invalid, the sequence terminates, returning iesBadActionData.</span></span> <span data-ttu-id="7ffa9-147">Pour plus d’informations sur la syntaxe des instructions conditionnelles, consultez [syntaxe d’instruction conditionnelle](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="7ffa9-147">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ffa9-148"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Séquence</span><span class="sxs-lookup"><span data-stu-id="7ffa9-148"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="7ffa9-149">Une valeur positive indique la position de séquence de l’action.</span><span class="sxs-lookup"><span data-stu-id="7ffa9-149">A positive value indicates the sequence position of the action.</span></span> <span data-ttu-id="7ffa9-150">Les valeurs négatives suivantes indiquent que l’action est appelée si le programme d’installation retourne l’indicateur d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="7ffa9-150">The following negative values indicate that the action is called if the installer returns the termination flag.</span></span> <span data-ttu-id="7ffa9-151">Chaque indicateur de fin (valeur négative) peut être utilisé avec une seule action.</span><span class="sxs-lookup"><span data-stu-id="7ffa9-151">Each termination flag (negative value) can be used with no more than one action.</span></span> <span data-ttu-id="7ffa9-152">Plusieurs actions peuvent avoir des indicateurs d’arrêt, mais elles doivent être des indicateurs différents.</span><span class="sxs-lookup"><span data-stu-id="7ffa9-152">Multiple actions can have termination flags, but they must be different flags.</span></span> <span data-ttu-id="7ffa9-153">Les indicateurs de fin (valeurs négatives) sont généralement utilisés avec les [boîtes de dialogue](dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="7ffa9-153">Termination flags (negative values) are typically used with [Dialog Boxes](dialog-boxes.md).</span></span>



| <span data-ttu-id="7ffa9-154">Indicateur de fin</span><span class="sxs-lookup"><span data-stu-id="7ffa9-154">Termination flag</span></span>          | <span data-ttu-id="7ffa9-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ffa9-155">Value</span></span> | <span data-ttu-id="7ffa9-156">Description</span><span class="sxs-lookup"><span data-stu-id="7ffa9-156">Description</span></span>                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7ffa9-157">msiDoActionStatusSuccess</span><span class="sxs-lookup"><span data-stu-id="7ffa9-157">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="7ffa9-158">-1</span><span class="sxs-lookup"><span data-stu-id="7ffa9-158">-1</span></span>    | <span data-ttu-id="7ffa9-159">Achèvement réussi.</span><span class="sxs-lookup"><span data-stu-id="7ffa9-159">Successful completion.</span></span> <span data-ttu-id="7ffa9-160">Utilisé avec les boîtes de dialogue [quitter](exit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="7ffa9-160">Used with [Exit](exit-dialog.md) dialog boxes.</span></span>               |
| <span data-ttu-id="7ffa9-161">msiDoActionStatusUserExit</span><span class="sxs-lookup"><span data-stu-id="7ffa9-161">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="7ffa9-162">-2</span><span class="sxs-lookup"><span data-stu-id="7ffa9-162">-2</span></span>    | <span data-ttu-id="7ffa9-163">L’utilisateur termine l’installation.</span><span class="sxs-lookup"><span data-stu-id="7ffa9-163">User terminates install.</span></span> <span data-ttu-id="7ffa9-164">Utilisé avec les boîtes de dialogue [UserExit](userexit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="7ffa9-164">Used with [UserExit](userexit-dialog.md) dialog boxes.</span></span>     |
| <span data-ttu-id="7ffa9-165">msiDoActionStatusFailure</span><span class="sxs-lookup"><span data-stu-id="7ffa9-165">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="7ffa9-166">-3</span><span class="sxs-lookup"><span data-stu-id="7ffa9-166">-3</span></span>    | <span data-ttu-id="7ffa9-167">La sortie irrécupérable s’arrête.</span><span class="sxs-lookup"><span data-stu-id="7ffa9-167">Fatal exit terminates.</span></span> <span data-ttu-id="7ffa9-168">Utilisé avec les boîtes de dialogue [FatalError](fatalerror-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="7ffa9-168">Used with a [FatalError](fatalerror-dialog.md) dialog boxes.</span></span> |
| <span data-ttu-id="7ffa9-169">msiDoActionStatusSuspend</span><span class="sxs-lookup"><span data-stu-id="7ffa9-169">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="7ffa9-170">-4</span><span class="sxs-lookup"><span data-stu-id="7ffa9-170">-4</span></span>    | <span data-ttu-id="7ffa9-171">L’installation est suspendue.</span><span class="sxs-lookup"><span data-stu-id="7ffa9-171">Install is suspended.</span></span>                                                                |



 

<span data-ttu-id="7ffa9-172">Zéro, tous les autres nombres négatifs ou une valeur null indique que l’action n’est jamais appelée.</span><span class="sxs-lookup"><span data-stu-id="7ffa9-172">Zero, all other negative numbers, or a null value indicate that the action is never called.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="7ffa9-173">Validation</span><span class="sxs-lookup"><span data-stu-id="7ffa9-173">Validation</span></span>

<dl>

[<span data-ttu-id="7ffa9-174">ICE03</span><span class="sxs-lookup"><span data-stu-id="7ffa9-174">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="7ffa9-175">ICE06</span><span class="sxs-lookup"><span data-stu-id="7ffa9-175">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="7ffa9-176">ICE12</span><span class="sxs-lookup"><span data-stu-id="7ffa9-176">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="7ffa9-177">ICE13</span><span class="sxs-lookup"><span data-stu-id="7ffa9-177">ICE13</span></span>](ice13.md)  
[<span data-ttu-id="7ffa9-178">ICE27</span><span class="sxs-lookup"><span data-stu-id="7ffa9-178">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="7ffa9-179">ICE46</span><span class="sxs-lookup"><span data-stu-id="7ffa9-179">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="7ffa9-180">ICE72</span><span class="sxs-lookup"><span data-stu-id="7ffa9-180">ICE72</span></span>](ice72.md)  
[<span data-ttu-id="7ffa9-181">ICE79</span><span class="sxs-lookup"><span data-stu-id="7ffa9-181">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="7ffa9-182">ICE82</span><span class="sxs-lookup"><span data-stu-id="7ffa9-182">ICE82</span></span>](ice82.md)  
[<span data-ttu-id="7ffa9-183">ICE83</span><span class="sxs-lookup"><span data-stu-id="7ffa9-183">ICE83</span></span>](ice83.md)  
[<span data-ttu-id="7ffa9-184">ICE84</span><span class="sxs-lookup"><span data-stu-id="7ffa9-184">ICE84</span></span>](ice84.md)  
[<span data-ttu-id="7ffa9-185">ICE86</span><span class="sxs-lookup"><span data-stu-id="7ffa9-185">ICE86</span></span>](ice86.md)  
[<span data-ttu-id="7ffa9-186">ICEM04</span><span class="sxs-lookup"><span data-stu-id="7ffa9-186">ICEM04</span></span>](icem04.md)  
</dl>

 

 



