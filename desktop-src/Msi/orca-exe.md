---
description: Orca.exe est un éditeur de table de base de données pour la création et la modification des packages Windows Installer et des modules de fusion.
ms.assetid: 4dddc262-1271-4e00-a986-53380b957b17
title: Orca.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4647b137650bfba521dba3976ea7a1ae66451ce
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102158"
---
# <a name="orcaexe"></a><span data-ttu-id="3d8f4-103">Orca.exe</span><span class="sxs-lookup"><span data-stu-id="3d8f4-103">Orca.exe</span></span>

<span data-ttu-id="3d8f4-104">Orca.exe est un éditeur de table de base de données pour la création et la modification des packages Windows Installer et des modules de fusion.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-104">Orca.exe is a database table editor for creating and editing Windows Installer packages and merge modules.</span></span> <span data-ttu-id="3d8f4-105">L’outil fournit une interface graphique pour la validation, en mettant en surbrillance les entrées particulières où se produisent des erreurs ou des avertissements de validation.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-105">The tool provides a graphical interface for validation, highlighting the particular entries where validation errors or warnings occur.</span></span>

<span data-ttu-id="3d8f4-106">Cet outil est disponible uniquement dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="3d8f4-106">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="3d8f4-107">Elle est fournie sous la forme d’un fichier de Orca.msi.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-107">It is provided as an Orca.msi file.</span></span> <span data-ttu-id="3d8f4-108">Après avoir installé les composants SDK Windows pour Windows Installer les développeurs, double-cliquez sur Orca.msi pour installer le fichier Orca.exe.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-108">After installing the Windows SDK Components for Windows Installer Developers, double click Orca.msi to install the Orca.exe file.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d8f4-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d8f4-109">Syntax</span></span>

<span data-ttu-id="3d8f4-110">\**Orca\*\*\*\[\<options>\]\[\<source file>\]*</span><span class="sxs-lookup"><span data-stu-id="3d8f4-110">**orca** *\[\<options>\]\[\<source file>\]*</span></span>

## <a name="command-line-options"></a><span data-ttu-id="3d8f4-111">Options de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="3d8f4-111">Command Line Options</span></span>

<span data-ttu-id="3d8f4-112">Orca.exe utilise les options de ligne de commande suivantes qui ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-112">Orca.exe uses the following case-insensitive command line options.</span></span> <span data-ttu-id="3d8f4-113">Un séparateur de barre oblique peut également être utilisé à la place d’un tiret.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-113">A slash delimiter may also be used in place of a dash.</span></span>



| <span data-ttu-id="3d8f4-114">Option</span><span class="sxs-lookup"><span data-stu-id="3d8f4-114">Option</span></span> | <span data-ttu-id="3d8f4-115">Description</span><span class="sxs-lookup"><span data-stu-id="3d8f4-115">Description</span></span>                                                 |
|--------|-------------------------------------------------------------|
| <span data-ttu-id="3d8f4-116">-q</span><span class="sxs-lookup"><span data-stu-id="3d8f4-116">-q</span></span>     | <span data-ttu-id="3d8f4-117">Mode silencieux</span><span class="sxs-lookup"><span data-stu-id="3d8f4-117">Quiet mode</span></span>                                                  |
| <span data-ttu-id="3d8f4-118">-S</span><span class="sxs-lookup"><span data-stu-id="3d8f4-118">-s</span></span>     | <span data-ttu-id="3d8f4-119"><base *de données> schéma* \[ « Orca. dat »-valeur par défaut\]</span><span class="sxs-lookup"><span data-stu-id="3d8f4-119"><*database*> Schema database \["orca.dat" - default\]</span></span> |
| <span data-ttu-id="3d8f4-120">-?</span><span class="sxs-lookup"><span data-stu-id="3d8f4-120">-?</span></span>     | <span data-ttu-id="3d8f4-121">Boîte de dialogue d’aide</span><span class="sxs-lookup"><span data-stu-id="3d8f4-121">Help dialog</span></span>                                                 |



 

<span data-ttu-id="3d8f4-122">Orca.exe utilise les options de ligne de commande suivantes qui ne respectent pas la casse avec les modules de fusion.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-122">Orca.exe uses the following case-insensitive command line options with merge modules.</span></span> <span data-ttu-id="3d8f4-123">Un séparateur de barre oblique peut également être utilisé à la place d’un tiret.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-123">A slash delimiter may also be used in place of a dash.</span></span> <span data-ttu-id="3d8f4-124">Lorsque vous effectuez une fusion, les>-f,-m et <*sourceFile* sont tous obligatoires.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-124">When performing a merge the -f, -m and <*sourcefile*> are all required.</span></span>



