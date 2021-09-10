---
title: Mise en forme de la capture audio
description: Mise en forme de la capture audio
ms.assetid: 3bbe34a6-8fd6-4780-b5af-fcf3d34ef701
keywords:
- capSetAudioFormat macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5f53553804aab401a9c2a4ada5dc9ee39170269
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124367831"
---
# <a name="formatting-audio-capture"></a>Mise en forme de la capture audio

L’exemple suivant utilise [**capSetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) pour définir le format audio sur PCM 8-kHz PCM 8 bits, stéréo.


```C++
WAVEFORMATEX wfex;

wfex.wFormatTag = WAVE_FORMAT_PCM;
wfex.nChannels = 2;                // Use stereo
wfex.nSamplesPerSec = 11025;
wfex.nAvgBytesPerSec = 22050;
wfex.nBlockAlign = 2;
wfex.wBitsPerSample = 8;
wfex.cbSize = 0;

capSetAudioFormat(hWndC, &wfex, sizeof(WAVEFORMATEX)); 
 
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la capture vidéo](using-video-capture.md)
</dt> </dl>

 

 




