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
# <a name="how-to-create-an-effect-chain"></a><span data-ttu-id="13827-104">Procédure : Créer une chaîne d’effets</span><span class="sxs-lookup"><span data-stu-id="13827-104">How to: Create an Effect Chain</span></span>

<span data-ttu-id="13827-105">Cette rubrique montre comment vous pouvez appliquer une chaîne d’effet à une voix pour permettre le traitement personnalisé des données audio pour cette voix.</span><span class="sxs-lookup"><span data-stu-id="13827-105">This topic shows you how you can apply an effect chain to a voice to allow custom processing of the audio data for that voice.</span></span> <span data-ttu-id="13827-106">Cette rubrique explique comment utiliser l’effet de réverbération, qui est l’un des effets XAudio2 intégrés.</span><span class="sxs-lookup"><span data-stu-id="13827-106">This topic describes how to use the reverb effect, which is one of the built-in XAudio2 effects.</span></span>

## <a name="to-create-a-basic-effect-chain-that-applies-an-effect-to-a-voice"></a><span data-ttu-id="13827-107">Pour créer une chaîne à effet de base qui applique un effet à une voix</span><span class="sxs-lookup"><span data-stu-id="13827-107">To create a basic effect chain that applies an effect to a voice</span></span>

1.  <span data-ttu-id="13827-108">Créez l’effet.</span><span class="sxs-lookup"><span data-stu-id="13827-108">Create the effect.</span></span>

    <span data-ttu-id="13827-109">Dans cet exemple, la fonction [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) crée un effet de réverbération.</span><span class="sxs-lookup"><span data-stu-id="13827-109">In this example, the [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) function creates a reverb effect.</span></span> <span data-ttu-id="13827-110">Consultez [effets audio XAudio2](xaudio2-audio-effects.md) pour obtenir la liste des sources d’effets possibles à utiliser avec XAudio2.</span><span class="sxs-lookup"><span data-stu-id="13827-110">See [XAudio2 Audio Effects](xaudio2-audio-effects.md) for a list of possible sources of effects for use with XAudio2.</span></span>

    ```
    IUnknown * pXAPO;
    hr = XAudio2CreateReverb(&pXAPO);
    ```

    

