---
description: Cette rubrique vous montre comment modifier le volume d’une voix au niveau global, à chaque canal de sortie, ou entre chaque canal d’une voix et une autre voix dans son sendlist.
ms.assetid: 40004128-4abb-4bcd-fe76-91276be8abec
title: 'Comment : modifier le volume vocal'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a307c5585e56fb6dc4dbdc40386c6844607498ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757695"
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

 

 
