---
description: Ce didacticiel utilise le writer de récepteur pour encoder un fichier vidéo.
ms.assetid: 3E297366-0863-4E89-A0D5-438CD1FC5AF9
title: 'Didacticiel : utilisation de l’enregistreur récepteur pour encoder une vidéo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3e6095355e18db6c8335cadcbc4afc56b35406
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516998"
---
# <a name="tutorial-using-the-sink-writer-to-encode-video"></a><span data-ttu-id="51620-103">Didacticiel : utilisation de l’enregistreur récepteur pour encoder une vidéo</span><span class="sxs-lookup"><span data-stu-id="51620-103">Tutorial: Using the Sink Writer to Encode Video</span></span>

<span data-ttu-id="51620-104">Ce didacticiel utilise le [writer de récepteur](sink-writer.md) pour encoder un fichier vidéo.</span><span class="sxs-lookup"><span data-stu-id="51620-104">This tutorial uses the [Sink Writer](sink-writer.md) to encode a video file.</span></span>

## <a name="define-the-video-format"></a><span data-ttu-id="51620-105">Définir le format vidéo</span><span class="sxs-lookup"><span data-stu-id="51620-105">Define the Video Format</span></span>

<span data-ttu-id="51620-106">Pour plus de simplicité, ce didacticiel utilise un format vidéo fixe, défini par les constantes suivantes :</span><span class="sxs-lookup"><span data-stu-id="51620-106">For simplicity, this tutorial uses a fixed video format, defined by the following constants:</span></span>


```C++
// Format constants
const UINT32 VIDEO_WIDTH = 640;
const UINT32 VIDEO_HEIGHT = 480;
const UINT32 VIDEO_FPS = 30;
const UINT64 VIDEO_FRAME_DURATION = 10 * 1000 * 1000 / VIDEO_FPS;
const UINT32 VIDEO_BIT_RATE = 800000;
const GUID   VIDEO_ENCODING_FORMAT = MFVideoFormat_WMV3;
const GUID   VIDEO_INPUT_FORMAT = MFVideoFormat_RGB32;
const UINT32 VIDEO_PELS = VIDEO_WIDTH * VIDEO_HEIGHT;
const UINT32 VIDEO_FRAME_COUNT = 20 * VIDEO_FPS;
```



<span data-ttu-id="51620-107">Ces constantes spécifient les paramètres suivants du format vidéo :</span><span class="sxs-lookup"><span data-stu-id="51620-107">These constants specify the following parameters of the video format:</span></span>

-   <span data-ttu-id="51620-108">Taille de la trame (largeur et hauteur)</span><span class="sxs-lookup"><span data-stu-id="51620-108">Frame size (width and height)</span></span>
-   <span data-ttu-id="51620-109">Images par seconde.</span><span class="sxs-lookup"><span data-stu-id="51620-109">Frames per second.</span></span>
-   <span data-ttu-id="51620-110">Vitesse de transmission encodée.</span><span class="sxs-lookup"><span data-stu-id="51620-110">Encoded bit rate.</span></span>
-   <span data-ttu-id="51620-111">Format d’encodage, Windows Media Video 9 (**MFVideoFormat \_ WMV3**).</span><span class="sxs-lookup"><span data-stu-id="51620-111">Encoding format, which is Windows Media Video 9 (**MFVideoFormat\_WMV3**).</span></span>
-   <span data-ttu-id="51620-112">Format d’entrée, qui est 32 bits RGB.</span><span class="sxs-lookup"><span data-stu-id="51620-112">Input format, which is 32-bit RGB.</span></span>
-   <span data-ttu-id="51620-113">Durée du fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="51620-113">Duration of the output file.</span></span>

<span data-ttu-id="51620-114">Le programme utilise ces constantes pour créer les types de média qui décrivent le format.</span><span class="sxs-lookup"><span data-stu-id="51620-114">The program uses these constants to create the media types that describe the format.</span></span> <span data-ttu-id="51620-115">Dans une application réelle, vous pouvez généralement prendre en charge une plage de profils d’encodage.</span><span class="sxs-lookup"><span data-stu-id="51620-115">In a real application, you would typically support a range of encoding profiles.</span></span>

