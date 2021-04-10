---
description: L’API XAPO fournit l’interface IXAPO et la classe CXAPOBase pour la génération de nouveaux types XAPO.
ms.assetid: 34f5c3d5-ee40-e304-7c97-d30c17621d26
title: 'Procédure : Créer un XAPO'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 549739462a0e76cbb437f0aa1403b099f72f5224
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210808"
---
# <a name="how-to-create-an-xapo"></a><span data-ttu-id="b426c-103">Procédure : Créer un XAPO</span><span class="sxs-lookup"><span data-stu-id="b426c-103">How to: Create an XAPO</span></span>

<span data-ttu-id="b426c-104">L’API XAPO fournit l’interface [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) et la classe [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) pour la génération de nouveaux types XAPO.</span><span class="sxs-lookup"><span data-stu-id="b426c-104">The XAPO API provides the [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) interface and the [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) class for building new XAPO types.</span></span> <span data-ttu-id="b426c-105">L’interface **IXAPO** contient toutes les méthodes qui doivent être implémentées pour créer un nouveau XAPO.</span><span class="sxs-lookup"><span data-stu-id="b426c-105">The **IXAPO** interface contains all of the methods that need to be implemented to create a new XAPO.</span></span> <span data-ttu-id="b426c-106">La classe **CXAPOBase** fournit une implémentation de base de l’interface **IXAPO** .</span><span class="sxs-lookup"><span data-stu-id="b426c-106">The **CXAPOBase** class provides a basic implementation of the **IXAPO** interface.</span></span> <span data-ttu-id="b426c-107">**CXAPOBase** implémente toutes les méthodes d’interface **IXAPO** , à l’exception de la méthode [**IXAPO ::P tionnaire**](/windows/win32/api/xapo/nf-xapo-ixapo-process) , qui est unique à chaque XAPO.</span><span class="sxs-lookup"><span data-stu-id="b426c-107">**CXAPOBase** implements all of the **IXAPO** interface methods except the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method, which is unique to each XAPO.</span></span>

## <a name="to-create-a-new-static-xapo"></a><span data-ttu-id="b426c-108">Pour créer un XAPO statique</span><span class="sxs-lookup"><span data-stu-id="b426c-108">To create a new static XAPO</span></span>

1.  <span data-ttu-id="b426c-109">Dérivez une nouvelle classe XAPO à partir de la classe de base [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) .</span><span class="sxs-lookup"><span data-stu-id="b426c-109">Derive a new XAPO class from the [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) base class.</span></span>

    > [!Note]  
    > <span data-ttu-id="b426c-110">XAPOs implémente l’interface **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="b426c-110">XAPOs implement the **IUnknown** interface.</span></span> <span data-ttu-id="b426c-111">Les interfaces [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) et [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) incluent les trois méthodes **IUnknown** : **QueryInterface**, **AddRef** et **Release**.</span><span class="sxs-lookup"><span data-stu-id="b426c-111">The [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) and [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) interfaces include the three **IUnknown** methods: **QueryInterface**, **AddRef**, and **Release**.</span></span> <span data-ttu-id="b426c-112">[**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) fournit des implémentations des trois méthodes **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="b426c-112">[**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) provides implementations of all three of the **IUnknown** methods.</span></span> <span data-ttu-id="b426c-113">Une nouvelle instance de **CXAPOBase** aura un compte de référence de 1.</span><span class="sxs-lookup"><span data-stu-id="b426c-113">A new instance of **CXAPOBase** will have a reference count of 1.</span></span> <span data-ttu-id="b426c-114">Elle sera détruite quand son décompte de références devient 0.</span><span class="sxs-lookup"><span data-stu-id="b426c-114">It will be destroyed when its reference count becomes 0.</span></span> <span data-ttu-id="b426c-115">Pour permettre à XAudio2 de détruire une instance d’un XAPO lorsqu’il n’est plus nécessaire, appelez **IUnknown :: Release** sur le XAPO après qu’il a été ajouté à une chaîne d’effet XAudio2.</span><span class="sxs-lookup"><span data-stu-id="b426c-115">To allow XAudio2 to destroy an instance of an XAPO when it is no longer needed, call **IUnknown::Release** on the XAPO after it is added to an XAudio2 effect chain.</span></span> <span data-ttu-id="b426c-116">Pour plus d’informations sur l’utilisation d’un XAPO avec XAudio2, voir [How to : Use an XAPO in XAudio2](how-to--use-an-xapo-in-xaudio2.md) .</span><span class="sxs-lookup"><span data-stu-id="b426c-116">See [How to: Use an XAPO in XAudio2](how-to--use-an-xapo-in-xaudio2.md) for more information about using an XAPO with XAudio2.</span></span>

     

