---
title: À propos de l’exemple de plug-in de vidéo DSP
description: À propos de l’exemple de plug-in de vidéo DSP
ms.assetid: f2ba8e9d-a0e4-4679-99dc-2bfe9e451ffd
keywords:
- Plug-ins du lecteur Windows Media, exemples
- plug-ins, exemples
- plug-ins de traitement de signal numérique, exemples
- Plug-ins DSP, exemples
- Plug-ins du lecteur Windows Media, DSP vidéo
- plug-ins, DSP vidéo
- plug-ins de traitement de signal numérique, exemples vidéo
- Plug-ins DSP, exemples vidéo
- exemples, plug-ins DSP
- plug-ins vidéo DSP, exemples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ede2eda82c834cefad0e31009805f24941cd4a6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509982"
---
# <a name="about-the-sample-video-dsp-plug-in"></a><span data-ttu-id="c6a61-113">À propos de l’exemple de plug-in de vidéo DSP</span><span class="sxs-lookup"><span data-stu-id="c6a61-113">About the Sample Video DSP Plug-in</span></span>

<span data-ttu-id="c6a61-114">L’exemple de plug-in Video DSP fournit une implémentation de traitement simple qui met à l’échelle la saturation de couleur de la vidéo par un facteur fourni par l’utilisateur dans la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="c6a61-114">The sample video DSP plug-in provides a simple processing implementation that scales the color saturation of the video by a factor provided by the user in the property page.</span></span> <span data-ttu-id="c6a61-115">Le plug-in accepte des valeurs comprises entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="c6a61-115">The plug-in accepts values between zero and 1.</span></span> <span data-ttu-id="c6a61-116">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="c6a61-116">The default value is 1.</span></span> <span data-ttu-id="c6a61-117">La valeur 1 n’a aucun effet sur l’image vidéo ; d’autres facteurs de mise à l’échelle désaturent la couleur de l’image.</span><span class="sxs-lookup"><span data-stu-id="c6a61-117">A value of 1 has no effect upon the video image; other scale factors desaturate the image color.</span></span> <span data-ttu-id="c6a61-118">Par exemple, la valeur 5 donne une saturation de couleur de 50%.</span><span class="sxs-lookup"><span data-stu-id="c6a61-118">For instance, a value of .5 would result in 50 percent color saturation.</span></span> <span data-ttu-id="c6a61-119">La valeur zéro produit une vidéo en nuances de gris.</span><span class="sxs-lookup"><span data-stu-id="c6a61-119">A value of zero results in grayscale video.</span></span>

<span data-ttu-id="c6a61-120">L’exemple de plug-in Video DSP fonctionne avec les formats vidéo suivants :</span><span class="sxs-lookup"><span data-stu-id="c6a61-120">The sample video DSP plug-in works with the following video formats:</span></span>

-   <span data-ttu-id="c6a61-121">NV12</span><span class="sxs-lookup"><span data-stu-id="c6a61-121">NV12</span></span>
-   <span data-ttu-id="c6a61-122">YV12</span><span class="sxs-lookup"><span data-stu-id="c6a61-122">YV12</span></span>
-   <span data-ttu-id="c6a61-123">YUY2</span><span class="sxs-lookup"><span data-stu-id="c6a61-123">YUY2</span></span>
-   <span data-ttu-id="c6a61-124">UYVY</span><span class="sxs-lookup"><span data-stu-id="c6a61-124">UYVY</span></span>
-   <span data-ttu-id="c6a61-125">RGB32</span><span class="sxs-lookup"><span data-stu-id="c6a61-125">RGB32</span></span>
-   <span data-ttu-id="c6a61-126">RGB24</span><span class="sxs-lookup"><span data-stu-id="c6a61-126">RGB24</span></span>
-   <span data-ttu-id="c6a61-127">RGB555</span><span class="sxs-lookup"><span data-stu-id="c6a61-127">RGB555</span></span>
-   <span data-ttu-id="c6a61-128">RGB565</span><span class="sxs-lookup"><span data-stu-id="c6a61-128">RGB565</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6a61-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c6a61-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6a61-130">**Génération d’un plug-in DSP**</span><span class="sxs-lookup"><span data-stu-id="c6a61-130">**Building a DSP Plug-in**</span></span>](building-a-dsp-plug-in.md)
</dt> </dl>

 

 




