---
description: ICE69 vérifie que toutes les sous-chaînes de la forme \[ $componentkey \] dans une chaîne mise en forme ne font pas référence à des composants.
ms.assetid: 6ab8f3b7-19e9-46f3-b09e-36bdb43d6f55
title: ICE69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95bd00efc6b141bfa872470adcc9e88a63a2c52d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209902"
---
# <a name="ice69"></a><span data-ttu-id="345f0-103">ICE69</span><span class="sxs-lookup"><span data-stu-id="345f0-103">ICE69</span></span>

<span data-ttu-id="345f0-104">ICE69 vérifie que toutes les sous-chaînes de la forme \[ $componentkey \] dans une chaîne [mise en forme](formatted.md) ne font pas référence à des composants.</span><span class="sxs-lookup"><span data-stu-id="345f0-104">ICE69 checks that all substrings of the form \[$componentkey\] within a [formatted](formatted.md) string do not cross-reference components.</span></span> <span data-ttu-id="345f0-105">Une référence entre composants se produit lorsque la \[ \] propriété $componentkey d’une chaîne mise en forme fait référence à un composant autre que le composant stocké dans la \_ colonne composant de vos tables.</span><span class="sxs-lookup"><span data-stu-id="345f0-105">A cross-component reference occurs when the \[$componentkey\] property of a formatted string refers to a component other than the component stored in the Component\_ column of your tables.</span></span>

<span data-ttu-id="345f0-106">Les problèmes de référencement entre composants proviennent de la façon dont les chaînes [mises en forme](formatted.md) sont évaluées.</span><span class="sxs-lookup"><span data-stu-id="345f0-106">Problems with cross-component referencing arise from the way [formatted](formatted.md) strings are evaluated.</span></span> <span data-ttu-id="345f0-107">Si le composant référencé avec la \[ propriété $componentkey \] est déjà installé et n’est pas modifié pendant l’installation actuelle (par exemple, s’il est réinstallé, déplacé vers la source, etc.), l’expression \[ $componentkey \] prend la valeur null, car l’état d’action du composant dans \[ $componentkey \] est null.</span><span class="sxs-lookup"><span data-stu-id="345f0-107">If the component referenced with the \[$componentkey\] property is already installed and is not being changed during the current installation (for example, being reinstalled, moved to source, and so forth), the expression \[$componentkey\] evaluates to null, because the action state of the component in \[$componentkey\] is null.</span></span> <span data-ttu-id="345f0-108">Des problèmes similaires peuvent se produire pendant les opérations de mise à niveau et de réparation.</span><span class="sxs-lookup"><span data-stu-id="345f0-108">Similar problems can occur during upgrade and repair operations.</span></span>

## <a name="result"></a><span data-ttu-id="345f0-109">Résultats</span><span class="sxs-lookup"><span data-stu-id="345f0-109">Result</span></span>

<span data-ttu-id="345f0-110">ICE69 retourne une erreur si un \[ $componentkey \] sous-chaîne d’une chaîne [mise en forme](formatted.md) fait référence à un composant d’une autre fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="345f0-110">ICE69 returns an error if a \[$componentkey\] substring within a [formatted](formatted.md) string cross-references a component in another feature.</span></span> <span data-ttu-id="345f0-111">ICE69 retourne un avertissement si un \[ $componentkey \] sous-chaîne d’une chaîne mise en forme fait référence à un composant dans la même fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="345f0-111">ICE69 returns a warning if a \[$componentkey\] substring within a formatted string cross-references a component in the same feature.</span></span> <span data-ttu-id="345f0-112">(La table [FeatureComponents](featurecomponents-table.md) est utilisée pour déterminer ce mappage.</span><span class="sxs-lookup"><span data-stu-id="345f0-112">(The [FeatureComponents](featurecomponents-table.md) table is used to determine this mapping.</span></span> <span data-ttu-id="345f0-113">Elle doit être mappée à la même fonctionnalité pour l’avertissement.</span><span class="sxs-lookup"><span data-stu-id="345f0-113">It must map to the same feature for the warning.</span></span> <span data-ttu-id="345f0-114">Le fait de référencer des composants dans des fonctionnalités parentes ou de référencer des composants dans des fonctionnalités enfants est considéré comme une erreur.)</span><span class="sxs-lookup"><span data-stu-id="345f0-114">Referencing components in parent features or referencing components in child features is considered to be an error.)</span></span>

