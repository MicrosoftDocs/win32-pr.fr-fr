---
description: Cette rubrique décrit les étapes permettant de remplir les structures requises pour lire des données audio dans XAudio2.
ms.assetid: caeb522e-d4f6-91e2-5e85-ea0af0f61300
title: 'Procédure : charger des fichiers de données audio dans XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 659b4d8e106b6f0b2eb942505f99562f56fdada7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113650"
---
# <a name="how-to-load-audio-data-files-in-xaudio2"></a><span data-ttu-id="12e87-103">Procédure : charger des fichiers de données audio dans XAudio2</span><span class="sxs-lookup"><span data-stu-id="12e87-103">How to: Load Audio Data Files in XAudio2</span></span>

> [!Note]  
> <span data-ttu-id="12e87-104">Ce contenu s’applique uniquement aux applications de bureau et nécessite une révision pour fonctionner dans une application Windows Store.</span><span class="sxs-lookup"><span data-stu-id="12e87-104">This content applies only to desktop apps and will require revision to function in a Windows Store app.</span></span> <span data-ttu-id="12e87-105">Reportez-vous à la documentation de [**CreateFile2**](/windows/win32/api/fileapi/nf-fileapi-createfile2), [**CreateEventEx**](/windows/win32/api/synchapi/nf-synchapi-createeventexa), [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex), [**SetFilePointerEx**](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex)et [**GetOverlappedResultEx**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresultex).</span><span class="sxs-lookup"><span data-stu-id="12e87-105">Please refer to the documentation for [**CreateFile2**](/windows/win32/api/fileapi/nf-fileapi-createfile2), [**CreateEventEx**](/windows/win32/api/synchapi/nf-synchapi-createeventexa), [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex), [**SetFilePointerEx**](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex), and [**GetOverlappedResultEx**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresultex).</span></span> <span data-ttu-id="12e87-106">Consultez SoundFileReader. h/. cpp dans l’exemple BasicSound Windows 8 de la [Galerie d’exemples SDK Windows](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20file%20playback%20sample%20(Windows%208)).</span><span class="sxs-lookup"><span data-stu-id="12e87-106">See SoundFileReader.h/.cpp in the BasicSound Windows 8 sample from the [Windows SDK Samples Gallery](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20file%20playback%20sample%20(Windows%208)).</span></span>

 

