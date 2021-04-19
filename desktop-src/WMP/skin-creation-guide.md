---
title: Guide de création d’apparence
description: Guide de création d’apparence
ms.assetid: 86c77764-5c8c-4493-ac2d-15268c1ba564
keywords:
- Lecteur Windows Media, habillages
- Apparences du lecteur Windows Media, Guide de création
- Skins, Guide de création
- créer des apparences, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7214accedf24bd80449bf8952bc9268f9b9bf49d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509792"
---
# <a name="skin-creation-guide"></a><span data-ttu-id="ec931-107">Guide de création d’apparence</span><span class="sxs-lookup"><span data-stu-id="ec931-107">Skin Creation Guide</span></span>

<span data-ttu-id="ec931-108">Ce guide est une série d’explications détaillées sur la façon de créer différents types d’apparences.</span><span class="sxs-lookup"><span data-stu-id="ec931-108">This guide is a series of detailed explanations of how to create different kinds of skins.</span></span> <span data-ttu-id="ec931-109">Pour plus d’informations générales sur les apparences, consultez [à propos des apparences](about-skins.md).</span><span class="sxs-lookup"><span data-stu-id="ec931-109">For more general information on skins, see [About Skins](about-skins.md).</span></span> <span data-ttu-id="ec931-110">Pour plus d’informations sur chaque attribut, méthode et événement utilisé dans les apparences, consultez la référence sur la programmation de l' [apparence](skin-programming-reference.md).</span><span class="sxs-lookup"><span data-stu-id="ec931-110">For specific details about every attribute, method, and event used in skins, see the [Skin Programming Reference](skin-programming-reference.md).</span></span> <span data-ttu-id="ec931-111">À mesure que vous êtes plus impliqué dans la programmation de votre apparence, vous pouvez lire la partie de ce kit de développement logiciel (SDK) couvrant le [modèle objet du lecteur Windows Media](windows-media-player-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="ec931-111">As you get more involved in the programming of your skin, you may want to read the part of this SDK covering the [Windows Media Player Object Model](windows-media-player-object-model.md).</span></span>

<span data-ttu-id="ec931-112">Dans ce guide, vous trouverez des instructions pour créer l’art pour Adobe Photoshop 5,5, un programme de manipulation des dessins populaires.</span><span class="sxs-lookup"><span data-stu-id="ec931-112">In this guide, instructions for creating the art will be given for Adobe Photoshop 5.5, a popular art manipulation program.</span></span> <span data-ttu-id="ec931-113">Les instructions spécifiques peuvent être différentes si vous disposez d’un programme artistique similaire, tel que Jasc Paint Shop Pro ou la viscosité de Sonic found, mais les concepts sont les mêmes.</span><span class="sxs-lookup"><span data-stu-id="ec931-113">The specific instructions may be different if you have a similar art program such as Jasc Paint Shop Pro or Sonic Foundry Viscosity, but the concepts will be the same.</span></span> <span data-ttu-id="ec931-114">Photoshop a été choisi pour deux raisons : il s’agit d’un programme art populaire pour les artistes commerciaux et il fonctionne avec des couches.</span><span class="sxs-lookup"><span data-stu-id="ec931-114">Photoshop was chosen for two reasons: it is a popular art program for commercial artists, and it works with layers.</span></span> <span data-ttu-id="ec931-115">Comme vous le verrez dans les didacticiels, les couches sont très utiles pour la création d’apparences.</span><span class="sxs-lookup"><span data-stu-id="ec931-115">As you will see in the tutorials, layers are very useful for skin creation.</span></span>

<span data-ttu-id="ec931-116">Ce guide aborde les tâches suivantes.</span><span class="sxs-lookup"><span data-stu-id="ec931-116">This guide will cover the following tasks.</span></span>



