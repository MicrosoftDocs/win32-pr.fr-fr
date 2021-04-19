---
description: ICE91 publie un avertissement en cas d’installation d’un fichier, d’un fichier. ini ou d’un fichier de raccourci dans un répertoire par utilisateur.
ms.assetid: 1834d841-b1d9-4646-8057-a41dd88310b6
title: ICE91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f5723369c21894817dacbc1755430a31f17199
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521325"
---
# <a name="ice91"></a><span data-ttu-id="1a8dc-103">ICE91</span><span class="sxs-lookup"><span data-stu-id="1a8dc-103">ICE91</span></span>

<span data-ttu-id="1a8dc-104">ICE91 publie un avertissement en cas d’installation d’un fichier, d’un fichier. ini ou d’un fichier de raccourci dans un répertoire par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-104">ICE91 posts a warning if a file, .ini file, or shortcut file is installed into a per-user only directory.</span></span> <span data-ttu-id="1a8dc-105">Ces avertissements sont inoffensifs si le package est utilisé uniquement pour l’installation dans le [contexte d’installation](installation-context.md) par utilisateur et jamais pour les installations par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-105">These warnings are harmless if the package is only used for installation in the per-user [installation context](installation-context.md) and never used for per-machine installations.</span></span>

<span data-ttu-id="1a8dc-106">Les fichiers, les fichiers. ini ou les raccourcis des répertoires par utilisateur uniquement sont installés dans un profil utilisateur particulier.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-106">Files, .ini files, or shortcuts in per-user only directories are installed into a particular user's profile.</span></span> <span data-ttu-id="1a8dc-107">Même si l’utilisateur définit la propriété [**ALLUSERS**](allusers.md) pour les installations par ordinateur, les fichiers, les fichiers. ini ou les raccourcis dans les répertoires par utilisateur uniquement ne sont pas copiés dans le profil « tous les utilisateurs » et ne sont pas disponibles pour les autres utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-107">Even if the user sets the [**ALLUSERS**](allusers.md) property for a per-machine installations, files, .ini files, or shortcuts in per-user only directories are not copied in to the "All Users" profile and are not available to other users.</span></span> <span data-ttu-id="1a8dc-108">Les répertoires par utilisateur uniquement ne varient pas avec la propriété **ALLUSERS** .</span><span class="sxs-lookup"><span data-stu-id="1a8dc-108">The per-user only directories do not vary with the **ALLUSERS** property.</span></span> <span data-ttu-id="1a8dc-109">Voici une liste des répertoires par utilisateur uniquement :</span><span class="sxs-lookup"><span data-stu-id="1a8dc-109">The following is a list of the per-user only directories:</span></span>

-   <span data-ttu-id="1a8dc-110">AppDataFolder</span><span class="sxs-lookup"><span data-stu-id="1a8dc-110">AppDataFolder</span></span>
-   <span data-ttu-id="1a8dc-111">FavoritesFolder</span><span class="sxs-lookup"><span data-stu-id="1a8dc-111">FavoritesFolder</span></span>
-   <span data-ttu-id="1a8dc-112">NetHoodFolder</span><span class="sxs-lookup"><span data-stu-id="1a8dc-112">NetHoodFolder</span></span>
-   <span data-ttu-id="1a8dc-113">PersonalFolder</span><span class="sxs-lookup"><span data-stu-id="1a8dc-113">PersonalFolder</span></span>
-   <span data-ttu-id="1a8dc-114">PrintHoodFolder</span><span class="sxs-lookup"><span data-stu-id="1a8dc-114">PrintHoodFolder</span></span>
-   <span data-ttu-id="1a8dc-115">RecentFolder</span><span class="sxs-lookup"><span data-stu-id="1a8dc-115">RecentFolder</span></span>
-   <span data-ttu-id="1a8dc-116">SendToFolder</span><span class="sxs-lookup"><span data-stu-id="1a8dc-116">SendToFolder</span></span>
-   <span data-ttu-id="1a8dc-117">MyPicturesFolder</span><span class="sxs-lookup"><span data-stu-id="1a8dc-117">MyPicturesFolder</span></span>
-   <span data-ttu-id="1a8dc-118">LocalAppDataFolder</span><span class="sxs-lookup"><span data-stu-id="1a8dc-118">LocalAppDataFolder</span></span>

## <a name="result"></a><span data-ttu-id="1a8dc-119">Résultats</span><span class="sxs-lookup"><span data-stu-id="1a8dc-119">Result</span></span>

<span data-ttu-id="1a8dc-120">ICE91 publie les avertissements suivants.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-120">ICE91 posts the following warnings.</span></span>



