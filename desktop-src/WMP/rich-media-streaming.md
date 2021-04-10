---
title: Diffusion multimédia enrichie
description: Diffusion multimédia enrichie
ms.assetid: 3a48ee9a-5bf8-4cd0-9eed-07ec6da0f578
keywords:
- Windows Media Player, présentations basées sur le Web
- Modèle objet du lecteur Windows Media, présentations basées sur le Web
- modèle objet, présentations basées sur le Web
- Windows Media Player Mobile, présentations basées sur le Web
- Contrôle ActiveX du lecteur Windows Media, présentations basées sur le Web
- Windows Media Player Mobile contrôle ActiveX, présentations basées sur le Web
- Contrôle ActiveX, présentations basées sur le Web
- Lecteur Windows Media, diffusion multimédia riche
- Modèle objet du lecteur Windows Media, diffusion multimédia riche
- modèle objet, diffusion multimédia riche
- Windows Media Player Mobile, diffusion multimédia riche
- Contrôle ActiveX du lecteur Windows Media, diffusion multimédia riche
- Windows Media Player Mobile contrôle ActiveX, diffusion multimédia riche
- Contrôle ActiveX, diffusion multimédia riche
- Présentations basées sur le Web, diffusion multimédia riche
- création de présentations basées sur le Web, diffusion multimédia riche
- diffusion multimédia enrichie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b454ef62f5f5aaaf424598d55d85c03684538c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674677"
---
# <a name="rich-media-streaming"></a><span data-ttu-id="d5f45-120">Diffusion multimédia enrichie</span><span class="sxs-lookup"><span data-stu-id="d5f45-120">Rich Media Streaming</span></span>

<span data-ttu-id="d5f45-121">Les pages Web complexes contiennent de nombreux composants différents qui sont normalement transférés séparément.</span><span class="sxs-lookup"><span data-stu-id="d5f45-121">Complex webpages contain many different components that are normally transferred separately.</span></span> <span data-ttu-id="d5f45-122">Sur une connexion lente, ces pages affichent un seul élément à la fois et peuvent prendre plusieurs minutes pour s’afficher complètement.</span><span class="sxs-lookup"><span data-stu-id="d5f45-122">On a slow connection, such pages display one piece at a time and may take several minutes to display completely.</span></span> <span data-ttu-id="d5f45-123">Cela peut vous empêcher de synchroniser efficacement les pages Web avec vos médias numériques.</span><span class="sxs-lookup"><span data-stu-id="d5f45-123">This may prevent you from effectively synchronizing webpages with your digital media.</span></span> <span data-ttu-id="d5f45-124">La solution à ce problème est la diffusion multimédia enrichie, ce qui signifie que vous ajoutez vos pages Web à votre flux de données multimédias numériques afin qu’elles soient fournies en même temps que les données audio ou vidéo.</span><span class="sxs-lookup"><span data-stu-id="d5f45-124">The solution to this problem is rich media streaming, which means adding your webpages to your digital media stream so that they are delivered at the same time as the audio or video data.</span></span>

<span data-ttu-id="d5f45-125">La diffusion multimédia en continu riche utilise une disposition de jeu de frames simple et se comporte exactement comme un basculement d’URL normal.</span><span class="sxs-lookup"><span data-stu-id="d5f45-125">Rich media streaming uses a simple frameset layout and behaves exactly like normal URL flipping.</span></span> <span data-ttu-id="d5f45-126">Tout comme dans le basculement d’URL, les commandes de script d’URL incorporées dans les flux de données multimédias numériques sont utilisées pour afficher le contenu dans le frame cible.</span><span class="sxs-lookup"><span data-stu-id="d5f45-126">Just as in URL flipping, URL script commands embedded in digital media streams are used to display the content in the target frame.</span></span> <span data-ttu-id="d5f45-127">Au lieu de pointer vers des pages sur le Web, toutefois, les commandes de script d’URL sont utilisées par le lecteur Windows Media 9 ou une version ultérieure pour accéder aux fichiers du cache Internet Explorer où le contenu HTML diffusé en continu est placé lors de sa réception.</span><span class="sxs-lookup"><span data-stu-id="d5f45-127">Instead of pointing to pages on the Web, however, the URL script commands are used by Windows Media Player 9 Series or later to access files in the Internet Explorer cache where the streamed HTML content is placed as it is received.</span></span> <span data-ttu-id="d5f45-128">Tout comme avec le basculement d’URL normal, vous pouvez écrire des gestionnaires d’événements qui répondent à ces commandes de script d’URL, ou vous pouvez laisser le contrôle du lecteur Windows Media traiter tout automatiquement.</span><span class="sxs-lookup"><span data-stu-id="d5f45-128">Just as with normal URL flipping, you can write event handlers that respond to these URL script commands, or you can let the Windows Media Player control handle everything automatically.</span></span>

> [!Note]  
> <span data-ttu-id="d5f45-129">Tout contenu HTML fourni via le streaming multimédia enrichi est lu dans la zone de sécurité Internet et est soumis aux paramètres de sécurité du navigateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d5f45-129">Any HTML content delivered through rich media streaming is played back in the Internet security zone, and is subject to the user's browser security settings.</span></span>

 

<span data-ttu-id="d5f45-130">Pour plus d’informations sur la création de présentations multimédias riches, consultez le kit de développement logiciel (SDK) Windows Media Format 9 ou version ultérieure et le kit de développement logiciel (SDK) Windows Media Encoder 9.</span><span class="sxs-lookup"><span data-stu-id="d5f45-130">For more information on creating rich media presentations, see the Windows Media Format 9 Series or later SDK and the Windows Media Encoder 9 Series SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5f45-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d5f45-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5f45-132">**Création de présentations Web-Based**</span><span class="sxs-lookup"><span data-stu-id="d5f45-132">**Creating Web-Based Presentations**</span></span>](creating-web-based-presentations.md)
</dt> <dt>

[<span data-ttu-id="d5f45-133">**Utilisation d’un script pour contrôler le basculement d’URL**</span><span class="sxs-lookup"><span data-stu-id="d5f45-133">**Using Script to Control URL Flipping**</span></span>](using-script-to-control-url-flipping.md)
</dt> </dl>

 

 