## <a name="create-an-uncompressed-video-frame"></a><span data-ttu-id="51620-116">Créer une image vidéo non compressée</span><span class="sxs-lookup"><span data-stu-id="51620-116">Create an Uncompressed Video Frame</span></span>

<span data-ttu-id="51620-117">Par ailleurs, pour des raisons de simplicité, ce didacticiel utilise une image vidéo statique comme entrée.</span><span class="sxs-lookup"><span data-stu-id="51620-117">Also for simplicity, this tutorial uses a static video frame as input.</span></span> <span data-ttu-id="51620-118">La trame vidéo contient un rectangle vert plein et est générée par programme.</span><span class="sxs-lookup"><span data-stu-id="51620-118">The video frame contains a solid green rectangle and is generated programmatically.</span></span> <span data-ttu-id="51620-119">La trame vidéo est stockée dans une variable globale sous la forme d’un tableau de **DWORD** s :</span><span class="sxs-lookup"><span data-stu-id="51620-119">The video frame is stored in a global variable as an array of **DWORD** s:</span></span>


```C++
// Buffer to hold the video frame data.
DWORD videoFrameBuffer[VIDEO_PELS];
```



<span data-ttu-id="51620-120">Le code suivant affecte la valeur vert à chaque pixel du cadre :</span><span class="sxs-lookup"><span data-stu-id="51620-120">The following code sets every pixel in the frame to green:</span></span>


```C++
    // Set all pixels to green
    for (DWORD i = 0; i < VIDEO_PELS; ++i)
    {
        videoFrameBuffer[i] = 0x0000FF00;
    }
```



## <a name="initialize-the-sink-writer"></a><span data-ttu-id="51620-121">Initialiser le writer du récepteur</span><span class="sxs-lookup"><span data-stu-id="51620-121">Initialize the Sink Writer</span></span>

<span data-ttu-id="51620-122">Pour initialiser le writer du récepteur, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="51620-122">To initialize the sink writer, perform the following steps.</span></span>

1.  <span data-ttu-id="51620-123">Appelez [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) pour créer une nouvelle instance de l’enregistreur du récepteur.</span><span class="sxs-lookup"><span data-stu-id="51620-123">Call [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) to create a new instance of the sink writer.</span></span>
2.  <span data-ttu-id="51620-124">Créez un type de média qui décrit la vidéo encodée.</span><span class="sxs-lookup"><span data-stu-id="51620-124">Create a media type that describes the encoded video.</span></span>
3.  <span data-ttu-id="51620-125">Transmettez ce type de média à la méthode [**IMFSinkWriter :: AddStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-addstream) .</span><span class="sxs-lookup"><span data-stu-id="51620-125">Pass this media type to the [**IMFSinkWriter::AddStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-addstream) method.</span></span>
4.  <span data-ttu-id="51620-126">Créez un deuxième type de média qui décrit l’entrée non compressée.</span><span class="sxs-lookup"><span data-stu-id="51620-126">Create a second media type that describes the uncompressed input.</span></span>
5.  <span data-ttu-id="51620-127">Transmettez le type de média non compressé à la méthode [**IMFSinkWriter :: SetInputMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-setinputmediatype) .</span><span class="sxs-lookup"><span data-stu-id="51620-127">Pass the uncompressed media type to the [**IMFSinkWriter::SetInputMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-setinputmediatype) method.</span></span>
6.  <span data-ttu-id="51620-128">Appelez la méthode [**IMFSinkWriter :: BeginWriting**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-beginwriting) .</span><span class="sxs-lookup"><span data-stu-id="51620-128">Call the [**IMFSinkWriter::BeginWriting**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-beginwriting) method.</span></span>
7.  <span data-ttu-id="51620-129">L’enregistreur du récepteur est maintenant prêt à accepter les exemples d’entrée.</span><span class="sxs-lookup"><span data-stu-id="51620-129">The sink writer is now ready to accept input samples.</span></span>

<span data-ttu-id="51620-130">Le code suivant illustre ces étapes.</span><span class="sxs-lookup"><span data-stu-id="51620-130">The following code shows these steps.</span></span>


