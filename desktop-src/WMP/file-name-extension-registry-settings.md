---
title: Paramètres de registre de l’extension de nom de fichier
description: Paramètres de registre de l’extension de nom de fichier
ms.assetid: a5c31cf7-e1e1-4f1a-8e94-ed08f99ad973
keywords:
- Lecteur Windows Media, registre
- Windows Media Player, extensions de nom de fichier
- Registre, extensions de noms de fichiers
- Registre, paramètres pour le lecteur Windows Media
- paramètres de registre de l’extension de nom de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c526e38ae1b2b76b942e0646df6f8aaa3b8e3417
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674834"
---
# <a name="file-name-extension-registry-settings"></a><span data-ttu-id="eb6eb-108">Paramètres de registre de l’extension de nom de fichier</span><span class="sxs-lookup"><span data-stu-id="eb6eb-108">File Name Extension Registry Settings</span></span>

<span data-ttu-id="eb6eb-109">Si vos fichiers multimédias numériques ont un format personnalisé, vous pouvez fournir au lecteur Windows Media des informations sur votre format personnalisé en plaçant des entrées dans le registre sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="eb6eb-109">If your digital media files have a custom format, you can provide Windows Media Player with information about your custom format by placing entries in the registry on the user's computer.</span></span> <span data-ttu-id="eb6eb-110">Le lecteur Windows Media inspecte vos entrées de Registre pour déterminer comment il doit gérer vos fichiers.</span><span class="sxs-lookup"><span data-stu-id="eb6eb-110">Windows Media Player inspects your registry entries to determine how it should handle your files.</span></span> <span data-ttu-id="eb6eb-111">La liste suivante présente plusieurs des opérations que vous pouvez effectuer en créant des entrées de Registre relatives à votre format de fichier multimédia personnalisé.</span><span class="sxs-lookup"><span data-stu-id="eb6eb-111">The following list shows several of the things you can do by creating registry entries that pertain to your custom media file format.</span></span>

-   <span data-ttu-id="eb6eb-112">Accordez l’autorisation au lecteur de lire, copier ou transcoder vos fichiers.</span><span class="sxs-lookup"><span data-stu-id="eb6eb-112">Grant permission for the Player to play, copy, or transcode your files.</span></span>
-   <span data-ttu-id="eb6eb-113">Spécifiez la technologie sous-jacente que le lecteur doit utiliser pour lire vos fichiers.</span><span class="sxs-lookup"><span data-stu-id="eb6eb-113">Specify the underlying technology that the Player should use to play your files.</span></span>
-   <span data-ttu-id="eb6eb-114">Spécifiez l’emplacement où le joueur doit afficher vos fichiers dans sa vue bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="eb6eb-114">Specify where the Player should display your files in its library view.</span></span>
-   <span data-ttu-id="eb6eb-115">Spécifiez un plug-in que le lecteur doit utiliser pour convertir vos fichiers dans un format standard.</span><span class="sxs-lookup"><span data-stu-id="eb6eb-115">Specify a plug-in that the Player should use to convert your files to a standard format.</span></span>
-   <span data-ttu-id="eb6eb-116">Spécifiez un code de format MTP (Media Transport Protocol) que le joueur peut utiliser pour déterminer si un périphérique portable particulier prend en charge votre format de fichier.</span><span class="sxs-lookup"><span data-stu-id="eb6eb-116">Specify a Media Transport Protocol (MTP) format code that the Player can use to determine whether a particular portable device supports your file format.</span></span>

