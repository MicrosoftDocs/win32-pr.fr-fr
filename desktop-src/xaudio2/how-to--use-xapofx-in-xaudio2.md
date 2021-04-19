---
description: Cette rubrique vous montre comment utiliser l’un des effets inclus dans XAPOFX dans une chaîne d’effet XAudio2.
ms.assetid: dc325584-13f7-231a-e0c7-17f38d54ae11
title: 'Procédure : utiliser un XAPOFX dans XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b0bb4cbeabb38f408d9102a2534634e8eed7cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516696"
---
# <a name="how-to-use-xapofx-in-xaudio2"></a>Procédure : utiliser un XAPOFX dans XAudio2

Cette rubrique vous montre comment utiliser l’un des effets inclus dans XAPOFX dans une chaîne d’effet XAudio2.

## <a name="to-use-an-effect-from-xapofx-in-an-xaudio2-effect-chain"></a>Pour utiliser un effet à partir de XAPOFX dans une chaîne d’effet XAudio2

1.  Créez l’effet en passant le CLSID d’un effet XAPOFX à la fonction [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) .

    Dans ce cas, l’effet de réverbération simplifié FXReverb est créé.

    ```
    IUnknown * pXAPO;
    CreateFX(__uuidof(FXReverb),&pXAPO);
    ```

    

2.  Remplir une structure de [**\_ \_ descripteur d’effet XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) avec des données.

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

3.  Remplir une structure de [**\_ \_ chaîne d’effet XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) avec des données.

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

4.  Appliquez la chaîne d’effet à une voix XAudio2 avec la fonction [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) .

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

    > [!Note]  
    > Vous pouvez également appliquer une chaîne d’effet à une voix quand vous créez la voix en passant la chaîne en tant que paramètre à [**IXAudio2 :: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2 :: CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice)ou [**IXAudio2 :: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).

     

5.  Libérer l’effet avec IUnknown :: Release. Lorsque vous créez un XAPO, il aura un nombre de références de 1. Lorsque XAPO est passé à XAudio2 avec [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 incrémente le décompte de références sur le XAPO. Le fait de libérer la référence du client au XAPO permet à XAudio2 de prendre possession du XAPO. Si XAudio2 a la seule référence à XAPO, cette référence est supprimée lorsqu’elle n’est plus utilisée par XAudio2. Si le code client doit conserver une référence à XAPO, par exemple, pour une réutilisation ultérieure, vous pouvez ignorer cette étape.

    ```
    pXAPO->Release();
    ```

    

6.  Renseignez la structure de paramètre, le cas échéant, associée à l’effet.

    Dans ce cas, la structure de [**\_ paramètres FXREVERB**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters) est utilisée pour définir la diffusion et la taille de la salle que l’effet de réverbération doit utiliser.

    ```
    FXREVERB_PARAMETERS XAPOParameters;
    XAPOParameters.Diffusion = FXREVERB_DEFAULT_DIFFUSION;
    XAPOParameters.RoomSize = FXREVERB_DEFAULT_ROOMSIZE;
    ```

    

7.  Transmettez la structure du paramètre Effect à l’effet en appelant la fonction [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) sur la voix à laquelle l’effet est attaché.

    ```
    hr = pVoice->SetEffectParameters( 0, &XAPOParameters, sizeof( FXREVERB_PARAMETERS ) );
    ```

    

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Effets audio](audio-effects.md)
</dt> <dt>

[Guide de programmation XAudio2](programming-guide.md)
</dt> </dl>

 

 
