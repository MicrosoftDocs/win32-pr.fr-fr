---
title: Sous-clé ConvertPluginCLSID
description: Sous-clé ConvertPluginCLSID
ms.assetid: 2bf5b6ad-31e9-40c2-a682-c7ad813e8f7a
keywords:
- Lecteur Windows Media, sous-clé ConvertPluginCLSID
- Windows Media Player, extensions de nom de fichier
- Lecteur Windows Media, registre
- Registre, extensions de noms de fichiers
- Registre, sous-clé ConvertPluginCLSID
- Registre, paramètres pour le lecteur Windows Media
- paramètres de registre de l’extension de nom de fichier
- Sous-clé ConvertPluginCLSID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4229617c3999708d89fac976e94b2747b5a69145
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029303"
---
# <a name="convertpluginclsid-subkey"></a><span data-ttu-id="edeee-111">Sous-clé ConvertPluginCLSID</span><span class="sxs-lookup"><span data-stu-id="edeee-111">ConvertPluginCLSID Subkey</span></span>

<span data-ttu-id="edeee-112">Lorsque le lecteur Windows Media 11 rencontre une extension de nom de fichier personnalisée, il recherche une sous-clé de Registre qui correspond à l’extension.</span><span class="sxs-lookup"><span data-stu-id="edeee-112">When Windows Media Player 11 encounters a custom file name extension, it looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="edeee-113">La sous-clé est décrite dans les paramètres de registre de l' [extension de nom de fichier](file-name-extension-registry-settings.md).</span><span class="sxs-lookup"><span data-stu-id="edeee-113">The subkey is described in [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="edeee-114">Dans certains cas, la sous-clé de l’extension a une sous-clé nommée **ConvertPluginCLSID**.</span><span class="sxs-lookup"><span data-stu-id="edeee-114">In some cases, the extension's subkey has a subkey named **ConvertPluginCLSID**.</span></span>

<span data-ttu-id="edeee-115">Par exemple, supposons que vous avez créé un format de fichier personnalisé (avec l’extension de nom de fichier. xyz) et un plug-in de conversion qui convertit les fichiers dans un format pris en charge par le lecteur Windows Media, puis vous stockiez l’ID de classe du plug-in dans l’une ou les deux sous-clés suivantes.</span><span class="sxs-lookup"><span data-stu-id="edeee-115">For example, suppose you have created a custom file format (with file name extension .xyz) and a conversion plug-in that converts the files to a format supported by Windows Media Player Then you would store the class ID of the plug-in in one or both of the following subkeys.</span></span>

<span data-ttu-id="edeee-116">**HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Multimedia \\ wmplayer \\ extensions \\ . xyz \\ ConvertPluginCLSID**</span><span class="sxs-lookup"><span data-stu-id="edeee-116">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Multimedia\\WMPlayer\\Extensions\\.xyz\\ConvertPluginCLSID**</span></span>

<span data-ttu-id="edeee-117">**HKEY \_ Current \_ User \\ Software \\ \\ extensions Microsoft \\ MediaPlayer \\ Player \\ . xyz \\ ConvertPluginCLSID**</span><span class="sxs-lookup"><span data-stu-id="edeee-117">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Player\\Extensions\\.xyz\\ConvertPluginCLSID**</span></span>

<span data-ttu-id="edeee-118">La sous-clé **ConvertPluginCLSID** spécifie les ID de classe des plug-ins que le lecteur Windows Media peut utiliser pour convertir un fichier multimédia à partir de son format personnalisé vers un format pris en charge par le lecteur.</span><span class="sxs-lookup"><span data-stu-id="edeee-118">The **ConvertPluginCLSID** subkey specifies the class IDs of plug-ins that Windows Media Player can use to convert a media file from its custom format to a format supported by the Player.</span></span>

<span data-ttu-id="edeee-119">La sous-clé **ConvertPluginCLSID** contient les entrées suivantes.</span><span class="sxs-lookup"><span data-stu-id="edeee-119">The **ConvertPluginCLSID** subkey has the following entries.</span></span>

