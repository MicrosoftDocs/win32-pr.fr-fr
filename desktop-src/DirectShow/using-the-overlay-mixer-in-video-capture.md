---
description: Utilisation du mélangeur de superposition dans la capture vidéo
ms.assetid: 43468fa2-6dea-439d-9e24-f47a053ad561
title: Utilisation du mélangeur de superposition dans la capture vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bff115d566654732e80c0bcb0f554c4ad96e65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034811"
---
# <a name="using-the-overlay-mixer-in-video-capture"></a><span data-ttu-id="f3cbd-103">Utilisation du mélangeur de superposition dans la capture vidéo</span><span class="sxs-lookup"><span data-stu-id="f3cbd-103">Using the Overlay Mixer in Video Capture</span></span>

<span data-ttu-id="f3cbd-104">Il existe certains genres de vidéos que le filtre de [convertisseur vidéo](video-renderer-filter.md) ne peut pas afficher par lui-même.</span><span class="sxs-lookup"><span data-stu-id="f3cbd-104">There are certain kinds of video that the [Video Renderer](video-renderer-filter.md) filter cannot display by itself.</span></span> <span data-ttu-id="f3cbd-105">Dans ce cas, le convertisseur vidéo doit fonctionner avec le filtre de [mixage de superposition](overlay-mixer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="f3cbd-105">In these situations, the Video Renderer must work with the [Overlay Mixer](overlay-mixer-filter.md) filter.</span></span> <span data-ttu-id="f3cbd-106">Le mélangeur de superposition gère le rendu, tandis que le convertisseur vidéo gère la fenêtre vidéo.</span><span class="sxs-lookup"><span data-stu-id="f3cbd-106">The Overlay Mixer manages the rendering, while the Video Renderer manages the video window.</span></span> <span data-ttu-id="f3cbd-107">Le mélangeur de superposition est nécessaire dans les situations suivantes :</span><span class="sxs-lookup"><span data-stu-id="f3cbd-107">The Overlay Mixer is needed in the following situations:</span></span>

-   <span data-ttu-id="f3cbd-108">Broches du port vidéo (VP).</span><span class="sxs-lookup"><span data-stu-id="f3cbd-108">Video port (VP) pins.</span></span> <span data-ttu-id="f3cbd-109">Si le périphérique de capture utilise un port vidéo, le mélangeur de superpositions gère la superposition matérielle.</span><span class="sxs-lookup"><span data-stu-id="f3cbd-109">If the capture device uses a video port, the Overlay Mixer manages the hardware overlay.</span></span>
-   <span data-ttu-id="f3cbd-110">Vidéo entrelacée.</span><span class="sxs-lookup"><span data-stu-id="f3cbd-110">Interlaced video.</span></span> <span data-ttu-id="f3cbd-111">Pour la vidéo entrelacée, le décodeur requiert un format [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , que le convertisseur vidéo ne prend pas en charge.</span><span class="sxs-lookup"><span data-stu-id="f3cbd-111">For interlaced video, the decoder requires a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format, which the Video Renderer does not support.</span></span>
-   <span data-ttu-id="f3cbd-112">Sous-titres.</span><span class="sxs-lookup"><span data-stu-id="f3cbd-112">Closed captions.</span></span> <span data-ttu-id="f3cbd-113">Le texte de légende est rendu sous forme de bitmaps de 8 bits par pixel, que le mélangeur de superposition recouvre sur la vidéo.</span><span class="sxs-lookup"><span data-stu-id="f3cbd-113">The caption text is rendered as 8-bits-per-pixel bitmaps, which the Overlay Mixer overlays onto the video.</span></span>

<span data-ttu-id="f3cbd-114">La méthode **RenderStream** du générateur de graphiques de capture insère le mélangeur de superposition chaque fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="f3cbd-114">The Capture Graph Builder's **RenderStream** method inserts the Overlay Mixer whenever needed.</span></span> <span data-ttu-id="f3cbd-115">Toutefois, si vous générez le graphique sans utiliser le générateur de graphiques de capture, vous devez vérifier chacune de ces situations et insérer vous-même le mélangeur de superposition.</span><span class="sxs-lookup"><span data-stu-id="f3cbd-115">If you are building the graph without using the Capture Graph Builder, however, you must check for each of these situations and insert the Overlay Mixer yourself.</span></span>

-   <span data-ttu-id="f3cbd-116">\[! Précieuse\]</span><span class="sxs-lookup"><span data-stu-id="f3cbd-116">\[!Important\]</span></span>  
    > <span data-ttu-id="f3cbd-117">Si l’appareil possède un code confidentiel de VP, vous devez le connecter même si vous n’avez pas besoin de la fonctionnalité d’aperçu dans votre application.</span><span class="sxs-lookup"><span data-stu-id="f3cbd-117">If the device has a VP pin, you must connect the Overlay Mixer even if you do not need preview functionality in your application.</span></span> <span data-ttu-id="f3cbd-118">Avec un port vidéo, l’appareil de capture envoie toujours les données vidéo à la superposition matérielle, de sorte que le mélangeur de superposition est toujours nécessaire.</span><span class="sxs-lookup"><span data-stu-id="f3cbd-118">With a video port, the capture device always sends the video data to the hardware overlay, so the Overlay Mixer is always needed.</span></span>

     

<span data-ttu-id="f3cbd-119">Les filtres de convertisseur de mixage vidéo (VMR-7 et VMR-9) prennent tous deux en charge la vidéo entrelacée et peuvent combiner des bitmaps de sous-titres sur la vidéo principale.</span><span class="sxs-lookup"><span data-stu-id="f3cbd-119">The Video Mixing Renderer filters (VMR-7 and VMR-9) both support interlaced video, and are able to mix closed caption bitmaps onto the primary video.</span></span> <span data-ttu-id="f3cbd-120">Si vous utilisez VMR pour ces scénarios, vous n’avez pas besoin d’utiliser le mélangeur de superposition.</span><span class="sxs-lookup"><span data-stu-id="f3cbd-120">If you are using the VMR for those scenarios, then you do not need to use the Overlay Mixer.</span></span> <span data-ttu-id="f3cbd-121">VMR-9 ne prend pas en charge les connexions à un pin de vice-président.</span><span class="sxs-lookup"><span data-stu-id="f3cbd-121">The VMR-9 does not support VP pin connections.</span></span> <span data-ttu-id="f3cbd-122">VMR-7 prend en charge les connexions de vice-président via le filtre du gestionnaire de port vidéo.</span><span class="sxs-lookup"><span data-stu-id="f3cbd-122">The VMR-7 supports VP pin connections through the Video Port Manager filter.</span></span> <span data-ttu-id="f3cbd-123">Toutefois, vous constaterez peut-être que certains pilotes ne fonctionnent pas correctement avec le gestionnaire de port vidéo.</span><span class="sxs-lookup"><span data-stu-id="f3cbd-123">However, you may find that some drivers do not work correctly with the Video Port Manager.</span></span> <span data-ttu-id="f3cbd-124">Pour cette raison, le mélangeur de superposition est toujours recommandé pour les broches du VP.</span><span class="sxs-lookup"><span data-stu-id="f3cbd-124">For that reason, the Overlay Mixer is still recommended for VP pins.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3cbd-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f3cbd-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3cbd-126">Rubriques avancées sur la capture</span><span class="sxs-lookup"><span data-stu-id="f3cbd-126">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="f3cbd-127">Broches de port vidéo</span><span class="sxs-lookup"><span data-stu-id="f3cbd-127">Video Port Pins</span></span>](video-port-pins.md)
</dt> <dt>

[<span data-ttu-id="f3cbd-128">Type de format VideoInfo2</span><span class="sxs-lookup"><span data-stu-id="f3cbd-128">VideoInfo2 Format Type</span></span>](videoinfo2-format-type.md)
</dt> </dl>

 

 



