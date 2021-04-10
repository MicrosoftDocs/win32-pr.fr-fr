---
description: La table de conditions peut être utilisée pour modifier l’état de sélection d’une entrée dans la table de fonctionnalités en fonction d’une expression conditionnelle.
ms.assetid: 8e2d7c8d-5734-49aa-ad29-16d4d32cccb4
title: Table de conditions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74d9a3c27d43b7d71bc8e5b0593771bc86a3ca4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950987"
---
# <a name="condition-table"></a><span data-ttu-id="9ea96-103">Table de conditions</span><span class="sxs-lookup"><span data-stu-id="9ea96-103">Condition Table</span></span>

<span data-ttu-id="9ea96-104">La table de conditions peut être utilisée pour modifier l’état de sélection d’une entrée dans la [table de fonctionnalités](feature-table.md) en fonction d’une expression conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="9ea96-104">The Condition table can be used to modify the selection state of any entry in the [Feature table](feature-table.md) based on a conditional expression.</span></span>

<span data-ttu-id="9ea96-105">La table de condition contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="9ea96-105">The Condition table has the following columns.</span></span>



| <span data-ttu-id="9ea96-106">Colonne</span><span class="sxs-lookup"><span data-stu-id="9ea96-106">Column</span></span>    | <span data-ttu-id="9ea96-107">Type</span><span class="sxs-lookup"><span data-stu-id="9ea96-107">Type</span></span>                         | <span data-ttu-id="9ea96-108">Clé</span><span class="sxs-lookup"><span data-stu-id="9ea96-108">Key</span></span> | <span data-ttu-id="9ea96-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="9ea96-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="9ea96-110">Fonctionnalité\_</span><span class="sxs-lookup"><span data-stu-id="9ea96-110">Feature\_</span></span> | [<span data-ttu-id="9ea96-111">Identificateur</span><span class="sxs-lookup"><span data-stu-id="9ea96-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="9ea96-112">O</span><span class="sxs-lookup"><span data-stu-id="9ea96-112">Y</span></span>   | <span data-ttu-id="9ea96-113">N</span><span class="sxs-lookup"><span data-stu-id="9ea96-113">N</span></span>        |
| <span data-ttu-id="9ea96-114">Level</span><span class="sxs-lookup"><span data-stu-id="9ea96-114">Level</span></span>     | [<span data-ttu-id="9ea96-115">Integer</span><span class="sxs-lookup"><span data-stu-id="9ea96-115">Integer</span></span>](integer.md)       | <span data-ttu-id="9ea96-116">O</span><span class="sxs-lookup"><span data-stu-id="9ea96-116">Y</span></span>   | <span data-ttu-id="9ea96-117">N</span><span class="sxs-lookup"><span data-stu-id="9ea96-117">N</span></span>        |
| <span data-ttu-id="9ea96-118">Condition</span><span class="sxs-lookup"><span data-stu-id="9ea96-118">Condition</span></span> | [<span data-ttu-id="9ea96-119">Condition</span><span class="sxs-lookup"><span data-stu-id="9ea96-119">Condition</span></span>](condition.md)   | <span data-ttu-id="9ea96-120">N</span><span class="sxs-lookup"><span data-stu-id="9ea96-120">N</span></span>   | <span data-ttu-id="9ea96-121">O</span><span class="sxs-lookup"><span data-stu-id="9ea96-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="9ea96-122">Colonnes</span><span class="sxs-lookup"><span data-stu-id="9ea96-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="9ea96-123"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Fonctionnalité\_</span><span class="sxs-lookup"><span data-stu-id="9ea96-123"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="9ea96-124">Clé externe dans la colonne une du tableau des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="9ea96-124">External key into column one of the Feature table.</span></span>

</dd> <dt>

<span data-ttu-id="9ea96-125"><span id="Level"></span><span id="level"></span><span id="LEVEL"></span>Niveau</span><span class="sxs-lookup"><span data-stu-id="9ea96-125"><span id="Level"></span><span id="level"></span><span id="LEVEL"></span>Level</span></span>
</dt> <dd>

<span data-ttu-id="9ea96-126">Un niveau d’installation conditionnelle pour la fonctionnalité dans la \_ colonne Feature de ce tableau.</span><span class="sxs-lookup"><span data-stu-id="9ea96-126">A conditional install level for the feature in the Feature\_ column of this table.</span></span> <span data-ttu-id="9ea96-127">Le programme d’installation définit le niveau d’installation de cette fonctionnalité au niveau spécifié dans cette colonne si l’expression dans la colonne condition prend la valeur TRUE.</span><span class="sxs-lookup"><span data-stu-id="9ea96-127">The installer sets the install level of this feature to the level specified in this column if the expression in the Condition column evaluates to TRUE.</span></span>

</dd> <dt>

<span data-ttu-id="9ea96-128"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Etat</span><span class="sxs-lookup"><span data-stu-id="9ea96-128"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="9ea96-129">Si cette expression conditionnelle prend la valeur TRUE, la colonne Level de la table Feature est définie sur le niveau d’installation conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="9ea96-129">If this conditional expression evaluates to TRUE, then the Level column in the Feature table is set to the conditional install level.</span></span>

<span data-ttu-id="9ea96-130">L’expression dans la colonne condition ne doit pas contenir de référence à l’état installé d’une fonctionnalité ou d’un composant.</span><span class="sxs-lookup"><span data-stu-id="9ea96-130">The expression in the Condition column should not contain reference to the installed state of any feature or component.</span></span> <span data-ttu-id="9ea96-131">Cela est dû au fait que les expressions de la colonne condition sont évaluées avant que le programme d’installation n’évalue les États installés des fonctionnalités et des composants.</span><span class="sxs-lookup"><span data-stu-id="9ea96-131">This is because the expressions in the Condition column are evaluated before the installer evaluates the installed states of features and components.</span></span> <span data-ttu-id="9ea96-132">Toute expression de la table de condition qui tente de vérifier l’état installé d’une fonctionnalité ou d’un composant prend toujours la valeur false.</span><span class="sxs-lookup"><span data-stu-id="9ea96-132">Any expression in the Condition table that attempts to check the installed state of a feature or component always evaluates to false.</span></span>

<span data-ttu-id="9ea96-133">Pour plus d’informations sur la syntaxe des instructions conditionnelles, consultez [syntaxe d’instruction conditionnelle](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="9ea96-133">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ea96-134">Notes</span><span class="sxs-lookup"><span data-stu-id="9ea96-134">Remarks</span></span>

<span data-ttu-id="9ea96-135">Une fonctionnalité peut être désactivée définitivement en affectant à la colonne niveau la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="9ea96-135">A feature can be permanently disabled by setting the Level column to 0.</span></span>

<span data-ttu-id="9ea96-136">Le niveau peut être défini en fonction d’une instruction conditionnelle, telle qu’un test pour la plateforme, le système d’exploitation ou un paramètre de propriété particulier.</span><span class="sxs-lookup"><span data-stu-id="9ea96-136">The Level may be set based on any conditional statement, such as a test for platform, operating system, or a particular property setting.</span></span>

<span data-ttu-id="9ea96-137">Les conditions doivent être choisies avec soin afin qu’une fonctionnalité ne soit pas activée lors de l’installation, puis désactivée lors de la désinstallation.</span><span class="sxs-lookup"><span data-stu-id="9ea96-137">Conditions should be carefully chosen so that a feature is not enabled on install and then disabled on uninstall.</span></span> <span data-ttu-id="9ea96-138">Cette fonctionnalité est orpheline et le produit ne peut pas être désinstallé.</span><span class="sxs-lookup"><span data-stu-id="9ea96-138">This will orphan the feature and the product will not be able to be uninstalled.</span></span>

<span data-ttu-id="9ea96-139">Cette table est référencée lorsque l' [action CostFinalize](costfinalize-action.md) est exécutée.</span><span class="sxs-lookup"><span data-stu-id="9ea96-139">This table is referred to when the [CostFinalize action](costfinalize-action.md) is executed.</span></span>

<span data-ttu-id="9ea96-140">Si la propriété [**présélectionnée**](preselected.md) a la valeur 1, le programme d’installation n’évalue pas la table de conditions.</span><span class="sxs-lookup"><span data-stu-id="9ea96-140">If the [**Preselected**](preselected.md) property has been set to 1, the installer does not evaluate the Condition table.</span></span> <span data-ttu-id="9ea96-141">La table de condition affecte uniquement l’installation des fonctionnalités lorsqu’aucune des propriétés suivantes n’a été définie :</span><span class="sxs-lookup"><span data-stu-id="9ea96-141">The Condition table affects only the installation of features when none of the following properties have been set:</span></span>

<dl>

[<span data-ttu-id="9ea96-142">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="9ea96-142">**ADDLOCAL**</span></span>](addlocal.md)  
[<span data-ttu-id="9ea96-143">**Installez**</span><span class="sxs-lookup"><span data-stu-id="9ea96-143">**REMOVE**</span></span>](remove.md)  
[<span data-ttu-id="9ea96-144">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="9ea96-144">**ADDSOURCE**</span></span>](addsource.md)  
[<span data-ttu-id="9ea96-145">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="9ea96-145">**ADDDEFAULT**</span></span>](adddefault.md)  
[<span data-ttu-id="9ea96-146">**INSTALLÉ**</span><span class="sxs-lookup"><span data-stu-id="9ea96-146">**REINSTALL**</span></span>](reinstall.md)  
[<span data-ttu-id="9ea96-147">**PUBLIÉS**</span><span class="sxs-lookup"><span data-stu-id="9ea96-147">**ADVERTISE**</span></span>](advertise.md)  
[<span data-ttu-id="9ea96-148">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="9ea96-148">**COMPADDLOCAL**</span></span>](compaddlocal.md)  
[<span data-ttu-id="9ea96-149">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="9ea96-149">**COMPADDSOURCE**</span></span>](compaddsource.md)  
[<span data-ttu-id="9ea96-150">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="9ea96-150">**COMPADDDEFAULT**</span></span>](compadddefault.md)  
[<span data-ttu-id="9ea96-151">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="9ea96-151">**FILEADDLOCAL**</span></span>](fileaddlocal.md)  
[<span data-ttu-id="9ea96-152">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="9ea96-152">**FILEADDSOURCE**</span></span>](fileaddsource.md)  
[<span data-ttu-id="9ea96-153">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="9ea96-153">**FILEADDDEFAULT**</span></span>](fileadddefault.md)  
</dl>

## <a name="validation"></a><span data-ttu-id="9ea96-154">Validation</span><span class="sxs-lookup"><span data-stu-id="9ea96-154">Validation</span></span>

<dl>

[<span data-ttu-id="9ea96-155">ICE03</span><span class="sxs-lookup"><span data-stu-id="9ea96-155">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="9ea96-156">ICE06</span><span class="sxs-lookup"><span data-stu-id="9ea96-156">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="9ea96-157">ICE32</span><span class="sxs-lookup"><span data-stu-id="9ea96-157">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="9ea96-158">ICE46</span><span class="sxs-lookup"><span data-stu-id="9ea96-158">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="9ea96-159">ICE79</span><span class="sxs-lookup"><span data-stu-id="9ea96-159">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="9ea96-160">ICE86</span><span class="sxs-lookup"><span data-stu-id="9ea96-160">ICE86</span></span>](ice86.md)  
</dl>

 

 



