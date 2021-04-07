---
description: ICE35 valide que les composants contenant des fichiers compressés stockés dans un fichier CAB ne sont pas configurés pour s’exécuter à partir de la source. Avec Windows Installer 2,0 ou une version ultérieure, cette restriction a été supprimée.
ms.assetid: b4df27e2-9790-4b18-a173-25fa8b0ecd4d
title: ICE35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea6a98079d3c57e0c796332cf0cd5f11045a07b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952286"
---
# <a name="ice35"></a><span data-ttu-id="a0646-104">ICE35</span><span class="sxs-lookup"><span data-stu-id="a0646-104">ICE35</span></span>

<span data-ttu-id="a0646-105">ICE35 valide que les composants contenant des fichiers compressés stockés dans un [fichier CAB](cabinet-files.md) ne sont pas configurés pour s’exécuter à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="a0646-105">ICE35 validates that components containing compressed files stored in a [cabinet file](cabinet-files.md) are not set to run from source.</span></span> <span data-ttu-id="a0646-106">Avec Windows Installer 2,0 ou une version ultérieure, cette restriction a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="a0646-106">With Windows Installer 2.0 or later, this restriction has been removed.</span></span>

<span data-ttu-id="a0646-107">ICE35 interroge la colonne CAB de la [table Media](media-table.md) pour déterminer quels fichiers sont compressés et stockés dans un fichier CAB.</span><span class="sxs-lookup"><span data-stu-id="a0646-107">ICE35 queries the Cabinet column of the [Media table](media-table.md) to determine which files are compressed and stored in a cabinet file.</span></span> <span data-ttu-id="a0646-108">Il interroge la [table de fichiers](file-table.md) pour identifier les composants qui contiennent ces fichiers.</span><span class="sxs-lookup"><span data-stu-id="a0646-108">It queries the [File table](file-table.md) to determine which components contain these files.</span></span> <span data-ttu-id="a0646-109">Enfin, il vérifie la [table des composants](component-table.md) pour déterminer si les bits d’exécution à partir de la source sont définis dans la colonne attributs.</span><span class="sxs-lookup"><span data-stu-id="a0646-109">Finally, it checks the [Component table](component-table.md) to determine whether the run-from-source bits are set in the Attributes column.</span></span>

## <a name="result"></a><span data-ttu-id="a0646-110">Résultats</span><span class="sxs-lookup"><span data-stu-id="a0646-110">Result</span></span>

<span data-ttu-id="a0646-111">ICE35 publie un message d’erreur s’il existe un fichier compressé stocké dans un fichier CAB appartenant à un composant avec le bit msidbComponentAttributesSourceOnly défini dans la colonne attributs de la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="a0646-111">ICE35 posts an error message if there is a compressed file stored in a cabinet file belonging to a component with the msidbComponentAttributesSourceOnly bit set in the Attributes column of the [Component table](component-table.md).</span></span> <span data-ttu-id="a0646-112">Avec Windows Installer 2,0 ou une version ultérieure, la valeur d’un message d’avertissement est remplacée par une erreur.</span><span class="sxs-lookup"><span data-stu-id="a0646-112">With Windows Installer 2.0 or later, this is changed from an error to a warning message.</span></span> <span data-ttu-id="a0646-113">Un package qui prend uniquement en charge Windows Installer 2,0 et versions ultérieures a la \_ propriété PID PageCount du flux d’informations de synthèse définie sur une valeur d’au moins 200.</span><span class="sxs-lookup"><span data-stu-id="a0646-113">A package that supports only Windows Installer 2.0 and later has the PID\_PAGECOUNT property of the Summary Information Stream set to a value of at least 200.</span></span>

<span data-ttu-id="a0646-114">ICE35 publie un message d’avertissement si un fichier compressé est stocké dans un fichier CAB appartenant à un composant avec le bit msidbComponentAttributesOptional défini dans la colonne attributs de la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="a0646-114">ICE35 posts warning message if there is a compressed file stored in a cabinet file belonging to a component with the msidbComponentAttributesOptional bit set in the Attributes column of the [Component table](component-table.md).</span></span> <span data-ttu-id="a0646-115">Ce message d’avertissement a été supprimé avec Windows Installer 2,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a0646-115">This warning message has been removed with Windows Installer 2.0 and later.</span></span>

<span data-ttu-id="a0646-116">Si plusieurs fichiers d’un composant se trouvent dans un fichier CAB, ICE35 signale les erreurs pour chaque fichier dont l’exécution provient du bit source défini.</span><span class="sxs-lookup"><span data-stu-id="a0646-116">If multiple files in a component are in a cabinet file, ICE35 reports errors for each file that has the run from source bit set.</span></span>

## <a name="example"></a><span data-ttu-id="a0646-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="a0646-117">Example</span></span>

<span data-ttu-id="a0646-118">ICE35 signale les erreurs et avertissements suivants pour l’exemple indiqué à l’aide d’une version antérieure à la version 2,0 de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="a0646-118">ICE35 reports the following errors and warnings for the example shown using a version earlier than Windows Installer version 2.0.</span></span>