```C++
HRESULT InitializeSinkWriter(IMFSinkWriter **ppWriter, DWORD *pStreamIndex)
{
    *ppWriter = NULL;
    *pStreamIndex = NULL;

    IMFSinkWriter   *pSinkWriter = NULL;
    IMFMediaType    *pMediaTypeOut = NULL;   
    IMFMediaType    *pMediaTypeIn = NULL;   
    DWORD           streamIndex;     

    HRESULT hr = MFCreateSinkWriterFromURL(L"output.wmv", NULL, NULL, &pSinkWriter);

    // Set the output media type.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pMediaTypeOut);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);     
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetGUID(MF_MT_SUBTYPE, VIDEO_ENCODING_FORMAT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetUINT32(MF_MT_AVG_BITRATE, VIDEO_BIT_RATE);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(pMediaTypeOut, MF_MT_FRAME_SIZE, VIDEO_WIDTH, VIDEO_HEIGHT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeOut, MF_MT_FRAME_RATE, VIDEO_FPS, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeOut, MF_MT_PIXEL_ASPECT_RATIO, 1, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->AddStream(pMediaTypeOut, &streamIndex);   
    }

    // Set the input media type.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pMediaTypeIn);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetGUID(MF_MT_SUBTYPE, VIDEO_INPUT_FORMAT);     
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(pMediaTypeIn, MF_MT_FRAME_SIZE, VIDEO_WIDTH, VIDEO_HEIGHT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeIn, MF_MT_FRAME_RATE, VIDEO_FPS, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeIn, MF_MT_PIXEL_ASPECT_RATIO, 1, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->SetInputMediaType(streamIndex, pMediaTypeIn, NULL);   
    }

    // Tell the sink writer to start accepting data.
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->BeginWriting();
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppWriter = pSinkWriter;
        (*ppWriter)->AddRef();
        *pStreamIndex = streamIndex;
    }

    SafeRelease(&pSinkWriter);
    SafeRelease(&pMediaTypeOut);
    SafeRelease(&pMediaTypeIn);
    return hr;
}
```



<span data-ttu-id="51620-131">La plupart des étapes de l’exemple de code précédent sont la définition des attributs de type de média pour les deux types de média.</span><span class="sxs-lookup"><span data-stu-id="51620-131">Most of the steps in previous code example are setting the media type attributes for the two media types.</span></span> <span data-ttu-id="51620-132">Les détails des types de médias dépendent du contenu source et du profil d’encodage souhaité.</span><span class="sxs-lookup"><span data-stu-id="51620-132">The details of the media types will depend on your source content and the desired encoding profile.</span></span>

## <a name="send-video-frames-to-the-sink-writer"></a><span data-ttu-id="51620-133">Envoyer des trames vidéo à l’enregistreur du récepteur</span><span class="sxs-lookup"><span data-stu-id="51620-133">Send Video Frames to the Sink Writer</span></span>

<span data-ttu-id="51620-134">Pour envoyer une image vidéo à l’enregistreur du récepteur, appelez la méthode [**IMFSinkWriter :: WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) .</span><span class="sxs-lookup"><span data-stu-id="51620-134">To send a video frame to the sink writer, call the [**IMFSinkWriter::WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) method.</span></span> <span data-ttu-id="51620-135">La méthode **WriteSample** prend un pointeur vers l’interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , qui représente un *exemple* d’objet multimédia.</span><span class="sxs-lookup"><span data-stu-id="51620-135">The **WriteSample** method takes a pointer to the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, which represents a *media sample* object.</span></span> <span data-ttu-id="51620-136">L’exemple de support contient un objet de *mémoire tampon de média* qui, à son tour, contient un pointeur vers l’image vidéo.</span><span class="sxs-lookup"><span data-stu-id="51620-136">The media sample contains a *media buffer* object, which in turn contains a pointer to the video frame.</span></span> <span data-ttu-id="51620-137">Pour plus d’informations sur les exemples de supports et la mémoire tampon, consultez les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="51620-137">For more information about media samples and buffer, see the following topics.</span></span>

