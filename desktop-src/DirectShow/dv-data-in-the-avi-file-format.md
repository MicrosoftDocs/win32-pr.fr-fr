---
description: Données DV au format de fichier AVI
ms.assetid: ae1ec184-afc3-4ec1-9b92-f53656293446
title: Données DV au format de fichier AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65f1393bfe4bbee4d080d90755f33cfa7f4a7fa4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482392"
---
# <a name="dv-data-in-the-avi-file-format"></a><span data-ttu-id="39091-103">Données DV au format de fichier AVI</span><span class="sxs-lookup"><span data-stu-id="39091-103">DV Data in the AVI File Format</span></span>

<span data-ttu-id="39091-104">Microsoft a spécifié le format de stockage des données vidéo numériques (DV) dans les fichiers AVI.</span><span class="sxs-lookup"><span data-stu-id="39091-104">Microsoft has specified the format for storage of digital video (DV) data in AVI files.</span></span> <span data-ttu-id="39091-105">La conformité à cette spécification permet de s’assurer que les fichiers AVI créés dans ce format seront compatibles avec les futures versions de l’architecture vidéo numérique DirectShow pour Windowsplatform.</span><span class="sxs-lookup"><span data-stu-id="39091-105">Conforming to this specification will ensure that the AVI files authored in this format will be compatible with future versions of the DirectShow digital video architecture for the Windowsplatform.</span></span>

<span data-ttu-id="39091-106">Cet article décrit le format des fichiers AVI contenant des données DV.</span><span class="sxs-lookup"><span data-stu-id="39091-106">This article describes the format of AVI files containing DV data.</span></span> <span data-ttu-id="39091-107">Des FOURCCs spécifiques (codes à quatre caractères) pour les flux de données DV entrelacés et les gestionnaires de flux de décompresseur/décompresseur DV sont définis.</span><span class="sxs-lookup"><span data-stu-id="39091-107">Specific FOURCCs (four-character codes) for interleaved DV data streams and DV compressor/decompressor stream handlers are defined.</span></span> <span data-ttu-id="39091-108">La structure du format de flux de données DV est définie.</span><span class="sxs-lookup"><span data-stu-id="39091-108">The stream format structure for DV data is defined.</span></span> <span data-ttu-id="39091-109">Les spécifications de deux méthodes de stockage des données DV au format de fichier AVI sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="39091-109">Specifications for two methods of storing DV data in the AVI file format are specified.</span></span>

<span data-ttu-id="39091-110">Il est supposé que le lecteur est familiarisé avec le format de données DV.</span><span class="sxs-lookup"><span data-stu-id="39091-110">It is assumed that the reader is familiar with the DV data format.</span></span> <span data-ttu-id="39091-111">(Ce format est défini dans la *spécification des magnétoscopes numériques à usage particulier*, également appelé Livre bleu.)</span><span class="sxs-lookup"><span data-stu-id="39091-111">(This format is defined in the *Specification of Consumer-use Digital VCRs*, also called the Blue Book.)</span></span>

<span data-ttu-id="39091-112">Il existe deux types de fichiers AVI DV : les fichiers AVI qui contiennent un flux de données DV, appelé fichiers *de type-1* ; et les fichiers AVI qui contiennent des vidéos DV en tant que flux « vids » et des fichiers audio DV en tant que flux « Auds », appelés fichiers *de type 2* .</span><span class="sxs-lookup"><span data-stu-id="39091-112">There are two types of DV AVI files: AVI files that contain one DV data stream, called *type-1* files; and AVI files that contain DV video as a 'vids' stream and DV audio as 'auds' streams, called *type-2* files.</span></span>

<span data-ttu-id="39091-113">**Fichiers AVI contenant un flux de données DV (type-1)**</span><span class="sxs-lookup"><span data-stu-id="39091-113">**AVI Files Containing One DV Data Stream (Type-1)**</span></span>

