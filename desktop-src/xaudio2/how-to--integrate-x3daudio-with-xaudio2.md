---
description: Cette rubrique montre comment intégrer X3DAudio à XAudio2.
ms.assetid: a8f41f0d-b284-aefa-923b-471b13b4a3ec
title: 'Procédure : intégrer X3DAudio avec XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dc54fa5f673e319712808ca6d2b587b8ad2d0fc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127225505"
---
# <a name="how-to-integrate-x3daudio-with-xaudio2"></a>Procédure : intégrer X3DAudio avec XAudio2

Cette rubrique montre comment intégrer X3DAudio à XAudio2. Vous pouvez utiliser X3DAudio pour fournir les valeurs de volume et de tangage pour XAudio2 Voices et les paramètres de l’effet de réverbération intégré à XAudio2. Cette rubrique suppose que vous avez créé un graphique audio comme décrit dans [Comment : créer un Graph de traitement audio de base](how-to--build-a-basic-audio-processing-graph.md). Si vous n’avez pas encore créé de graphique audio, [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) échoue.

**Pour initialiser X3DAudio**

1.  Initialisez X3DAudio en appelant [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize).

    La fonction [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) prend des indicateurs qui indiquent la configuration de l’orateur, la vitesse du son dans les unités universelles définies par l’utilisateur par seconde et un handle pour retourner une instance du moteur X3DAudio. Appelez [**IXAudio2MasteringVoice :: GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask) pour accéder au masque de canal du format de sortie.

    ```
    DWORD dwChannelMask;       
    pMasteringVoice->GetChannelMask( &dwChannelMask );       

    X3DAUDIO_HANDLE X3DInstance;
    X3DAudioInitialize( dwChannelMask, X3DAUDIO_SPEED_OF_SOUND, X3DInstance );
    ```

    

