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
# <a name="how-to-use-xapofx-in-xaudio2"></a><span data-ttu-id="cec11-103">Procédure : utiliser un XAPOFX dans XAudio2</span><span class="sxs-lookup"><span data-stu-id="cec11-103">How to: Use XAPOFX in XAudio2</span></span>

<span data-ttu-id="cec11-104">Cette rubrique vous montre comment utiliser l’un des effets inclus dans XAPOFX dans une chaîne d’effet XAudio2.</span><span class="sxs-lookup"><span data-stu-id="cec11-104">This topic shows you how to use one of the effects included in XAPOFX in an XAudio2 effect chain.</span></span>

## <a name="to-use-an-effect-from-xapofx-in-an-xaudio2-effect-chain"></a><span data-ttu-id="cec11-105">Pour utiliser un effet à partir de XAPOFX dans une chaîne d’effet XAudio2</span><span class="sxs-lookup"><span data-stu-id="cec11-105">To use an effect from XAPOFX in an XAudio2 effect chain</span></span>

1.  <span data-ttu-id="cec11-106">Créez l’effet en passant le CLSID d’un effet XAPOFX à la fonction [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) .</span><span class="sxs-lookup"><span data-stu-id="cec11-106">Create the effect by passing the CLSID of an XAPOFX effect to the [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) function.</span></span>

    <span data-ttu-id="cec11-107">Dans ce cas, l’effet de réverbération simplifié FXReverb est créé.</span><span class="sxs-lookup"><span data-stu-id="cec11-107">In this case, the simplified reverb effect FXReverb is being created.</span></span>

    ```
    IUnknown * pXAPO;
    CreateFX(__uuidof(FXReverb),&pXAPO);
    ```

    

2.  <span data-ttu-id="cec11-108">Remplir une structure de [**\_ \_ descripteur d’effet XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) avec des données.</span><span class="sxs-lookup"><span data-stu-id="cec11-108">Populate an [**XAUDIO2\_EFFECT\_DESCRIPTOR**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) structure with data.</span></span>

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

3.  <span data-ttu-id="cec11-109">Remplir une structure de [**\_ \_ chaîne d’effet XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) avec des données.</span><span class="sxs-lookup"><span data-stu-id="cec11-109">Populate an [**XAUDIO2\_EFFECT\_CHAIN**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) structure with data.</span></span>

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

4.  <span data-ttu-id="cec11-110">Appliquez la chaîne d’effet à une voix XAudio2 avec la fonction [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) .</span><span class="sxs-lookup"><span data-stu-id="cec11-110">Apply the effect chain to an XAudio2 voice with the [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) function.</span></span>

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

    > [!Note]  
    > <span data-ttu-id="cec11-111">Vous pouvez également appliquer une chaîne d’effet à une voix quand vous créez la voix en passant la chaîne en tant que paramètre à [**IXAudio2 :: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2 :: CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice)ou [**IXAudio2 :: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).</span><span class="sxs-lookup"><span data-stu-id="cec11-111">You can also apply an effect chain to a voice when you create the voice by passing the chain as a parameter to [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2::CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice), or [**IXAudio2::CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).</span></span>

     

5.  <span data-ttu-id="cec11-112">Libérer l’effet avec IUnknown :: Release.</span><span class="sxs-lookup"><span data-stu-id="cec11-112">Release the effect with IUnknown::Release.</span></span> <span data-ttu-id="cec11-113">Lorsque vous créez un XAPO, il aura un nombre de références de 1.</span><span class="sxs-lookup"><span data-stu-id="cec11-113">When you create an XAPO, it will have a reference count of 1.</span></span> <span data-ttu-id="cec11-114">Lorsque XAPO est passé à XAudio2 avec [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 incrémente le décompte de références sur le XAPO.</span><span class="sxs-lookup"><span data-stu-id="cec11-114">When the XAPO is passed to XAudio2 with [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 increments the reference count on the XAPO.</span></span> <span data-ttu-id="cec11-115">Le fait de libérer la référence du client au XAPO permet à XAudio2 de prendre possession du XAPO.</span><span class="sxs-lookup"><span data-stu-id="cec11-115">Releasing the client's reference to the XAPO allows XAudio2 to take ownership of the XAPO.</span></span> <span data-ttu-id="cec11-116">Si XAudio2 a la seule référence à XAPO, cette référence est supprimée lorsqu’elle n’est plus utilisée par XAudio2.</span><span class="sxs-lookup"><span data-stu-id="cec11-116">If XAudio2 has the only reference to the XAPO, this reference is disposed of when it is no longer being used by XAudio2.</span></span> <span data-ttu-id="cec11-117">Si le code client doit conserver une référence à XAPO, par exemple, pour une réutilisation ultérieure, vous pouvez ignorer cette étape.</span><span class="sxs-lookup"><span data-stu-id="cec11-117">If the client code needs to maintain a reference to the XAPO—for example, for reuse later—you can skip this step.</span></span>

    ```
    pXAPO->Release();
    ```

    

6.  <span data-ttu-id="cec11-118">Renseignez la structure de paramètre, le cas échéant, associée à l’effet.</span><span class="sxs-lookup"><span data-stu-id="cec11-118">Populate the parameter structure, if any, associated with the effect.</span></span>

    <span data-ttu-id="cec11-119">Dans ce cas, la structure de [**\_ paramètres FXREVERB**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters) est utilisée pour définir la diffusion et la taille de la salle que l’effet de réverbération doit utiliser.</span><span class="sxs-lookup"><span data-stu-id="cec11-119">In this case, the [**FXREVERB\_PARAMETERS**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters) structure is used to set the diffusion and room size that the reverb effect should use.</span></span>

    ```
    FXREVERB_PARAMETERS XAPOParameters;
    XAPOParameters.Diffusion = FXREVERB_DEFAULT_DIFFUSION;
    XAPOParameters.RoomSize = FXREVERB_DEFAULT_ROOMSIZE;
    ```

    

7.  <span data-ttu-id="cec11-120">Transmettez la structure du paramètre Effect à l’effet en appelant la fonction [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) sur la voix à laquelle l’effet est attaché.</span><span class="sxs-lookup"><span data-stu-id="cec11-120">Pass the effect parameter structure to the effect by calling the [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) function on the voice to which the effect is attached.</span></span>

    ```
    hr = pVoice->SetEffectParameters( 0, &XAPOParameters, sizeof( FXREVERB_PARAMETERS ) );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="cec11-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cec11-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cec11-122">Effets audio</span><span class="sxs-lookup"><span data-stu-id="cec11-122">Audio Effects</span></span>](audio-effects.md)
</dt> <dt>

[<span data-ttu-id="cec11-123">Guide de programmation XAudio2</span><span class="sxs-lookup"><span data-stu-id="cec11-123">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 