-   <span data-ttu-id="edeee-120">Entrée par défaut qui représente le plug-in de conversion par défaut.</span><span class="sxs-lookup"><span data-stu-id="edeee-120">A default entry that represents the default conversion plug-in.</span></span>
-   <span data-ttu-id="edeee-121">Entrée nommée qui représente le plug-in de conversion par défaut.</span><span class="sxs-lookup"><span data-stu-id="edeee-121">A named entry that represents the default conversion plug-in.</span></span>
-   <span data-ttu-id="edeee-122">Entrées nommées supplémentaires qui représentent d’autres plug-ins de conversion.</span><span class="sxs-lookup"><span data-stu-id="edeee-122">Additional named entries that represent alternate conversion plug-ins.</span></span>

<span data-ttu-id="edeee-123">Par exemple, supposons qu’un format de fichier personnalisé possède un plug-in de conversion par défaut et deux autres plug-ins de conversion. Les entrées de Registre sous la sous-clé **ConvertPluginCLSID** se présentent sous la forme suivante.</span><span class="sxs-lookup"><span data-stu-id="edeee-123">For example, suppose a custom file format has a default conversion plug-in and two alternate conversion plug-ins. The registry entries under the **ConvertPluginCLSID** subkey would have the following form.</span></span>



| <span data-ttu-id="edeee-124">Nom</span><span class="sxs-lookup"><span data-stu-id="edeee-124">Name</span></span>                                                                          | <span data-ttu-id="edeee-125">Type</span><span class="sxs-lookup"><span data-stu-id="edeee-125">Type</span></span>        | <span data-ttu-id="edeee-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="edeee-126">Value</span></span>                                                                |
|-------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------|
| <span data-ttu-id="edeee-127">Default</span><span class="sxs-lookup"><span data-stu-id="edeee-127">Default</span></span>                                                                       | <span data-ttu-id="edeee-128">**SZ de REG \_**</span><span class="sxs-lookup"><span data-stu-id="edeee-128">**REG\_SZ**</span></span> | <span data-ttu-id="edeee-129">ID de classe, au format de Registre, du plug-in de conversion par défaut.</span><span class="sxs-lookup"><span data-stu-id="edeee-129">The class ID, in registry format, of the default conversion plug-in.</span></span> |
| <span data-ttu-id="edeee-130">ID de classe, au format de Registre, du plug-in de conversion par défaut.</span><span class="sxs-lookup"><span data-stu-id="edeee-130">The class ID, in registry format, of the default conversion plug-in.</span></span>          | <span data-ttu-id="edeee-131">**SZ de REG \_**</span><span class="sxs-lookup"><span data-stu-id="edeee-131">**REG\_SZ**</span></span> | <span data-ttu-id="edeee-132">Nom convivial du plug-in de conversion par défaut.</span><span class="sxs-lookup"><span data-stu-id="edeee-132">The friendly name of the default conversion plug-in.</span></span>                 |
| <span data-ttu-id="edeee-133">ID de classe, au format de Registre, du premier plug-in de conversion.</span><span class="sxs-lookup"><span data-stu-id="edeee-133">The class ID, in registry format, of the first alternate conversion plug-in.</span></span>  | <span data-ttu-id="edeee-134">**SZ de REG \_**</span><span class="sxs-lookup"><span data-stu-id="edeee-134">**REG\_SZ**</span></span> | <span data-ttu-id="edeee-135">Nom convivial du premier plug-in de conversion.</span><span class="sxs-lookup"><span data-stu-id="edeee-135">The friendly name of the first alternate conversion plug-in.</span></span>         |
| <span data-ttu-id="edeee-136">ID de classe, au format de Registre, du deuxième plug-in de conversion.</span><span class="sxs-lookup"><span data-stu-id="edeee-136">The class ID, in registry format, of the second alternate conversion plug-in.</span></span> | <span data-ttu-id="edeee-137">**SZ de REG \_**</span><span class="sxs-lookup"><span data-stu-id="edeee-137">**REG\_SZ**</span></span> | <span data-ttu-id="edeee-138">Nom convivial du deuxième plug-in de conversion.</span><span class="sxs-lookup"><span data-stu-id="edeee-138">The friendly name of the second alternate conversion plug-in.</span></span>        |



 

