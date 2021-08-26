---
description: Utilisation de données privées de codec vidéo
ms.assetid: 0cc24fe4-a5b6-4805-8c8e-3066d12ec4bd
title: Utilisation de données privées de codec vidéo (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7e417d4d83cc3ae3174e1bbf3310a6abb2900e2c5f3323192a8d17643e4066f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887089"
---
# <a name="using-video-codec-private-data-microsoft-media-foundation"></a>Utilisation de données privées de codec vidéo (Microsoft Media Foundation)

la sortie compressée générée par les codecs Windows Media Video 9 ne peut pas être décompressée correctement sans que des données soient fournies par l’encodeur. Ces données, appelées données privées du codec, doivent être ajoutées au type de média de sortie. Vous pouvez récupérer les données privées du codec en appelant les méthodes de l’interface [IWMCodecPrivateData](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecprivatedata) . transmettez le DMO la structure du [**\_ \_ TYPE de média**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) à [IWMCodecPrivateData :: SetPartialOutputType](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-setpartialoutputtype). Appelez ensuite [IWMCodecPrivateData :: GetPrivateData](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-getprivatedata) à deux reprises, une fois pour obtenir la taille des données, puis de nouveau pour copier les données dans une mémoire tampon de cette taille. Créez une mémoire tampon destinée à contenir la structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) avec les données privées ajoutées, puis copiez la structure et les données dans cette mémoire tampon. enfin, définissez le membre **pbFormat** de la structure de **\_ \_ TYPE de média DMO** sur l’adresse de la mémoire tampon nouvellement créée et définissez le membre **cbFormat** sur la taille combinée, en octets, du **VIDEOINFOHEADER** et des données privées.

si vous utilisez MediaFoundation, vous pouvez construire une structure de [**\_ \_ TYPE de média DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) à partir d’une interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) en appelant [**MFCreateAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype).

Vous devez utiliser les données privées du codec obtenues après avoir défini les propriétés sur l’encodeur. Si des propriétés sont modifiées, vous devez vous procurer de nouvelles données privées. Si vous n’utilisez pas les données privées obtenues après que toutes les propriétés ont été définies pour la session d’encodage, le décodeur risque de ne pas pouvoir décompresser les données.

L’exemple de code suivant montre comment obtenir les données privées d’un type de vidéo :


```
HRESULT GetFinalOutputType(DMO_MEDIA_TYPE* pMedia, IMediaObject* pDMO)
{
    // WARNING //
    // This function does not deallocate the memory pointed to by 
    // pMedia->pbFormat. If the VIDEOINFOHEADER referenced by pbFormat
    // was dynamically allocated, a reference to it must be kept before
    //  calling this function so that it can be freed.

    // Perform simple parameter checks.
    if(pMedia == NULL || pDMO == NULL)
        return E_POINTER;
    if(pMedia->formattype != MEDIATYPE_VideoInfo)
        return E_INVALIDARG;

    HRESULT hr = S_OK;

    IWMCodecPrivateData* pPrivData = NULL;
    BYTE* pbData = NULL;
    DWORD cbData = 0;

    BYTE* pbNewVidInf  = NULL;
    DWORD cbNewVidInf  = 0;
    BYTE* pbNewPriv    = NULL;

    // Get the private data interface.
    hr = pDMO->QueryInterface(IID_IWMCodecPrivateData,
                              (void**)&pPrivData);
    GOTO_EXIT_IF_FAILED(hr);

    // Set the partial media type.
    hr = pPrivData->SetPartialOutputType(pMedia);
    GOTO_EXIT_IF_FAILED(hr);

    // Get the size of the private data.
    hr = pPrivData->GetPrivateData(NULL, &cbData);
    GOTO_EXIT_IF_FAILED(hr);

    // Allocate memory for the private data.
    pbData = new BYTE[cbData];
    if(pbData == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto Exit:
    }

    // Get the private data.
    hr = pPrivData->GetPrivateData(pbData, &cbData);

    // Allocate memory for the new VIDEOINFOHEADER.
    cbNewVidInf = pMedia->cbFormat + cbData;
    pbNewVidInf = new BYTE[cbNewVidInf];

    // Copy the VIDEOINFOHEADER to the new buffer.
    memcpy((void*)pbNewVidInf, (void*)pMedia->pbFormat, pMedia->cbFormat);

    // Get the address of the first byte following the VIDEOINFOHEADER.
    pbNewPriv = pbNewVidInf + pMedia->cbFormat;

    // Copy the private data to the new buffer.
    memcpy((void*)pbNewPriv, (void*)pbData, cbData);

    // Set the new VIDEOINFOHEADER in the DMO_MEDIA_TYPE.
    pMedia->pbFormat = pbNewVidInf;
    pMedia->cbFormat = cbNewVidInf;

Exit:
    SAFE_RELEASE(pPrivData);
    SAFE_ARRAY_DELETE(pbData);
    pbNewPriv = NULL;
    return hr;
}
```



> [!Note]  
> Il n’est pas garanti que les données privées du codec fournies par un encodeur vidéo soient les mêmes que celles fournies par une implémentation différente du même codec pour la même configuration. Vous devez toujours générer cette valeur à l’aide des étapes décrites dans cette rubrique. ne copiez jamais les données privées d’un autre fichier.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configuration de l’encodage vidéo](configuringvideoencoding.md)
</dt> <dt>

[Utilisation de la vidéo](workingwithvideo.md)
</dt> </dl>

 

 