2.  Créez des instances de [**l' \_ écouteur X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) et des structures d' [**\_ émetteur X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) .

    La structure d' [**\_ écouteur X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) représente la position de ce qui est à l’écoute du son. En règle générale, il s’agit de la position de l’appareil photo ou d’une position proche. La structure d' [**\_ émetteur X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) représente la position de l’élément qui fait le son. Il y aura une structure d' **\_ émetteur X3DAUDIO** pour chaque son suivi.

    Les membres des structures qui ne seront pas mises à jour dans une boucle de jeu doivent être initialisés ici. La plupart des membres des structures peuvent simplement être initialisés à zéro. Toutefois, certains membres de [**l' \_ émetteur X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) doivent être configurés pour être initialisés à des valeurs non nulles. Le membre ChannelCount de l' **\_ émetteur X3DAUDIO** doit être initialisé avec le nombre de canaux dans la voix que l’émetteur représente. En outre, le membre CurveDistanceScaler de l' **\_ émetteur X3DAUDIO** doit être compris entre FLT \_ min et FLT \_ Max.

    ```
    X3DAUDIO_LISTENER Listener = {0};
    X3DAUDIO_EMITTER Emitter = {0};
    Emitter.ChannelCount = 1;
    Emitter.CurveDistanceScaler = FLT_MIN;
    ```

    

3.  Créez une instance de la structure de [**\_ \_ paramètres X3DAUDIO DSP**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) .

    La structure des [**\_ \_ paramètres X3DAUDIO DSP**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) est utilisée pour retourner les résultats calculés par [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate). La fonction **X3DAudioCalculate** n’alloue pas de mémoire pour l’un de ses paramètres. Cela signifie que vous devez allouer des tableaux pour les membres pMatrixCoefficients et pDelayTimes de la structure de **\_ \_ paramètres X3DAUDIO DSP** si vous envisagez de les utiliser. En outre, vous devez définir les membres SrcChannelCount et DstChannelCount sur le nombre de canaux dans les voix source et de destination de l’émetteur.

    ```
    X3DAUDIO_DSP_SETTINGS DSPSettings = {0};
    FLOAT32 * matrix = new FLOAT32[deviceDetails.OutputFormat.Format.nChannels];
    DSPSettings.SrcChannelCount = 1;
    DSPSettings.DstChannelCount = deviceDetails.OutputFormat.Format.nChannels;
    DSPSettings.pMatrixCoefficients = matrix;
    ```

    

    > [!Note]  
    > Utilisez [**IXAudio2Voice :: GetVoiceDetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails) sur la voix de mastérisation pour obtenir le nombre de InputChannels pour **nChannels**. pour les versions du kit de développement logiciel (SDK) DirectX de XAUDIO2 antérieures à Windows 8, utilisez IXAudio2 :: GetDeviceDetails.

     

Effectuez ces étapes une fois toutes les deux à trois frames pour calculer de nouveaux paramètres et les appliquer. Dans cet exemple, une voix source est envoyée directement à la voix de mastérisation et à une voix de mixage secondaire avec un effet de réverbération appliqué.

**Pour utiliser X3DAudio pour calculer et appliquer de nouveaux paramètres audio 3D**

1.  Mettez à jour les structures d' [**\_ écouteur X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) et d' [**\_ émetteur X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) avec leur position, vélocité et orientation actuelles.

    ```
    Emitter.OrientFront = EmitterOrientFront;
    Emitter.OrientTop = EmitterOrientTop;
    Emitter.Position = EmitterPosition;
    Emitter.Velocity = EmitterVelocity;
    Listener.OrientFront = ListenerOrientFront;
    Listener.OrientTop = ListenerOrientTop;
    Listener.Position = ListenerPosition;
    Listener.Velocity = ListenerVelocity;
    ```

    

2.  Appelez [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) pour calculer les nouveaux paramètres des voix.

    Les paramètres pour [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) sont l' [**\_ écouteur X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) et les structures [**d' \_ émetteur de X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) mis à jour. Les indicateurs indiquent les valeurs que **X3DAudioCalculate** doit calculer, et la structure de [**\_ \_ paramètres X3DAUDIO DSP**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) qui contiendra les résultats des calculs effectués.

    ```
    X3DAudioCalculate(X3DInstance, &Listener, &Emitter,
        X3DAUDIO_CALCULATE_MATRIX | X3DAUDIO_CALCULATE_DOPPLER | X3DAUDIO_CALCULATE_LPF_DIRECT | X3DAUDIO_CALCULATE_REVERB,
        &DSPSettings );
    ```

    

3.  Utilisez [**IXAudio2Voice :: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) et [**IXAudio2SourceVoice :: SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) pour appliquer les valeurs de volume et de tangage à la voix source.

    ```
    pSFXSourceVoice->SetOutputMatrix( pMasterVoice, 1, deviceDetails.OutputFormat.Format.nChannels, DSPSettings.pMatrixCoefficients ) ;
    pSFXSourceVoice->SetFrequencyRatio(DSPSettings.DopplerFactor);
    ```

    

4.  Utilisez [**IXAudio2Voice :: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) pour appliquer le niveau de réverbération calculé à la voix de mixage secondaire.

    ```
    pSFXSourceVoice->SetOutputMatrix(pSubmixVoice, 1, 1, &DSPSettings.ReverbLevel);
    ```

    

5.  Utilisez [**IXAudio2Voice :: SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters) pour appliquer le coefficient direct du filtre de passe faible calculé à la voix source.

    ```
    XAUDIO2_FILTER_PARAMETERS FilterParameters = { LowPassFilter, 2.0f * sinf(X3DAUDIO_PI/6.0f * DSPSettings.LPFDirectCoefficient), 1.0f };
    pSFXSourceVoice->SetFilterParameters(&FilterParameters);
    ```

    

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[X3DAudio](x3daudio.md)
</dt> <dt>

[Présentation de X3DAudio](x3daudio-overview.md)
</dt> <dt>

[Guide de programmation XAudio2](programming-guide.md)
</dt> <dt>

[Contrôle du volume et du tangage XAudio2](volume-and-pitch-control.md)
</dt> </dl>

 

 
