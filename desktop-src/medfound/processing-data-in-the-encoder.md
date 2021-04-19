---
description: Traitement des données dans l’encodeur
ms.assetid: 7be4c5e7-db2c-4063-8e5c-af6ffb861aa5
title: Traitement des données dans l’encodeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99b7fedef50df61851408d084b511497eacd0288
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529722"
---
# <a name="processing-data-in-the-encoder"></a><span data-ttu-id="bab9c-103">Traitement des données dans l’encodeur</span><span class="sxs-lookup"><span data-stu-id="bab9c-103">Processing Data in the Encoder</span></span>

<span data-ttu-id="bab9c-104">Après avoir négocié le type d’entrée et le type de sortie pour la table MFT de l’encodeur, comme décrit dans [négociation de type de média sur l’encodeur](media-type-negotiation-on-the-encoder.md), vous pouvez commencer à traiter des exemples de données multimédias.</span><span class="sxs-lookup"><span data-stu-id="bab9c-104">After you have negotiated the input type and output type for the encoder MFT, as described in [Media Type Negotiation on the Encoder](media-type-negotiation-on-the-encoder.md), you can start processing media data samples.</span></span> <span data-ttu-id="bab9c-105">Les données sont transmises sous forme d’exemples de supports (interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) ) et sont également reçus à partir de la sortie en tant qu’exemples de médias.</span><span class="sxs-lookup"><span data-stu-id="bab9c-105">The data is passed in form of media samples ([**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface) and also received from the output as media samples.</span></span>

<span data-ttu-id="bab9c-106">Avant d’envoyer des données à l’encodeur en vue de leur traitement, vous devez allouer un échantillon de support et ajouter un ou plusieurs tampons de média contenant des données multimédias qui doivent être encodées.</span><span class="sxs-lookup"><span data-stu-id="bab9c-106">Before sending data to the encoder for processing, you must allocate a media sample and add one of more media buffers containing media data that needs to be encoded.</span></span> <span data-ttu-id="bab9c-107">Appelez [**IMFTransform ::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) et transmettez un pointeur vers l’exemple de média alloué.</span><span class="sxs-lookup"><span data-stu-id="bab9c-107">Call [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) and pass a pointer to the allocated media sample.</span></span> <span data-ttu-id="bab9c-108">En plus de l’exemple de support, **ProcessInput** a également besoin de l’identificateur de flux d’entrée.</span><span class="sxs-lookup"><span data-stu-id="bab9c-108">In addition to the media sample, **ProcessInput** also needs the input stream identifier.</span></span> <span data-ttu-id="bab9c-109">Pour récupérer l’identificateur de flux, appelez [**IMFTransform :: GetStreamIDs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids).</span><span class="sxs-lookup"><span data-stu-id="bab9c-109">To get the stream identifier, call [**IMFTransform::GetStreamIDs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids).</span></span> <span data-ttu-id="bab9c-110">Comme un encodeur est conçu pour avoir une seule sortie et une sortie, ces identificateurs de flux ont toujours la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="bab9c-110">Because an encoder is designed to have only one and one output, these stream identifiers always have the value of 0.</span></span>

<span data-ttu-id="bab9c-111">Pour récupérer des données à partir de l’encodeur, appelez [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span><span class="sxs-lookup"><span data-stu-id="bab9c-111">To get data from the encoder, call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span></span> <span data-ttu-id="bab9c-112">Avant d’appeler [**ProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput), vous devez déterminer si l’encodeur alloue les exemples de supports de sortie ou si vous devez le faire explicitement.</span><span class="sxs-lookup"><span data-stu-id="bab9c-112">Before you call [**ProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput), you need to find out whether the encoder allocates the output media samples or you must do so explicitly.</span></span> <span data-ttu-id="bab9c-113">Pour ce faire, appelez [**IMFTransform :: GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo).</span><span class="sxs-lookup"><span data-stu-id="bab9c-113">To do this, call [**IMFTransform::GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo).</span></span> <span data-ttu-id="bab9c-114">Cela retourne des informations sur l’exemple de support de sortie dans la structure d' [**\_ informations du \_ flux \_ de sortie MFT**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_stream_info) .</span><span class="sxs-lookup"><span data-stu-id="bab9c-114">This returns output media sample information in the [**MFT\_OUTPUT\_STREAM\_INFO**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_stream_info) structure.</span></span> <span data-ttu-id="bab9c-115">Si l’encodeur alloue des exemples de médias, il retourne le \_ flux de sortie MFT \_ \_ fournit \_ des exemples d’indicateurs dans le membre **dwFlags** et le membre **cbSize** contient la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="bab9c-115">If the encoder allocates media samples, it returns the MFT\_OUTPUT\_STREAM\_PROVIDES\_SAMPLES flag in the **dwFlags** member and the **cbSize** member contains zero.</span></span> <span data-ttu-id="bab9c-116">Si l’encodeur s’attend à allouer la mémoire tampon de sortie, créez l’exemple de support de sortie et la mémoire tampon de média associée en fonction de la taille retournée dans **cbSize**.</span><span class="sxs-lookup"><span data-stu-id="bab9c-116">If the encoder expects you to allocate the output buffer, create the output media sample and the associated media buffer based on the size returned in **cbSize**.</span></span> <span data-ttu-id="bab9c-117">Quand vous appelez [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample), passer un pointeur vers l’exemple de support nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="bab9c-117">When you call [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample), pass a pointer to the newly created media sample.</span></span> <span data-ttu-id="bab9c-118">Pendant la session d’encodage, l’encodeur remplit les tampons de média, pointés par l’exemple de support de sortie, avec les données encodées.</span><span class="sxs-lookup"><span data-stu-id="bab9c-118">During the encoding session, the encoder fills the media buffers, pointed by the output media sample, with the encoded data.</span></span>

<span data-ttu-id="bab9c-119">Pour démarrer la session d’encodage, transmettez l’exemple de média d’entrée à l’encodeur en appelant [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span><span class="sxs-lookup"><span data-stu-id="bab9c-119">To start the encoding session, pass the input media sample to the encoder by calling [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span></span> <span data-ttu-id="bab9c-120">L’encodeur commence le traitement et les données et produit un ou plusieurs échantillons de média de sortie qui doivent être récupérés par [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) tant qu’il retourne MF \_ E \_ Transform a \_ besoin d’une \_ \_ entrée supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="bab9c-120">The encoder starts processing and the data and produces one or more output media samples that must be retrieved by [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) as long as it returns MF\_E\_TRANSFORM\_NEED\_MORE\_INPUT.</span></span> <span data-ttu-id="bab9c-121">Si vous appelez **ProcessInput** pour passer davantage d’entrées tant qu’il y a des données de sortie à récupérer, **PROCESSINPUT** échoue avec MF \_ E \_ NOTACCEPTING.</span><span class="sxs-lookup"><span data-stu-id="bab9c-121">If you call **ProcessInput** to pass more input as long as there is output data to be retrieved, **ProcessInput** fails with MF\_E\_NOTACCEPTING.</span></span> <span data-ttu-id="bab9c-122">L’encodeur n’accepte plus d’entrée tant que le client n’a pas appelé **ProcessOutput** au moins une fois.</span><span class="sxs-lookup"><span data-stu-id="bab9c-122">The encoder does not accept any more input until the client calls **ProcessOutput** at least once.</span></span>

<span data-ttu-id="bab9c-123">Vous devez définir des horodatages précis et des durées pour tous les exemples d’entrée passés.</span><span class="sxs-lookup"><span data-stu-id="bab9c-123">You should set accurate time stamps and durations for all input samples passed.</span></span> <span data-ttu-id="bab9c-124">Les horodatages ne sont pas strictement obligatoires, mais ils permettent de maintenir la synchronisation audio/vidéo.</span><span class="sxs-lookup"><span data-stu-id="bab9c-124">Time stamps are not strictly required but help maintain audio/video synchronization.</span></span> <span data-ttu-id="bab9c-125">Si vous n’avez pas les horodatages de vos échantillons, il est préférable de les exclure de l’utilisation de valeurs incertaines.</span><span class="sxs-lookup"><span data-stu-id="bab9c-125">If you do not have the time stamps for your samples it is better to leave them out than to use uncertain values.</span></span>

## <a name="encoder-processing-example"></a><span data-ttu-id="bab9c-126">Exemple de traitement d’encodeur</span><span class="sxs-lookup"><span data-stu-id="bab9c-126">Encoder Processing Example</span></span>

<span data-ttu-id="bab9c-127">L’exemple de code suivant montre comment appeler [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) pour récupérer un exemple encodé.</span><span class="sxs-lookup"><span data-stu-id="bab9c-127">The following example code shows how to call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) to get an encoded sample.</span></span> <span data-ttu-id="bab9c-128">Pour obtenir le contexte complet de cet exemple, consultez [exemple de code d’encodeur](encoder-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="bab9c-128">For the complete context of this example, see [Encoder Example Code](encoder-example-code.md).</span></span>


```C++
HRESULT CWmaEncoder::ProcessOutput(IMFSample **ppSample)
{
    if (m_pMFT == NULL)
    {
        return MF_E_NOT_INITIALIZED;
    }

    *ppSample = NULL;

    IMFMediaBuffer* pBufferOut = NULL;
    IMFSample* pSampleOut = NULL;

    DWORD dwStatus;
  
    MFT_OUTPUT_STREAM_INFO mftStreamInfo = { 0 };
    MFT_OUTPUT_DATA_BUFFER mftOutputData = { 0 };

    HRESULT hr = m_pMFT->GetOutputStreamInfo(m_dwOutputID, &mftStreamInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    //create a buffer for the output sample
    hr = MFCreateMemoryBuffer(mftStreamInfo.cbSize, &pBufferOut);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create the output sample
    hr = MFCreateSample(&pSampleOut);
    if (FAILED(hr))
    {
        goto done;
    }

    //Add the output buffer 
    hr = pSampleOut->AddBuffer(pBufferOut);
    if (FAILED(hr))
    {
        goto done;
    }
 
    //Set the output sample
    mftOutputData.pSample = pSampleOut;

    //Set the output id
    mftOutputData.dwStreamID = m_dwOutputID;

    //Generate the output sample
    hr = m_pMFT->ProcessOutput(0, 1, &mftOutputData, &dwStatus);
    if (hr == MF_E_TRANSFORM_NEED_MORE_INPUT)
    {
        hr = S_OK;
        goto done;
    }

    // TODO: Handle MF_E_TRANSFORM_STREAM_CHANGE

    if (FAILED(hr))
    {
        goto done;
    }

    *ppSample = pSampleOut;
    (*ppSample)->AddRef();

done:
    SafeRelease(&pBufferOut);
    SafeRelease(&pSampleOut);
    return hr;
};
```



## <a name="related-topics"></a><span data-ttu-id="bab9c-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bab9c-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bab9c-130">Multiplexeur ASF</span><span class="sxs-lookup"><span data-stu-id="bab9c-130">ASF Multiplexer</span></span>](asf-multiplexer.md)
</dt> <dt>

[<span data-ttu-id="bab9c-131">Instanciation d’une table MFT d’encodeur</span><span class="sxs-lookup"><span data-stu-id="bab9c-131">Instantiating an Encoder MFT</span></span>](instantiating-the-encoder-mft.md)
</dt> <dt>

[<span data-ttu-id="bab9c-132">Encodeurs Windows Media</span><span class="sxs-lookup"><span data-stu-id="bab9c-132">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 



