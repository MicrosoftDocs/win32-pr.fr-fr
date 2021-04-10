---
title: Utilisation de commandes de script prises en charge par le lecteur Windows Media
description: Utilisation de commandes de script prises en charge par le lecteur Windows Media
ms.assetid: 7054ce49-c000-4978-891e-825a83bfda5c
keywords:
- Windows Media Format SDK, commandes de script
- Windows Media Format SDK, Windows Media Player
- ASF (Advanced Systems Format), commandes de script
- ASF (format des systèmes avancés), commandes de script
- ASF (Advanced Systems Format), Windows Media Player
- ASF (format avancé des systèmes), Windows Media Player
- scripts, commandes
- scripts, Windows Media Player
- Lecteur Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25302b5f5b6789be0d9e18b0a93e1e781a9dc06b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029294"
---
# <a name="using-script-commands-supported-by-windows-media-player"></a><span data-ttu-id="b66d7-112">Utilisation de commandes de script prises en charge par le lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="b66d7-112">Using Script Commands Supported by Windows Media Player</span></span>

<span data-ttu-id="b66d7-113">Le kit de développement logiciel (SDK) Windows Media format ne fournit pas de prise en charge native pour l’analyse et la réponse aux commandes de script.</span><span class="sxs-lookup"><span data-stu-id="b66d7-113">The Windows Media Format SDK does not provide native support for parsing and responding to script commands.</span></span> <span data-ttu-id="b66d7-114">Vous devez inclure toute logique relative aux commandes de script dans votre application.</span><span class="sxs-lookup"><span data-stu-id="b66d7-114">You must include any logic related to script commands in your application.</span></span> <span data-ttu-id="b66d7-115">Les types de script que vous utilisez doivent également être définis dans votre application.</span><span class="sxs-lookup"><span data-stu-id="b66d7-115">The script types that you use must also be defined in your application.</span></span>

<span data-ttu-id="b66d7-116">Vous pouvez inclure du code pour gérer les mêmes commandes de script que celles prises en charge par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b66d7-116">You can include code to handle the same script commands that are supported by Windows Media Player.</span></span> <span data-ttu-id="b66d7-117">La gestion de la compatibilité avec le lecteur Windows Media rend vos fichiers plus universels que si vous incorporez des commandes de script personnalisées.</span><span class="sxs-lookup"><span data-stu-id="b66d7-117">Maintaining compatibility with Windows Media Player makes your files more universal than if you embed custom script commands.</span></span>

<span data-ttu-id="b66d7-118">Le tableau suivant répertorie les types de scripts pris en charge par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b66d7-118">The following table lists script types that are supported by Windows Media Player.</span></span>



| <span data-ttu-id="b66d7-119">Type de script</span><span class="sxs-lookup"><span data-stu-id="b66d7-119">Script type</span></span> | <span data-ttu-id="b66d7-120">Description</span><span class="sxs-lookup"><span data-stu-id="b66d7-120">Description</span></span>                                                                                                                                                                                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b66d7-121">URL</span><span class="sxs-lookup"><span data-stu-id="b66d7-121">URL</span></span>         | <span data-ttu-id="b66d7-122">Le lecteur envoie l’URL spécifiée au navigateur pour qu’il s’affiche à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b66d7-122">The player sends the specified URL to the browser for display to the user.</span></span> <span data-ttu-id="b66d7-123">Si un contrôle de lecteur incorporé est utilisé, vous pouvez ajouter une référence de frame spécifique à l’URL à l’aide de la syntaxe &&*frameName* .</span><span class="sxs-lookup"><span data-stu-id="b66d7-123">If an embedded player control is being used, you can add a specific frame reference to the URL by using the &&*framename* syntax.</span></span>                                                                             |
| <span data-ttu-id="b66d7-124">EXTENSION</span><span class="sxs-lookup"><span data-stu-id="b66d7-124">FILENAME</span></span>    | <span data-ttu-id="b66d7-125">URL vers un autre fichier multimédia à lire.</span><span class="sxs-lookup"><span data-stu-id="b66d7-125">A URL to another media file to be played.</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="b66d7-126">CAPTION</span><span class="sxs-lookup"><span data-stu-id="b66d7-126">CAPTION</span></span>     | <span data-ttu-id="b66d7-127">Chaîne de texte qui est affichée dans la zone légendes du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b66d7-127">A text string that is displayed in the captions area of Windows Media Player.</span></span> <span data-ttu-id="b66d7-128">Ce type prend en charge la mise en forme HTML standard. le texte peut donc être mis en forme comme vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="b66d7-128">This type supports standard HTML formatting, so the text can be formatted as you wish.</span></span> <span data-ttu-id="b66d7-129">Le sous-titrage est un exemple d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="b66d7-129">An example of use is closed captioning.</span></span>                                                                             |
| <span data-ttu-id="b66d7-130">ÉVÉNEMENT</span><span class="sxs-lookup"><span data-stu-id="b66d7-130">EVENT</span></span>       | <span data-ttu-id="b66d7-131">Nom d’un événement qui doit se produire.</span><span class="sxs-lookup"><span data-stu-id="b66d7-131">The name of an event that is to occur.</span></span> <span data-ttu-id="b66d7-132">Le type d’événement prend en charge la personnalisation pour vos propres utilisations.</span><span class="sxs-lookup"><span data-stu-id="b66d7-132">The EVENT type supports customization for your own uses.</span></span> <span data-ttu-id="b66d7-133">Le code de l’événement spécifié doit être défini dans le métafichier Windows Media pour le flux afin que le lecteur puisse exécuter l’événement spécifié.</span><span class="sxs-lookup"><span data-stu-id="b66d7-133">The code for the specified event must be defined in the Windows Media metafile for the stream in order for the player to perform the specified event.</span></span> <span data-ttu-id="b66d7-134">Un exemple d’utilisation est l’insertion d’une publicité.</span><span class="sxs-lookup"><span data-stu-id="b66d7-134">An example of use is ad insertion.</span></span> |
| <span data-ttu-id="b66d7-135">OPENEVENT</span><span class="sxs-lookup"><span data-stu-id="b66d7-135">OPENEVENT</span></span>   | <span data-ttu-id="b66d7-136">Ce script précède l’événement réel.</span><span class="sxs-lookup"><span data-stu-id="b66d7-136">This script precedes the actual EVENT.</span></span> <span data-ttu-id="b66d7-137">Le OPENEVENT permet au joueur de mettre en mémoire tampon le contenu afin que lorsque l’événement se produise, le basculement entre les flux semble être transparent.</span><span class="sxs-lookup"><span data-stu-id="b66d7-137">The OPENEVENT allows the player to pre-buffer the content so that when the EVENT occurs, the switch between streams appears to be seamless.</span></span>                                                                                                       |
| <span data-ttu-id="b66d7-138">TEXT</span><span class="sxs-lookup"><span data-stu-id="b66d7-138">TEXT</span></span>        | <span data-ttu-id="b66d7-139">Chaîne de texte qui est affichée dans la zone légendes du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b66d7-139">A TEXT string that is displayed in the captions area of Windows Media Player.</span></span> <span data-ttu-id="b66d7-140">Peut être du texte brut, du texte SAMI ou du texte mis en forme HTML.</span><span class="sxs-lookup"><span data-stu-id="b66d7-140">Can be plain text, SAMI, or HTML formatted text.</span></span>                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="b66d7-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b66d7-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b66d7-142">**Utilisation des commandes de script**</span><span class="sxs-lookup"><span data-stu-id="b66d7-142">**Using Script Commands**</span></span>](using-script-commands.md)
</dt> </dl>

 

 




