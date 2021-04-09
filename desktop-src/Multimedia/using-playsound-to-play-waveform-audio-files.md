---
title: Utilisation de PlaySound pour lire des fichiers Waveform-Audio
description: Utilisation de PlaySound pour lire des fichiers Waveform-Audio
ms.assetid: 8b7d191b-6b0c-4dff-84de-cb3a5c314b80
keywords:
- Wave audio, fonction PlaySound
- sons Waveform, fichiers de lecture
- Wave audio, extension de nom de fichier WAV
- PlaySound, fonction, lecture de fichiers audio Waveform
- lecture de fichiers Waveform-Audio, fonction PlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9d5dde46827b7892217f760c749e75e19f368f5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940984"
---
# <a name="using-playsound-to-play-waveform-audio-files"></a><span data-ttu-id="f7aa7-108">Utilisation de PlaySound pour lire des fichiers Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="f7aa7-108">Using PlaySound to Play Waveform-Audio Files</span></span>

<span data-ttu-id="f7aa7-109">La plupart des fichiers audio Waveform utilisent le. Extension de nom de fichier WAV.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-109">Most waveform-audio files use the .WAV filename extension.</span></span>

<span data-ttu-id="f7aa7-110">L’instruction suivante lit les \\ \\ cloches C :. Fichier WAV :</span><span class="sxs-lookup"><span data-stu-id="f7aa7-110">The following statement plays the C:\\SOUNDS\\BELLS.WAV file:</span></span>


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_SYNC); 
```



<span data-ttu-id="f7aa7-111">Si le fichier spécifié n’existe pas, ou si le fichier ne tient pas dans la mémoire disponible, [**PlaySound**](/previous-versions//dd743680(v=vs.85)) lit le son système par défaut.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-111">If the specified file does not exist, or if the file does not fit into the available memory, [**PlaySound**](/previous-versions//dd743680(v=vs.85)) plays the default system sound.</span></span> <span data-ttu-id="f7aa7-112">Si aucun son du système par défaut n’a été défini, **PlaySound** échoue sans produire de son.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-112">If no default system sound has been defined, **PlaySound** fails without producing any sound.</span></span> <span data-ttu-id="f7aa7-113">Si vous ne souhaitez pas que le son du système par défaut soit lu, spécifiez l' \_ indicateur SND NODEFAULT, comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="f7aa7-113">If you do not want the default system sound to play, specify the SND\_NODEFAULT flag, as shown in the following example:</span></span>


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_SYNC | SND_NODEFAULT); 
```



 

 