---
description: Ce didacticiel montre comment utiliser le lecteur source pour décoder l’audio d’un fichier multimédia et écrire l’audio dans un fichier WAVE.
ms.assetid: ed40e201-c6ed-444f-bdaa-a5f33d1cc068
title: 'Didacticiel : décodage de l’audio'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539eb6d9f48419b62fa1c379c636abaf2bb0a63a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568107"
---
# <a name="tutorial-decoding-audio"></a><span data-ttu-id="9e439-103">Didacticiel : décodage de l’audio</span><span class="sxs-lookup"><span data-stu-id="9e439-103">Tutorial: Decoding Audio</span></span>

<span data-ttu-id="9e439-104">Ce didacticiel montre comment utiliser le [lecteur source](source-reader.md) pour décoder l’audio d’un fichier multimédia et écrire l’audio dans un fichier wave.</span><span class="sxs-lookup"><span data-stu-id="9e439-104">This tutorial shows how to use the [Source Reader](source-reader.md) to decode audio from a media file and write the audio to a WAVE file.</span></span> <span data-ttu-id="9e439-105">Ce didacticiel est basé sur l’exemple de [clip audio](audio-clip-sample.md) .</span><span class="sxs-lookup"><span data-stu-id="9e439-105">The tutorial is based on the [Audio Clip](audio-clip-sample.md) sample.</span></span>