| <span data-ttu-id="a0646-119">Erreur ICE35</span><span class="sxs-lookup"><span data-stu-id="a0646-119">ICE35 Error</span></span>                                                                                                | <span data-ttu-id="a0646-120">Description</span><span class="sxs-lookup"><span data-stu-id="a0646-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0646-121">ERREUR : le composant Component3 ne peut pas être exécuté à partir de la source uniquement, car son fichier membre’fichier3 'est compressé.</span><span class="sxs-lookup"><span data-stu-id="a0646-121">ERROR: Component Component3 cannot be Run From Source only, because its member file 'File3' is compressed.</span></span> | <span data-ttu-id="a0646-122">Un fichier compressé est stocké dans un fichier CAB et ce fichier appartient à un composant avec le bit SourceOnly défini dans la colonne attributs de la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="a0646-122">There is a compressed file stored in a cabinet file and this file belongs to a component with the SourceOnly bit set in the Attributes column of the [Component table](component-table.md).</span></span> <span data-ttu-id="a0646-123">Pour corriger cette erreur, remplacez les 2 bits inférieurs de la valeur des attributs Component2's par « 00 », ce qui correspond uniquement à local, ou supprimez Fichier4 du fichier CAB.</span><span class="sxs-lookup"><span data-stu-id="a0646-123">To fix this error change the lower 2 bits of Component2's Attributes value to "00", meaning Local only, or remove File4 from the CAB file.</span></span><br/>                                                                                                                                                                         |
| <span data-ttu-id="a0646-124">ERREUR : le composant Component3 ne peut pas être exécuté à partir de la source uniquement, car son fichier membre’fichier3 'est compressé.</span><span class="sxs-lookup"><span data-stu-id="a0646-124">ERROR: Component Component3 cannot be Run From Source only, because its member file 'File3' is compressed.</span></span> | <span data-ttu-id="a0646-125">Un fichier compressé est stocké dans un fichier CAB et ce fichier appartient à un composant avec le bit SourceOnly défini dans la colonne attributs de la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="a0646-125">There is a compressed file stored in a cabinet file and this file belongs to a component with the SourceOnly bit set in the Attributes column of the [Component table](component-table.md).</span></span> <span data-ttu-id="a0646-126">Étant donné que les fichiers d’un composant ne doivent pas nécessairement provenir du même support, ICE35 signale les erreurs pour chaque fichier du composant qui se trouve dans un fichier CAB.</span><span class="sxs-lookup"><span data-stu-id="a0646-126">Because the files in a component do not all have to originate from the same media, ICE35 reports errors for each file in the component that is in a cabinet.</span></span><br/> <span data-ttu-id="a0646-127">Pour corriger cette erreur, remplacez les 2 bits inférieurs de la valeur des attributs Component2's par « 00 », ce qui correspond uniquement à local, ou supprimez Fichier4 du fichier CAB.</span><span class="sxs-lookup"><span data-stu-id="a0646-127">To fix this error change the lower 2 bits of Component2's Attributes value to "00", meaning Local only, or remove File4 from the CAB file.</span></span><br/> |



 

