---
description: ICE19 vérifie que les composants publiés font référence à un fichier dans la colonne keyPath de la table Component et qu’un raccourci publié fait référence à un répertoire dans cette colonne.
ms.assetid: 438153c1-bc4b-4ecf-ab85-d66ad69c987c
title: ICE19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a53aa3268a1c77f674d4a130c9de02c44b56243
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203583"
---
# <a name="ice19"></a><span data-ttu-id="3915c-103">ICE19</span><span class="sxs-lookup"><span data-stu-id="3915c-103">ICE19</span></span>

<span data-ttu-id="3915c-104">ICE19 vérifie que les composants publiés font référence à un fichier dans la colonne keyPath de la [table Component](component-table.md) et qu’un raccourci publié fait référence à un répertoire dans cette colonne.</span><span class="sxs-lookup"><span data-stu-id="3915c-104">ICE19 validates that advertised components reference a file in the KeyPath column of the [Component table](component-table.md) and that an advertised shortcut references a directory in this column.</span></span>

<span data-ttu-id="3915c-105">ICE19 vérifie que les composants ou les raccourcis publiés ont un ComponentId.</span><span class="sxs-lookup"><span data-stu-id="3915c-105">ICE19 validates that advertised components or shortcuts have a ComponentId.</span></span> <span data-ttu-id="3915c-106">Les composants de la [table PublishComponent](publishcomponent-table.md), qui ne sont pas publiés dans une autre table, sont uniquement vérifiés pour voir s’ils ont un ComponentID.</span><span class="sxs-lookup"><span data-stu-id="3915c-106">Components in the [PublishComponent table](publishcomponent-table.md), which are not advertised in another table, are only checked to see whether they have a ComponentId.</span></span>

## <a name="result"></a><span data-ttu-id="3915c-107">Résultats</span><span class="sxs-lookup"><span data-stu-id="3915c-107">Result</span></span>

<span data-ttu-id="3915c-108">ICE19 publie un message d’erreur si la colonne keyPath de la table Component ne fait pas référence à un fichier dans le cas d’un composant publié ou d’un répertoire dans le cas d’un raccourci publié.</span><span class="sxs-lookup"><span data-stu-id="3915c-108">ICE19 posts an error message if the KeyPath column of the Component table does not reference a file in the case of an advertised component or a directory in the case of an advertised shortcut.</span></span> <span data-ttu-id="3915c-109">ICE19 publie un message d’erreur si des composants ou des raccourcis publiés n’ont pas d’ID de composant.</span><span class="sxs-lookup"><span data-stu-id="3915c-109">ICE19 posts an error message if any advertised components or shortcuts do not have a ComponentId.</span></span>

## <a name="example"></a><span data-ttu-id="3915c-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="3915c-110">Example</span></span>

<span data-ttu-id="3915c-111">ICE19 publie les messages d’erreur suivants pour l’exemple illustré :</span><span class="sxs-lookup"><span data-stu-id="3915c-111">ICE19 posts the following error messages for the example shown:</span></span>

-   <span data-ttu-id="3915c-112">L’extension FLP fait référence au composant COMP1 qui n’a pas d’ID de l’élément spécifié dans la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="3915c-112">Extension flp references the component Comp1 which does not have a ComponentId specified in the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="3915c-113">L’extension exe référence le composant Comp4 qui fait référence à un répertoire comme son chemin d’accès keyPath.</span><span class="sxs-lookup"><span data-stu-id="3915c-113">Extension exe references the component Comp4 which references a directory as its KeyPath.</span></span> <span data-ttu-id="3915c-114">KeyPath a la valeur null dans la table des composants.</span><span class="sxs-lookup"><span data-stu-id="3915c-114">The KeyPath is Null in the Component table.</span></span>
-   <span data-ttu-id="3915c-115">Le raccourci Shortcut2 fait référence au composant COMP3 qui fait référence à une entrée de registre en tant que chemin d’accès de clé.</span><span class="sxs-lookup"><span data-stu-id="3915c-115">Shortcut Shortcut2 references the component Comp3 which references a Registry entry as the key path.</span></span> <span data-ttu-id="3915c-116">La valeur de la colonne attributs dans la table Component est 4.</span><span class="sxs-lookup"><span data-stu-id="3915c-116">The value of the Attributes column in the Component table is 4.</span></span>