-   [<span data-ttu-id="9e439-106">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="9e439-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="9e439-107">Fichiers d’en-tête et de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9e439-107">Header and Library Files</span></span>](#header-and-library-files)
-   [<span data-ttu-id="9e439-108">Implémenter wmain</span><span class="sxs-lookup"><span data-stu-id="9e439-108">Implement wmain</span></span>](#implement-wmain)
-   [<span data-ttu-id="9e439-109">Écrire le fichier WAVE</span><span class="sxs-lookup"><span data-stu-id="9e439-109">Write the WAVE File</span></span>](#write-the-wave-file)
-   [<span data-ttu-id="9e439-110">Configurer le lecteur source</span><span class="sxs-lookup"><span data-stu-id="9e439-110">Configure the Source Reader</span></span>](#configure-the-source-reader)
-   [<span data-ttu-id="9e439-111">Écrire l’en-tête de fichier WAVE</span><span class="sxs-lookup"><span data-stu-id="9e439-111">Write the WAVE File Header</span></span>](#write-the-wave-file-header)
-   [<span data-ttu-id="9e439-112">Calculer la taille de données maximale</span><span class="sxs-lookup"><span data-stu-id="9e439-112">Calculate the Maximum Data Size</span></span>](#calculate-the-maximum-data-size)
-   [<span data-ttu-id="9e439-113">Décoder l’audio</span><span class="sxs-lookup"><span data-stu-id="9e439-113">Decode the Audio</span></span>](#decode-the-audio)
-   [<span data-ttu-id="9e439-114">Finaliser l’en-tête de fichier</span><span class="sxs-lookup"><span data-stu-id="9e439-114">Finalize the File Header</span></span>](#finalize-the-file-header)
-   [<span data-ttu-id="9e439-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9e439-115">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="9e439-116">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="9e439-116">Overview</span></span>

<span data-ttu-id="9e439-117">Dans ce didacticiel, vous allez créer une application console qui prend deux arguments de ligne de commande : le nom d’un fichier d’entrée qui contient un flux audio et le nom du fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="9e439-117">In this tutorial, you will create a console application that takes two command-line arguments: The name of an input file that contains an audio stream, and the output file name.</span></span> <span data-ttu-id="9e439-118">L’application lit cinq secondes de données audio à partir du fichier d’entrée et écrit l’audio dans le fichier de sortie en tant que données WAVE.</span><span class="sxs-lookup"><span data-stu-id="9e439-118">The application reads five seconds of audio data from the input file and writes the audio to the output file as WAVE data.</span></span>

<span data-ttu-id="9e439-119">Pour récupérer les données audio décodées, l’application utilise l’objet lecteur source.</span><span class="sxs-lookup"><span data-stu-id="9e439-119">To get the decoded audio data, the application uses the source reader object.</span></span> <span data-ttu-id="9e439-120">Le lecteur source expose l’interface [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) .</span><span class="sxs-lookup"><span data-stu-id="9e439-120">The source reader exposes the [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) interface.</span></span> <span data-ttu-id="9e439-121">Pour écrire les données audio décodées dans le fichier WAVE, les applications utilisent les fonctions d’e/s de Windows.</span><span class="sxs-lookup"><span data-stu-id="9e439-121">To write the decoded audio to the WAVE file, the applications uses Windows I/O functions.</span></span> <span data-ttu-id="9e439-122">L’illustration suivante montre ce processus.</span><span class="sxs-lookup"><span data-stu-id="9e439-122">The following image illustrates this process.</span></span>

![Diagramme montrant le lecteur source qui obtient les données audio du fichier source.](images/audio-clip-tutorial.gif)

<span data-ttu-id="9e439-124">Dans sa forme la plus simple, un fichier WAVE présente la structure suivante :</span><span class="sxs-lookup"><span data-stu-id="9e439-124">In its simplest form, a WAVE file has the following structure:</span></span>



| <span data-ttu-id="9e439-125">Type de données</span><span class="sxs-lookup"><span data-stu-id="9e439-125">Data Type</span></span>                              | <span data-ttu-id="9e439-126">Taille (octets)</span><span class="sxs-lookup"><span data-stu-id="9e439-126">Size (Bytes)</span></span> | <span data-ttu-id="9e439-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e439-127">Value</span></span>                                                                 |
|----------------------------------------|--------------|-----------------------------------------------------------------------|
| <span data-ttu-id="9e439-128">**FOURCC**</span><span class="sxs-lookup"><span data-stu-id="9e439-128">**FOURCC**</span></span>                             | <span data-ttu-id="9e439-129">4</span><span class="sxs-lookup"><span data-stu-id="9e439-129">4</span></span>            | <span data-ttu-id="9e439-130">RÉPARTITION</span><span class="sxs-lookup"><span data-stu-id="9e439-130">'RIFF'</span></span>                                                                |
| <span data-ttu-id="9e439-131">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="9e439-131">**DWORD**</span></span>                              | <span data-ttu-id="9e439-132">4</span><span class="sxs-lookup"><span data-stu-id="9e439-132">4</span></span>            | <span data-ttu-id="9e439-133">Taille totale du fichier, à l’exclusion des 8 premiers octets</span><span class="sxs-lookup"><span data-stu-id="9e439-133">Total file size, not including the first 8 bytes</span></span>                      |
| <span data-ttu-id="9e439-134">**FOURCC**</span><span class="sxs-lookup"><span data-stu-id="9e439-134">**FOURCC**</span></span>                             | <span data-ttu-id="9e439-135">4</span><span class="sxs-lookup"><span data-stu-id="9e439-135">4</span></span>            | <span data-ttu-id="9e439-136">Wave</span><span class="sxs-lookup"><span data-stu-id="9e439-136">'WAVE'</span></span>                                                                |
| <span data-ttu-id="9e439-137">**FOURCC**</span><span class="sxs-lookup"><span data-stu-id="9e439-137">**FOURCC**</span></span>                             | <span data-ttu-id="9e439-138">4</span><span class="sxs-lookup"><span data-stu-id="9e439-138">4</span></span>            | <span data-ttu-id="9e439-139">fmt</span><span class="sxs-lookup"><span data-stu-id="9e439-139">'fmt '</span></span>                                                                |
| <span data-ttu-id="9e439-140">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="9e439-140">**DWORD**</span></span>                              | <span data-ttu-id="9e439-141">4</span><span class="sxs-lookup"><span data-stu-id="9e439-141">4</span></span>            | <span data-ttu-id="9e439-142">Taille des données [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) qui suivent.</span><span class="sxs-lookup"><span data-stu-id="9e439-142">Size of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) data that follows.</span></span> |
| <span data-ttu-id="9e439-143">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9e439-143">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> | <span data-ttu-id="9e439-144">Variable</span><span class="sxs-lookup"><span data-stu-id="9e439-144">Varies</span></span>       | <span data-ttu-id="9e439-145">En-tête de format audio.</span><span class="sxs-lookup"><span data-stu-id="9e439-145">Audio format header.</span></span>                                                  |
| <span data-ttu-id="9e439-146">**FOURCC**</span><span class="sxs-lookup"><span data-stu-id="9e439-146">**FOURCC**</span></span>                             | <span data-ttu-id="9e439-147">4</span><span class="sxs-lookup"><span data-stu-id="9e439-147">4</span></span>            | <span data-ttu-id="9e439-148">métadonnée</span><span class="sxs-lookup"><span data-stu-id="9e439-148">'data'</span></span>                                                                |
| <span data-ttu-id="9e439-149">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="9e439-149">**DWORD**</span></span>                              | <span data-ttu-id="9e439-150">4</span><span class="sxs-lookup"><span data-stu-id="9e439-150">4</span></span>            | <span data-ttu-id="9e439-151">Taille des données audio.</span><span class="sxs-lookup"><span data-stu-id="9e439-151">Size of the audio data.</span></span>                                               |
| <span data-ttu-id="9e439-152">**POIDS**\[\]</span><span class="sxs-lookup"><span data-stu-id="9e439-152">**BYTE**\[\]</span></span>                           | <span data-ttu-id="9e439-153">Variable</span><span class="sxs-lookup"><span data-stu-id="9e439-153">Varies</span></span>       | <span data-ttu-id="9e439-154">Données audio.</span><span class="sxs-lookup"><span data-stu-id="9e439-154">Audio data.</span></span>                                                           |



 

> [!Note]  
> <span data-ttu-id="9e439-155">Un **FourCC** est une **valeur DWORD** formée par la concaténation de quatre caractères ASCII.</span><span class="sxs-lookup"><span data-stu-id="9e439-155">A **FOURCC** is a **DWORD** formed by concatenating four ASCII characters.</span></span>

 

<span data-ttu-id="9e439-156">Cette structure de base peut être étendue en ajoutant des métadonnées de fichier et d’autres informations, qui n’entrent pas dans le cadre de ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="9e439-156">This basic structure can be extended by adding file metadata and other information, which is beyond the scope of this tutorial.</span></span>

## <a name="header-and-library-files"></a><span data-ttu-id="9e439-157">Fichiers d’en-tête et de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9e439-157">Header and Library Files</span></span>

<span data-ttu-id="9e439-158">Incluez les fichiers d’en-tête suivants dans votre projet :</span><span class="sxs-lookup"><span data-stu-id="9e439-158">Include the following header files in your project:</span></span>


```C++
#define WINVER _WIN32_WINNT_WIN7

#include <windows.h>
#include <mfapi.h>
#include <mfidl.h>
#include <mfreadwrite.h>
#include <stdio.h>
#include <mferror.h>
```



<span data-ttu-id="9e439-159">Lien vers les bibliothèques suivantes :</span><span class="sxs-lookup"><span data-stu-id="9e439-159">Link to the following libraries:</span></span>

-   <span data-ttu-id="9e439-160">mfplat. lib</span><span class="sxs-lookup"><span data-stu-id="9e439-160">mfplat.lib</span></span>
-   <span data-ttu-id="9e439-161">mfreadwrite. lib</span><span class="sxs-lookup"><span data-stu-id="9e439-161">mfreadwrite.lib</span></span>
-   <span data-ttu-id="9e439-162">mfuuid. lib</span><span class="sxs-lookup"><span data-stu-id="9e439-162">mfuuid.lib</span></span>

## <a name="implement-wmain"></a><span data-ttu-id="9e439-163">Implémenter wmain</span><span class="sxs-lookup"><span data-stu-id="9e439-163">Implement wmain</span></span>

<span data-ttu-id="9e439-164">Le code suivant illustre la fonction de point d’entrée pour l’application.</span><span class="sxs-lookup"><span data-stu-id="9e439-164">The following code shows the entry-point function for the application.</span></span>


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



<span data-ttu-id="9e439-165">Cette fonction effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="9e439-165">This function does the following:</span></span>

1.  <span data-ttu-id="9e439-166">Appelle [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) pour initialiser la bibliothèque com.</span><span class="sxs-lookup"><span data-stu-id="9e439-166">Calls [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) to initialize the COM library.</span></span>
2.  <span data-ttu-id="9e439-167">Appelle [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) pour initialiser la plateforme Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="9e439-167">Calls [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) to initialize the Media Foundation platform.</span></span>
3.  <span data-ttu-id="9e439-168">Appelle [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl) pour créer le lecteur source.</span><span class="sxs-lookup"><span data-stu-id="9e439-168">Calls [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl) to create the source reader.</span></span> <span data-ttu-id="9e439-169">Cette fonction prend le nom du fichier d’entrée et reçoit un pointeur d’interface [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) .</span><span class="sxs-lookup"><span data-stu-id="9e439-169">This function takes the name of the input file and receives an [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) interface pointer.</span></span>
4.  <span data-ttu-id="9e439-170">Crée le fichier de sortie en appelant la fonction **CreateFile** , qui retourne un handle de fichier.</span><span class="sxs-lookup"><span data-stu-id="9e439-170">Creates the output file by calling the **CreateFile** function, which returns a file handle.</span></span>
5.  <span data-ttu-id="9e439-171">Appelle la fonction [WriteWavFile](#write-the-wave-file) définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="9e439-171">Calls the application-defined [WriteWavFile](#write-the-wave-file) function.</span></span> <span data-ttu-id="9e439-172">Cette fonction décode l’audio et écrit le fichier WAVE.</span><span class="sxs-lookup"><span data-stu-id="9e439-172">This function decodes the audio and writes the WAVE file.</span></span>
6.  <span data-ttu-id="9e439-173">Libère le pointeur [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) et le handle de fichier.</span><span class="sxs-lookup"><span data-stu-id="9e439-173">Releases the [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) pointer and the file handle.</span></span>
7.  <span data-ttu-id="9e439-174">Appelle [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) pour arrêter la plateforme Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="9e439-174">Calls [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) to shut down the Media Foundation platform.</span></span>
8.  <span data-ttu-id="9e439-175">Appelle [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) pour libérer la bibliothèque com.</span><span class="sxs-lookup"><span data-stu-id="9e439-175">Calls [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) to release the COM library.</span></span>

## <a name="write-the-wave-file"></a><span data-ttu-id="9e439-176">Écrire le fichier WAVE</span><span class="sxs-lookup"><span data-stu-id="9e439-176">Write the WAVE File</span></span>

<span data-ttu-id="9e439-177">La majeure partie du travail se produit dans la `WriteWavFile` fonction, qui est appelée à partir de `wmain` .</span><span class="sxs-lookup"><span data-stu-id="9e439-177">Most of the work happens in the `WriteWavFile` function, which is called from `wmain`.</span></span>


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



<span data-ttu-id="9e439-178">Cette fonction appelle une série d’autres fonctions définies par l’application :</span><span class="sxs-lookup"><span data-stu-id="9e439-178">This function calls a series of other application-defined functions:</span></span>

1.  <span data-ttu-id="9e439-179">La fonction [ConfigureAudioStream](#configure-the-source-reader) Initialise le lecteur source.</span><span class="sxs-lookup"><span data-stu-id="9e439-179">The [ConfigureAudioStream](#configure-the-source-reader) function initializes the source reader.</span></span> <span data-ttu-id="9e439-180">Cette fonction reçoit un pointeur vers l’interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , qui est utilisée pour obtenir une description du format audio décodé, y compris le taux d’échantillonnage, le nombre de canaux et la profondeur de bit (bits par échantillon).</span><span class="sxs-lookup"><span data-stu-id="9e439-180">This function receives a pointer to the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface, which is used to get a description of the decoded audio format, including sample rate, number of channels, and bit depth (bits per sample).</span></span>
2.  <span data-ttu-id="9e439-181">La fonction WriteWaveHeader écrit la première partie du fichier WAVE, y compris l’en-tête et le début du segment « Data ».</span><span class="sxs-lookup"><span data-stu-id="9e439-181">The WriteWaveHeader function writes the first part of the WAVE file, including the header and the start of the 'data' chunk.</span></span>
3.  <span data-ttu-id="9e439-182">La fonction CalculateMaxAudioDataSize calcule la quantité maximale de données audio à écrire dans le fichier, en octets.</span><span class="sxs-lookup"><span data-stu-id="9e439-182">The CalculateMaxAudioDataSize function calculates the maximum amount of audio to write to the file, in bytes.</span></span>
4.  <span data-ttu-id="9e439-183">La fonction WriteWaveData écrit les données audio PCM dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="9e439-183">The WriteWaveData function writes the PCM audio data to the file.</span></span>
5.  <span data-ttu-id="9e439-184">La fonction FixUpChunkSizes écrit les informations de taille de fichier qui apparaissent après les valeurs **FourCC** « Riff » et « Data » dans le fichier wave.</span><span class="sxs-lookup"><span data-stu-id="9e439-184">The FixUpChunkSizes function writes the file-size information that appears after the 'RIFF' and 'data' **FOURCC** values in the WAVE file.</span></span> <span data-ttu-id="9e439-185">(Ces valeurs ne sont pas connues jusqu’à la `WriteWaveData` fin.)</span><span class="sxs-lookup"><span data-stu-id="9e439-185">(These values are not known until `WriteWaveData` completes.)</span></span>

<span data-ttu-id="9e439-186">Ces fonctions sont présentées dans les sections restantes de ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="9e439-186">These functions are shown in the remaining sections of this tutorial.</span></span>

## <a name="configure-the-source-reader"></a><span data-ttu-id="9e439-187">Configurer le lecteur source</span><span class="sxs-lookup"><span data-stu-id="9e439-187">Configure the Source Reader</span></span>

<span data-ttu-id="9e439-188">La `ConfigureAudioStream` fonction configure le lecteur source pour décoder le flux audio dans le fichier source.</span><span class="sxs-lookup"><span data-stu-id="9e439-188">The `ConfigureAudioStream` function configures the source reader to decode the audio stream in the source file.</span></span> <span data-ttu-id="9e439-189">Elle retourne également des informations sur le format de l’audio décodé.</span><span class="sxs-lookup"><span data-stu-id="9e439-189">It also returns information about the format of the decoded audio.</span></span>

<span data-ttu-id="9e439-190">Dans Media Foundation, les formats multimédias sont décrits à l’aide d’objets de *type de média* .</span><span class="sxs-lookup"><span data-stu-id="9e439-190">In Media Foundation, media formats are described using *media type* objects.</span></span> <span data-ttu-id="9e439-191">Un objet de type de média expose l’interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , qui hérite de l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="9e439-191">A media type object exposes the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface, which inherits the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="9e439-192">Fondamentalement, un type de média est une collection de propriétés qui décrivent le format.</span><span class="sxs-lookup"><span data-stu-id="9e439-192">Essentially, a media type is a collection of properties that describe the format.</span></span> <span data-ttu-id="9e439-193">Pour plus d’informations, consultez [types de médias](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="9e439-193">For more information, see [Media Types](media-types.md).</span></span>


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



<span data-ttu-id="9e439-194">La `ConfigureAudioStream` fonction effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="9e439-194">The `ConfigureAudioStream` function does the following:</span></span>

1.  <span data-ttu-id="9e439-195">Appelle la méthode [**IMFSourceReader :: SetStreamSelection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) pour sélectionner le flux audio et désélectionner tous les autres flux.</span><span class="sxs-lookup"><span data-stu-id="9e439-195">Calls the [**IMFSourceReader::SetStreamSelection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) method to select the audio stream and deselect all other streams.</span></span> <span data-ttu-id="9e439-196">Cette étape peut améliorer les performances, car elle empêche le lecteur source de tenir sur des trames vidéo que l’application n’utilise pas.</span><span class="sxs-lookup"><span data-stu-id="9e439-196">This step can improve performance, because it prevents the source reader from holding onto video frames that the application does not use.</span></span>
2.  <span data-ttu-id="9e439-197">Crée un type de média *partiel* qui spécifie l’audio PCM.</span><span class="sxs-lookup"><span data-stu-id="9e439-197">Creates a *partial* media type that specifies PCM audio.</span></span> <span data-ttu-id="9e439-198">La fonction crée le type partiel comme suit :</span><span class="sxs-lookup"><span data-stu-id="9e439-198">The function creates the partial type as follows:</span></span>
    1.  <span data-ttu-id="9e439-199">Appelle [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) pour créer un objet de type de média vide.</span><span class="sxs-lookup"><span data-stu-id="9e439-199">Calls [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) to create an empty media type object.</span></span>
    2.  <span data-ttu-id="9e439-200">Affecte à l’attribut de [**\_ \_ \_ type principal MF MT**](mf-mt-major-type-attribute.md) la valeur **\_ audio MFMediaType**.</span><span class="sxs-lookup"><span data-stu-id="9e439-200">Sets the [**MF\_MT\_MAJOR\_TYPE**](mf-mt-major-type-attribute.md) attribute to **MFMediaType\_Audio**.</span></span>
    3.  <span data-ttu-id="9e439-201">Définit l’attribut de [**\_ sous- \_ type MF MT**](mf-mt-subtype-attribute.md) sur **MFAudioFormat \_ PCM**.</span><span class="sxs-lookup"><span data-stu-id="9e439-201">Sets the [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md) attribute to **MFAudioFormat\_PCM**.</span></span>
3.  <span data-ttu-id="9e439-202">Appelle [**IMFSourceReader :: SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) pour définir le type partiel sur le lecteur source.</span><span class="sxs-lookup"><span data-stu-id="9e439-202">Calls [**IMFSourceReader::SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) to set the partial type on the source reader.</span></span> <span data-ttu-id="9e439-203">Si le fichier source contient des données audio encodées, le lecteur source charge automatiquement le décodeur audio nécessaire.</span><span class="sxs-lookup"><span data-stu-id="9e439-203">If the source file contains encoded audio, the source reader automatically loads the necessary audio decoder.</span></span>
4.  <span data-ttu-id="9e439-204">Appelle [**IMFSourceReader :: GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) pour récupérer le type de média PCM réel.</span><span class="sxs-lookup"><span data-stu-id="9e439-204">Calls [**IMFSourceReader::GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) to get the actual PCM media type.</span></span> <span data-ttu-id="9e439-205">Cette méthode retourne un type de média avec tous les détails de format renseignés, tels que le taux d’échantillonnage audio et le nombre de canaux.</span><span class="sxs-lookup"><span data-stu-id="9e439-205">This method returns a media type with all of the format details filled in, such as the audio sample rate and the number of channels.</span></span>
5.  <span data-ttu-id="9e439-206">Appelle [**IMFSourceReader :: SetStreamSelection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) pour activer le flux audio.</span><span class="sxs-lookup"><span data-stu-id="9e439-206">Calls [**IMFSourceReader::SetStreamSelection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) to enable the audio stream.</span></span>

## <a name="write-the-wave-file-header"></a><span data-ttu-id="9e439-207">Écrire l’en-tête de fichier WAVE</span><span class="sxs-lookup"><span data-stu-id="9e439-207">Write the WAVE File Header</span></span>

<span data-ttu-id="9e439-208">La `WriteWaveHeader` fonction écrit l’en-tête de fichier wave.</span><span class="sxs-lookup"><span data-stu-id="9e439-208">The `WriteWaveHeader` function writes the WAVE file header.</span></span>

<span data-ttu-id="9e439-209">La seule API Media Foundation appelée à partir de cette fonction est [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype), qui convertit le type de média en structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9e439-209">The only Media Foundation API called from this function is [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype), which converts the media type to a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>


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



<span data-ttu-id="9e439-210">La `WriteToFile` fonction est une fonction d’assistance simple qui encapsule la fonction **WriteFile** Windows et retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9e439-210">The `WriteToFile` function is a simple helper function that wraps the Windows **WriteFile** function and returns an **HRESULT** value.</span></span>


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



## <a name="calculate-the-maximum-data-size"></a><span data-ttu-id="9e439-211">Calculer la taille de données maximale</span><span class="sxs-lookup"><span data-stu-id="9e439-211">Calculate the Maximum Data Size</span></span>

<span data-ttu-id="9e439-212">Étant donné que la taille du fichier est stockée sous la forme d’une valeur de 4 octets dans l’en-tête de fichier, un fichier WAVE est limité à une taille maximale de 0xFFFFFFFF octets, soit environ 4 Go.</span><span class="sxs-lookup"><span data-stu-id="9e439-212">Because the file size is stored as a 4-byte value in the file header, a WAVE file is limited to a maximum size of 0xFFFFFFFF bytes—approximately 4 GB.</span></span> <span data-ttu-id="9e439-213">Cette valeur comprend la taille de l’en-tête de fichier.</span><span class="sxs-lookup"><span data-stu-id="9e439-213">This value includes the size of the file header.</span></span> <span data-ttu-id="9e439-214">Le format audio PCM a une vitesse binaire constante, ce qui vous permet de calculer la taille maximale des données à partir du format audio, comme suit :</span><span class="sxs-lookup"><span data-stu-id="9e439-214">PCM audio has a constant bit rate, so you can calculate the maximum data size from the audio format, as follows:</span></span>


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



<span data-ttu-id="9e439-215">Pour éviter les images audio partielles, la taille est arrondie à l’alignement de bloc, qui est stocké dans l’attribut d' [**\_ \_ \_ \_ alignement de bloc audio MF MT**](mf-mt-audio-block-alignment-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="9e439-215">To avoid partial audio frames, the size is rounded to the block alignment, which is stored in the [**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**](mf-mt-audio-block-alignment-attribute.md) attribute.</span></span>

## <a name="decode-the-audio"></a><span data-ttu-id="9e439-216">Décoder l’audio</span><span class="sxs-lookup"><span data-stu-id="9e439-216">Decode the Audio</span></span>

<span data-ttu-id="9e439-217">La `WriteWaveData` fonction lit les données audio décodées à partir du fichier source et les écrit dans le fichier wave.</span><span class="sxs-lookup"><span data-stu-id="9e439-217">The `WriteWaveData` function reads decoded audio from the source file and writes to the WAVE file.</span></span>


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



<span data-ttu-id="9e439-218">La `WriteWaveData` fonction effectue les opérations suivantes dans une boucle :</span><span class="sxs-lookup"><span data-stu-id="9e439-218">The `WriteWaveData` function does the following in a loop:</span></span>

1.  <span data-ttu-id="9e439-219">Appelle [**IMFSourceReader :: ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) pour lire l’audio à partir du fichier source.</span><span class="sxs-lookup"><span data-stu-id="9e439-219">Calls [**IMFSourceReader::ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) to read audio from the source file.</span></span> <span data-ttu-id="9e439-220">Le paramètre *dwFlags* reçoit un or **au niveau du** bit des indicateurs de l’énumération de l' [**\_ \_ \_ indicateur de lecteur source MF**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag) .</span><span class="sxs-lookup"><span data-stu-id="9e439-220">The *dwFlags* parameter receives a bitwise **OR** of flags from the [**MF\_SOURCE\_READER\_FLAG**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag) enumeration.</span></span> <span data-ttu-id="9e439-221">Le paramètre *pSample* reçoit un pointeur vers l’interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , qui est utilisée pour accéder aux données audio.</span><span class="sxs-lookup"><span data-stu-id="9e439-221">The *pSample* parameter receives a pointer to the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, which is used to access the audio data.</span></span> <span data-ttu-id="9e439-222">Dans certains cas, un appel à **ReadSample** ne génère pas de données, auquel cas le pointeur **IMFSample** est **null**.</span><span class="sxs-lookup"><span data-stu-id="9e439-222">In some cases a call to **ReadSample** does not generate data, in which case the **IMFSample** pointer is **NULL**.</span></span>
2.  <span data-ttu-id="9e439-223">Recherche les indicateurs suivants dans *dwFlags* :</span><span class="sxs-lookup"><span data-stu-id="9e439-223">Checks *dwFlags* for the following flags:</span></span>
    -   <span data-ttu-id="9e439-224">**MF \_ SOURCE \_ READERF \_ CURRENTMEDIATYPECHANGED**.</span><span class="sxs-lookup"><span data-stu-id="9e439-224">**MF\_SOURCE\_READERF\_CURRENTMEDIATYPECHANGED**.</span></span> <span data-ttu-id="9e439-225">Cet indicateur indique une modification de format dans le fichier source.</span><span class="sxs-lookup"><span data-stu-id="9e439-225">This flag indicates a format change in the source file.</span></span> <span data-ttu-id="9e439-226">Les fichiers WAVE ne prennent pas en charge les modifications de format.</span><span class="sxs-lookup"><span data-stu-id="9e439-226">WAVE files do not support format changes.</span></span>
    -   <span data-ttu-id="9e439-227">**MF \_ SOURCE \_ READERF \_ ENDOFSTREAM**.</span><span class="sxs-lookup"><span data-stu-id="9e439-227">**MF\_SOURCE\_READERF\_ENDOFSTREAM**.</span></span> <span data-ttu-id="9e439-228">Cet indicateur indique la fin du flux.</span><span class="sxs-lookup"><span data-stu-id="9e439-228">This flag indicates the end of the stream.</span></span>
3.  <span data-ttu-id="9e439-229">Appelle [**IMFSample :: ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer) pour obtenir un pointeur vers un objet de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="9e439-229">Calls [**IMFSample::ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer) to get a pointer to a buffer object.</span></span>
4.  <span data-ttu-id="9e439-230">Appelle [**IMFMediaBuffer :: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) pour obtenir un pointeur vers la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="9e439-230">Calls [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to get a pointer to the buffer memory.</span></span>
5.  <span data-ttu-id="9e439-231">Écrit les données audio dans le fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="9e439-231">Writes the audio data to the output file.</span></span>
6.  <span data-ttu-id="9e439-232">Appelle [**IMFMediaBuffer :: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) pour déverrouiller l’objet de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="9e439-232">Calls [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) to unlock the buffer object.</span></span>

<span data-ttu-id="9e439-233">La fonction s’arrête hors de la boucle lorsque l’un des éléments suivants se produit :</span><span class="sxs-lookup"><span data-stu-id="9e439-233">The function breaks out of the loop when any of the following occur:</span></span>

-   <span data-ttu-id="9e439-234">Le format de flux change.</span><span class="sxs-lookup"><span data-stu-id="9e439-234">The stream format changes.</span></span>
-   <span data-ttu-id="9e439-235">La fin du flux est atteinte.</span><span class="sxs-lookup"><span data-stu-id="9e439-235">The end of the stream is reached.</span></span>
-   <span data-ttu-id="9e439-236">La quantité maximale de données audio est écrite dans le fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="9e439-236">The maximum amount of audio data is written to the output file.</span></span>
-   <span data-ttu-id="9e439-237">Une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="9e439-237">An error occurs.</span></span>

## <a name="finalize-the-file-header"></a><span data-ttu-id="9e439-238">Finaliser l’en-tête de fichier</span><span class="sxs-lookup"><span data-stu-id="9e439-238">Finalize the File Header</span></span>

<span data-ttu-id="9e439-239">Les valeurs de taille stockées dans l’en-tête WAVE ne sont pas connues jusqu’à la fin de la fonction précédente.</span><span class="sxs-lookup"><span data-stu-id="9e439-239">The size values that are stored in the WAVE header are not known until the previous function completes.</span></span> <span data-ttu-id="9e439-240">Le `FixUpChunkSizes` remplit ces valeurs :</span><span class="sxs-lookup"><span data-stu-id="9e439-240">The `FixUpChunkSizes` fills in these values:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="9e439-241">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9e439-241">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e439-242">Types de média audio</span><span class="sxs-lookup"><span data-stu-id="9e439-242">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="9e439-243">Lecteur source</span><span class="sxs-lookup"><span data-stu-id="9e439-243">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="9e439-244">**IMFSourceReader**</span><span class="sxs-lookup"><span data-stu-id="9e439-244">**IMFSourceReader**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 
