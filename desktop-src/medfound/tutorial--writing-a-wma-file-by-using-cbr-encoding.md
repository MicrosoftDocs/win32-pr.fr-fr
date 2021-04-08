---
description: Ce didacticiel illustre l’écriture d’un nouveau fichier audio (. WMA) en extrayant du contenu multimédia à partir d’un fichier audio non compressé (. wav), puis en le compressant au format ASF.
ms.assetid: f310c6ed-52e7-4828-9d4c-2f7ced9080c5
title: 'Didacticiel : écriture d’un fichier WMA à l’aide d’objets WMContainer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d156b75ced6cde2953ec90362ed13b0cc53bb83c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863937"
---
# <a name="tutorial-writing-a-wma-file-by-using-wmcontainer-objects"></a><span data-ttu-id="afc0e-103">Didacticiel : écriture d’un fichier WMA à l’aide d’objets WMContainer</span><span class="sxs-lookup"><span data-stu-id="afc0e-103">Tutorial: Writing a WMA File by Using WMContainer Objects</span></span>

<span data-ttu-id="afc0e-104">Ce didacticiel illustre l’écriture d’un nouveau fichier audio (. WMA) en extrayant du contenu multimédia à partir d’un fichier audio non compressé (. wav), puis en le compressant au format ASF.</span><span class="sxs-lookup"><span data-stu-id="afc0e-104">This tutorial demonstrates writing a new audio file (.wma) by extracting media content from an uncompressed audio file (.wav) and then compressing it in ASF format.</span></span> <span data-ttu-id="afc0e-105">Le mode d’encodage utilisé pour la conversion est le CBR ( [constant bit rate encodage](constant-bit-rate-encoding.md) ).</span><span class="sxs-lookup"><span data-stu-id="afc0e-105">The encoding mode used for the conversion is [Constant Bit Rate Encoding](constant-bit-rate-encoding.md) (CBR).</span></span> <span data-ttu-id="afc0e-106">Dans ce mode, avant la session d’encodage, l’application spécifie une vitesse de transmission cible que l’encodeur doit atteindre.</span><span class="sxs-lookup"><span data-stu-id="afc0e-106">In this mode, before the encoding session, the application specifies a target bit rate that the encoder must achieve.</span></span>

<span data-ttu-id="afc0e-107">Dans ce didacticiel, vous allez créer une application console qui accepte les noms de fichiers d’entrée et de sortie comme arguments.</span><span class="sxs-lookup"><span data-stu-id="afc0e-107">In this tutorial, you will create a console application that takes the input and output filenames as arguments.</span></span> <span data-ttu-id="afc0e-108">L’application obtient les exemples de supports non compressés à partir d’une application d’analyse de fichiers wave, qui est fournie dans ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="afc0e-108">The application gets the uncompressed media samples from a wave file parsing application, which is provided with this tutorial.</span></span> <span data-ttu-id="afc0e-109">Ces exemples sont envoyés à l’encodeur pour la conversion au format Windows Media Audio 9.</span><span class="sxs-lookup"><span data-stu-id="afc0e-109">These samples are sent to the encoder for conversion to Windows Media Audio 9 format.</span></span> <span data-ttu-id="afc0e-110">L’encodeur est configuré pour l’encodage CBR et utilise le premier taux de bits disponible pendant la négociation de type de média comme vitesse de transmission cible.</span><span class="sxs-lookup"><span data-stu-id="afc0e-110">The encoder is configured for CBR encoding and uses the first bit rate available during media type negotiation as the target bit rate.</span></span> <span data-ttu-id="afc0e-111">Les exemples encodés sont envoyés au multiplexeur pour la transmission de paquets au format de données ASF.</span><span class="sxs-lookup"><span data-stu-id="afc0e-111">The encoded samples are sent to the multiplexer for packetization in ASF data format.</span></span> <span data-ttu-id="afc0e-112">Ces paquets sont écrits dans un flux d’octets qui représente l’objet de données ASF.</span><span class="sxs-lookup"><span data-stu-id="afc0e-112">These packets will be written to a byte stream that represents the ASF Data Object.</span></span> <span data-ttu-id="afc0e-113">Une fois la section des données prête, vous allez créer un fichier audio ASF et écrire le nouvel objet d’en-tête ASF qui consolide toutes les informations d’en-tête, puis ajouter le flux d’octets de l’objet de données ASF.</span><span class="sxs-lookup"><span data-stu-id="afc0e-113">After the data section is ready, you will create an ASF audio file and write the new ASF Header Object that consolidates all the header information and then append the ASF Data Object byte stream.</span></span>

<span data-ttu-id="afc0e-114">Ce didacticiel contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="afc0e-114">This tutorial contains the following sections:</span></span>