<span data-ttu-id="eb6eb-117">La plupart des entrées que vous fournissez se trouvent sous une sous-clé associée à votre extension de nom de fichier personnalisée.</span><span class="sxs-lookup"><span data-stu-id="eb6eb-117">Most of the entries that you provide will be under a subkey that is associated with your custom file name extension.</span></span> <span data-ttu-id="eb6eb-118">Vous pouvez créer cette sous-arborescence dans la sous-arborescence de l' \_ ordinateur local HKEY \_ et dans la sous-arborescence de l' \_ utilisateur actuel HKEY \_ .</span><span class="sxs-lookup"><span data-stu-id="eb6eb-118">You can create that subkey in the HKEY\_LOCAL\_MACHINE subtree and in the HKEY\_CURRENT\_USER subtree.</span></span> <span data-ttu-id="eb6eb-119">Le lecteur Windows Media recherche d’abord dans la sous-arborescence de la \_ machine locale HKEY \_ .</span><span class="sxs-lookup"><span data-stu-id="eb6eb-119">Windows Media Player looks first in the HKEY\_LOCAL\_MACHINE subtree.</span></span> <span data-ttu-id="eb6eb-120">S’il ne trouve pas ce dont il a besoin, il regarde dans la sous-arborescence de la sous-arborescence de l' \_ \_ utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="eb6eb-120">If it doesn't find what it needs there, it looks in the HKEY\_CURRENT\_USER subtree.</span></span> <span data-ttu-id="eb6eb-121">Notez que tout code qui tente d’écrire dans le registre sur l’ordinateur de l’utilisateur peut écrire dans la sous-arborescence de l' \_ ordinateur local HKEY \_ uniquement si l’utilisateur actuel dispose de privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="eb6eb-121">Note that any code that attempts to write to the registry on the user's computer can write to the HKEY\_LOCAL\_MACHINE subtree only if the current user has administrative privileges.</span></span>

<span data-ttu-id="eb6eb-122">Pour écrire des informations sur votre format de fichier personnalisé dans \_ la \_ sous-arborescence de l’ordinateur local HKEY, créez la sous-clé suivante.</span><span class="sxs-lookup"><span data-stu-id="eb6eb-122">To write information about your custom file format to the HKEY\_LOCAL\_MACHINE subtree, create the following subkey.</span></span>

<span data-ttu-id="eb6eb-123">**HKEY \_ Logiciel de l' \_ ordinateur local \\ \\ Microsoft \\ Multimedia \\ wmplayer \\ \\ Extensions** *customExtension*</span><span class="sxs-lookup"><span data-stu-id="eb6eb-123">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Multimedia\\WMPlayer\\Extensions\\** *customExtension*</span></span>

<span data-ttu-id="eb6eb-124">où *customExtension* est l’extension de nom de fichier, y compris le séparateur de points (.).</span><span class="sxs-lookup"><span data-stu-id="eb6eb-124">where *customExtension* is the file name extension including the dot (.) separator.</span></span> <span data-ttu-id="eb6eb-125">Par exemple, si l’extension de votre format de fichier personnalisé est. xyz, créez la sous-clé suivante.</span><span class="sxs-lookup"><span data-stu-id="eb6eb-125">For example, if the extension for your custom file format is .xyz, create the following subkey.</span></span>

<span data-ttu-id="eb6eb-126">**HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Multimedia \\ wmplayer \\ extensions \\ . xyz**</span><span class="sxs-lookup"><span data-stu-id="eb6eb-126">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Multimedia\\WMPlayer\\Extensions\\.xyz**</span></span>

<span data-ttu-id="eb6eb-127">Pour écrire des informations sur votre format de fichier personnalisé dans \_ la \_ sous-arborescence de l’utilisateur actuel HKEY, créez la sous-clé suivante.</span><span class="sxs-lookup"><span data-stu-id="eb6eb-127">To write information about your custom file format to the HKEY\_CURRENT\_USER subtree, create the following subkey.</span></span>

<span data-ttu-id="eb6eb-128">**HKEY \_ \_Logiciel utilisateur \\ actuel \\ \\ \\ \\ extensions \\ de lecteur Microsoft MediaPlayer** </span><span class="sxs-lookup"><span data-stu-id="eb6eb-128">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Player\\Extensions\\** *customExtension*</span></span>

<span data-ttu-id="eb6eb-129">Vous pouvez écrire une ou plusieurs des entrées suivantes dans votre sous-clé *customExtension* .</span><span class="sxs-lookup"><span data-stu-id="eb6eb-129">You can write one or more of the following entries in your *customExtension* subkey.</span></span>

