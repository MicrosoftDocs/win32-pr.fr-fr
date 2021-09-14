---
description: Ce didacticiel montre comment récupérer des paquets de données à partir d’un fichier ASF (Advanced Systems Format) à l’aide du séparateur ASF.
ms.assetid: e3a55275-e8f0-4ab7-98db-a2f2c54d5a51
title: 'Didacticiel : lecture d’un fichier ASF à l’aide d’objets WMContainer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0225f434f650f0423771122e6fc345022e69ec1a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235806"
---
# <a name="tutorial-reading-an-asf-file-by-using-wmcontainer-objects"></a>Didacticiel : lecture d’un fichier ASF à l’aide d’objets WMContainer

Ce didacticiel montre comment récupérer des paquets de données à partir d’un fichier ASF (Advanced Systems Format) à l’aide du [séparateur ASF](asf-splitter.md). Dans ce didacticiel, vous allez créer une application console simple qui lit un fichier ASF et génère des exemples de supports compressés pour le premier flux vidéo du fichier. L’application affiche des informations sur les images clés du flux vidéo.

Ce didacticiel comprend les étapes suivantes :

-   [Composants requis](#prerequisites)
-   [1. Configurez le Project](#1-set-up-the-project)
-   [2. ouvrir un fichier ASF](#2-open-an-asf-file)
-   [3. lire l’objet d’en-tête ASF](#3-read-the-asf-header-object)
-   [4. créer le séparateur ASF](#4-create-the-asf-splitter)
-   [5. Sélectionner un flux pour l’analyse](#5-select-a-stream-for-parsing)
-   [6. générer des exemples de supports compressés](#6-generate-compressed-media-samples)
-   [7. écrire la fonction Entry-Point](#7-write-the-entry-point-function)
-   [Liste des programmes](#program-listing)
-   [Rubriques connexes](#related-topics)

Ce didacticiel ne traite pas de la façon de décoder les données compressées que l’application obtient du séparateur ASF.

## <a name="prerequisites"></a>Prérequis

Ce didacticiel part des principes suivants :

-   Vous êtes familiarisé avec la structure d’un fichier ASF et les composants fournis par Media Foundation pour travailler avec des objets ASF. Ces composants incluent l’objet ContentInfo, le séparateur, le multiplexeur et le profil. Pour plus d’informations, consultez [WMCONTAINER ASF Components](wmcontainer-asf-components.md).
-   Vous êtes familiarisé avec les [mémoires tampons de média](media-buffers.md) et les flux d’octets : en particulier, les opérations de fichier utilisant un flux d’octets, la lecture d’un flux d’octets dans une mémoire tampon de média et l’écriture du contenu d’une mémoire tampon de média dans un flux d’octets.

## <a name="1-set-up-the-project"></a>1. Configurez le Project

Incluez les en-têtes suivants dans votre fichier source :


```C++
#include <stdio.h>       // Standard I/O
#include <windows.h>     // Windows headers
#include <mfapi.h>       // Media Foundation platform
#include <wmcontainer.h> // ASF interfaces
#include <Mferror.h>
```



Lien vers les fichiers de bibliothèque suivants :

-   mfplat. lib
-   MF. lib
-   mfuuid. lib

Déclarez la fonction [SafeRelease](saferelease.md) :


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



## <a name="2-open-an-asf-file"></a>2. ouvrir un fichier ASF

Ensuite, ouvrez le fichier spécifié en appelant la fonction [**MFCreateFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) . La méthode retourne un pointeur vers l’objet de flux d’octets qui contient le contenu du fichier. Le nom de fichier est spécifié par l’utilisateur via les arguments de ligne de commande de l’application.

L’exemple de code suivant prend un nom de fichier et retourne un pointeur vers un objet de flux d’octets qui peut être utilisé pour lire le fichier.


```C++
        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);
```



## <a name="3-read-the-asf-header-object"></a>3. lire l’objet d’en-tête ASF

Créez ensuite l' [objet ASF ContentInfo](asf-contentinfo-object.md) et utilisez-le pour analyser l’objet d’en-tête ASF du fichier spécifié. L’objet ContentInfo stocke les informations de l’en-tête ASF, y compris les attributs de fichier globaux et les informations sur chaque flux. Vous utiliserez l’objet ContentInfo plus tard dans le didacticiel pour initialiser le séparateur ASF et récupérer le numéro de flux du flux vidéo.

Pour créer l’objet ASF ContentInfo :

1.  Appelez la fonction [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) pour créer un objet ContentInfo. La méthode retourne un pointeur vers l’interface [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) .
2.  Lire les 30 premiers octets de données du fichier ASF dans une mémoire tampon de média.
3.  Transmettez la mémoire tampon du média à la méthode [**IMFASFContentInfo :: GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) . Cette méthode retourne la taille totale de l’objet d’en-tête dans le fichier ASF.
4.  Transmettez le même tampon de média à la méthode [**IMFASFContentInfo ::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) .
5.  Lisez le reste de l’objet d’en-tête dans une nouvelle mémoire tampon de média.
6.  Transmettez la deuxième mémoire tampon à la méthode [**ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) . Spécifiez le décalage de 30 octets dans le paramètre *cbOffsetWithinHeader* de **ParseHeader**. La méthode **ParseHeader** Initialise l’objet ContentInfo avec les informations collectées à partir des divers objets ASF contenus dans l’objet d’en-tête.


```C++
// Read the ASF Header Object from a byte stream and return a pointer to the 
// populated ASF ContentInfo object.
//
// The current read position of the byte stream must be at the start of the
// ASF Header Object.

HRESULT CreateContentInfo(IMFByteStream *pStream, 
    IMFASFContentInfo **ppContentInfo)
{
    const DWORD MIN_ASF_HEADER_SIZE = 30;
    
    QWORD cbHeader = 0;
    DWORD cbBuffer = 0;

    IMFASFContentInfo *pContentInfo = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    // Create the ASF ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);
    
    // Read the first 30 bytes to find the total header size.

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(MIN_ASF_HEADER_SIZE, &pBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer,MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GetHeaderSize(pBuffer, &cbHeader);
    }

    // Pass the first 30 bytes to the ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, 0);
    }

    SafeRelease(&pBuffer);

    if (SUCCEEDED(hr))
    {
        cbBuffer = (DWORD)(cbHeader - MIN_ASF_HEADER_SIZE);

        hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);
    }

    // Read the rest of the header and finish parsing the header.
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer, cbBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        // Return the pointer to the caller.
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();
    }
    SafeRelease(&pBuffer);
    SafeRelease(&pContentInfo);
    return hr;
} 
```



Cette fonction utilise la `ReadFromByteStream` fonction pour lire un flux d’octets dans une mémoire tampon de média :


```C++
// Read data from a byte stream into a media buffer.
//
// This function reads a maximum of cbMax bytes, or up to the size size of the 
// buffer, whichever is smaller. If the end of the byte stream is reached, the 
// actual amount of data read might be less than either of these values.
//
// To find out how much data was read, call IMFMediaBuffer::GetCurrentLength.

HRESULT ReadFromByteStream(
    IMFByteStream *pStream,     // Pointer to the byte stream.
    IMFMediaBuffer *pBuffer,    // Pointer to the media buffer.
    DWORD cbMax                 // Maximum amount to read.
    )
{
    DWORD cbBufferMax = 0;
    DWORD cbRead = 0;
    BYTE *pData= NULL;

    HRESULT hr = pBuffer->Lock(&pData, &cbBufferMax, NULL);

    // Do not exceed the maximum size of the buffer.
    if (SUCCEEDED(hr))
    {
        if (cbMax > cbBufferMax)
        {
            cbMax = cbBufferMax;
        }

        // Read up to cbMax bytes.
        hr = pStream->Read(pData, cbMax, &cbRead);
    }

    // Update the size of the valid data in the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbRead);
    }
    if (pData)
    {
        pBuffer->Unlock();
    }
    return hr;
}
```



## <a name="4-create-the-asf-splitter"></a>4. créer le séparateur ASF

Ensuite, créez l’objet [séparateur ASF](asf-splitter.md) . Vous allez utiliser le séparateur ASF pour analyser l’objet de données ASF, qui contient des données multimédias en paquets pour le fichier ASF.

Pour créer un objet Splitter pour le fichier ASF :

1.  Appelez la fonction [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) pour créer le séparateur ASF. La fonction retourne un pointeur vers l’interface [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) .
2.  Appelez [**IMFASFSplitter :: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) pour initialiser le séparateur ASF. Cette méthode prend un pointeur vers l’objet ContentInfo, qui a été créé dans la procédure 3.


```C++
// Create and initialize the ASF splitter.

HRESULT CreateASFSplitter (IMFASFContentInfo* pContentInfo, 
    IMFASFSplitter** ppSplitter)
{
    IMFASFSplitter *pSplitter = NULL;

    // Create the splitter object.
    HRESULT hr = MFCreateASFSplitter(&pSplitter);

    // Initialize the splitter to work with specific ASF data.
    if (SUCCEEDED(hr))
    {
        hr = pSplitter->Initialize(pContentInfo);
    }
    if (SUCCEEDED(hr))
    {
        // Return the object to the caller.
        *ppSplitter = pSplitter;
        (*ppSplitter)->AddRef();
    }
    SafeRelease(&pSplitter);
    return hr;
}
```



## <a name="5-select-a-stream-for-parsing"></a>5. Sélectionner un flux pour l’analyse

Ensuite, énumérez les flux dans le fichier ASF et sélectionnez le premier flux vidéo à analyser. Pour énumérer les flux, vous allez utiliser un objet de profil ASF et rechercher les flux qui ont un type de média vidéo.

Pour sélectionner le flux vidéo :

1.  Appelez [**IMFASFContentInfo :: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile) sur l’objet ContentInfo pour créer un profil ASF. Parmi d’autres informations, le profil décrit les flux dans le fichier ASF.
2.  Appelez [**IMFASFProfile :: GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) pour connaître le nombre de flux dans le fichier ASF.
3.  Appelez [**IMFASFProfile :: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) dans une boucle pour énumérer les flux. La méthode retourne un pointeur vers l’interface [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) . Elle retourne également l’identificateur de flux.
4.  Appelez [**IMFASFStreamConfig :: GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) pour obtenir le GUID du type principal du flux. Si le GUID de type principal est MFMediaType \_ vidéo, le flux contient une vidéo.
5.  Si vous avez trouvé un flux vidéo à l’étape 4, appelez [**IMFASFSplitter :: SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) pour sélectionner le flux. Cette méthode prend un tableau d’identificateurs de flux. Pour ce didacticiel, la taille du tableau est 1 parce que l’application analyse un seul flux.

L’exemple de code suivant énumère les flux du fichier ASF et sélectionne le premier flux vidéo sur le séparateur ASF :


```C++
// Select the first video stream for parsing with the ASF splitter.

HRESULT SelectVideoStream(IMFASFContentInfo *pContentInfo, 
    IMFASFSplitter *pSplitter, BOOL *pbHasVideo)
{
    DWORD   cStreams = 0;
    WORD    wStreamID = 0;

    IMFASFProfile *pProfile = NULL;
    IMFASFStreamConfig *pStream = NULL;

    // Get the ASF profile from the ContentInfo object.
    HRESULT hr = pContentInfo->GetProfile(&pProfile);

    // Loop through all of the streams in the profile.
    if (SUCCEEDED(hr))
    {
        hr = pProfile->GetStreamCount(&cStreams);
    }

    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cStreams; i++)
        {
            GUID    streamType = GUID_NULL;

            // Get the stream type and stream identifier.
            hr = pProfile->GetStream(i, &wStreamID, &pStream);
            if (FAILED(hr)) 
            {
                break;
            }

            hr = pStream->GetStreamType(&streamType);
            if (FAILED(hr)) 
            {
                break;
            }

            if (streamType == MFMediaType_Video)
            {
                *pbHasVideo = TRUE;
                break;
            }
            SafeRelease(&pStream);
        }
    }

    // Select the video stream, if found.
    if (SUCCEEDED(hr))
    {
        if (*pbHasVideo)
        {
            // SelectStreams takes an array of stream identifiers.
            hr = pSplitter->SelectStreams(&wStreamID, 1);
        }
    }
    SafeRelease(&pStream);
    SafeRelease(&pProfile);
    return hr;
}
```



## <a name="6-generate-compressed-media-samples"></a>6. générer des exemples de supports compressés

Ensuite, utilisez le séparateur ASF pour analyser l’objet de données ASF et obtenir les paquets de données pour le flux vidéo sélectionné. L’application lit les données du fichier ASF dans des blocs de taille fixe et les transmet au séparateur ASF. Le séparateur analyse les données et génère des [exemples de médias](media-samples.md) qui contiennent les données vidéo compressées. L’application vérifie si chaque échantillon représente une image clé. Si c’est le cas, l’application affiche des informations de base sur l’exemple :

-   Nombre de mémoires tampons de média
-   Taille totale des données
-   Horodatage

Pour générer des exemples de supports compressés :

1.  Allouez un nouveau tampon de média.
2.  Lit les données du flux d’octets dans la mémoire tampon du média.
3.  Transmettez la mémoire tampon du média à la méthode [**IMFASFSplitter ::P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) . La méthode analyse les données ASF dans la mémoire tampon.
4.  Dans une boucle, récupérez des échantillons de média à partir du séparateur en appelant [**IMFASFSplitter :: GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample). Si le paramètre *ppISample* reçoit un pointeur [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) valide, cela signifie que le séparateur ASF a analysé un ou plusieurs paquets de données. Si *ppISample* reçoit la valeur **null**, interrompez la boucle et revenez à l’étape 1.
5.  Affiche des informations sur l’exemple.
6.  Arrêter à partir de la boucle dans les conditions suivantes :
    -   Le paramètre *ppISample* reçoit la valeur **null**.
    -   Le paramètre *pdwStatusFlags* ne reçoit pas l' **indicateur \_ STATUSFLAGS ASF \_ incomplet** .

Répétez ces étapes jusqu’à ce que vous atteigniez la fin du fichier. Le code suivant illustre ces étapes :


```C++
// Parse the video stream and display information about the video samples.
//
// The current read position of the byte stream must be at the start of the ASF
// Data Object.

HRESULT DisplayKeyFrames(IMFByteStream *pStream, IMFASFSplitter *pSplitter)
{
    const DWORD cbReadSize = 2048;  // Read size (arbitrary value)

    IMFMediaBuffer *pBuffer = NULL;
    IMFSample *pSample = NULL;

    HRESULT hr = S_OK;
    while (SUCCEEDED(hr))
    {
        // The parser must get a newly allocated buffer each time.
        hr = MFCreateMemoryBuffer(cbReadSize, &pBuffer);
        if (FAILED(hr))
        {
            break;
        }

        // Read data into the buffer.
        hr = ReadFromByteStream(pStream, pBuffer, cbReadSize);
        if (FAILED(hr)) 
        {
            break; 
        }

        // Get the amound of data that was read.
        DWORD cbData;
        hr = pBuffer->GetCurrentLength(&cbData);
        if (FAILED(hr)) 
        { 
            break; 
        }

        if (cbData == 0)
        {
            break; // End of file.
        }

        // Send the data to the ASF splitter.
        hr = pSplitter->ParseData(pBuffer, 0, 0);
        SafeRelease(&pBuffer);
        if (FAILED(hr)) 
        { 
            break; 
        }

        // Pull samples from the splitter.
        DWORD parsingStatus = 0;
        do
        {
            WORD streamID;
            hr = pSplitter->GetNextSample(&parsingStatus, &streamID, &pSample);
            if (FAILED(hr)) 
            { 
                break; 
            }
            if (pSample == NULL)
            {
                // No samples yet. Parse more data.
                break;
            }
            if (IsRandomAccessPoint(pSample))
            {
                DisplayKeyFrame(pSample);
            }
            SafeRelease(&pSample);
            
        } while (parsingStatus & ASF_STATUSFLAGS_INCOMPLETE);
    }
    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



La fonction IsKeyFrame teste si un exemple est une image clé, en obtenant la valeur de l’attribut [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md) .


```C++
inline BOOL IsRandomAccessPoint(IMFSample *pSample)
{
    // Check for the "clean point" attribute. Default to FALSE.
    return MFGetAttributeUINT32(pSample, MFSampleExtension_CleanPoint, FALSE);
}
```



À des fins d’illustration, ce didacticiel affiche des informations pour chaque image clé vidéo, en appelant la fonction suivante :


```C++
void DisplayKeyFrame(IMFSample *pSample)
{
    DWORD   cBuffers = 0;           // Buffer count
    DWORD   cbTotalLength = 0;      // Buffer length
    MFTIME  hnsTime = 0;            // Time stamp

    // Print various information about the key frame.
    if (SUCCEEDED(pSample->GetBufferCount(&cBuffers)))
    {
        wprintf_s(L"Buffer count: %d\n", cBuffers);
    }
    if (SUCCEEDED(pSample->GetTotalLength(&cbTotalLength)))
    {
        wprintf_s(L"Length: %d bytes\n", cbTotalLength);
    }
    if (SUCCEEDED(pSample->GetSampleTime(&hnsTime)))
    {
        // Convert the time stamp to seconds.
        double sec = static_cast<double>(hnsTime / 10000) / 1000;
        wprintf_s(L"Time stamp: %f sec.\n", sec);
    }
    wprintf_s(L"\n");
}
```



Une application classique utilise les paquets de données pour le décodage, l’remuxing, l’envoi sur le réseau ou une autre tâche.

## <a name="7-write-the-entry-point-function"></a>7. écrire la fonction Entry-Point

Vous pouvez maintenant mettre ensemble les étapes précédentes dans une application complète. Avant d’utiliser l’un des objets Media Foundation, initialisez la plateforme Media Foundation en appelant [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup). Lorsque vous avez terminé, appelez [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown). Pour plus d’informations, [l’initialisation de Media Foundation](initializing-media-foundation.md).


```C++
int wmain(int argc, WCHAR* argv[])
{
    if (argc != 2)
    {
        _s(L"Usage: %s input.wmv");
        return 0;
    }

    // Start the Media Foundation platform.
    HRESULT hr = MFStartup(MF_VERSION);
    if (SUCCEEDED(hr))
    {
        PCWSTR pszFileName = argv[1]; 
        BOOL   bHasVideo = FALSE;

        IMFByteStream       *pStream = NULL;
        IMFASFContentInfo   *pContentInfo = NULL;
        IMFASFSplitter      *pSplitter = NULL;

        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);

        // Read the ASF header.
        if (SUCCEEDED(hr))
        {
            hr = CreateContentInfo(pStream, &pContentInfo);
        }

        // Create the ASF splitter.
        if (SUCCEEDED(hr))
        {
            hr = CreateASFSplitter(pContentInfo, &pSplitter);
        }

        // Select the first video stream.
        if (SUCCEEDED(hr))
        {
            hr = SelectVideoStream(pContentInfo, pSplitter, &bHasVideo);
        }

        // Parse the ASF file.
        if (SUCCEEDED(hr))
        {
            if (bHasVideo)
            {
                hr = DisplayKeyFrames(pStream, pSplitter);
            }
            else
            {
                wprintf_s(L"No video stream.\n");
            }
        }
        SafeRelease(&pSplitter);
        SafeRelease(&pContentInfo);
        SafeRelease(&pStream);
    
        // Shut down the Media Foundation platform.
        MFShutdown();
    }
    if (FAILED(hr))
    {
        wprintf_s(L"Error: 0x%X\n", hr);
    }
    return 0;
}
```



## <a name="program-listing"></a>Liste des programmes

Le code suivant illustre la liste complète du didacticiel.


```C++
#include <stdio.h>       // Standard I/O
#include <windows.h>     // Windows headers
#include <mfapi.h>       // Media Foundation platform
#include <wmcontainer.h> // ASF interfaces
#include <Mferror.h>

#pragma comment(lib, "mfplat")
#pragma comment(lib, "mf")
#pragma comment(lib, "mfuuid")

template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}

// Read data from a byte stream into a media buffer.
//
// This function reads a maximum of cbMax bytes, or up to the size size of the 
// buffer, whichever is smaller. If the end of the byte stream is reached, the 
// actual amount of data read might be less than either of these values.
//
// To find out how much data was read, call IMFMediaBuffer::GetCurrentLength.

HRESULT ReadFromByteStream(
    IMFByteStream *pStream,     // Pointer to the byte stream.
    IMFMediaBuffer *pBuffer,    // Pointer to the media buffer.
    DWORD cbMax                 // Maximum amount to read.
    )
{
    DWORD cbBufferMax = 0;
    DWORD cbRead = 0;
    BYTE *pData= NULL;

    HRESULT hr = pBuffer->Lock(&pData, &cbBufferMax, NULL);

    // Do not exceed the maximum size of the buffer.
    if (SUCCEEDED(hr))
    {
        if (cbMax > cbBufferMax)
        {
            cbMax = cbBufferMax;
        }

        // Read up to cbMax bytes.
        hr = pStream->Read(pData, cbMax, &cbRead);
    }

    // Update the size of the valid data in the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbRead);
    }
    if (pData)
    {
        pBuffer->Unlock();
    }
    return hr;
}


// Read the ASF Header Object from a byte stream and return a pointer to the 
// populated ASF ContentInfo object.
//
// The current read position of the byte stream must be at the start of the
// ASF Header Object.

HRESULT CreateContentInfo(IMFByteStream *pStream, 
    IMFASFContentInfo **ppContentInfo)
{
    const DWORD MIN_ASF_HEADER_SIZE = 30;
    
    QWORD cbHeader = 0;
    DWORD cbBuffer = 0;

    IMFASFContentInfo *pContentInfo = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    // Create the ASF ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);
    
    // Read the first 30 bytes to find the total header size.

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(MIN_ASF_HEADER_SIZE, &pBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer,MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GetHeaderSize(pBuffer, &cbHeader);
    }

    // Pass the first 30 bytes to the ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, 0);
    }

    SafeRelease(&pBuffer);

    if (SUCCEEDED(hr))
    {
        cbBuffer = (DWORD)(cbHeader - MIN_ASF_HEADER_SIZE);

        hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);
    }

    // Read the rest of the header and finish parsing the header.
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer, cbBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        // Return the pointer to the caller.
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();
    }
    SafeRelease(&pBuffer);
    SafeRelease(&pContentInfo);
    return hr;
} 

// Create and initialize the ASF splitter.

HRESULT CreateASFSplitter (IMFASFContentInfo* pContentInfo, 
    IMFASFSplitter** ppSplitter)
{
    IMFASFSplitter *pSplitter = NULL;

    // Create the splitter object.
    HRESULT hr = MFCreateASFSplitter(&pSplitter);

    // Initialize the splitter to work with specific ASF data.
    if (SUCCEEDED(hr))
    {
        hr = pSplitter->Initialize(pContentInfo);
    }
    if (SUCCEEDED(hr))
    {
        // Return the object to the caller.
        *ppSplitter = pSplitter;
        (*ppSplitter)->AddRef();
    }
    SafeRelease(&pSplitter);
    return hr;
}


// Select the first video stream for parsing with the ASF splitter.

HRESULT SelectVideoStream(IMFASFContentInfo *pContentInfo, 
    IMFASFSplitter *pSplitter, BOOL *pbHasVideo)
{
    DWORD   cStreams = 0;
    WORD    wStreamID = 0;

    IMFASFProfile *pProfile = NULL;
    IMFASFStreamConfig *pStream = NULL;

    // Get the ASF profile from the ContentInfo object.
    HRESULT hr = pContentInfo->GetProfile(&pProfile);

    // Loop through all of the streams in the profile.
    if (SUCCEEDED(hr))
    {
        hr = pProfile->GetStreamCount(&cStreams);
    }

    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cStreams; i++)
        {
            GUID    streamType = GUID_NULL;

            // Get the stream type and stream identifier.
            hr = pProfile->GetStream(i, &wStreamID, &pStream);
            if (FAILED(hr)) 
            {
                break;
            }

            hr = pStream->GetStreamType(&streamType);
            if (FAILED(hr)) 
            {
                break;
            }

            if (streamType == MFMediaType_Video)
            {
                *pbHasVideo = TRUE;
                break;
            }
            SafeRelease(&pStream);
        }
    }

    // Select the video stream, if found.
    if (SUCCEEDED(hr))
    {
        if (*pbHasVideo)
        {
            // SelectStreams takes an array of stream identifiers.
            hr = pSplitter->SelectStreams(&wStreamID, 1);
        }
    }
    SafeRelease(&pStream);
    SafeRelease(&pProfile);
    return hr;
}

inline BOOL IsRandomAccessPoint(IMFSample *pSample)
{
    // Check for the "clean point" attribute. Default to FALSE.
    return MFGetAttributeUINT32(pSample, MFSampleExtension_CleanPoint, FALSE);
}

void DisplayKeyFrame(IMFSample *pSample)
{
    DWORD   cBuffers = 0;           // Buffer count
    DWORD   cbTotalLength = 0;      // Buffer length
    MFTIME  hnsTime = 0;            // Time stamp

    // Print various information about the key frame.
    if (SUCCEEDED(pSample->GetBufferCount(&cBuffers)))
    {
        wprintf_s(L"Buffer count: %d\n", cBuffers);
    }
    if (SUCCEEDED(pSample->GetTotalLength(&cbTotalLength)))
    {
        wprintf_s(L"Length: %d bytes\n", cbTotalLength);
    }
    if (SUCCEEDED(pSample->GetSampleTime(&hnsTime)))
    {
        // Convert the time stamp to seconds.
        double sec = static_cast<double>(hnsTime / 10000) / 1000;
        wprintf_s(L"Time stamp: %f sec.\n", sec);
    }
    wprintf_s(L"\n");
}


// Parse the video stream and display information about the video samples.
//
// The current read position of the byte stream must be at the start of the ASF
// Data Object.

HRESULT DisplayKeyFrames(IMFByteStream *pStream, IMFASFSplitter *pSplitter)
{
    const DWORD cbReadSize = 2048;  // Read size (arbitrary value)

    IMFMediaBuffer *pBuffer = NULL;
    IMFSample *pSample = NULL;

    HRESULT hr = S_OK;
    while (SUCCEEDED(hr))
    {
        // The parser must get a newly allocated buffer each time.
        hr = MFCreateMemoryBuffer(cbReadSize, &pBuffer);
        if (FAILED(hr))
        {
            break;
        }

        // Read data into the buffer.
        hr = ReadFromByteStream(pStream, pBuffer, cbReadSize);
        if (FAILED(hr)) 
        {
            break; 
        }

        // Get the amound of data that was read.
        DWORD cbData;
        hr = pBuffer->GetCurrentLength(&cbData);
        if (FAILED(hr)) 
        { 
            break; 
        }

        if (cbData == 0)
        {
            break; // End of file.
        }

        // Send the data to the ASF splitter.
        hr = pSplitter->ParseData(pBuffer, 0, 0);
        SafeRelease(&pBuffer);
        if (FAILED(hr)) 
        { 
            break; 
        }

        // Pull samples from the splitter.
        DWORD parsingStatus = 0;
        do
        {
            WORD streamID;
            hr = pSplitter->GetNextSample(&parsingStatus, &streamID, &pSample);
            if (FAILED(hr)) 
            { 
                break; 
            }
            if (pSample == NULL)
            {
                // No samples yet. Parse more data.
                break;
            }
            if (IsRandomAccessPoint(pSample))
            {
                DisplayKeyFrame(pSample);
            }
            SafeRelease(&pSample);
            
        } while (parsingStatus & ASF_STATUSFLAGS_INCOMPLETE);
    }
    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}

int wmain(int argc, WCHAR* argv[])
{
    if (argc != 2)
    {
        _s(L"Usage: %s input.wmv");
        return 0;
    }

    // Start the Media Foundation platform.
    HRESULT hr = MFStartup(MF_VERSION);
    if (SUCCEEDED(hr))
    {
        PCWSTR pszFileName = argv[1]; 
        BOOL   bHasVideo = FALSE;

        IMFByteStream       *pStream = NULL;
        IMFASFContentInfo   *pContentInfo = NULL;
        IMFASFSplitter      *pSplitter = NULL;

        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);

        // Read the ASF header.
        if (SUCCEEDED(hr))
        {
            hr = CreateContentInfo(pStream, &pContentInfo);
        }

        // Create the ASF splitter.
        if (SUCCEEDED(hr))
        {
            hr = CreateASFSplitter(pContentInfo, &pSplitter);
        }

        // Select the first video stream.
        if (SUCCEEDED(hr))
        {
            hr = SelectVideoStream(pContentInfo, pSplitter, &bHasVideo);
        }

        // Parse the ASF file.
        if (SUCCEEDED(hr))
        {
            if (bHasVideo)
            {
                hr = DisplayKeyFrames(pStream, pSplitter);
            }
            else
            {
                wprintf_s(L"No video stream.\n");
            }
        }
        SafeRelease(&pSplitter);
        SafeRelease(&pContentInfo);
        SafeRelease(&pStream);
    
        // Shut down the Media Foundation platform.
        MFShutdown();
    }
    if (FAILED(hr))
    {
        wprintf_s(L"Error: 0x%X\n", hr);
    }
    return 0;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Composants WMContainer ASF](wmcontainer-asf-components.md)
</dt> <dt>

[Prise en charge ASF dans Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