<span data-ttu-id="edeee-139">Notez que le plug-in de conversion par défaut est représenté par deux entrées de Registre : l’entrée par défaut et une entrée nommée.</span><span class="sxs-lookup"><span data-stu-id="edeee-139">Note that the default conversion plug-in is represented by two registry entries: the default entry and a named entry.</span></span> <span data-ttu-id="edeee-140">Le lecteur Windows Media utilise l’entrée par défaut pour déterminer quel plug-in est le plug-in de conversion par défaut (principal).</span><span class="sxs-lookup"><span data-stu-id="edeee-140">Windows Media Player uses the default entry to determine which plug-in is the default (primary) conversion plug-in.</span></span> <span data-ttu-id="edeee-141">Le lecteur Windows Media utilise les entrées nommées pour obtenir des noms conviviaux pour tous les plug-ins de conversion, y compris le plug-in par défaut.</span><span class="sxs-lookup"><span data-stu-id="edeee-141">Windows Media Player uses the named entries to obtain friendly names for all conversion plug-ins, including the default plug-in.</span></span>

<span data-ttu-id="edeee-142">Le nom convivial d’un plug-in de conversion est déterminé par la société qui crée le plug-in.</span><span class="sxs-lookup"><span data-stu-id="edeee-142">The friendly name of a conversion plug-in is determined by the company that creates the plug-in.</span></span> <span data-ttu-id="edeee-143">Le lecteur Windows Media peut afficher le nom convivial dans son interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="edeee-143">Windows Media Player might display the friendly name in its user interface.</span></span>

<span data-ttu-id="edeee-144">Lorsque le lecteur Windows Media tente de convertir un fichier d’un format personnalisé vers un format standard, il commence par charger le plug-in par défaut.</span><span class="sxs-lookup"><span data-stu-id="edeee-144">When Windows Media Player attempts to convert a file from a custom format to a standard format, it first loads the default plug-in.</span></span> <span data-ttu-id="edeee-145">Si le plug-in par défaut ne parvient pas à convertir le fichier et retourne le plug-in de conversion du plug-in NS \_ E \_ WMP \_ \_ \_ \_ \_ , le lecteur charge chaque plug-in jusqu’à ce qu’une conversion réussisse ou qu’il n’y ait plus de plug-ins à essayer.</span><span class="sxs-lookup"><span data-stu-id="edeee-145">If the default plug-in fails to convert the file and returns NS\_E\_WMP\_CONVERT\_PLUGIN\_UNKNOWN\_FILE\_OWNER, the Player loads each alternate plug-in until a successful conversion happens or there are no more plug-ins to try.</span></span> <span data-ttu-id="edeee-146">Le lecteur n’affiche pas de message d’avertissement si aucun plug-in de conversion n’est trouvé pour l’extension de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="edeee-146">The Player does not display a warning message if no conversion plug-in is found for the file name extension.</span></span>

<span data-ttu-id="edeee-147">L’entrée de Registre **ConvertPluginCLSID** est prise en charge par le lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="edeee-147">The **ConvertPluginCLSID** registry entry is supported by Windows Media Player 11.</span></span>

## <a name="related-topics"></a><span data-ttu-id="edeee-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="edeee-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edeee-149">**Paramètres de registre de l’extension de nom de fichier**</span><span class="sxs-lookup"><span data-stu-id="edeee-149">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> <dt>

[<span data-ttu-id="edeee-150">**Plug-ins de conversion du lecteur Windows Media**</span><span class="sxs-lookup"><span data-stu-id="edeee-150">**Windows Media Player Conversion Plug-ins**</span></span>](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