-   [<span data-ttu-id="51620-138">Exemples de supports</span><span class="sxs-lookup"><span data-stu-id="51620-138">Media Samples</span></span>](media-samples.md)
-   [<span data-ttu-id="51620-139">Mémoires tampons de média</span><span class="sxs-lookup"><span data-stu-id="51620-139">Media Buffers</span></span>](media-buffers.md)

<span data-ttu-id="51620-140">Selon votre application, vous pouvez récupérer les exemples de média à partir du [lecteur source](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="51620-140">Depending on your application, you might get the media samples from the [Source Reader](source-reader.md).</span></span> <span data-ttu-id="51620-141">Vous pouvez également créer les exemples de média et manipuler directement les données dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="51620-141">Alternatively, you can create the media samples and directly manipulate the data in the buffer.</span></span> <span data-ttu-id="51620-142">Le code suivant illustre la deuxième approche.</span><span class="sxs-lookup"><span data-stu-id="51620-142">The following code shows the second approach.</span></span> <span data-ttu-id="51620-143">Il crée une mémoire tampon et écrit une seule image vidéo dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="51620-143">It creates a memory buffer and writes a single video frame to the buffer.</span></span> <span data-ttu-id="51620-144">Ensuite, il ajoute ce tampon à un exemple de média et envoie l’exemple de support à l’enregistreur du récepteur.</span><span class="sxs-lookup"><span data-stu-id="51620-144">Then it adds that buffer to a media sample, and sends the media sample to the sink writer.</span></span>


```C++
HRESULT WriteFrame(
    IMFSinkWriter *pWriter, 
    DWORD streamIndex, 
    const LONGLONG& rtStart        // Time stamp.
    )
{
    IMFSample *pSample = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    const LONG cbWidth = 4 * VIDEO_WIDTH;
    const DWORD cbBuffer = cbWidth * VIDEO_HEIGHT;

    BYTE *pData = NULL;

    // Create a new memory buffer.
    HRESULT hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);

    // Lock the buffer and copy the video frame to the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFCopyImage(
            pData,                      // Destination buffer.
            cbWidth,                    // Destination stride.
            (BYTE*)videoFrameBuffer,    // First row in source image.
            cbWidth,                    // Source stride.
            cbWidth,                    // Image width in bytes.
            VIDEO_HEIGHT                // Image height in pixels.
            );
    }
    if (pBuffer)
    {
        pBuffer->Unlock();
    }

    // Set the data length of the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbBuffer);
    }

    // Create a media sample and add the buffer to the sample.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateSample(&pSample);
    }
    if (SUCCEEDED(hr))
    {
        hr = pSample->AddBuffer(pBuffer);
    }

    // Set the time stamp and the duration.
    if (SUCCEEDED(hr))
    {
        hr = pSample->SetSampleTime(rtStart);
    }
    if (SUCCEEDED(hr))
    {
        hr = pSample->SetSampleDuration(VIDEO_FRAME_DURATION);
    }

    // Send the sample to the Sink Writer.
    if (SUCCEEDED(hr))
    {
        hr = pWriter->WriteSample(streamIndex, pSample);
    }

    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



<span data-ttu-id="51620-145">Ce code effectue les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="51620-145">This code performs the following steps.</span></span>

1.  <span data-ttu-id="51620-146">Appelez [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) pour créer un objet de mémoire tampon de média.</span><span class="sxs-lookup"><span data-stu-id="51620-146">Call [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) to create a media buffer object.</span></span> <span data-ttu-id="51620-147">Cette fonction alloue la mémoire pour la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="51620-147">This function allocates the memory for the buffer.</span></span>
2.  <span data-ttu-id="51620-148">Appelez [**IMFMediaBuffer :: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) pour verrouiller la mémoire tampon et obtenir un pointeur vers la mémoire.</span><span class="sxs-lookup"><span data-stu-id="51620-148">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to lock the buffer and get a pointer to the memory.</span></span>
3.  <span data-ttu-id="51620-149">Appelez [**MFCopyImage**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) pour copier l’image vidéo dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="51620-149">Call [**MFCopyImage**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) to copy the video frame into the buffer.</span></span>
    > [!Note]  
    > <span data-ttu-id="51620-150">Dans cet exemple particulier, l’utilisation de **memcpy** fonctionnera aussi bien.</span><span class="sxs-lookup"><span data-stu-id="51620-150">In this particular example, using **memcpy** would work just as well.</span></span> <span data-ttu-id="51620-151">Toutefois, la fonction [**MFCopyImage**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) gère correctement le cas où le Stride de l’image source ne correspond pas à la mémoire tampon cible.</span><span class="sxs-lookup"><span data-stu-id="51620-151">However, the [**MFCopyImage**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) function correctly handles the case where the stride of the source image does not match the target buffer.</span></span> <span data-ttu-id="51620-152">Pour plus d’informations, consultez l' [image Stride](image-stride.md).</span><span class="sxs-lookup"><span data-stu-id="51620-152">For more information, see [Image Stride](image-stride.md).</span></span>

     

4.  <span data-ttu-id="51620-153">Appelez [**IMFMediaBuffer :: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) pour déverrouiller la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="51620-153">Call [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) to unlock the buffer.</span></span>
5.  <span data-ttu-id="51620-154">Appelez [**IMFMediaBuffer :: SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) pour mettre à jour la longueur des données valides dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="51620-154">Call [**IMFMediaBuffer::SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) to update the length of the valid data in the buffer.</span></span> <span data-ttu-id="51620-155">(Sinon, cette valeur est définie par défaut sur zéro.)</span><span class="sxs-lookup"><span data-stu-id="51620-155">(Otherwise, this value defaults to zero.)</span></span>
6.  <span data-ttu-id="51620-156">Appelez [**MFCreateSample**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) pour créer un exemple d’objet de support.</span><span class="sxs-lookup"><span data-stu-id="51620-156">Call [**MFCreateSample**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) to create a media sample object.</span></span>
7.  <span data-ttu-id="51620-157">Appelez [**IMFSample :: AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer) pour ajouter la mémoire tampon du média à l’exemple de support.</span><span class="sxs-lookup"><span data-stu-id="51620-157">Call [**IMFSample::AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer) to add the media buffer to the media sample.</span></span>
8.  <span data-ttu-id="51620-158">Appelez [**IMFSample :: SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime) pour définir l’horodatage de la trame vidéo.</span><span class="sxs-lookup"><span data-stu-id="51620-158">Call [**IMFSample::SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime) to set the time stamp for the video frame.</span></span>
9.  <span data-ttu-id="51620-159">Appelez [**IMFSample :: SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration) pour définir la durée de l’image vidéo.</span><span class="sxs-lookup"><span data-stu-id="51620-159">Call [**IMFSample::SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration) to set the duration of the video frame.</span></span>
10. <span data-ttu-id="51620-160">Appelez [**IMFSinkWriter :: WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) pour envoyer l’exemple de support au writer du récepteur.</span><span class="sxs-lookup"><span data-stu-id="51620-160">Call [**IMFSinkWriter::WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) to send the media sample to the sink writer.</span></span>

## <a name="write-the-main-function"></a><span data-ttu-id="51620-161">Écrire la fonction main</span><span class="sxs-lookup"><span data-stu-id="51620-161">Write the main Function</span></span>

<span data-ttu-id="51620-162">À l’intérieur de la `main` fonction, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="51620-162">Inside the `main` function, perform the following steps.</span></span>

1.  <span data-ttu-id="51620-163">Appelez [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) pour initialiser la bibliothèque com.</span><span class="sxs-lookup"><span data-stu-id="51620-163">Call [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) to initialize the COM library.</span></span>
2.  <span data-ttu-id="51620-164">Appelez [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) pour initialiser Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="51620-164">Call [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) to initialize Microsoft Media Foundation.</span></span>
3.  <span data-ttu-id="51620-165">Créez le writer du récepteur.</span><span class="sxs-lookup"><span data-stu-id="51620-165">Create the sink writer.</span></span>
4.  <span data-ttu-id="51620-166">Envoyer des trames vidéo à l’enregistreur du récepteur.</span><span class="sxs-lookup"><span data-stu-id="51620-166">Send video frames to the sink writer.</span></span>
5.  <span data-ttu-id="51620-167">Appelez [**IMFSinkWriter :: Finalize**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-finalize) pour finaliser le fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="51620-167">Call [**IMFSinkWriter::Finalize**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-finalize) to finalize the output file.</span></span>
6.  <span data-ttu-id="51620-168">Libère le pointeur vers le writer du récepteur.</span><span class="sxs-lookup"><span data-stu-id="51620-168">Release the pointer to the sink writer.</span></span>
7.  <span data-ttu-id="51620-169">Appelez [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span><span class="sxs-lookup"><span data-stu-id="51620-169">Call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span></span>
8.  <span data-ttu-id="51620-170">Appeler [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span><span class="sxs-lookup"><span data-stu-id="51620-170">Call [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span></span>


```C++
void main()
{
    // Set all pixels to green
    for (DWORD i = 0; i < VIDEO_PELS; ++i)
    {
        videoFrameBuffer[i] = 0x0000FF00;
    }

    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (SUCCEEDED(hr))
    {
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            IMFSinkWriter *pSinkWriter = NULL;
            DWORD stream;

            hr = InitializeSinkWriter(&pSinkWriter, &stream);
            if (SUCCEEDED(hr))
            {
                // Send frames to the sink writer.
                LONGLONG rtStart = 0;


                for (DWORD i = 0; i < VIDEO_FRAME_COUNT; ++i)
                {
                    hr = WriteFrame(pSinkWriter, stream, rtStart);
                    if (FAILED(hr))
                    {
                        break;
                    }
                    rtStart += VIDEO_FRAME_DURATION;
                }
            }
            if (SUCCEEDED(hr))
            {
                hr = pSinkWriter->Finalize();
            }
            SafeRelease(&pSinkWriter);
            MFShutdown();
        }
        CoUninitialize();
    }
}
```



## <a name="example-code"></a><span data-ttu-id="51620-171">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="51620-171">Example Code</span></span>

<span data-ttu-id="51620-172">Le code suivant illustre le programme complet.</span><span class="sxs-lookup"><span data-stu-id="51620-172">The following code shows the complete program.</span></span>


```C++
#include <Windows.h>
#include <mfapi.h>
#include <mfidl.h>
#include <Mfreadwrite.h>
#include <mferror.h>

