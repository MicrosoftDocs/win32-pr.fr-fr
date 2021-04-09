---
description: Cette rubrique montre comment vous pouvez appliquer une chaîne d’effet à une voix pour permettre le traitement personnalisé des données audio pour cette voix. Cette rubrique explique comment utiliser l’effet de réverbération, qui est l’un des effets XAudio2 intégrés.
ms.assetid: 4c33bd83-2654-cd6f-ea6c-bbc0d5872638
title: 'Procédure : Créer une chaîne d’effets'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85d58186b623dca04da99001a29e54cf3ecc39fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113654"
---
# <a name="how-to-create-an-effect-chain"></a>Procédure : Créer une chaîne d’effets

Cette rubrique montre comment vous pouvez appliquer une chaîne d’effet à une voix pour permettre le traitement personnalisé des données audio pour cette voix. Cette rubrique explique comment utiliser l’effet de réverbération, qui est l’un des effets XAudio2 intégrés.

## <a name="to-create-a-basic-effect-chain-that-applies-an-effect-to-a-voice"></a>Pour créer une chaîne à effet de base qui applique un effet à une voix

1.  Créez l’effet.

    Dans cet exemple, la fonction [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) crée un effet de réverbération. Consultez [effets audio XAudio2](xaudio2-audio-effects.md) pour obtenir la liste des sources d’effets possibles à utiliser avec XAudio2.

    ```
    IUnknown * pXAPO;
    hr = XAudio2CreateReverb(&pXAPO);
    ```

    

2.  Remplir une structure de [**\_ \_ descripteur d’effet XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) avec des données.

    S’il y a plusieurs effets dans la chaîne, chaque effet nécessite une structure de [**\_ \_ descripteur d’effet XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) .

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

3.  Remplir une structure de [**\_ \_ chaîne d’effet XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) avec des données. Dans ce cas, la chaîne n’a qu’un seul effet. Si la chaîne a plusieurs effets, le membre EffectCount contiendra le nombre d’effets et le membre pEffectDescriptors pointera vers un tableau de \_ \_ structures de descripteur d’effet XAUDIO2.

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

4.  Appliquez la chaîne d’effet à une voix avec la fonction [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) .

    Vous pouvez appliquer des chaînes d’effet aux voix principales, aux voix source et aux voix de mixage secondaire.

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

5.  Libérer l’effet avec IUnknown :: Release.

    Lorsque vous créez un XAPO, il aura un nombre de références de 1. Lorsque XAPO est passé à XAudio2 avec [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 incrémente le décompte de références sur le XAPO. Le fait de libérer la référence du client au XAPO permet à XAudio2 de prendre possession du XAPO. Si XAudio2 a la seule référence à XAPO, il sera supprimé lorsqu’il n’est plus utilisé par XAudio2. Si le code client doit conserver une référence à XAPO, par exemple pour une réutilisation ultérieure, vous devez ignorer cette étape.

    ```
    pXAPO->Release();
    ```

    

6.  Renseignez la structure de paramètre, le cas échéant, associée à l’effet. L’effet de réverbération utilise une structure de [**\_ \_ paramètres de réverbération XAUDIO2FX**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters) .

    ```
    XAUDIO2FX_REVERB_PARAMETERS reverbParameters;
    reverbParameters.ReflectionsDelay = XAUDIO2FX_REVERB_DEFAULT_REFLECTIONS_DELAY;
    reverbParameters.ReverbDelay = XAUDIO2FX_REVERB_DEFAULT_REVERB_DELAY;
    reverbParameters.RearDelay = XAUDIO2FX_REVERB_DEFAULT_REAR_DELAY;
    reverbParameters.PositionLeft = XAUDIO2FX_REVERB_DEFAULT_POSITION;
    reverbParameters.PositionRight = XAUDIO2FX_REVERB_DEFAULT_POSITION;
    reverbParameters.PositionMatrixLeft = XAUDIO2FX_REVERB_DEFAULT_POSITION_MATRIX;
    reverbParameters.PositionMatrixRight = XAUDIO2FX_REVERB_DEFAULT_POSITION_MATRIX;
    reverbParameters.EarlyDiffusion = XAUDIO2FX_REVERB_DEFAULT_EARLY_DIFFUSION;
    reverbParameters.LateDiffusion = XAUDIO2FX_REVERB_DEFAULT_LATE_DIFFUSION;
    reverbParameters.LowEQGain = XAUDIO2FX_REVERB_DEFAULT_LOW_EQ_GAIN;
    reverbParameters.LowEQCutoff = XAUDIO2FX_REVERB_DEFAULT_LOW_EQ_CUTOFF;
    reverbParameters.HighEQGain = XAUDIO2FX_REVERB_DEFAULT_HIGH_EQ_GAIN;
    reverbParameters.HighEQCutoff = XAUDIO2FX_REVERB_DEFAULT_HIGH_EQ_CUTOFF;
    reverbParameters.RoomFilterFreq = XAUDIO2FX_REVERB_DEFAULT_ROOM_FILTER_FREQ;
    reverbParameters.RoomFilterMain = XAUDIO2FX_REVERB_DEFAULT_ROOM_FILTER_MAIN;
    reverbParameters.RoomFilterHF = XAUDIO2FX_REVERB_DEFAULT_ROOM_FILTER_HF;
    reverbParameters.ReflectionsGain = XAUDIO2FX_REVERB_DEFAULT_REFLECTIONS_GAIN;
    reverbParameters.ReverbGain = XAUDIO2FX_REVERB_DEFAULT_REVERB_GAIN;
    reverbParameters.DecayTime = XAUDIO2FX_REVERB_DEFAULT_DECAY_TIME;
    reverbParameters.Density = XAUDIO2FX_REVERB_DEFAULT_DENSITY;
    reverbParameters.RoomSize = XAUDIO2FX_REVERB_DEFAULT_ROOM_SIZE;
    reverbParameters.WetDryMix = XAUDIO2FX_REVERB_DEFAULT_WET_DRY_MIX;
    ```

    

7.  Transmettez la structure du paramètre Effect à l’effet en appelant la fonction [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) sur la voix à laquelle l’effet est attaché.

    ```
    hr = pVoice->SetEffectParameters( 0, &reverbParameters, sizeof( reverbParameters ) );
    ```

    

8.  Désactivez ou activez l’effet, le cas échéant.

    Vous pouvez utiliser [**DisableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) à tout moment pour désactiver un effet.

    ```
    pVoice->DisableEffect(0);
    ```

    

    Vous pouvez réactiver un effet avec [**EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect).

    ```
    pVoice->EnableEffect(0);
    ```

    

    Les paramètres pour [**DisableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) et [**EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect) spécifient l’effet de la chaîne à activer ou désactiver.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Effets audio](audio-effects.md)
</dt> <dt>

[Guide de programmation XAudio2](programming-guide.md)
</dt> <dt>

[Procédure : créer un graphique de traitement audio de base](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Présentation de XAPO](xapo-overview.md)
</dt> <dt>

[Comment : utiliser XAOPFX dans XAudio2](how-to--use-xapofx-in-xaudio2.md)
</dt> <dt>

[Comment : utiliser un XAOP dans XAudio2](how-to--use-an-xapo-in-xaudio2.md)
</dt> </dl>

 

 
