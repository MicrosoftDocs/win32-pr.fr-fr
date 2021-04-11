---
description: ICEM09 vérifie que le module de fusion gère les répertoires prédéfinis en toute sécurité.
ms.assetid: 747ae5ee-adc1-4aa7-8239-2379f76bfd0f
title: ICEM09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee4b4d2d52c35d6dd3670daff5150a785e19d0b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203780"
---
# <a name="icem09"></a><span data-ttu-id="04134-103">ICEM09</span><span class="sxs-lookup"><span data-stu-id="04134-103">ICEM09</span></span>

<span data-ttu-id="04134-104">ICEM09 vérifie que le module de fusion gère les répertoires prédéfinis en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="04134-104">ICEM09 verifies the merge module safely handles predefined directories.</span></span> <span data-ttu-id="04134-105">Pour ce faire, il vérifie qu’aucun composant du module n’installe un répertoire dans un répertoire système prédéfini comme « ProgramFilesFolder » ou « StartMenuFolder ».</span><span class="sxs-lookup"><span data-stu-id="04134-105">It does this by verifying that no component in the module installs a directory to a predefined system directory such as "ProgramFilesFolder" or "StartMenuFolder".</span></span> <span data-ttu-id="04134-106">Au lieu de cela, les modules doivent utiliser des répertoires avec des noms uniques (créés avec la Convention de nommage des modules de fusion) et utiliser des actions personnalisées pour cibler le répertoire cible approprié.</span><span class="sxs-lookup"><span data-stu-id="04134-106">Instead, modules should use directories with unique names (created with the merge module naming convention) and use custom actions to target the appropriate target directory.</span></span> <span data-ttu-id="04134-107">Cette approche empêche les modules d’entrer en conflit avec une structure de répertoires existante dans la base de données finale.</span><span class="sxs-lookup"><span data-stu-id="04134-107">This approach prevents modules from conflicting with an existing directory structure in the final database.</span></span> <span data-ttu-id="04134-108">ICEM09 vérifie que les actions personnalisées nécessaires à cette technique pour fonctionner n’existent pas (afin que l’outil de fusion puisse les générer) ou qu’elles existent dans le format approprié (afin qu’elles fonctionnent comme prévu).</span><span class="sxs-lookup"><span data-stu-id="04134-108">ICEM09 checks that the custom actions needed for this technique to work either do not exist (so that the merge tool can generate them) or exist in the correct form (so that they work as expected).</span></span>

<span data-ttu-id="04134-109">L’échec de la résolution d’un avertissement ou d’une erreur signalée par ICEM09 peut provoquer des problèmes pour les clients de votre module de fusion.</span><span class="sxs-lookup"><span data-stu-id="04134-109">Failure to fix a warning or error reported by ICEM09 could cause problems for the clients of your merge module.</span></span> <span data-ttu-id="04134-110">Les lignes de la table de répertoires avec des clés primaires telles que ProgramFilesFolder existent souvent dans une base de données ; par conséquent, si les composants de votre module s’installent directement dans des répertoires prédéfinis tels que ProgramFilesFolder, les entrées de répertoire dans le module peuvent entrer en conflit avec des lignes déjà existantes.</span><span class="sxs-lookup"><span data-stu-id="04134-110">Directory table rows with primary keys such as ProgramFilesFolder often exist in a database; therefore, if components in your module install directly to predefined directories such as ProgramFilesFolder, the directory entries in the module may collide with already existing rows.</span></span> <span data-ttu-id="04134-111">Cette condition oblige l’utilisateur de votre module à fractionner les fichiers sources de votre module afin qu’il corresponde au répertoire source existant.</span><span class="sxs-lookup"><span data-stu-id="04134-111">This condition would require the user of your module to split the source files from your module in order to match the existing source directory.</span></span>

## <a name="result"></a><span data-ttu-id="04134-112">Résultats</span><span class="sxs-lookup"><span data-stu-id="04134-112">Result</span></span>

<span data-ttu-id="04134-113">ICEM09 signale une erreur ou un avertissement lorsqu’un composant de module installe un répertoire dans un répertoire système prédéfini, provoquant ainsi un conflit de noms avec la structure de répertoires existante.</span><span class="sxs-lookup"><span data-stu-id="04134-113">ICEM09 reports an error or warning when a module component installs a directory to a pre-defined system directory, causing a possible name conflict with the existing directory structure.</span></span>

