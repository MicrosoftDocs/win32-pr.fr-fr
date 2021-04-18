---
title: Entrées de registre de classification de bibliothèque
description: Entrées de registre de classification de bibliothèque
ms.assetid: 3ef7d384-503f-4b8f-9f4b-e0ef3c56616b
keywords:
- Lecteur Windows Media, bibliothèque
- Lecteur Windows Media, entrées de registre de classification
- Windows Media Player, extensions de nom de fichier
- Lecteur Windows Media, registre
- Registre, extensions de noms de fichiers
- Registre, entrées de classification de bibliothèque
- Registre, paramètres pour le lecteur Windows Media
- paramètres de registre de l’extension de nom de fichier
- bibliothèque, entrées de registre de classification
- bibliothèque, registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e48ea1aacdd1e4c553a7e83bfdd711ff331c0878
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512457"
---
# <a name="library-classification-registry-entries"></a><span data-ttu-id="b73d8-113">Entrées de registre de classification de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b73d8-113">Library Classification Registry Entries</span></span>

<span data-ttu-id="b73d8-114">Lorsque le lecteur Windows Media rencontre un fichier multimédia qui a une extension de nom de fichier personnalisée, il ne sait pas si le fichier doit être classé comme audio, vidéo ou tout autre type.</span><span class="sxs-lookup"><span data-stu-id="b73d8-114">When Windows Media Player encounters a media file that has a custom file name extension, it does not know whether the file should be classified as audio, video, or some other type.</span></span> <span data-ttu-id="b73d8-115">Par défaut, le lecteur Windows Media place ces fichiers dans l’autre partie média de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="b73d8-115">By default, Windows Media Player places such files in the Other Media portion of the library.</span></span>

<span data-ttu-id="b73d8-116">Si vos fichiers multimédias numériques ont un format personnalisé, vous pouvez fournir au lecteur Windows Media des informations sur l’emplacement où vos fichiers doivent apparaître dans la bibliothèque du lecteur en plaçant deux entrées dans le registre sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b73d8-116">If your digital media files have a custom format, you can provide Windows Media Player with information about where your files should appear in the Player's library by placing two entries in the registry on the user's computer.</span></span>

<span data-ttu-id="b73d8-117">Une entrée est insérée dans la sous-clé suivante.</span><span class="sxs-lookup"><span data-stu-id="b73d8-117">One entry goes in the following subkey.</span></span>

<span data-ttu-id="b73d8-118">**HKEY \_ local \_ machine \\ Software \\ Microsoft \\ MediaPlayer \\ MLS \\ Extensions**</span><span class="sxs-lookup"><span data-stu-id="b73d8-118">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\MediaPlayer\\MLS\\Extensions**</span></span>

<span data-ttu-id="b73d8-119">L’entrée de registre a le format suivant.</span><span class="sxs-lookup"><span data-stu-id="b73d8-119">The registry entry has the following format.</span></span>



| <span data-ttu-id="b73d8-120">Nom</span><span class="sxs-lookup"><span data-stu-id="b73d8-120">Name</span></span>                                                  | <span data-ttu-id="b73d8-121">Type de données</span><span class="sxs-lookup"><span data-stu-id="b73d8-121">Data type</span></span>   | <span data-ttu-id="b73d8-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="b73d8-122">Value</span></span>                                      |
|-------------------------------------------------------|-------------|--------------------------------------------|
| <span data-ttu-id="b73d8-123">L’extension de nom de fichier sans séparateur de points (.)</span><span class="sxs-lookup"><span data-stu-id="b73d8-123">The file name extension without the dot (.) separator</span></span> | <span data-ttu-id="b73d8-124">**SZ de REG \_**</span><span class="sxs-lookup"><span data-stu-id="b73d8-124">**REG\_SZ**</span></span> | <span data-ttu-id="b73d8-125">Chaîne qui spécifie un emplacement de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b73d8-125">A string that specifies a library location</span></span> |



 

<span data-ttu-id="b73d8-126">L’autre entrée de Registre est insérée dans la sous-clé suivante que vous créez.</span><span class="sxs-lookup"><span data-stu-id="b73d8-126">The other registry entry goes in the following subkey that you create.</span></span>

<span data-ttu-id="b73d8-127">**HKEY \_ CLASSES \_ racine \\** *customExtension*</span><span class="sxs-lookup"><span data-stu-id="b73d8-127">**HKEY\_CLASSES\_ROOT\\** *customExtension*</span></span>