| <span data-ttu-id="ec931-117">Tâche</span><span class="sxs-lookup"><span data-stu-id="ec931-117">Task</span></span>                                                     | <span data-ttu-id="ec931-118">Description</span><span class="sxs-lookup"><span data-stu-id="ec931-118">Description</span></span>                                                                                     |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ec931-119">Création de votre première apparence</span><span class="sxs-lookup"><span data-stu-id="ec931-119">Building Your First Skin</span></span>](building-your-first-skin.md) | <span data-ttu-id="ec931-120">Procédure pas à pas d’une apparence simple qui démarre et arrête le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ec931-120">A walk-through of a simple skin that starts and stops Windows Media Player.</span></span>                     |
| [<span data-ttu-id="ec931-121">Ajout d’une sélection</span><span class="sxs-lookup"><span data-stu-id="ec931-121">Adding a Playlist</span></span>](adding-a-playlist.md)               | <span data-ttu-id="ec931-122">Comment utiliser une sélection simple.</span><span class="sxs-lookup"><span data-stu-id="ec931-122">How to use a simple playlist.</span></span>                                                                   |
| [<span data-ttu-id="ec931-123">Choix des fichiers</span><span class="sxs-lookup"><span data-stu-id="ec931-123">Choosing Files</span></span>](choosing-files.md)                     | <span data-ttu-id="ec931-124">Comment sélectionner des fichiers avec une boîte de dialogue Ouvrir un fichier.</span><span class="sxs-lookup"><span data-stu-id="ec931-124">How to pick files with an open file dialog box.</span></span>                                                 |
| [<span data-ttu-id="ec931-125">Ajout d’une vidéo</span><span class="sxs-lookup"><span data-stu-id="ec931-125">Adding Video</span></span>](adding-video.md)                         | <span data-ttu-id="ec931-126">Comment placer une fenêtre vidéo dans votre apparence.</span><span class="sxs-lookup"><span data-stu-id="ec931-126">How to put a video window into your skin.</span></span>                                                       |
| [<span data-ttu-id="ec931-127">Ajout de visualisations</span><span class="sxs-lookup"><span data-stu-id="ec931-127">Adding Visualizations</span></span>](adding-visualizations.md)       | <span data-ttu-id="ec931-128">Comment ajouter des visualisations.</span><span class="sxs-lookup"><span data-stu-id="ec931-128">How to add visualizations.</span></span>                                                                      |
| [<span data-ttu-id="ec931-129">Ajout d’un curseur</span><span class="sxs-lookup"><span data-stu-id="ec931-129">Adding a Slider</span></span>](adding-a-slider.md)                   | <span data-ttu-id="ec931-130">Comment utiliser un curseur pour suivre la progression de votre contenu multimédia... et laissez l’utilisateur changer !</span><span class="sxs-lookup"><span data-stu-id="ec931-130">How to use a slider to track the progress of your media content ... and let the user change it!</span></span> |
| [<span data-ttu-id="ec931-131">Création de curseurs personnalisés</span><span class="sxs-lookup"><span data-stu-id="ec931-131">Creating Custom Sliders</span></span>](creating-custom-sliders.md)   | <span data-ttu-id="ec931-132">Comment contrôler le volume à l’aide d’un curseur personnalisé.</span><span class="sxs-lookup"><span data-stu-id="ec931-132">How to control the volume with a custom slider.</span></span>                                                 |
| [<span data-ttu-id="ec931-133">Autres exemples d’apparence</span><span class="sxs-lookup"><span data-stu-id="ec931-133">Other Skin Samples</span></span>](other-skin-samples.md)             | <span data-ttu-id="ec931-134">Consultez la section exemples du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="ec931-134">See the samples section of the SDK.</span></span>                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="ec931-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ec931-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec931-136">**Apparences du lecteur Windows Media**</span><span class="sxs-lookup"><span data-stu-id="ec931-136">**Windows Media Player Skins**</span></span>](windows-media-player-skins.md)
</dt> </dl>

 

 