<span data-ttu-id="39091-114">Les données DV entrelacées peuvent être stockées dans leur format natif sous la forme d’un flux unique dans un fichier. AVI RIFF.</span><span class="sxs-lookup"><span data-stu-id="39091-114">Interleaved DV data can be stored in its native format as a single stream within an AVI RIFF file.</span></span> <span data-ttu-id="39091-115">Cela présente l’avantage d’utiliser le volume minimum de stockage de données pour le format DV.</span><span class="sxs-lookup"><span data-stu-id="39091-115">This has the advantage of using the minimum amount of data storage for DV.</span></span> <span data-ttu-id="39091-116">L’inconvénient principal est que ce format de fichier n’est pas à compatibilité descendante avec la vidéo pour Windows, car il ne contient pas de vidéo « vids » ou de flux audio « Auds ».</span><span class="sxs-lookup"><span data-stu-id="39091-116">The primary disadvantage is that this file format is not backward-compatible with Video for Windows, because it doesn't contain either a video 'vids' or an audio 'auds' stream.</span></span> <span data-ttu-id="39091-117">Le support est fourni pour le flux DV entrelacé par le biais des filtres de [séparateur](dv-splitter-filter.md) DV [du multiplexeur](dv-muxer-filter.md) et DV fournis avec DirectShow.</span><span class="sxs-lookup"><span data-stu-id="39091-117">Support is provided for the interleaved DV stream through the [DV Muxer](dv-muxer-filter.md) and [DV Splitter](dv-splitter-filter.md) filters provided with DirectShow.</span></span>

<span data-ttu-id="39091-118">Les données DV peuvent être stockées dans un seul flux au sein d’un fichier. AVI, en spécifiant le « IAVs » (flux audio et vidéo entrelacé) FOURCC (code à quatre caractères) dans le membre **fccType** et l’un ou l’autre des dvsl « DVSD », « dvhd » ou « FOURCCs » dans le membre **fccHandler** du bloc d’en-tête de flux « Strh ».</span><span class="sxs-lookup"><span data-stu-id="39091-118">DV data can be stored in a single stream within an AVI RIFF file by specifying the 'iavs' (interleaved audio and video stream) FOURCC (four-character code) in the **fccType** member and either of the 'dvsd', 'dvhd', or 'dvsl' FOURCCs in the **fccHandler** member of the 'strh' stream header chunk.</span></span> <span data-ttu-id="39091-119">Les images par seconde du flux vidéo doivent être spécifiées dans les membres **dwRate** et **dwScale** et le nombre total de blocs vidéo dans le segment « movi » du membre **dwLength** .</span><span class="sxs-lookup"><span data-stu-id="39091-119">The frames per second of the video stream must be specified in the **dwRate** and **dwScale** members and the total number of video blocks in the 'movi' chunk in the **dwLength** member.</span></span>

<span data-ttu-id="39091-120">Le gestionnaire de flux « DVSD » FOURCC spécifie que les données DV sont définies dans la partie 2 de la *spécification des magnétoscopes numériques à usage particulier*.</span><span class="sxs-lookup"><span data-stu-id="39091-120">The 'dvsd' stream handler FOURCC specifies that the DV data is as defined in Part 2 of the *Specification of Consumer-use Digital VCRs*.</span></span> <span data-ttu-id="39091-121">La vidéo est au format 525 lignes à 29,97 Hz (525-60) ou 625 lignes à 25,00 Hz (625-50).</span><span class="sxs-lookup"><span data-stu-id="39091-121">Video is in the format of 525 lines at 29.97 Hz (525-60) or 625 lines at 25.00 Hz (625-50).</span></span>