#pragma comment(lib, "mfreadwrite")
#pragma comment(lib, "mfplat")
#pragma comment(lib, "mfuuid")

template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}

// Format constants
const UINT32 VIDEO_WIDTH = 640;
const UINT32 VIDEO_HEIGHT = 480;
const UINT32 VIDEO_FPS = 30;
const UINT64 VIDEO_FRAME_DURATION = 10 * 1000 * 1000 / VIDEO_FPS;
const UINT32 VIDEO_BIT_RATE = 800000;
const GUID   VIDEO_ENCODING_FORMAT = MFVideoFormat_WMV3;
const GUID   VIDEO_INPUT_FORMAT = MFVideoFormat_RGB32;
const UINT32 VIDEO_PELS = VIDEO_WIDTH * VIDEO_HEIGHT;
const UINT32 VIDEO_FRAME_COUNT = 20 * VIDEO_FPS;

// Buffer to hold the video frame data.
DWORD videoFrameBuffer[VIDEO_PELS];

HRESULT InitializeSinkWriter(IMFSinkWriter **ppWriter, DWORD *pStreamIndex)
{
    *ppWriter = NULL;
    *pStreamIndex = NULL;

    IMFSinkWriter   *pSinkWriter = NULL;
    IMFMediaType    *pMediaTypeOut = NULL;   
    IMFMediaType    *pMediaTypeIn = NULL;   
    DWORD           streamIndex;     

    HRESULT hr = MFCreateSinkWriterFromURL(L"output.wmv", NULL, NULL, &pSinkWriter);

    // Set the output media type.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pMediaTypeOut);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);     
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetGUID(MF_MT_SUBTYPE, VIDEO_ENCODING_FORMAT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetUINT32(MF_MT_AVG_BITRATE, VIDEO_BIT_RATE);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(pMediaTypeOut, MF_MT_FRAME_SIZE, VIDEO_WIDTH, VIDEO_HEIGHT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeOut, MF_MT_FRAME_RATE, VIDEO_FPS, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeOut, MF_MT_PIXEL_ASPECT_RATIO, 1, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->AddStream(pMediaTypeOut, &streamIndex);   
    }

    // Set the input media type.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pMediaTypeIn);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetGUID(MF_MT_SUBTYPE, VIDEO_INPUT_FORMAT);     
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(pMediaTypeIn, MF_MT_FRAME_SIZE, VIDEO_WIDTH, VIDEO_HEIGHT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeIn, MF_MT_FRAME_RATE, VIDEO_FPS, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeIn, MF_MT_PIXEL_ASPECT_RATIO, 1, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->SetInputMediaType(streamIndex, pMediaTypeIn, NULL);   
    }

    // Tell the sink writer to start accepting data.
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->BeginWriting();
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppWriter = pSinkWriter;
        (*ppWriter)->AddRef();
        *pStreamIndex = streamIndex;
    }

    SafeRelease(&pSinkWriter);
    SafeRelease(&pMediaTypeOut);
    SafeRelease(&pMediaTypeIn);
    return hr;
}

