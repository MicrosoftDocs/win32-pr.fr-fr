---
description: Cette rubrique vous montre comment modifier le volume d’une voix au niveau global, à chaque canal de sortie, ou entre chaque canal d’une voix et une autre voix dans son sendlist.
ms.assetid: 40004128-4abb-4bcd-fe76-91276be8abec
title: 'Comment : modifier le volume vocal'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab433cc0e5c0e3ddc4bea3c58f49afae36cf8833fa8f003c99f1c45b237c70a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118696256"
---
# <a name="how-to-change-voice-volume"></a>Comment : modifier le volume vocal

Cette rubrique vous montre comment modifier le volume d’une voix au niveau global, à chaque canal de sortie, ou entre chaque canal d’une voix et une autre voix dans son [**sendlist**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends).

## <a name="to-set-an-overall-volume-level-for-the-voices-input"></a>Pour définir un niveau de volume global pour l’entrée de la voix

-   Utilisez la fonction [**setVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) .

    ```
    pSourceVoice->SetVolume(1.0);
    ```

    

## <a name="to-set-the-volume-of-the-voices-output-channels"></a>Pour définir le volume des canaux de sortie de la voix

1.  Créez un tableau de nombres à virgule flottante qui contiennent les volumes souhaités de tous les canaux de sortie de la voix.

    Le tableau aura une entrée pour chaque canal de la voix.

    ```
    float SourceVoiceChannelVolumes[1] = {1.0};
    ```

    

2.  Utilisez la fonction [**SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes) pour définir le volume des canaux de sortie.

    ```
    hr = pSourceVoice->SetChannelVolumes(1,SourceVoiceChannelVolumes);
    ```

    

## <a name="to-set-the-volume-of-connections"></a>Pour définir le volume des connexions

Définissez le volume de connexion entre la voix et une voix dans son [**sendlist**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends).

1.  Créez un tableau de nombres à virgule flottante qui définit une matrice de sortie si la voix envoie à une autre voix.

    > [!Note]  
    > Le tableau doit avoir un nombre d’entrées égal aux canaux vocaux source × canaux vocaux de destination. Dans cet exemple, le mappage provient d’une voix avec un canal vers une voix avec deux canaux.

     

    ```
    float outputMatrix[2] = {1.0f,0.05f};
    ```

    

2.  Utilisez la fonction [**SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) pour définir la matrice de sortie.

    ```
    pSourceVoice->SetOutputMatrix(pSubmixVoice,1,2,outputMatrix);
    ```

    

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation XAudio2](programming-guide.md)
</dt> <dt>

[Procédure : créer un graphique de traitement audio de base](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Contrôle du volume et du tangage XAudio2](volume-and-pitch-control.md)
</dt> </dl>

 

 