| <span data-ttu-id="1a8dc-121">AVERTISSEMENT ICE91</span><span class="sxs-lookup"><span data-stu-id="1a8dc-121">ICE91 warning</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="1a8dc-122">Description</span><span class="sxs-lookup"><span data-stu-id="1a8dc-122">Description</span></span>                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a8dc-123">Le fichier « \[ 1 \] » sera installé dans le répertoire par utilisateur « \[ 2 \] » qui ne varie pas en fonction de la valeur de [**ALLUSERS**](allusers.md) .</span><span class="sxs-lookup"><span data-stu-id="1a8dc-123">The file '\[1\]' will be installed to the per user directory '\[2\]' that does not vary based on [**ALLUSERS**](allusers.md) value.</span></span> <span data-ttu-id="1a8dc-124">Ce fichier ne sera pas copié dans le profil de chaque utilisateur même si une installation par ordinateur est souhaitée.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-124">This file won't be copied to each user's profile even if a per machine installation is desired.</span></span>     | <span data-ttu-id="1a8dc-125">Le fichier est installé dans un répertoire par utilisateur uniquement.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-125">The file is installed into a per-user only directory.</span></span> <span data-ttu-id="1a8dc-126">Il n’est pas installé dans le profil de chaque utilisateur au cours d’une installation par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-126">It is not installed into each user's profile during a per-machine installation.</span></span>      |
| <span data-ttu-id="1a8dc-127">Le IniFile « \[ 1 \] » sera installé dans le répertoire par utilisateur « \[ 2 \] » qui ne varie pas en fonction de la valeur de [**ALLUSERS**](allusers.md) .</span><span class="sxs-lookup"><span data-stu-id="1a8dc-127">The IniFile '\[1\]' will be installed to the per user directory '\[2\]' that does not vary based on [**ALLUSERS**](allusers.md) value.</span></span> <span data-ttu-id="1a8dc-128">Ce fichier ne sera pas copié dans le profil de chaque utilisateur même si une installation par ordinateur est souhaitée.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-128">This file won't be copied to each user's profile even if a per machine installation is desired.</span></span>  | <span data-ttu-id="1a8dc-129">Le fichier. ini est installé dans un répertoire par utilisateur uniquement.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-129">The .ini file is installed into a per-user only directory.</span></span> <span data-ttu-id="1a8dc-130">Il n’est pas installé dans le profil de chaque utilisateur au cours d’une installation par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-130">It is not installed into each user's profile during a per-machine installation.</span></span> |
| <span data-ttu-id="1a8dc-131">Le raccourci « \[ 1 \] » sera installé dans le répertoire par utilisateur « \[ 2 \] » qui ne varie pas en fonction de la valeur de [**ALLUSERS**](allusers.md) .</span><span class="sxs-lookup"><span data-stu-id="1a8dc-131">The shortcut '\[1\]' will be installed to the per user directory '\[2\]' that does not vary based on [**ALLUSERS**](allusers.md) value.</span></span> <span data-ttu-id="1a8dc-132">Ce fichier ne sera pas copié dans le profil de chaque utilisateur même si une installation par ordinateur est souhaitée.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-132">This file won't be copied to each user's profile even if a per machine installation is desired.</span></span> | <span data-ttu-id="1a8dc-133">Le raccourci est installé dans un répertoire par utilisateur uniquement.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-133">The shortcut is installed into a per-user only directory.</span></span> <span data-ttu-id="1a8dc-134">Il n’est pas installé dans le profil de chaque utilisateur au cours d’une installation par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="1a8dc-134">It is not installed into each user's profile during a per-machine installation.</span></span>  |



 

## <a name="example"></a><span data-ttu-id="1a8dc-135">Exemple</span><span class="sxs-lookup"><span data-stu-id="1a8dc-135">Example</span></span>

<span data-ttu-id="1a8dc-136">ICE91 signale les avertissements suivants pour l’exemple :</span><span class="sxs-lookup"><span data-stu-id="1a8dc-136">ICE91 reports the following warnings for the example:</span></span>

``` syntax
The file 'File1' will be installed to the per user directory 'MyPicturesFolder' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.

The IniFile 'IniFile1' will be installed to the per user directory 'MyIniDir' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.

The shortcut 'Shortcut1' will be installed to the per user directory 'MyShortcutDir' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.
```

