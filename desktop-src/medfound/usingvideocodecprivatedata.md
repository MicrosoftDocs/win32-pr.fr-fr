---
description: Utilisation de données privées de codec vidéo
ms.assetid: 0cc24fe4-a5b6-4805-8c8e-3066d12ec4bd
title: Utilisation de données privées de codec vidéo (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83e86fc31a50d2c4e553b5947717ea930698d812
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533822"
---
# <a name="using-video-codec-private-data-microsoft-media-foundation"></a><span data-ttu-id="da508-103">Utilisation de données privées de codec vidéo (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="da508-103">Using Video Codec Private Data (Microsoft Media Foundation)</span></span>

<span data-ttu-id="da508-104">La sortie compressée générée par les codecs Windows Media Video 9 ne peut pas être décompressée correctement sans que des données soient fournies par l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="da508-104">The compressed output produced by the Windows Media Video 9 codecs cannot be properly decompressed without some data provided by the encoder.</span></span> <span data-ttu-id="da508-105">Ces données, appelées données privées du codec, doivent être ajoutées au type de média de sortie.</span><span class="sxs-lookup"><span data-stu-id="da508-105">This data, called codec private data, must be appended to the output media type.</span></span> <span data-ttu-id="da508-106">Vous pouvez récupérer les données privées du codec en appelant les méthodes de l’interface [IWMCodecPrivateData](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecprivatedata) .</span><span class="sxs-lookup"><span data-stu-id="da508-106">You can get the codec private data by calling the methods of the [IWMCodecPrivateData](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecprivatedata) interface.</span></span> <span data-ttu-id="da508-107">Transmettez la structure [**du \_ \_ type de média DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) dans le cas contraire à [IWMCodecPrivateData :: SetPartialOutputType](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-setpartialoutputtype).</span><span class="sxs-lookup"><span data-stu-id="da508-107">Pass the otherwise complete [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure to [IWMCodecPrivateData::SetPartialOutputType](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-setpartialoutputtype).</span></span> <span data-ttu-id="da508-108">Appelez ensuite [IWMCodecPrivateData :: GetPrivateData](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-getprivatedata) à deux reprises, une fois pour obtenir la taille des données, puis de nouveau pour copier les données dans une mémoire tampon de cette taille.</span><span class="sxs-lookup"><span data-stu-id="da508-108">Then call [IWMCodecPrivateData::GetPrivateData](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-getprivatedata) twice, once to get the size of the data, and then again to copy the data to a buffer of that size.</span></span> <span data-ttu-id="da508-109">Créez une mémoire tampon destinée à contenir la structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) avec les données privées ajoutées, puis copiez la structure et les données dans cette mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="da508-109">Create a new buffer to hold the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure with the private data appended, and copy the structure and the data to that buffer.</span></span> <span data-ttu-id="da508-110">Enfin, définissez le membre **pbFormat** de la structure de **\_ \_ type de média DMO** sur l’adresse de la mémoire tampon qui vient d’être créée et définissez le membre **cbFormat** sur la taille combinée, en octets, du **VIDEOINFOHEADER** et des données privées.</span><span class="sxs-lookup"><span data-stu-id="da508-110">Finally, set the **pbFormat** member of the **DMO\_MEDIA\_TYPE** structure to the address of the newly created buffer and set the **cbFormat** member to the combined size, in bytes, of the **VIDEOINFOHEADER** and the private data.</span></span>

<span data-ttu-id="da508-111">Si vous utilisez MediaFoundation, vous pouvez construire une structure de [**\_ \_ type de média DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) à partir d’une interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) en appelant [**MFCreateAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype).</span><span class="sxs-lookup"><span data-stu-id="da508-111">If you are using MediaFoundation you can construct a [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure from an [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface by calling [**MFCreateAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype).</span></span>

<span data-ttu-id="da508-112">Vous devez utiliser les données privées du codec obtenues après avoir défini les propriétés sur l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="da508-112">You must use the codec private data obtained after first setting the properties on the encoder.</span></span> <span data-ttu-id="da508-113">Si des propriétés sont modifiées, vous devez vous procurer de nouvelles données privées.</span><span class="sxs-lookup"><span data-stu-id="da508-113">If any properties are changed, you must get new private data.</span></span> <span data-ttu-id="da508-114">Si vous n’utilisez pas les données privées obtenues après que toutes les propriétés ont été définies pour la session d’encodage, le décodeur risque de ne pas pouvoir décompresser les données.</span><span class="sxs-lookup"><span data-stu-id="da508-114">If you do not use the private data obtained after all the properties are set for the encoding session, the decoder may not be able to decompress the data.</span></span>

<span data-ttu-id="da508-115">L’exemple de code suivant montre comment obtenir les données privées d’un type de vidéo :</span><span class="sxs-lookup"><span data-stu-id="da508-115">The following code example demonstrates how to obtain the private data for a video type:</span></span>


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
> <span data-ttu-id="da508-116">Il n’est pas garanti que les données privées du codec fournies par un encodeur vidéo soient les mêmes que celles fournies par une implémentation différente du même codec pour la même configuration.</span><span class="sxs-lookup"><span data-stu-id="da508-116">The codec private data delivered by a video encoder is not guaranteed to be the same as the private data delivered by a different implementation of the same codec for the same configuration.</span></span> <span data-ttu-id="da508-117">Vous devez toujours générer cette valeur à l’aide des étapes décrites dans cette rubrique. ne copiez jamais les données privées d’un autre fichier.</span><span class="sxs-lookup"><span data-stu-id="da508-117">You must always generate this value using the steps in this topic; never copy the private data from another file.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="da508-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="da508-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da508-119">Configuration de l’encodage vidéo</span><span class="sxs-lookup"><span data-stu-id="da508-119">Configuring Video Encoding</span></span>](configuringvideoencoding.md)
</dt> <dt>

[<span data-ttu-id="da508-120">Utilisation de la vidéo</span><span class="sxs-lookup"><span data-stu-id="da508-120">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 
