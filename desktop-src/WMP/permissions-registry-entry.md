---
title: Entrée de registre des autorisations
description: Entrée de registre des autorisations
ms.assetid: 01d55d2d-fe29-4006-a34b-9fbc730f9cbc
keywords:
- Windows Media Player, extensions de nom de fichier
- Lecteur Windows Media, autorisations
- Lecteur Windows Media, registre
- Registre, extensions de noms de fichiers
- Registre, autorisations
- Registre, paramètres pour le lecteur Windows Media
- paramètres de registre de l’extension de nom de fichier
- autorisations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aec86b4facec4babed4afed04ca342903670dbb
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030780"
---
# <a name="permissions-registry-entry"></a><span data-ttu-id="e0244-111">Entrée de registre des autorisations</span><span class="sxs-lookup"><span data-stu-id="e0244-111">Permissions Registry Entry</span></span>

<span data-ttu-id="e0244-112">Lorsque le lecteur Windows Media rencontre une extension de nom de fichier personnalisée, il recherche une sous-clé de Registre qui correspond à l’extension.</span><span class="sxs-lookup"><span data-stu-id="e0244-112">When Windows Media Player encounters a custom file name extension, it looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="e0244-113">La sous-clé est décrite dans les paramètres de registre de l' [extension de nom de fichier](file-name-extension-registry-settings.md).</span><span class="sxs-lookup"><span data-stu-id="e0244-113">The subkey is described in [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="e0244-114">L’une des entrées de Registre qui peuvent apparaître sous la sous-clé de l’extension est l’entrée d' **autorisations** .</span><span class="sxs-lookup"><span data-stu-id="e0244-114">One of the registry entries that can appear under the extension's subkey is the **Permissions** entry.</span></span>

<span data-ttu-id="e0244-115">L’entrée **autorisations** spécifie les actions que le lecteur Windows Media est autorisé à effectuer sur les fichiers qui ont l’extension personnalisée.</span><span class="sxs-lookup"><span data-stu-id="e0244-115">The **Permissions** entry specifies the actions that Windows Media Player is allowed to perform on files that have the custom extension.</span></span> <span data-ttu-id="e0244-116">L’entrée d' **autorisation** se présente sous la forme suivante.</span><span class="sxs-lookup"><span data-stu-id="e0244-116">The **Permissions** entry has the following form.</span></span>



| <span data-ttu-id="e0244-117">Nom</span><span class="sxs-lookup"><span data-stu-id="e0244-117">Name</span></span>        | <span data-ttu-id="e0244-118">Type</span><span class="sxs-lookup"><span data-stu-id="e0244-118">Type</span></span>           | <span data-ttu-id="e0244-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0244-119">Value</span></span>                                                                  |
|-------------|----------------|------------------------------------------------------------------------|
| <span data-ttu-id="e0244-120">Autorisations</span><span class="sxs-lookup"><span data-stu-id="e0244-120">Permissions</span></span> | <span data-ttu-id="e0244-121">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="e0244-121">**REG\_DWORD**</span></span> | <span data-ttu-id="e0244-122">Ensemble d’indicateurs, chacun d’entre eux octroyant l’autorisation pour une action spécifique.</span><span class="sxs-lookup"><span data-stu-id="e0244-122">A set of flags, each of which grants permission for a specific action.</span></span> |



 

<span data-ttu-id="e0244-123">La valeur de l’entrée d' **autorisation** est une **opération de bits or d'** un ou plusieurs des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="e0244-123">The value of the **Permissions** entry is a bitwise **OR** of one or more of the following flags.</span></span>



