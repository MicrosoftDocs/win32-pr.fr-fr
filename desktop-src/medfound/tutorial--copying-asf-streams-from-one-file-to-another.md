---
description: Une façon de créer un fichier ASF consiste à copier des flux ASF à partir d’un fichier existant.
ms.assetid: 158fe3a1-42e6-461d-b56b-5419cd961fca
title: 'Didacticiel : copie de flux ASF à l’aide d’objets WMContainer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44bac13626a8c80f474eeb029db4eb1351273910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518621"
---
# <a name="tutorial-copying-asf-streams-by-using-wmcontainer-objects"></a><span data-ttu-id="4820d-103">Didacticiel : copie de flux ASF à l’aide d’objets WMContainer</span><span class="sxs-lookup"><span data-stu-id="4820d-103">Tutorial: Copying ASF Streams by Using WMContainer Objects</span></span>

<span data-ttu-id="4820d-104">Une façon de créer un fichier ASF consiste à copier des flux ASF à partir d’un fichier existant.</span><span class="sxs-lookup"><span data-stu-id="4820d-104">One way to create an ASF file is to copy ASF streams from an existing file.</span></span> <span data-ttu-id="4820d-105">Pour ce faire, vous pouvez récupérer les données du média à partir du fichier source et écrire dans le fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="4820d-105">To do this, you can retrieve the media data from the source file and write to the output file.</span></span> <span data-ttu-id="4820d-106">Si le fichier source est un fichier ASF, vous pouvez copier des exemples de flux sans les décompresser et les recompresser.</span><span class="sxs-lookup"><span data-stu-id="4820d-106">If the source file is an ASF file, you can copy stream samples without decompressing and recompressing them.</span></span>

<span data-ttu-id="4820d-107">Ce didacticiel présente ce scénario en extrayant le premier flux audio d’un fichier vidéo audio ASF (. wmv) et en le copiant dans un nouveau fichier audio ASF (. WMA).</span><span class="sxs-lookup"><span data-stu-id="4820d-107">This tutorial demonstrates this scenario by extracting the first audio stream from an ASF audio-video file (.wmv) and copying it to a new ASF audio file (.wma).</span></span> <span data-ttu-id="4820d-108">Dans ce didacticiel, vous allez créer une application console qui accepte les noms de fichiers d’entrée et de sortie comme arguments.</span><span class="sxs-lookup"><span data-stu-id="4820d-108">In this tutorial, you will create a console application that takes the input and output filenames as arguments.</span></span> <span data-ttu-id="4820d-109">L’application utilise le séparateur ASF pour analyser les exemples de flux d’entrée, puis les envoie au multiplexeur ASF pour écrire les paquets de données ASF pour le flux audio.</span><span class="sxs-lookup"><span data-stu-id="4820d-109">The application uses the ASF Splitter to parse the input stream samples and then sends them to the ASF Multiplexer to write the ASF data packets for the audio stream.</span></span>

<span data-ttu-id="4820d-110">Ce didacticiel comprend les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="4820d-110">This tutorial contains the following steps:</span></span>