2.  <span data-ttu-id="b426c-117">Substituez l’implémentation de la classe [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) de la méthode [**IXAPO :: LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) .</span><span class="sxs-lookup"><span data-stu-id="b426c-117">Override the [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) class implementation of the [**IXAPO::LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) method.</span></span>

    <span data-ttu-id="b426c-118">Le remplacement de [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) permet d’obtenir des informations sur le format des données audio à stocker en vue de leur utilisation dans [**IXAPO ::P tionnaire**](/windows/win32/api/xapo/nf-xapo-ixapo-process).</span><span class="sxs-lookup"><span data-stu-id="b426c-118">Overriding [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) allows information about the format of audio data to be stored for use in [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process).</span></span>

3.  <span data-ttu-id="b426c-119">Implémentez la méthode [**IXAPO ::P tionnaire**](/windows/win32/api/xapo/nf-xapo-ixapo-process) .</span><span class="sxs-lookup"><span data-stu-id="b426c-119">Implement the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method.</span></span>

    <span data-ttu-id="b426c-120">XAudio2 appelle la méthode [**IXAPO ::P tionnaire**](/windows/win32/api/xapo/nf-xapo-ixapo-process) chaque fois qu’un XAPO doit traiter des données audio.</span><span class="sxs-lookup"><span data-stu-id="b426c-120">XAudio2 calls the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method whenever an XAPO needs to process audio data.</span></span> <span data-ttu-id="b426c-121">Le **processus** contient l’essentiel du code pour un XAPO.</span><span class="sxs-lookup"><span data-stu-id="b426c-121">**Process** contains the bulk of the code for an XAPO.</span></span>

## <a name="implementing-the-process-method"></a><span data-ttu-id="b426c-122">Implémentation de la méthode Process</span><span class="sxs-lookup"><span data-stu-id="b426c-122">Implementing the Process Method</span></span>

