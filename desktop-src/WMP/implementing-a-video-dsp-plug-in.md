---
title: Implémentation d’un plug-in de DSP vidéo
description: Implémentation d’un plug-in de DSP vidéo
ms.assetid: 36c06c57-7623-430b-8280-9dba7b0a2e9b
keywords:
- Plug-ins du lecteur Windows Media, DSP vidéo
- plug-ins, DSP vidéo
- plug-ins de traitement de signal numérique, implémentation du code
- Plug-ins DSP, implémentation du code
- plug-ins de traitement de signal numérique, modification de l’exemple de code
- Plug-ins DSP, modification de l’exemple de code
- plug-ins de traitement de signal numérique, implémentation vidéo
- Plug-ins DSP, implémentation vidéo
- plug-ins vidéo DSP, implémentation du code
- plug-ins vidéo DSP, modification de l’exemple de code
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43f1b819f328fc586d21208c00b6f0d03dca4fe9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310258"
---
# <a name="implementing-a-video-dsp-plug-in"></a><span data-ttu-id="17c24-113">Implémentation d’un plug-in de DSP vidéo</span><span class="sxs-lookup"><span data-stu-id="17c24-113">Implementing a Video DSP Plug-in</span></span>

<span data-ttu-id="17c24-114">Les adaptateurs d’affichage vidéo de l’ordinateur prennent en charge un ensemble de formats vidéo.</span><span class="sxs-lookup"><span data-stu-id="17c24-114">Computer video display adapters support a set of video formats.</span></span> <span data-ttu-id="17c24-115">Les codecs vidéo numériques prennent également en charge un ensemble de formats vidéo.</span><span class="sxs-lookup"><span data-stu-id="17c24-115">Digital video codecs also support a set of video formats.</span></span> <span data-ttu-id="17c24-116">Lorsque vous tentez de lire un fichier vidéo particulier, le lecteur Windows Media doit choisir un format à utiliser pour le rendu.</span><span class="sxs-lookup"><span data-stu-id="17c24-116">When attempting to play a particular video file, Windows Media Player must choose a format to use for rendering.</span></span> <span data-ttu-id="17c24-117">Le joueur tente de trouver la meilleure correspondance entre les formats pris en charge par le codec vidéo et les formats pris en charge par la carte vidéo, c’est-à-dire celui qui donne la meilleure qualité.</span><span class="sxs-lookup"><span data-stu-id="17c24-117">The Player attempts to find the best match between the formats supported by the video codec and the formats supported by the video display adapter—that is, the one that yields the highest quality.</span></span>

<span data-ttu-id="17c24-118">Pour créer un plug-in Windows Media Player DSP qui traite la vidéo, vous devez d’abord décider quels formats vidéo vous souhaitez faire traiter par votre plug-in.</span><span class="sxs-lookup"><span data-stu-id="17c24-118">To create a Windows Media Player DSP plug-in that processes video, you'll first need to decide which video formats you'd like your plug-in to process.</span></span> <span data-ttu-id="17c24-119">L’exemple de plug-in Video DSP fonctionne avec les formats vidéo suivants :</span><span class="sxs-lookup"><span data-stu-id="17c24-119">The sample video DSP plug-in works with the following video formats:</span></span>

-   <span data-ttu-id="17c24-120">NV12</span><span class="sxs-lookup"><span data-stu-id="17c24-120">NV12</span></span>
-   <span data-ttu-id="17c24-121">YV12</span><span class="sxs-lookup"><span data-stu-id="17c24-121">YV12</span></span>
-   <span data-ttu-id="17c24-122">YUY2</span><span class="sxs-lookup"><span data-stu-id="17c24-122">YUY2</span></span>
-   <span data-ttu-id="17c24-123">UYVY</span><span class="sxs-lookup"><span data-stu-id="17c24-123">UYVY</span></span>
-   <span data-ttu-id="17c24-124">RGB32</span><span class="sxs-lookup"><span data-stu-id="17c24-124">RGB32</span></span>
-   <span data-ttu-id="17c24-125">RGB24</span><span class="sxs-lookup"><span data-stu-id="17c24-125">RGB24</span></span>
-   <span data-ttu-id="17c24-126">RGB555</span><span class="sxs-lookup"><span data-stu-id="17c24-126">RGB555</span></span>
-   <span data-ttu-id="17c24-127">RGB565</span><span class="sxs-lookup"><span data-stu-id="17c24-127">RGB565</span></span>

<span data-ttu-id="17c24-128">Vous avez le choix entre les formats à traiter.</span><span class="sxs-lookup"><span data-stu-id="17c24-128">Which formats you choose to process is up to you.</span></span> <span data-ttu-id="17c24-129">Vous pouvez supprimer des formats de l’exemple de plug-in afin qu’ils ne soient plus pris en charge et vous pouvez ajouter du code pour traiter des formats supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="17c24-129">You can remove formats from the sample plug-in so that they aren't supported any longer and you can add code to process additional formats.</span></span>

<span data-ttu-id="17c24-130">Les sections suivantes fournissent des informations supplémentaires que vous devez connaître avant de créer votre propre plug-in de DSP vidéo pour le lecteur Windows Media :</span><span class="sxs-lookup"><span data-stu-id="17c24-130">The following sections provide additional information you should know before creating your own video DSP plug-in for Windows Media Player:</span></span>

-   [<span data-ttu-id="17c24-131">Négociation du format vidéo dans l’exemple de plug-in de la vidéo DSP</span><span class="sxs-lookup"><span data-stu-id="17c24-131">Video Format Negotiation in the Sample Video DSP Plug-in</span></span>](video-format-negotiation-in-the-sample-video-dsp-plug-in.md)
-   [<span data-ttu-id="17c24-132">DoProcessOutput dans l’exemple de plug-in DSP de vidéo</span><span class="sxs-lookup"><span data-stu-id="17c24-132">DoProcessOutput in the Sample Video DSP Plug-in</span></span>](doprocessoutput-in-the-sample-video-dsp-plug-in.md)
-   [<span data-ttu-id="17c24-133">Traitement de la vidéo</span><span class="sxs-lookup"><span data-stu-id="17c24-133">Processing the Video</span></span>](processing-the-video.md)

## <a name="related-topics"></a><span data-ttu-id="17c24-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="17c24-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17c24-135">**Implémentation de votre code DSP**</span><span class="sxs-lookup"><span data-stu-id="17c24-135">**Implementing Your DSP Code**</span></span>](implementing-your-dsp-code.md)
</dt> </dl>

 

 




