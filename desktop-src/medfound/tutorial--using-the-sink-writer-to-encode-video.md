---
description: Ce didacticiel utilise le writer de récepteur pour encoder un fichier vidéo.
ms.assetid: 3E297366-0863-4E89-A0D5-438CD1FC5AF9
title: 'Didacticiel : utilisation de l’enregistreur récepteur pour encoder une vidéo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3e6095355e18db6c8335cadcbc4afc56b35406
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235793"
---
# <a name="tutorial-using-the-sink-writer-to-encode-video"></a>Didacticiel : utilisation de l’enregistreur récepteur pour encoder une vidéo

Ce didacticiel utilise le [writer de récepteur](sink-writer.md) pour encoder un fichier vidéo.

## <a name="define-the-video-format"></a>Définir le format vidéo

Pour plus de simplicité, ce didacticiel utilise un format vidéo fixe, défini par les constantes suivantes :


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



Ces constantes spécifient les paramètres suivants du format vidéo :

-   Taille de la trame (largeur et hauteur)
-   Images par seconde.
-   Vitesse de transmission encodée.
-   format d’encodage, Windows Media Video 9 (**MFVideoFormat \_ WMV3**).
-   Format d’entrée, qui est 32 bits RGB.
-   Durée du fichier de sortie.

Le programme utilise ces constantes pour créer les types de média qui décrivent le format. Dans une application réelle, vous pouvez généralement prendre en charge une plage de profils d’encodage.

## <a name="create-an-uncompressed-video-frame"></a>Créer une image vidéo non compressée

Par ailleurs, pour des raisons de simplicité, ce didacticiel utilise une image vidéo statique comme entrée. La trame vidéo contient un rectangle vert plein et est générée par programme. La trame vidéo est stockée dans une variable globale sous la forme d’un tableau de **DWORD** s :


```C++
// Buffer to hold the video frame data.
DWORD videoFrameBuffer[VIDEO_PELS];
```



Le code suivant affecte la valeur vert à chaque pixel du cadre :


```C++
    // Set all pixels to green
    for (DWORD i = 0; i < VIDEO_PELS; ++i)
    {
        videoFrameBuffer[i] = 0x0000FF00;
    }
```



## <a name="initialize-the-sink-writer"></a>Initialiser le writer du récepteur

Pour initialiser le writer du récepteur, procédez comme suit.

1.  Appelez [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) pour créer une nouvelle instance de l’enregistreur du récepteur.
2.  Créez un type de média qui décrit la vidéo encodée.
3.  Transmettez ce type de média à la méthode [**IMFSinkWriter :: AddStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-addstream) .
4.  Créez un deuxième type de média qui décrit l’entrée non compressée.
5.  Transmettez le type de média non compressé à la méthode [**IMFSinkWriter :: SetInputMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-setinputmediatype) .
6.  Appelez la méthode [**IMFSinkWriter :: BeginWriting**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-beginwriting) .
7.  L’enregistreur du récepteur est maintenant prêt à accepter les exemples d’entrée.

Le code suivant illustre ces étapes.


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



La plupart des étapes de l’exemple de code précédent sont la définition des attributs de type de média pour les deux types de média. Les détails des types de médias dépendent du contenu source et du profil d’encodage souhaité.

## <a name="send-video-frames-to-the-sink-writer"></a>Envoyer des trames vidéo à l’enregistreur du récepteur

Pour envoyer une image vidéo à l’enregistreur du récepteur, appelez la méthode [**IMFSinkWriter :: WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) . La méthode **WriteSample** prend un pointeur vers l’interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , qui représente un *exemple* d’objet multimédia. L’exemple de support contient un objet de *mémoire tampon de média* qui, à son tour, contient un pointeur vers l’image vidéo. Pour plus d’informations sur les exemples de supports et la mémoire tampon, consultez les rubriques suivantes.

-   [Exemples de supports](media-samples.md)
-   [Mémoires tampons de média](media-buffers.md)

Selon votre application, vous pouvez récupérer les exemples de média à partir du [lecteur source](source-reader.md). Vous pouvez également créer les exemples de média et manipuler directement les données dans la mémoire tampon. Le code suivant illustre la deuxième approche. Il crée une mémoire tampon et écrit une seule image vidéo dans la mémoire tampon. Ensuite, il ajoute ce tampon à un exemple de média et envoie l’exemple de support à l’enregistreur du récepteur.


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



Ce code effectue les étapes suivantes.

1.  Appelez [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) pour créer un objet de mémoire tampon de média. Cette fonction alloue la mémoire pour la mémoire tampon.
2.  Appelez [**IMFMediaBuffer :: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) pour verrouiller la mémoire tampon et obtenir un pointeur vers la mémoire.
3.  Appelez [**MFCopyImage**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) pour copier l’image vidéo dans la mémoire tampon.
    > [!Note]  
    > Dans cet exemple particulier, l’utilisation de **memcpy** fonctionnera aussi bien. Toutefois, la fonction [**MFCopyImage**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) gère correctement le cas où le Stride de l’image source ne correspond pas à la mémoire tampon cible. Pour plus d’informations, consultez l' [image Stride](image-stride.md).

     

4.  Appelez [**IMFMediaBuffer :: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) pour déverrouiller la mémoire tampon.
5.  Appelez [**IMFMediaBuffer :: SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) pour mettre à jour la longueur des données valides dans la mémoire tampon. (Sinon, cette valeur est définie par défaut sur zéro.)
6.  Appelez [**MFCreateSample**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) pour créer un exemple d’objet de support.
7.  Appelez [**IMFSample :: AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer) pour ajouter la mémoire tampon du média à l’exemple de support.
8.  Appelez [**IMFSample :: SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime) pour définir l’horodatage de la trame vidéo.
9.  Appelez [**IMFSample :: SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration) pour définir la durée de l’image vidéo.
10. Appelez [**IMFSinkWriter :: WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) pour envoyer l’exemple de support au writer du récepteur.

## <a name="write-the-main-function"></a>Écrire la fonction main

À l’intérieur de la `main` fonction, procédez comme suit.

1.  Appelez [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) pour initialiser la bibliothèque com.
2.  Appelez [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) pour initialiser Microsoft Media Foundation.
3.  Créez le writer du récepteur.
4.  Envoyer des trames vidéo à l’enregistreur du récepteur.
5.  Appelez [**IMFSinkWriter :: Finalize**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-finalize) pour finaliser le fichier de sortie.
6.  Libère le pointeur vers le writer du récepteur.
7.  Appelez [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).
8.  Appeler [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).


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



## <a name="example-code"></a>Exemple de code

Le code suivant illustre le programme complet.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Enregistreur du récepteur](sink-writer.md)
</dt> </dl>

 

 