## <a name="example"></a><span data-ttu-id="04134-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="04134-114">Example</span></span>

<span data-ttu-id="04134-115">ICEM09 publie les avertissements suivants pour un module contenant les entrées de base de données affichées.</span><span class="sxs-lookup"><span data-stu-id="04134-115">ICEM09 posts the following warnings for a module containing the database entries shown.</span></span>

``` syntax
Warning: The component 'Component1.<GUID>' installs directly into the pre-defined 
directory 'ProgramFilesFolder'. It is recommended that merge modules alias 
all such directories to unique names.
```

<span data-ttu-id="04134-116">Renommez le répertoire du module de fusion afin qu’il ne corresponde pas à une propriété Windows Installer et qu’il soit unique.</span><span class="sxs-lookup"><span data-stu-id="04134-116">Rename the merge module directory so it does not match a Windows Installer property and therefore is unique.</span></span> <span data-ttu-id="04134-117">Affectez ensuite à une propriété du même nom la valeur de l’Windows Installer Directory.</span><span class="sxs-lookup"><span data-stu-id="04134-117">Then set a property of the same name to the value of the Windows Installer directory.</span></span> <span data-ttu-id="04134-118">Lorsque la résolution de répertoire a lieu, le répertoire a une propriété du même nom, donc l’emplacement d’installation du répertoire est la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="04134-118">When directory resolution takes place, the directory has a property of the same name, so the install location of the directory is the value of the property.</span></span> <span data-ttu-id="04134-119">Les fichiers sont déplacés de l’emplacement source distinct vers le même emplacement cible.</span><span class="sxs-lookup"><span data-stu-id="04134-119">Files move from the distinct source location to the same target location.</span></span> <span data-ttu-id="04134-120">Ce processus doit supprimer complètement les conflits de fusion.</span><span class="sxs-lookup"><span data-stu-id="04134-120">This process should completely remove the merge conflicts.</span></span>

``` syntax
Warning: The 'ModuleInstallExecuteSequence' table contains a type 51 action 
(StartMenuFolder.<GUID>) for a pre-defined directory, but this action 
does not have sequence number '1'
```

<span data-ttu-id="04134-121">Si l’action n’a pas le numéro de séquence 1, il est possible qu’elle n’effectue pas de fusion dans la base de données cible suffisamment tôt dans la séquence pour fonctionner efficacement.</span><span class="sxs-lookup"><span data-stu-id="04134-121">If the action does not have sequence number 1, it may not merge in to the target database early enough in the sequence to work effectively.</span></span>

<span data-ttu-id="04134-122">Pour résoudre cet avertissement, définissez le numéro de séquence sur 1.</span><span class="sxs-lookup"><span data-stu-id="04134-122">To fix this warning, set the sequence number to 1.</span></span> <span data-ttu-id="04134-123">Notez que la plupart des outils de fusion actuels (mais pas certaines versions antérieures) génèrent ces actions personnalisées au moment de la fusion. par conséquent, il n’est pas toujours nécessaire de créer explicitement les actions dans le module de fusion.</span><span class="sxs-lookup"><span data-stu-id="04134-123">Note that most current merge tools (but not some older versions) will generate these custom actions at merge time, so it is not always necessary to explicitly author the actions into the merge module.</span></span>

``` syntax
Warning: The 'CustomAction' table contains a type 51 action (MyAppDataFolderAction) 
for a pre-defined directory, but the name is not the same as the target directory. 
Many merge tools will generate duplicate actions."
```

<span data-ttu-id="04134-124">Étant donné que la colonne CustomAction est la clé primaire de la table CustomAction, certains outils de fusion peuvent générer des actions en double, car le nom de l’action précréée est différent.</span><span class="sxs-lookup"><span data-stu-id="04134-124">Because the CustomAction column is the primary key of CustomAction table, some merge tools may generate duplicate actions because the pre-authored action name is different.</span></span>