<span data-ttu-id="12e87-107">Cette rubrique décrit les étapes permettant de remplir les structures requises pour lire des données audio dans XAudio2.</span><span class="sxs-lookup"><span data-stu-id="12e87-107">This topic describes the steps to populate the structures required to play audio data in XAudio2.</span></span> <span data-ttu-id="12e87-108">Les étapes suivantes chargent les segments « fmt » et « Data » d’un fichier audio, et les utilisent pour remplir une structure **WAVEFORMATEXTENSIBLE** et une structure de [**\_ mémoire tampon XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .</span><span class="sxs-lookup"><span data-stu-id="12e87-108">The following steps load the 'fmt ' and 'data' chunks of an audio file, and uses them to populate a **WAVEFORMATEXTENSIBLE** structure and an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span>

-   [<span data-ttu-id="12e87-109">Préparation de l’analyse du fichier audio.</span><span class="sxs-lookup"><span data-stu-id="12e87-109">Preparing to parse the audio file.</span></span>](#preparing-to-parse-the-audio-file)
-   [<span data-ttu-id="12e87-110">Remplissage des structures XAudio2 avec le contenu de blocs RIFF.</span><span class="sxs-lookup"><span data-stu-id="12e87-110">Populating XAudio2 structures with the contents of RIFF chunks.</span></span>](#populating-xaudio2-structures-with-the-contents-of-riff-chunks)

## <a name="preparing-to-parse-the-audio-file"></a><span data-ttu-id="12e87-111">Préparation de l’analyse du fichier audio</span><span class="sxs-lookup"><span data-stu-id="12e87-111">Preparing to parse the audio file</span></span>

<span data-ttu-id="12e87-112">Les fichiers audio pris en charge par XAudio2 utilisent le format RIFF (Resource Interchange File Format).</span><span class="sxs-lookup"><span data-stu-id="12e87-112">Audio files supported by XAudio2 use the Resource Interchange File Format (RIFF).</span></span> <span data-ttu-id="12e87-113">RIFF est décrit dans la vue d’ensemble du [format RIFF (Resource Interchange File Format)](resource-interchange-file-format--riff-.md) .</span><span class="sxs-lookup"><span data-stu-id="12e87-113">RIFF is described in the [Resource Interchange File Format (RIFF)](resource-interchange-file-format--riff-.md) overview.</span></span> <span data-ttu-id="12e87-114">Les données audio d’un fichier RIFF sont chargées en recherchant le bloc RIFF, puis en parcourant le bloc pour rechercher des blocs individuels contenus dans le bloc RIFF.</span><span class="sxs-lookup"><span data-stu-id="12e87-114">Audio data in a RIFF file is loaded by finding the RIFF chunk and then looping through the chunk to find individual chunks contained in the RIFF chunk.</span></span> <span data-ttu-id="12e87-115">Les fonctions suivantes sont des exemples de code permettant de rechercher des segments et de charger des données contenues dans les segments.</span><span class="sxs-lookup"><span data-stu-id="12e87-115">The following functions are examples of code to find chunks and load data contained in the chunks.</span></span>

-   <span data-ttu-id="12e87-116">Pour rechercher un segment dans un fichier RIFF :</span><span class="sxs-lookup"><span data-stu-id="12e87-116">To find a chunk in a RIFF file:</span></span>

    ```
    #ifdef _XBOX //Big-Endian
    #define fourccRIFF 'RIFF'
    #define fourccDATA 'data'
    #define fourccFMT 'fmt '
    #define fourccWAVE 'WAVE'
    #define fourccXWMA 'XWMA'
    #define fourccDPDS 'dpds'
    #endif

    #ifndef _XBOX //Little-Endian
    #define fourccRIFF 'FFIR'
    #define fourccDATA 'atad'
    #define fourccFMT ' tmf'
    #define fourccWAVE 'EVAW'
    #define fourccXWMA 'AMWX'
    #define fourccDPDS 'sdpd'
    #endif
    HRESULT FindChunk(HANDLE hFile, DWORD fourcc, DWORD & dwChunkSize, DWORD & dwChunkDataPosition)
    {
        HRESULT hr = S_OK;
        if( INVALID_SET_FILE_POINTER == SetFilePointer( hFile, 0, NULL, FILE_BEGIN ) )
            return HRESULT_FROM_WIN32( GetLastError() );

        DWORD dwChunkType;
        DWORD dwChunkDataSize;
        DWORD dwRIFFDataSize = 0;
        DWORD dwFileType;
        DWORD bytesRead = 0;
        DWORD dwOffset = 0;

        while (hr == S_OK)
        {
            DWORD dwRead;
            if( 0 == ReadFile( hFile, &dwChunkType, sizeof(DWORD), &dwRead, NULL ) )
                hr = HRESULT_FROM_WIN32( GetLastError() );

            if( 0 == ReadFile( hFile, &dwChunkDataSize, sizeof(DWORD), &dwRead, NULL ) )
                hr = HRESULT_FROM_WIN32( GetLastError() );

            switch (dwChunkType)
            {
            case fourccRIFF:
                dwRIFFDataSize = dwChunkDataSize;
                dwChunkDataSize = 4;
                if( 0 == ReadFile( hFile, &dwFileType, sizeof(DWORD), &dwRead, NULL ) )
                    hr = HRESULT_FROM_WIN32( GetLastError() );
                break;

            default:
                if( INVALID_SET_FILE_POINTER == SetFilePointer( hFile, dwChunkDataSize, NULL, FILE_CURRENT ) )
                return HRESULT_FROM_WIN32( GetLastError() );            
            }

            dwOffset += sizeof(DWORD) * 2;
            
            if (dwChunkType == fourcc)
            {
                dwChunkSize = dwChunkDataSize;
                dwChunkDataPosition = dwOffset;
                return S_OK;
            }

            dwOffset += dwChunkDataSize;
            
            if (bytesRead >= dwRIFFDataSize) return S_FALSE;

        }

        return S_OK;
        
    }
    ```

    

-   <span data-ttu-id="12e87-117">Pour lire des données dans un segment une fois qu’elles ont été localisées.</span><span class="sxs-lookup"><span data-stu-id="12e87-117">To read data in a chunk after it has been located.</span></span>

    <span data-ttu-id="12e87-118">Une fois qu’un segment souhaité est trouvé, ses données peuvent être lues en ajustant le pointeur de fichier au début de la section de données du bloc.</span><span class="sxs-lookup"><span data-stu-id="12e87-118">Once a desired chunk is found, its data can be read by adjusting the file pointer to the beginning of the data section of the chunk.</span></span> <span data-ttu-id="12e87-119">Une fonction permettant de lire les données à partir d’un segment une fois qu’elle a été trouvée peut se présenter comme suit.</span><span class="sxs-lookup"><span data-stu-id="12e87-119">A function to read the data from a chunk once it is found might look like this.</span></span>

    ```
    HRESULT ReadChunkData(HANDLE hFile, void * buffer, DWORD buffersize, DWORD bufferoffset)
    {
        HRESULT hr = S_OK;
        if( INVALID_SET_FILE_POINTER == SetFilePointer( hFile, bufferoffset, NULL, FILE_BEGIN ) )
            return HRESULT_FROM_WIN32( GetLastError() );
        DWORD dwRead;
        if( 0 == ReadFile( hFile, buffer, buffersize, &dwRead, NULL ) )
            hr = HRESULT_FROM_WIN32( GetLastError() );
        return hr;
    }
    ```

    

## <a name="populating-xaudio2-structures-with-the-contents-of-riff-chunks"></a><span data-ttu-id="12e87-120">Remplissage de structures XAudio2 avec le contenu de blocs RIFF</span><span class="sxs-lookup"><span data-stu-id="12e87-120">Populating XAudio2 structures with the contents of RIFF chunks</span></span>

<span data-ttu-id="12e87-121">Pour que XAudio2 lise l’audio avec une voix source, il a besoin d’une structure **WAVEFORMATEX** et d’une structure de [**\_ mémoire tampon XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .</span><span class="sxs-lookup"><span data-stu-id="12e87-121">In order for XAudio2 to play audio with a source voice, it needs a **WAVEFORMATEX** structure and an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span> <span data-ttu-id="12e87-122">La structure **WAVEFORMATEX** peut être une plus grande structure telle que **WAVEFORMATEXTENSIBLE** qui contient une structure **WAVEFORMATEX** comme premier membre.</span><span class="sxs-lookup"><span data-stu-id="12e87-122">The **WAVEFORMATEX** structure may be a larger structure such as **WAVEFORMATEXTENSIBLE** that contains a **WAVEFORMATEX** structure as its first member.</span></span> <span data-ttu-id="12e87-123">Pour plus d’informations, consultez la page de référence de **WAVEFORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="12e87-123">See the **WAVEFORMATEX** reference page for more information.</span></span>

<span data-ttu-id="12e87-124">Dans cet exemple, un **WAVEFORMATEXTENSIBLE** est utilisé pour autoriser le chargement de fichiers audio PCM avec plus de deux canaux.</span><span class="sxs-lookup"><span data-stu-id="12e87-124">In this example a **WAVEFORMATEXTENSIBLE** is being used to allow loading of PCM audio files with more than two channels.</span></span>

<span data-ttu-id="12e87-125">Les étapes suivantes illustrent l’utilisation des fonctions décrites ci-dessus pour remplir une structure **WAVEFORMATEXTENSIBLE** et une structure de [**\_ mémoire tampon XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .</span><span class="sxs-lookup"><span data-stu-id="12e87-125">The following steps illustrate using the functions described above to populate a **WAVEFORMATEXTENSIBLE** structure and an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span> <span data-ttu-id="12e87-126">Dans ce cas, le fichier audio en cours de chargement contient des données PCM et ne contient qu’un segment « RIFF », « fmt » et « Data ».</span><span class="sxs-lookup"><span data-stu-id="12e87-126">In this case, the audio file being loaded contains PCM data, and will only contain a 'RIFF', 'fmt ', and 'data' chunk.</span></span> <span data-ttu-id="12e87-127">D’autres formats peuvent contenir des types de blocs supplémentaires, comme décrit dans le [fichier RIFF (Resource Interchange File Format)](resource-interchange-file-format--riff-.md).</span><span class="sxs-lookup"><span data-stu-id="12e87-127">Other formats may contain additional chunk types as described in [Resource Interchange File Format (RIFF)](resource-interchange-file-format--riff-.md).</span></span>

1.  <span data-ttu-id="12e87-128">Déclarez les structures de [**\_ mémoire tampon**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) **WAVEFORMATEXTENSIBLE** et XAUDIO2.</span><span class="sxs-lookup"><span data-stu-id="12e87-128">Declare **WAVEFORMATEXTENSIBLE** and [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structures.</span></span>
    ```
    WAVEFORMATEXTENSIBLE wfx = {0};
    XAUDIO2_BUFFER buffer = {0};
    ```

    

2.  <span data-ttu-id="12e87-129">Ouvrez le fichier audio avec CreateFile.</span><span class="sxs-lookup"><span data-stu-id="12e87-129">Open the audio file with CreateFile.</span></span>
    ```
    #ifdef _XBOX
    char * strFileName = "game:\\media\\MusicMono.wav";
    #else
    TCHAR * strFileName = _TEXT("media\\MusicMono.wav");
    #endif
    // Open the file
    HANDLE hFile = CreateFile(
        strFileName,
        GENERIC_READ,
        FILE_SHARE_READ,
        NULL,
        OPEN_EXISTING,
        0,
        NULL );

    if( INVALID_HANDLE_VALUE == hFile )
        return HRESULT_FROM_WIN32( GetLastError() );

    if( INVALID_SET_FILE_POINTER == SetFilePointer( hFile, 0, NULL, FILE_BEGIN ) )
        return HRESULT_FROM_WIN32( GetLastError() );
    ```

    

3.  <span data-ttu-id="12e87-130">Localisez le bloc « RIFF » dans le fichier audio, puis vérifiez le type de fichier.</span><span class="sxs-lookup"><span data-stu-id="12e87-130">Locate the 'RIFF' chunk in the audio file, and check the file type.</span></span>
    ```
    DWORD dwChunkSize;
    DWORD dwChunkPosition;
    //check the file type, should be fourccWAVE or 'XWMA'
    FindChunk(hFile,fourccRIFF,dwChunkSize, dwChunkPosition );
    DWORD filetype;
    ReadChunkData(hFile,&filetype,sizeof(DWORD),dwChunkPosition);
    if (filetype != fourccWAVE)
        return S_FALSE;
    ```

    

4.  <span data-ttu-id="12e87-131">Localisez le segment « fmt » et copiez son contenu dans une structure **WAVEFORMATEXTENSIBLE** .</span><span class="sxs-lookup"><span data-stu-id="12e87-131">Locate the 'fmt ' chunk, and copy its contents into a **WAVEFORMATEXTENSIBLE** structure.</span></span>
    ```
    FindChunk(hFile,fourccFMT, dwChunkSize, dwChunkPosition );
    ReadChunkData(hFile, &wfx, dwChunkSize, dwChunkPosition );
    ```

    

5.  <span data-ttu-id="12e87-132">Localisez le segment « Data » et lisez son contenu dans une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="12e87-132">Locate the 'data' chunk, and read its contents into a buffer.</span></span>
    ```
    //fill out the audio data buffer with the contents of the fourccDATA chunk
    FindChunk(hFile,fourccDATA,dwChunkSize, dwChunkPosition );
    BYTE * pDataBuffer = new BYTE[dwChunkSize];
    ReadChunkData(hFile, pDataBuffer, dwChunkSize, dwChunkPosition);
    ```

    

6.  <span data-ttu-id="12e87-133">Remplir une structure de [**\_ mémoire tampon XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .</span><span class="sxs-lookup"><span data-stu-id="12e87-133">Populate an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span>
    ```
    buffer.AudioBytes = dwChunkSize;  //size of the audio buffer in bytes
    buffer.pAudioData = pDataBuffer;  //buffer containing audio data
    buffer.Flags = XAUDIO2_END_OF_STREAM; // tell the source voice not to expect any data after this buffer
    ```

    

## <a name="related-topics"></a><span data-ttu-id="12e87-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="12e87-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12e87-135">Prise en main</span><span class="sxs-lookup"><span data-stu-id="12e87-135">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="12e87-136">Procédure : lire un son avec XAudio2</span><span class="sxs-lookup"><span data-stu-id="12e87-136">How to: Play a Sound with XAudio2</span></span>](how-to--play-a-sound-with-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="12e87-137">Référence de programmation XAudio2</span><span class="sxs-lookup"><span data-stu-id="12e87-137">XAudio2 Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 
