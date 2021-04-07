---
title: Paramètres de Registre du schéma personnalisé
description: Paramètres de Registre du schéma personnalisé
ms.assetid: ded2b492-7755-4ba5-87cf-720a79ec79de
keywords:
- Lecteur Windows Media, paramètres de Registre du schéma personnalisé
- Windows Media Player, schémas
- Lecteur Windows Media, registre
- Registre, paramètres de schéma personnalisés
- Registre, schémas
- Registre, paramètres pour le lecteur Windows Media
- schémas
- paramètres de Registre du schéma personnalisé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a02649d9536140fff0ff0d3188a5b25feb49688
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028800"
---
# <a name="custom-scheme-registry-settings"></a><span data-ttu-id="5b56b-111">Paramètres de Registre du schéma personnalisé</span><span class="sxs-lookup"><span data-stu-id="5b56b-111">Custom Scheme Registry Settings</span></span>

<span data-ttu-id="5b56b-112">Les schémas sont des protocoles personnalisés.</span><span class="sxs-lookup"><span data-stu-id="5b56b-112">Schemes are custom protocols.</span></span> <span data-ttu-id="5b56b-113">Le lecteur Windows Media gère une liste de schémas dans le registre sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5b56b-113">Windows Media Player maintains a list of schemes in the registry on the user's computer.</span></span> <span data-ttu-id="5b56b-114">Lorsque l’utilisateur tente de lire un fichier multimédia numérique, le lecteur vérifie d’abord si le kit de développement logiciel (SDK) du format Windows Media prend en charge le schéma.</span><span class="sxs-lookup"><span data-stu-id="5b56b-114">When the user attempts to play a digital media file, the Player first checks whether the Windows Media Format SDK supports the scheme.</span></span> <span data-ttu-id="5b56b-115">Si ce n’est pas le cas, le lecteur vérifie le schéma par rapport à la liste figurant dans le registre.</span><span class="sxs-lookup"><span data-stu-id="5b56b-115">If it doesn't, the Player checks the scheme against the list in the registry.</span></span> <span data-ttu-id="5b56b-116">Si une correspondance est trouvée, le lecteur vérifie ensuite une valeur qui indique la technologie sous-jacente, ou le *Runtime* (par exemple, Microsoft DirectShow ou le kit de développement logiciel (SDK) Windows Media Format), peut être utilisé pour lire le fichier.</span><span class="sxs-lookup"><span data-stu-id="5b56b-116">If a match is found, the Player then checks a value that indicates which underlying technology, or *runtime* (such as Microsoft DirectShow or the Windows Media Format SDK), can be used to play the file.</span></span> <span data-ttu-id="5b56b-117">Si aucune correspondance n’est trouvée, le lecteur présente à l’utilisateur une boîte de dialogue d’avertissement qui demande à l’utilisateur l’autorisation d’essayer de lire le fichier.</span><span class="sxs-lookup"><span data-stu-id="5b56b-117">If no match is found, the Player presents the user with a warning dialog box that prompts the user for permission to attempt to play the file.</span></span> <span data-ttu-id="5b56b-118">Si vous diffusez en continu des fichiers multimédias numériques à l’aide d’un schéma de protocole personnalisé, vous pouvez empêcher l’affichage de cet avertissement sur l’ordinateur de l’utilisateur en inscrivant le schéma et en fournissant une valeur pour le Runtime.</span><span class="sxs-lookup"><span data-stu-id="5b56b-118">If you stream digital media files using a custom protocol scheme, you can prevent this warning from appearing on the user's computer by registering the scheme and providing a value for the runtime.</span></span>

