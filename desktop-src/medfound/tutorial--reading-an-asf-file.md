---
description: Ce didacticiel montre comment récupérer des paquets de données à partir d’un fichier ASF (Advanced Systems Format) à l’aide du séparateur ASF.
ms.assetid: e3a55275-e8f0-4ab7-98db-a2f2c54d5a51
title: 'Didacticiel : lecture d’un fichier ASF à l’aide d’objets WMContainer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0225f434f650f0423771122e6fc345022e69ec1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527399"
---
# <a name="tutorial-reading-an-asf-file-by-using-wmcontainer-objects"></a><span data-ttu-id="dbf36-103">Didacticiel : lecture d’un fichier ASF à l’aide d’objets WMContainer</span><span class="sxs-lookup"><span data-stu-id="dbf36-103">Tutorial: Reading an ASF File by Using WMContainer Objects</span></span>

<span data-ttu-id="dbf36-104">Ce didacticiel montre comment récupérer des paquets de données à partir d’un fichier ASF (Advanced Systems Format) à l’aide du [séparateur ASF](asf-splitter.md).</span><span class="sxs-lookup"><span data-stu-id="dbf36-104">This tutorial shows how to get data packets from an Advanced Systems Format (ASF) file using the [ASF Splitter](asf-splitter.md).</span></span> <span data-ttu-id="dbf36-105">Dans ce didacticiel, vous allez créer une application console simple qui lit un fichier ASF et génère des exemples de supports compressés pour le premier flux vidéo du fichier.</span><span class="sxs-lookup"><span data-stu-id="dbf36-105">In this tutorial, you will create a simple console application that reads an ASF file and generates compressed media samples for the first video stream in the file.</span></span> <span data-ttu-id="dbf36-106">L’application affiche des informations sur les images clés du flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="dbf36-106">The application displays information about the key frames in the video stream.</span></span>

<span data-ttu-id="dbf36-107">Ce didacticiel comprend les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="dbf36-107">This tutorial contains the following steps:</span></span>

