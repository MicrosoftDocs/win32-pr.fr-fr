---
description: Ce didacticiel montre comment utiliser le lecteur source pour décoder l’audio d’un fichier multimédia et écrire l’audio dans un fichier WAVE.
ms.assetid: ed40e201-c6ed-444f-bdaa-a5f33d1cc068
title: 'Didacticiel : décodage de l’audio'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4ad5dbac47680c4d8faa73affa711b987edf220e05324d88cd0ffbda3bb93e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118237662"
---
# <a name="tutorial-decoding-audio"></a>Didacticiel : décodage de l’audio

Ce didacticiel montre comment utiliser le [lecteur source](source-reader.md) pour décoder l’audio d’un fichier multimédia et écrire l’audio dans un fichier wave. Ce didacticiel est basé sur l’exemple de [clip audio](audio-clip-sample.md) .

-   [Vue d'ensemble](#overview)
-   [Fichiers d’en-tête et de bibliothèque](#header-and-library-files)
-   [Implémenter wmain](#implement-wmain)
-   [Écrire le fichier WAVE](#write-the-wave-file)
-   [Configurer le lecteur source](#configure-the-source-reader)
-   [Écrire l’en-tête de fichier WAVE](#write-the-wave-file-header)
-   [Calculer la taille de données maximale](#calculate-the-maximum-data-size)
-   [Décoder l’audio](#decode-the-audio)
-   [Finaliser l’en-tête de fichier](#finalize-the-file-header)
-   [Rubriques connexes](#related-topics)

## <a name="overview"></a>Vue d’ensemble

Dans ce didacticiel, vous allez créer une application console qui prend deux arguments de ligne de commande : le nom d’un fichier d’entrée qui contient un flux audio et le nom du fichier de sortie. L’application lit cinq secondes de données audio à partir du fichier d’entrée et écrit l’audio dans le fichier de sortie en tant que données WAVE.

Pour récupérer les données audio décodées, l’application utilise l’objet lecteur source. Le lecteur source expose l’interface [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) . pour écrire les données audio décodées dans le fichier WAVE, les applications utilisent Windows fonctions d’e/s. L’illustration suivante montre ce processus.

![Diagramme montrant le lecteur source qui obtient les données audio du fichier source.](images/audio-clip-tutorial.gif)

Dans sa forme la plus simple, un fichier WAVE présente la structure suivante :



| Type de données                              | Taille (octets) | Valeur                                                                 |
|----------------------------------------|--------------|-----------------------------------------------------------------------|
| **FOURCC**                             | 4            | RÉPARTITION                                                                |
| **DWORD**                              | 4            | Taille totale du fichier, à l’exclusion des 8 premiers octets                      |
| **FOURCC**                             | 4            | Wave                                                                |
| **FOURCC**                             | 4            | fmt                                                                |
| **DWORD**                              | 4            | Taille des données [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) qui suivent. |
| [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) | Variable       | En-tête de format audio.                                                  |
| **FOURCC**                             | 4            | métadonnée                                                                |
| **DWORD**                              | 4            | Taille des données audio.                                               |
| **POIDS**\[\]                           | Variable       | Données audio.                                                           |



 

> [!Note]  
> Un **FourCC** est une **valeur DWORD** formée par la concaténation de quatre caractères ASCII.

 

Cette structure de base peut être étendue en ajoutant des métadonnées de fichier et d’autres informations, qui n’entrent pas dans le cadre de ce didacticiel.

## <a name="header-and-library-files"></a>Fichiers d’en-tête et de bibliothèque

Incluez les fichiers d’en-tête suivants dans votre projet :


```C++
#define WINVER _WIN32_WINNT_WIN7

#include <windows.h>
#include <mfapi.h>
#include <mfidl.h>
#include <mfreadwrite.h>
#include <stdio.h>
#include <mferror.h>
```



Lien vers les bibliothèques suivantes :

-   mfplat. lib
-   mfreadwrite. lib
-   mfuuid. lib

## <a name="implement-wmain"></a>Implémenter wmain

Le code suivant illustre la fonction de point d’entrée pour l’application.


```C++
int wmain(int argc, wchar_t* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc != 3)
    {
        printf("arguments: input_file output_file.wav\n");
        return 1;
    }

    const WCHAR *wszSourceFile = argv[1];
    const WCHAR *wszTargetFile = argv[2];

    const LONG MAX_AUDIO_DURATION_MSEC = 5000; // 5 seconds

    HRESULT hr = S_OK;

    IMFSourceReader *pReader = NULL;
    HANDLE hFile = INVALID_HANDLE_VALUE;

    // Initialize the COM library.
    hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);

    // Initialize the Media Foundation platform.
    if (SUCCEEDED(hr))
    {
        hr = MFStartup(MF_VERSION);
    }

    // Create the source reader to read the input file.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateSourceReaderFromURL(wszSourceFile, NULL, &pReader);
        if (FAILED(hr))
        {
            printf("Error opening input file: %S\n", wszSourceFile, hr);
        }
    }

    // Open the output file for writing.
    if (SUCCEEDED(hr))
    {
        hFile = CreateFile(wszTargetFile, GENERIC_WRITE, FILE_SHARE_READ, NULL,
            CREATE_ALWAYS, 0, NULL);

        if (hFile == INVALID_HANDLE_VALUE)
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
            printf("Cannot create output file: %S\n", wszTargetFile, hr);
        }
    }

    // Write the WAVE file.
    if (SUCCEEDED(hr))
    {
        hr = WriteWaveFile(pReader, hFile, MAX_AUDIO_DURATION_MSEC);
    }

    if (FAILED(hr))
    {
        printf("Failed, hr = 0x%X\n", hr);
    }

    // Clean up.
    if (hFile != INVALID_HANDLE_VALUE)
    {
        CloseHandle(hFile);
    }

    SafeRelease(&pReader);
    MFShutdown();
    CoUninitialize();

    return SUCCEEDED(hr) ? 0 : 1;
};
```



Cette fonction effectue les opérations suivantes :

1.  Appelle [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) pour initialiser la bibliothèque com.
2.  Appelle [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) pour initialiser la plateforme Media Foundation.
3.  Appelle [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl) pour créer le lecteur source. Cette fonction prend le nom du fichier d’entrée et reçoit un pointeur d’interface [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) .
4.  Crée le fichier de sortie en appelant la fonction **CreateFile** , qui retourne un handle de fichier.
5.  Appelle la fonction [WriteWavFile](#write-the-wave-file) définie par l’application. Cette fonction décode l’audio et écrit le fichier WAVE.
6.  Libère le pointeur [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) et le handle de fichier.
7.  Appelle [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) pour arrêter la plateforme Media Foundation.
8.  Appelle [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) pour libérer la bibliothèque com.

## <a name="write-the-wave-file"></a>Écrire le fichier WAVE

La majeure partie du travail se produit dans la `WriteWavFile` fonction, qui est appelée à partir de `wmain` .


```C++
//-------------------------------------------------------------------
// WriteWaveFile
//
// Writes a WAVE file by getting audio data from the source reader.
//
//-------------------------------------------------------------------

HRESULT WriteWaveFile(
    IMFSourceReader *pReader,   // Pointer to the source reader.
    HANDLE hFile,               // Handle to the output file.
    LONG msecAudioData          // Maximum amount of audio data to write, in msec.
    )
{
    HRESULT hr = S_OK;

    DWORD cbHeader = 0;         // Size of the WAVE file header, in bytes.
    DWORD cbAudioData = 0;      // Total bytes of PCM audio data written to the file.
    DWORD cbMaxAudioData = 0;

    IMFMediaType *pAudioType = NULL;    // Represents the PCM audio format.

    // Configure the source reader to get uncompressed PCM audio from the source file.

    hr = ConfigureAudioStream(pReader, &pAudioType);

    // Write the WAVE file header.
    if (SUCCEEDED(hr))
    {
        hr = WriteWaveHeader(hFile, pAudioType, &cbHeader);
    }

    // Calculate the maximum amount of audio to decode, in bytes.
    if (SUCCEEDED(hr))
    {
        cbMaxAudioData = CalculateMaxAudioDataSize(pAudioType, cbHeader, msecAudioData);

        // Decode audio data to the file.
        hr = WriteWaveData(hFile, pReader, cbMaxAudioData, &cbAudioData);
    }

    // Fix up the RIFF headers with the correct sizes.
    if (SUCCEEDED(hr))
    {
        hr = FixUpChunkSizes(hFile, cbHeader, cbAudioData);
    }

    SafeRelease(&pAudioType);
    return hr;
}
```



Cette fonction appelle une série d’autres fonctions définies par l’application :

1.  La fonction [ConfigureAudioStream](#configure-the-source-reader) Initialise le lecteur source. Cette fonction reçoit un pointeur vers l’interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , qui est utilisée pour obtenir une description du format audio décodé, y compris le taux d’échantillonnage, le nombre de canaux et la profondeur de bit (bits par échantillon).
2.  La fonction WriteWaveHeader écrit la première partie du fichier WAVE, y compris l’en-tête et le début du segment « Data ».
3.  La fonction CalculateMaxAudioDataSize calcule la quantité maximale de données audio à écrire dans le fichier, en octets.
4.  La fonction WriteWaveData écrit les données audio PCM dans le fichier.
5.  La fonction FixUpChunkSizes écrit les informations de taille de fichier qui apparaissent après les valeurs **FourCC** « Riff » et « Data » dans le fichier wave. (Ces valeurs ne sont pas connues jusqu’à la `WriteWaveData` fin.)

Ces fonctions sont présentées dans les sections restantes de ce didacticiel.

## <a name="configure-the-source-reader"></a>Configurer le lecteur source

La `ConfigureAudioStream` fonction configure le lecteur source pour décoder le flux audio dans le fichier source. Elle retourne également des informations sur le format de l’audio décodé.

Dans Media Foundation, les formats multimédias sont décrits à l’aide d’objets de *type de média* . Un objet de type de média expose l’interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , qui hérite de l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Fondamentalement, un type de média est une collection de propriétés qui décrivent le format. Pour plus d’informations, consultez [types de médias](media-types.md).


```C++
//-------------------------------------------------------------------
// ConfigureAudioStream
//
// Selects an audio stream from the source file, and configures the
// stream to deliver decoded PCM audio.
//-------------------------------------------------------------------

HRESULT ConfigureAudioStream(
    IMFSourceReader *pReader,   // Pointer to the source reader.
    IMFMediaType **ppPCMAudio   // Receives the audio format.
    )
{
    IMFMediaType *pUncompressedAudioType = NULL;
    IMFMediaType *pPartialType = NULL;

    // Select the first audio stream, and deselect all other streams.
    HRESULT hr = pReader->SetStreamSelection(
        (DWORD)MF_SOURCE_READER_ALL_STREAMS, FALSE);

    if (SUCCEEDED(hr))
    {
        hr = pReader->SetStreamSelection(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM, TRUE);
    }

    // Create a partial media type that specifies uncompressed PCM audio.
    hr = MFCreateMediaType(&pPartialType);

    if (SUCCEEDED(hr))
    {
        hr = pPartialType->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Audio);
    }

    if (SUCCEEDED(hr))
    {
        hr = pPartialType->SetGUID(MF_MT_SUBTYPE, MFAudioFormat_PCM);
    }

    // Set this type on the source reader. The source reader will
    // load the necessary decoder.
    if (SUCCEEDED(hr))
    {
        hr = pReader->SetCurrentMediaType(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM,
            NULL, pPartialType);
    }

    // Get the complete uncompressed format.
    if (SUCCEEDED(hr))
    {
        hr = pReader->GetCurrentMediaType(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM,
            &pUncompressedAudioType);
    }

    // Ensure the stream is selected.
    if (SUCCEEDED(hr))
    {
        hr = pReader->SetStreamSelection(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM,
            TRUE);
    }

    // Return the PCM format to the caller.
    if (SUCCEEDED(hr))
    {
        *ppPCMAudio = pUncompressedAudioType;
        (*ppPCMAudio)->AddRef();
    }

    SafeRelease(&pUncompressedAudioType);
    SafeRelease(&pPartialType);
    return hr;
}
```



La `ConfigureAudioStream` fonction effectue les opérations suivantes :

1.  Appelle la méthode [**IMFSourceReader :: SetStreamSelection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) pour sélectionner le flux audio et désélectionner tous les autres flux. Cette étape peut améliorer les performances, car elle empêche le lecteur source de tenir sur des trames vidéo que l’application n’utilise pas.
2.  Crée un type de média *partiel* qui spécifie l’audio PCM. La fonction crée le type partiel comme suit :
    1.  Appelle [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) pour créer un objet de type de média vide.
    2.  Affecte à l’attribut de [**\_ \_ \_ type principal MF MT**](mf-mt-major-type-attribute.md) la valeur **\_ audio MFMediaType**.
    3.  Définit l’attribut de [**\_ sous- \_ type MF MT**](mf-mt-subtype-attribute.md) sur **MFAudioFormat \_ PCM**.
3.  Appelle [**IMFSourceReader :: SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) pour définir le type partiel sur le lecteur source. Si le fichier source contient des données audio encodées, le lecteur source charge automatiquement le décodeur audio nécessaire.
4.  Appelle [**IMFSourceReader :: GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) pour récupérer le type de média PCM réel. Cette méthode retourne un type de média avec tous les détails de format renseignés, tels que le taux d’échantillonnage audio et le nombre de canaux.
5.  Appelle [**IMFSourceReader :: SetStreamSelection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) pour activer le flux audio.

## <a name="write-the-wave-file-header"></a>Écrire l’en-tête de fichier WAVE

La `WriteWaveHeader` fonction écrit l’en-tête de fichier wave.

La seule API Media Foundation appelée à partir de cette fonction est [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype), qui convertit le type de média en structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .


```C++
//-------------------------------------------------------------------
// WriteWaveHeader
//
// Write the WAVE file header.
//
// Note: This function writes placeholder values for the file size
// and data size, as these values will need to be filled in later.
//-------------------------------------------------------------------

HRESULT WriteWaveHeader(
    HANDLE hFile,               // Output file.
    IMFMediaType *pMediaType,   // PCM audio format.
    DWORD *pcbWritten           // Receives the size of the header.
    )
{
    HRESULT hr = S_OK;
    UINT32 cbFormat = 0;

    WAVEFORMATEX *pWav = NULL;

    *pcbWritten = 0;

    // Convert the PCM audio format into a WAVEFORMATEX structure.
    hr = MFCreateWaveFormatExFromMFMediaType(pMediaType, &pWav, &cbFormat);

    // Write the 'RIFF' header and the start of the 'fmt ' chunk.
    if (SUCCEEDED(hr))
    {
        DWORD header[] = {
            // RIFF header
            FCC('RIFF'),
            0,
            FCC('WAVE'),
            // Start of 'fmt ' chunk
            FCC('fmt '),
            cbFormat
        };

        DWORD dataHeader[] = { FCC('data'), 0 };

        hr = WriteToFile(hFile, header, sizeof(header));

        // Write the WAVEFORMATEX structure.
        if (SUCCEEDED(hr))
        {
            hr = WriteToFile(hFile, pWav, cbFormat);
        }

        // Write the start of the 'data' chunk

        if (SUCCEEDED(hr))
        {
            hr = WriteToFile(hFile, dataHeader, sizeof(dataHeader));
        }

        if (SUCCEEDED(hr))
        {
            *pcbWritten = sizeof(header) + cbFormat + sizeof(dataHeader);
        }
    }


    CoTaskMemFree(pWav);
    return hr;
}
```



la `WriteToFile` fonction est une fonction d’assistance simple qui encapsule le Windows fonction **WriteFile** et retourne une valeur **HRESULT** .


```C++
//-------------------------------------------------------------------
//
// Writes a block of data to a file
//
// hFile: Handle to the file.
// p: Pointer to the buffer to write.
// cb: Size of the buffer, in bytes.
//
//-------------------------------------------------------------------

HRESULT WriteToFile(HANDLE hFile, void* p, DWORD cb)
{
    DWORD cbWritten = 0;
    HRESULT hr = S_OK;

    BOOL bResult = WriteFile(hFile, p, cb, &cbWritten, NULL);
    if (!bResult)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }
    return hr;
}
```



## <a name="calculate-the-maximum-data-size"></a>Calculer la taille de données maximale

Étant donné que la taille du fichier est stockée sous la forme d’une valeur de 4 octets dans l’en-tête de fichier, un fichier WAVE est limité à une taille maximale de 0xFFFFFFFF octets, soit environ 4 Go. Cette valeur comprend la taille de l’en-tête de fichier. Le format audio PCM a une vitesse binaire constante, ce qui vous permet de calculer la taille maximale des données à partir du format audio, comme suit :


```C++
//-------------------------------------------------------------------
// CalculateMaxAudioDataSize
//
// Calculates how much audio to write to the WAVE file, given the
// audio format and the maximum duration of the WAVE file.
//-------------------------------------------------------------------

DWORD CalculateMaxAudioDataSize(
    IMFMediaType *pAudioType,    // The PCM audio format.
    DWORD cbHeader,              // The size of the WAVE file header.
    DWORD msecAudioData          // Maximum duration, in milliseconds.
    )
{
    UINT32 cbBlockSize = 0;         // Audio frame size, in bytes.
    UINT32 cbBytesPerSecond = 0;    // Bytes per second.

    // Get the audio block size and number of bytes/second from the audio format.

    cbBlockSize = MFGetAttributeUINT32(pAudioType, MF_MT_AUDIO_BLOCK_ALIGNMENT, 0);
    cbBytesPerSecond = MFGetAttributeUINT32(pAudioType, MF_MT_AUDIO_AVG_BYTES_PER_SECOND, 0);

    // Calculate the maximum amount of audio data to write.
    // This value equals (duration in seconds x bytes/second), but cannot
    // exceed the maximum size of the data chunk in the WAVE file.

        // Size of the desired audio clip in bytes:
    DWORD cbAudioClipSize = (DWORD)MulDiv(cbBytesPerSecond, msecAudioData, 1000);

    // Largest possible size of the data chunk:
    DWORD cbMaxSize = MAXDWORD - cbHeader;

    // Maximum size altogether.
    cbAudioClipSize = min(cbAudioClipSize, cbMaxSize);

    // Round to the audio block size, so that we do not write a partial audio frame.
    cbAudioClipSize = (cbAudioClipSize / cbBlockSize) * cbBlockSize;

    return cbAudioClipSize;
}
```



Pour éviter les images audio partielles, la taille est arrondie à l’alignement de bloc, qui est stocké dans l’attribut d' [**\_ \_ \_ \_ alignement de bloc audio MF MT**](mf-mt-audio-block-alignment-attribute.md) .

## <a name="decode-the-audio"></a>Décoder l’audio

La `WriteWaveData` fonction lit les données audio décodées à partir du fichier source et les écrit dans le fichier wave.


```C++
//-------------------------------------------------------------------
// WriteWaveData
//
// Decodes PCM audio data from the source file and writes it to
// the WAVE file.
//-------------------------------------------------------------------

HRESULT WriteWaveData(
    HANDLE hFile,               // Output file.
    IMFSourceReader *pReader,   // Source reader.
    DWORD cbMaxAudioData,       // Maximum amount of audio data (bytes).
    DWORD *pcbDataWritten       // Receives the amount of data written.
    )
{
    HRESULT hr = S_OK;
    DWORD cbAudioData = 0;
    DWORD cbBuffer = 0;
    BYTE *pAudioData = NULL;

    IMFSample *pSample = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    // Get audio samples from the source reader.
    while (true)
    {
        DWORD dwFlags = 0;

        // Read the next sample.
        hr = pReader->ReadSample(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM,
            0, NULL, &dwFlags, NULL, &pSample );

        if (FAILED(hr)) { break; }

        if (dwFlags & MF_SOURCE_READERF_CURRENTMEDIATYPECHANGED)
        {
            printf("Type change - not supported by WAVE file format.\n");
            break;
        }
        if (dwFlags & MF_SOURCE_READERF_ENDOFSTREAM)
        {
            printf("End of input file.\n");
            break;
        }

        if (pSample == NULL)
        {
            printf("No sample\n");
            continue;
        }

        // Get a pointer to the audio data in the sample.

        hr = pSample->ConvertToContiguousBuffer(&pBuffer);

        if (FAILED(hr)) { break; }


        hr = pBuffer->Lock(&pAudioData, NULL, &cbBuffer);

        if (FAILED(hr)) { break; }


        // Make sure not to exceed the specified maximum size.
        if (cbMaxAudioData - cbAudioData < cbBuffer)
        {
            cbBuffer = cbMaxAudioData - cbAudioData;
        }

        // Write this data to the output file.
        hr = WriteToFile(hFile, pAudioData, cbBuffer);

        if (FAILED(hr)) { break; }

        // Unlock the buffer.
        hr = pBuffer->Unlock();
        pAudioData = NULL;

        if (FAILED(hr)) { break; }

        // Update running total of audio data.
        cbAudioData += cbBuffer;

        if (cbAudioData >= cbMaxAudioData)
        {
            break;
        }

        SafeRelease(&pSample);
        SafeRelease(&pBuffer);
    }

    if (SUCCEEDED(hr))
    {
        printf("Wrote %d bytes of audio data.\n", cbAudioData);

        *pcbDataWritten = cbAudioData;
    }

    if (pAudioData)
    {
        pBuffer->Unlock();
    }

    SafeRelease(&pBuffer);
    SafeRelease(&pSample);
    return hr;
}
```



La `WriteWaveData` fonction effectue les opérations suivantes dans une boucle :

1.  Appelle [**IMFSourceReader :: ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) pour lire l’audio à partir du fichier source. Le paramètre *dwFlags* reçoit un or **au niveau du** bit des indicateurs de l’énumération de l' [**\_ \_ \_ indicateur de lecteur source MF**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag) . Le paramètre *pSample* reçoit un pointeur vers l’interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , qui est utilisée pour accéder aux données audio. Dans certains cas, un appel à **ReadSample** ne génère pas de données, auquel cas le pointeur **IMFSample** est **null**.
2.  Recherche les indicateurs suivants dans *dwFlags* :
    -   **MF \_ SOURCE \_ READERF \_ CURRENTMEDIATYPECHANGED**. Cet indicateur indique une modification de format dans le fichier source. Les fichiers WAVE ne prennent pas en charge les modifications de format.
    -   **MF \_ SOURCE \_ READERF \_ ENDOFSTREAM**. Cet indicateur indique la fin du flux.
3.  Appelle [**IMFSample :: ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer) pour obtenir un pointeur vers un objet de mémoire tampon.
4.  Appelle [**IMFMediaBuffer :: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) pour obtenir un pointeur vers la mémoire tampon.
5.  Écrit les données audio dans le fichier de sortie.
6.  Appelle [**IMFMediaBuffer :: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) pour déverrouiller l’objet de mémoire tampon.

La fonction s’arrête hors de la boucle lorsque l’un des éléments suivants se produit :

-   Le format de flux change.
-   La fin du flux est atteinte.
-   La quantité maximale de données audio est écrite dans le fichier de sortie.
-   Une erreur se produit.

## <a name="finalize-the-file-header"></a>Finaliser l’en-tête de fichier

Les valeurs de taille stockées dans l’en-tête WAVE ne sont pas connues jusqu’à la fin de la fonction précédente. Le `FixUpChunkSizes` remplit ces valeurs :


```C++
//-------------------------------------------------------------------
// FixUpChunkSizes
//
// Writes the file-size information into the WAVE file header.
//
// WAVE files use the RIFF file format. Each RIFF chunk has a data
// size, and the RIFF header has a total file size.
//-------------------------------------------------------------------

HRESULT FixUpChunkSizes(
    HANDLE hFile,           // Output file.
    DWORD cbHeader,         // Size of the 'fmt ' chuck.
    DWORD cbAudioData       // Size of the 'data' chunk.
    )
{
    HRESULT hr = S_OK;

    LARGE_INTEGER ll;
    ll.QuadPart = cbHeader - sizeof(DWORD);

    if (0 == SetFilePointerEx(hFile, ll, NULL, FILE_BEGIN))
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }

    // Write the data size.

    if (SUCCEEDED(hr))
    {
        hr = WriteToFile(hFile, &cbAudioData, sizeof(cbAudioData));
    }

    if (SUCCEEDED(hr))
    {
        // Write the file size.
        ll.QuadPart = sizeof(FOURCC);

        if (0 == SetFilePointerEx(hFile, ll, NULL, FILE_BEGIN))
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
        }
    }

    if (SUCCEEDED(hr))
    {
        DWORD cbRiffFileSize = cbHeader + cbAudioData - 8;

        // NOTE: The "size" field in the RIFF header does not include
        // the first 8 bytes of the file. (That is, the size of the
        // data that appears after the size field.)

        hr = WriteToFile(hFile, &cbRiffFileSize, sizeof(cbRiffFileSize));
    }

    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de média audio](audio-media-types.md)
</dt> <dt>

[Lecteur source](source-reader.md)
</dt> <dt>

[**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 
