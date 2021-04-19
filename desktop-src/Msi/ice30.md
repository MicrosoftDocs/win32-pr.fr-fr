---
description: ICE30 vérifie que l’installation des composants contenant le même fichier n’installe jamais le fichier plus d’une fois dans le même répertoire.
ms.assetid: 74cb455b-a53e-4c6b-98ff-08cf0858f11f
title: ICE30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78fa96899231015d864e5a0912b8ff73cedbbe75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518764"
---
# <a name="ice30"></a><span data-ttu-id="fe859-103">ICE30</span><span class="sxs-lookup"><span data-stu-id="fe859-103">ICE30</span></span>

<span data-ttu-id="fe859-104">ICE30 vérifie que l’installation des composants contenant le même fichier n’installe jamais le fichier plus d’une fois dans le même répertoire.</span><span class="sxs-lookup"><span data-stu-id="fe859-104">ICE30 validates that the installation of components containing the same file never installs the file more than once in the same directory.</span></span>

<span data-ttu-id="fe859-105">ICE30 accède à chaque composant de la [table des composants](component-table.md) , puis détermine le répertoire cible du composant à partir de la [table de répertoires](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="fe859-105">ICE30 goes to every component in the [Component table](component-table.md) and then determines the component's target directory from the [Directory table](directory-table.md).</span></span> <span data-ttu-id="fe859-106">Il vérifie ensuite quels composants s’installent dans le même répertoire cible.</span><span class="sxs-lookup"><span data-stu-id="fe859-106">It then checks to see which of these components install to the same target directory.</span></span> <span data-ttu-id="fe859-107">Enfin, elle utilise la [table file](file-table.md) pour vérifier qu’aucun des fichiers de ces composants n’a le même nom.</span><span class="sxs-lookup"><span data-stu-id="fe859-107">Finally, it uses the [File table](file-table.md) to verify that none of the files in these components have the same name.</span></span>

<span data-ttu-id="fe859-108">ICE30 vérifie les noms de fichiers longs (LFN) et les noms de fichiers courts (SFN).</span><span class="sxs-lookup"><span data-stu-id="fe859-108">ICE30 checks both long file names (LFN) and short file names (SFN).</span></span>

<span data-ttu-id="fe859-109">ICE30 n’évalue pas les propriétés dans la résolution des répertoires, car ces propriétés peuvent changer au moment de l’exécution et modifier le schéma de résolution d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="fe859-109">ICE30 does not evaluate properties in the resolution of directories because these properties can change at runtime and alter the directory resolution scheme.</span></span> <span data-ttu-id="fe859-110">Cela signifie que ICE30 peut détecter des collisions de fichiers en raison des répertoires ayant la même propriété dans leurs chemins d’accès, mais ne détecte pas les collisions résultant de deux propriétés ayant la même valeur.</span><span class="sxs-lookup"><span data-stu-id="fe859-110">This means ICE30 can detect file collisions due to directories with the same property in their paths, but does not detect collisions resulting from two properties having the same value.</span></span>

## <a name="result"></a><span data-ttu-id="fe859-111">Résultats</span><span class="sxs-lookup"><span data-stu-id="fe859-111">Result</span></span>

<span data-ttu-id="fe859-112">ICE30 publie un message d’erreur pour chaque paire de composants qui installe le même fichier dans le même répertoire.</span><span class="sxs-lookup"><span data-stu-id="fe859-112">ICE30 posts an error message for each pair of components that installs the same file to the same directory.</span></span>

## <a name="example"></a><span data-ttu-id="fe859-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="fe859-113">Example</span></span>

<span data-ttu-id="fe859-114">L’exemple présenté retourne chaque erreur suivante deux fois.</span><span class="sxs-lookup"><span data-stu-id="fe859-114">The example shown returns each of the following errors twice.</span></span>



| <span data-ttu-id="fe859-115">Erreur ou avertissement ICE30</span><span class="sxs-lookup"><span data-stu-id="fe859-115">ICE30 error or warning</span></span>                                                                                                                                                                                                                                                                    | <span data-ttu-id="fe859-116">Description</span><span class="sxs-lookup"><span data-stu-id="fe859-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe859-117">ERREUR : le fichier cible’README. 1re’est installé dans le’TARGETDIR \\ Product’par deux composants différents sur un système SFN : 'Composant1 'et’COMPONENT2 '.</span><span class="sxs-lookup"><span data-stu-id="fe859-117">ERROR: The target file 'README.1st' is installed in 'TARGETDIR\\PRODUCT' by two different components on an SFN system: 'Component1' and 'Component2'.</span></span> <span data-ttu-id="fe859-118">Cela interrompt le décompte de références de composants.</span><span class="sxs-lookup"><span data-stu-id="fe859-118">This breaks component reference counting.</span></span>                                                                                           | <span data-ttu-id="fe859-119">Composant1 et COMPONENT2 ont tous les deux un fichier nommé « READEME. 1er ».</span><span class="sxs-lookup"><span data-stu-id="fe859-119">Component1 and Component2 both have a file named 'READEME.1st'.</span></span> <span data-ttu-id="fe859-120">Lorsque vous utilisez des noms de fichiers courts, le programme d’installation installe à la fois Dir1 et dir2 dans le même répertoire, TARGETDIR \\ Product.</span><span class="sxs-lookup"><span data-stu-id="fe859-120">When using short file names, the installer installs both Dir1 and Dir2 to the same directory, TARGETDIR\\PRODUCT.</span></span><br/> <span data-ttu-id="fe859-121">ICE30 génère deux erreurs, une pour chaque fichier.</span><span class="sxs-lookup"><span data-stu-id="fe859-121">ICE30 generate two errors, one for each file.</span></span> <span data-ttu-id="fe859-122">Dans un environnement de création qui affiche des emplacements d’erreur, la première erreur se trouve à l’entrée d’un fichier dans la [table de fichiers](file-table.md)et la seconde à l’emplacement de l’autre fichier.</span><span class="sxs-lookup"><span data-stu-id="fe859-122">In an authoring environment that displays error locations, the first error is at one file's entry in the [File Table](file-table.md), and the second at the location of the other file.</span></span><br/> |
| <span data-ttu-id="fe859-123">ERREUR : l’installation d’un composant conditionnel entraînerait l’installation du fichier cible « README. 1er » dans « TARGETDIR \\ Common Tools » par deux composants différents sur un système LFN : « Component3 » et « Component4 ».</span><span class="sxs-lookup"><span data-stu-id="fe859-123">ERROR: Installation of a conditionalized component would cause the target file 'README.1st' to be installed in 'TARGETDIR\\COMMON TOOLS' by two different components on an LFN system: 'Component3' and 'Component4'.</span></span> <span data-ttu-id="fe859-124">Cela rompt le décompte de références de composants.</span><span class="sxs-lookup"><span data-stu-id="fe859-124">This would break component reference counting.</span></span>                      | <span data-ttu-id="fe859-125">Component4 a une entrée dans la colonne condition de la [table Component](component-table.md) et Component3 ne le fait pas.</span><span class="sxs-lookup"><span data-stu-id="fe859-125">Component4 has an entry in the Condition column of the [Component table](component-table.md) and Component3 does not.</span></span> <span data-ttu-id="fe859-126">Si [**VersionNT**](versionnt.md) a la valeur true, Component4 est installé et il y a une collision avec le fichier Readme. la première est toujours installée par Component3.</span><span class="sxs-lookup"><span data-stu-id="fe859-126">If [**VersionNT**](versionnt.md) is True, Component4 is installed, and there a collision with the Readme.1st always installed by Component3.</span></span><br/> <span data-ttu-id="fe859-127">ICE30 génère 4 erreurs, une paire pour SFN, une pour LFN.</span><span class="sxs-lookup"><span data-stu-id="fe859-127">ICE30 generates 4 errors, one pair for SFN, one for LFN.</span></span><br/>                                                                                            |
| <span data-ttu-id="fe859-128">AVERTISSEMENT : le fichier cible « README. premier » peut être installé dans « TARGETDIR \\ Common Tools » par deux composants conditionnels différents sur un système SFN : « Component4 » et « Component5 ».</span><span class="sxs-lookup"><span data-stu-id="fe859-128">WARNING: The target file 'README.1st' might be installed in 'TARGETDIR\\COMMON TOOLS' by two different conditionalized components on an SFN system: 'Component4' and 'Component5'.</span></span> <span data-ttu-id="fe859-129">Si les conditions ne s’excluent pas mutuellement, le système de comptage des références du composant sera rompu.</span><span class="sxs-lookup"><span data-stu-id="fe859-129">If the conditions are not mutually exclusive, this will break the component reference counting system.</span></span> | <span data-ttu-id="fe859-130">Étant donné que Component4 et Component5 ont tous les deux des entrées dans la colonne condition de la [table des composants](component-table.md) , cette collision de fichier peut ne pas se produire.</span><span class="sxs-lookup"><span data-stu-id="fe859-130">Because Component4 and Component5 both have entries in the Condition column of the [Component table](component-table.md) this file collision may not occur.</span></span> <span data-ttu-id="fe859-131">ICE30 publie un avertissement uniquement parce que les conditions doivent être déterminées au moment de l’installation.</span><span class="sxs-lookup"><span data-stu-id="fe859-131">ICE30 only posts a warning because the conditions must be determined at the time of the installation.</span></span><br/> <span data-ttu-id="fe859-132">ICE30 génère 4 avertissements, une paire pour SFN, un pour LFN.</span><span class="sxs-lookup"><span data-stu-id="fe859-132">ICE30 generates 4 warnings, one pair for SFN, one for LFN.</span></span><br/>                                                                                            |



 

<span data-ttu-id="fe859-133">[Table des composants](component-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="fe859-133">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="fe859-134">Composant</span><span class="sxs-lookup"><span data-stu-id="fe859-134">Component</span></span>  | <span data-ttu-id="fe859-135">Répertoire</span><span class="sxs-lookup"><span data-stu-id="fe859-135">Directory</span></span> | <span data-ttu-id="fe859-136">Condition</span><span class="sxs-lookup"><span data-stu-id="fe859-136">Condition</span></span> |
|------------|-----------|-----------|
| <span data-ttu-id="fe859-137">Composant1</span><span class="sxs-lookup"><span data-stu-id="fe859-137">Component1</span></span> | <span data-ttu-id="fe859-138">Dir1</span><span class="sxs-lookup"><span data-stu-id="fe859-138">Dir1</span></span>      |           |
| <span data-ttu-id="fe859-139">Component2</span><span class="sxs-lookup"><span data-stu-id="fe859-139">Component2</span></span> | <span data-ttu-id="fe859-140">Dir2</span><span class="sxs-lookup"><span data-stu-id="fe859-140">Dir2</span></span>      |           |
| <span data-ttu-id="fe859-141">Component3</span><span class="sxs-lookup"><span data-stu-id="fe859-141">Component3</span></span> | <span data-ttu-id="fe859-142">Dir3</span><span class="sxs-lookup"><span data-stu-id="fe859-142">Dir3</span></span>      |           |
| <span data-ttu-id="fe859-143">Component4</span><span class="sxs-lookup"><span data-stu-id="fe859-143">Component4</span></span> | <span data-ttu-id="fe859-144">Dir3</span><span class="sxs-lookup"><span data-stu-id="fe859-144">Dir3</span></span>      | <span data-ttu-id="fe859-145">VersionNT</span><span class="sxs-lookup"><span data-stu-id="fe859-145">VersionNT</span></span> |
| <span data-ttu-id="fe859-146">Component5</span><span class="sxs-lookup"><span data-stu-id="fe859-146">Component5</span></span> | <span data-ttu-id="fe859-147">Dir3</span><span class="sxs-lookup"><span data-stu-id="fe859-147">Dir3</span></span>      | <span data-ttu-id="fe859-148">Version9X</span><span class="sxs-lookup"><span data-stu-id="fe859-148">Version9X</span></span> |



 

[<span data-ttu-id="fe859-149">Table de répertoire</span><span class="sxs-lookup"><span data-stu-id="fe859-149">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="fe859-150">Répertoire</span><span class="sxs-lookup"><span data-stu-id="fe859-150">Directory</span></span> | <span data-ttu-id="fe859-151">\_Répertoire parent</span><span class="sxs-lookup"><span data-stu-id="fe859-151">Parent\_Directory</span></span> | <span data-ttu-id="fe859-152">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="fe859-152">DefaultDir</span></span>                    |
|-----------|-------------------|-------------------------------|
| <span data-ttu-id="fe859-153">SOURCEDIR</span><span class="sxs-lookup"><span data-stu-id="fe859-153">SOURCEDIR</span></span> |                   | <span data-ttu-id="fe859-154">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="fe859-154">TARGETDIR</span></span>                     |
| <span data-ttu-id="fe859-155">Dir1</span><span class="sxs-lookup"><span data-stu-id="fe859-155">Dir1</span></span>      | <span data-ttu-id="fe859-156">SOURCEDIR</span><span class="sxs-lookup"><span data-stu-id="fe859-156">SOURCEDIR</span></span>         | <span data-ttu-id="fe859-157">Produit \| Composant1 produit :.</span><span class="sxs-lookup"><span data-stu-id="fe859-157">Product\|Component1 Product:.</span></span> |
| <span data-ttu-id="fe859-158">Dir2</span><span class="sxs-lookup"><span data-stu-id="fe859-158">Dir2</span></span>      | <span data-ttu-id="fe859-159">SOURCEDIR</span><span class="sxs-lookup"><span data-stu-id="fe859-159">SOURCEDIR</span></span>         | <span data-ttu-id="fe859-160">Produit :.</span><span class="sxs-lookup"><span data-stu-id="fe859-160">Product:.</span></span>                     |
| <span data-ttu-id="fe859-161">Dir3</span><span class="sxs-lookup"><span data-stu-id="fe859-161">Dir3</span></span>      | <span data-ttu-id="fe859-162">SOURCEDIR</span><span class="sxs-lookup"><span data-stu-id="fe859-162">SOURCEDIR</span></span>         | <span data-ttu-id="fe859-163">\|Outils courants courants :</span><span class="sxs-lookup"><span data-stu-id="fe859-163">Common\|Common Tools:</span></span>         |



 

<span data-ttu-id="fe859-164">[Table de fichiers](file-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="fe859-164">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="fe859-165">Fichier</span><span class="sxs-lookup"><span data-stu-id="fe859-165">File</span></span>  | <span data-ttu-id="fe859-166">-\_</span><span class="sxs-lookup"><span data-stu-id="fe859-166">Component\_</span></span> | <span data-ttu-id="fe859-167">FileName</span><span class="sxs-lookup"><span data-stu-id="fe859-167">FileName</span></span>   |
|-------|-------------|------------|
| <span data-ttu-id="fe859-168">Fichier1</span><span class="sxs-lookup"><span data-stu-id="fe859-168">File1</span></span> | <span data-ttu-id="fe859-169">Composant1</span><span class="sxs-lookup"><span data-stu-id="fe859-169">Component1</span></span>  | <span data-ttu-id="fe859-170">Lisez-moi. 1re</span><span class="sxs-lookup"><span data-stu-id="fe859-170">README.1st</span></span> |
| <span data-ttu-id="fe859-171">Fichier2</span><span class="sxs-lookup"><span data-stu-id="fe859-171">File2</span></span> | <span data-ttu-id="fe859-172">Component2</span><span class="sxs-lookup"><span data-stu-id="fe859-172">Component2</span></span>  | <span data-ttu-id="fe859-173">Lisez-moi. 1re</span><span class="sxs-lookup"><span data-stu-id="fe859-173">README.1st</span></span> |
| <span data-ttu-id="fe859-174">Fichier3</span><span class="sxs-lookup"><span data-stu-id="fe859-174">File3</span></span> | <span data-ttu-id="fe859-175">Component3</span><span class="sxs-lookup"><span data-stu-id="fe859-175">Component3</span></span>  | <span data-ttu-id="fe859-176">Lisez-moi. 1re</span><span class="sxs-lookup"><span data-stu-id="fe859-176">README.1st</span></span> |
| <span data-ttu-id="fe859-177">Fichier4</span><span class="sxs-lookup"><span data-stu-id="fe859-177">File4</span></span> | <span data-ttu-id="fe859-178">Component4</span><span class="sxs-lookup"><span data-stu-id="fe859-178">Component4</span></span>  | <span data-ttu-id="fe859-179">Lisez-moi. 1re</span><span class="sxs-lookup"><span data-stu-id="fe859-179">README.1st</span></span> |
| <span data-ttu-id="fe859-180">Fichier5</span><span class="sxs-lookup"><span data-stu-id="fe859-180">File5</span></span> | <span data-ttu-id="fe859-181">Component5</span><span class="sxs-lookup"><span data-stu-id="fe859-181">Component5</span></span>  | <span data-ttu-id="fe859-182">Lisez-moi. 1re</span><span class="sxs-lookup"><span data-stu-id="fe859-182">README.1st</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="fe859-183">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fe859-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe859-184">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="fe859-184">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