<span data-ttu-id="1a8dc-137">[Table de fichiers](file-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="1a8dc-137">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="1a8dc-138">Fichier</span><span class="sxs-lookup"><span data-stu-id="1a8dc-138">File</span></span>  | <span data-ttu-id="1a8dc-139">-\_</span><span class="sxs-lookup"><span data-stu-id="1a8dc-139">Component\_</span></span> |
|-------|-------------|
| <span data-ttu-id="1a8dc-140">Fichier1</span><span class="sxs-lookup"><span data-stu-id="1a8dc-140">File1</span></span> | <span data-ttu-id="1a8dc-141">C1</span><span class="sxs-lookup"><span data-stu-id="1a8dc-141">C1</span></span>          |



 

<span data-ttu-id="1a8dc-142">[Table de composants](component-table.md) (partielle) (partielle) (partielle)</span><span class="sxs-lookup"><span data-stu-id="1a8dc-142">[Component Table](component-table.md) (partial) (partial) (partial) (partial)</span></span>



| <span data-ttu-id="1a8dc-143">Composant</span><span class="sxs-lookup"><span data-stu-id="1a8dc-143">Component</span></span> | <span data-ttu-id="1a8dc-144">Répertoire\_</span><span class="sxs-lookup"><span data-stu-id="1a8dc-144">Directory\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="1a8dc-145">C1</span><span class="sxs-lookup"><span data-stu-id="1a8dc-145">C1</span></span>        | <span data-ttu-id="1a8dc-146">MyDir</span><span class="sxs-lookup"><span data-stu-id="1a8dc-146">MyDir</span></span>       |



 

[<span data-ttu-id="1a8dc-147">Table IniFile</span><span class="sxs-lookup"><span data-stu-id="1a8dc-147">IniFile Table</span></span>](inifile-table.md)



| <span data-ttu-id="1a8dc-148">IniFile</span><span class="sxs-lookup"><span data-stu-id="1a8dc-148">IniFile</span></span>  | <span data-ttu-id="1a8dc-149">DirProperty</span><span class="sxs-lookup"><span data-stu-id="1a8dc-149">DirProperty</span></span> |
|----------|-------------|
| <span data-ttu-id="1a8dc-150">IniFile1</span><span class="sxs-lookup"><span data-stu-id="1a8dc-150">IniFile1</span></span> | <span data-ttu-id="1a8dc-151">MyIniDir</span><span class="sxs-lookup"><span data-stu-id="1a8dc-151">MyIniDir</span></span>    |



 

[<span data-ttu-id="1a8dc-152">Tableau de raccourcis</span><span class="sxs-lookup"><span data-stu-id="1a8dc-152">Shortcut Table</span></span>](shortcut-table.md)



| <span data-ttu-id="1a8dc-153">Raccourci</span><span class="sxs-lookup"><span data-stu-id="1a8dc-153">Shortcut</span></span>  | <span data-ttu-id="1a8dc-154">Répertoire\_</span><span class="sxs-lookup"><span data-stu-id="1a8dc-154">Directory\_</span></span>   |
|-----------|---------------|
| <span data-ttu-id="1a8dc-155">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="1a8dc-155">Shortcut1</span></span> | <span data-ttu-id="1a8dc-156">MyShortcutDir</span><span class="sxs-lookup"><span data-stu-id="1a8dc-156">MyShortcutDir</span></span> |



 

[<span data-ttu-id="1a8dc-157">Table de répertoire</span><span class="sxs-lookup"><span data-stu-id="1a8dc-157">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="1a8dc-158">Répertoire</span><span class="sxs-lookup"><span data-stu-id="1a8dc-158">Directory</span></span>     | <span data-ttu-id="1a8dc-159">Répertoire \_ parent</span><span class="sxs-lookup"><span data-stu-id="1a8dc-159">Directory\_Parent</span></span>  |
|---------------|--------------------|
| <span data-ttu-id="1a8dc-160">MyDir</span><span class="sxs-lookup"><span data-stu-id="1a8dc-160">MyDir</span></span>         | <span data-ttu-id="1a8dc-161">FavoritesFolder</span><span class="sxs-lookup"><span data-stu-id="1a8dc-161">FavoritesFolder</span></span>    |
| <span data-ttu-id="1a8dc-162">MyIniDir</span><span class="sxs-lookup"><span data-stu-id="1a8dc-162">MyIniDir</span></span>      | <span data-ttu-id="1a8dc-163">LocalAppDataFolder</span><span class="sxs-lookup"><span data-stu-id="1a8dc-163">LocalAppDataFolder</span></span> |
| <span data-ttu-id="1a8dc-164">MyShortcutDir</span><span class="sxs-lookup"><span data-stu-id="1a8dc-164">MyShortcutDir</span></span> | <span data-ttu-id="1a8dc-165">PersonalFolder</span><span class="sxs-lookup"><span data-stu-id="1a8dc-165">PersonalFolder</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="1a8dc-166">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1a8dc-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a8dc-167">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="1a8dc-167">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



