---
title: Création de présentations Web-Based
description: Création de présentations Web-Based
ms.assetid: 60d8be10-ebed-4a4f-b17f-700475b51b34
keywords:
- Windows Media Player, présentations basées sur le Web
- Modèle objet du lecteur Windows Media, présentations basées sur le Web
- modèle objet, présentations basées sur le Web
- Windows Media Player Mobile, présentations basées sur le Web
- Contrôle ActiveX du lecteur Windows Media, présentations basées sur le Web
- Windows Media Player Mobile contrôle ActiveX, présentations basées sur le Web
- Contrôle ActiveX, présentations basées sur le Web
- Présentations basées sur le Web, création
- création de présentations basées sur le Web, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 117ee00164b50d319699f6e1d1806c4d8bf374af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311413"
---
# <a name="creating-web-based-presentations"></a><span data-ttu-id="db48b-112">Création de présentations Web-Based</span><span class="sxs-lookup"><span data-stu-id="db48b-112">Creating Web-Based Presentations</span></span>

<span data-ttu-id="db48b-113">Le contrôle du lecteur Windows Media vous permet de créer facilement des présentations sur le Web qui combinent du contenu audio et vidéo avec du code HTML.</span><span class="sxs-lookup"><span data-stu-id="db48b-113">The Windows Media Player control lets you easily create Web-based slide-show presentations that combine audio and video with HTML.</span></span> <span data-ttu-id="db48b-114">En ajoutant des commandes de script de type URL à vos fichiers multimédias, vous pouvez faire en sorte que les pages Web spécifiées s’affichent dans un cadre de navigateur Web spécifié à des moments spécifiques pendant la lecture des médias numériques.</span><span class="sxs-lookup"><span data-stu-id="db48b-114">By adding URL-type script commands to your media files, you can cause specified webpages to display in a specified Web browser frame at specific times during digital media playback.</span></span>

<span data-ttu-id="db48b-115">Le lecteur Windows Media offre également une diffusion multimédia riche pour permettre une livraison efficace des données HTML sur un réseau à l’intérieur d’un seul fichier ou flux Windows Media.</span><span class="sxs-lookup"><span data-stu-id="db48b-115">Windows Media Player also features rich media streaming to enable efficient delivery of HTML data over a network inside a single Windows Media stream or file.</span></span> <span data-ttu-id="db48b-116">Le lecteur et le serveur gèrent la livraison en temps utile de l’audio, de la vidéo et du code HTML dans le navigateur.</span><span class="sxs-lookup"><span data-stu-id="db48b-116">The Player and server handle the smooth, timely delivery of audio, video, and HTML to the browser.</span></span> <span data-ttu-id="db48b-117">Tout comme dans les présentations Web qui n’utilisent pas de diffusion multimédia enrichie, les commandes de script incorporées affichent la présentation dans une trame de navigateur spécifiée à des moments précis.</span><span class="sxs-lookup"><span data-stu-id="db48b-117">Just as in Web presentations that do not use rich media streaming, embedded script commands render the presentation in a specified browser frame at specified times.</span></span>

<span data-ttu-id="db48b-118">Une disposition classique des présentations Web utilise deux frames.</span><span class="sxs-lookup"><span data-stu-id="db48b-118">A typical layout for Web-based presentations uses two frames.</span></span> <span data-ttu-id="db48b-119">Une image contient une page Web qui incorpore le contrôle du lecteur Windows Media et affiche la partie vidéo d’une présentation.</span><span class="sxs-lookup"><span data-stu-id="db48b-119">One frame contains a webpage that embeds the Windows Media Player control and displays the video part of a presentation.</span></span> <span data-ttu-id="db48b-120">L’autre cadre affiche des pages Web qui changent à différents moments de la lecture de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="db48b-120">The other frame displays webpages that change at various times as the video plays.</span></span>

<span data-ttu-id="db48b-121">Si les supports numériques accompagnant vos pages Web contiennent uniquement de l’audio, vous pouvez masquer le frame qui contient le contrôle du lecteur Windows Media en définissant sa largeur sur zéro.</span><span class="sxs-lookup"><span data-stu-id="db48b-121">If the digital media accompanying your webpages contains audio only, you can hide the frame that contains the Windows Media Player control by setting its width to zero.</span></span> <span data-ttu-id="db48b-122">De cette façon, l’audio peut s’exécuter sans interruption en arrière-plan pendant que vos pages Web s’affichent dans la fenêtre de navigateur complète.</span><span class="sxs-lookup"><span data-stu-id="db48b-122">This way, the audio can play uninterrupted in the background while your webpages display in the full browser window.</span></span>

<span data-ttu-id="db48b-123">Les sections suivantes décrivent les techniques courantes d’activation des présentations basées sur le Web :</span><span class="sxs-lookup"><span data-stu-id="db48b-123">The following sections describe common techniques for enabling Web-based presentations:</span></span>

-   [<span data-ttu-id="db48b-124">Retournement d’URL</span><span class="sxs-lookup"><span data-stu-id="db48b-124">URL Flipping</span></span>](url-flipping.md)
-   [<span data-ttu-id="db48b-125">Diffusion multimédia enrichie</span><span class="sxs-lookup"><span data-stu-id="db48b-125">Rich Media Streaming</span></span>](rich-media-streaming.md)

## <a name="related-topics"></a><span data-ttu-id="db48b-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="db48b-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db48b-127">**Guide de contrôle du lecteur**</span><span class="sxs-lookup"><span data-stu-id="db48b-127">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




