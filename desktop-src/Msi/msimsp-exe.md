---
description: La méthode recommandée pour générer un package de correctif consiste à utiliser des outils de création de correctifs tels que Msimsp.exe et Patchwiz.dll. L’outil Msimsp.exe est disponible uniquement dans les composants SDK Windows pour les développeurs Windows Installer.
ms.assetid: fa8e9d68-3db1-4d17-aa99-2ca0ed421c7a
title: Msimsp.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1810fd0c544695742273bbb0e63b22138529c129
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106520249"
---
# <a name="msimspexe"></a><span data-ttu-id="76ea8-104">Msimsp.exe</span><span class="sxs-lookup"><span data-stu-id="76ea8-104">Msimsp.exe</span></span>

<span data-ttu-id="76ea8-105">La méthode recommandée pour générer un package de correctif consiste à utiliser des outils de création de correctifs tels que Msimsp.exe et [Patchwiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="76ea8-105">The recommended method for generating a patch package is to use patch creation tools such as Msimsp.exe and [Patchwiz.dll](patchwiz-dll.md).</span></span> <span data-ttu-id="76ea8-106">L’outil Msimsp.exe est disponible uniquement dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="76ea8-106">The Msimsp.exe tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="76ea8-107">Msimsp.exe est un fichier exécutable qui appelle [Patchwiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="76ea8-107">Msimsp.exe is a executable file that calls [Patchwiz.dll](patchwiz-dll.md).</span></span> <span data-ttu-id="76ea8-108">L’outil peut être utilisé pour créer un package de correctifs en passant le chemin d’accès à un fichier de propriétés de création de correctifs (fichier. PCP) et le chemin d’accès au package de correctifs en cours de création.</span><span class="sxs-lookup"><span data-stu-id="76ea8-108">The tool can be used to create a patch package by passing in the path to a patch creation properties file (.pcp file) and the path to the patch package that is being created.</span></span> <span data-ttu-id="76ea8-109">Msimsp. ex peut également être utilisé pour créer un fichier journal et pour spécifier un dossier temporaire dans lequel les transformations, les armoires et les fichiers utilisés pour créer le package de correctif sont enregistrés.</span><span class="sxs-lookup"><span data-stu-id="76ea8-109">Msimsp.ex can also be used to create a log file and to specify a temporary folder in which the transforms, cabinets, and files that are used to create the patch package are saved.</span></span>

<span data-ttu-id="76ea8-110">La syntaxe de la ligne de commande pour Msimsp.exe est :</span><span class="sxs-lookup"><span data-stu-id="76ea8-110">The command-line syntax for Msimsp.exe is:</span></span>

<span data-ttu-id="76ea8-111">**Msimsp.exe-s** *\[ chemin d’accès au fichier \] . PCP* **-p** *\[ chemin d’accès \] au fichier. msp* **{options}**</span><span class="sxs-lookup"><span data-stu-id="76ea8-111">**Msimsp.exe -s** *\[path to .pcp file\]* **-p** *\[path to .msp file\]* **{options}**</span></span>

<span data-ttu-id="76ea8-112">Les options de ligne de commande ne respectent pas la casse, et les séparateurs de barres obliques peuvent être utilisés à la place d’un tiret.</span><span class="sxs-lookup"><span data-stu-id="76ea8-112">The command-line options are not case-sensitive, and slash delimiters can be used instead of a dash.</span></span> <span data-ttu-id="76ea8-113">Si aucune option n’est spécifiée, Msimsp.exe affiche les valeurs actuelles des propriétés des informations de résumé.</span><span class="sxs-lookup"><span data-stu-id="76ea8-113">If no options are specified, Msimsp.exe displays the current values of the summary Information properties.</span></span>

<dl> <dt>

<span data-ttu-id="76ea8-114"><span id="-s_path_to_.pcp_file_"></span><span id="-S_PATH_TO_.PCP_FILE_"></span>**-s**_\[ chemin d’accès au fichier \] . PCP_</span><span class="sxs-lookup"><span data-stu-id="76ea8-114"><span id="-s_path_to_.pcp_file_"></span><span id="-S_PATH_TO_.PCP_FILE_"></span>**-s**_\[path to .pcp file\]_</span></span>
</dt> <dd>

<span data-ttu-id="76ea8-115">Cette valeur est obligatoire et doit être suivie du chemin d’accès au fichier de propriétés de création de correctifs (extension. PCP).</span><span class="sxs-lookup"><span data-stu-id="76ea8-115">This is required and must be followed by the path to the patch creation properties file (.pcp extension).</span></span> <span data-ttu-id="76ea8-116">Pour plus d’informations, consultez [PatchWiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="76ea8-116">For more information, see [PatchWiz.dll](patchwiz-dll.md).</span></span>

</dd> <dt>

<span data-ttu-id="76ea8-117"><span id="-ppath_to_.msp_file"></span><span id="-PPATH_TO_.MSP_FILE"></span>**-p**_chemin d’accès au fichier. msp_</span><span class="sxs-lookup"><span data-stu-id="76ea8-117"><span id="-ppath_to_.msp_file"></span><span id="-PPATH_TO_.MSP_FILE"></span>**-p**_path to .msp file_</span></span>
</dt> <dd>

<span data-ttu-id="76ea8-118">Cette valeur est obligatoire et suivie du chemin d’accès au package de correctifs en cours de création (extension. msp).</span><span class="sxs-lookup"><span data-stu-id="76ea8-118">This is required and followed by the path to patch package that is being created (.msp extension).</span></span>

</dd> <dt>

<span data-ttu-id="76ea8-119"><span id="-fpath_to_temporary_folder"></span><span id="-FPATH_TO_TEMPORARY_FOLDER"></span>**-f**_chemin d’accès au dossier temporaire_</span><span class="sxs-lookup"><span data-stu-id="76ea8-119"><span id="-fpath_to_temporary_folder"></span><span id="-FPATH_TO_TEMPORARY_FOLDER"></span>**-f**_path to temporary folder_</span></span>
</dt> <dd>

<span data-ttu-id="76ea8-120">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="76ea8-120">Optional.</span></span> <span data-ttu-id="76ea8-121">Suivi du chemin d’accès au dossier temporaire.</span><span class="sxs-lookup"><span data-stu-id="76ea8-121">Followed by path to temporary folder.</span></span> <span data-ttu-id="76ea8-122">L’emplacement par défaut est% TMP% \\ ~ PCW \_ tmp. tmp \\ .</span><span class="sxs-lookup"><span data-stu-id="76ea8-122">The default location is %TMP%\\~pcw\_tmp.tmp\\.</span></span>

</dd> <dt>

<span data-ttu-id="76ea8-123"><span id="-k"></span><span id="-K"></span>**-k**</span><span class="sxs-lookup"><span data-stu-id="76ea8-123"><span id="-k"></span><span id="-K"></span>**-k**</span></span>
</dt> <dd>

<span data-ttu-id="76ea8-124">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="76ea8-124">Optional.</span></span> <span data-ttu-id="76ea8-125">Échoue si le dossier temporaire existe déjà.</span><span class="sxs-lookup"><span data-stu-id="76ea8-125">Fail if the temporary folder already exists.</span></span>

</dd> <dt>

<span data-ttu-id="76ea8-126"><span id="-lpath_to_log_file"></span><span id="-LPATH_TO_LOG_FILE"></span>**-l**_chemin du fichier journal_</span><span class="sxs-lookup"><span data-stu-id="76ea8-126"><span id="-lpath_to_log_file"></span><span id="-LPATH_TO_LOG_FILE"></span>**-l**_path to log file_</span></span>
</dt> <dd>

<span data-ttu-id="76ea8-127">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="76ea8-127">Optional.</span></span> <span data-ttu-id="76ea8-128">Suivi du chemin d’accès au fichier journal décrivant le processus de création des correctifs et les erreurs.</span><span class="sxs-lookup"><span data-stu-id="76ea8-128">Followed by the path to the log file that describes the patch creation process and errors.</span></span> <span data-ttu-id="76ea8-129">Pour plus d’informations, consultez [valeurs de retour pour UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).</span><span class="sxs-lookup"><span data-stu-id="76ea8-129">For more information, see [Return Values for UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="76ea8-130"><span id="-lppath_to_log_file_with_performance_data"></span><span id="-LPPATH_TO_LOG_FILE_WITH_PERFORMANCE_DATA"></span>**-**_chemin d’accès LP au fichier journal avec les données de performances_</span><span class="sxs-lookup"><span data-stu-id="76ea8-130"><span id="-lppath_to_log_file_with_performance_data"></span><span id="-LPPATH_TO_LOG_FILE_WITH_PERFORMANCE_DATA"></span>**-lp**_path to log file with performance data_</span></span>
</dt> <dd>

<span data-ttu-id="76ea8-131">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="76ea8-131">Optional.</span></span> <span data-ttu-id="76ea8-132">Suivi du chemin d’accès au fichier journal décrivant le processus de création des correctifs et les erreurs.</span><span class="sxs-lookup"><span data-stu-id="76ea8-132">Followed by the path to the log file that describes the patch creation process and errors.</span></span> <span data-ttu-id="76ea8-133">Cette option permet d’écrire les données de performances dans le fichier journal.</span><span class="sxs-lookup"><span data-stu-id="76ea8-133">This option writes performance data to log file.</span></span> <span data-ttu-id="76ea8-134">Cette option requiert la version 4,0 de Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="76ea8-134">This option requires version 4.0 of Patchwiz.dll.</span></span>

</dd> <dt>

<span data-ttu-id="76ea8-135"><span id="-d"></span><span id="-D"></span>**-d**</span><span class="sxs-lookup"><span data-stu-id="76ea8-135"><span id="-d"></span><span id="-D"></span>**-d**</span></span>
</dt> <dd>

<span data-ttu-id="76ea8-136">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="76ea8-136">Optional.</span></span> <span data-ttu-id="76ea8-137">Affiche une boîte de dialogue si la création du correctif se termine correctement.</span><span class="sxs-lookup"><span data-stu-id="76ea8-137">Displays a dialog if the patch creation completes successfully.</span></span>

</dd> <dt>

<span data-ttu-id="76ea8-138"><span id="-_"></span>**-?**</span><span class="sxs-lookup"><span data-stu-id="76ea8-138"><span id="-_"></span>**-?**</span></span>
</dt> <dd>

<span data-ttu-id="76ea8-139">Affiche l'aide de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="76ea8-139">Displays command-line help.</span></span>

</dd> </dl>

> [!Note]
> <span data-ttu-id="76ea8-140">Msimsp.exe peut échouer lorsqu’il appelle Makecab.exe s’il existe des valeurs dans la colonne fichier de la [table de fichiers](file-table.md) du package d’installation qui diffèrent uniquement par la casse.</span><span class="sxs-lookup"><span data-stu-id="76ea8-140">Msimsp.exe can fail when it calls Makecab.exe if there are values in the File column of the [File table](file-table.md) of the installation package that differ only by case.</span></span> <span data-ttu-id="76ea8-141">Windows Installer est sensible à la casse et permet à un package d’installation comme dans le tableau ci-dessous uniquement lorsque COMP1 et Comp2 sont installés dans des répertoires différents.</span><span class="sxs-lookup"><span data-stu-id="76ea8-141">Windows Installer is case-sensitive and allows an installation package such as in the table below only when Comp1 and Comp2 are installed into different directories.</span></span> <span data-ttu-id="76ea8-142">Toutefois, dans ce scénario, vous ne pouvez pas utiliser Msimsp.exe ou [Patchwiz.dll](patchwiz-dll.md) pour générer un correctif pour le package, car Msimsp.exe et Patchwiz.dll appellent Makecab.exe, ce qui ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="76ea8-142">However, in this scenario you cannot use Msimsp.exe or [Patchwiz.dll](patchwiz-dll.md) to generate a patch for the package, because Msimsp.exe and Patchwiz.dll call Makecab.exe, which is case-insensitive.</span></span>
> 
> <span data-ttu-id="76ea8-143">Évitez de créer un package d’installation, tel que la [table de fichiers](file-table.md)partielle suivante.</span><span class="sxs-lookup"><span data-stu-id="76ea8-143">Avoid authoring an installation package such as the following partial [File table](file-table.md).</span></span>
> 
> | <span data-ttu-id="76ea8-144">Fichier</span><span class="sxs-lookup"><span data-stu-id="76ea8-144">File</span></span>       | <span data-ttu-id="76ea8-145">-\_</span><span class="sxs-lookup"><span data-stu-id="76ea8-145">Component\_</span></span> | <span data-ttu-id="76ea8-146">FileName</span><span class="sxs-lookup"><span data-stu-id="76ea8-146">FileName</span></span>   |
> |------------|-------------|------------|
> | <span data-ttu-id="76ea8-147">readme.txt</span><span class="sxs-lookup"><span data-stu-id="76ea8-147">readme.txt</span></span> | <span data-ttu-id="76ea8-148">COMP1</span><span class="sxs-lookup"><span data-stu-id="76ea8-148">Comp1</span></span>       | <span data-ttu-id="76ea8-149">readme.txt</span><span class="sxs-lookup"><span data-stu-id="76ea8-149">readme.txt</span></span> |
> | <span data-ttu-id="76ea8-150">ReadMe.txt</span><span class="sxs-lookup"><span data-stu-id="76ea8-150">ReadMe.txt</span></span> | <span data-ttu-id="76ea8-151">COMP2</span><span class="sxs-lookup"><span data-stu-id="76ea8-151">Comp2</span></span>       | <span data-ttu-id="76ea8-152">readme.txt</span><span class="sxs-lookup"><span data-stu-id="76ea8-152">readme.txt</span></span> |


## <a name="related-topics"></a><span data-ttu-id="76ea8-153">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="76ea8-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76ea8-154">Création d’un package de correctifs</span><span class="sxs-lookup"><span data-stu-id="76ea8-154">Creating a Patch Package</span></span>](creating-a-patch-package.md)
</dt> <dt>

[<span data-ttu-id="76ea8-155">Exemple de mise à jour corrective de petite taille</span><span class="sxs-lookup"><span data-stu-id="76ea8-155">A Small Update Patching Example</span></span>](a-small-update-patching-example.md)
</dt> <dt>

[<span data-ttu-id="76ea8-156">Outils de développement Windows Installer</span><span class="sxs-lookup"><span data-stu-id="76ea8-156">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="76ea8-157">Versions, outils et redistribuables publiés</span><span class="sxs-lookup"><span data-stu-id="76ea8-157">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



