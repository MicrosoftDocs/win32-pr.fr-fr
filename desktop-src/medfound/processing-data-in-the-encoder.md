---
description: Traitement des données dans l’encodeur
ms.assetid: 7be4c5e7-db2c-4063-8e5c-af6ffb861aa5
title: Traitement des données dans l’encodeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 666c2a2ff2139aadcb489022eb9b324eff1de523551244c2fd12ad0e11f68f1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238730"
---
# <a name="processing-data-in-the-encoder"></a>Traitement des données dans l’encodeur

Après avoir négocié le type d’entrée et le type de sortie pour la table MFT de l’encodeur, comme décrit dans [négociation de type de média sur l’encodeur](media-type-negotiation-on-the-encoder.md), vous pouvez commencer à traiter des exemples de données multimédias. Les données sont transmises sous forme d’exemples de supports (interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) ) et sont également reçus à partir de la sortie en tant qu’exemples de médias.

Avant d’envoyer des données à l’encodeur en vue de leur traitement, vous devez allouer un échantillon de support et ajouter un ou plusieurs tampons de média contenant des données multimédias qui doivent être encodées. Appelez [**IMFTransform ::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) et transmettez un pointeur vers l’exemple de média alloué. En plus de l’exemple de support, **ProcessInput** a également besoin de l’identificateur de flux d’entrée. Pour récupérer l’identificateur de flux, appelez [**IMFTransform :: GetStreamIDs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids). Comme un encodeur est conçu pour avoir une seule sortie et une sortie, ces identificateurs de flux ont toujours la valeur 0.

Pour récupérer des données à partir de l’encodeur, appelez [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Avant d’appeler [**ProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput), vous devez déterminer si l’encodeur alloue les exemples de supports de sortie ou si vous devez le faire explicitement. Pour ce faire, appelez [**IMFTransform :: GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo). Cela retourne des informations sur l’exemple de support de sortie dans la structure d' [**\_ informations du \_ flux \_ de sortie MFT**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_stream_info) . Si l’encodeur alloue des exemples de médias, il retourne le \_ flux de sortie MFT \_ \_ fournit \_ des exemples d’indicateurs dans le membre **dwFlags** et le membre **cbSize** contient la valeur zéro. Si l’encodeur s’attend à allouer la mémoire tampon de sortie, créez l’exemple de support de sortie et la mémoire tampon de média associée en fonction de la taille retournée dans **cbSize**. Quand vous appelez [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample), passer un pointeur vers l’exemple de support nouvellement créé. Pendant la session d’encodage, l’encodeur remplit les tampons de média, pointés par l’exemple de support de sortie, avec les données encodées.

Pour démarrer la session d’encodage, transmettez l’exemple de média d’entrée à l’encodeur en appelant [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput). L’encodeur commence le traitement et les données et produit un ou plusieurs échantillons de média de sortie qui doivent être récupérés par [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) tant qu’il retourne MF \_ E \_ Transform a \_ besoin d’une \_ \_ entrée supplémentaire. Si vous appelez **ProcessInput** pour passer davantage d’entrées tant qu’il y a des données de sortie à récupérer, **PROCESSINPUT** échoue avec MF \_ E \_ NOTACCEPTING. L’encodeur n’accepte plus d’entrée tant que le client n’a pas appelé **ProcessOutput** au moins une fois.

Vous devez définir des horodatages précis et des durées pour tous les exemples d’entrée passés. Les horodatages ne sont pas strictement obligatoires, mais ils permettent de maintenir la synchronisation audio/vidéo. Si vous n’avez pas les horodatages de vos échantillons, il est préférable de les exclure de l’utilisation de valeurs incertaines.

## <a name="encoder-processing-example"></a>Exemple de traitement d’encodeur

L’exemple de code suivant montre comment appeler [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) pour récupérer un exemple encodé. Pour obtenir le contexte complet de cet exemple, consultez [exemple de code d’encodeur](encoder-example-code.md).


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Multiplexeur ASF](asf-multiplexer.md)
</dt> <dt>

[Instanciation d’une table MFT d’encodeur](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Encodeurs multimédias](windows-media-encoders.md)
</dt> </dl>

 

 



