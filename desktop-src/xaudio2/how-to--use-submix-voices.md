---
description: Cette rubrique vous montre comment définir des groupes de voix pour envoyer leur sortie à la même voix de mixage. Cela permet d’effectuer une seule modification sur une voix de mixage secondaire pour affecter un groupe entier de voix.
ms.assetid: 76c1c138-4846-9c4f-7875-446867436ee9
title: 'Procédure : utiliser des voix prémixées'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 688a190bcf105945c3b596960083d850955d2b9f59bb6a991dfb6d120bd7b713
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005819"
---
# <a name="how-to-use-submix-voices"></a>Procédure : utiliser des voix prémixées

Cette rubrique vous montre comment définir des groupes de voix pour envoyer leur sortie à la même voix de mixage. Cela permet d’effectuer une seule modification sur une voix de mixage secondaire pour affecter un groupe entier de voix.

1.  Créez une [**voix de mixage secondaire**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) à laquelle toutes les voix des effets sonores du jeu sont envoyées.
    ```
    IXAudio2SubmixVoice * pSFXSubmixVoice;
    pXAudio2->CreateSubmixVoice(&pSFXSubmixVoice,1,44100,0,0,0,0);
    ```

    

2.  Créer une [**XAUDIO2 \_ Voice \_ envoie**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) une structure qui contient une référence à la voix du mixage secondaire.
    ```
    XAUDIO2_SEND_DESCRIPTOR SFXSend = {0, pSFXSubmixVoice};
    XAUDIO2_VOICE_SENDS SFXSendList = {1, &SFXSend};
    ```

    

3.  Transmettez la [**XAUDIO2 \_ Voice \_ envoie**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) une structure aux nouvelles voix source au fur et à mesure de leur création.
    ```
    IXAudio2SourceVoice* pSFXSourceVoice;
    if( FAILED(hr = pXaudio2->CreateSourceVoice( &pSFXSourceVoice, (WAVEFORMATEX*)&wfx,
        0, XAUDIO2_DEFAULT_FREQ_RATIO, pCallback, pSFXSendList, NULL ) ) )
        return hr;
    ```

    

4.  Appliquez les modifications à toutes les voix des effets sonores en réglant la voix du mixage secondaire.

    Dans cet exemple, la modification du volume de la voix de mixage secondaire avec la fonction [**setVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) modifie efficacement le volume de toutes les voix qui lui sont produites.

    ```
    pSFXSubmixVoice->SetVolume(0.1);
    ```

    

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Voix](voices.md)
</dt> <dt>

[Guide de programmation XAudio2](programming-guide.md)
</dt> <dt>

[Procédure : créer un graphique de traitement audio de base](how-to--build-a-basic-audio-processing-graph.md)
</dt> </dl>

 

 
