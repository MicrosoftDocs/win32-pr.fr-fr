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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369332"
---
# <a name="using-playsound-to-play-waveform-audio-files"></a>Utilisation de PlaySound pour lire des fichiers Waveform-Audio

La plupart des fichiers audio Waveform utilisent le. Extension de nom de fichier WAV.

L’instruction suivante lit les \\ \\ cloches C :. Fichier WAV :


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_SYNC); 
```



Si le fichier spécifié n’existe pas, ou si le fichier ne tient pas dans la mémoire disponible, [**PlaySound**](/previous-versions//dd743680(v=vs.85)) lit le son système par défaut. Si aucun son du système par défaut n’a été défini, **PlaySound** échoue sans produire de son. Si vous ne souhaitez pas que le son du système par défaut soit lu, spécifiez l' \_ indicateur SND NODEFAULT, comme indiqué dans l’exemple suivant :


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_SYNC | SND_NODEFAULT); 
```



 

 