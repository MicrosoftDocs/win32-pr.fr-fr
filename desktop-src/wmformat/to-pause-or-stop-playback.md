---
title: Pour suspendre ou arrêter la lecture
description: Pour suspendre ou arrêter la lecture
ms.assetid: 8e43ea80-36c7-4530-8ed3-dfdb64a3a2e3
keywords:
- ASF (Advanced Systems Format), suspension de la lecture
- ASF (format de systèmes avancés), suspension de la lecture
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), arrêt de la lecture
- ASF (format des systèmes avancés), arrêt de la lecture
- ASF (Advanced Systems Format), lecture suspendue ou arrêtée
- ASF (format avancé des systèmes), lecture en suspens ou en cours d’arrêt
- lecteurs asynchrones, suspension de la lecture
- lecteurs asynchrones, arrêt de la lecture
- lecteurs asynchrones, lecture suspendue ou arrêtée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728ce4c58f9198f605764d0f19d0d5f55c7f6c6b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104507787"
---
# <a name="to-pause-or-stop-playback"></a><span data-ttu-id="f3f72-114">Pour suspendre ou arrêter la lecture</span><span class="sxs-lookup"><span data-stu-id="f3f72-114">To Pause or Stop Playback</span></span>

<span data-ttu-id="f3f72-115">Quand vous appelez [**IWMReader :: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) pour commencer à lire un fichier, le lecteur asynchrone continue le traitement dans ses propres threads distincts jusqu’à ce que la fin du fichier soit atteinte.</span><span class="sxs-lookup"><span data-stu-id="f3f72-115">When you call [**IWMReader::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) to begin playing a file, the asynchronous reader will continue processing in its own separate threads until the end of the file is reached.</span></span> <span data-ttu-id="f3f72-116">Vous pouvez suspendre ou arrêter la remise des exemples à l’aide des méthodes [**IWMReader ::P ause**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-pause) ou [**IWMReader :: Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop) , respectivement.</span><span class="sxs-lookup"><span data-stu-id="f3f72-116">You can pause or stop the delivery of samples using the [**IWMReader::Pause**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-pause) or [**IWMReader::Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop) methods respectively.</span></span>

## <a name="pausing"></a><span data-ttu-id="f3f72-117">Suspension en cours</span><span class="sxs-lookup"><span data-stu-id="f3f72-117">Pausing</span></span>

<span data-ttu-id="f3f72-118">Quand vous appelez **IWMReader ::P ause** pour suspendre la lecture d’un fichier, le lecteur effectue le suivi de la position actuelle dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="f3f72-118">When you call **IWMReader::Pause** to pause playback of a file, the reader keeps track of the current position in the file.</span></span> <span data-ttu-id="f3f72-119">Pour reprendre la diffusion après une pause, appelez [**IWMReader :: Resume**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-resume).</span><span class="sxs-lookup"><span data-stu-id="f3f72-119">To resume playing after pausing, call [**IWMReader::Resume**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-resume).</span></span> <span data-ttu-id="f3f72-120">La lecture reprendra à partir du point où elle a été suspendue.</span><span class="sxs-lookup"><span data-stu-id="f3f72-120">Playback will resume from the point at which it paused.</span></span>

## <a name="stopping"></a><span data-ttu-id="f3f72-121">En cours d’arrêt</span><span class="sxs-lookup"><span data-stu-id="f3f72-121">Stopping</span></span>

<span data-ttu-id="f3f72-122">Quand vous appelez **IWMReader :: Stop** pour arrêter la lecture d’un fichier, le lecteur n’effectue pas le suivi des informations sur la progression de la lecture.</span><span class="sxs-lookup"><span data-stu-id="f3f72-122">When you call **IWMReader::Stop** to halt playback of a file, the reader does not keep track of any information about the progress of playback.</span></span> <span data-ttu-id="f3f72-123">Pour utiliser **Stop** , puis revenir au point d’arrêt, vous devez enregistrer l’heure de présentation du dernier exemple livré et l’utiliser dans votre appel à **IWMReader :: Start**.</span><span class="sxs-lookup"><span data-stu-id="f3f72-123">To use **Stop** and later return to the stopping point you must save the presentation time of the last sample delivered and use it in your call to **IWMReader::Start**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3f72-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f3f72-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3f72-125">**Interface IWMReader**</span><span class="sxs-lookup"><span data-stu-id="f3f72-125">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="f3f72-126">**Lecture des fichiers avec le lecteur asynchrone**</span><span class="sxs-lookup"><span data-stu-id="f3f72-126">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




