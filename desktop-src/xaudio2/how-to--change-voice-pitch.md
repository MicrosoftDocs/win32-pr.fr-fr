---
description: Cette rubrique montre comment vous pouvez augmenter ou diminuer le pas de données audio en modifiant son taux de lecture à l’aide de la fonction SetFrequencyRatio sur une voix source.
ms.assetid: 93408116-1c1f-307f-7e1f-090f2663ff0b
title: 'Comment : modifier la tonalité des voix'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7143dda30eae48bd8ed966c4170da2884d2633ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113655"
---
# <a name="how-to-change-voice-pitch"></a><span data-ttu-id="2911d-103">Comment : modifier la tonalité des voix</span><span class="sxs-lookup"><span data-stu-id="2911d-103">How to: Change Voice Pitch</span></span>

<span data-ttu-id="2911d-104">Cette rubrique montre comment vous pouvez augmenter ou diminuer le pas de données audio en modifiant son taux de lecture à l’aide de la fonction [**SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) sur une voix source.</span><span class="sxs-lookup"><span data-stu-id="2911d-104">This topic shows you how you can raise or lower the pitch of audio data by changing its rate of playback using the [**SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) function on a source voice.</span></span>

## <a name="to-change-the-pitch-of-a-source-voice"></a><span data-ttu-id="2911d-105">Pour modifier la hauteur d’une voix source</span><span class="sxs-lookup"><span data-stu-id="2911d-105">To change the pitch of a source voice</span></span>

1.  <span data-ttu-id="2911d-106">Déterminez le rapport de fréquence souhaité pour la [**voix source**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice).</span><span class="sxs-lookup"><span data-stu-id="2911d-106">Determine the desired frequency ratio for the [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice).</span></span>

    <span data-ttu-id="2911d-107">Pour plus d’informations sur le calcul du rapport de fréquence [, voir contrôle du volume et](xaudio2-volume-and-pitch-control.md) de la hauteur de XAudio2.</span><span class="sxs-lookup"><span data-stu-id="2911d-107">See [XAudio2 Volume and Pitch Control](xaudio2-volume-and-pitch-control.md) for more information about calculating the frequency ratio.</span></span>

    ```
    float frequencyRatio = sourceRate / targetRate;
    ```

    

2.  <span data-ttu-id="2911d-108">Utilisez la fonction [**SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) pour définir le rapport de fréquence de la voix source.</span><span class="sxs-lookup"><span data-stu-id="2911d-108">Use the [**SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) function to set the frequency ratio of the source voice.</span></span>

    ```
    pSourceVoice->SetFrequencyRatio(frequencyRatio);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="2911d-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2911d-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2911d-110">Guide de programmation XAudio2</span><span class="sxs-lookup"><span data-stu-id="2911d-110">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="2911d-111">Procédure : créer un graphique de traitement audio de base</span><span class="sxs-lookup"><span data-stu-id="2911d-111">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="2911d-112">Contrôle du volume et du tangage XAudio2</span><span class="sxs-lookup"><span data-stu-id="2911d-112">XAudio2 Volume and Pitch Control</span></span>](volume-and-pitch-control.md)
</dt> </dl>

 

 