| <span data-ttu-id="e0244-124">Flag (valeur décimale)</span><span class="sxs-lookup"><span data-stu-id="e0244-124">Flag (decimal value)</span></span> | <span data-ttu-id="e0244-125">Description</span><span class="sxs-lookup"><span data-stu-id="e0244-125">Description</span></span>                                                                                                                                                                                                                                                                   |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0244-126">1</span><span class="sxs-lookup"><span data-stu-id="e0244-126">1</span></span>                    | <span data-ttu-id="e0244-127">Autorisation de lecture.</span><span class="sxs-lookup"><span data-stu-id="e0244-127">Permission for playback.</span></span> <span data-ttu-id="e0244-128">Les fichiers dont l’extension de nom de fichier est enregistrée peuvent être lus.</span><span class="sxs-lookup"><span data-stu-id="e0244-128">Files having the registered file name extension can be played.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="e0244-129">2</span><span class="sxs-lookup"><span data-stu-id="e0244-129">2</span></span>                    | <span data-ttu-id="e0244-130">Autorisation pour la suppression du dossier.</span><span class="sxs-lookup"><span data-stu-id="e0244-130">Permission for folder drop.</span></span> <span data-ttu-id="e0244-131">Les fichiers dont l’extension de nom de fichier est enregistrée seront inclus dans la sélection créée lorsque l’utilisateur fait glisser un dossier contenant les fichiers et le supprime de l’interface utilisateur du lecteur.</span><span class="sxs-lookup"><span data-stu-id="e0244-131">Files having the registered file name extension will be included in the playlist created when the user drags a folder containing the files and drops it on the user interface of the Player.</span></span>                                                      |
| <span data-ttu-id="e0244-132">4</span><span class="sxs-lookup"><span data-stu-id="e0244-132">4</span></span>                    | <span data-ttu-id="e0244-133">Autorisation pour CD multimédia.</span><span class="sxs-lookup"><span data-stu-id="e0244-133">Permission for media CD.</span></span> <span data-ttu-id="e0244-134">Les fichiers dont l’extension de nom de fichier est enregistrée seront inclus dans la sélection créée lorsqu’un CD contenant les fichiers est inséré dans le lecteur de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="e0244-134">Files having the registered file name extension will be included in the playlist created when a CD containing the files is inserted into the CD-ROM drive.</span></span>                                                                                           |
| <span data-ttu-id="e0244-135">8</span><span class="sxs-lookup"><span data-stu-id="e0244-135">8</span></span>                    | <span data-ttu-id="e0244-136">Autorisation pour la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="e0244-136">Permission for the library.</span></span> <span data-ttu-id="e0244-137">Les fichiers dont l’extension de nom de fichier est enregistrée peuvent être ajoutés à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="e0244-137">Files having the registered file name extension can be added to the library.</span></span> <span data-ttu-id="e0244-138">Requis pour les plug-ins de conversion.</span><span class="sxs-lookup"><span data-stu-id="e0244-138">Required for conversion plug-ins.</span></span>                                                                                                                                    |
| <span data-ttu-id="e0244-139">16</span><span class="sxs-lookup"><span data-stu-id="e0244-139">16</span></span>                   | <span data-ttu-id="e0244-140">Autorisation pour la diffusion en continu HTML.</span><span class="sxs-lookup"><span data-stu-id="e0244-140">Permission for HTML streaming.</span></span> <span data-ttu-id="e0244-141">Les fichiers dont l’extension de nom de fichier est enregistrée sont insérés dans le cache Internet Explorer lorsqu’ils sont remis à partir d’un flux Web.</span><span class="sxs-lookup"><span data-stu-id="e0244-141">Files having the registered file name extension will be inserted into the Internet Explorer cache when delivered from a Web stream.</span></span>                                                                                                            |
| <span data-ttu-id="e0244-142">128</span><span class="sxs-lookup"><span data-stu-id="e0244-142">128</span></span>                  | <span data-ttu-id="e0244-143">Autorisation de transcodage.</span><span class="sxs-lookup"><span data-stu-id="e0244-143">Permission for transcoding.</span></span> <span data-ttu-id="e0244-144">Les fichiers dont l’extension de nom de fichier est enregistrée peuvent être transcodés au format Windows Media sous certaines conditions.</span><span class="sxs-lookup"><span data-stu-id="e0244-144">Files having the registered file name extension can be transcoded to Windows Media Format under certain conditions.</span></span> <span data-ttu-id="e0244-145">Consultez [IWMPTranscodePolicy :: allowTranscode](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmptranscodepolicy-allowtranscode).</span><span class="sxs-lookup"><span data-stu-id="e0244-145">See [IWMPTranscodePolicy::allowTranscode](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmptranscodepolicy-allowtranscode).</span></span> <span data-ttu-id="e0244-146">Requiert le lecteur Windows Media 10 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="e0244-146">Requires Windows Media Player 10 or later.</span></span> |



 

<span data-ttu-id="e0244-147">Lorsque l’utilisateur tente de lire un fichier multimédia qui a une extension de nom de fichier personnalisée, le lecteur Windows Media recherche une sous-clé de Registre qui correspond à l’extension.</span><span class="sxs-lookup"><span data-stu-id="e0244-147">When the user attempts to play a media file that has a custom file name extension, Windows Media Player looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="e0244-148">Si aucune correspondance n’est trouvée, le lecteur présente à l’utilisateur une boîte de dialogue d’avertissement qui demande à l’utilisateur l’autorisation d’essayer de lire le fichier.</span><span class="sxs-lookup"><span data-stu-id="e0244-148">If no match is found, the Player presents the user with a warning dialog box that prompts the user for permission to attempt to play the file.</span></span> <span data-ttu-id="e0244-149">Si vous créez des fichiers multimédias numériques avec des extensions de nom de fichier personnalisées, vous pouvez empêcher l’affichage de cet avertissement sur l’ordinateur de l’utilisateur en inscrivant l’extension de nom de fichier et en fournissant une entrée d' **autorisation** .</span><span class="sxs-lookup"><span data-stu-id="e0244-149">If you create digital media files with custom file name extensions, you can prevent this warning from appearing on the user's computer by registering the file name extension and providing a **Permissions** entry.</span></span>

<span data-ttu-id="e0244-150">L’entrée d' **autorisation** (à l’exception de la valeur d’indicateur 128) est prise en charge par le lecteur Windows Media 9 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e0244-150">The **Permissions** entry (except for the flag value 128) is supported by Windows Media Player 9 Series and later.</span></span> <span data-ttu-id="e0244-151">La valeur d’indicateur 128 est prise en charge par le lecteur Windows Media 10 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e0244-151">The flag value 128 is supported by Windows Media Player 10 and later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0244-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e0244-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0244-153">**Paramètres de registre de l’extension de nom de fichier**</span><span class="sxs-lookup"><span data-stu-id="e0244-153">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