<span data-ttu-id="5b56b-119">La liste des schémas est conservée sous la forme d’un ensemble de clés de Registre qui correspondent aux schémas inscrits, sans le signe deux-points et les deux barres obliques (://).</span><span class="sxs-lookup"><span data-stu-id="5b56b-119">The list of schemes is maintained as a set of registry keys that match the registered schemes, without the colon and the two slashes (://).</span></span> <span data-ttu-id="5b56b-120">Par exemple, la clé pour le schéma wmhtml://, qui est utilisé pour diffuser des médias enrichis, est nommée « wmhtml ».</span><span class="sxs-lookup"><span data-stu-id="5b56b-120">For example, the key for the wmhtml:// scheme, which is used to stream rich media, is named "wmhtml".</span></span> <span data-ttu-id="5b56b-121">Une liste distincte est conservée pour l’ordinateur local et pour chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5b56b-121">A separate list is maintained for the local machine and for each user.</span></span> <span data-ttu-id="5b56b-122">Pour l’ordinateur local, les clés de schéma sont des sous-clés de la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="5b56b-122">For the local machine, the scheme keys are subkeys of the following registry key:</span></span>

<span data-ttu-id="5b56b-123">**HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Multimedia pour les \\ \\ modèles wmplayer\\**</span><span class="sxs-lookup"><span data-stu-id="5b56b-123">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Multimedia\\WMPlayer\\Schemes\\**</span></span>

<span data-ttu-id="5b56b-124">Par exemple, la clé du schéma wmhtml://pour l’ordinateur local est la suivante :</span><span class="sxs-lookup"><span data-stu-id="5b56b-124">For example, the key for the wmhtml:// scheme for the local machine is:</span></span>

<span data-ttu-id="5b56b-125">**HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Multimedia \\ \\ wmhtml schemas \\**</span><span class="sxs-lookup"><span data-stu-id="5b56b-125">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Multimedia\\WMPlayer\\Schemes\\wmhtml**</span></span>

<span data-ttu-id="5b56b-126">Pour modifier les valeurs de cette clé ou pour créer une nouvelle sous-clé, l’utilisateur actuel doit être administrateur de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="5b56b-126">To change values in this key or to create a new subkey, the current user must be an administrator for the computer.</span></span>

<span data-ttu-id="5b56b-127">Pour les utilisateurs individuels, les clés de schéma sont des sous-clés de la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="5b56b-127">For individual users, the scheme keys are subkeys of the following registry key:</span></span>

<span data-ttu-id="5b56b-128">**HKEY \_ Current \_ User \\ Software \\ Microsoft \\ MediaPlayer \\ Player \\ schemas\\**</span><span class="sxs-lookup"><span data-stu-id="5b56b-128">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Player\\Schemes\\**</span></span>

<span data-ttu-id="5b56b-129">Par exemple, la clé du schéma wmhtml://pour l’utilisateur actuel est :</span><span class="sxs-lookup"><span data-stu-id="5b56b-129">For example, the key for the wmhtml:// scheme for the current user is:</span></span>

<span data-ttu-id="5b56b-130">**HKEY \_ Current \_ User \\ Software \\ Microsoft \\ MediaPlayer \\ Player \\ schemas \\ wmhtml**</span><span class="sxs-lookup"><span data-stu-id="5b56b-130">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Player\\Schemes\\wmhtml**</span></span>

<span data-ttu-id="5b56b-131">Lors de la vérification des schémas inscrits, le lecteur vérifie d’abord les valeurs situées dans **HKEY \_ local \_ machine**.</span><span class="sxs-lookup"><span data-stu-id="5b56b-131">When checking for registered schemes, the Player first checks the values located in **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="5b56b-132">Si aucune valeur n’est trouvée pour le schéma actuel, le lecteur vérifie ensuite les valeurs dans **HKEY \_ Current \_ User**.</span><span class="sxs-lookup"><span data-stu-id="5b56b-132">If none are found for the current scheme, the Player next checks the values in **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="5b56b-133">Si aucune valeur n’est trouvée pour le schéma actuel, le lecteur affiche l’avertissement à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5b56b-133">If none are found for the current scheme, the Player displays the warning to the user.</span></span>

<span data-ttu-id="5b56b-134">Chaque sous-clé de schéma peut contenir l’une des valeurs possibles suivantes pour l' *exécution*.</span><span class="sxs-lookup"><span data-stu-id="5b56b-134">Each scheme subkey may contain one of the following possible values for *Runtime*.</span></span>



| <span data-ttu-id="5b56b-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b56b-135">Value</span></span> | <span data-ttu-id="5b56b-136">Description</span><span class="sxs-lookup"><span data-stu-id="5b56b-136">Description</span></span>                                |
|-------|--------------------------------------------|
| <span data-ttu-id="5b56b-137">6</span><span class="sxs-lookup"><span data-stu-id="5b56b-137">6</span></span>     | <span data-ttu-id="5b56b-138">Rendu à l’aide du kit de développement logiciel (SDK) Windows Media format.</span><span class="sxs-lookup"><span data-stu-id="5b56b-138">Render using the Windows Media Format SDK.</span></span> |
| <span data-ttu-id="5b56b-139">7</span><span class="sxs-lookup"><span data-stu-id="5b56b-139">7</span></span>     | <span data-ttu-id="5b56b-140">Rendu à l’aide de Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="5b56b-140">Render using Microsoft DirectShow.</span></span>         |



 

<span data-ttu-id="5b56b-141">La modification de la valeur d' *exécution* d’un schéma pris en charge par le kit de développement logiciel (SDK) du format Windows Media n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="5b56b-141">Changing the *Runtime* value for a scheme that the Windows Media Format SDK supports will have no effect.</span></span> <span data-ttu-id="5b56b-142">Le lecteur utilisera toujours le kit de développement logiciel (SDK) de format Windows Media comme Runtime pour les schémas pris en charge par le kit de développement logiciel (SDK) Windows Media format.</span><span class="sxs-lookup"><span data-stu-id="5b56b-142">The Player will always use the Windows Media Format SDK as the runtime for schemes that the Windows Media Format SDK supports.</span></span> <span data-ttu-id="5b56b-143">Cette valeur de Registre est conçue pour permettre la configuration du runtime pour les schémas personnalisés.</span><span class="sxs-lookup"><span data-stu-id="5b56b-143">This registry value is designed to allow runtime configuration for custom schemes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5b56b-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5b56b-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b56b-145">**Paramètres du Registre**</span><span class="sxs-lookup"><span data-stu-id="5b56b-145">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