2.  <span data-ttu-id="13827-111">Remplir une structure de [**\_ \_ descripteur d’effet XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) avec des données.</span><span class="sxs-lookup"><span data-stu-id="13827-111">Populate an [**XAUDIO2\_EFFECT\_DESCRIPTOR**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) structure with data.</span></span>

    <span data-ttu-id="13827-112">S’il y a plusieurs effets dans la chaîne, chaque effet nécessite une structure de [**\_ \_ descripteur d’effet XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="13827-112">If there are multiple effects in the chain, each effect will need a [**XAUDIO2\_EFFECT\_DESCRIPTOR**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) structure.</span></span>

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

3.  <span data-ttu-id="13827-113">Remplir une structure de [**\_ \_ chaîne d’effet XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) avec des données.</span><span class="sxs-lookup"><span data-stu-id="13827-113">Populate an [**XAUDIO2\_EFFECT\_CHAIN**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) structure with data.</span></span> <span data-ttu-id="13827-114">Dans ce cas, la chaîne n’a qu’un seul effet.</span><span class="sxs-lookup"><span data-stu-id="13827-114">In this case, the chain only has one effect.</span></span> <span data-ttu-id="13827-115">Si la chaîne a plusieurs effets, le membre EffectCount contiendra le nombre d’effets et le membre pEffectDescriptors pointera vers un tableau de \_ \_ structures de descripteur d’effet XAUDIO2.</span><span class="sxs-lookup"><span data-stu-id="13827-115">If the chain has more than one effect, the EffectCount member will contain the count of effects, and the pEffectDescriptors member will point to an array of XAUDIO2\_EFFECT\_DESCRIPTOR structures.</span></span>

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

4.  <span data-ttu-id="13827-116">Appliquez la chaîne d’effet à une voix avec la fonction [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) .</span><span class="sxs-lookup"><span data-stu-id="13827-116">Apply the effect chain to a voice with the [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) function.</span></span>

    <span data-ttu-id="13827-117">Vous pouvez appliquer des chaînes d’effet aux voix principales, aux voix source et aux voix de mixage secondaire.</span><span class="sxs-lookup"><span data-stu-id="13827-117">You can apply effect chains to master voices, source voices, and submix voices.</span></span>

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

5.  <span data-ttu-id="13827-118">Libérer l’effet avec IUnknown :: Release.</span><span class="sxs-lookup"><span data-stu-id="13827-118">Release the effect with IUnknown::Release.</span></span>

    <span data-ttu-id="13827-119">Lorsque vous créez un XAPO, il aura un nombre de références de 1.</span><span class="sxs-lookup"><span data-stu-id="13827-119">When you create an XAPO, it will have a reference count of 1.</span></span> <span data-ttu-id="13827-120">Lorsque XAPO est passé à XAudio2 avec [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 incrémente le décompte de références sur le XAPO.</span><span class="sxs-lookup"><span data-stu-id="13827-120">When the XAPO is passed to XAudio2 with [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 increments the reference count on the XAPO.</span></span> <span data-ttu-id="13827-121">Le fait de libérer la référence du client au XAPO permet à XAudio2 de prendre possession du XAPO.</span><span class="sxs-lookup"><span data-stu-id="13827-121">Releasing the client's reference to the XAPO allows XAudio2 to take ownership of the XAPO.</span></span> <span data-ttu-id="13827-122">Si XAudio2 a la seule référence à XAPO, il sera supprimé lorsqu’il n’est plus utilisé par XAudio2.</span><span class="sxs-lookup"><span data-stu-id="13827-122">If XAudio2 has the only reference to the XAPO, it will be disposed of when it is no longer being used by XAudio2.</span></span> <span data-ttu-id="13827-123">Si le code client doit conserver une référence à XAPO, par exemple pour une réutilisation ultérieure, vous devez ignorer cette étape.</span><span class="sxs-lookup"><span data-stu-id="13827-123">If the client code needs to maintain a reference to the XAPO—for example for later reuse—you should skip this step.</span></span>

    ```
    pXAPO->Release();
    ```

    

6.  <span data-ttu-id="13827-124">Renseignez la structure de paramètre, le cas échéant, associée à l’effet.</span><span class="sxs-lookup"><span data-stu-id="13827-124">Populate the parameter structure, if any, associated with the effect.</span></span> <span data-ttu-id="13827-125">L’effet de réverbération utilise une structure de [**\_ \_ paramètres de réverbération XAUDIO2FX**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters) .</span><span class="sxs-lookup"><span data-stu-id="13827-125">The reverb effect uses an [**XAUDIO2FX\_REVERB\_PARAMETERS**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters) structure.</span></span>

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

    

7.  <span data-ttu-id="13827-126">Transmettez la structure du paramètre Effect à l’effet en appelant la fonction [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) sur la voix à laquelle l’effet est attaché.</span><span class="sxs-lookup"><span data-stu-id="13827-126">Pass the effect parameter structure to the effect by calling the [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) function on the voice to which the effect is attached.</span></span>

    ```
    hr = pVoice->SetEffectParameters( 0, &reverbParameters, sizeof( reverbParameters ) );
    ```

    

8.  <span data-ttu-id="13827-127">Désactivez ou activez l’effet, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="13827-127">Disable or enable the effect, whenever appropriate.</span></span>

    <span data-ttu-id="13827-128">Vous pouvez utiliser [**DisableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) à tout moment pour désactiver un effet.</span><span class="sxs-lookup"><span data-stu-id="13827-128">You can use [**DisableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) at any time to turn an effect off.</span></span>

    ```
    pVoice->DisableEffect(0);
    ```

    

    <span data-ttu-id="13827-129">Vous pouvez réactiver un effet avec [**EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect).</span><span class="sxs-lookup"><span data-stu-id="13827-129">You can turn on an effect again with [**EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect).</span></span>

    ```
    pVoice->EnableEffect(0);
    ```

    

    <span data-ttu-id="13827-130">Les paramètres pour [**DisableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) et [**EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect) spécifient l’effet de la chaîne à activer ou désactiver.</span><span class="sxs-lookup"><span data-stu-id="13827-130">The parameters for [**DisableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) and [**EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect) specify which effect in the chain to enable or disable.</span></span>

## <a name="related-topics"></a><span data-ttu-id="13827-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="13827-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13827-132">Effets audio</span><span class="sxs-lookup"><span data-stu-id="13827-132">Audio Effects</span></span>](audio-effects.md)
</dt> <dt>

[<span data-ttu-id="13827-133">Guide de programmation XAudio2</span><span class="sxs-lookup"><span data-stu-id="13827-133">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="13827-134">Procédure : créer un graphique de traitement audio de base</span><span class="sxs-lookup"><span data-stu-id="13827-134">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="13827-135">Présentation de XAPO</span><span class="sxs-lookup"><span data-stu-id="13827-135">XAPO Overview</span></span>](xapo-overview.md)
</dt> <dt>

[<span data-ttu-id="13827-136">Comment : utiliser XAOPFX dans XAudio2</span><span class="sxs-lookup"><span data-stu-id="13827-136">How to: Use XAOPFX in XAudio2</span></span>](how-to--use-xapofx-in-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="13827-137">Comment : utiliser un XAOP dans XAudio2</span><span class="sxs-lookup"><span data-stu-id="13827-137">How to: Use an XAOP in XAudio2</span></span>](how-to--use-an-xapo-in-xaudio2.md)
</dt> </dl>

 

 