<span data-ttu-id="3915c-117">[Table des composants](component-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="3915c-117">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="3915c-118">Composant</span><span class="sxs-lookup"><span data-stu-id="3915c-118">Component</span></span> | <span data-ttu-id="3915c-119">ComponentId</span><span class="sxs-lookup"><span data-stu-id="3915c-119">ComponentId</span></span>                            | <span data-ttu-id="3915c-120">Attributs</span><span class="sxs-lookup"><span data-stu-id="3915c-120">Attributes</span></span> | <span data-ttu-id="3915c-121">KeyPath</span><span class="sxs-lookup"><span data-stu-id="3915c-121">KeyPath</span></span> |
|-----------|----------------------------------------|------------|---------|
| <span data-ttu-id="3915c-122">COMP1</span><span class="sxs-lookup"><span data-stu-id="3915c-122">Comp1</span></span>     | <span data-ttu-id="3915c-123">Null</span><span class="sxs-lookup"><span data-stu-id="3915c-123">Null</span></span>                                   | <span data-ttu-id="3915c-124">0</span><span class="sxs-lookup"><span data-stu-id="3915c-124">0</span></span>          | <span data-ttu-id="3915c-125">Fichier1</span><span class="sxs-lookup"><span data-stu-id="3915c-125">File1</span></span>   |
| <span data-ttu-id="3915c-126">COMP2</span><span class="sxs-lookup"><span data-stu-id="3915c-126">Comp2</span></span>     | {00000002-0003-0000-0000-624474736554} | <span data-ttu-id="3915c-127">0</span><span class="sxs-lookup"><span data-stu-id="3915c-127">0</span></span>          | <span data-ttu-id="3915c-128">Fichier2</span><span class="sxs-lookup"><span data-stu-id="3915c-128">File2</span></span>   |
| <span data-ttu-id="3915c-129">COMP3</span><span class="sxs-lookup"><span data-stu-id="3915c-129">Comp3</span></span>     | {00000003-0003-0000-0000-624474736554} | <span data-ttu-id="3915c-130">4</span><span class="sxs-lookup"><span data-stu-id="3915c-130">4</span></span>          | <span data-ttu-id="3915c-131">Reg3</span><span class="sxs-lookup"><span data-stu-id="3915c-131">Reg3</span></span>    |
| <span data-ttu-id="3915c-132">Comp4</span><span class="sxs-lookup"><span data-stu-id="3915c-132">Comp4</span></span>     | {00000004-0003-0000-0000-624474736554} | <span data-ttu-id="3915c-133">0</span><span class="sxs-lookup"><span data-stu-id="3915c-133">0</span></span>          | <span data-ttu-id="3915c-134">Null</span><span class="sxs-lookup"><span data-stu-id="3915c-134">Null</span></span>    |



 

<span data-ttu-id="3915c-135">[Table d’extension](extension-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="3915c-135">[Extension Table](extension-table.md) (partial)</span></span>



| <span data-ttu-id="3915c-136">Extension</span><span class="sxs-lookup"><span data-stu-id="3915c-136">Extension</span></span> | <span data-ttu-id="3915c-137">-\_</span><span class="sxs-lookup"><span data-stu-id="3915c-137">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="3915c-138">FLP</span><span class="sxs-lookup"><span data-stu-id="3915c-138">flp</span></span>       | <span data-ttu-id="3915c-139">COMP1</span><span class="sxs-lookup"><span data-stu-id="3915c-139">Comp1</span></span>       |
| <span data-ttu-id="3915c-140">TST</span><span class="sxs-lookup"><span data-stu-id="3915c-140">tst</span></span>       | <span data-ttu-id="3915c-141">COMP2</span><span class="sxs-lookup"><span data-stu-id="3915c-141">Comp2</span></span>       |
| <span data-ttu-id="3915c-142">exe</span><span class="sxs-lookup"><span data-stu-id="3915c-142">exe</span></span>       | <span data-ttu-id="3915c-143">Comp4</span><span class="sxs-lookup"><span data-stu-id="3915c-143">Comp4</span></span>       |



 

<span data-ttu-id="3915c-144">[Table de raccourcis](shortcut-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="3915c-144">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="3915c-145">Raccourci</span><span class="sxs-lookup"><span data-stu-id="3915c-145">Shortcut</span></span>  | <span data-ttu-id="3915c-146">-\_</span><span class="sxs-lookup"><span data-stu-id="3915c-146">Component\_</span></span> | <span data-ttu-id="3915c-147">Fonctionnalité\_</span><span class="sxs-lookup"><span data-stu-id="3915c-147">Feature\_</span></span>      |
|-----------|-------------|----------------|
| <span data-ttu-id="3915c-148">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="3915c-148">Shortcut1</span></span> | <span data-ttu-id="3915c-149">Comp4</span><span class="sxs-lookup"><span data-stu-id="3915c-149">Comp4</span></span>       | <span data-ttu-id="3915c-150">ProductFeature</span><span class="sxs-lookup"><span data-stu-id="3915c-150">ProductFeature</span></span> |
| <span data-ttu-id="3915c-151">Shortcut2</span><span class="sxs-lookup"><span data-stu-id="3915c-151">Shortcut2</span></span> | <span data-ttu-id="3915c-152">COMP3</span><span class="sxs-lookup"><span data-stu-id="3915c-152">Comp3</span></span>       | <span data-ttu-id="3915c-153">ProductFeature</span><span class="sxs-lookup"><span data-stu-id="3915c-153">ProductFeature</span></span> |



 

<span data-ttu-id="3915c-154">[Table des fonctionnalités](feature-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="3915c-154">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="3915c-155">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="3915c-155">Feature</span></span>        |
|----------------|
| <span data-ttu-id="3915c-156">ProductFeature</span><span class="sxs-lookup"><span data-stu-id="3915c-156">ProductFeature</span></span> |



 

> [!Note]  
> <span data-ttu-id="3915c-157">Si l’extension FLP et exe font toutes deux référence au même composant, le serveur EXE ou COM qui les ouvre doivent être identiques.</span><span class="sxs-lookup"><span data-stu-id="3915c-157">If the extension flp and exe both reference the same component, the EXE or COM server that opens them must be the same.</span></span> <span data-ttu-id="3915c-158">Ce fichier EXE est normalement le chemin d’accès du composant.</span><span class="sxs-lookup"><span data-stu-id="3915c-158">This EXE is normally the KeyPath for the Component.</span></span> <span data-ttu-id="3915c-159">Pour OFFICE, les extensions doc et xls ne peuvent pas faire référence au même composant, car le même EXE n’ouvre pas les deux extensions.</span><span class="sxs-lookup"><span data-stu-id="3915c-159">For OFFICE, the extensions doc and xls cannot reference the same component because the same EXE does not open both extensions.</span></span> <span data-ttu-id="3915c-160">Vous avez besoin d' winword.exe pour ouvrir les extensions de document et vous avez besoin d' excel.exe pour ouvrir les extensions xls.</span><span class="sxs-lookup"><span data-stu-id="3915c-160">You need winword.exe to open doc extensions and you need excel.exe to open xls extensions.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3915c-161">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3915c-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3915c-162">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="3915c-162">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