<span data-ttu-id="39091-122">Le gestionnaire de flux « dvhd » FOURCC spécifie que les données DV sont définies dans la partie 3 de la *spécification des magnétoscopes numériques à usage particulier*.</span><span class="sxs-lookup"><span data-stu-id="39091-122">The 'dvhd' stream handler FOURCC specifies that the DV data is as defined in Part 3 of the *Specification of Consumer-use Digital VCRs*.</span></span> <span data-ttu-id="39091-123">La vidéo est au format 1125 lignes à 30,00 Hz (1125-60) ou 1250 lignes à 25,00 Hz (1250-50).</span><span class="sxs-lookup"><span data-stu-id="39091-123">Video is in the format of 1125 lines at 30.00 Hz (1125-60) or 1250 lines at 25.00 Hz (1250-50).</span></span>

<span data-ttu-id="39091-124">Le gestionnaire de flux « dvsl » FOURCC spécifie que les données DV sont définies dans la partie 6 de la *spécification des magnétoscopes numériques à usage particulier*.</span><span class="sxs-lookup"><span data-stu-id="39091-124">The 'dvsl' stream handler FOURCC specifies that the DV data is as defined in Part 6 of *Specification of Consumer-use Digital VCRs*.</span></span> <span data-ttu-id="39091-125">La vidéo est au format de haute compression SD (SDL).</span><span class="sxs-lookup"><span data-stu-id="39091-125">Video is in the format of high-compression SD (SDL).</span></span>

> [!Note]  
> <span data-ttu-id="39091-126">Le reste de cet article fournit des définitions pour les flux « DVSD ».</span><span class="sxs-lookup"><span data-stu-id="39091-126">The remainder of this article provides definitions for 'dvsd' streams.</span></span>

 

<span data-ttu-id="39091-127">Le bloc d’en-tête de flux doit être suivi d’un bloc de format de flux [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) .</span><span class="sxs-lookup"><span data-stu-id="39091-127">The stream header chunk must be followed by a [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) stream format chunk.</span></span>

<span data-ttu-id="39091-128">Les données DV réelles sont stockées en tant que \# \# segments « DC » dans le bloc « movi » (le \# \# format représente l’identificateur de flux).</span><span class="sxs-lookup"><span data-stu-id="39091-128">The actual DV data is stored as '\#\#dc' chunks in the 'movi' chunk (the \#\# in the format represents the stream identifier).</span></span> <span data-ttu-id="39091-129">Chaque segment contient une trame de données, soit 10 ou 12 séquences DV DIF pour les systèmes 525-60 ou 625-50, respectivement.</span><span class="sxs-lookup"><span data-stu-id="39091-129">Each chunk contains one frame of data, either 10 or 12 DV DIF sequences for 525-60 or 625-50 systems, respectively.</span></span> <span data-ttu-id="39091-130">Le format de séquence DIF DV SD (« DVSD ») est défini dans la partie 2 de la *spécification des magnétoscopes numériques à usage particulier*.</span><span class="sxs-lookup"><span data-stu-id="39091-130">The DV SD ('dvsd') DIF sequence format is defined in Part 2 of the *Specification of Consumer-use Digital VCRs*.</span></span>

<span data-ttu-id="39091-131">L’exemple suivant illustre la forme de formulaire RIFF AIFF pour un fichier AVI avec un flux de données DV, développée avec des blocs d’en-tête terminés.</span><span class="sxs-lookup"><span data-stu-id="39091-131">The following example shows the AIFF RIFF form for an AVI file with one DV data stream, expanded with completed header chunks.</span></span>