-   [<span data-ttu-id="4820d-111">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="4820d-111">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="4820d-112">Terminologie</span><span class="sxs-lookup"><span data-stu-id="4820d-112">Terminology</span></span>](#terminology)
-   [<span data-ttu-id="4820d-113">1. configurer le projet</span><span class="sxs-lookup"><span data-stu-id="4820d-113">1. Set up the Project</span></span>](#1-set-up-the-project)
-   [<span data-ttu-id="4820d-114">2. déclarer des fonctions d’assistance</span><span class="sxs-lookup"><span data-stu-id="4820d-114">2. Declare Helper Functions</span></span>](#2-declare-helper-functions)
-   [<span data-ttu-id="4820d-115">3. Ouvrez le fichier ASF d’entrée</span><span class="sxs-lookup"><span data-stu-id="4820d-115">3. Open the Input ASF File</span></span>](#3-open-the-input-asf-file)
-   [<span data-ttu-id="4820d-116">4. initialiser des objets pour le fichier d’entrée</span><span class="sxs-lookup"><span data-stu-id="4820d-116">4. Initialize Objects for the Input File</span></span>](#4-initialize-objects-for-the-input-file)
-   [<span data-ttu-id="4820d-117">5. créer un profil audio</span><span class="sxs-lookup"><span data-stu-id="4820d-117">5. Create an Audio Profile</span></span>](#5-create-an-audio-profile)
-   [<span data-ttu-id="4820d-118">6. initialiser des objets pour le fichier de sortie</span><span class="sxs-lookup"><span data-stu-id="4820d-118">6. Initialize Objects for the Output File</span></span>](#6-initialize-objects-for-the-output-file)
-   [<span data-ttu-id="4820d-119">7. générer de nouveaux paquets de données ASF</span><span class="sxs-lookup"><span data-stu-id="4820d-119">7. Generate New ASF Data Packets</span></span>](#7-generate-new-asf-data-packets)
-   [<span data-ttu-id="4820d-120">8. écrire les objets ASF dans le nouveau fichier</span><span class="sxs-lookup"><span data-stu-id="4820d-120">8. Write the ASF Objects in the New File</span></span>](#8-write-the-asf-objects-in-the-new-file)
-   [<span data-ttu-id="4820d-121">9 écrire la fonction Entry-Point</span><span class="sxs-lookup"><span data-stu-id="4820d-121">9 Write the Entry-Point Function</span></span>](#9-write-the-entry-point-function)
-   [<span data-ttu-id="4820d-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4820d-122">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="4820d-123">Prérequis</span><span class="sxs-lookup"><span data-stu-id="4820d-123">Prerequisites</span></span>

<span data-ttu-id="4820d-124">Ce didacticiel part des principes suivants :</span><span class="sxs-lookup"><span data-stu-id="4820d-124">This tutorial assumes the following:</span></span>

-   <span data-ttu-id="4820d-125">Vous êtes familiarisé avec la structure d’un fichier ASF et les composants fournis par Media Foundation pour travailler avec des objets ASF.</span><span class="sxs-lookup"><span data-stu-id="4820d-125">You are familiar with the structure of an ASF file and the components provided by Media Foundation to work with ASF Objects.</span></span> <span data-ttu-id="4820d-126">Ces composants incluent les objets ContentInfo, Splitter, multiplexer et Profile.</span><span class="sxs-lookup"><span data-stu-id="4820d-126">These components include ContentInfo, splitter, multiplexer, and profile objects.</span></span> <span data-ttu-id="4820d-127">Pour plus d’informations, consultez [WMCONTAINER ASF Components](wmcontainer-asf-components.md).</span><span class="sxs-lookup"><span data-stu-id="4820d-127">For more information, see [WMContainer ASF Components](wmcontainer-asf-components.md).</span></span>
-   <span data-ttu-id="4820d-128">Vous êtes familiarisé avec le processus d’analyse de l’objet d’en-tête ASF et des paquets de données ASF d’un fichier existant et de génération d’exemples de flux compressés à l’aide du séparateur.</span><span class="sxs-lookup"><span data-stu-id="4820d-128">You are familiar with the process of parsing the ASF Header Object and the ASF data packets of an existing file and generating compressed stream samples by using the splitter.</span></span> <span data-ttu-id="4820d-129">Pour plus d’informations, consultez [Didacticiel : lecture d’un fichier ASF](tutorial--reading-an-asf-file.md).</span><span class="sxs-lookup"><span data-stu-id="4820d-129">For more information see [Tutorial: Reading an ASF File](tutorial--reading-an-asf-file.md).</span></span>
-   <span data-ttu-id="4820d-130">Vous êtes familiarisé avec les mémoires tampons de média et les flux d’octets : en particulier, les opérations de fichier utilisant un flux d’octets et l’écriture du contenu d’une mémoire tampon de média dans un flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="4820d-130">You are familiar with media buffers and byte streams: Specifically, file operations using a byte stream, and writing the contents of a media buffer into a byte stream.</span></span> <span data-ttu-id="4820d-131">(Voir [2. Déclarer des fonctions d’assistance](#2-declare-helper-functions).)</span><span class="sxs-lookup"><span data-stu-id="4820d-131">(See [2. Declare Helper Functions](#2-declare-helper-functions).)</span></span>

## <a name="terminology"></a><span data-ttu-id="4820d-132">Terminologie</span><span class="sxs-lookup"><span data-stu-id="4820d-132">Terminology</span></span>

<span data-ttu-id="4820d-133">Ce didacticiel utilise les termes suivants :</span><span class="sxs-lookup"><span data-stu-id="4820d-133">This tutorial uses the following terms:</span></span>

-   <span data-ttu-id="4820d-134">Source d’octet source : objet de flux d’octets, expose l’interface [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , qui contient le contenu du fichier d’entrée.</span><span class="sxs-lookup"><span data-stu-id="4820d-134">Source byte stream: Byte stream object, exposes [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface, which contains the contents of the input file.</span></span>
-   <span data-ttu-id="4820d-135">Objet ContentInfo source : objet ContentInfo, qui expose l’interface [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) , qui représente l’objet d’en-tête ASF du fichier d’entrée.</span><span class="sxs-lookup"><span data-stu-id="4820d-135">Source ContentInfo object: ContentInfo object, exposes [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface, which represents the ASF Header Object of the input file.</span></span>
-   <span data-ttu-id="4820d-136">Profil audio : objet de profil, expose l’interface [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) , qui contient uniquement les flux audio du fichier d’entrée.</span><span class="sxs-lookup"><span data-stu-id="4820d-136">Audio profile: Profile object, exposes [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface, which contains only audio streams of the input file.</span></span>
-   <span data-ttu-id="4820d-137">Exemple de flux : Sample Media, expose l’interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , générée par le séparateur, représente les données multimédia du flux sélectionné obtenues à partir du fichier d’entrée dans un État compressé.</span><span class="sxs-lookup"><span data-stu-id="4820d-137">Stream sample: Media sample, exposes [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, generated by the splitter represents the selected stream's media data obtained from the input file in compressed state.</span></span>
-   <span data-ttu-id="4820d-138">Objet de sortie ContentInfo : objet ContentInfo, qui expose l’interface [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) , qui représente l’objet d’en-tête ASF du fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="4820d-138">Output ContentInfo object: ContentInfo object, exposes [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface, which represents the ASF Header Object of the output file.</span></span>
-   <span data-ttu-id="4820d-139">Flux d’octets de données : objet de flux d’octets, expose l’interface [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , qui représente la partie entière de l’objet de données ASF du fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="4820d-139">Data byte stream: Byte stream object, exposes [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface, which represents the entire ASF Data Object portion of the output file.</span></span>
-   <span data-ttu-id="4820d-140">Paquet de données : l’exemple de support, expose l’interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , généré par le multiplexeur représente un paquet de données ASF qui sera écrit dans le flux d’octets de données.</span><span class="sxs-lookup"><span data-stu-id="4820d-140">Data packet: Media sample, exposes [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, generated by the multiplexer represents an ASF data packet that will be written to the data byte stream.</span></span>
-   <span data-ttu-id="4820d-141">Sortie d’octet de sortie : objet de flux d’octets, expose l’interface [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , qui contient le contenu du fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="4820d-141">Output byte stream: Byte stream object, exposes [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface, which contains the contents of the output file.</span></span>

## <a name="1-set-up-the-project"></a><span data-ttu-id="4820d-142">1. configurer le projet</span><span class="sxs-lookup"><span data-stu-id="4820d-142">1. Set up the Project</span></span>

<span data-ttu-id="4820d-143">Incluez les en-têtes suivants dans votre fichier source :</span><span class="sxs-lookup"><span data-stu-id="4820d-143">Include the following headers in your source file:</span></span>


```C++
#include <stdio.h>       // Standard I/O
#include <windows.h>     // Windows headers
#include <mfapi.h>       // Media Foundation platform
#include <wmcontainer.h> // ASF interfaces
#include <mferror.h>     // Media Foundation error codes
```



<span data-ttu-id="4820d-144">Lien vers les fichiers de bibliothèque suivants :</span><span class="sxs-lookup"><span data-stu-id="4820d-144">Link to the following library files:</span></span>

-   <span data-ttu-id="4820d-145">mfplat. lib</span><span class="sxs-lookup"><span data-stu-id="4820d-145">mfplat.lib</span></span>
-   <span data-ttu-id="4820d-146">MF. lib</span><span class="sxs-lookup"><span data-stu-id="4820d-146">mf.lib</span></span>
-   <span data-ttu-id="4820d-147">mfuuid. lib</span><span class="sxs-lookup"><span data-stu-id="4820d-147">mfuuid.lib</span></span>

<span data-ttu-id="4820d-148">Déclarez la fonction [SafeRelease](saferelease.md) :</span><span class="sxs-lookup"><span data-stu-id="4820d-148">Declare the [SafeRelease](saferelease.md) function:</span></span>


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



## <a name="2-declare-helper-functions"></a><span data-ttu-id="4820d-149">2. déclarer des fonctions d’assistance</span><span class="sxs-lookup"><span data-stu-id="4820d-149">2. Declare Helper Functions</span></span>

<span data-ttu-id="4820d-150">Ce didacticiel utilise les fonctions d’assistance suivantes pour lire et écrire à partir d’un flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="4820d-150">This tutorial uses the following helper functions to read and write from a byte stream.</span></span>

<span data-ttu-id="4820d-151">La `AllocReadFromByteStream` fonction lit les données à partir d’un flux d’octets et alloue une nouvelle mémoire tampon de média pour contenir les données.</span><span class="sxs-lookup"><span data-stu-id="4820d-151">The `AllocReadFromByteStream` function reads data from a byte stream and allocates a new media buffer to hold the data.</span></span> <span data-ttu-id="4820d-152">Pour plus d’informations, consultez [**IMFByteStream :: Read**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-read).</span><span class="sxs-lookup"><span data-stu-id="4820d-152">For more information, see [**IMFByteStream::Read**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-read).</span></span>


```C++
//-------------------------------------------------------------------
// AllocReadFromByteStream
//
// Reads data from a byte stream and returns a media buffer that
// contains the data.
//-------------------------------------------------------------------

HRESULT AllocReadFromByteStream(
    IMFByteStream *pStream,         // Pointer to the byte stream.
    DWORD cbToRead,                 // Number of bytes to read.
    IMFMediaBuffer **ppBuffer       // Receives a pointer to the media buffer. 
    )
{
    HRESULT hr = S_OK;
    BYTE *pData = NULL;
    DWORD cbRead = 0;   // Actual amount of data read.

    IMFMediaBuffer *pBuffer = NULL;

    // Create the media buffer. 
    // This function allocates the memory for the buffer.
    hr = MFCreateMemoryBuffer(cbToRead, &pBuffer);

    // Get a pointer to the memory buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }

    // Read the data from the byte stream.
    if (SUCCEEDED(hr))
    {
        hr = pStream->Read(pData, cbToRead, &cbRead);
    }

    // Update the size of the valid data in the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbRead);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppBuffer = pBuffer;
        (*ppBuffer)->AddRef();
    }

    if (pData)
    {
        pBuffer->Unlock();
    }
    SafeRelease(&pBuffer);
    return hr;
}
```



<span data-ttu-id="4820d-153">La `WriteBufferToByteStream` fonction écrit des données à partir d’une mémoire tampon de média dans un flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="4820d-153">The `WriteBufferToByteStream` function writes data from a media buffer to a byte stream.</span></span> <span data-ttu-id="4820d-154">Pour plus d’informations, consultez [**IMFByteStream :: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span><span class="sxs-lookup"><span data-stu-id="4820d-154">For more information, see [**IMFByteStream::Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span></span>


```C++
//-------------------------------------------------------------------
// WriteBufferToByteStream
//
// Writes data from a media buffer to a byte stream.
//-------------------------------------------------------------------

HRESULT WriteBufferToByteStream(
    IMFByteStream *pStream,   // Pointer to the byte stream.
    IMFMediaBuffer *pBuffer,  // Pointer to the media buffer.
    DWORD *pcbWritten         // Receives the number of bytes written.
    )
{
    HRESULT hr = S_OK;
    DWORD cbData = 0;
    DWORD cbWritten = 0;
    BYTE *pMem = NULL;

    hr = pBuffer->Lock(&pMem, NULL, &cbData);

    if (SUCCEEDED(hr))
    {
        hr = pStream->Write(pMem, cbData, &cbWritten);
    }

    if (SUCCEEDED(hr))
    {
        if (pcbWritten)
        {
            *pcbWritten = cbWritten;
        }
    }

    if (pMem)
    {
        pBuffer->Unlock();
    }
    return hr;
}
```



<span data-ttu-id="4820d-155">La `AppendToByteStream` fonction ajoute le contenu d’un flux d’octets à un autre :</span><span class="sxs-lookup"><span data-stu-id="4820d-155">The `AppendToByteStream` function appends the contents of one byte stream to another:</span></span>


```C++
//-------------------------------------------------------------------
// AppendToByteStream
//
// Reads the contents of pSrc and writes them to pDest.
//-------------------------------------------------------------------

HRESULT AppendToByteStream(IMFByteStream *pSrc, IMFByteStream *pDest)
{
    HRESULT hr = S_OK;

    const DWORD READ_SIZE = 1024;

    BYTE buffer[READ_SIZE];

    while (1)
    {
        ULONG cbRead;

        hr = pSrc->Read(buffer, READ_SIZE, &cbRead);

        if (FAILED(hr)) { break; }

        if (cbRead == 0)
        {
            break;
        }

        hr = pDest->Write(buffer, cbRead, &cbRead);

        if (FAILED(hr)) { break; }
    }

    return hr;
}
```



## <a name="3-open-the-input-asf-file"></a><span data-ttu-id="4820d-156">3. Ouvrez le fichier ASF d’entrée</span><span class="sxs-lookup"><span data-stu-id="4820d-156">3. Open the Input ASF File</span></span>

<span data-ttu-id="4820d-157">Ouvrez le fichier d’entrée en appelant la fonction [**MFCreateFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) .</span><span class="sxs-lookup"><span data-stu-id="4820d-157">Open the input file by calling the [**MFCreateFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) function.</span></span> <span data-ttu-id="4820d-158">La méthode retourne un pointeur vers l’objet de flux d’octets qui contient le contenu du fichier.</span><span class="sxs-lookup"><span data-stu-id="4820d-158">The method returns a pointer to the byte stream object that contains the contents of the file.</span></span> <span data-ttu-id="4820d-159">Le nom de fichier est spécifié par l’utilisateur via les arguments de ligne de commande de l’application.</span><span class="sxs-lookup"><span data-stu-id="4820d-159">The filename is specified by the user through command line arguments of the application.</span></span>

<span data-ttu-id="4820d-160">L’exemple de code suivant prend un nom de fichier et retourne un pointeur vers un objet de flux d’octets qui peut être utilisé pour lire le fichier.</span><span class="sxs-lookup"><span data-stu-id="4820d-160">The following example code takes a file name and returns a pointer to a byte stream object that can be used to read the file.</span></span>


```C++
        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);
```



## <a name="4-initialize-objects-for-the-input-file"></a><span data-ttu-id="4820d-161">4. initialiser des objets pour le fichier d’entrée</span><span class="sxs-lookup"><span data-stu-id="4820d-161">4. Initialize Objects for the Input File</span></span>

<span data-ttu-id="4820d-162">Ensuite, vous allez créer et initialiser l’objet de la source ContentInfo et le séparateur pour générer des exemples de flux.</span><span class="sxs-lookup"><span data-stu-id="4820d-162">Next, you will create and initialize the source ContentInfo object and the splitter for generating stream samples.</span></span>

<span data-ttu-id="4820d-163">Ce flux d’octet source créé à l’étape 2 sera utilisé pour analyser l’objet d’en-tête ASF et remplir l’objet de la source ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="4820d-163">This source byte stream created in step 2 will be used to parse the ASF Header Object and populate the source ContentInfo object.</span></span> <span data-ttu-id="4820d-164">Cet objet sera utilisé pour initialiser le séparateur afin de faciliter l’analyse des paquets de données ASF pour le flux audio dans le fichier d’entrée.</span><span class="sxs-lookup"><span data-stu-id="4820d-164">This object will be used to initialize the splitter to facilitate the parsing of the ASF data packets for the audio stream in the input file.</span></span> <span data-ttu-id="4820d-165">Vous allez également récupérer la longueur de l’objet de données ASF dans le fichier d’entrée et le décalage vers le premier paquet de données ASF relatif au début du fichier.</span><span class="sxs-lookup"><span data-stu-id="4820d-165">You will also retrieve the length of the ASF Data Object in the input file and the offset to the first ASF data packet relative to the start of the file.</span></span> <span data-ttu-id="4820d-166">Ces attributs seront utilisés par le séparateur pour générer des exemples de flux audio.</span><span class="sxs-lookup"><span data-stu-id="4820d-166">These attributes will be used by the splitter to generate audio stream samples.</span></span>

<span data-ttu-id="4820d-167">Pour créer et initialiser des composants ASF pour le fichier d’entrée :</span><span class="sxs-lookup"><span data-stu-id="4820d-167">To create and initialize ASF components for the input file:</span></span>

1.  <span data-ttu-id="4820d-168">Appelez [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) pour créer l’objet ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="4820d-168">Call [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) to create the ContentInfo object.</span></span> <span data-ttu-id="4820d-169">Cette fonction retourne un pointeur vers l’interface [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) .</span><span class="sxs-lookup"><span data-stu-id="4820d-169">This function returns a pointer to the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface.</span></span>
2.  <span data-ttu-id="4820d-170">Appelez [**IMFASFContentInfo ::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) pour analyser l’en-tête ASF.</span><span class="sxs-lookup"><span data-stu-id="4820d-170">Call [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) to parse the ASF Header.</span></span> <span data-ttu-id="4820d-171">Pour plus d’informations sur cette étape, consultez [lecture de l’objet d’en-tête ASF d’un fichier existant](reading-the-asf-header-object-of-an-existing-file.md).</span><span class="sxs-lookup"><span data-stu-id="4820d-171">For more information about this step, see [Reading the ASF Header Object of an Existing File](reading-the-asf-header-object-of-an-existing-file.md).</span></span>
3.  <span data-ttu-id="4820d-172">Appelez [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) pour créer l’objet Splitter ASF.</span><span class="sxs-lookup"><span data-stu-id="4820d-172">Call [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) to create the ASF splitter object.</span></span> <span data-ttu-id="4820d-173">Cette fonction retourne un pointeur vers l’interface [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) .</span><span class="sxs-lookup"><span data-stu-id="4820d-173">This function returns a pointer to the [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) interface.</span></span>
4.  <span data-ttu-id="4820d-174">Appelez [**IMFASFSplitter :: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize), en passant le pointeur [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo).</span><span class="sxs-lookup"><span data-stu-id="4820d-174">Call [**IMFASFSplitter::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize), passing in the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)pointer.</span></span> <span data-ttu-id="4820d-175">Pour plus d’informations sur cette étape, consultez [création de l’objet Splitter ASF](creating-the-asf-splitter-object.md).</span><span class="sxs-lookup"><span data-stu-id="4820d-175">For more information about this step, see [Creating the ASF Splitter Object](creating-the-asf-splitter-object.md).</span></span>
5.  <span data-ttu-id="4820d-176">Appelez [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) pour obtenir un descripteur de présentation pour le fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="4820d-176">Call [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) to get a presentation descriptor for the ASF file.</span></span>
6.  <span data-ttu-id="4820d-177">Obtient la valeur de l’attribut de [**\_ décalage de \_ \_ \_ début \_ de données ASF**](mf-pd-asf-data-start-offset-attribute.md) pour la norme MF PD à partir du descripteur de présentation.</span><span class="sxs-lookup"><span data-stu-id="4820d-177">Get the value of the [**MF\_PD\_ASF\_DATA\_START\_OFFSET**](mf-pd-asf-data-start-offset-attribute.md) attribute from the presentation descriptor.</span></span> <span data-ttu-id="4820d-178">Cette valeur correspond à l’emplacement de l’objet de données ASF dans le fichier, sous la forme d’un décalage d’octet par rapport au début du fichier.</span><span class="sxs-lookup"><span data-stu-id="4820d-178">This value is the location of the ASF Data Object in the file, as a byte offset from the start of the file.</span></span>
7.  <span data-ttu-id="4820d-179">Obtient la valeur de l’attribut de [**\_ \_ \_ \_ longueur de données ASF**](mf-pd-asf-data-length-attribute.md) pour la norme MF PD à partir du descripteur de présentation.</span><span class="sxs-lookup"><span data-stu-id="4820d-179">Get the value of the [**MF\_PD\_ASF\_DATA\_LENGTH**](mf-pd-asf-data-length-attribute.md) attribute from the presentation descriptor.</span></span> <span data-ttu-id="4820d-180">Cette valeur correspond à la taille totale de l’objet de données ASF, en octets.</span><span class="sxs-lookup"><span data-stu-id="4820d-180">This value is the total size of the ASF Data Object, in bytes.</span></span> <span data-ttu-id="4820d-181">Pour plus d’informations, consultez [obtention d’informations à partir d’objets d’en-tête ASF](getting-information-from-asf-header-objects.md).</span><span class="sxs-lookup"><span data-stu-id="4820d-181">For more information, see [Getting Information from ASF Header Objects](getting-information-from-asf-header-objects.md).</span></span>

<span data-ttu-id="4820d-182">L’exemple de code suivant montre une fonction qui consolide toutes les étapes.</span><span class="sxs-lookup"><span data-stu-id="4820d-182">The following example code shows a function that consolidates all of the steps.</span></span> <span data-ttu-id="4820d-183">Cette fonction accepte un pointeur vers le flux d’octets source et retourne des pointeurs vers l’objet ContentInfo source et le séparateur.</span><span class="sxs-lookup"><span data-stu-id="4820d-183">This function takes a pointer to the source byte stream and returns pointers to the source ContentInfo object and the splitter.</span></span> <span data-ttu-id="4820d-184">En outre, il reçoit la longueur et les décalages de l’objet de données ASF.</span><span class="sxs-lookup"><span data-stu-id="4820d-184">Also, it receives the length and offsets to the ASF Data Object.</span></span>


```C++
//-------------------------------------------------------------------
// CreateSourceParsers
//
// Creates the ASF splitter and the ASF Content Info object for the 
// source file.
// 
// This function also calulates the offset and length of the ASF 
// Data Object.
//-------------------------------------------------------------------

HRESULT CreateSourceParsers(
    IMFByteStream *pSourceStream,
    IMFASFContentInfo **ppSourceContentInfo,
    IMFASFSplitter **ppSplitter,
    UINT64 *pcbDataOffset,
    UINT64 *pcbDataLength
    )
{
    const DWORD MIN_ASF_HEADER_SIZE = 30;

    IMFMediaBuffer *pBuffer = NULL;
    IMFPresentationDescriptor *pPD = NULL;
    IMFASFContentInfo *pSourceContentInfo = NULL;
    IMFASFSplitter *pSplitter = NULL;

    QWORD cbHeader = 0;

    /*------- Parse the ASF header. -------*/

    // Create the ASF ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pSourceContentInfo);
    
    // Read the first 30 bytes to find the total header size.
    if (SUCCEEDED(hr))
    {
        hr = AllocReadFromByteStream(
            pSourceStream, 
            MIN_ASF_HEADER_SIZE, 
            &pBuffer
            );
    }

    // Get the header size.
    if (SUCCEEDED(hr))
    {
        hr = pSourceContentInfo->GetHeaderSize(pBuffer, &cbHeader);
    }

    // Release the buffer; we will reuse it.
    SafeRelease(&pBuffer);
    
    // Read the entire header into a buffer.
    if (SUCCEEDED(hr))
    {
        hr = pSourceStream->SetCurrentPosition(0);
    }

    if (SUCCEEDED(hr))
    {
        hr = AllocReadFromByteStream(
            pSourceStream, 
            (DWORD)cbHeader, 
            &pBuffer
            );
    }

    // Parse the buffer and populate the header object.
    if (SUCCEEDED(hr))
    {
        hr = pSourceContentInfo->ParseHeader(pBuffer, 0);
    }

    /*------- Initialize the ASF splitter. -------*/

    // Create the splitter.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFSplitter(&pSplitter);
    }
    
    // initialize the splitter with the ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pSplitter->Initialize(pSourceContentInfo);
    }


    /*------- Get the offset and size of the ASF Data Object. -------*/

    // Generate the presentation descriptor.
    if (SUCCEEDED(hr))
    {
        hr =  pSourceContentInfo->GeneratePresentationDescriptor(&pPD);
    }

    // Get the offset to the start of the Data Object.
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_DATA_START_OFFSET, pcbDataOffset);
    }

    // Get the length of the Data Object.
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_DATA_LENGTH, pcbDataLength);
    }

    // Return the pointers to the caller.
    if (SUCCEEDED(hr))
    {
        *ppSourceContentInfo = pSourceContentInfo;
        (*ppSourceContentInfo)->AddRef();

        *ppSplitter = pSplitter;
        (*ppSplitter)->AddRef();

    }

    SafeRelease(&pPD);
    SafeRelease(&pBuffer);
    SafeRelease(&pSourceContentInfo);
    SafeRelease(&pSplitter);

    return S_OK;
}
```



## <a name="5-create-an-audio-profile"></a><span data-ttu-id="4820d-185">5. créer un profil audio</span><span class="sxs-lookup"><span data-stu-id="4820d-185">5. Create an Audio Profile</span></span>

<span data-ttu-id="4820d-186">Ensuite, vous allez créer un objet de profil pour le fichier d’entrée en l’obtenant à partir de l’objet de la source ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="4820d-186">Next, you will create a profile object for the input file by obtaining it from the source ContentInfo object.</span></span> <span data-ttu-id="4820d-187">Vous allez ensuite configurer le profil afin qu’il ne contienne que les flux audio du fichier d’entrée.</span><span class="sxs-lookup"><span data-stu-id="4820d-187">You will then configure the profile so that it contains only the audio streams of the input file.</span></span> <span data-ttu-id="4820d-188">Pour ce faire, énumérez les flux et supprimez les flux non audio du profil.</span><span class="sxs-lookup"><span data-stu-id="4820d-188">To do this, enumerate the streams and remove non-audio streams from the profile.</span></span> <span data-ttu-id="4820d-189">L’objet profil audio sera utilisé ultérieurement dans ce didacticiel pour initialiser l’objet ContentInfo de sortie.</span><span class="sxs-lookup"><span data-stu-id="4820d-189">The audio profile object will be used later in this tutorial to initialize the output ContentInfo object.</span></span>

<span data-ttu-id="4820d-190">Pour créer un profil audio</span><span class="sxs-lookup"><span data-stu-id="4820d-190">To create an audio profile</span></span>

1.  <span data-ttu-id="4820d-191">Récupérez l’objet de profil du fichier d’entrée à partir de l’objet de la source ContentInfo en appelant [**IMFASFContentInfo :: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span><span class="sxs-lookup"><span data-stu-id="4820d-191">Get the profile object for the input file from the source ContentInfo object by calling [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span></span> <span data-ttu-id="4820d-192">La méthode retourne un pointeur vers un objet de profil qui contient tous les flux du fichier d’entrée.</span><span class="sxs-lookup"><span data-stu-id="4820d-192">The method returns a pointer to a profile object that contains all of the streams in the input file.</span></span> <span data-ttu-id="4820d-193">Pour plus d’informations, consultez [création d’un profil ASF](creating-an-asf-profile.md).</span><span class="sxs-lookup"><span data-stu-id="4820d-193">For more information see [Creating an ASF Profile](creating-an-asf-profile.md).</span></span>
2.  <span data-ttu-id="4820d-194">Supprimez tous les objets d’exclusion mutuelle du profil.</span><span class="sxs-lookup"><span data-stu-id="4820d-194">Remove any mutual exclusion objects from the profile.</span></span> <span data-ttu-id="4820d-195">Cette étape est requise car les flux non audio seront supprimés du profil, ce qui pourrait invalider les objets d’exclusion mutuelle.</span><span class="sxs-lookup"><span data-stu-id="4820d-195">This step is required because non-audio streams will be removed from the profile, which could invalidate the mutual exclusion objects.</span></span>
3.  <span data-ttu-id="4820d-196">Supprimez tous les flux non audio du profil, comme suit :</span><span class="sxs-lookup"><span data-stu-id="4820d-196">Remove all non-audio streams from the profile, as follows:</span></span>
    -   <span data-ttu-id="4820d-197">Appelez [**IMFASFProfile :: GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) pour connaître le nombre de flux.</span><span class="sxs-lookup"><span data-stu-id="4820d-197">Call [**IMFASFProfile::GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) to get the number of streams.</span></span>
    -   <span data-ttu-id="4820d-198">Dans une boucle, appelez [**IMFASFProfile :: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) pour obtenir chaque flux par index.</span><span class="sxs-lookup"><span data-stu-id="4820d-198">In a loop, call [**IMFASFProfile::GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) to get each stream by index.</span></span>
    -   <span data-ttu-id="4820d-199">Appelez [**IMFASFStreamConfig :: GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) pour accéder au type de flux.</span><span class="sxs-lookup"><span data-stu-id="4820d-199">Call [**IMFASFStreamConfig::GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) to get the stream type.</span></span>
    -   <span data-ttu-id="4820d-200">Pour les flux non audio, appelez [**IMFASFProfile :: RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream) pour supprimer le flux.</span><span class="sxs-lookup"><span data-stu-id="4820d-200">For non-audio streams, call [**IMFASFProfile::RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream) to remove the stream.</span></span>
4.  <span data-ttu-id="4820d-201">Stocke le numéro de flux du premier flux audio.</span><span class="sxs-lookup"><span data-stu-id="4820d-201">Store the stream number of the first audio stream.</span></span> <span data-ttu-id="4820d-202">Ce sera sélectionné sur le séparateur pour générer des exemples de flux.</span><span class="sxs-lookup"><span data-stu-id="4820d-202">This will be selected on the splitter to generate stream samples.</span></span> <span data-ttu-id="4820d-203">Si le numéro de flux est égal à zéro, l’appelant peut supposer qu’il n’y avait pas de fichier de flux audio.</span><span class="sxs-lookup"><span data-stu-id="4820d-203">If the stream number is zero, the caller can assume that there were no audio streams file.</span></span>

<span data-ttu-id="4820d-204">Le code suivant décrit ces étapes :</span><span class="sxs-lookup"><span data-stu-id="4820d-204">The following code these steps:</span></span>


```C++
//-------------------------------------------------------------------
// GetAudioProfile
//
// Gets the ASF profile from the source file and removes any video
// streams from the profile.
//-------------------------------------------------------------------

HRESULT GetAudioProfile(
    IMFASFContentInfo *pSourceContentInfo, 
    IMFASFProfile **ppAudioProfile, 
    WORD *pwSelectStreamNumber
    )
{
    IMFASFStreamConfig *pStream = NULL;
    IMFASFProfile *pProfile = NULL;

    DWORD dwTotalStreams = 0;
    WORD  wStreamNumber = 0; 
    GUID guidMajorType = GUID_NULL;
    
    // Get the profile object from the source ContentInfo object.
    HRESULT hr = pSourceContentInfo->GetProfile(&pProfile);

    // Remove mutexes from the profile
    if (SUCCEEDED(hr))
    {
        hr = RemoveMutexes(pProfile);
    }

    // Get the total number of streams on the profile.
    if (SUCCEEDED(hr))
    {
        hr = pProfile->GetStreamCount(&dwTotalStreams);
    }

    // Enumerate the streams and remove the non-audio streams.
    if (SUCCEEDED(hr))
    {
        for (DWORD index = 0; index < dwTotalStreams; )
        {
            hr = pProfile->GetStream(index, &wStreamNumber, &pStream);

            if (FAILED(hr)) { break; }

            hr = pStream->GetStreamType(&guidMajorType);

            SafeRelease(&pStream);

            if (FAILED(hr)) { break; }

            if (guidMajorType != MFMediaType_Audio)
            {
                hr = pProfile->RemoveStream(wStreamNumber);
    
                if (FAILED(hr)) { break; }

                index = 0;
                dwTotalStreams--;
            }
            else
            {
                // Store the first audio stream number. 
                // This will be selected on the splitter.

                if (*pwSelectStreamNumber == 0)
                {
                    *pwSelectStreamNumber = wStreamNumber;
                }

                index++;
            }
        }
    }

    if (SUCCEEDED(hr))
    {
        *ppAudioProfile = pProfile;
        (*ppAudioProfile)->AddRef();
    }

    SafeRelease(&pStream);
    SafeRelease(&pProfile);

    return S_OK;
}
```



<span data-ttu-id="4820d-205">La `RemoveMutexes` fonction supprime tous les objets d’exclusion mutuelle du profil :</span><span class="sxs-lookup"><span data-stu-id="4820d-205">The `RemoveMutexes` function removes any mutual exclusion objects from the profile:</span></span>


```C++
HRESULT RemoveMutexes(IMFASFProfile *pProfile)
{
    DWORD cMutex = 0;
    HRESULT hr = pProfile->GetMutualExclusionCount(&cMutex);

    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cMutex; i++)
        {
            hr = pProfile->RemoveMutualExclusion(0);

            if (FAILED(hr))
            {
                break;
            }
        }
    }

    return hr;
}
```



## <a name="6-initialize-objects-for-the-output-file"></a><span data-ttu-id="4820d-206">6. initialiser des objets pour le fichier de sortie</span><span class="sxs-lookup"><span data-stu-id="4820d-206">6. Initialize Objects for the Output File</span></span>

<span data-ttu-id="4820d-207">Ensuite, vous allez créer l’objet ContentInfo de sortie et le multiplexeur pour générer des paquets de données pour le fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="4820d-207">Next, you will create the output ContentInfo object and the multiplexer for generating data packets for the output file.</span></span>

<span data-ttu-id="4820d-208">Le profil audio créé à l’étape 4 sera utilisé pour remplir l’objet ContentInfo de sortie.</span><span class="sxs-lookup"><span data-stu-id="4820d-208">The audio profile created in step 4 will be used to populate the output ContentInfo object.</span></span> <span data-ttu-id="4820d-209">Cet objet contient des informations telles que des attributs de fichier globaux et des propriétés de flux.</span><span class="sxs-lookup"><span data-stu-id="4820d-209">This object contains information such as global file attributes and stream properties.</span></span> <span data-ttu-id="4820d-210">L’objet ContentInfo de sortie sera utilisé pour initialiser le multiplexeur qui générera des paquets de données pour le fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="4820d-210">The output ContentInfo object will be used to initialize the multiplexer that will generate data packets for the output file.</span></span> <span data-ttu-id="4820d-211">Une fois les paquets de données générés, l’objet ContentInfo doit être mis à jour pour refléter les nouvelles valeurs.</span><span class="sxs-lookup"><span data-stu-id="4820d-211">After the data packets are generated, the ContentInfo object must be updated to reflect the new values.</span></span>

<span data-ttu-id="4820d-212">Pour créer et initialiser des composants ASF pour le fichier de sortie</span><span class="sxs-lookup"><span data-stu-id="4820d-212">To create and initialize ASF components for the output file</span></span>

1.  <span data-ttu-id="4820d-213">Créez un objet ContentInfo vide en appelant [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) et remplissez-le avec les informations du profil audio créé à l’étape 3 en appelant [**IMFASFContentInfo :: SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile).</span><span class="sxs-lookup"><span data-stu-id="4820d-213">Create an empty ContentInfo object by calling [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) and populate it with information from the audio profile created in step 3 by calling [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile).</span></span> <span data-ttu-id="4820d-214">Pour plus d’informations, consultez [initialisation de l’objet ContentInfo d’un nouveau fichier ASF](initializing-the-contentinfo-object-of-a-new-asf-file.md).</span><span class="sxs-lookup"><span data-stu-id="4820d-214">For more information, see [Initializing the ContentInfo Object of a New ASF File](initializing-the-contentinfo-object-of-a-new-asf-file.md).</span></span>
2.  <span data-ttu-id="4820d-215">Créez et initialisez l’objet multiplexeur à l’aide de l’objet ContentInfo de sortie.</span><span class="sxs-lookup"><span data-stu-id="4820d-215">Create and initialize the multiplexer object by using the output ContentInfo object.</span></span> <span data-ttu-id="4820d-216">Pour plus d’informations, consultez [création de l’objet multiplexeur](creating-the-multiplexer-object.md).</span><span class="sxs-lookup"><span data-stu-id="4820d-216">For more information, see [Creating the Multiplexer Object](creating-the-multiplexer-object.md).</span></span>

<span data-ttu-id="4820d-217">L’exemple de code suivant montre une fonction qui consolide les étapes.</span><span class="sxs-lookup"><span data-stu-id="4820d-217">The following example code shows a function that consolidates the steps.</span></span> <span data-ttu-id="4820d-218">Cette fonction accepte un pointeur vers un objet de profil et retourne des pointeurs vers l’objet ContentInfo de sortie et le multiplexeur.</span><span class="sxs-lookup"><span data-stu-id="4820d-218">This function takes a pointer to a profile object and returns pointers to the output ContentInfo object and the multiplexer.</span></span>


```C++
//-------------------------------------------------------------------
// CreateOutputGenerators
//
// Creates the ASF mux and the ASF Content Info object for the 
// output file.
//-------------------------------------------------------------------

HRESULT CreateOutputGenerators(
    IMFASFProfile *pProfile, 
    IMFASFContentInfo **ppContentInfo, 
    IMFASFMultiplexer **ppMux
    )
{
    IMFASFContentInfo *pContentInfo = NULL;
    IMFASFMultiplexer *pMux = NULL;

    // Use the ASF profile to create the ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);

    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->SetProfile(pProfile);
    }

    // Create the ASF Multiplexer object.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFMultiplexer(&pMux);
    }
    
    // Initialize it using the new ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pMux->Initialize(pContentInfo);
    }

    // Return the pointers to the caller.
    if (SUCCEEDED(hr))
    {
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();

        *ppMux = pMux;
        (*ppMux)->AddRef();
    }

    SafeRelease(&pContentInfo);
    SafeRelease(&pMux);

    return hr;
}
```



## <a name="7-generate-new-asf-data-packets"></a><span data-ttu-id="4820d-219">7. générer de nouveaux paquets de données ASF</span><span class="sxs-lookup"><span data-stu-id="4820d-219">7. Generate New ASF Data Packets</span></span>

<span data-ttu-id="4820d-220">Ensuite, vous allez générer des exemples de flux audio à partir du flux d’octets source à l’aide du séparateur et les envoyer au multiplexeur pour créer des paquets de données ASF.</span><span class="sxs-lookup"><span data-stu-id="4820d-220">Next, you will generate audio stream samples from the source byte stream by using the splitter and send them to the multiplexer to create ASF data packets.</span></span> <span data-ttu-id="4820d-221">Ces paquets de données constituent l’objet de données ASF final pour le nouveau fichier.</span><span class="sxs-lookup"><span data-stu-id="4820d-221">These data packets will constitute the final ASF Data Object for the new file.</span></span>

<span data-ttu-id="4820d-222">Pour générer des exemples de flux audio</span><span class="sxs-lookup"><span data-stu-id="4820d-222">To generate audio stream samples</span></span>

1.  <span data-ttu-id="4820d-223">Sélectionnez le premier flux audio sur le séparateur en appelant [**IMFASFSplitter :: SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams).</span><span class="sxs-lookup"><span data-stu-id="4820d-223">Select the first audio stream on the splitter by calling [**IMFASFSplitter::SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams).</span></span>
2.  <span data-ttu-id="4820d-224">Lit les blocs de taille fixe des données multimédias à partir du flux d’octets source dans une mémoire tampon de média.</span><span class="sxs-lookup"><span data-stu-id="4820d-224">Read fixed-size blocks of media data from the source byte stream into a media buffer.</span></span>
3.  <span data-ttu-id="4820d-225">Collectez les exemples de flux en tant qu’exemples de supports à partir du séparateur en appelant [**IMFASFSplitter :: GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) dans une boucle, à condition qu’il reçoive l' \_ indicateur ASF STATUSFLAGS \_ incomplet dans le paramètre *pdwStatusFlags* .</span><span class="sxs-lookup"><span data-stu-id="4820d-225">Collect the stream samples as media samples from the splitter by calling [**IMFASFSplitter::GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) in a loop as long as it receives the ASF\_STATUSFLAGS\_INCOMPLETE flag in the *pdwStatusFlags* parameter.</span></span> <span data-ttu-id="4820d-226">Pour plus d’informations, consultez génération d’exemples pour les paquets de données ASF» dans [génération d’exemples de flux à partir d’un objet de données ASF existant](generating-stream-samples-from-an-existing-asf-data-object.md).</span><span class="sxs-lookup"><span data-stu-id="4820d-226">For more information, see Generating Samples for ASF Data Packets" in [Generating Stream Samples from an Existing ASF Data Object](generating-stream-samples-from-an-existing-asf-data-object.md).</span></span>
4.  <span data-ttu-id="4820d-227">Pour chaque exemple de support, appelez [**IMFASFMultiplexer ::P rocesssample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) pour envoyer l’exemple de support au multiplexeur.</span><span class="sxs-lookup"><span data-stu-id="4820d-227">For each media sample, call [**IMFASFMultiplexer::ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) to send the media sample to the multiplexer.</span></span> <span data-ttu-id="4820d-228">Le multiplexeur génère les paquets de données pour l’objet de données ASF.</span><span class="sxs-lookup"><span data-stu-id="4820d-228">The multiplexer generates the data packets for the ASF Data Object.</span></span>
5.  <span data-ttu-id="4820d-229">Écrire le paquet de données généré par le multiplexeur dans le flux d’octets de données.</span><span class="sxs-lookup"><span data-stu-id="4820d-229">Write the data packet generated by the multiplexer to the data byte stream.</span></span>
6.  <span data-ttu-id="4820d-230">Une fois tous les paquets de données générés, appelez [**IMFASFMultiplexer :: end**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) pour mettre à jour l’objet ContentInfo de sortie avec les informations collectées pendant la génération des paquets de données ASF.</span><span class="sxs-lookup"><span data-stu-id="4820d-230">After all the data packets have been generated, call [**IMFASFMultiplexer::End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) to update the output ContentInfo object with information collected during ASF data packet generation.</span></span>

<span data-ttu-id="4820d-231">L’exemple de code suivant génère des exemples de flux à partir du séparateur ASF et les envoie au multiplexeur.</span><span class="sxs-lookup"><span data-stu-id="4820d-231">The following example code generates stream samples from the ASF splitter and sends them to the multiplexer.</span></span> <span data-ttu-id="4820d-232">Le multiplexeur génère des paquets de données ASF et les écrit dans un flux.</span><span class="sxs-lookup"><span data-stu-id="4820d-232">The multiplexer generates ASF data packets and writes it to a stream.</span></span>


```C++
//-------------------------------------------------------------------
// GenerateASFDataObject
// 
// Creates a byte stream that contains the ASF Data Object for the
// output file.
//-------------------------------------------------------------------

HRESULT GenerateASFDataObject(
    IMFByteStream *pSourceStream, 
    IMFASFSplitter *pSplitter, 
    IMFASFMultiplexer *pMux, 
    UINT64   cbDataOffset,
    UINT64   cbDataLength,
    IMFByteStream **ppDataStream
    )
{
    IMFMediaBuffer *pBuffer = NULL;
    IMFByteStream *pDataStream = NULL;
    
    const DWORD READ_SIZE = 1024 * 4;

    // Flush the splitter to remove any pending samples.
    HRESULT hr = pSplitter->Flush();

    if (SUCCEEDED(hr))
    {
        hr = MFCreateTempFile(
            MF_ACCESSMODE_READWRITE, 
            MF_OPENMODE_DELETE_IF_EXIST,
            MF_FILEFLAGS_NONE,
            &pDataStream
            );
    }

    if (SUCCEEDED(hr))
    {
        hr = pSourceStream->SetCurrentPosition(cbDataOffset);
    }

    if (SUCCEEDED(hr))
    {
        while (cbDataLength > 0)
        {
            DWORD cbRead = min(READ_SIZE, (DWORD)cbDataLength);

            hr = AllocReadFromByteStream(
                pSourceStream, 
                cbRead, 
                &pBuffer
                );

            if (FAILED(hr)) 
            { 
                break; 
            }

            cbDataLength -= cbRead;

            // Push data on the splitter.
            hr =  pSplitter->ParseData(pBuffer, 0, 0);

            if (FAILED(hr)) 
            { 
                break; 
            }

            // Get ASF packets from the splitter and feed them to the mux.
            hr = GetPacketsFromSplitter(pSplitter, pMux, pDataStream);

            if (FAILED(hr)) 
            { 
                break; 
            }

            SafeRelease(&pBuffer);
        }
    }

    // Flush the mux and generate any remaining samples.
    if (SUCCEEDED(hr))
    {
        hr = pMux->Flush();
    }

    if (SUCCEEDED(hr))
    {
        hr = GenerateASFDataPackets(pMux, pDataStream);
    }

     // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppDataStream = pDataStream;
        (*ppDataStream)->AddRef();
    }

    SafeRelease(&pBuffer);
    SafeRelease(&pDataStream);
    return hr;
}
```



<span data-ttu-id="4820d-233">Pour recevoir des paquets du séparateur ASF, le code précédent appelle la `GetPacketsFromSplitter` fonction, comme indiqué ici :</span><span class="sxs-lookup"><span data-stu-id="4820d-233">To get packets from the ASF splitter, the previous code calls the `GetPacketsFromSplitter` function, shown here:</span></span>


```C++
//-------------------------------------------------------------------
// GetPacketsFromSplitter
//
// Gets samples from the ASF splitter.
//
// This function is called after calling IMFASFSplitter::ParseData.
//-------------------------------------------------------------------

HRESULT GetPacketsFromSplitter(
    IMFASFSplitter *pSplitter,
    IMFASFMultiplexer *pMux,
    IMFByteStream *pDataStream
    )
{
    HRESULT hr = S_OK;
    DWORD   dwStatus = ASF_STATUSFLAGS_INCOMPLETE;
    WORD    wStreamNum = 0;

    IMFSample *pSample = NULL;

    while (dwStatus & ASF_STATUSFLAGS_INCOMPLETE) 
    {
        hr = pSplitter->GetNextSample(&dwStatus, &wStreamNum, &pSample);

        if (FAILED(hr))
        {
            break;
        }

        if (pSample)
        {
            //Send to the multiplexer to convert it into ASF format
            hr = pMux->ProcessSample(wStreamNum, pSample, 0);

            if (FAILED(hr)) 
            { 
                break; 
            }

            hr = GenerateASFDataPackets(pMux, pDataStream);

            if (FAILED(hr)) 
            { 
                break; 
            }
        }

        SafeRelease(&pSample);
    }

    SafeRelease(&pSample);
    return hr;
}
```



<span data-ttu-id="4820d-234">La `GenerateDataPackets` fonction obtient les paquets de données du multiplexeur.</span><span class="sxs-lookup"><span data-stu-id="4820d-234">The `GenerateDataPackets` function gets data packets from multiplexer.</span></span> <span data-ttu-id="4820d-235">Pour plus d’informations, consultez [obtention de paquets de données ASF](generating-new-asf-data-packets.md).</span><span class="sxs-lookup"><span data-stu-id="4820d-235">For more information, see [Getting ASF Data Packets](generating-new-asf-data-packets.md).</span></span>


```C++
//-------------------------------------------------------------------
// GenerateASFDataPackets
// 
// Gets data packets from the mux. This function is called after 
// calling IMFASFMultiplexer::ProcessSample. 
//-------------------------------------------------------------------

HRESULT GenerateASFDataPackets( 
    IMFASFMultiplexer *pMux, 
    IMFByteStream *pDataStream
    )
{
    HRESULT hr = S_OK;

    IMFSample *pOutputSample = NULL;
    IMFMediaBuffer *pDataPacketBuffer = NULL;

    DWORD dwMuxStatus = ASF_STATUSFLAGS_INCOMPLETE;

    while (dwMuxStatus & ASF_STATUSFLAGS_INCOMPLETE)
    {
        hr = pMux->GetNextPacket(&dwMuxStatus, &pOutputSample);

        if (FAILED(hr))
        {
            break;
        }

        if (pOutputSample)
        {
            //Convert to contiguous buffer
            hr = pOutputSample->ConvertToContiguousBuffer(&pDataPacketBuffer);
            
            if (FAILED(hr))
            {
                break;
            }

            //Write buffer to byte stream
            hr = WriteBufferToByteStream(pDataStream, pDataPacketBuffer, NULL);

            if (FAILED(hr))
            {
                break;
            }
        }

        SafeRelease(&pDataPacketBuffer);
        SafeRelease(&pOutputSample);
    }

    SafeRelease(&pOutputSample);
    SafeRelease(&pDataPacketBuffer);
    return hr;
}
```



## <a name="8-write-the-asf-objects-in-the-new-file"></a><span data-ttu-id="4820d-236">8. écrire les objets ASF dans le nouveau fichier</span><span class="sxs-lookup"><span data-stu-id="4820d-236">8. Write the ASF Objects in the New File</span></span>

<span data-ttu-id="4820d-237">Ensuite, vous allez écrire le contenu de l’objet ContentInfo de sortie dans une mémoire tampon de média en appelant [**IMFASFContentInfo :: GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader).</span><span class="sxs-lookup"><span data-stu-id="4820d-237">Next, you will write the contents of the output ContentInfo object to a media buffer by calling [**IMFASFContentInfo::GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader).</span></span> <span data-ttu-id="4820d-238">Cette méthode convertit les données stockées dans l’objet ContentInfo en données binaires au format d’objet d’en-tête ASF.</span><span class="sxs-lookup"><span data-stu-id="4820d-238">This method converts data stored in the ContentInfo object into binary data in ASF Header Object format.</span></span> <span data-ttu-id="4820d-239">Pour plus d’informations, consultez [génération d’un nouvel objet d’en-tête ASF](generating-a-new-asf-header-object.md).</span><span class="sxs-lookup"><span data-stu-id="4820d-239">For more information, see [Generating a New ASF Header Object](generating-a-new-asf-header-object.md).</span></span>

<span data-ttu-id="4820d-240">Une fois le nouvel objet d’en-tête ASF généré, écrivez le fichier de sortie en écrivant d’abord l’objet d’en-tête dans le flux d’octets de sortie créé à l’étape 2 en appelant la fonction d’assistance WriteBufferToByteStream.</span><span class="sxs-lookup"><span data-stu-id="4820d-240">After the new ASF Header Object has been generated, write the output file by first writing the Header Object to the output byte stream created in step 2 by calling the helper function WriteBufferToByteStream.</span></span> <span data-ttu-id="4820d-241">Suivez l’objet d’en-tête avec l’objet de données contenu dans le flux d’octets de données.</span><span class="sxs-lookup"><span data-stu-id="4820d-241">Follow the Header Object with the Data Object contained in the data byte stream.</span></span> <span data-ttu-id="4820d-242">L’exemple de code montre une fonction qui transfère le contenu du flux d’octets de données vers le flux d’octets de sortie.</span><span class="sxs-lookup"><span data-stu-id="4820d-242">The example code shows a function that transfers contents of the data bytes stream to the output byte stream.</span></span>


```C++
//-------------------------------------------------------------------
// WriteASFFile
//
// Writes the complete ASF file.
//-------------------------------------------------------------------

HRESULT WriteASFFile( 
    IMFASFContentInfo *pContentInfo, // ASF Content Info for the output file.
    IMFByteStream *pDataStream,      // Data stream.
    PCWSTR pszFile                   // Output file name.
    )
{
    
    IMFMediaBuffer *pHeaderBuffer = NULL;
    IMFByteStream *pWmaStream = NULL;

    DWORD cbHeaderSize = 0;
    DWORD cbWritten = 0;

    // Create output file.
    HRESULT hr = MFCreateFile(
        MF_ACCESSMODE_WRITE, 
        MF_OPENMODE_DELETE_IF_EXIST,
        MF_FILEFLAGS_NONE,
        pszFile,
        &pWmaStream
        );

    // Get the size of the ASF Header Object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GenerateHeader(NULL, &cbHeaderSize);
    }

    // Create a media buffer.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(cbHeaderSize, &pHeaderBuffer);
    }

    // Populate the media buffer with the ASF Header Object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GenerateHeader(pHeaderBuffer, &cbHeaderSize);
    }
 
    // Write the header contents to the byte stream for the output file.
    if (SUCCEEDED(hr))
    {
        hr = WriteBufferToByteStream(pWmaStream, pHeaderBuffer, &cbWritten);
    }

    if (SUCCEEDED(hr))
    {
        hr = pDataStream->SetCurrentPosition(0);
    }

    // Append the data stream to the file.

    if (SUCCEEDED(hr))
    {
        hr = AppendToByteStream(pDataStream, pWmaStream);
    }

    SafeRelease(&pHeaderBuffer);
    SafeRelease(&pWmaStream);

    return hr;
}
```



## <a name="9-write-the-entry-point-function"></a><span data-ttu-id="4820d-243">9 écrire la fonction Entry-Point</span><span class="sxs-lookup"><span data-stu-id="4820d-243">9 Write the Entry-Point Function</span></span>

<span data-ttu-id="4820d-244">Vous pouvez maintenant mettre ensemble les étapes précédentes dans une application complète.</span><span class="sxs-lookup"><span data-stu-id="4820d-244">Now you can put the previous steps together into a complete application.</span></span> <span data-ttu-id="4820d-245">Avant d’utiliser l’un des objets Media Foundation, initialisez la plateforme Media Foundation en appelant [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span><span class="sxs-lookup"><span data-stu-id="4820d-245">Before using any of the Media Foundation objects, initialize the Media Foundation platform by calling [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span></span> <span data-ttu-id="4820d-246">Lorsque vous avez terminé, appelez [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span><span class="sxs-lookup"><span data-stu-id="4820d-246">When you are done, call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span></span> <span data-ttu-id="4820d-247">Pour plus d’informations, consultez [initialisation des Media Foundation](initializing-media-foundation.md).</span><span class="sxs-lookup"><span data-stu-id="4820d-247">For more information, see [Initializing Media Foundation](initializing-media-foundation.md).</span></span>

<span data-ttu-id="4820d-248">Le code suivant illustre l’application console complète.</span><span class="sxs-lookup"><span data-stu-id="4820d-248">The following code shows the complete console application.</span></span> <span data-ttu-id="4820d-249">L’argument de ligne de commande spécifie le nom du fichier à convertir et le nom du nouveau fichier audio.</span><span class="sxs-lookup"><span data-stu-id="4820d-249">The command-line argument specifies the name of the file to convert and the name of the new audio file.</span></span>


```C++
int wmain(int argc, WCHAR* argv[])
{
    if (argc != 3)
    {
        wprintf_s(L"Usage: %s input.wmv, %s output.wma\n");
        return 0;
    }

    HRESULT hr = MFStartup(MF_VERSION);

    if (FAILED(hr))
    {
        wprintf_s(L"MFStartup failed: 0x%X\n", hr);
        return 0;
    }

    PCWSTR pszInputFile = argv[1];      
    PCWSTR pszOutputFile = argv[2];     
    
    IMFByteStream      *pSourceStream = NULL;       
    IMFASFContentInfo  *pSourceContentInfo = NULL;  
    IMFASFProfile      *pAudioProfile = NULL;       
    IMFASFContentInfo  *pOutputContentInfo = NULL;  
    IMFByteStream      *pDataStream = NULL;         
    IMFASFSplitter     *pSplitter = NULL;           
    IMFASFMultiplexer  *pMux = NULL;                

    UINT64  cbDataOffset = 0;           
    UINT64  cbDataLength = 0;           
    WORD    wSelectStreamNumber = 0;    

    // Open the input file.

    hr = OpenFile(pszInputFile, &pSourceStream);

    // Initialize the objects that will parse the source file.

    if (SUCCEEDED(hr))
    {
        hr = CreateSourceParsers(
            pSourceStream, 
            &pSourceContentInfo,    // ASF Header for the source file.
            &pSplitter,             // Generates audio samples.
            &cbDataOffset,          // Offset to the first data packet.
            &cbDataLength           // Length of the ASF Data Object.
            );
    }

    // Create a profile object for the audio streams in the source file.

    if (SUCCEEDED(hr))
    {
        hr = GetAudioProfile(
            pSourceContentInfo, 
            &pAudioProfile,         // ASF profile for the audio stream.
            &wSelectStreamNumber    // Stream number of the first audio stream.
            );
    }

    // Initialize the objects that will generate the output data.

    if (SUCCEEDED(hr))
    {
        hr = CreateOutputGenerators(
            pAudioProfile, 
            &pOutputContentInfo,    // ASF Header for the output file.
            &pMux                   // Generates ASF data packets.
            );
    }

    // Set up the splitter to generate samples for the first
    // audio stream in the source media.

    if (SUCCEEDED(hr))
    {
        hr = pSplitter->SelectStreams(&wSelectStreamNumber, 1);
    }
    
    // Generate ASF Data Packets and store them in a byte stream.

    if (SUCCEEDED(hr))
    {
        hr = GenerateASFDataObject(
               pSourceStream, 
               pSplitter, 
               pMux, 
               cbDataOffset, 
               cbDataLength, 
               &pDataStream    // Byte stream for the ASF data packets.    
               );
    }

    // Update the header with new information if any.

    if (SUCCEEDED(hr))
    {
        hr = pMux->End(pOutputContentInfo);
    }

    //Write the ASF objects to the output file
    if (SUCCEEDED(hr))
    {
        hr = WriteASFFile(pOutputContentInfo, pDataStream, pszOutputFile);
    }

    // Clean up.
    SafeRelease(&pMux);
    SafeRelease(&pSplitter);
    SafeRelease(&pDataStream);
    SafeRelease(&pOutputContentInfo);
    SafeRelease(&pAudioProfile);
    SafeRelease(&pSourceContentInfo);
    SafeRelease(&pSourceStream);

    MFShutdown();

    if (FAILED(hr))
    {
        wprintf_s(L"Could not create the audio file: 0x%X\n", hr);
    }

    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="4820d-250">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4820d-250">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4820d-251">Composants WMContainer ASF</span><span class="sxs-lookup"><span data-stu-id="4820d-251">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="4820d-252">Prise en charge ASF dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4820d-252">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



