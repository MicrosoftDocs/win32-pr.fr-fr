---
description: Cette rubrique vous montre comment utiliser un effet créé avec l’API XAPO dans une chaîne d’effet XAudio2.
ms.assetid: d4d24177-25eb-13ca-0e38-0c876a273e0d
title: 'Procédure : Utiliser un XAPO dans XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 780e0ba59b5032ddc01b2709f1f3e9c5a0fcce1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514862"
---
# <a name="how-to-use-an-xapo-in-xaudio2"></a>Procédure : Utiliser un XAPO dans XAudio2

Cette rubrique vous montre comment utiliser un effet créé avec l’API XAPO dans une chaîne d’effet XAudio2.

1.  Créez le XAPO comme décrit dans [How to : Create a XAPO](how-to--create-an-xapo.md).

    Vous pouvez également implémenter des fonctionnalités de paramètre au moment de l’exécution, comme décrit dans [Comment : ajouter la prise en charge des paramètres d’exécution à un XAPO](how-to--add-run-time-parameter-support-to-an-xapo.md).

2.  Créez une instance de XAPO.

    ```
    IUnknown * pXAPO;
    pXAPO = new SimpleXAPO();
    ```

    

3.  Remplir une structure de [**\_ \_ descripteur d’effet XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) avec des données.

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

4.  Remplir une structure de [**\_ \_ chaîne d’effet XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) avec des données.

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

5.  Appliquez la chaîne d’effet à une voix XAudio2 avec la fonction [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) .

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

    > [!Note]  
    > Une chaîne d’effet peut également être appliquée à une voix lorsque la voix est créée en passant la chaîne en tant que paramètre à [**IXAudio2 :: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2 :: CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice)ou [**IXAudio2 :: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).

     

6.  Libérer l’effet avec IUnknown :: Release.

    Lorsque vous créez un XAPO, il aura un nombre de références de 1. Lorsque XAPO est passé à XAudio2 avec [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 incrémente le décompte de références sur le XAPO. Le fait de libérer la référence du client au XAPO permet à XAudio2 de prendre possession du XAPO. Si XAudio2 a la seule référence à XAPO, il sera supprimé lorsqu’il n’est plus utilisé par XAudio2. Si le code client doit conserver une référence à XAPO pour une réutilisation ultérieure, par exemple, vous devez ignorer cette étape.

    ```
    pXAPO->Release();
    ```

    

7.  Renseignez la structure de paramètre, le cas échéant, associée à l’effet. Dans ce cas, pourcentage de la puissance totale à laquelle l’effet doit être appliqué.

    ```
    XAPO_PARAMETERS XAPOParameters;
    XAPOParameters.Level = 0.75;
    ```

    

8.  Transmettez la structure du paramètre Effect à l’effet en appelant la fonction [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) sur la voix à laquelle l’effet est attaché.

    ```
    hr = pVoice->SetEffectParameters( 0, &XAPOParameters, sizeof( XAPO_PARAMETERS ) );
    ```

    

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Effets audio](audio-effects.md)
</dt> <dt>

[Présentation de XAPO](xapo-overview.md)
</dt> <dt>

[Guide de programmation XAudio2](programming-guide.md)
</dt> </dl>

 

 
