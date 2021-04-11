---
description: ICE50 vérifie que les icônes de raccourci sont spécifiées pour s’afficher correctement et correspondent à l’extension du fichier cible.
ms.assetid: 19288c87-fddb-46c9-8145-59e1b870a261
title: ICE50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de88dda0dd1cdd18a10a35c32ef612acb75c871e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952596"
---
# <a name="ice50"></a><span data-ttu-id="30cc2-103">ICE50</span><span class="sxs-lookup"><span data-stu-id="30cc2-103">ICE50</span></span>

<span data-ttu-id="30cc2-104">ICE50 vérifie que les icônes de raccourci sont spécifiées pour s’afficher correctement et correspondent à l’extension du fichier cible.</span><span class="sxs-lookup"><span data-stu-id="30cc2-104">ICE50 checks that shortcut icons are specified to display correctly and match their target file's extension.</span></span>

## <a name="result"></a><span data-ttu-id="30cc2-105">Résultats</span><span class="sxs-lookup"><span data-stu-id="30cc2-105">Result</span></span>

<span data-ttu-id="30cc2-106">ICE50 publie un message d’erreur si l’extension de l’icône et les fichiers cibles ne correspondent pas.</span><span class="sxs-lookup"><span data-stu-id="30cc2-106">ICE50 posts an error message if the extension of the icon and target files do not match.</span></span> <span data-ttu-id="30cc2-107">ICE50 publie un avertissement si les icônes sont stockées dans des fichiers qui n’ont pas d’extension. exe ou. ico.</span><span class="sxs-lookup"><span data-stu-id="30cc2-107">ICE50 posts a warning if icons are stored in files that do not have an .exe or .ico extension.</span></span>

## <a name="example"></a><span data-ttu-id="30cc2-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="30cc2-108">Example</span></span>

<span data-ttu-id="30cc2-109">ICE50 signale l’erreur suivante pour l’exemple indiqué.</span><span class="sxs-lookup"><span data-stu-id="30cc2-109">ICE50 reports the following error for the example shown.</span></span>



| <span data-ttu-id="30cc2-110">Erreur ou avertissement ICE50</span><span class="sxs-lookup"><span data-stu-id="30cc2-110">ICE50 error or warning</span></span>                                                                                                              | <span data-ttu-id="30cc2-111">Description</span><span class="sxs-lookup"><span data-stu-id="30cc2-111">Description</span></span>                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30cc2-112">L’extension de l’icône « Icon2. dat » pour le raccourci « Shortcut2 » ne correspond pas à l’extension du fichier de clé pour le composant « COMPONENT2 ».</span><span class="sxs-lookup"><span data-stu-id="30cc2-112">The extension of Icon 'Icon2.dat' for Shortcut 'Shortcut2' does not match the extension of the Key File for component 'Component2'.</span></span> | <span data-ttu-id="30cc2-113">Si les extensions de l’icône et du fichier cible ne correspondent pas, le menu contextuel est incorrect lorsque le composant est publié.</span><span class="sxs-lookup"><span data-stu-id="30cc2-113">If the extensions of the icon and the target file do not match, the shortcut will not have the correct context menu when the component is advertised.</span></span> <span data-ttu-id="30cc2-114">Pour corriger cette erreur, renommez l’icône pour qu’elle corresponde à l’extension du fichier cible.</span><span class="sxs-lookup"><span data-stu-id="30cc2-114">To fix this error, rename the icon to match the extension of the target file.</span></span><br/> |
| <span data-ttu-id="30cc2-115">L’extension de l’icône' Icon1.bat 'pour le raccourci’Shortcut1 'n’est pas "exe" ou "ico".</span><span class="sxs-lookup"><span data-stu-id="30cc2-115">The extension of Icon 'Icon1.bat' for Shortcut 'Shortcut1' is not "exe" or "ico".</span></span> <span data-ttu-id="30cc2-116">L’icône ne s’affiche pas correctement.</span><span class="sxs-lookup"><span data-stu-id="30cc2-116">The Icon will not be displayed correctly.</span></span>         | <span data-ttu-id="30cc2-117">Toutes les versions du shell n’affichent pas correctement les icônes stockées dans les fichiers qui n’ont pas d’extension « exe » ou « ico ».</span><span class="sxs-lookup"><span data-stu-id="30cc2-117">Not all versions of the shell correctly display icons stored in files that do not have extensions of "exe" or "ico".</span></span> <span data-ttu-id="30cc2-118">Pour résoudre cet avertissement, renommez l’icône avec l’extension « exe » ou « ico ».</span><span class="sxs-lookup"><span data-stu-id="30cc2-118">To fix this warning, rename the icon have an extension of "exe" or "ico".</span></span><br/>                                      |



 

