---
description: ICE32 valide que les clés et les clés étrangères du fichier. msi sont des mêmes types de définition de taille et de colonne.
ms.assetid: cc488ec5-e17a-4829-9763-38ba3c33bfde
title: ICE32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d6ff9e4de592ac073050b357aff0c63d984f0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536718"
---
# <a name="ice32"></a><span data-ttu-id="e45a7-103">ICE32</span><span class="sxs-lookup"><span data-stu-id="e45a7-103">ICE32</span></span>

<span data-ttu-id="e45a7-104">ICE32 valide que les clés et les clés étrangères du fichier. msi sont des mêmes types de définition de taille et de colonne.</span><span class="sxs-lookup"><span data-stu-id="e45a7-104">ICE32 validates that keys and foreign keys in the .msi file are of the same size and column definition types.</span></span> <span data-ttu-id="e45a7-105">Cette action personnalisée ICE effectue la comparaison à l’aide de la [ \_ table de validation](-validation-table.md) et à l’aide des types de définition retournés par [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo).</span><span class="sxs-lookup"><span data-stu-id="e45a7-105">This ICE custom action makes the comparison using the [\_Validation table](-validation-table.md) and using the definition types that are returned by [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo).</span></span> <span data-ttu-id="e45a7-106">Pour plus d’informations, consultez [format de définition de colonne](column-definition-format.md).</span><span class="sxs-lookup"><span data-stu-id="e45a7-106">For more information, see [Column Definition Format](column-definition-format.md).</span></span>

## <a name="result"></a><span data-ttu-id="e45a7-107">Résultats</span><span class="sxs-lookup"><span data-stu-id="e45a7-107">Result</span></span>

<span data-ttu-id="e45a7-108">ICE32 publie des erreurs si le fichier. msi contient des clés étrangères aux clés d’un type de données de longueur de colonne ou de colonne différent.</span><span class="sxs-lookup"><span data-stu-id="e45a7-108">ICE32 posts errors if the .msi file contains any foreign keys to keys of a different column length or column data type.</span></span>

## <a name="example"></a><span data-ttu-id="e45a7-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="e45a7-109">Example</span></span>

<span data-ttu-id="e45a7-110">ICE32 publie deux erreurs pour l’exemple ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="e45a7-110">ICE32 posts two errors for the example shown:</span></span>

-   <span data-ttu-id="e45a7-111">Une clé étrangère et une clé définie ont une taille différente.</span><span class="sxs-lookup"><span data-stu-id="e45a7-111">There is a foreign key and key defined that differ in size.</span></span>
-   <span data-ttu-id="e45a7-112">Une clé étrangère et une clé définies diffèrent dans leur type de définition.</span><span class="sxs-lookup"><span data-stu-id="e45a7-112">There is a foreign key and key defined that differ in their definition type.</span></span>

