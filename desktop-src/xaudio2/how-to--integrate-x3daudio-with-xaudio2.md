---
description: Cette rubrique montre comment intégrer X3DAudio à XAudio2.
ms.assetid: a8f41f0d-b284-aefa-923b-471b13b4a3ec
title: 'Procédure : intégrer X3DAudio avec XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dc54fa5f673e319712808ca6d2b587b8ad2d0fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757690"
---
# <a name="how-to-integrate-x3daudio-with-xaudio2"></a><span data-ttu-id="ffebd-103">Procédure : intégrer X3DAudio avec XAudio2</span><span class="sxs-lookup"><span data-stu-id="ffebd-103">How to: Integrate X3DAudio with XAudio2</span></span>

<span data-ttu-id="ffebd-104">Cette rubrique montre comment intégrer X3DAudio à XAudio2.</span><span class="sxs-lookup"><span data-stu-id="ffebd-104">This topic shows how to integrate X3DAudio with XAudio2.</span></span> <span data-ttu-id="ffebd-105">Vous pouvez utiliser X3DAudio pour fournir les valeurs de volume et de tangage pour XAudio2 Voices et les paramètres de l’effet de réverbération intégré à XAudio2.</span><span class="sxs-lookup"><span data-stu-id="ffebd-105">You can use X3DAudio to provide the volume and pitch values for XAudio2 voices and the parameters for the XAudio2 built in reverb effect.</span></span> <span data-ttu-id="ffebd-106">Cette rubrique suppose que vous avez créé un graphique audio comme décrit dans [Comment : générer un graphique de traitement audio de base](how-to--build-a-basic-audio-processing-graph.md).</span><span class="sxs-lookup"><span data-stu-id="ffebd-106">This topic assumes that you have created an audio graph as described in [How to: Build a Basic Audio Processing Graph](how-to--build-a-basic-audio-processing-graph.md).</span></span> <span data-ttu-id="ffebd-107">Si vous n’avez pas encore créé de graphique audio, [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) échoue.</span><span class="sxs-lookup"><span data-stu-id="ffebd-107">If you have not already created an audio graph, [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) will fail.</span></span>

<span data-ttu-id="ffebd-108">**Pour initialiser X3DAudio**</span><span class="sxs-lookup"><span data-stu-id="ffebd-108">**To initialize X3DAudio**</span></span>

1.  <span data-ttu-id="ffebd-109">Initialisez X3DAudio en appelant [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize).</span><span class="sxs-lookup"><span data-stu-id="ffebd-109">Initialize X3DAudio by calling [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize).</span></span>

    <span data-ttu-id="ffebd-110">La fonction [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) prend des indicateurs qui indiquent la configuration de l’orateur, la vitesse du son dans les unités universelles définies par l’utilisateur par seconde et un handle pour retourner une instance du moteur X3DAudio.</span><span class="sxs-lookup"><span data-stu-id="ffebd-110">The [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) function takes flags indicating the speaker setup, the speed of sound in user-defined world units per second, and a handle to return an instance of the X3DAudio engine.</span></span> <span data-ttu-id="ffebd-111">Appelez [**IXAudio2MasteringVoice :: GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask) pour accéder au masque de canal du format de sortie.</span><span class="sxs-lookup"><span data-stu-id="ffebd-111">Call [**IXAudio2MasteringVoice::GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask) to get the output format's channel mask.</span></span>

    ```
    DWORD dwChannelMask;       
    pMasteringVoice->GetChannelMask( &dwChannelMask );       

    X3DAUDIO_HANDLE X3DInstance;
    X3DAudioInitialize( dwChannelMask, X3DAUDIO_SPEED_OF_SOUND, X3DInstance );
    ```

    