<span data-ttu-id="a0646-128">[Table des médias](media-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="a0646-128">[Media Table](media-table.md) (partial)</span></span>



| <span data-ttu-id="a0646-129">DiskID</span><span class="sxs-lookup"><span data-stu-id="a0646-129">DiskID</span></span> | <span data-ttu-id="a0646-130">LastSequence</span><span class="sxs-lookup"><span data-stu-id="a0646-130">LastSequence</span></span> | <span data-ttu-id="a0646-131">CAB</span><span class="sxs-lookup"><span data-stu-id="a0646-131">Cabinet</span></span>   |
|--------|--------------|-----------|
| <span data-ttu-id="a0646-132">1</span><span class="sxs-lookup"><span data-stu-id="a0646-132">1</span></span>      | <span data-ttu-id="a0646-133">2</span><span class="sxs-lookup"><span data-stu-id="a0646-133">2</span></span>            |           |
| <span data-ttu-id="a0646-134">2</span><span class="sxs-lookup"><span data-stu-id="a0646-134">2</span></span>      | <span data-ttu-id="a0646-135">4</span><span class="sxs-lookup"><span data-stu-id="a0646-135">4</span></span>            | <span data-ttu-id="a0646-136">One.cab</span><span class="sxs-lookup"><span data-stu-id="a0646-136">One.cab</span></span>   |
| <span data-ttu-id="a0646-137">3</span><span class="sxs-lookup"><span data-stu-id="a0646-137">3</span></span>      | <span data-ttu-id="a0646-138">5</span><span class="sxs-lookup"><span data-stu-id="a0646-138">5</span></span>            | <span data-ttu-id="a0646-139">\#Two.cab</span><span class="sxs-lookup"><span data-stu-id="a0646-139">\#Two.cab</span></span> |



 

<span data-ttu-id="a0646-140">[Table de fichiers](file-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="a0646-140">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="a0646-141">Fichier</span><span class="sxs-lookup"><span data-stu-id="a0646-141">File</span></span>  | <span data-ttu-id="a0646-142">-\_</span><span class="sxs-lookup"><span data-stu-id="a0646-142">Component\_</span></span> | <span data-ttu-id="a0646-143">Séquence</span><span class="sxs-lookup"><span data-stu-id="a0646-143">Sequence</span></span> |
|-------|-------------|----------|
| <span data-ttu-id="a0646-144">Fichier1</span><span class="sxs-lookup"><span data-stu-id="a0646-144">File1</span></span> | <span data-ttu-id="a0646-145">Composant1</span><span class="sxs-lookup"><span data-stu-id="a0646-145">Component1</span></span>  | <span data-ttu-id="a0646-146">1</span><span class="sxs-lookup"><span data-stu-id="a0646-146">1</span></span>        |
| <span data-ttu-id="a0646-147">Fichier2</span><span class="sxs-lookup"><span data-stu-id="a0646-147">File2</span></span> | <span data-ttu-id="a0646-148">Component2</span><span class="sxs-lookup"><span data-stu-id="a0646-148">Component2</span></span>  | <span data-ttu-id="a0646-149">2</span><span class="sxs-lookup"><span data-stu-id="a0646-149">2</span></span>        |
| <span data-ttu-id="a0646-150">Fichier3</span><span class="sxs-lookup"><span data-stu-id="a0646-150">File3</span></span> | <span data-ttu-id="a0646-151">Component2</span><span class="sxs-lookup"><span data-stu-id="a0646-151">Component2</span></span>  | <span data-ttu-id="a0646-152">3</span><span class="sxs-lookup"><span data-stu-id="a0646-152">3</span></span>        |
| <span data-ttu-id="a0646-153">Fichier4</span><span class="sxs-lookup"><span data-stu-id="a0646-153">File4</span></span> | <span data-ttu-id="a0646-154">Component3</span><span class="sxs-lookup"><span data-stu-id="a0646-154">Component3</span></span>  | <span data-ttu-id="a0646-155">4</span><span class="sxs-lookup"><span data-stu-id="a0646-155">4</span></span>        |
| <span data-ttu-id="a0646-156">Fichier5</span><span class="sxs-lookup"><span data-stu-id="a0646-156">File5</span></span> | <span data-ttu-id="a0646-157">Component3</span><span class="sxs-lookup"><span data-stu-id="a0646-157">Component3</span></span>  | <span data-ttu-id="a0646-158">5</span><span class="sxs-lookup"><span data-stu-id="a0646-158">5</span></span>        |



 

<span data-ttu-id="a0646-159">[Table des composants](component-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="a0646-159">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="a0646-160">Composant</span><span class="sxs-lookup"><span data-stu-id="a0646-160">Component</span></span>  | <span data-ttu-id="a0646-161">Attributs</span><span class="sxs-lookup"><span data-stu-id="a0646-161">Attributes</span></span> |
|------------|------------|
| <span data-ttu-id="a0646-162">Composant1</span><span class="sxs-lookup"><span data-stu-id="a0646-162">Component1</span></span> | <span data-ttu-id="a0646-163">0</span><span class="sxs-lookup"><span data-stu-id="a0646-163">0</span></span>          |
| <span data-ttu-id="a0646-164">Component2</span><span class="sxs-lookup"><span data-stu-id="a0646-164">Component2</span></span> | <span data-ttu-id="a0646-165">2</span><span class="sxs-lookup"><span data-stu-id="a0646-165">2</span></span>          |
| <span data-ttu-id="a0646-166">Component3</span><span class="sxs-lookup"><span data-stu-id="a0646-166">Component3</span></span> | <span data-ttu-id="a0646-167">1</span><span class="sxs-lookup"><span data-stu-id="a0646-167">1</span></span>          |



 

<span data-ttu-id="a0646-168">[Table de raccourcis](shortcut-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="a0646-168">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="a0646-169">Raccourci</span><span class="sxs-lookup"><span data-stu-id="a0646-169">Shortcut</span></span>  | <span data-ttu-id="a0646-170">Icône\_</span><span class="sxs-lookup"><span data-stu-id="a0646-170">Icon\_</span></span> |
|-----------|--------|
| <span data-ttu-id="a0646-171">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="a0646-171">Shortcut1</span></span> | <span data-ttu-id="a0646-172">Icon2</span><span class="sxs-lookup"><span data-stu-id="a0646-172">Icon2</span></span>  |



 

<span data-ttu-id="a0646-173">Notez que les fichiers peuvent également être marqués comme compressés à l’aide de la propriété [**Résumé du nombre de mots**](word-count-summary.md) du flux d’informations de [synthèse](summary-information-stream.md).</span><span class="sxs-lookup"><span data-stu-id="a0646-173">Note that files can also be marked as compressed using the [**Word Count Summary**](word-count-summary.md) Property of the [Summary Information stream](summary-information-stream.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0646-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a0646-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0646-175">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="a0646-175">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