-   <span data-ttu-id="eb6eb-130">**autorisations**</span><span class="sxs-lookup"><span data-stu-id="eb6eb-130">**Permissions**</span></span>
-   <span data-ttu-id="eb6eb-131">**Runtime**</span><span class="sxs-lookup"><span data-stu-id="eb6eb-131">**Runtime**</span></span>
-   <span data-ttu-id="eb6eb-132">**FormatCode**</span><span class="sxs-lookup"><span data-stu-id="eb6eb-132">**FormatCode**</span></span>

<span data-ttu-id="eb6eb-133">Pour spécifier des plug-ins de conversion pour votre format de fichier multimédia personnalisé, créez une sous-clé **ConvertPluginCLSID** dans votre sous-clé *customExtension* .</span><span class="sxs-lookup"><span data-stu-id="eb6eb-133">To specify conversion plug-ins for your custom media file format, create a **ConvertPluginCLSID** subkey in your *customExtension* subkey.</span></span>

<span data-ttu-id="eb6eb-134">Pour spécifier l’emplacement où le lecteur Windows Media doit afficher vos fichiers dans sa vue bibliothèque, écrivez une entrée qui représente votre format de fichier personnalisé dans la sous-clé suivante.</span><span class="sxs-lookup"><span data-stu-id="eb6eb-134">To specify where Windows Media Player should display your files in its library view, write an entry that represents your custom file format in the following subkey.</span></span>

<span data-ttu-id="eb6eb-135">**HKEY \_ local \_ machine \\ Software \\ Microsoft \\ MediaPlayer \\ MLS \\ Extensions**</span><span class="sxs-lookup"><span data-stu-id="eb6eb-135">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\MediaPlayer\\MLS\\Extensions**</span></span>

<span data-ttu-id="eb6eb-136">Les rubriques suivantes décrivent les sous-clés et les entrées de Registre qui fournissent au lecteur Windows Media des informations sur les formats de fichiers multimédias personnalisés.</span><span class="sxs-lookup"><span data-stu-id="eb6eb-136">The following topics describe the registry subkeys and entries that provide Windows Media Player with information about custom media file formats.</span></span>

-   [<span data-ttu-id="eb6eb-137">Entrée de registre des autorisations</span><span class="sxs-lookup"><span data-stu-id="eb6eb-137">Permissions Registry Entry</span></span>](permissions-registry-entry.md)
-   [<span data-ttu-id="eb6eb-138">Entrée du Registre du Runtime</span><span class="sxs-lookup"><span data-stu-id="eb6eb-138">Runtime Registry Entry</span></span>](runtime-registry-entry.md)
-   [<span data-ttu-id="eb6eb-139">Entrée de Registre FormatCode</span><span class="sxs-lookup"><span data-stu-id="eb6eb-139">FormatCode Registry Entry</span></span>](formatcode-registry-entry.md)
-   [<span data-ttu-id="eb6eb-140">Entrées de registre de classification de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="eb6eb-140">Library Classification Registry Entries</span></span>](library-classification-registry-entries.md)
-   [<span data-ttu-id="eb6eb-141">Sous-clé ConvertPluginCLSID</span><span class="sxs-lookup"><span data-stu-id="eb6eb-141">ConvertPluginCLSID Subkey</span></span>](convertpluginclsid-subkey.md)

## <a name="related-topics"></a><span data-ttu-id="eb6eb-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eb6eb-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb6eb-143">**Paramètres du Registre**</span><span class="sxs-lookup"><span data-stu-id="eb6eb-143">**Registry Settings**</span></span>](registry-settings.md)
</dt> <dt>

[<span data-ttu-id="eb6eb-144">**Plug-ins de conversion du lecteur Windows Media**</span><span class="sxs-lookup"><span data-stu-id="eb6eb-144">**Windows Media Player Conversion Plug-ins**</span></span>](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