<span data-ttu-id="b73d8-128">où *customExtension* est l’extension de nom de fichier, y compris le séparateur de points (.).</span><span class="sxs-lookup"><span data-stu-id="b73d8-128">where *customExtension* is the file name extension including the dot (.) separator.</span></span>

<span data-ttu-id="b73d8-129">L’entrée de registre a le format suivant.</span><span class="sxs-lookup"><span data-stu-id="b73d8-129">The registry entry has the following format.</span></span>



| <span data-ttu-id="b73d8-130">Nom</span><span class="sxs-lookup"><span data-stu-id="b73d8-130">Name</span></span>          | <span data-ttu-id="b73d8-131">Type de données</span><span class="sxs-lookup"><span data-stu-id="b73d8-131">Data type</span></span>   | <span data-ttu-id="b73d8-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="b73d8-132">Value</span></span>                                      |
|---------------|-------------|--------------------------------------------|
| <span data-ttu-id="b73d8-133">PerceivedType</span><span class="sxs-lookup"><span data-stu-id="b73d8-133">PerceivedType</span></span> | <span data-ttu-id="b73d8-134">**SZ de REG \_**</span><span class="sxs-lookup"><span data-stu-id="b73d8-134">**REG\_SZ**</span></span> | <span data-ttu-id="b73d8-135">Chaîne qui spécifie un emplacement de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b73d8-135">A string that specifies a library location</span></span> |



 

<span data-ttu-id="b73d8-136">Les deux entrées de Registre doivent avoir la même valeur.</span><span class="sxs-lookup"><span data-stu-id="b73d8-136">Both registry entries must have the same value.</span></span> <span data-ttu-id="b73d8-137">Les valeurs possibles sont indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b73d8-137">Possible values are given in the following table.</span></span>



| <span data-ttu-id="b73d8-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="b73d8-138">Value</span></span> | <span data-ttu-id="b73d8-139">Description</span><span class="sxs-lookup"><span data-stu-id="b73d8-139">Description</span></span>                                                                      |
|-------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b73d8-140">audio</span><span class="sxs-lookup"><span data-stu-id="b73d8-140">audio</span></span> | <span data-ttu-id="b73d8-141">Les fichiers qui ont l’extension personnalisée s’affichent dans la partie musique de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="b73d8-141">Files that have the custom extension appear in the music portion of the library.</span></span> |
| <span data-ttu-id="b73d8-142">video</span><span class="sxs-lookup"><span data-stu-id="b73d8-142">video</span></span> | <span data-ttu-id="b73d8-143">Les fichiers qui ont l’extension personnalisée s’affichent dans la partie vidéo de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="b73d8-143">Files that have the custom extension appear in the video portion of the library.</span></span> |



 

<span data-ttu-id="b73d8-144">Par exemple, les entrées de Registre suivantes spécifient que les fichiers portant l’extension de nom de fichier. xyz s’afficheront dans la partie musique de la bibliothèque :</span><span class="sxs-lookup"><span data-stu-id="b73d8-144">For example, the following registry entries specify that files having the file name extension .xyz will appear in the music portion of the library:</span></span>


```C++

HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\MLS\Extensions
    xyz     REG_SZ     audio

HKEY_CLASSES_ROOT\.xyz
    PerceivedType     REG_SZ     audio

```



<span data-ttu-id="b73d8-145">Notez que tout code qui tente d’écrire dans le registre sur l’ordinateur de l’utilisateur peut écrire dans la sous-arborescence de l' \_ ordinateur local HKEY \_ uniquement si l’utilisateur actuel dispose de privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="b73d8-145">Note that any code that attempts to write to the registry on the user's computer can write to the HKEY\_LOCAL\_MACHINE subtree only if the current user has administrative privileges.</span></span>

<span data-ttu-id="b73d8-146">Les entrées de registre de classification de bibliothèque sont prises en charge par les versions suivantes du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b73d8-146">Library classification registry entries are supported by the following versions of Windows Media Player.</span></span>

-   <span data-ttu-id="b73d8-147">Lecteur Windows Media série 9 avec le correctif 823275</span><span class="sxs-lookup"><span data-stu-id="b73d8-147">Windows Media Player 9 Series with hotfix 823275</span></span>
-   <span data-ttu-id="b73d8-148">Lecteur Windows Media 10 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="b73d8-148">Windows Media Player 10 and later</span></span>

## <a name="related-topics"></a><span data-ttu-id="b73d8-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b73d8-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b73d8-150">**Paramètres de registre de l’extension de nom de fichier**</span><span class="sxs-lookup"><span data-stu-id="b73d8-150">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