| <span data-ttu-id="3d8f4-125">Option</span><span class="sxs-lookup"><span data-stu-id="3d8f4-125">Option</span></span>     | <span data-ttu-id="3d8f4-126">Description</span><span class="sxs-lookup"><span data-stu-id="3d8f4-126">Description</span></span>                                                                |
|------------|----------------------------------------------------------------------------|
| <span data-ttu-id="3d8f4-127">-c</span><span class="sxs-lookup"><span data-stu-id="3d8f4-127">-c</span></span>         | <span data-ttu-id="3d8f4-128">Valider la fusion dans la base de données si aucune erreur n’est détectée.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-128">Commit merge to database if no errors.</span></span>                                     |
| <span data-ttu-id="3d8f4-129">-!</span><span class="sxs-lookup"><span data-stu-id="3d8f4-129">-!</span></span>         | <span data-ttu-id="3d8f4-130">Validation de la fusion dans une base de données même en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-130">Commit merge to a database even if there are errors.</span></span>                       |
| <span data-ttu-id="3d8f4-131">-M</span><span class="sxs-lookup"><span data-stu-id="3d8f4-131">-m</span></span>         | <span data-ttu-id="3d8f4-132"><*module*> module de fusion à fusionner dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-132"><*module*> Merge Module to merge into database.</span></span>                      |
| <span data-ttu-id="3d8f4-133">-f</span><span class="sxs-lookup"><span data-stu-id="3d8f4-133">-f</span></span>         | <span data-ttu-id="3d8f4-134">Fonctionnalité \[ : la \] ou les fonctionnalités feature2 pour se connecter au module de fusion.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-134">Feature\[:Feature2\] Feature(s) to connect to Merge Module.</span></span>                |
| <span data-ttu-id="3d8f4-135">-r</span><span class="sxs-lookup"><span data-stu-id="3d8f4-135">-r</span></span>         | <span data-ttu-id="3d8f4-136"><*ID de répertoire*> entrée de répertoire pour la redirection racine du module.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-136"><*directory id*> Directory entry for the module root redirection.</span></span>    |
| <span data-ttu-id="3d8f4-137">-X</span><span class="sxs-lookup"><span data-stu-id="3d8f4-137">-x</span></span>         | <span data-ttu-id="3d8f4-138"><*répertoire*> de l’extraction des fichiers vers une image sous le répertoire.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-138"><*directory*> Extract files to an image under the directory.</span></span>         |
| <span data-ttu-id="3d8f4-139">-g</span><span class="sxs-lookup"><span data-stu-id="3d8f4-139">-g</span></span>         | <span data-ttu-id="3d8f4-140"><*langage> langage* utilisé pour ouvrir un module.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-140"><*language*> Language used to open a module.</span></span>                         |
| <span data-ttu-id="3d8f4-141">-l</span><span class="sxs-lookup"><span data-stu-id="3d8f4-141">-l</span></span>         | <span data-ttu-id="3d8f4-142"><fichier *journal*> fichier à utiliser en tant que journal, ajouter s’il existe déjà.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-142"><*log file*> File to use as a log, append if it already exists.</span></span>      |
| <span data-ttu-id="3d8f4-143">-i</span><span class="sxs-lookup"><span data-stu-id="3d8f4-143">-i</span></span>         | <span data-ttu-id="3d8f4-144"><*répertoire*> de l’extraction des fichiers vers l’image source sous le répertoire.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-144"><*directory*> Extract files to the source image under the directory.</span></span> |
| <span data-ttu-id="3d8f4-145">-CAB</span><span class="sxs-lookup"><span data-stu-id="3d8f4-145">-cab</span></span>       | <span data-ttu-id="3d8f4-146"><*nom* de fichier> de l’extraction de l’armoire MSM vers le fichier.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-146"><*filename*> Extract the MSM cabinet to file.</span></span>                        |
| <span data-ttu-id="3d8f4-147">-lfn</span><span class="sxs-lookup"><span data-stu-id="3d8f4-147">-lfn</span></span>       | <span data-ttu-id="3d8f4-148">Utilisez des noms de fichiers longs pendant l’extraction.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-148">Use Long File Names during the extraction.</span></span>                                 |
| <span data-ttu-id="3d8f4-149">-configurer</span><span class="sxs-lookup"><span data-stu-id="3d8f4-149">-configure</span></span> | <span data-ttu-id="3d8f4-150"><*filename*> configurer le module à l’aide des données d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-150"><*filename*> Configure the module using data from a file.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="3d8f4-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3d8f4-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d8f4-152">Outils de développement Windows Installer</span><span class="sxs-lookup"><span data-stu-id="3d8f4-152">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="3d8f4-153">Versions, outils et redistribuables publiés</span><span class="sxs-lookup"><span data-stu-id="3d8f4-153">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



