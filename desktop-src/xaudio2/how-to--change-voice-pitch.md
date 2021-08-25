---
description: Cette rubrique montre comment vous pouvez augmenter ou diminuer le pas de données audio en modifiant son taux de lecture à l’aide de la fonction SetFrequencyRatio sur une voix source.
ms.assetid: 93408116-1c1f-307f-7e1f-090f2663ff0b
title: 'Comment : modifier la tonalité des voix'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc44fe757c563e3556f760ead594bb619da9f62fb2c3eafc774e15d7b9e5bc85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926469"
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

 

 
