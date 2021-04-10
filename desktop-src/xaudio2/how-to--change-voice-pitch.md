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
# <a name="how-to-change-voice-pitch"></a>Comment : modifier la tonalité des voix

Cette rubrique montre comment vous pouvez augmenter ou diminuer le pas de données audio en modifiant son taux de lecture à l’aide de la fonction [**SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) sur une voix source.

## <a name="to-change-the-pitch-of-a-source-voice"></a>Pour modifier la hauteur d’une voix source

1.  Déterminez le rapport de fréquence souhaité pour la [**voix source**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice).

    Pour plus d’informations sur le calcul du rapport de fréquence [, voir contrôle du volume et](xaudio2-volume-and-pitch-control.md) de la hauteur de XAudio2.

    ```
    float frequencyRatio = sourceRate / targetRate;
    ```

    

2.  Utilisez la fonction [**SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) pour définir le rapport de fréquence de la voix source.

    ```
    pSourceVoice->SetFrequencyRatio(frequencyRatio);
    ```

    

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation XAudio2](programming-guide.md)
</dt> <dt>

[Procédure : créer un graphique de traitement audio de base](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Contrôle du volume et du tangage XAudio2](volume-and-pitch-control.md)
</dt> </dl>

 

 