<span data-ttu-id="30cc2-119">[Table de fichiers](file-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="30cc2-119">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="30cc2-120">Fichier</span><span class="sxs-lookup"><span data-stu-id="30cc2-120">File</span></span>  | <span data-ttu-id="30cc2-121">FileName</span><span class="sxs-lookup"><span data-stu-id="30cc2-121">FileName</span></span>  |
|-------|-----------|
| <span data-ttu-id="30cc2-122">Fichier1</span><span class="sxs-lookup"><span data-stu-id="30cc2-122">File1</span></span> | <span data-ttu-id="30cc2-123">File1.bat</span><span class="sxs-lookup"><span data-stu-id="30cc2-123">File1.bat</span></span> |
| <span data-ttu-id="30cc2-124">Fichier2</span><span class="sxs-lookup"><span data-stu-id="30cc2-124">File2</span></span> | <span data-ttu-id="30cc2-125">File2.pl</span><span class="sxs-lookup"><span data-stu-id="30cc2-125">File2.pl</span></span>  |



 

<span data-ttu-id="30cc2-126">[Table des fonctionnalités](feature-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="30cc2-126">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="30cc2-127">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="30cc2-127">Feature</span></span>  |
|----------|
| <span data-ttu-id="30cc2-128">Feature1</span><span class="sxs-lookup"><span data-stu-id="30cc2-128">Feature1</span></span> |



 

<span data-ttu-id="30cc2-129">[Table des composants](component-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="30cc2-129">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="30cc2-130">Composant</span><span class="sxs-lookup"><span data-stu-id="30cc2-130">Component</span></span>  | <span data-ttu-id="30cc2-131">KeyPath</span><span class="sxs-lookup"><span data-stu-id="30cc2-131">KeyPath</span></span> |
|------------|---------|
| <span data-ttu-id="30cc2-132">Composant1</span><span class="sxs-lookup"><span data-stu-id="30cc2-132">Component1</span></span> | <span data-ttu-id="30cc2-133">Fichier1</span><span class="sxs-lookup"><span data-stu-id="30cc2-133">File1</span></span>   |
| <span data-ttu-id="30cc2-134">Component2</span><span class="sxs-lookup"><span data-stu-id="30cc2-134">Component2</span></span> | <span data-ttu-id="30cc2-135">Fichier2</span><span class="sxs-lookup"><span data-stu-id="30cc2-135">File2</span></span>   |



 

[<span data-ttu-id="30cc2-136">Table d’icônes</span><span class="sxs-lookup"><span data-stu-id="30cc2-136">Icon Table</span></span>](icon-table.md)



| <span data-ttu-id="30cc2-137">Nom</span><span class="sxs-lookup"><span data-stu-id="30cc2-137">Name</span></span>      | <span data-ttu-id="30cc2-138">Données</span><span class="sxs-lookup"><span data-stu-id="30cc2-138">Data</span></span>            |
|-----------|-----------------|
| <span data-ttu-id="30cc2-139">Icon1.bat</span><span class="sxs-lookup"><span data-stu-id="30cc2-139">Icon1.bat</span></span> | <span data-ttu-id="30cc2-140">\[Binary Data\]</span><span class="sxs-lookup"><span data-stu-id="30cc2-140">\[Binary Data\]</span></span> |
| <span data-ttu-id="30cc2-141">Icon2. dat</span><span class="sxs-lookup"><span data-stu-id="30cc2-141">Icon2.dat</span></span> | <span data-ttu-id="30cc2-142">\[Binary Data\]</span><span class="sxs-lookup"><span data-stu-id="30cc2-142">\[Binary Data\]</span></span> |



 

<span data-ttu-id="30cc2-143">[Table de raccourcis](shortcut-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="30cc2-143">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="30cc2-144">Raccourci</span><span class="sxs-lookup"><span data-stu-id="30cc2-144">Shortcut</span></span>  | <span data-ttu-id="30cc2-145">Composant</span><span class="sxs-lookup"><span data-stu-id="30cc2-145">Component</span></span>  | <span data-ttu-id="30cc2-146">Cible</span><span class="sxs-lookup"><span data-stu-id="30cc2-146">Target</span></span>   | <span data-ttu-id="30cc2-147">Icône\_</span><span class="sxs-lookup"><span data-stu-id="30cc2-147">Icon\_</span></span>    |
|-----------|------------|----------|-----------|
| <span data-ttu-id="30cc2-148">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="30cc2-148">Shortcut1</span></span> | <span data-ttu-id="30cc2-149">Composant1</span><span class="sxs-lookup"><span data-stu-id="30cc2-149">Component1</span></span> | <span data-ttu-id="30cc2-150">Feature1</span><span class="sxs-lookup"><span data-stu-id="30cc2-150">Feature1</span></span> | <span data-ttu-id="30cc2-151">Icon1.bat</span><span class="sxs-lookup"><span data-stu-id="30cc2-151">Icon1.bat</span></span> |
| <span data-ttu-id="30cc2-152">Shortcut2</span><span class="sxs-lookup"><span data-stu-id="30cc2-152">Shortcut2</span></span> | <span data-ttu-id="30cc2-153">Component2</span><span class="sxs-lookup"><span data-stu-id="30cc2-153">Component2</span></span> | <span data-ttu-id="30cc2-154">Feature1</span><span class="sxs-lookup"><span data-stu-id="30cc2-154">Feature1</span></span> | <span data-ttu-id="30cc2-155">Icon2. dat</span><span class="sxs-lookup"><span data-stu-id="30cc2-155">Icon2.dat</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="30cc2-156">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="30cc2-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30cc2-157">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="30cc2-157">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