<span data-ttu-id="e45a7-113">[ \_ Table de validation](-validation-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="e45a7-113">[\_Validation Table](-validation-table.md) (partial)</span></span>



| <span data-ttu-id="e45a7-114">Table de charge de travail</span><span class="sxs-lookup"><span data-stu-id="e45a7-114">Table</span></span> | <span data-ttu-id="e45a7-115">Colonne</span><span class="sxs-lookup"><span data-stu-id="e45a7-115">Column</span></span>  | <span data-ttu-id="e45a7-116">Keytable</span><span class="sxs-lookup"><span data-stu-id="e45a7-116">KeyTable</span></span> | <span data-ttu-id="e45a7-117">KeyColumn</span><span class="sxs-lookup"><span data-stu-id="e45a7-117">KeyColumn</span></span> |
|-------|---------|----------|-----------|
| <span data-ttu-id="e45a7-118">Fichier</span><span class="sxs-lookup"><span data-stu-id="e45a7-118">File</span></span>  | <span data-ttu-id="e45a7-119">Version</span><span class="sxs-lookup"><span data-stu-id="e45a7-119">Version</span></span> | <span data-ttu-id="e45a7-120">Fichier</span><span class="sxs-lookup"><span data-stu-id="e45a7-120">File</span></span>     | <span data-ttu-id="e45a7-121">1</span><span class="sxs-lookup"><span data-stu-id="e45a7-121">1</span></span>         |
| <span data-ttu-id="e45a7-122">Ailes</span><span class="sxs-lookup"><span data-stu-id="e45a7-122">Flap</span></span>  | <span data-ttu-id="e45a7-123">Colonne8</span><span class="sxs-lookup"><span data-stu-id="e45a7-123">Column8</span></span> | <span data-ttu-id="e45a7-124">Ailes</span><span class="sxs-lookup"><span data-stu-id="e45a7-124">Flap</span></span>     | <span data-ttu-id="e45a7-125">1</span><span class="sxs-lookup"><span data-stu-id="e45a7-125">1</span></span>         |



 

<span data-ttu-id="e45a7-126">Définitions de colonne (partielles)</span><span class="sxs-lookup"><span data-stu-id="e45a7-126">Column Definitions (partial)</span></span>



| <span data-ttu-id="e45a7-127">Table de charge de travail</span><span class="sxs-lookup"><span data-stu-id="e45a7-127">Table</span></span> | <span data-ttu-id="e45a7-128">Colonne</span><span class="sxs-lookup"><span data-stu-id="e45a7-128">Column</span></span>  | <span data-ttu-id="e45a7-129">Type</span><span class="sxs-lookup"><span data-stu-id="e45a7-129">Type</span></span> | <span data-ttu-id="e45a7-130">Taille</span><span class="sxs-lookup"><span data-stu-id="e45a7-130">Size</span></span> |
|-------|---------|------|------|
| <span data-ttu-id="e45a7-131">Fichier</span><span class="sxs-lookup"><span data-stu-id="e45a7-131">File</span></span>  | <span data-ttu-id="e45a7-132">Fichier</span><span class="sxs-lookup"><span data-stu-id="e45a7-132">File</span></span>    | <span data-ttu-id="e45a7-133">s</span><span class="sxs-lookup"><span data-stu-id="e45a7-133">s</span></span>    | <span data-ttu-id="e45a7-134">72</span><span class="sxs-lookup"><span data-stu-id="e45a7-134">72</span></span>   |
| <span data-ttu-id="e45a7-135">Fichier</span><span class="sxs-lookup"><span data-stu-id="e45a7-135">File</span></span>  | <span data-ttu-id="e45a7-136">Version</span><span class="sxs-lookup"><span data-stu-id="e45a7-136">Version</span></span> | <span data-ttu-id="e45a7-137">S</span><span class="sxs-lookup"><span data-stu-id="e45a7-137">S</span></span>    | <span data-ttu-id="e45a7-138">32</span><span class="sxs-lookup"><span data-stu-id="e45a7-138">32</span></span>   |
| <span data-ttu-id="e45a7-139">Ailes</span><span class="sxs-lookup"><span data-stu-id="e45a7-139">Flap</span></span>  | <span data-ttu-id="e45a7-140">Column1</span><span class="sxs-lookup"><span data-stu-id="e45a7-140">Column1</span></span> | <span data-ttu-id="e45a7-141">i</span><span class="sxs-lookup"><span data-stu-id="e45a7-141">i</span></span>    | <span data-ttu-id="e45a7-142">2</span><span class="sxs-lookup"><span data-stu-id="e45a7-142">2</span></span>    |
| <span data-ttu-id="e45a7-143">Ailes</span><span class="sxs-lookup"><span data-stu-id="e45a7-143">Flap</span></span>  | <span data-ttu-id="e45a7-144">Colonne8</span><span class="sxs-lookup"><span data-stu-id="e45a7-144">Column8</span></span> | <span data-ttu-id="e45a7-145">S</span><span class="sxs-lookup"><span data-stu-id="e45a7-145">S</span></span>    | <span data-ttu-id="e45a7-146">32</span><span class="sxs-lookup"><span data-stu-id="e45a7-146">32</span></span>   |



 

<span data-ttu-id="e45a7-147">La colonne de version de la table de fichiers peut être une clé étrangère vers un autre fichier de la table de fichiers.</span><span class="sxs-lookup"><span data-stu-id="e45a7-147">The Version column of the File table can be a foreign key to another file in the File table.</span></span> <span data-ttu-id="e45a7-148">Cela se produit avec les fichiers d’accompagnement.</span><span class="sxs-lookup"><span data-stu-id="e45a7-148">This occurs with companion files.</span></span> <span data-ttu-id="e45a7-149">Toutefois, la colonne version autorise uniquement une longueur de chaîne de 32, alors que la colonne fichier autorise une longueur de chaîne de 72.</span><span class="sxs-lookup"><span data-stu-id="e45a7-149">However, the Version column only allows a string length 32, whereas the File column allows a string length 72.</span></span> <span data-ttu-id="e45a7-150">Pour corriger cette erreur, modifiez les longueurs de chaîne pour qu’elles correspondent.</span><span class="sxs-lookup"><span data-stu-id="e45a7-150">To fix this error change the string lengths to match.</span></span>

<span data-ttu-id="e45a7-151">Une clé étrangère et une clé définies diffèrent dans leurs types de définition.</span><span class="sxs-lookup"><span data-stu-id="e45a7-151">There is a foreign key and key defined that differ in their definition types.</span></span> <span data-ttu-id="e45a7-152">Le Column8 de la table de rabats est listé comme clé étrangère à Colonne1.</span><span class="sxs-lookup"><span data-stu-id="e45a7-152">Column8 of the Flap Table is listed as a foreign key to Column1.</span></span> <span data-ttu-id="e45a7-153">Column8 est une colonne de chaîne et Colonne1 est une colonne de type entier.</span><span class="sxs-lookup"><span data-stu-id="e45a7-153">Column8 is a string column and Column1 is an integer column.</span></span> <span data-ttu-id="e45a7-154">Les paires clé étrangère et clé doivent être définies de sorte que leurs types de données correspondent.</span><span class="sxs-lookup"><span data-stu-id="e45a7-154">The foreign key and key pairs must be defined so that their data types match.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e45a7-155">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e45a7-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e45a7-156">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="e45a7-156">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