```C++
00000000 RIFF (0FAE35D4) 'AVI '
0000000C     LIST (00000106) 'hdrl'
00000018         avih (00000038)
                     dwMicroSecPerFrame    : 33367
                     dwMaxBytesPerSec      : 3728000
                     dwPaddingGranularity  : 0
                     dwFlags               : 0x810 HASINDEX | TRUSTCKTYPE
                     dwTotalFrames         : 2192
                     dwInitialFrames       : 0
                     dwStreams             : 1
                     dwSuggestedBufferSize : 120000
                     dwWidth               : 720
                     dwHeight              : 480
                     dwReserved            : 0x0
00000058         LIST (0000006C) 'strl'
00000064             strh (00000038)
                         fccType               : 'iavs'
                         fccHandler            : 'dvsd'
                         dwFlags               : 0x0
                         wPriority             : 0
                         wLanguage             : 0x0 undefined
                         dwInitialFrames       : 0
                         dwScale               : 100 (29.970 Frames/Sec)
                         dwRate                : 2997
                         dwStart               : 0
                         dwLength              : 2192
                         dwSuggestedBufferSize : 120000
                         dwQuality             : 0
                         dwSampleSize          : 0
                         rcFrame               : 0,0,720,480
000000A4             strf (00000020)
                         dwDVAAuxSrc     : 0x........
                         dwDVAAuxCtl     : 0x........
                         dwDVAAuxSrc1    : 0x........
                         dwDVAAuxCtl1    : 0x........
                         dwDVVAuxSrc     : 0x........
                         dwDVVAuxCtl     : 0x........
                         dwDVReserved[2] : 0,0
000000CC     LIST (0FADAC00) 'movi'
0FADACD4     idx1 (00008900)
```



<span data-ttu-id="39091-132">**Fichiers AVI contenant des flux vidéo DV et audio DV (type-2)**</span><span class="sxs-lookup"><span data-stu-id="39091-132">**AVI Files Containing DV Video and DV Audio Streams (Type-2)**</span></span>

<span data-ttu-id="39091-133">Les données DV entrelacées peuvent être fractionnées en un flux vidéo et un à quatre flux audio au sein d’un fichier. AVI RIFF.</span><span class="sxs-lookup"><span data-stu-id="39091-133">Interleaved DV data can be split into a video stream and one to four audio streams within an AVI RIFF file.</span></span> <span data-ttu-id="39091-134">Cela présente l’avantage de bénéficier d’une compatibilité descendante avec la vidéo pour Windows, car elle contient un flux « vids » vidéo standard et au moins un flux audio standard « Auds ». l’inconvénient principal est que ce format de fichier nécessite que les données audio soient stockées de façon redondante sous forme de flux audio.</span><span class="sxs-lookup"><span data-stu-id="39091-134">This has the advantage of being backward-compatible with Video for Windows, because it contains a standard video 'vids' stream and at least one standard audio 'auds' stream The primary disadvantage is that this file format requires the audio data to be redundantly stored as audio streams.</span></span> <span data-ttu-id="39091-135">Le flux « vidéo » est en fait le flux de données DV entrelacées natives.</span><span class="sxs-lookup"><span data-stu-id="39091-135">The "video" stream is actually the native interleaved DV data stream.</span></span> <span data-ttu-id="39091-136">Toutefois, en tant que flux « vids » standard avec un type de gestionnaire « DVSD », le [décodeur vidéo DV](dv-video-decoder-filter.md) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="39091-136">However, as a standard 'vids' stream with a handler type of 'dvsd', the [DV Video Decoder](dv-video-decoder-filter.md) is used.</span></span> <span data-ttu-id="39091-137">Ce format requiert également l’utilisation du filtre de [séparateur DV](dv-splitter-filter.md) pour fractionner les fichiers « capturés » avant de les écrire en tant que fichiers AVI.</span><span class="sxs-lookup"><span data-stu-id="39091-137">This format also requires using the [DV Splitter](dv-splitter-filter.md) filter to split "captured" files before writing them as AVI files.</span></span>