<span data-ttu-id="345f0-115">ICE69 signale une erreur si la \[ \# \] sous-chaîne FileKey dans une chaîne [mise en forme](formatted.md) fait référence à un fichier qui n’est pas spécifié dans la table de [fichiers](file-table.md) comme appartenant au même composant.</span><span class="sxs-lookup"><span data-stu-id="345f0-115">ICE69 reports an error if the \[\#FileKey\] substring within a [formatted](formatted.md) string references a file which is not specified in the [File](file-table.md) table as belonging to the same component.</span></span>

## <a name="example"></a><span data-ttu-id="345f0-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="345f0-116">Example</span></span>

<span data-ttu-id="345f0-117">ICE69 signale les éléments suivants pour les exemples indiqués.</span><span class="sxs-lookup"><span data-stu-id="345f0-117">ICE69 reports the following for the examples shown.</span></span>

``` syntax
WARNING: "Mismatched component reference. Entry 'Test' of the Shortcut table belongs to component 'QuickTest'. However, the formatted string in column 'Argument' references component 'Test'. Components are in the same feature."
ERROR: "Mismatched component reference. Entry 'Shortcut2' of the Shortcut table belongs to component 'QuickTest'. However, the formatted string in column 'Argument' references component 'Test2'. Components are not in the same feature."
```

<span data-ttu-id="345f0-118">Pour corriger cette erreur, ne faites pas référence à des composants.</span><span class="sxs-lookup"><span data-stu-id="345f0-118">To fix this error, do not cross-reference components.</span></span> <span data-ttu-id="345f0-119">Modifiez le \[ $componentkey \] pour qu’il corresponde au composant du raccourci.</span><span class="sxs-lookup"><span data-stu-id="345f0-119">Change the \[$componentkey\] to match the component of the shortcut.</span></span>

<span data-ttu-id="345f0-120">[Table de raccourcis](shortcut-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="345f0-120">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="345f0-121">Raccourci</span><span class="sxs-lookup"><span data-stu-id="345f0-121">Shortcut</span></span>  | <span data-ttu-id="345f0-122">-\_</span><span class="sxs-lookup"><span data-stu-id="345f0-122">Component\_</span></span> | <span data-ttu-id="345f0-123">Argument</span><span class="sxs-lookup"><span data-stu-id="345f0-123">Argument</span></span>     |
|-----------|-------------|--------------|
| <span data-ttu-id="345f0-124">Test</span><span class="sxs-lookup"><span data-stu-id="345f0-124">Test</span></span>      | <span data-ttu-id="345f0-125">QuickTest</span><span class="sxs-lookup"><span data-stu-id="345f0-125">QuickTest</span></span>   | <span data-ttu-id="345f0-126">$Test-v \[\]</span><span class="sxs-lookup"><span data-stu-id="345f0-126">-v \[$Test\]</span></span> |
| <span data-ttu-id="345f0-127">Shortcut2</span><span class="sxs-lookup"><span data-stu-id="345f0-127">Shortcut2</span></span> | <span data-ttu-id="345f0-128">QuickTest</span><span class="sxs-lookup"><span data-stu-id="345f0-128">QuickTest</span></span>   | <span data-ttu-id="345f0-129">\[$Test 2\]</span><span class="sxs-lookup"><span data-stu-id="345f0-129">\[$Test2\]</span></span>   |



 

<span data-ttu-id="345f0-130">Les tables de [verbes](verb-table.md) et d' [Extensions](extension-table.md) sont des cas spéciaux dans le cas où la table de verbes fait référence à une extension qui appartient à un composant.</span><span class="sxs-lookup"><span data-stu-id="345f0-130">The [Verb](verb-table.md) and [Extension](extension-table.md) tables are special cases in that the Verb table references an extension that belongs to a component.</span></span> <span data-ttu-id="345f0-131">Toutefois, une extension peut appartenir à plusieurs composants, car la clé primaire de la table d’extension est constituée des colonnes d’extension et de composant \_ .</span><span class="sxs-lookup"><span data-stu-id="345f0-131">An Extension, however, can belong to multiple components because the primary key for the extension table is made up of the Extension and Component\_ columns.</span></span> <span data-ttu-id="345f0-132">Vous pouvez logiquement avoir la situation suivante.</span><span class="sxs-lookup"><span data-stu-id="345f0-132">You can logically have the following situation.</span></span>

<span data-ttu-id="345f0-133">[Table de verbes](verb-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="345f0-133">[Verb Table](verb-table.md) (partial)</span></span>



| <span data-ttu-id="345f0-134">Extension</span><span class="sxs-lookup"><span data-stu-id="345f0-134">Extension</span></span> | <span data-ttu-id="345f0-135">Verbe\_</span><span class="sxs-lookup"><span data-stu-id="345f0-135">Verb\_</span></span> | <span data-ttu-id="345f0-136">Argument</span><span class="sxs-lookup"><span data-stu-id="345f0-136">Argument</span></span>                |
|-----------|--------|-------------------------|
| <span data-ttu-id="345f0-137">TST</span><span class="sxs-lookup"><span data-stu-id="345f0-137">tst</span></span>       | <span data-ttu-id="345f0-138">ouvert</span><span class="sxs-lookup"><span data-stu-id="345f0-138">open</span></span>   | <span data-ttu-id="345f0-139">-v \[ $COMP 1 \] \[ $COMP 2\]</span><span class="sxs-lookup"><span data-stu-id="345f0-139">-v \[$comp1\]\[$comp2\]</span></span> |



 

<span data-ttu-id="345f0-140">[Table d’extension](extension-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="345f0-140">[Extension Table](extension-table.md) (partial)</span></span>



| <span data-ttu-id="345f0-141">Extension</span><span class="sxs-lookup"><span data-stu-id="345f0-141">Extension</span></span> | <span data-ttu-id="345f0-142">-\_</span><span class="sxs-lookup"><span data-stu-id="345f0-142">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="345f0-143">TST</span><span class="sxs-lookup"><span data-stu-id="345f0-143">tst</span></span>       | <span data-ttu-id="345f0-144">COMP1</span><span class="sxs-lookup"><span data-stu-id="345f0-144">comp1</span></span>       |
| <span data-ttu-id="345f0-145">TST</span><span class="sxs-lookup"><span data-stu-id="345f0-145">tst</span></span>       | <span data-ttu-id="345f0-146">COMP2</span><span class="sxs-lookup"><span data-stu-id="345f0-146">comp2</span></span>       |



 

[<span data-ttu-id="345f0-147">Table FeatureComponents</span><span class="sxs-lookup"><span data-stu-id="345f0-147">FeatureComponents Table</span></span>](featurecomponents-table.md)



| <span data-ttu-id="345f0-148">Fonctionnalité\_</span><span class="sxs-lookup"><span data-stu-id="345f0-148">Feature\_</span></span> | <span data-ttu-id="345f0-149">-\_</span><span class="sxs-lookup"><span data-stu-id="345f0-149">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="345f0-150">Feature1</span><span class="sxs-lookup"><span data-stu-id="345f0-150">Feature1</span></span>  | <span data-ttu-id="345f0-151">QuickTest</span><span class="sxs-lookup"><span data-stu-id="345f0-151">QuickTest</span></span>   |
| <span data-ttu-id="345f0-152">Feature1</span><span class="sxs-lookup"><span data-stu-id="345f0-152">Feature1</span></span>  | <span data-ttu-id="345f0-153">Test</span><span class="sxs-lookup"><span data-stu-id="345f0-153">Test</span></span>        |
| <span data-ttu-id="345f0-154">Feature2</span><span class="sxs-lookup"><span data-stu-id="345f0-154">Feature2</span></span>  | <span data-ttu-id="345f0-155">Test 2</span><span class="sxs-lookup"><span data-stu-id="345f0-155">Test2</span></span>       |



 

<span data-ttu-id="345f0-156">Dans ce cas, vous devez vous assurer qu’au moins une des \[ Propriétés de $componentkey \] correspond à une valeur non null.</span><span class="sxs-lookup"><span data-stu-id="345f0-156">In this case, you must ensure that at least one of the \[$componentkey\] properties evaluates to a non-null value.</span></span> <span data-ttu-id="345f0-157">Toutefois, chaque \[ \] propriété $componentkey dans la colonne argument de la table de verbes ( \[ $comp 1 \] et \[ $COMP 2 \] dans l’exemple ci-dessus) doit référencer un composant possible inclus avec l’extension associée au verbe.</span><span class="sxs-lookup"><span data-stu-id="345f0-157">However, every \[$componentkey\] property in the Argument column of the Verb table (\[$comp1\] and \[$comp2\] in the above example) must reference a possible component included with the extension associated with the verb.</span></span> <span data-ttu-id="345f0-158">Une référence comme \[ $COMP 3 \] génère un avertissement à partir de ICE69.</span><span class="sxs-lookup"><span data-stu-id="345f0-158">A reference like \[$comp3\] would result in a warning from ICE69.</span></span>

<span data-ttu-id="345f0-159">La [table AppID](appid-table.md) présente une situation similaire à celle de la table de verbes.</span><span class="sxs-lookup"><span data-stu-id="345f0-159">The [AppId table](appid-table.md) has a similar situation to the Verb table.</span></span> <span data-ttu-id="345f0-160">Elle utilise la [table de classe](class-table.md) pour sa référence de composant.</span><span class="sxs-lookup"><span data-stu-id="345f0-160">It uses the [Class table](class-table.md) for its component reference.</span></span> <span data-ttu-id="345f0-161">Dans ce cas, la table AppId est validée de la même façon que la validation Verb-Extension (désormais AppId-Class).</span><span class="sxs-lookup"><span data-stu-id="345f0-161">In this case, the AppId table is validated in the same way as the Verb-Extension validation (now AppId-Class).</span></span>

<span data-ttu-id="345f0-162">La colonne argument de la table de classes est validée comme le [raccourci](shortcut-table.md), le [registre](registry-table.md)et les tables similaires.</span><span class="sxs-lookup"><span data-stu-id="345f0-162">The Class table's Argument column is validated like the [Shortcut](shortcut-table.md), [Registry](registry-table.md), and similar tables.</span></span>

## <a name="table-used-during-execution-only-if-found"></a><span data-ttu-id="345f0-163">Table utilisée lors de l’exécution (uniquement si elle est trouvée)</span><span class="sxs-lookup"><span data-stu-id="345f0-163">Table used during execution (only if found)</span></span>

[<span data-ttu-id="345f0-164">IniFile</span><span class="sxs-lookup"><span data-stu-id="345f0-164">IniFile</span></span>](inifile-table.md)

[<span data-ttu-id="345f0-165">RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="345f0-165">RemoveIniFile</span></span>](removeinifile-table.md)

[<span data-ttu-id="345f0-166">Registre</span><span class="sxs-lookup"><span data-stu-id="345f0-166">Registry</span></span>](registry-table.md)

[<span data-ttu-id="345f0-167">RemoveRegistry</span><span class="sxs-lookup"><span data-stu-id="345f0-167">RemoveRegistry</span></span>](removeregistry-table.md)

[<span data-ttu-id="345f0-168">ServiceControl</span><span class="sxs-lookup"><span data-stu-id="345f0-168">ServiceControl</span></span>](servicecontrol-table.md)

[<span data-ttu-id="345f0-169">ServiceInstall</span><span class="sxs-lookup"><span data-stu-id="345f0-169">ServiceInstall</span></span>](serviceinstall-table.md)

[<span data-ttu-id="345f0-170">Raccourci</span><span class="sxs-lookup"><span data-stu-id="345f0-170">Shortcut</span></span>](shortcut-table.md)

[<span data-ttu-id="345f0-171">Verbe</span><span class="sxs-lookup"><span data-stu-id="345f0-171">Verb</span></span>](verb-table.md)

[<span data-ttu-id="345f0-172">Extension</span><span class="sxs-lookup"><span data-stu-id="345f0-172">Extension</span></span>](extension-table.md)

[<span data-ttu-id="345f0-173">Classe</span><span class="sxs-lookup"><span data-stu-id="345f0-173">Class</span></span>](class-table.md)

[<span data-ttu-id="345f0-174">AppId</span><span class="sxs-lookup"><span data-stu-id="345f0-174">AppId</span></span>](appid-table.md)

[<span data-ttu-id="345f0-175">Environment</span><span class="sxs-lookup"><span data-stu-id="345f0-175">Environment</span></span>](environment-table.md)

## <a name="related-topics"></a><span data-ttu-id="345f0-176">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="345f0-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="345f0-177">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="345f0-177">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



