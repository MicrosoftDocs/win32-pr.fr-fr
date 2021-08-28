---
description: Cette rubrique décrit les étapes permettant de remplir les structures requises pour lire des données audio dans XAudio2.
ms.assetid: caeb522e-d4f6-91e2-5e85-ea0af0f61300
title: 'Procédure : charger des fichiers de données audio dans XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bacf08e8f16e5cd9c42409776b02846990b9d66d685a0186314445742f23341
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962658"
---
# <a name="how-to-load-audio-data-files-in-xaudio2"></a>Procédure : charger des fichiers de données audio dans XAudio2

> [!Note]  
> ce contenu s’applique uniquement aux applications de bureau et nécessite une révision pour fonctionner dans une application Windows Store. Reportez-vous à la documentation de [**CreateFile2**](/windows/win32/api/fileapi/nf-fileapi-createfile2), [**CreateEventEx**](/windows/win32/api/synchapi/nf-synchapi-createeventexa), [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex), [**SetFilePointerEx**](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex)et [**GetOverlappedResultEx**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresultex). consultez SoundFileReader. h/. cpp dans l’exemple BasicSound Windows 8 dans la [galerie d’exemples SDK Windows](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20file%20playback%20sample%20(Windows%208)).

 

Cette rubrique décrit les étapes permettant de remplir les structures requises pour lire des données audio dans XAudio2. Les étapes suivantes chargent les segments « fmt » et « Data » d’un fichier audio, et les utilisent pour remplir une structure **WAVEFORMATEXTENSIBLE** et une structure de [**\_ mémoire tampon XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .

-   [Préparation de l’analyse du fichier audio.](#preparing-to-parse-the-audio-file)
-   [Remplissage des structures XAudio2 avec le contenu de blocs RIFF.](#populating-xaudio2-structures-with-the-contents-of-riff-chunks)

## <a name="preparing-to-parse-the-audio-file"></a>Préparation de l’analyse du fichier audio

Les fichiers audio pris en charge par XAudio2 utilisent le format RIFF (Resource Interchange File Format). RIFF est décrit dans la vue d’ensemble du [format RIFF (Resource Interchange File Format)](resource-interchange-file-format--riff-.md) . Les données audio d’un fichier RIFF sont chargées en recherchant le bloc RIFF, puis en parcourant le bloc pour rechercher des blocs individuels contenus dans le bloc RIFF. Les fonctions suivantes sont des exemples de code permettant de rechercher des segments et de charger des données contenues dans les segments.

-   Pour rechercher un segment dans un fichier RIFF :

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

    

-   Pour lire des données dans un segment une fois qu’elles ont été localisées.

    Une fois qu’un segment souhaité est trouvé, ses données peuvent être lues en ajustant le pointeur de fichier au début de la section de données du bloc. Une fonction permettant de lire les données à partir d’un segment une fois qu’elle a été trouvée peut se présenter comme suit.

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

    

## <a name="populating-xaudio2-structures-with-the-contents-of-riff-chunks"></a>Remplissage de structures XAudio2 avec le contenu de blocs RIFF

Pour que XAudio2 lise l’audio avec une voix source, il a besoin d’une structure **WAVEFORMATEX** et d’une structure de [**\_ mémoire tampon XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) . La structure **WAVEFORMATEX** peut être une plus grande structure telle que **WAVEFORMATEXTENSIBLE** qui contient une structure **WAVEFORMATEX** comme premier membre. Pour plus d’informations, consultez la page de référence de **WAVEFORMATEX** .

Dans cet exemple, un **WAVEFORMATEXTENSIBLE** est utilisé pour autoriser le chargement de fichiers audio PCM avec plus de deux canaux.

Les étapes suivantes illustrent l’utilisation des fonctions décrites ci-dessus pour remplir une structure **WAVEFORMATEXTENSIBLE** et une structure de [**\_ mémoire tampon XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) . Dans ce cas, le fichier audio en cours de chargement contient des données PCM et ne contient qu’un segment « RIFF », « fmt » et « Data ». D’autres formats peuvent contenir des types de blocs supplémentaires, comme décrit dans le [fichier RIFF (Resource Interchange File Format)](resource-interchange-file-format--riff-.md).

1.  Déclarez les structures de [**\_ mémoire tampon**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) **WAVEFORMATEXTENSIBLE** et XAUDIO2.
    ```
    WAVEFORMATEXTENSIBLE wfx = {0};
    XAUDIO2_BUFFER buffer = {0};
    ```

    

2.  Ouvrez le fichier audio avec CreateFile.
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

    

3.  Localisez le bloc « RIFF » dans le fichier audio, puis vérifiez le type de fichier.
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

    

4.  Localisez le segment « fmt » et copiez son contenu dans une structure **WAVEFORMATEXTENSIBLE** .
    ```
    FindChunk(hFile,fourccFMT, dwChunkSize, dwChunkPosition );
    ReadChunkData(hFile, &wfx, dwChunkSize, dwChunkPosition );
    ```

    

5.  Localisez le segment « Data » et lisez son contenu dans une mémoire tampon.
    ```
    //fill out the audio data buffer with the contents of the fourccDATA chunk
    FindChunk(hFile,fourccDATA,dwChunkSize, dwChunkPosition );
    BYTE * pDataBuffer = new BYTE[dwChunkSize];
    ReadChunkData(hFile, pDataBuffer, dwChunkSize, dwChunkPosition);
    ```

    

6.  Remplir une structure de [**\_ mémoire tampon XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .
    ```
    buffer.AudioBytes = dwChunkSize;  //size of the audio buffer in bytes
    buffer.pAudioData = pDataBuffer;  //buffer containing audio data
    buffer.Flags = XAUDIO2_END_OF_STREAM; // tell the source voice not to expect any data after this buffer
    ```

    

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en main](getting-started.md)
</dt> <dt>

[Procédure : lire un son avec XAudio2](how-to--play-a-sound-with-xaudio2.md)
</dt> <dt>

[Référence de programmation XAudio2](programming-reference.md)
</dt> </dl>

 

 