<span data-ttu-id="39091-138">Les données DV peuvent être stockées sous la forme d’un flux vidéo avec un nombre distinct de flux audio dans un fichier RIFF AVI.</span><span class="sxs-lookup"><span data-stu-id="39091-138">DV data can be stored as a video stream with a separate number of audio streams in an AVI RIFF file.</span></span> <span data-ttu-id="39091-139">Le flux vidéo est spécifié avec un en-tête de flux vidéo standard (la valeur du membre **fccType** est’vids').</span><span class="sxs-lookup"><span data-stu-id="39091-139">The video stream is specified with a standard video stream header (the **fccType** member value is 'vids').</span></span> <span data-ttu-id="39091-140">Le membre **fccHandler** est spécifié en tant que « DVSD », « dvhd » ou « dvsl ».</span><span class="sxs-lookup"><span data-stu-id="39091-140">The **fccHandler** member is specified as 'dvsd', 'dvhd', or 'dvsl'.</span></span> <span data-ttu-id="39091-141">Les images par seconde du flux vidéo doivent être spécifiées dans les membres **dwRate** et **dwScale** et le nombre total de blocs vidéo dans le segment « movi » du membre **dwLength** .</span><span class="sxs-lookup"><span data-stu-id="39091-141">The frames per second of the video stream must be specified in the **dwRate** and **dwScale** members and the total number of video blocks in the 'movi' chunk in the **dwLength** member.</span></span>

<span data-ttu-id="39091-142">Dans ce fichier AVI contenant la vidéo DV en tant que flux de données « vids » et DV audio en tant que flux « Auds », le bloc format de flux vidéo est une structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) standard.</span><span class="sxs-lookup"><span data-stu-id="39091-142">In this AVI file containing DV video as a 'vids' stream and DV audio as 'auds' streams form of DV, the video stream format chunk is a standard [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span> <span data-ttu-id="39091-143">Le bloc de format de flux peut éventuellement être étendu pour inclure le segment [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) , en accroissant la taille de segment de format de flux de 40 octets (taille de la structure **BITMAPINFOHEADER** ) à 72 octets (taille de **BITMAPINFOHEADER** plus structures **DVINFO** ) et immédiatement après la structure de données **BITMAPINFOHEADER** avec une structure de données **DVINFO** .</span><span class="sxs-lookup"><span data-stu-id="39091-143">The stream format chunk can be optionally extended to include the [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) chunk, by increasing the stream format chunk size from 40 bytes (size of the **BITMAPINFOHEADER** structure) to 72 bytes (size of **BITMAPINFOHEADER** plus **DVINFO** structures) and immediately following the **BITMAPINFOHEADER** data structure with a **DVINFO** data structure.</span></span>

<span data-ttu-id="39091-144">Le ou les flux audio sont spécifiés avec un en-tête de flux audio standard (la valeur du membre **fccType** est’Auds').</span><span class="sxs-lookup"><span data-stu-id="39091-144">The audio stream(s) is specified with a standard audio stream header (the **fccType** member value is 'auds').</span></span> <span data-ttu-id="39091-145">Le membre **fccHandler** n’est pas utilisé pour les flux audio.</span><span class="sxs-lookup"><span data-stu-id="39091-145">The **fccHandler** member is not used for audio streams.</span></span>

<span data-ttu-id="39091-146">Les données vidéo DV sont stockées en tant que \# \# segments « DC », tels que définis dans la description précédente d’un fichier AVI avec une donnée DV, et les données audio sont stockées en tant que \# \# segments « WB » dans le bloc « movi ».</span><span class="sxs-lookup"><span data-stu-id="39091-146">The DV video data is stored as '\#\#dc' chunks, as defined in the preceding description of an AVI file with one DV data, and the audio data is stored as '\#\#wb' chunks in the 'movi' chunk.</span></span>

> [!Note]  
> <span data-ttu-id="39091-147">La *spécification des magnétoscopes numériques à usage particulier* peut ne pas être disponible dans certains langages et pays.</span><span class="sxs-lookup"><span data-stu-id="39091-147">The *Specification of Consumer-use Digital VCRs* may not be available in some languages and countries.</span></span>

 

<span data-ttu-id="39091-148">L’exemple suivant illustre la forme de formulaire RIFF AIFF pour un fichier AVI contenant une vidéo DV en tant que flux « vids » et audio DV en tant que flux « Auds » développés avec des blocs d’en-tête terminés (y compris les données [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) facultatives qui suivent le [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) dans le sous-bloc « Strf » pour le flux « vids »).</span><span class="sxs-lookup"><span data-stu-id="39091-148">The following example shows the AIFF RIFF form for an AVI file containing DV video as a 'vids' stream and DV audio as 'auds' streams expanded with completed header chunks (including optional [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) data following the [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) in the 'strf' sub-chunk for the 'vids' stream).</span></span>


```C++
00000000 RIFF (103E2920) 'AVI '
0000000C     LIST (00000146) 'hdrl'
00000018         avih (00000038)
                     dwMicroSecPerFrame    : 33367
                     dwMaxBytesPerSec      : 3728000
                     dwPaddingGranularity  : 0
                     dwFlags               : 0x810 HASINDEX | TRUSTCKTYPE
                     dwTotalFrames         : 2192
                     dwInitialFrames       : 0
                     dwStreams             : 2
                     dwSuggestedBufferSize : 120000
                     dwWidth               : 720
                     dwHeight              : 480
                     dwReserved            : 0x0
00000058         LIST (00000094) 'strl'
00000064             strh (00000038)
                         fccType               : 'vids'
                         fccHandler            : 'dvsd'
                         dwFlags               : 0x0
                         wPriority             : 0
                         wLanguage             : 0x0 undefined
                         dwInitialFrames       : 0
                         dwScale               : 100 (29.970 Frames/Sec)
                         dwRate                : 2997
                         dwStart               : 0
                         dwLength              : 2192
                         dwSuggestedBufferSize : 120000
                         dwQuality             : 0
                         dwSampleSize          : 0
                         rcFrame               : 0,0,720,480
000000A4             strf (00000048)
                         biSize          : 40
                         biWidth         : 720
                         biHeight        : 480
                         biPlanes        : 1
                         biBitCount      : 24
                         biCompression   : 0x64737664 'dvsd'
                         biSizeImage     : 120000
                         biXPelsPerMeter : 0
                         biYPelsPerMeter : 0
                         biClrUsed       : 0
                         biClrImportant  : 0
                         dwDVAAuxSrc     : 0x........
                         dwDVAAuxCtl     : 0x........
                         dwDVAAuxSrc1    : 0x........
                         dwDVAAuxCtl1    : 0x........
                         dwDVVAuxSrc     : 0x........
                         dwDVVAuxCtl     : 0x........
                         dwDVReserved[2] : 0,0
000000F4         LIST (0000005E) 'strl'
00000100             strh (00000038)
                         fccType               : 'auds'
                         fccHandler            : '    '
                         dwFlags               : 0x0
                         wPriority             : 0
                         wLanguage             : 0x0 undefined
                         dwInitialFrames       : 0
                         dwScale               : 1 (32000.000 Samples/Sec)
                         dwRate                : 32000
                         dwStart               : 0
                         dwLength              : 2340474
                         dwSuggestedBufferSize : 4272
                         dwQuality             : 0
                         dwSampleSize          : 4
                         rcFrame               : 0,0,0,0
00000140             strf (00000012)
                         wFormatTag      : 1 PCM
                         nChannels       : 2
                         nSamplesPerSec  : 32000
                         nAvgBytesPerSec : 128000
                         nBlockAlign     : 4
                         wBitsPerSample  : 16
                         cbSize          : 0
00000814     LIST (103D0EF4) 'movi'
103D1710     idx1 (00011210)
```



## <a name="related-topics"></a><span data-ttu-id="39091-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="39091-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39091-150">Format de fichier AVI</span><span class="sxs-lookup"><span data-stu-id="39091-150">AVI File Format</span></span>](avi-file-format.md)
</dt> </dl>

 

 