2.  <span data-ttu-id="ffebd-112">Créez des instances de [**l' \_ écouteur X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) et des structures d' [**\_ émetteur X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) .</span><span class="sxs-lookup"><span data-stu-id="ffebd-112">Create instances of the [**X3DAUDIO\_LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) and [**X3DAUDIO\_EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) structures.</span></span>

    <span data-ttu-id="ffebd-113">La structure d' [**\_ écouteur X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) représente la position de ce qui est à l’écoute du son.</span><span class="sxs-lookup"><span data-stu-id="ffebd-113">The [**X3DAUDIO\_LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) structure represents the position of whatever is hearing the sound.</span></span> <span data-ttu-id="ffebd-114">En règle générale, il s’agit de la position de l’appareil photo ou d’une position proche.</span><span class="sxs-lookup"><span data-stu-id="ffebd-114">Generally, this is the position of the camera or a position close to it.</span></span> <span data-ttu-id="ffebd-115">La structure d' [**\_ émetteur X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) représente la position de l’élément qui fait le son.</span><span class="sxs-lookup"><span data-stu-id="ffebd-115">The [**X3DAUDIO\_EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) structure represents the position of the thing making the sound.</span></span> <span data-ttu-id="ffebd-116">Il y aura une structure d' **\_ émetteur X3DAUDIO** pour chaque son suivi.</span><span class="sxs-lookup"><span data-stu-id="ffebd-116">There will be one **X3DAUDIO\_EMITTER** structure for each sound that is being tracked.</span></span>

    <span data-ttu-id="ffebd-117">Les membres des structures qui ne seront pas mises à jour dans une boucle de jeu doivent être initialisés ici.</span><span class="sxs-lookup"><span data-stu-id="ffebd-117">Members of the structures that will not be updated in a game loop should be initialized here.</span></span> <span data-ttu-id="ffebd-118">La plupart des membres des structures peuvent simplement être initialisés à zéro.</span><span class="sxs-lookup"><span data-stu-id="ffebd-118">Most members of the structures can simply be initialized to zero.</span></span> <span data-ttu-id="ffebd-119">Toutefois, certains membres de [**l' \_ émetteur X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) doivent être configurés pour être initialisés à des valeurs non nulles.</span><span class="sxs-lookup"><span data-stu-id="ffebd-119">However, some members of [**X3DAUDIO\_EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) need to be set to be initialized to non-zero values.</span></span> <span data-ttu-id="ffebd-120">Le membre ChannelCount de l' **\_ émetteur X3DAUDIO** doit être initialisé avec le nombre de canaux dans la voix que l’émetteur représente.</span><span class="sxs-lookup"><span data-stu-id="ffebd-120">The ChannelCount member of the **X3DAUDIO\_EMITTER** needs to be initialized to the number of channels in the voice the emitter represents.</span></span> <span data-ttu-id="ffebd-121">En outre, le membre CurveDistanceScaler de l' **\_ émetteur X3DAUDIO** doit être compris entre FLT \_ min et FLT \_ Max.</span><span class="sxs-lookup"><span data-stu-id="ffebd-121">Also, the CurveDistanceScaler member of **X3DAUDIO\_EMITTER** must be in the range FLT\_MIN to FLT\_MAX.</span></span>

    ```
    X3DAUDIO_LISTENER Listener = {0};
    X3DAUDIO_EMITTER Emitter = {0};
    Emitter.ChannelCount = 1;
    Emitter.CurveDistanceScaler = FLT_MIN;
    ```

    

3.  <span data-ttu-id="ffebd-122">Créez une instance de la structure de [**\_ \_ paramètres X3DAUDIO DSP**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) .</span><span class="sxs-lookup"><span data-stu-id="ffebd-122">Create an instance of the [**X3DAUDIO\_DSP\_SETTINGS**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) structure.</span></span>

    <span data-ttu-id="ffebd-123">La structure des [**\_ \_ paramètres X3DAUDIO DSP**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) est utilisée pour retourner les résultats calculés par [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate).</span><span class="sxs-lookup"><span data-stu-id="ffebd-123">The [**X3DAUDIO\_DSP\_SETTINGS**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) structure is used to return results calculated by [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate).</span></span> <span data-ttu-id="ffebd-124">La fonction **X3DAudioCalculate** n’alloue pas de mémoire pour l’un de ses paramètres.</span><span class="sxs-lookup"><span data-stu-id="ffebd-124">The **X3DAudioCalculate** function does not allocate memory for any of its parameters.</span></span> <span data-ttu-id="ffebd-125">Cela signifie que vous devez allouer des tableaux pour les membres pMatrixCoefficients et pDelayTimes de la structure de **\_ \_ paramètres X3DAUDIO DSP** si vous envisagez de les utiliser.</span><span class="sxs-lookup"><span data-stu-id="ffebd-125">This means that you need to allocate arrays for the **X3DAUDIO\_DSP\_SETTINGS** structure's pMatrixCoefficients and pDelayTimes members if you intend to use them.</span></span> <span data-ttu-id="ffebd-126">En outre, vous devez définir les membres SrcChannelCount et DstChannelCount sur le nombre de canaux dans les voix source et de destination de l’émetteur.</span><span class="sxs-lookup"><span data-stu-id="ffebd-126">In addition, you need to set the SrcChannelCount and DstChannelCount members to the number of channels in the emitter's source and destination voices.</span></span>

    ```
    X3DAUDIO_DSP_SETTINGS DSPSettings = {0};
    FLOAT32 * matrix = new FLOAT32[deviceDetails.OutputFormat.Format.nChannels];
    DSPSettings.SrcChannelCount = 1;
    DSPSettings.DstChannelCount = deviceDetails.OutputFormat.Format.nChannels;
    DSPSettings.pMatrixCoefficients = matrix;
    ```

    

    > [!Note]  
    > <span data-ttu-id="ffebd-127">Utilisez [**IXAudio2Voice :: GetVoiceDetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails) sur la voix de mastérisation pour obtenir le nombre de InputChannels pour **nChannels**.</span><span class="sxs-lookup"><span data-stu-id="ffebd-127">Use [**IXAudio2Voice::GetVoiceDetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails) on the mastering voice to obtain the number of InputChannels for **nChannels**.</span></span> <span data-ttu-id="ffebd-128">Pour les versions du kit de développement logiciel (SDK) DirectX de XAUDIO2 antérieures à Windows 8, utilisez IXAudio2 :: GetDeviceDetails.</span><span class="sxs-lookup"><span data-stu-id="ffebd-128">For DirectX SDK versions of XAUDIO2 prior to Windows 8, use IXAudio2::GetDeviceDetails.</span></span>

     

<span data-ttu-id="ffebd-129">Effectuez ces étapes une fois toutes les deux à trois frames pour calculer de nouveaux paramètres et les appliquer.</span><span class="sxs-lookup"><span data-stu-id="ffebd-129">Perform these steps once every two to three frames to calculate new settings and apply them.</span></span> <span data-ttu-id="ffebd-130">Dans cet exemple, une voix source est envoyée directement à la voix de mastérisation et à une voix de mixage secondaire avec un effet de réverbération appliqué.</span><span class="sxs-lookup"><span data-stu-id="ffebd-130">In this example, a source voice is sending directly to the mastering voice and to a submix voice with a reverb effect applied to it.</span></span>

<span data-ttu-id="ffebd-131">**Pour utiliser X3DAudio pour calculer et appliquer de nouveaux paramètres audio 3D**</span><span class="sxs-lookup"><span data-stu-id="ffebd-131">**To use X3DAudio to calculate and apply new 3D audio settings**</span></span>

1.  <span data-ttu-id="ffebd-132">Mettez à jour les structures d' [**\_ écouteur X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) et d' [**\_ émetteur X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) avec leur position, vélocité et orientation actuelles.</span><span class="sxs-lookup"><span data-stu-id="ffebd-132">Update the [**X3DAUDIO\_LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) and [**X3DAUDIO\_EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) structures with their current position, velocity, and orientation.</span></span>

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

    

2.  <span data-ttu-id="ffebd-133">Appelez [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) pour calculer les nouveaux paramètres des voix.</span><span class="sxs-lookup"><span data-stu-id="ffebd-133">Call [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) to calculate new settings for the voices.</span></span>

    <span data-ttu-id="ffebd-134">Les paramètres pour [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) sont l' [**\_ écouteur X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) et les structures [**d' \_ émetteur de X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) mis à jour.</span><span class="sxs-lookup"><span data-stu-id="ffebd-134">The parameters for [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) will be the updated [**X3DAUDIO\_LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) and [**X3DAUDIO\_EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) structures.</span></span> <span data-ttu-id="ffebd-135">Les indicateurs indiquent les valeurs que **X3DAudioCalculate** doit calculer, et la structure de [**\_ \_ paramètres X3DAUDIO DSP**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) qui contiendra les résultats des calculs effectués.</span><span class="sxs-lookup"><span data-stu-id="ffebd-135">The flags will indicate what values **X3DAudioCalculate** should calculate, and which [**X3DAUDIO\_DSP\_SETTINGS**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) structure will hold the results of the calculations performed.</span></span>

    ```
    X3DAudioCalculate(X3DInstance, &Listener, &Emitter,
        X3DAUDIO_CALCULATE_MATRIX | X3DAUDIO_CALCULATE_DOPPLER | X3DAUDIO_CALCULATE_LPF_DIRECT | X3DAUDIO_CALCULATE_REVERB,
        &DSPSettings );
    ```

    

3.  <span data-ttu-id="ffebd-136">Utilisez [**IXAudio2Voice :: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) et [**IXAudio2SourceVoice :: SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) pour appliquer les valeurs de volume et de tangage à la voix source.</span><span class="sxs-lookup"><span data-stu-id="ffebd-136">Use [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) and [**IXAudio2SourceVoice::SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) to apply the volume and pitch values to the source voice.</span></span>

    ```
    pSFXSourceVoice->SetOutputMatrix( pMasterVoice, 1, deviceDetails.OutputFormat.Format.nChannels, DSPSettings.pMatrixCoefficients ) ;
    pSFXSourceVoice->SetFrequencyRatio(DSPSettings.DopplerFactor);
    ```

    

4.  <span data-ttu-id="ffebd-137">Utilisez [**IXAudio2Voice :: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) pour appliquer le niveau de réverbération calculé à la voix de mixage secondaire.</span><span class="sxs-lookup"><span data-stu-id="ffebd-137">Use [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) to apply the calculated reverb level to the submix voice.</span></span>

    ```
    pSFXSourceVoice->SetOutputMatrix(pSubmixVoice, 1, 1, &DSPSettings.ReverbLevel);
    ```

    

5.  <span data-ttu-id="ffebd-138">Utilisez [**IXAudio2Voice :: SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters) pour appliquer le coefficient direct du filtre de passe faible calculé à la voix source.</span><span class="sxs-lookup"><span data-stu-id="ffebd-138">Use [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters) to apply the calculated low pass filter direct coefficient to the source voice.</span></span>

    ```
    XAUDIO2_FILTER_PARAMETERS FilterParameters = { LowPassFilter, 2.0f * sinf(X3DAUDIO_PI/6.0f * DSPSettings.LPFDirectCoefficient), 1.0f };
    pSFXSourceVoice->SetFilterParameters(&FilterParameters);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="ffebd-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ffebd-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffebd-140">X3DAudio</span><span class="sxs-lookup"><span data-stu-id="ffebd-140">X3DAudio</span></span>](x3daudio.md)
</dt> <dt>

[<span data-ttu-id="ffebd-141">Présentation de X3DAudio</span><span class="sxs-lookup"><span data-stu-id="ffebd-141">X3DAudio Overview</span></span>](x3daudio-overview.md)
</dt> <dt>

[<span data-ttu-id="ffebd-142">Guide de programmation XAudio2</span><span class="sxs-lookup"><span data-stu-id="ffebd-142">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="ffebd-143">Contrôle du volume et du tangage XAudio2</span><span class="sxs-lookup"><span data-stu-id="ffebd-143">XAudio2 Volume and Pitch Control</span></span>](volume-and-pitch-control.md)
</dt> </dl>

 

 
