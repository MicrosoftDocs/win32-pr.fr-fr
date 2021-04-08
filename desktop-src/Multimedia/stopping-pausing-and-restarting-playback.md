---
title: Arrêt, suspension et redémarrage de la lecture
description: Arrêt, suspension et redémarrage de la lecture
ms.assetid: 39751342-63bc-4e68-bf9e-38665db8a05c
keywords:
- Wave audio, arrêt de la lecture
- Waveform-interface audio, arrêt de la lecture
- lecture des fichiers Waveform-Audio, arrêt de la lecture
- Wave audio, suspension de la lecture
- Waveform-interface audio, suspension de la lecture
- lecture de fichiers Waveform-Audio, suspension de la lecture
- audio Wave, redémarrage de la lecture
- Wave-interface audio, redémarrage de la lecture
- lecture de fichiers wave-audio, redémarrage de la lecture
- waveOutPause fonction)
- waveOutReset fonction)
- waveOutRestart fonction)
- arrêt de la lecture des données Waveform
- suspension de la lecture des signaux audio
- redémarrage de la lecture Waveform-Audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6a4756a08317923056114259588a95bc62e97f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101492"
---
# <a name="stopping-pausing-and-restarting-playback"></a><span data-ttu-id="73c4c-118">Arrêt, suspension et redémarrage de la lecture</span><span class="sxs-lookup"><span data-stu-id="73c4c-118">Stopping, Pausing, and Restarting Playback</span></span>

<span data-ttu-id="73c4c-119">Vous pouvez arrêter ou suspendre la lecture pendant la lecture de l’audio Wave.</span><span class="sxs-lookup"><span data-stu-id="73c4c-119">You can stop or pause playback while waveform audio is playing.</span></span> <span data-ttu-id="73c4c-120">Une fois la lecture suspendue, vous pouvez la redémarrer.</span><span class="sxs-lookup"><span data-stu-id="73c4c-120">After playback has been paused, you can restart it.</span></span> <span data-ttu-id="73c4c-121">Windows fournit les fonctions suivantes pour contrôler la lecture des signaux Wave-audio.</span><span class="sxs-lookup"><span data-stu-id="73c4c-121">Windows provides the following functions for controlling waveform-audio playback.</span></span>



| <span data-ttu-id="73c4c-122">Fonction</span><span class="sxs-lookup"><span data-stu-id="73c4c-122">Function</span></span>                                 | <span data-ttu-id="73c4c-123">Description</span><span class="sxs-lookup"><span data-stu-id="73c4c-123">Description</span></span>                                                                                 |
|------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="73c4c-124">**waveOutPause**</span><span class="sxs-lookup"><span data-stu-id="73c4c-124">**waveOutPause**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause)     | <span data-ttu-id="73c4c-125">Suspend la lecture sur un appareil de sortie Waveform-Audio.</span><span class="sxs-lookup"><span data-stu-id="73c4c-125">Pauses playback on a waveform-audio output device.</span></span>                                          |
| [<span data-ttu-id="73c4c-126">**waveOutReset**</span><span class="sxs-lookup"><span data-stu-id="73c4c-126">**waveOutReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)     | <span data-ttu-id="73c4c-127">Arrête la lecture sur un périphérique de sortie Waveform-Audio et marque tous les blocs de données en attente comme terminés.</span><span class="sxs-lookup"><span data-stu-id="73c4c-127">Stops playback on a waveform-audio output device and marks all pending data blocks as done.</span></span> |
| [<span data-ttu-id="73c4c-128">**waveOutRestart**</span><span class="sxs-lookup"><span data-stu-id="73c4c-128">**waveOutRestart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart) | <span data-ttu-id="73c4c-129">Reprend la lecture sur un appareil de sortie Waveform-Audio suspendu.</span><span class="sxs-lookup"><span data-stu-id="73c4c-129">Resumes playback on a paused waveform-audio output device.</span></span>                                  |



 

<span data-ttu-id="73c4c-130">La suspension d’un périphérique Wave-audio à l’aide de [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause) peut ne pas être instantanée. le pilote peut terminer la lecture du bloc actuel avant la suspension de la lecture.</span><span class="sxs-lookup"><span data-stu-id="73c4c-130">Pausing a waveform-audio device by using [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause) might not be instantaneous; the driver may finish playing the current block before pausing playback.</span></span>

<span data-ttu-id="73c4c-131">En général, dès que le premier bloc de données Waveform Audio est envoyé à l’aide de la fonction [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) , le périphérique Waveform-Audio commence à fonctionner.</span><span class="sxs-lookup"><span data-stu-id="73c4c-131">Generally, as soon as the first waveform-audio data block is sent by using the [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) function, the waveform-audio device begins playing.</span></span> <span data-ttu-id="73c4c-132">Si vous ne souhaitez pas que le son commence immédiatement, appelez **waveOutPause** avant d’appeler **waveOutWrite**.</span><span class="sxs-lookup"><span data-stu-id="73c4c-132">If you do not want the sound to start playing immediately, call **waveOutPause** before calling **waveOutWrite**.</span></span> <span data-ttu-id="73c4c-133">Ensuite, lorsque vous souhaitez commencer à émettre des données Waveform-Audio, appelez [**waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart).</span><span class="sxs-lookup"><span data-stu-id="73c4c-133">Then, when you want to begin playing waveform-audio data, call [**waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart).</span></span>

<span data-ttu-id="73c4c-134">Vous ne pouvez pas utiliser **waveOutRestart** pour redémarrer un appareil qui a été arrêté avec [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset); vous devez utiliser **waveOutWrite** pour envoyer le premier bloc de données afin de reprendre la lecture sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="73c4c-134">You cannot use **waveOutRestart** to restart a device that has been stopped with [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset); you must use **waveOutWrite** to send the first data block to resume playback on the device.</span></span>

 

 