<span data-ttu-id="04134-125">Pour résoudre cet avertissement, nommez l’action de la même façon que le répertoire cible.</span><span class="sxs-lookup"><span data-stu-id="04134-125">To fix this warning, name the action the same as the target directory.</span></span> <span data-ttu-id="04134-126">Notez que la plupart des outils de fusion actuels (mais pas certaines versions antérieures) génèrent ces actions personnalisées au moment de la fusion. il n’est donc pas toujours nécessaire de créer explicitement les actions dans le module de fusion.</span><span class="sxs-lookup"><span data-stu-id="04134-126">Note that most current merge tools (but not some older versions) generate these custom actions at merge time, so it is not always necessary to explicitly author the actions into the merge module.</span></span>

[<span data-ttu-id="04134-127">Table de répertoire</span><span class="sxs-lookup"><span data-stu-id="04134-127">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="04134-128">Répertoire</span><span class="sxs-lookup"><span data-stu-id="04134-128">Directory</span></span>          | <span data-ttu-id="04134-129">Répertoire \_ parent</span><span class="sxs-lookup"><span data-stu-id="04134-129">Directory\_Parent</span></span> | <span data-ttu-id="04134-130">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="04134-130">DefaultDir</span></span> |
|--------------------|-------------------|------------|
| <span data-ttu-id="04134-131">ProgramFilesFolder</span><span class="sxs-lookup"><span data-stu-id="04134-131">ProgramFilesFolder</span></span> | <span data-ttu-id="04134-132">Répertoire1</span><span class="sxs-lookup"><span data-stu-id="04134-132">Directory1</span></span>        | <span data-ttu-id="04134-133">Un</span><span class="sxs-lookup"><span data-stu-id="04134-133">A</span></span>          |
| <span data-ttu-id="04134-134">StartMenuFolder</span><span class="sxs-lookup"><span data-stu-id="04134-134">StartMenuFolder</span></span>    | <span data-ttu-id="04134-135">Directory2</span><span class="sxs-lookup"><span data-stu-id="04134-135">Directory2</span></span>        | <span data-ttu-id="04134-136">B:C</span><span class="sxs-lookup"><span data-stu-id="04134-136">B:C</span></span>        |
| <span data-ttu-id="04134-137">AppDataFolder</span><span class="sxs-lookup"><span data-stu-id="04134-137">AppDataFolder</span></span>      | <span data-ttu-id="04134-138">Directory3</span><span class="sxs-lookup"><span data-stu-id="04134-138">Directory3</span></span>        | <span data-ttu-id="04134-139">D</span><span class="sxs-lookup"><span data-stu-id="04134-139">D</span></span>          |
| <span data-ttu-id="04134-140">MyPicturesFolder</span><span class="sxs-lookup"><span data-stu-id="04134-140">MyPicturesFolder</span></span>   | <span data-ttu-id="04134-141">Directory4</span><span class="sxs-lookup"><span data-stu-id="04134-141">Directory4</span></span>        | <span data-ttu-id="04134-142">E</span><span class="sxs-lookup"><span data-stu-id="04134-142">E</span></span>          |



 

[<span data-ttu-id="04134-143">Table des composants</span><span class="sxs-lookup"><span data-stu-id="04134-143">Component Table</span></span>](component-table.md)



| <span data-ttu-id="04134-144">Composant</span><span class="sxs-lookup"><span data-stu-id="04134-144">Component</span></span>               | <span data-ttu-id="04134-145">Répertoire</span><span class="sxs-lookup"><span data-stu-id="04134-145">Directory</span></span>          |
|-------------------------|--------------------|
| <span data-ttu-id="04134-146">Composant1.<GUID></span><span class="sxs-lookup"><span data-stu-id="04134-146">Component1.<GUID></span></span> | <span data-ttu-id="04134-147">ProgramFilesFolder</span><span class="sxs-lookup"><span data-stu-id="04134-147">ProgramFilesFolder</span></span> |
| <span data-ttu-id="04134-148">Component2.<GUID></span><span class="sxs-lookup"><span data-stu-id="04134-148">Component2.<GUID></span></span> | <span data-ttu-id="04134-149">StartMenuFolder</span><span class="sxs-lookup"><span data-stu-id="04134-149">StartMenuFolder</span></span>    |
| <span data-ttu-id="04134-150">Component3.<GUID></span><span class="sxs-lookup"><span data-stu-id="04134-150">Component3.<GUID></span></span> | <span data-ttu-id="04134-151">AppDataFolder</span><span class="sxs-lookup"><span data-stu-id="04134-151">AppDataFolder</span></span>      |
| <span data-ttu-id="04134-152">Component4.<GUID></span><span class="sxs-lookup"><span data-stu-id="04134-152">Component4.<GUID></span></span> | <span data-ttu-id="04134-153">MyPicturesFolder</span><span class="sxs-lookup"><span data-stu-id="04134-153">MyPicturesFolder</span></span>   |



 

[<span data-ttu-id="04134-154">Table CustomAction</span><span class="sxs-lookup"><span data-stu-id="04134-154">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="04134-155">CustomAction</span><span class="sxs-lookup"><span data-stu-id="04134-155">CustomAction</span></span>                 | <span data-ttu-id="04134-156">Type</span><span class="sxs-lookup"><span data-stu-id="04134-156">Type</span></span> | <span data-ttu-id="04134-157">Source</span><span class="sxs-lookup"><span data-stu-id="04134-157">Source</span></span>                       | <span data-ttu-id="04134-158">Cible</span><span class="sxs-lookup"><span data-stu-id="04134-158">Target</span></span>              |
|------------------------------|------|------------------------------|---------------------|
| <span data-ttu-id="04134-159">StartMenuFolder.<GUID></span><span class="sxs-lookup"><span data-stu-id="04134-159">StartMenuFolder.<GUID></span></span> | <span data-ttu-id="04134-160">51</span><span class="sxs-lookup"><span data-stu-id="04134-160">51</span></span>   | <span data-ttu-id="04134-161">StartMenuFolder.<GUID></span><span class="sxs-lookup"><span data-stu-id="04134-161">StartMenuFolder.<GUID></span></span> | <span data-ttu-id="04134-162">\[StartMenuFolder\]</span><span class="sxs-lookup"><span data-stu-id="04134-162">\[StartMenuFolder\]</span></span> |
| <span data-ttu-id="04134-163">MyAppDataFolderAction</span><span class="sxs-lookup"><span data-stu-id="04134-163">MyAppDataFolderAction</span></span>        | <span data-ttu-id="04134-164">51</span><span class="sxs-lookup"><span data-stu-id="04134-164">51</span></span>   | <span data-ttu-id="04134-165">AppDataFolder.<GUID></span><span class="sxs-lookup"><span data-stu-id="04134-165">AppDataFolder.<GUID></span></span>   | <span data-ttu-id="04134-166">\[AppDataFolder\]</span><span class="sxs-lookup"><span data-stu-id="04134-166">\[AppDataFolder\]</span></span>   |



 

[<span data-ttu-id="04134-167">Table ModuleInstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="04134-167">ModuleInstallExecuteSequence Table</span></span>](moduleinstallexecutesequence-table.md)



| <span data-ttu-id="04134-168">Action</span><span class="sxs-lookup"><span data-stu-id="04134-168">Action</span></span>                       | <span data-ttu-id="04134-169">Séquence</span><span class="sxs-lookup"><span data-stu-id="04134-169">Sequence</span></span> | <span data-ttu-id="04134-170">BaseAction</span><span class="sxs-lookup"><span data-stu-id="04134-170">BaseAction</span></span> | <span data-ttu-id="04134-171">After</span><span class="sxs-lookup"><span data-stu-id="04134-171">After</span></span> | <span data-ttu-id="04134-172">Condition</span><span class="sxs-lookup"><span data-stu-id="04134-172">Condition</span></span> |
|------------------------------|----------|------------|-------|-----------|
| <span data-ttu-id="04134-173">StartMenuFolder.<GUID></span><span class="sxs-lookup"><span data-stu-id="04134-173">StartMenuFolder.<GUID></span></span> | <span data-ttu-id="04134-174">100</span><span class="sxs-lookup"><span data-stu-id="04134-174">100</span></span>      |            |       |           |



 

## <a name="related-topics"></a><span data-ttu-id="04134-175">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="04134-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04134-176">Référence ICE du module de fusion</span><span class="sxs-lookup"><span data-stu-id="04134-176">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