-   [<span data-ttu-id="afc0e-115">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="afc0e-115">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="afc0e-116">Terminologie</span><span class="sxs-lookup"><span data-stu-id="afc0e-116">Terminology</span></span>](#terminology)
-   [<span data-ttu-id="afc0e-117">1. configurer le projet</span><span class="sxs-lookup"><span data-stu-id="afc0e-117">1. Set up the Project</span></span>](#1-set-up-the-project)
-   [<span data-ttu-id="afc0e-118">2. déclarer des fonctions d’assistance</span><span class="sxs-lookup"><span data-stu-id="afc0e-118">2. Declare Helper Functions</span></span>](#2-declare-helper-functions)
-   [<span data-ttu-id="afc0e-119">3. ouvrir un fichier audio</span><span class="sxs-lookup"><span data-stu-id="afc0e-119">3. Open an Audio File</span></span>](#3-open-an-audio-file)
-   [<span data-ttu-id="afc0e-120">4. configurer l’encodeur</span><span class="sxs-lookup"><span data-stu-id="afc0e-120">4. Configure the Encoder</span></span>](#4-configure-the-encoder)
-   [<span data-ttu-id="afc0e-121">5. Créez l’objet ASF ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="afc0e-121">5. Create the ASF ContentInfo object.</span></span>](#5-create-the-asf-contentinfo-object)
-   [<span data-ttu-id="afc0e-122">6. créer le multiplexeur ASF</span><span class="sxs-lookup"><span data-stu-id="afc0e-122">6. Create the ASF Multiplexer</span></span>](#6-create-the-asf-multiplexer)
-   [<span data-ttu-id="afc0e-123">7. générer de nouveaux paquets de données ASF</span><span class="sxs-lookup"><span data-stu-id="afc0e-123">7. Generate New ASF Data Packets</span></span>](#7-generate-new-asf-data-packets)
-   [<span data-ttu-id="afc0e-124">8. écrire le fichier ASF</span><span class="sxs-lookup"><span data-stu-id="afc0e-124">8. Write the ASF File</span></span>](#8-write-the-asf-file)
-   [<span data-ttu-id="afc0e-125">9. définir la fonction Entry-Point</span><span class="sxs-lookup"><span data-stu-id="afc0e-125">9. Define the Entry-Point Function</span></span>](#9-define-the-entry-point-function)
-   [<span data-ttu-id="afc0e-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="afc0e-126">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="afc0e-127">Prérequis</span><span class="sxs-lookup"><span data-stu-id="afc0e-127">Prerequisites</span></span>

<span data-ttu-id="afc0e-128">Ce didacticiel part des principes suivants :</span><span class="sxs-lookup"><span data-stu-id="afc0e-128">This tutorial assumes the following:</span></span>

-   <span data-ttu-id="afc0e-129">Vous êtes familiarisé avec la structure d’un fichier ASF et les composants fournis par Media Foundation pour travailler avec des objets ASF.</span><span class="sxs-lookup"><span data-stu-id="afc0e-129">You are familiar with the structure of an ASF file and the components provided by Media Foundation to work with ASF Objects.</span></span> <span data-ttu-id="afc0e-130">Ces composants incluent les objets ContentInfo, Splitter, multiplexer et Profile.</span><span class="sxs-lookup"><span data-stu-id="afc0e-130">These components include ContentInfo, splitter, multiplexer, and profile objects.</span></span> <span data-ttu-id="afc0e-131">Pour plus d’informations, consultez [WMCONTAINER ASF Components](wmcontainer-asf-components.md).</span><span class="sxs-lookup"><span data-stu-id="afc0e-131">For more information, see [WMContainer ASF Components](wmcontainer-asf-components.md).</span></span>
-   <span data-ttu-id="afc0e-132">Vous êtes familiarisé avec les encodeurs Windows Media et les différents types d’encodage, particulièrement CBR.</span><span class="sxs-lookup"><span data-stu-id="afc0e-132">You are familiar with Windows Media encoders, and the various encoding types, particularly CBR.</span></span> <span data-ttu-id="afc0e-133">Pour plus d’informations, consultez [encodeurs Windows Media](windows-media-encoders.md) .</span><span class="sxs-lookup"><span data-stu-id="afc0e-133">For more information, see [Windows Media Encoders](windows-media-encoders.md) .</span></span>
-   <span data-ttu-id="afc0e-134">Vous êtes familiarisé avec les [mémoires tampons de média](media-buffers.md) et les flux d’octets : en particulier, les opérations de fichier utilisant un flux d’octets et l’écriture du contenu d’une mémoire tampon de média dans un flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="afc0e-134">You are familiar with [Media Buffers](media-buffers.md) and byte streams: Specifically, file operations using a byte stream, and writing the contents of a media buffer to a byte stream.</span></span>

## <a name="terminology"></a><span data-ttu-id="afc0e-135">Terminologie</span><span class="sxs-lookup"><span data-stu-id="afc0e-135">Terminology</span></span>

<span data-ttu-id="afc0e-136">Ce didacticiel utilise les termes suivants :</span><span class="sxs-lookup"><span data-stu-id="afc0e-136">This tutorial uses the following terms:</span></span>

-   <span data-ttu-id="afc0e-137">Type de média source : objet de type de média, expose l’interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , qui décrit le contenu du fichier d’entrée.</span><span class="sxs-lookup"><span data-stu-id="afc0e-137">Source media type: Media type object, exposes [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface, which describes the contents of the input file.</span></span>
-   <span data-ttu-id="afc0e-138">Profil audio : objet de profil, expose l’interface [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) , qui contient uniquement les flux audio du fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="afc0e-138">Audio profile: Profile object, exposes [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface, which contains only audio streams of the output file.</span></span>
-   <span data-ttu-id="afc0e-139">Exemple de flux : exemple de support, qui expose l’interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , représente les données multimédia du fichier d’entrée obtenues à partir de l’encodeur dans un État compressé.</span><span class="sxs-lookup"><span data-stu-id="afc0e-139">Stream sample: Media sample, exposes [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, represents the input file's media data obtained from the encoder in a compressed state.</span></span>
-   <span data-ttu-id="afc0e-140">Objet ContentInfo : [objet ASF ContentInfo](asf-contentinfo-object.md), qui expose l’interface [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) , qui représente l’objet d’en-tête ASF du fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="afc0e-140">ContentInfo object: [ASF ContentInfo Object](asf-contentinfo-object.md), exposes [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface, which represents the ASF Header Object of the output file.</span></span>
-   <span data-ttu-id="afc0e-141">Flux d’octets de données : objet de flux d’octets, expose l’interface [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , qui représente la partie entière de l’objet de données ASF du fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="afc0e-141">Data byte stream: Byte stream object, exposes [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface, which represents the entire ASF Data Object portion of the output file.</span></span>
-   <span data-ttu-id="afc0e-142">Paquet de données : exemple de support, expose l’interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , générée par le [multiplexeur ASF](asf-multiplexer.md); représente un paquet de données ASF qui sera écrit dans le flux d’octets de données.</span><span class="sxs-lookup"><span data-stu-id="afc0e-142">Data packet: Media sample, exposes [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, generated by the [ASF Multiplexer](asf-multiplexer.md); represents an ASF data packet that will be written to the data byte stream.</span></span>
-   <span data-ttu-id="afc0e-143">Sortie d’octet de sortie : objet de flux d’octets, expose l’interface [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , qui contient le contenu du fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="afc0e-143">Output byte stream: Byte stream object, exposes [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface, which contains the contents of the output file.</span></span>

## <a name="1-set-up-the-project"></a><span data-ttu-id="afc0e-144">1. configurer le projet</span><span class="sxs-lookup"><span data-stu-id="afc0e-144">1. Set up the Project</span></span>

1.  <span data-ttu-id="afc0e-145">Incluez les en-têtes suivants dans votre fichier source :</span><span class="sxs-lookup"><span data-stu-id="afc0e-145">Include the following headers in your source file:</span></span>

    ```C++
    #include <new>
    #include <stdio.h>       // Standard I/O
    #include <windows.h>     // Windows headers
    #include <mfapi.h>       // Media Foundation platform
    #include <wmcontainer.h> // ASF interfaces
    #include <mferror.h>     // Media Foundation error codes
    ```

    

2.  <span data-ttu-id="afc0e-146">Lien vers les fichiers de bibliothèque suivants :</span><span class="sxs-lookup"><span data-stu-id="afc0e-146">Link to the following library files:</span></span>

    -   <span data-ttu-id="afc0e-147">mfplat. lib</span><span class="sxs-lookup"><span data-stu-id="afc0e-147">mfplat.lib</span></span>
    -   <span data-ttu-id="afc0e-148">MF. lib</span><span class="sxs-lookup"><span data-stu-id="afc0e-148">mf.lib</span></span>
    -   <span data-ttu-id="afc0e-149">mfuuid. lib</span><span class="sxs-lookup"><span data-stu-id="afc0e-149">mfuuid.lib</span></span>

3.  <span data-ttu-id="afc0e-150">Déclarez la fonction [SafeRelease](saferelease.md) .</span><span class="sxs-lookup"><span data-stu-id="afc0e-150">Declare the [SafeRelease](saferelease.md) function.</span></span>
4.  <span data-ttu-id="afc0e-151">Incluez la classe CWmaEncoder dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="afc0e-151">Include the CWmaEncoder class in your project.</span></span> <span data-ttu-id="afc0e-152">Pour obtenir le code source complet de cette classe, consultez [exemple de code d’encodeur](encoder-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="afc0e-152">For the complete source code of this class, see [Encoder Example Code](encoder-example-code.md).</span></span>

## <a name="2-declare-helper-functions"></a><span data-ttu-id="afc0e-153">2. déclarer des fonctions d’assistance</span><span class="sxs-lookup"><span data-stu-id="afc0e-153">2. Declare Helper Functions</span></span>

<span data-ttu-id="afc0e-154">Ce didacticiel utilise les fonctions d’assistance suivantes pour lire et écrire à partir d’un flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="afc0e-154">This tutorial uses the following helper functions to read and write from a byte stream.</span></span>

-   <span data-ttu-id="afc0e-155">`AppendToByteStream`: Ajoute le contenu d’un flux d’octets à un autre flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="afc0e-155">`AppendToByteStream`: Appends the contents of one byte stream to another byte stream.</span></span>
-   <span data-ttu-id="afc0e-156">WriteBufferToByteStream : écrit les données d’une mémoire tampon de média dans un flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="afc0e-156">WriteBufferToByteStream: Writes data from a media buffer to a byte stream.</span></span>

<span data-ttu-id="afc0e-157">Pour plus d’informations, consultez [**IMFByteStream :: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span><span class="sxs-lookup"><span data-stu-id="afc0e-157">For more information, see [**IMFByteStream::Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span></span> <span data-ttu-id="afc0e-158">Le code suivant illustre ces fonctions d’assistance :</span><span class="sxs-lookup"><span data-stu-id="afc0e-158">The following code shows these helper functions:</span></span>


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



## <a name="3-open-an-audio-file"></a><span data-ttu-id="afc0e-159">3. ouvrir un fichier audio</span><span class="sxs-lookup"><span data-stu-id="afc0e-159">3. Open an Audio File</span></span>

<span data-ttu-id="afc0e-160">Ce didacticiel part du principe que votre application génère un fichier audio non compressé pour l’encodage.</span><span class="sxs-lookup"><span data-stu-id="afc0e-160">This tutorial assumes that your application will generate uncompressed audio for encoding.</span></span> <span data-ttu-id="afc0e-161">À cet effet, deux fonctions sont déclarées dans ce didacticiel :</span><span class="sxs-lookup"><span data-stu-id="afc0e-161">For that purpose, two functions are declared in this tutorial:</span></span>


```C++
HRESULT OpenAudioFile(PCWSTR pszURL, IMFMediaType **ppAudioFormat);
HRESULT GetNextAudioSample(BOOL *pbEOS, IMFSample **ppSample);
```



<span data-ttu-id="afc0e-162">L’implémentation de ces fonctions est laissée au lecteur.</span><span class="sxs-lookup"><span data-stu-id="afc0e-162">The implementation of these functions is left to the reader.</span></span>

-   <span data-ttu-id="afc0e-163">La `OpenAudioFile` fonction doit ouvrir le fichier multimédia spécifié par *pszURL* et retourner un pointeur vers un type de média qui décrit un flux audio.</span><span class="sxs-lookup"><span data-stu-id="afc0e-163">The `OpenAudioFile` function should open the media file specified by *pszURL* and return a pointer to a media type that describes an audio stream.</span></span>
-   <span data-ttu-id="afc0e-164">La `GetNextAudioSample` fonction doit lire le fichier audio PCM non compressé à partir du fichier qui a été ouvert par `OpenAudioFile` .</span><span class="sxs-lookup"><span data-stu-id="afc0e-164">The `GetNextAudioSample` function should read uncompressed PCM audio from the file that was opened by `OpenAudioFile`.</span></span> <span data-ttu-id="afc0e-165">Lorsque la fin du fichier est atteinte, *pbEOS* reçoit la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="afc0e-165">When the end of the file is reached, *pbEOS* receives the value **TRUE**.</span></span> <span data-ttu-id="afc0e-166">Sinon, *ppSample* reçoit un exemple de support qui contient la mémoire tampon audio.</span><span class="sxs-lookup"><span data-stu-id="afc0e-166">Otherwise, *ppSample* receives a media sample that contains the audio buffer.</span></span>

## <a name="4-configure-the-encoder"></a><span data-ttu-id="afc0e-167">4. configurer l’encodeur</span><span class="sxs-lookup"><span data-stu-id="afc0e-167">4. Configure the Encoder</span></span>

<span data-ttu-id="afc0e-168">Ensuite, créez l’encodeur, configurez-le pour produire des exemples de flux encodés CBR et négociez les types de médias d’entrée et de sortie.</span><span class="sxs-lookup"><span data-stu-id="afc0e-168">Next, create the encoder, configure it to produce CBR-encoded stream samples, and negotiate the input and the output media types.</span></span>

<span data-ttu-id="afc0e-169">Dans Media Foundation, les encodeurs (exposent l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) ) sont implémentés en tant que [Media Foundation des transformations](media-foundation-transforms.md) (MFT).</span><span class="sxs-lookup"><span data-stu-id="afc0e-169">In Media Foundation, encoders (expose the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface) are implemented as [Media Foundation Transforms](media-foundation-transforms.md) (MFT).</span></span>

<span data-ttu-id="afc0e-170">Dans ce didacticiel, l’encodeur est implémenté dans la `CWmaEncoder` classe qui fournit un wrapper pour la table MFT.</span><span class="sxs-lookup"><span data-stu-id="afc0e-170">In this tutorial, the encoder is implemented in the `CWmaEncoder` class that provides a wrapper for the MFT.</span></span> <span data-ttu-id="afc0e-171">Pour obtenir le code source complet de cette classe, consultez [exemple de code d’encodeur](encoder-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="afc0e-171">For the complete source code of this class, see [Encoder Example Code](encoder-example-code.md).</span></span>

> [!Note]  
> <span data-ttu-id="afc0e-172">Vous pouvez éventuellement spécifier le type d’encodage CBR.</span><span class="sxs-lookup"><span data-stu-id="afc0e-172">You can optionally specify the encoding type as CBR.</span></span> <span data-ttu-id="afc0e-173">Par défaut, l’encodeur est configuré pour utiliser l’encodage CBR.</span><span class="sxs-lookup"><span data-stu-id="afc0e-173">By default, the encoder is configured to use CBR encoding.</span></span> <span data-ttu-id="afc0e-174">Pour plus d’informations, consultez [encodage à taux binaire constant](constant-bit-rate-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="afc0e-174">For more information, see [Constant Bit Rate Encoding](constant-bit-rate-encoding.md).</span></span> <span data-ttu-id="afc0e-175">Vous pouvez définir des propriétés supplémentaires en fonction du type d’encodage, pour obtenir des informations sur les propriétés qui sont spécifiques à un mode d’encodage, consultez encodage à taux binaire [variable basé](quality-based-variable-bit-rate--vbr--encoding.md)sur la qualité, encodage à vitesse de transmission variable non [contrainte](unconstrained-variable-bit-rate--vbr--encoding.md)et [codage à vitesse de transmission variable à contrainte maximale](peak-constrained-variable-bit-rate--vbr--encoding.md).</span><span class="sxs-lookup"><span data-stu-id="afc0e-175">You can set additional properties depending on the type of encoding, for information about the properties that are specific to an encoding mode, see [Quality-Based Variable Bit Rate Encoding](quality-based-variable-bit-rate--vbr--encoding.md), [Unconstrained Variable Bit Rate Encoding](unconstrained-variable-bit-rate--vbr--encoding.md), and [Peak-Constrained Variable Bit Rate Encoding](peak-constrained-variable-bit-rate--vbr--encoding.md).</span></span>

 


```C++
    CWmaEncoder* pEncoder = NULL; //Pointer to the Encoder object.

    hr = OpenAudioFile(sInputFileName, &pInputType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Initialize the WMA encoder wrapper.

    pEncoder = new (std::nothrow) CWmaEncoder();
    if (pEncoder == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pEncoder->Initialize();
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetEncodingType(EncodeMode_CBR);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetInputType(pInputType);
    if (FAILED(hr))
    {
        goto done;
    }
```



## <a name="5-create-the-asf-contentinfo-object"></a><span data-ttu-id="afc0e-176">5. Créez l’objet ASF ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="afc0e-176">5. Create the ASF ContentInfo object.</span></span>

<span data-ttu-id="afc0e-177">L' [objet ASF ContentInfo](asf-contentinfo-object.md) contient des informations sur les différents objets d’en-tête du fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="afc0e-177">The [ASF ContentInfo Object](asf-contentinfo-object.md) contains information about the various header objects of the output file.</span></span>

<span data-ttu-id="afc0e-178">Tout d’abord, créez un profil ASF pour le flux audio :</span><span class="sxs-lookup"><span data-stu-id="afc0e-178">First, create an ASF profile for the audio stream:</span></span>

1.  <span data-ttu-id="afc0e-179">Appelez [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) pour créer un objet de profil ASF vide.</span><span class="sxs-lookup"><span data-stu-id="afc0e-179">Call [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) to create an empty ASF profile object.</span></span> <span data-ttu-id="afc0e-180">Le profil ASF expose l’interface [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) .</span><span class="sxs-lookup"><span data-stu-id="afc0e-180">The ASF profile exposes the [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface.</span></span> <span data-ttu-id="afc0e-181">Pour plus d’informations, consultez [création et configuration de flux ASF](creating-and-configuring-asf-streams.md).</span><span class="sxs-lookup"><span data-stu-id="afc0e-181">For more information, see [Creating and Configuring ASF Streams](creating-and-configuring-asf-streams.md).</span></span>
2.  <span data-ttu-id="afc0e-182">Obtient le format audio encodé à partir de l' `CWmaEncoder` objet.</span><span class="sxs-lookup"><span data-stu-id="afc0e-182">Get the encoded audio format from the `CWmaEncoder` object.</span></span>
3.  <span data-ttu-id="afc0e-183">Appelez [**IMFASFProfile :: CreateStream,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) pour créer un flux pour le profil ASF.</span><span class="sxs-lookup"><span data-stu-id="afc0e-183">Call [**IMFASFProfile::CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) to create a new stream for the ASF profile.</span></span> <span data-ttu-id="afc0e-184">Transmettez un pointeur vers l’interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , qui représente le format de flux.</span><span class="sxs-lookup"><span data-stu-id="afc0e-184">Pass in a pointer to the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface, which represents the stream format.</span></span>
4.  <span data-ttu-id="afc0e-185">Appelez [**IMFASFStreamConfig :: SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) pour assigner un identificateur de flux.</span><span class="sxs-lookup"><span data-stu-id="afc0e-185">Call [**IMFASFStreamConfig::SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) to assign a stream identifier.</span></span>
5.  <span data-ttu-id="afc0e-186">Définissez les paramètres de la « plage perdue » en définissant l’attribut [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) sur l’objet de flux.</span><span class="sxs-lookup"><span data-stu-id="afc0e-186">Set the "leaky bucket" parameters by setting the [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) attribute on the stream object.</span></span>
6.  <span data-ttu-id="afc0e-187">Appelez [**IMFASFProfile :: SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) pour ajouter le nouveau flux au profil.</span><span class="sxs-lookup"><span data-stu-id="afc0e-187">Call [**IMFASFProfile::SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) to add the new stream to the profile.</span></span>

<span data-ttu-id="afc0e-188">Créez maintenant l’objet ASF ContentInfo comme suit :</span><span class="sxs-lookup"><span data-stu-id="afc0e-188">Now create the ASF ContentInfo object as follows:</span></span>

1.  <span data-ttu-id="afc0e-189">Appelez [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) pour créer un objet ContentInfo vide.</span><span class="sxs-lookup"><span data-stu-id="afc0e-189">Call [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) to create an empty ContentInfo object.</span></span>
2.  <span data-ttu-id="afc0e-190">Appelez [**IMFASFContentInfo :: SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) pour définir le profil ASF.</span><span class="sxs-lookup"><span data-stu-id="afc0e-190">Call [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) to set the ASF profile.</span></span>

<span data-ttu-id="afc0e-191">Le code suivant illustre ces étapes :</span><span class="sxs-lookup"><span data-stu-id="afc0e-191">The following code shows these steps:</span></span>


```C++
HRESULT CreateASFContentInfo(
    CWmaEncoder* pEncoder,
    IMFASFContentInfo** ppContentInfo
    )
{
    HRESULT hr = S_OK;
    
    IMFASFProfile* pProfile = NULL;
    IMFMediaType* pMediaType = NULL;
    IMFASFStreamConfig* pStream = NULL;
    IMFASFContentInfo* pContentInfo = NULL;

    // Create the ASF profile object.

    hr = MFCreateASFProfile(&pProfile); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a stream description for the encoded audio.

    hr = pEncoder->GetOutputType(&pMediaType); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProfile->CreateStream(pMediaType, &pStream); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pStream->SetStreamNumber(DEFAULT_STREAM_NUMBER); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Set "leaky bucket" values.

    LeakyBucket bucket;

    hr = pEncoder->GetLeakyBucket1(&bucket);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pStream->SetBlob(
        MF_ASFSTREAMCONFIG_LEAKYBUCKET1, 
        (UINT8*)&bucket, 
        sizeof(bucket)
        );

    if (FAILED(hr))
    {
        goto done;
    }

    //Add the stream to the profile

    hr = pProfile->SetStream(pStream);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the ASF ContentInfo object.

    hr = MFCreateASFContentInfo(&pContentInfo); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pContentInfo->SetProfile(pProfile); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.

    *ppContentInfo = pContentInfo;
    (*ppContentInfo)->AddRef();

done:
    SafeRelease(&pProfile);
    SafeRelease(&pStream);
    SafeRelease(&pMediaType);
    SafeRelease(&pContentInfo);
    return hr;
}
```



## <a name="6-create-the-asf-multiplexer"></a><span data-ttu-id="afc0e-192">6. créer le multiplexeur ASF</span><span class="sxs-lookup"><span data-stu-id="afc0e-192">6. Create the ASF Multiplexer</span></span>

<span data-ttu-id="afc0e-193">Le [multiplexeur ASF](asf-multiplexer.md) génère des paquets de données ASF.</span><span class="sxs-lookup"><span data-stu-id="afc0e-193">The [ASF Multiplexer](asf-multiplexer.md) generates ASF data packets.</span></span>

1.  <span data-ttu-id="afc0e-194">Appelez [**MFCreateASFMultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer) pour créer le multiplexeur ASF.</span><span class="sxs-lookup"><span data-stu-id="afc0e-194">Call [**MFCreateASFMultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer) to create the ASF multiplexer.</span></span>
2.  <span data-ttu-id="afc0e-195">Appelez [**IMFASFMultiplexer :: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) pour initialiser le multiplexeur.</span><span class="sxs-lookup"><span data-stu-id="afc0e-195">Call [**IMFASFMultiplexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) to initialize the multiplexer.</span></span> <span data-ttu-id="afc0e-196">Transmettez un pointeur vers l’objet d’informations de contenu ASF qui a été créé dans la section précédente.</span><span class="sxs-lookup"><span data-stu-id="afc0e-196">Pass in a pointer to the ASF Content Info object, which was created in the previous section.</span></span>
3.  <span data-ttu-id="afc0e-197">Appelez [**IMFASFMultiplexer :: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) pour définir l’indicateur de **\_ vitesse de \_ \_ transmission du multiplexeur MFASF** .</span><span class="sxs-lookup"><span data-stu-id="afc0e-197">Call [**IMFASFMultiplexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) to set the **MFASF\_MULTIPLEXER\_AUTOADJUST\_BITRATE** flag.</span></span> <span data-ttu-id="afc0e-198">Lorsque ce paramètre est utilisé, le multiplexeur ajuste automatiquement la vitesse de transmission du contenu ASF pour qu’il corresponde aux caractéristiques des flux en cours de multiplexage.</span><span class="sxs-lookup"><span data-stu-id="afc0e-198">When this setting is used, the multiplexer automatically adjusts the bit rate of the ASF content to match the characteristics of the streams being multiplexed.</span></span>


```C++
HRESULT CreateASFMux( 
    IMFASFContentInfo* pContentInfo,
    IMFASFMultiplexer** ppMultiplexer
    )
{
    HRESULT hr = S_OK;
    
    IMFMediaType* pMediaType = NULL;
    IMFASFMultiplexer *pMultiplexer = NULL;

    // Create and initialize the ASF Multiplexer object.

    hr = MFCreateASFMultiplexer(&pMultiplexer);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pMultiplexer->Initialize(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    // Enable automatic bit-rate adjustment.

    hr = pMultiplexer->SetFlags(MFASF_MULTIPLEXER_AUTOADJUST_BITRATE);
    if (FAILED(hr))
    {
        goto done;
    }

    *ppMultiplexer = pMultiplexer;
    (*ppMultiplexer)->AddRef();

done:
    SafeRelease(&pMultiplexer);
    return hr;
}
```



## <a name="7-generate-new-asf-data-packets"></a><span data-ttu-id="afc0e-199">7. générer de nouveaux paquets de données ASF</span><span class="sxs-lookup"><span data-stu-id="afc0e-199">7. Generate New ASF Data Packets</span></span>

<span data-ttu-id="afc0e-200">Générez ensuite des paquets de données ASF pour le nouveau fichier.</span><span class="sxs-lookup"><span data-stu-id="afc0e-200">Next, generate ASF data packets for the new file.</span></span> <span data-ttu-id="afc0e-201">Ces paquets de données constituent l’objet de données ASF final pour le nouveau fichier.</span><span class="sxs-lookup"><span data-stu-id="afc0e-201">These data packets will constitute the final ASF Data Object for the new file.</span></span> <span data-ttu-id="afc0e-202">Pour générer de nouveaux paquets de données ASF :</span><span class="sxs-lookup"><span data-stu-id="afc0e-202">To generate new ASF data packets:</span></span>

1.  <span data-ttu-id="afc0e-203">Appelez [**MFCreateTempFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatetempfile) pour créer un flux d’octets temporaire qui contiendra les paquets de données ASF.</span><span class="sxs-lookup"><span data-stu-id="afc0e-203">Call [**MFCreateTempFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatetempfile) to create a temporary byte stream to hold the ASF data packets.</span></span>
2.  <span data-ttu-id="afc0e-204">Appelez la fonction définie par l’application `GetNextAudioSample` pour obtenir des données audio non compressées pour l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="afc0e-204">Call the application-defined `GetNextAudioSample` function to get uncompressed audio data for the encoder.</span></span>
3.  <span data-ttu-id="afc0e-205">Transmettez l’audio non compressé à l’encodeur pour la compression.</span><span class="sxs-lookup"><span data-stu-id="afc0e-205">Pass the uncompressed audio to the encoder for compression.</span></span> <span data-ttu-id="afc0e-206">Pour plus d’informations, consultez [traitement des données dans l’encodeur](processing-data-in-the-encoder.md) .</span><span class="sxs-lookup"><span data-stu-id="afc0e-206">For more information, see [Processing Data in the Encoder](processing-data-in-the-encoder.md)</span></span>
4.  <span data-ttu-id="afc0e-207">Appelez [**IMFASFMultiplexer ::P rocesssample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) pour envoyer les échantillons audio compressés au multiplexeur ASF en vue de la paquetage.</span><span class="sxs-lookup"><span data-stu-id="afc0e-207">Call [**IMFASFMultiplexer::ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) to send the compressed audio samples to the ASF multiplexer for packetization.</span></span>
5.  <span data-ttu-id="afc0e-208">Récupérez les paquets ASF du multiplexeur et écrivez-les dans le flux d’octets temporaire.</span><span class="sxs-lookup"><span data-stu-id="afc0e-208">Get the ASF packets from the multiplexer and write them to the temporary byte stream.</span></span> <span data-ttu-id="afc0e-209">Pour plus d’informations, consultez [génération de nouveaux paquets de données ASF](generating-new-asf-data-packets.md).</span><span class="sxs-lookup"><span data-stu-id="afc0e-209">For more information, see [Generating New ASF Data Packets](generating-new-asf-data-packets.md).</span></span>
6.  <span data-ttu-id="afc0e-210">Lorsque vous atteignez la fin du flux source, drainez l’encodeur et tirez les échantillons compressés restants à partir de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="afc0e-210">When you reach the end of the source stream, drain the encoder and pull the remaining compressed samples from the encoder.</span></span> <span data-ttu-id="afc0e-211">Pour plus d’informations sur la vidange d’une table MFT, consultez [modèle de traitement MFT de base](basic-mft-processing-model.md).</span><span class="sxs-lookup"><span data-stu-id="afc0e-211">For more information about draining an MFT, see [Basic MFT Processing Model](basic-mft-processing-model.md).</span></span>
7.  <span data-ttu-id="afc0e-212">Une fois tous les exemples envoyés au multiplexeur, appelez [**IMFASFMultiplexer :: Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) et tirez les paquets ASF restants à partir du multiplexeur.</span><span class="sxs-lookup"><span data-stu-id="afc0e-212">After all samples are sent to the multiplexer, call [**IMFASFMultiplexer::Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) and pull the remaining ASF packets from the multiplexer.</span></span>
8.  <span data-ttu-id="afc0e-213">Appelez [**IMFASFMultiplexer :: end**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end).</span><span class="sxs-lookup"><span data-stu-id="afc0e-213">Call [**IMFASFMultiplexer::End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end).</span></span>

<span data-ttu-id="afc0e-214">Le code suivant génère des paquets de données ASF.</span><span class="sxs-lookup"><span data-stu-id="afc0e-214">The following code generates ASF data packets.</span></span> <span data-ttu-id="afc0e-215">La fonction retourne un pointeur vers un flux d’octets qui contient l’objet de données ASF.</span><span class="sxs-lookup"><span data-stu-id="afc0e-215">The function returns a pointer to a byte stream that contains the ASF Data Object.</span></span>


```C++
HRESULT EncodeData(
    CWmaEncoder* pEncoder, 
    IMFASFContentInfo* pContentInfo,
    IMFASFMultiplexer* pMux, 
    IMFByteStream** ppDataStream) 
{
    HRESULT hr = S_OK;

    IMFByteStream* pStream = NULL;
    IMFSample* pInputSample = NULL;
    IMFSample* pWmaSample = NULL;

    BOOL bEOF = FALSE;

   // Create a temporary file to hold the data stream.
   hr = MFCreateTempFile(
        MF_ACCESSMODE_READWRITE, 
        MF_OPENMODE_DELETE_IF_EXIST,
        MF_FILEFLAGS_NONE,
        &pStream
        );

   if (FAILED(hr))
   {
       goto done;
   }

    BOOL bNeedInput = TRUE;

    while (TRUE)
    {
        if (bNeedInput)
        {
            hr = GetNextAudioSample(&bEOF, &pInputSample);
            if (FAILED(hr))
            {
                goto done;
            }

            if (bEOF)
            {
                // Reached the end of the input file.
                break;
            }

            // Encode the uncompressed audio sample.
            hr = pEncoder->ProcessInput(pInputSample);
            if (FAILED(hr))
            {
                goto done;
            }

            bNeedInput = FALSE;
        }

        if (bNeedInput == FALSE)
        {
            // Get data from the encoder.

            hr = pEncoder->ProcessOutput(&pWmaSample);
            if (FAILED(hr))
            {
                goto done;
            }

            // pWmaSample can be NULL if the encoder needs more input.

            if (pWmaSample)
            {
                hr = pMux->ProcessSample(DEFAULT_STREAM_NUMBER, pWmaSample, 0);
                if (FAILED(hr))
                {
                    goto done;
                }

                //Collect the data packets and write them to a stream
                hr = GenerateASFDataPackets(pMux, pStream);
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            else
            {
                bNeedInput = TRUE;
            }
        }
        
        SafeRelease(&pInputSample);
        SafeRelease(&pWmaSample);
    }

    // Drain the MFT and pull any remaining samples from the encoder.

    hr = pEncoder->Drain();
    if (FAILED(hr))
    {
        goto done;
    }

    while (TRUE)
    {
        hr = pEncoder->ProcessOutput(&pWmaSample);
        if (FAILED(hr))
        {
            goto done;
        }

        if (pWmaSample == NULL)
        {
            break;
        }

        hr = pMux->ProcessSample(DEFAULT_STREAM_NUMBER, pWmaSample, 0);
        if (FAILED(hr))
        {
            goto done;
        }

        //Collect the data packets and write them to a stream
        hr = GenerateASFDataPackets(pMux, pStream);
        if (FAILED(hr))
        {
            goto done;
        }

        SafeRelease(&pWmaSample);
    }

    // Flush the mux and get any pending ASF data packets.
    hr = pMux->Flush();
    if (FAILED(hr))
    {
        goto done;
    }

    hr = GenerateASFDataPackets(pMux, pStream);
    if (FAILED(hr))
    {
        goto done;
    }
    
    // Update the ContentInfo object
    hr = pMux->End(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    //Return stream to the caller that contains the ASF encoded data.
    *ppDataStream = pStream;
    (*ppDataStream)->AddRef();

done:
    SafeRelease(&pStream);
    SafeRelease(&pInputSample);
    SafeRelease(&pWmaSample);
    return hr;
}
```



<span data-ttu-id="afc0e-216">Le code de la `GenerateASFDataPackets` fonction est affiché dans la rubrique [génération de nouveaux paquets de données ASF](generating-new-asf-data-packets.md).</span><span class="sxs-lookup"><span data-stu-id="afc0e-216">Code for the `GenerateASFDataPackets` function is shown in the topic [Generating New ASF Data Packets](generating-new-asf-data-packets.md).</span></span>

## <a name="8-write-the-asf-file"></a><span data-ttu-id="afc0e-217">8. écrire le fichier ASF</span><span class="sxs-lookup"><span data-stu-id="afc0e-217">8. Write the ASF File</span></span>

<span data-ttu-id="afc0e-218">Ensuite, écrivez l’en-tête ASF dans une mémoire tampon de média en appelant [**IMFASFContentInfo :: GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader).</span><span class="sxs-lookup"><span data-stu-id="afc0e-218">Next, write the ASF header to a media buffer by calling [**IMFASFContentInfo::GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader).</span></span> <span data-ttu-id="afc0e-219">Cette méthode convertit les données stockées dans l’objet ContentInfo en données binaires au format d’objet d’en-tête ASF.</span><span class="sxs-lookup"><span data-stu-id="afc0e-219">This method converts data stored in the ContentInfo object into binary data in ASF Header Object format.</span></span> <span data-ttu-id="afc0e-220">Pour plus d’informations, consultez [génération d’un nouvel objet d’en-tête ASF](generating-a-new-asf-header-object.md).</span><span class="sxs-lookup"><span data-stu-id="afc0e-220">For more information, see [Generating a New ASF Header Object](generating-a-new-asf-header-object.md).</span></span>

<span data-ttu-id="afc0e-221">Une fois que le nouvel objet d’en-tête ASF a été généré, créez un flux d’octets pour le fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="afc0e-221">After the new ASF Header Object has been generated, create a byte stream for the output file.</span></span> <span data-ttu-id="afc0e-222">Tout d’abord, écrivez l’objet d’en-tête dans le flux d’octets de sortie.</span><span class="sxs-lookup"><span data-stu-id="afc0e-222">First write the Header Object to the output byte stream.</span></span> <span data-ttu-id="afc0e-223">Suivez l’objet d’en-tête avec l’objet de données contenu dans le flux d’octets de données.</span><span class="sxs-lookup"><span data-stu-id="afc0e-223">Follow the Header Object with the Data Object contained in the data byte stream.</span></span>


```C++
HRESULT WriteASFFile( 
     IMFASFContentInfo *pContentInfo, 
     IMFByteStream *pDataStream,
     PCWSTR pszFile
     )
{
    HRESULT hr = S_OK;
    
    IMFMediaBuffer* pHeaderBuffer = NULL;
    IMFByteStream* pWmaStream = NULL;

    DWORD cbHeaderSize = 0;
    DWORD cbWritten = 0;

    //Create output file
    hr = MFCreateFile(MF_ACCESSMODE_WRITE, MF_OPENMODE_DELETE_IF_EXIST,
        MF_FILEFLAGS_NONE, pszFile, &pWmaStream);

    if (FAILED(hr))
    {
        goto done;
    }


    // Get the size of the ASF Header Object.
    hr = pContentInfo->GenerateHeader (NULL, &cbHeaderSize);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a media buffer.
    hr = MFCreateMemoryBuffer(cbHeaderSize, &pHeaderBuffer);
    if (FAILED(hr))
    {
        goto done;
    }

    // Populate the media buffer with the ASF Header Object.
    hr = pContentInfo->GenerateHeader(pHeaderBuffer, &cbHeaderSize);
    if (FAILED(hr))
    {
        goto done;
    }

    // Write the ASF header to the output file.
    hr = WriteBufferToByteStream(pWmaStream, pHeaderBuffer, &cbWritten);
    if (FAILED(hr))
    {
        goto done;
    }

    // Append the data stream to the file.

    hr = pDataStream->SetCurrentPosition(0);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = AppendToByteStream(pDataStream, pWmaStream);

done:
    SafeRelease(&pHeaderBuffer);
    SafeRelease(&pWmaStream);
    return hr;
}
```



## <a name="9-define-the-entry-point-function"></a><span data-ttu-id="afc0e-224">9. définir la fonction Entry-Point</span><span class="sxs-lookup"><span data-stu-id="afc0e-224">9. Define the Entry-Point Function</span></span>

<span data-ttu-id="afc0e-225">Vous pouvez maintenant mettre ensemble les étapes précédentes dans une application complète.</span><span class="sxs-lookup"><span data-stu-id="afc0e-225">Now you can put the previous steps together into a complete application.</span></span> <span data-ttu-id="afc0e-226">Avant d’utiliser l’un des objets Media Foundation, initialisez la plateforme Media Foundation en appelant [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span><span class="sxs-lookup"><span data-stu-id="afc0e-226">Before using any of the Media Foundation objects, initialize the Media Foundation platform by calling [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span></span> <span data-ttu-id="afc0e-227">Lorsque vous avez terminé, appelez [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span><span class="sxs-lookup"><span data-stu-id="afc0e-227">When you are done, call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span></span> <span data-ttu-id="afc0e-228">Pour plus d’informations, consultez [initialisation des Media Foundation](initializing-media-foundation.md).</span><span class="sxs-lookup"><span data-stu-id="afc0e-228">For more information, see [Initializing Media Foundation](initializing-media-foundation.md).</span></span>

<span data-ttu-id="afc0e-229">Le code suivant illustre l’application console complète.</span><span class="sxs-lookup"><span data-stu-id="afc0e-229">The following code shows the complete console application.</span></span> <span data-ttu-id="afc0e-230">L’argument de ligne de commande spécifie le nom du fichier à convertir et le nom du nouveau fichier audio.</span><span class="sxs-lookup"><span data-stu-id="afc0e-230">The command-line argument specifies the name of the file to convert and the name of the new audio file.</span></span>


```C++
int wmain(int argc, WCHAR* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc != 3)
    {
        wprintf_s(L"Usage: %s input.wmv, %s output.wma");
        return 0;
    }

    const WCHAR* sInputFileName = argv[1];    // Source file name
    const WCHAR* sOutputFileName = argv[2];  // Output file name
    
    IMFMediaType* pInputType = NULL;
    IMFASFContentInfo* pContentInfo = NULL;
    IMFASFMultiplexer* pMux = NULL;
    IMFByteStream* pDataStream = NULL;

    CWmaEncoder* pEncoder = NULL; //Pointer to the Encoder object.

    HRESULT hr = CoInitializeEx(
        NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);

    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFStartup(MF_VERSION);
    if (FAILED(hr))
    {
        goto done;
    }

    CWmaEncoder* pEncoder = NULL; //Pointer to the Encoder object.

    hr = OpenAudioFile(sInputFileName, &pInputType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Initialize the WMA encoder wrapper.

    pEncoder = new (std::nothrow) CWmaEncoder();
    if (pEncoder == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pEncoder->Initialize();
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetEncodingType(EncodeMode_CBR);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetInputType(pInputType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the WMContainer objects.
    hr = CreateASFContentInfo(pEncoder, &pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CreateASFMux(pContentInfo, &pMux);
    if (FAILED(hr))
    {
        goto done;
    }

    // Convert uncompressed data to ASF format.
    hr = EncodeData(pEncoder, pContentInfo, pMux, &pDataStream);
    if (FAILED(hr))
    {
        goto done;
    }

    // Write the ASF objects to the output file.
    hr = WriteASFFile(pContentInfo, pDataStream, sOutputFileName);

done:
    SafeRelease(&pInputType);
    SafeRelease(&pContentInfo);
    SafeRelease(&pMux);
    SafeRelease(&pDataStream);
    delete pEncoder;

    MFShutdown();
    CoUninitialize();

    if (FAILED(hr))
    {
        wprintf_s(L"Error: 0x%X\n", hr);
    }

    return 0;
} 
```



## <a name="related-topics"></a><span data-ttu-id="afc0e-231">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="afc0e-231">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afc0e-232">Composants WMContainer ASF</span><span class="sxs-lookup"><span data-stu-id="afc0e-232">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="afc0e-233">Prise en charge ASF dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="afc0e-233">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