<span data-ttu-id="b426c-123">La méthode [**IXAPO ::P tionnaire**](/windows/win32/api/xapo/nf-xapo-ixapo-process) accepte les mémoires tampons de flux pour les données audio d’entrée et de sortie.</span><span class="sxs-lookup"><span data-stu-id="b426c-123">The [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method accepts stream buffers for input and output audio data.</span></span> <span data-ttu-id="b426c-124">Un XAPO classique attend une mémoire tampon de flux d’entrée et une mémoire tampon de flux de sortie.</span><span class="sxs-lookup"><span data-stu-id="b426c-124">A typical XAPO will expect one input stream buffer and one output stream buffer.</span></span> <span data-ttu-id="b426c-125">Vous devez baser le traitement des données à partir de la mémoire tampon du flux d’entrée au format spécifié dans la fonction [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) et tous les indicateurs passés à la fonction de **traitement** avec la mémoire tampon du flux d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b426c-125">You should base the processing of data from the input stream buffer on the format specified in the [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) function and any flags passed to the **Process** function with the input stream buffer.</span></span> <span data-ttu-id="b426c-126">Copiez les données de mémoire tampon du flux d’entrée traitées dans la mémoire tampon du flux de sortie.</span><span class="sxs-lookup"><span data-stu-id="b426c-126">Copy the processed input stream buffer data to the output stream buffer.</span></span> <span data-ttu-id="b426c-127">Définissez le paramètre BufferFlags de la mémoire tampon du flux de sortie en tant que tampon [**XAPO \_ \_ valide**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags) ou **XAPO en \_ \_ mode silencieux**.</span><span class="sxs-lookup"><span data-stu-id="b426c-127">Set the output stream buffer's BufferFlags parameter as either [**XAPO\_BUFFER\_VALID**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags) or **XAPO\_BUFFER\_SILENT**.</span></span>

<span data-ttu-id="b426c-128">L’exemple suivant illustre une implémentation de [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) et de [**processus**](/windows/win32/api/xapo/nf-xapo-ixapo-process) qui copie simplement les données d’une mémoire tampon d’entrée vers une mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="b426c-128">The following example demonstrates a [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) and [**Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) implementation that simply copies data from an input buffer to an output buffer.</span></span> <span data-ttu-id="b426c-129">Toutefois, il n’y a aucun traitement si la mémoire tampon d’entrée est marquée avec le [**\_ \_ mode silencieux de la mémoire tampon XAPO**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags).</span><span class="sxs-lookup"><span data-stu-id="b426c-129">However, there is no processing if the input buffer is marked with [**XAPO\_BUFFER\_SILENT**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags).</span></span>


```
STDMETHOD(LockForProcess) (UINT32 InputLockedParameterCount,
          const XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS* pInputLockedParameters,
          UINT32 OutputLockedParameterCount,
          const XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS* pOutputLockedParameters)
{
    assert(!IsLocked());
    assert(InputLockedParameterCount == 1);
    assert(OutputLockedParameterCount == 1);
    assert(pInputLockedParameters != NULL);
    assert(pOutputLockedParameters != NULL);
    assert(pInputLockedParameters[0].pFormat != NULL);
    assert(pOutputLockedParameters[0].pFormat != NULL);


    m_uChannels = pInputLockedParameters[0].pFormat->nChannels;
    m_uBytesPerSample = (pInputLockedParameters[0].pFormat->wBitsPerSample >> 3);

    return CXAPOBase::LockForProcess(
        InputLockedParameterCount,
        pInputLockedParameters,
        OutputLockedParameterCount,
        pOutputLockedParameters);
}
STDMETHOD_(void, Process)(UINT32 InputProcessParameterCount,
           const XAPO_PROCESS_BUFFER_PARAMETERS* pInputProcessParameters,
           UINT32 OutputProcessParameterCount,
           XAPO_PROCESS_BUFFER_PARAMETERS* pOutputProcessParameters,
           BOOL IsEnabled)
{
    assert(IsLocked());
    assert(InputProcessParameterCount == 1);
    assert(OutputProcessParameterCount == 1);
    assert(NULL != pInputProcessParameters);
    assert(NULL != pOutputProcessParameters);


    XAPO_BUFFER_FLAGS inFlags = pInputProcessParameters[0].BufferFlags;
    XAPO_BUFFER_FLAGS outFlags = pOutputProcessParameters[0].BufferFlags;

    // assert buffer flags are legitimate
    assert(inFlags == XAPO_BUFFER_VALID || inFlags == XAPO_BUFFER_SILENT);
    assert(outFlags == XAPO_BUFFER_VALID || outFlags == XAPO_BUFFER_SILENT);

    // check input APO_BUFFER_FLAGS
    switch (inFlags)
    {
    case XAPO_BUFFER_VALID:
        {
            void* pvSrc = pInputProcessParameters[0].pBuffer;
            assert(pvSrc != NULL);

            void* pvDst = pOutputProcessParameters[0].pBuffer;
            assert(pvDst != NULL);

            memcpy(pvDst,pvSrc,pInputProcessParameters[0].ValidFrameCount * m_uChannels * m_uBytesPerSample);
            break;
        }

    case XAPO_BUFFER_SILENT:
        {
            // All that needs to be done for this case is setting the
            // output buffer flag to XAPO_BUFFER_SILENT which is done below.
            break;
        }

    }

    // set destination valid frame count, and buffer flags
    pOutputProcessParameters[0].ValidFrameCount = pInputProcessParameters[0].ValidFrameCount; // set destination frame count same as source
    pOutputProcessParameters[0].BufferFlags     = pInputProcessParameters[0].BufferFlags;     // set destination buffer flags same as source

}
```



<span data-ttu-id="b426c-130">Lors de l’écriture d’une méthode de [**processus**](/windows/win32/api/xapo/nf-xapo-ixapo-process) , il est important de noter que les données audio XAudio2 sont entrelacées.</span><span class="sxs-lookup"><span data-stu-id="b426c-130">When writing a [**Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method, it is important to note XAudio2 audio data is interleaved.</span></span> <span data-ttu-id="b426c-131">Cela signifie que les données de chaque canal sont adjacentes pour un exemple de numéro particulier.</span><span class="sxs-lookup"><span data-stu-id="b426c-131">This means data from each channel is adjacent for a particular sample number.</span></span> <span data-ttu-id="b426c-132">Par exemple, si une vague à 4 canaux est lue dans une voix source XAudio2, les données audio sont un exemple de canal 0, un exemple de canal 1, un exemple de canal 2, un exemple de canal 3, puis l’échantillon suivant de canaux 0, 1, 2, 3, etc.</span><span class="sxs-lookup"><span data-stu-id="b426c-132">For example, if there is a 4-channel wave playing into an XAudio2 source voice, the audio data is a sample of channel 0, a sample of channel 1, a sample of channel 2, a sample of channel 3, and then the next sample of channels 0, 1, 2, 3, and so on.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b426c-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b426c-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b426c-134">Effets audio</span><span class="sxs-lookup"><span data-stu-id="b426c-134">Audio Effects</span></span>](audio-effects.md)
</dt> <dt>

[<span data-ttu-id="b426c-135">Présentation de XAPO</span><span class="sxs-lookup"><span data-stu-id="b426c-135">XAPO Overview</span></span>](xapo-overview.md)
</dt> </dl>

 

 
