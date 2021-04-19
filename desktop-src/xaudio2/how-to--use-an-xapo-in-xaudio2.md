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
# <a name="how-to-use-an-xapo-in-xaudio2"></a><span data-ttu-id="99380-103">Procédure : Utiliser un XAPO dans XAudio2</span><span class="sxs-lookup"><span data-stu-id="99380-103">How to: Use an XAPO in XAudio2</span></span>

<span data-ttu-id="99380-104">Cette rubrique vous montre comment utiliser un effet créé avec l’API XAPO dans une chaîne d’effet XAudio2.</span><span class="sxs-lookup"><span data-stu-id="99380-104">This topic shows you how to use an effect created with the XAPO API in an XAudio2 effect chain.</span></span>

1.  <span data-ttu-id="99380-105">Créez le XAPO comme décrit dans [How to : Create a XAPO](how-to--create-an-xapo.md).</span><span class="sxs-lookup"><span data-stu-id="99380-105">Create the XAPO as described in [How to: Create an XAPO](how-to--create-an-xapo.md).</span></span>

    <span data-ttu-id="99380-106">Vous pouvez également implémenter des fonctionnalités de paramètre au moment de l’exécution, comme décrit dans [Comment : ajouter la prise en charge des paramètres d’exécution à un XAPO](how-to--add-run-time-parameter-support-to-an-xapo.md).</span><span class="sxs-lookup"><span data-stu-id="99380-106">You can also implement run-time parameter functionality as described in [How to: Add Run-time Parameter Support to an XAPO](how-to--add-run-time-parameter-support-to-an-xapo.md).</span></span>

2.  <span data-ttu-id="99380-107">Créez une instance de XAPO.</span><span class="sxs-lookup"><span data-stu-id="99380-107">Create an instance of the XAPO.</span></span>

    ```
    IUnknown * pXAPO;
    pXAPO = new SimpleXAPO();
    ```

    

3.  <span data-ttu-id="99380-108">Remplir une structure de [**\_ \_ descripteur d’effet XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) avec des données.</span><span class="sxs-lookup"><span data-stu-id="99380-108">Populate an [**XAUDIO2\_EFFECT\_DESCRIPTOR**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) structure with data.</span></span>

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

4.  <span data-ttu-id="99380-109">Remplir une structure de [**\_ \_ chaîne d’effet XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) avec des données.</span><span class="sxs-lookup"><span data-stu-id="99380-109">Populate an [**XAUDIO2\_EFFECT\_CHAIN**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) structure with data.</span></span>

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

5.  <span data-ttu-id="99380-110">Appliquez la chaîne d’effet à une voix XAudio2 avec la fonction [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) .</span><span class="sxs-lookup"><span data-stu-id="99380-110">Apply the effect chain to an XAudio2 voice with the [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) function.</span></span>

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

    > [!Note]  
    > <span data-ttu-id="99380-111">Une chaîne d’effet peut également être appliquée à une voix lorsque la voix est créée en passant la chaîne en tant que paramètre à [**IXAudio2 :: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2 :: CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice)ou [**IXAudio2 :: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).</span><span class="sxs-lookup"><span data-stu-id="99380-111">An effect chain can also be applied to a voice when the voice is created by passing the chain as a parameter to [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2::CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice), or [**IXAudio2::CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).</span></span>

     

6.  <span data-ttu-id="99380-112">Libérer l’effet avec IUnknown :: Release.</span><span class="sxs-lookup"><span data-stu-id="99380-112">Release the effect with IUnknown::Release.</span></span>

    <span data-ttu-id="99380-113">Lorsque vous créez un XAPO, il aura un nombre de références de 1.</span><span class="sxs-lookup"><span data-stu-id="99380-113">When you create an XAPO, it will have a reference count of 1.</span></span> <span data-ttu-id="99380-114">Lorsque XAPO est passé à XAudio2 avec [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 incrémente le décompte de références sur le XAPO.</span><span class="sxs-lookup"><span data-stu-id="99380-114">When the XAPO is passed to XAudio2 with [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 increments the reference count on the XAPO.</span></span> <span data-ttu-id="99380-115">Le fait de libérer la référence du client au XAPO permet à XAudio2 de prendre possession du XAPO.</span><span class="sxs-lookup"><span data-stu-id="99380-115">Releasing the client's reference to the XAPO allows XAudio2 to take ownership of the XAPO.</span></span> <span data-ttu-id="99380-116">Si XAudio2 a la seule référence à XAPO, il sera supprimé lorsqu’il n’est plus utilisé par XAudio2.</span><span class="sxs-lookup"><span data-stu-id="99380-116">If XAudio2 has the only reference to the XAPO, it will be disposed of when it is no longer being used by XAudio2.</span></span> <span data-ttu-id="99380-117">Si le code client doit conserver une référence à XAPO pour une réutilisation ultérieure, par exemple, vous devez ignorer cette étape.</span><span class="sxs-lookup"><span data-stu-id="99380-117">If the client code needs to maintain a reference to the XAPO for later reuse, for example, you should skip this step.</span></span>

    ```
    pXAPO->Release();
    ```

    

7.  <span data-ttu-id="99380-118">Renseignez la structure de paramètre, le cas échéant, associée à l’effet.</span><span class="sxs-lookup"><span data-stu-id="99380-118">Populate the parameter structure, if any, associated with the effect.</span></span> <span data-ttu-id="99380-119">Dans ce cas, pourcentage de la puissance totale à laquelle l’effet doit être appliqué.</span><span class="sxs-lookup"><span data-stu-id="99380-119">In this case, the percentage of full strength at which the effect should be applied.</span></span>

    ```
    XAPO_PARAMETERS XAPOParameters;
    XAPOParameters.Level = 0.75;
    ```

    

8.  <span data-ttu-id="99380-120">Transmettez la structure du paramètre Effect à l’effet en appelant la fonction [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) sur la voix à laquelle l’effet est attaché.</span><span class="sxs-lookup"><span data-stu-id="99380-120">Pass the effect parameter structure to the effect by calling the [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) function on the voice to which the effect is attached.</span></span>

    ```
    hr = pVoice->SetEffectParameters( 0, &XAPOParameters, sizeof( XAPO_PARAMETERS ) );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="99380-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="99380-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99380-122">Effets audio</span><span class="sxs-lookup"><span data-stu-id="99380-122">Audio Effects</span></span>](audio-effects.md)
</dt> <dt>

[<span data-ttu-id="99380-123">Présentation de XAPO</span><span class="sxs-lookup"><span data-stu-id="99380-123">XAPO Overview</span></span>](xapo-overview.md)
</dt> <dt>

[<span data-ttu-id="99380-124">Guide de programmation XAudio2</span><span class="sxs-lookup"><span data-stu-id="99380-124">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 
