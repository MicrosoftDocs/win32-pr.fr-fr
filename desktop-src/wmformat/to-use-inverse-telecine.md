---
title: Pour utiliser IVTC (inverse telecine)
description: Pour utiliser IVTC (inverse telecine)
ms.assetid: 7752d1ac-34b1-446a-a69c-29463c9e10f7
keywords:
- Windows Media Format SDK, inversement Telecine
- Kit de développement logiciel (SDK) Windows Media format, télécinéma
- ASF (Advanced Systems Format), inversement
- ASF (format avancé des systèmes), inversement
- ASF (Advanced Systems Format), télécinéma
- ASF (format avancé des systèmes), télécinéma
- inverser Telecine
- télécinéma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b17d4f4e3ae34c2a9efcaa4fe8e5ce7256474404
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "106509244"
---
# <a name="to-use-inverse-telecine"></a><span data-ttu-id="09340-111">Pour utiliser IVTC (inverse telecine)</span><span class="sxs-lookup"><span data-stu-id="09340-111">To Use Inverse Telecine</span></span>

<span data-ttu-id="09340-112">Telecine est le processus de conversion d’un film, qui compte 24 images par seconde, en vidéo, qui contient 60 champs (demi-frames) par seconde.</span><span class="sxs-lookup"><span data-stu-id="09340-112">Telecine is the process of converting film, which has 24 frames per second, to video, which has 60 fields (half frames) per second.</span></span> <span data-ttu-id="09340-113">Ce processus place les images de chaque image de film dans plusieurs champs vidéo.</span><span class="sxs-lookup"><span data-stu-id="09340-113">This process puts images from each film frame in multiple video fields.</span></span>

<span data-ttu-id="09340-114">Quand vous encodez numériquement une vidéo qui a été créée à partir d’un film à l’aide de Telecine, le processus de compression peut entraîner des artefacts de mouvement et d’autres dégradations de qualité.</span><span class="sxs-lookup"><span data-stu-id="09340-114">When you digitally encode a video that was created from film by using telecine, the compression process can cause motion artifacts and other degradations in quality.</span></span> <span data-ttu-id="09340-115">Pour éviter d’affecter la qualité de la sortie numérique, le codec Windows Media Video 9 prend en charge l’inverse de Telecine.</span><span class="sxs-lookup"><span data-stu-id="09340-115">To avoid affecting the quality of the digital output, the Windows Media Video 9 codec supports inverse telecine.</span></span> <span data-ttu-id="09340-116">Lorsque vous utilisez l’inverse telecine, le codec reconstruit les 24 images d’origine par seconde à partir de la vidéo d’entrée avant de coder le contenu.</span><span class="sxs-lookup"><span data-stu-id="09340-116">When using inverse telecine, the codec reconstructs the original 24 film frames per second from the input video before encoding the content.</span></span>

<span data-ttu-id="09340-117">Pour utiliser l’inverse telecine, vous devez :</span><span class="sxs-lookup"><span data-stu-id="09340-117">To use inverse telecine, you must:</span></span>

-   <span data-ttu-id="09340-118">Utilisez un profil avec un flux vidéo défini sur 24 images par seconde.</span><span class="sxs-lookup"><span data-stu-id="09340-118">Use a profile with a video stream set to 24 frames per second.</span></span>
-   <span data-ttu-id="09340-119">Connaître la configuration de champ de la vidéo d’entrée.</span><span class="sxs-lookup"><span data-stu-id="09340-119">Know the field configuration of the input video.</span></span>

<span data-ttu-id="09340-120">Pour utiliser l’inverse telecine pour une entrée au writer, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="09340-120">To use inverse telecine for an input to the writer, perform the following steps.</span></span>

1.  <span data-ttu-id="09340-121">Configurez le writer comme d’habitude.</span><span class="sxs-lookup"><span data-stu-id="09340-121">Set up the writer as usual.</span></span> <span data-ttu-id="09340-122">Pour plus d’informations, consultez [écriture de fichiers ASF](writing-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="09340-122">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span>
2.  <span data-ttu-id="09340-123">Avant de commencer à écrire des exemples, obtenez un pointeur vers l’interface [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) en appelant **IWMWriter :: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="09340-123">Before beginning to write samples, obtain a pointer to the [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) interface by calling **IWMWriter::QueryInterface**.</span></span>
3.  <span data-ttu-id="09340-124">Identifiez le flux à reconstruire en appelant [**IWMWriterAdvanced2 :: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) pour le numéro d’entrée souhaité.</span><span class="sxs-lookup"><span data-stu-id="09340-124">Identify the stream to be reconstructed by calling [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) for the desired input number.</span></span> <span data-ttu-id="09340-125">Pass g \_ wszDeinterlaceMode comme paramètre et WM \_ DM \_ désentrelace \_ INVERSETELECINE comme valeur.</span><span class="sxs-lookup"><span data-stu-id="09340-125">Pass g\_wszDeinterlaceMode as the setting and WM\_DM\_DEINTERLACE\_INVERSETELECINE as the value.</span></span>
4.  <span data-ttu-id="09340-126">Appelez à nouveau **SetInputSetting** pour définir g \_ wszInitialPatternForInverseTelecine.</span><span class="sxs-lookup"><span data-stu-id="09340-126">Call **SetInputSetting** again to set g\_wszInitialPatternForInverseTelecine.</span></span>
5.  <span data-ttu-id="09340-127">Écrivez le fichier comme d’habitude.</span><span class="sxs-lookup"><span data-stu-id="09340-127">Write the file as usual.</span></span>

## <a name="related-topics"></a><span data-ttu-id="09340-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="09340-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09340-129">**Rubriques avancées**</span><span class="sxs-lookup"><span data-stu-id="09340-129">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="09340-130">**Interface IWMWriter**</span><span class="sxs-lookup"><span data-stu-id="09340-130">**IWMWriter Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[<span data-ttu-id="09340-131">**Interface IWMWriterAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="09340-131">**IWMWriterAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2)
</dt> </dl>

 

 