-   [<span data-ttu-id="dbf36-108">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="dbf36-108">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="dbf36-109">1. configurer le projet</span><span class="sxs-lookup"><span data-stu-id="dbf36-109">1. Set up the Project</span></span>](#1-set-up-the-project)
-   [<span data-ttu-id="dbf36-110">2. ouvrir un fichier ASF</span><span class="sxs-lookup"><span data-stu-id="dbf36-110">2. Open an ASF File</span></span>](#2-open-an-asf-file)
-   [<span data-ttu-id="dbf36-111">3. lire l’objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="dbf36-111">3. Read the ASF Header Object</span></span>](#3-read-the-asf-header-object)
-   [<span data-ttu-id="dbf36-112">4. créer le séparateur ASF</span><span class="sxs-lookup"><span data-stu-id="dbf36-112">4. Create the ASF Splitter</span></span>](#4-create-the-asf-splitter)
-   [<span data-ttu-id="dbf36-113">5. Sélectionner un flux pour l’analyse</span><span class="sxs-lookup"><span data-stu-id="dbf36-113">5. Select a Stream for Parsing</span></span>](#5-select-a-stream-for-parsing)
-   [<span data-ttu-id="dbf36-114">6. générer des exemples de supports compressés</span><span class="sxs-lookup"><span data-stu-id="dbf36-114">6. Generate Compressed Media Samples</span></span>](#6-generate-compressed-media-samples)
-   [<span data-ttu-id="dbf36-115">7. écrire la fonction Entry-Point</span><span class="sxs-lookup"><span data-stu-id="dbf36-115">7. Write the Entry-Point Function</span></span>](#7-write-the-entry-point-function)
-   [<span data-ttu-id="dbf36-116">Liste des programmes</span><span class="sxs-lookup"><span data-stu-id="dbf36-116">Program Listing</span></span>](#program-listing)
-   [<span data-ttu-id="dbf36-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dbf36-117">Related topics</span></span>](#related-topics)

<span data-ttu-id="dbf36-118">Ce didacticiel ne traite pas de la façon de décoder les données compressées que l’application obtient du séparateur ASF.</span><span class="sxs-lookup"><span data-stu-id="dbf36-118">The tutorial does not cover how to decode the compressed data that the application gets from the ASF splitter.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="dbf36-119">Prérequis</span><span class="sxs-lookup"><span data-stu-id="dbf36-119">Prerequisites</span></span>

<span data-ttu-id="dbf36-120">Ce didacticiel part des principes suivants :</span><span class="sxs-lookup"><span data-stu-id="dbf36-120">This tutorial assumes the following:</span></span>

-   <span data-ttu-id="dbf36-121">Vous êtes familiarisé avec la structure d’un fichier ASF et les composants fournis par Media Foundation pour travailler avec des objets ASF.</span><span class="sxs-lookup"><span data-stu-id="dbf36-121">You are familiar with the structure of an ASF file and the components provided by Media Foundation to work with ASF Objects.</span></span> <span data-ttu-id="dbf36-122">Ces composants incluent l’objet ContentInfo, le séparateur, le multiplexeur et le profil.</span><span class="sxs-lookup"><span data-stu-id="dbf36-122">These components include the ContentInfo object, splitter, multiplexer, and profile.</span></span> <span data-ttu-id="dbf36-123">Pour plus d’informations, consultez [WMCONTAINER ASF Components](wmcontainer-asf-components.md).</span><span class="sxs-lookup"><span data-stu-id="dbf36-123">For more information, see [WMContainer ASF Components](wmcontainer-asf-components.md).</span></span>
-   <span data-ttu-id="dbf36-124">Vous êtes familiarisé avec les [mémoires tampons de média](media-buffers.md) et les flux d’octets : en particulier, les opérations de fichier utilisant un flux d’octets, la lecture d’un flux d’octets dans une mémoire tampon de média et l’écriture du contenu d’une mémoire tampon de média dans un flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="dbf36-124">You are familiar with [Media Buffers](media-buffers.md) and byte streams: Specifically, file operations using a byte stream, reading from a byte stream into a media buffer, and writing the contents of a media buffer to a byte stream.</span></span>

## <a name="1-set-up-the-project"></a><span data-ttu-id="dbf36-125">1. configurer le projet</span><span class="sxs-lookup"><span data-stu-id="dbf36-125">1. Set up the Project</span></span>

<span data-ttu-id="dbf36-126">Incluez les en-têtes suivants dans votre fichier source :</span><span class="sxs-lookup"><span data-stu-id="dbf36-126">Include the following headers in your source file:</span></span>


```C++
#include <stdio.h>       // Standard I/O
#include <windows.h>     // Windows headers
#include <mfapi.h>       // Media Foundation platform
#include <wmcontainer.h> // ASF interfaces
#include <Mferror.h>
```



<span data-ttu-id="dbf36-127">Lien vers les fichiers de bibliothèque suivants :</span><span class="sxs-lookup"><span data-stu-id="dbf36-127">Link to the following library files:</span></span>

-   <span data-ttu-id="dbf36-128">mfplat. lib</span><span class="sxs-lookup"><span data-stu-id="dbf36-128">mfplat.lib</span></span>
-   <span data-ttu-id="dbf36-129">MF. lib</span><span class="sxs-lookup"><span data-stu-id="dbf36-129">mf.lib</span></span>
-   <span data-ttu-id="dbf36-130">mfuuid. lib</span><span class="sxs-lookup"><span data-stu-id="dbf36-130">mfuuid.lib</span></span>

<span data-ttu-id="dbf36-131">Déclarez la fonction [SafeRelease](saferelease.md) :</span><span class="sxs-lookup"><span data-stu-id="dbf36-131">Declare the [SafeRelease](saferelease.md) function:</span></span>


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



## <a name="2-open-an-asf-file"></a><span data-ttu-id="dbf36-132">2. ouvrir un fichier ASF</span><span class="sxs-lookup"><span data-stu-id="dbf36-132">2. Open an ASF File</span></span>

<span data-ttu-id="dbf36-133">Ensuite, ouvrez le fichier spécifié en appelant la fonction [**MFCreateFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) .</span><span class="sxs-lookup"><span data-stu-id="dbf36-133">Next, open the specified file by calling the [**MFCreateFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) function.</span></span> <span data-ttu-id="dbf36-134">La méthode retourne un pointeur vers l’objet de flux d’octets qui contient le contenu du fichier.</span><span class="sxs-lookup"><span data-stu-id="dbf36-134">The method returns a pointer to the byte stream object that contains the contents of the file.</span></span> <span data-ttu-id="dbf36-135">Le nom de fichier est spécifié par l’utilisateur via les arguments de ligne de commande de l’application.</span><span class="sxs-lookup"><span data-stu-id="dbf36-135">The filename is specified by the user through command line arguments of the application.</span></span>

<span data-ttu-id="dbf36-136">L’exemple de code suivant prend un nom de fichier et retourne un pointeur vers un objet de flux d’octets qui peut être utilisé pour lire le fichier.</span><span class="sxs-lookup"><span data-stu-id="dbf36-136">The following example code takes a file name and returns a pointer to a byte stream object that can be used to read the file.</span></span>


```C++
        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);
```



## <a name="3-read-the-asf-header-object"></a><span data-ttu-id="dbf36-137">3. lire l’objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="dbf36-137">3. Read the ASF Header Object</span></span>

<span data-ttu-id="dbf36-138">Créez ensuite l' [objet ASF ContentInfo](asf-contentinfo-object.md) et utilisez-le pour analyser l’objet d’en-tête ASF du fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="dbf36-138">Next, create the [ASF ContentInfo Object](asf-contentinfo-object.md) and use it to parse the ASF Header Object of the specified file.</span></span> <span data-ttu-id="dbf36-139">L’objet ContentInfo stocke les informations de l’en-tête ASF, y compris les attributs de fichier globaux et les informations sur chaque flux.</span><span class="sxs-lookup"><span data-stu-id="dbf36-139">The ContentInfo object stores information from the ASF header, including global file attributes and information about each stream.</span></span> <span data-ttu-id="dbf36-140">Vous utiliserez l’objet ContentInfo plus tard dans le didacticiel pour initialiser le séparateur ASF et récupérer le numéro de flux du flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="dbf36-140">You will use the ContentInfo object later in the tutorial to initialize the ASF splitter and get the stream number of the video stream.</span></span>

<span data-ttu-id="dbf36-141">Pour créer l’objet ASF ContentInfo :</span><span class="sxs-lookup"><span data-stu-id="dbf36-141">To create the ASF ContentInfo object:</span></span>

1.  <span data-ttu-id="dbf36-142">Appelez la fonction [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) pour créer un objet ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="dbf36-142">Call the [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) function to create a ContentInfo object.</span></span> <span data-ttu-id="dbf36-143">La méthode retourne un pointeur vers l’interface [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) .</span><span class="sxs-lookup"><span data-stu-id="dbf36-143">The method returns a pointer to the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface.</span></span>
2.  <span data-ttu-id="dbf36-144">Lire les 30 premiers octets de données du fichier ASF dans une mémoire tampon de média.</span><span class="sxs-lookup"><span data-stu-id="dbf36-144">Read the first 30 bytes of data from the ASF file into a media buffer.</span></span>
3.  <span data-ttu-id="dbf36-145">Transmettez la mémoire tampon du média à la méthode [**IMFASFContentInfo :: GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) .</span><span class="sxs-lookup"><span data-stu-id="dbf36-145">Pass the media buffer to the [**IMFASFContentInfo::GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) method.</span></span> <span data-ttu-id="dbf36-146">Cette méthode retourne la taille totale de l’objet d’en-tête dans le fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="dbf36-146">This method returns the total size of the Header Object in the ASF file.</span></span>
4.  <span data-ttu-id="dbf36-147">Transmettez le même tampon de média à la méthode [**IMFASFContentInfo ::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) .</span><span class="sxs-lookup"><span data-stu-id="dbf36-147">Pass the same media buffer to the [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method.</span></span>
5.  <span data-ttu-id="dbf36-148">Lisez le reste de l’objet d’en-tête dans une nouvelle mémoire tampon de média.</span><span class="sxs-lookup"><span data-stu-id="dbf36-148">Read the remainder of the Header Object into a new media buffer.</span></span>
6.  <span data-ttu-id="dbf36-149">Transmettez la deuxième mémoire tampon à la méthode [**ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) .</span><span class="sxs-lookup"><span data-stu-id="dbf36-149">Pass the second buffer to the [**ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method.</span></span> <span data-ttu-id="dbf36-150">Spécifiez le décalage de 30 octets dans le paramètre *cbOffsetWithinHeader* de **ParseHeader**.</span><span class="sxs-lookup"><span data-stu-id="dbf36-150">Specify the 30-byte offset in the *cbOffsetWithinHeader* parameter of **ParseHeader**.</span></span> <span data-ttu-id="dbf36-151">La méthode **ParseHeader** Initialise l’objet ContentInfo avec les informations collectées à partir des divers objets ASF contenus dans l’objet d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="dbf36-151">The **ParseHeader** method initializes the ContentInfo object with information gathered from the various ASF objects contained in the Header Object.</span></span>


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



<span data-ttu-id="dbf36-152">Cette fonction utilise la `ReadFromByteStream` fonction pour lire un flux d’octets dans une mémoire tampon de média :</span><span class="sxs-lookup"><span data-stu-id="dbf36-152">This function uses the `ReadFromByteStream` function to read from a byte stream into a media buffer:</span></span>


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



## <a name="4-create-the-asf-splitter"></a><span data-ttu-id="dbf36-153">4. créer le séparateur ASF</span><span class="sxs-lookup"><span data-stu-id="dbf36-153">4. Create the ASF Splitter</span></span>

<span data-ttu-id="dbf36-154">Ensuite, créez l’objet [séparateur ASF](asf-splitter.md) .</span><span class="sxs-lookup"><span data-stu-id="dbf36-154">Next, create the [ASF Splitter](asf-splitter.md) object.</span></span> <span data-ttu-id="dbf36-155">Vous allez utiliser le séparateur ASF pour analyser l’objet de données ASF, qui contient des données multimédias en paquets pour le fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="dbf36-155">You will use the ASF splitter to parse the ASF Data Object, which contains packetized media data for the ASF file.</span></span>

<span data-ttu-id="dbf36-156">Pour créer un objet Splitter pour le fichier ASF :</span><span class="sxs-lookup"><span data-stu-id="dbf36-156">To create a splitter object for the ASF File:</span></span>

1.  <span data-ttu-id="dbf36-157">Appelez la fonction [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) pour créer le séparateur ASF.</span><span class="sxs-lookup"><span data-stu-id="dbf36-157">Call the [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) function to create the ASF splitter.</span></span> <span data-ttu-id="dbf36-158">La fonction retourne un pointeur vers l’interface [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) .</span><span class="sxs-lookup"><span data-stu-id="dbf36-158">The function returns a pointer to the [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) interface.</span></span>
2.  <span data-ttu-id="dbf36-159">Appelez [**IMFASFSplitter :: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) pour initialiser le séparateur ASF.</span><span class="sxs-lookup"><span data-stu-id="dbf36-159">Call [**IMFASFSplitter::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) to initialize the ASF splitter.</span></span> <span data-ttu-id="dbf36-160">Cette méthode prend un pointeur vers l’objet ContentInfo, qui a été créé dans la procédure 3.</span><span class="sxs-lookup"><span data-stu-id="dbf36-160">This method takes a pointer to the ContentInfo object, which was created in procedure 3.</span></span>


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



## <a name="5-select-a-stream-for-parsing"></a><span data-ttu-id="dbf36-161">5. Sélectionner un flux pour l’analyse</span><span class="sxs-lookup"><span data-stu-id="dbf36-161">5. Select a Stream for Parsing</span></span>

<span data-ttu-id="dbf36-162">Ensuite, énumérez les flux dans le fichier ASF et sélectionnez le premier flux vidéo à analyser.</span><span class="sxs-lookup"><span data-stu-id="dbf36-162">Next, enumerate the streams in the ASF file and select the first video stream for parsing.</span></span> <span data-ttu-id="dbf36-163">Pour énumérer les flux, vous allez utiliser un objet de profil ASF et rechercher les flux qui ont un type de média vidéo.</span><span class="sxs-lookup"><span data-stu-id="dbf36-163">To enumerate the streams, you will use an ASF profile object and search for streams that have a video media type.</span></span>

<span data-ttu-id="dbf36-164">Pour sélectionner le flux vidéo :</span><span class="sxs-lookup"><span data-stu-id="dbf36-164">To select the video stream:</span></span>

1.  <span data-ttu-id="dbf36-165">Appelez [**IMFASFContentInfo :: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile) sur l’objet ContentInfo pour créer un profil ASF.</span><span class="sxs-lookup"><span data-stu-id="dbf36-165">Call [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile) on the ContentInfo object to create an ASF profile.</span></span> <span data-ttu-id="dbf36-166">Parmi d’autres informations, le profil décrit les flux dans le fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="dbf36-166">Among other information, the profile describes the streams in the ASF file.</span></span>
2.  <span data-ttu-id="dbf36-167">Appelez [**IMFASFProfile :: GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) pour connaître le nombre de flux dans le fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="dbf36-167">Call [**IMFASFProfile::GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) to get the number of streams in the ASF file.</span></span>
3.  <span data-ttu-id="dbf36-168">Appelez [**IMFASFProfile :: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) dans une boucle pour énumérer les flux.</span><span class="sxs-lookup"><span data-stu-id="dbf36-168">Call [**IMFASFProfile::GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) in a loop to enumerate the streams.</span></span> <span data-ttu-id="dbf36-169">La méthode retourne un pointeur vers l’interface [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .</span><span class="sxs-lookup"><span data-stu-id="dbf36-169">The method returns a pointer to the [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface.</span></span> <span data-ttu-id="dbf36-170">Elle retourne également l’identificateur de flux.</span><span class="sxs-lookup"><span data-stu-id="dbf36-170">It also returns the stream identifier.</span></span>
4.  <span data-ttu-id="dbf36-171">Appelez [**IMFASFStreamConfig :: GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) pour obtenir le GUID du type principal du flux.</span><span class="sxs-lookup"><span data-stu-id="dbf36-171">Call [**IMFASFStreamConfig::GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) to get the major type GUID for the stream.</span></span> <span data-ttu-id="dbf36-172">Si le GUID de type principal est MFMediaType \_ vidéo, le flux contient une vidéo.</span><span class="sxs-lookup"><span data-stu-id="dbf36-172">If the major type GUID is MFMediaType\_Video, the stream contains video.</span></span>
5.  <span data-ttu-id="dbf36-173">Si vous avez trouvé un flux vidéo à l’étape 4, appelez [**IMFASFSplitter :: SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) pour sélectionner le flux.</span><span class="sxs-lookup"><span data-stu-id="dbf36-173">If you found a video stream in step 4, call [**IMFASFSplitter::SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) to select the stream.</span></span> <span data-ttu-id="dbf36-174">Cette méthode prend un tableau d’identificateurs de flux.</span><span class="sxs-lookup"><span data-stu-id="dbf36-174">This method takes an array of stream identifiers.</span></span> <span data-ttu-id="dbf36-175">Pour ce didacticiel, la taille du tableau est 1 parce que l’application analyse un seul flux.</span><span class="sxs-lookup"><span data-stu-id="dbf36-175">For this tutorial, the array size is 1 because the application will parse a single stream.</span></span>

<span data-ttu-id="dbf36-176">L’exemple de code suivant énumère les flux du fichier ASF et sélectionne le premier flux vidéo sur le séparateur ASF :</span><span class="sxs-lookup"><span data-stu-id="dbf36-176">The following example code enumerates the streams in the ASF file and selects the first video stream on the ASF splitter:</span></span>


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



## <a name="6-generate-compressed-media-samples"></a><span data-ttu-id="dbf36-177">6. générer des exemples de supports compressés</span><span class="sxs-lookup"><span data-stu-id="dbf36-177">6. Generate Compressed Media Samples</span></span>

<span data-ttu-id="dbf36-178">Ensuite, utilisez le séparateur ASF pour analyser l’objet de données ASF et obtenir les paquets de données pour le flux vidéo sélectionné.</span><span class="sxs-lookup"><span data-stu-id="dbf36-178">Next, use the ASF splitter to parse the ASF Data Object and get the data packets for the selected video stream.</span></span> <span data-ttu-id="dbf36-179">L’application lit les données du fichier ASF dans des blocs de taille fixe et les transmet au séparateur ASF.</span><span class="sxs-lookup"><span data-stu-id="dbf36-179">The application reads data from the ASF file in fixed-size blocks and passes the data to the ASF splitter.</span></span> <span data-ttu-id="dbf36-180">Le séparateur analyse les données et génère des [exemples de médias](media-samples.md) qui contiennent les données vidéo compressées.</span><span class="sxs-lookup"><span data-stu-id="dbf36-180">The splitter parses the data and generates [Media Samples](media-samples.md) that contain the compressed video data.</span></span> <span data-ttu-id="dbf36-181">L’application vérifie si chaque échantillon représente une image clé.</span><span class="sxs-lookup"><span data-stu-id="dbf36-181">The application checks whether each sample represents a key frame.</span></span> <span data-ttu-id="dbf36-182">Si c’est le cas, l’application affiche des informations de base sur l’exemple :</span><span class="sxs-lookup"><span data-stu-id="dbf36-182">If so, the application displays some basic information about the sample:</span></span>

-   <span data-ttu-id="dbf36-183">Nombre de mémoires tampons de média</span><span class="sxs-lookup"><span data-stu-id="dbf36-183">Number of media buffers</span></span>
-   <span data-ttu-id="dbf36-184">Taille totale des données</span><span class="sxs-lookup"><span data-stu-id="dbf36-184">Total size of the data</span></span>
-   <span data-ttu-id="dbf36-185">Horodatage</span><span class="sxs-lookup"><span data-stu-id="dbf36-185">Time stamp</span></span>

<span data-ttu-id="dbf36-186">Pour générer des exemples de supports compressés :</span><span class="sxs-lookup"><span data-stu-id="dbf36-186">To generate compressed media samples:</span></span>

1.  <span data-ttu-id="dbf36-187">Allouez un nouveau tampon de média.</span><span class="sxs-lookup"><span data-stu-id="dbf36-187">Allocate a new media buffer.</span></span>
2.  <span data-ttu-id="dbf36-188">Lit les données du flux d’octets dans la mémoire tampon du média.</span><span class="sxs-lookup"><span data-stu-id="dbf36-188">Read data from the byte stream into the media buffer.</span></span>
3.  <span data-ttu-id="dbf36-189">Transmettez la mémoire tampon du média à la méthode [**IMFASFSplitter ::P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) .</span><span class="sxs-lookup"><span data-stu-id="dbf36-189">Pass the media buffer to the [**IMFASFSplitter::ParseData**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) method.</span></span> <span data-ttu-id="dbf36-190">La méthode analyse les données ASF dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="dbf36-190">The method parses the ASF data in the buffer.</span></span>
4.  <span data-ttu-id="dbf36-191">Dans une boucle, récupérez des échantillons de média à partir du séparateur en appelant [**IMFASFSplitter :: GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample).</span><span class="sxs-lookup"><span data-stu-id="dbf36-191">In a loop, get media samples from the splitter by calling [**IMFASFSplitter::GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample).</span></span> <span data-ttu-id="dbf36-192">Si le paramètre *ppISample* reçoit un pointeur [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) valide, cela signifie que le séparateur ASF a analysé un ou plusieurs paquets de données.</span><span class="sxs-lookup"><span data-stu-id="dbf36-192">If the *ppISample* parameter receives a valid [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pointer, it means the ASF splitter has parsed one or more data packets.</span></span> <span data-ttu-id="dbf36-193">Si *ppISample* reçoit la valeur **null**, interrompez la boucle et revenez à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="dbf36-193">If *ppISample* receives the value **NULL**, break from the loop and go back to step 1.</span></span>
5.  <span data-ttu-id="dbf36-194">Affiche des informations sur l’exemple.</span><span class="sxs-lookup"><span data-stu-id="dbf36-194">Display information about the sample.</span></span>
6.  <span data-ttu-id="dbf36-195">Arrêter à partir de la boucle dans les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="dbf36-195">Break from the loop in the following conditions:</span></span>
    -   <span data-ttu-id="dbf36-196">Le paramètre *ppISample* reçoit la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="dbf36-196">The *ppISample* parameter receives the value **NULL**.</span></span>
    -   <span data-ttu-id="dbf36-197">Le paramètre *pdwStatusFlags* ne reçoit pas l' **indicateur \_ STATUSFLAGS ASF \_ incomplet** .</span><span class="sxs-lookup"><span data-stu-id="dbf36-197">The *pdwStatusFlags* parameter does not receive the **ASF\_STATUSFLAGS\_INCOMPLETE** flag.</span></span>

<span data-ttu-id="dbf36-198">Répétez ces étapes jusqu’à ce que vous atteigniez la fin du fichier.</span><span class="sxs-lookup"><span data-stu-id="dbf36-198">Repeat these steps until you reach the end of the file.</span></span> <span data-ttu-id="dbf36-199">Le code suivant illustre ces étapes :</span><span class="sxs-lookup"><span data-stu-id="dbf36-199">The following code shows these steps:</span></span>


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



<span data-ttu-id="dbf36-200">La fonction IsKeyFrame teste si un exemple est une image clé, en obtenant la valeur de l’attribut [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="dbf36-200">The IsKeyFrame function tests whether a sample is a key frame, by getting the value of the [**MFSampleExtension\_CleanPoint**](mfsampleextension-cleanpoint-attribute.md) attribute.</span></span>


```C++
inline BOOL IsRandomAccessPoint(IMFSample *pSample)
{
    // Check for the "clean point" attribute. Default to FALSE.
    return MFGetAttributeUINT32(pSample, MFSampleExtension_CleanPoint, FALSE);
}
```



<span data-ttu-id="dbf36-201">À des fins d’illustration, ce didacticiel affiche des informations pour chaque image clé vidéo, en appelant la fonction suivante :</span><span class="sxs-lookup"><span data-stu-id="dbf36-201">For illustration purposes, this tutorial displays some information for each video key frame, by calling the following function:</span></span>


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



<span data-ttu-id="dbf36-202">Une application classique utilise les paquets de données pour le décodage, l’remuxing, l’envoi sur le réseau ou une autre tâche.</span><span class="sxs-lookup"><span data-stu-id="dbf36-202">A typical application would use the data packets for decoding, remuxing, sending over the network, or some other task.</span></span>

## <a name="7-write-the-entry-point-function"></a><span data-ttu-id="dbf36-203">7. écrire la fonction Entry-Point</span><span class="sxs-lookup"><span data-stu-id="dbf36-203">7. Write the Entry-Point Function</span></span>

<span data-ttu-id="dbf36-204">Vous pouvez maintenant mettre ensemble les étapes précédentes dans une application complète.</span><span class="sxs-lookup"><span data-stu-id="dbf36-204">Now you can put the previous steps together into a complete application.</span></span> <span data-ttu-id="dbf36-205">Avant d’utiliser l’un des objets Media Foundation, initialisez la plateforme Media Foundation en appelant [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span><span class="sxs-lookup"><span data-stu-id="dbf36-205">Before using any of the Media Foundation objects, initialize the Media Foundation platform by calling [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span></span> <span data-ttu-id="dbf36-206">Lorsque vous avez terminé, appelez [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span><span class="sxs-lookup"><span data-stu-id="dbf36-206">When you are done, call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span></span> <span data-ttu-id="dbf36-207">Pour plus d’informations, [l’initialisation de Media Foundation](initializing-media-foundation.md).</span><span class="sxs-lookup"><span data-stu-id="dbf36-207">For more information, [Initializing Media Foundation](initializing-media-foundation.md).</span></span>


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



## <a name="program-listing"></a><span data-ttu-id="dbf36-208">Liste des programmes</span><span class="sxs-lookup"><span data-stu-id="dbf36-208">Program Listing</span></span>

<span data-ttu-id="dbf36-209">Le code suivant illustre la liste complète du didacticiel.</span><span class="sxs-lookup"><span data-stu-id="dbf36-209">The following code shows the complete listing for the tutorial.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="dbf36-210">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dbf36-210">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dbf36-211">Composants WMContainer ASF</span><span class="sxs-lookup"><span data-stu-id="dbf36-211">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="dbf36-212">Prise en charge ASF dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dbf36-212">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