HRESULT WriteFrame(
    IMFSinkWriter *pWriter, 
    DWORD streamIndex, 
    const LONGLONG& rtStart        // Time stamp.
    )
{
    IMFSample *pSample = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    const LONG cbWidth = 4 * VIDEO_WIDTH;
    const DWORD cbBuffer = cbWidth * VIDEO_HEIGHT;

    BYTE *pData = NULL;

    // Create a new memory buffer.
    HRESULT hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);

    // Lock the buffer and copy the video frame to the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFCopyImage(
            pData,                      // Destination buffer.
            cbWidth,                    // Destination stride.
            (BYTE*)videoFrameBuffer,    // First row in source image.
            cbWidth,                    // Source stride.
            cbWidth,                    // Image width in bytes.
            VIDEO_HEIGHT                // Image height in pixels.
            );
    }
    if (pBuffer)
    {
        pBuffer->Unlock();
    }

    // Set the data length of the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbBuffer);
    }

    // Create a media sample and add the buffer to the sample.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateSample(&pSample);
    }
    if (SUCCEEDED(hr))
    {
        hr = pSample->AddBuffer(pBuffer);
    }

    // Set the time stamp and the duration.
    if (SUCCEEDED(hr))
    {
        hr = pSample->SetSampleTime(rtStart);
    }
    if (SUCCEEDED(hr))
    {
        hr = pSample->SetSampleDuration(VIDEO_FRAME_DURATION);
    }

    // Send the sample to the Sink Writer.
    if (SUCCEEDED(hr))
    {
        hr = pWriter->WriteSample(streamIndex, pSample);
    }

    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}

void main()
{
    // Set all pixels to green
    for (DWORD i = 0; i < VIDEO_PELS; ++i)
    {
        videoFrameBuffer[i] = 0x0000FF00;
    }

    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (SUCCEEDED(hr))
    {
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            IMFSinkWriter *pSinkWriter = NULL;
            DWORD stream;

            hr = InitializeSinkWriter(&pSinkWriter, &stream);
            if (SUCCEEDED(hr))
            {
                // Send frames to the sink writer.
                LONGLONG rtStart = 0;


                for (DWORD i = 0; i < VIDEO_FRAME_COUNT; ++i)
                {
                    hr = WriteFrame(pSinkWriter, stream, rtStart);
                    if (FAILED(hr))
                    {
                        break;
                    }
                    rtStart += VIDEO_FRAME_DURATION;
                }
            }
            if (SUCCEEDED(hr))
            {
                hr = pSinkWriter->Finalize();
            }
            SafeRelease(&pSinkWriter);
            MFShutdown();
        }
        CoUninitialize();
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="51620-173">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="51620-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51620-174">Enregistreur du récepteur</span><span class="sxs-lookup"><span data-stu-id="51620-174">Sink Writer</span></span>](sink-writer.md)
</dt> </dl>

 

 
