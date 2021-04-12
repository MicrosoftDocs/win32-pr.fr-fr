---
description: Cette rubrique explique comment utiliser le lecteur source pour traiter les données multimédias.
ms.assetid: 583f5736-f767-47c5-8fdc-b3645aed59f6
title: Utilisation du lecteur source pour traiter les données multimédias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b19bce4d83298693825037aef92a220d78ed7c7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321449"
---
# <a name="using-the-source-reader-to-process-media-data"></a><span data-ttu-id="28594-103">Utilisation du lecteur source pour traiter les données multimédias</span><span class="sxs-lookup"><span data-stu-id="28594-103">Using the Source Reader to Process Media Data</span></span>

<span data-ttu-id="28594-104">Cette rubrique explique comment utiliser le [lecteur source](source-reader.md) pour traiter les données multimédias.</span><span class="sxs-lookup"><span data-stu-id="28594-104">This topic describes how to use the [Source Reader](source-reader.md) to process media data.</span></span>

<span data-ttu-id="28594-105">Pour utiliser le lecteur source, suivez les étapes de base suivantes :</span><span class="sxs-lookup"><span data-stu-id="28594-105">To use the Source Reader, follow these basic steps:</span></span>

1.  <span data-ttu-id="28594-106">Créez une instance du lecteur source.</span><span class="sxs-lookup"><span data-stu-id="28594-106">Create an instance of the Source Reader.</span></span>
2.  <span data-ttu-id="28594-107">Énumérer les formats de sortie possibles.</span><span class="sxs-lookup"><span data-stu-id="28594-107">Enumerate the possible output formats.</span></span>
3.  <span data-ttu-id="28594-108">Définissez le format de sortie réel pour chaque flux.</span><span class="sxs-lookup"><span data-stu-id="28594-108">Set the actual output format for each stream.</span></span>
4.  <span data-ttu-id="28594-109">Traiter les données de la source.</span><span class="sxs-lookup"><span data-stu-id="28594-109">Process data from the source.</span></span>

<span data-ttu-id="28594-110">Le reste de cette rubrique décrit ces étapes en détail.</span><span class="sxs-lookup"><span data-stu-id="28594-110">The remainder of this topic describes these steps in detail.</span></span>

-   [<span data-ttu-id="28594-111">Création du lecteur source</span><span class="sxs-lookup"><span data-stu-id="28594-111">Creating the Source Reader</span></span>](#creating-the-source-reader)
-   [<span data-ttu-id="28594-112">Énumération des formats de sortie</span><span class="sxs-lookup"><span data-stu-id="28594-112">Enumerating Output Formats</span></span>](#enumerating-output-formats)
-   [<span data-ttu-id="28594-113">Définition des formats de sortie</span><span class="sxs-lookup"><span data-stu-id="28594-113">Setting Output Formats</span></span>](#setting-output-formats)
-   [<span data-ttu-id="28594-114">Traitement des données multimédias</span><span class="sxs-lookup"><span data-stu-id="28594-114">Processing Media Data</span></span>](#using-the-source-reader-to-process-media-data)
-   [<span data-ttu-id="28594-115">Drainage du pipeline de données</span><span class="sxs-lookup"><span data-stu-id="28594-115">Draining the Data Pipeline</span></span>](#draining-the-data-pipeline)
-   [<span data-ttu-id="28594-116">Obtention de la durée du fichier</span><span class="sxs-lookup"><span data-stu-id="28594-116">Getting the File Duration</span></span>](#getting-the-file-duration)
-   [<span data-ttu-id="28594-117">Cherche</span><span class="sxs-lookup"><span data-stu-id="28594-117">Seeking</span></span>](#seeking)
-   [<span data-ttu-id="28594-118">Vitesse de lecture</span><span class="sxs-lookup"><span data-stu-id="28594-118">Playback Rate</span></span>](#playback-rate)
-   [<span data-ttu-id="28594-119">Accélération matérielle</span><span class="sxs-lookup"><span data-stu-id="28594-119">Hardware Acceleration</span></span>](#hardware-acceleration)
-   [<span data-ttu-id="28594-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="28594-120">Related topics</span></span>](#related-topics)

## <a name="creating-the-source-reader"></a><span data-ttu-id="28594-121">Création du lecteur source</span><span class="sxs-lookup"><span data-stu-id="28594-121">Creating the Source Reader</span></span>

<span data-ttu-id="28594-122">Pour créer une instance du lecteur source, appelez l’une des fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="28594-122">To create an instance of the Source Reader, call one of the following functions:</span></span>



| <span data-ttu-id="28594-123">Fonction</span><span class="sxs-lookup"><span data-stu-id="28594-123">Function</span></span>                                                                                                                                                                                                                                                        | <span data-ttu-id="28594-124">Description</span><span class="sxs-lookup"><span data-stu-id="28594-124">Description</span></span>                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28594-125"><span id="MFCreateSourceReaderFromURL"></span><span id="mfcreatesourcereaderfromurl"></span><span id="MFCREATESOURCEREADERFROMURL"></span>[**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)</span><span class="sxs-lookup"><span data-stu-id="28594-125"><span id="MFCreateSourceReaderFromURL"></span><span id="mfcreatesourcereaderfromurl"></span><span id="MFCREATESOURCEREADERFROMURL"></span>[**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)</span></span><br/>                                         | <span data-ttu-id="28594-126">Prend une URL comme entrée.</span><span class="sxs-lookup"><span data-stu-id="28594-126">Takes a URL as input.</span></span> <span data-ttu-id="28594-127">Cette fonction utilise le programme de [résolution source](source-resolver.md) pour créer une source de média à partir de l’URL.</span><span class="sxs-lookup"><span data-stu-id="28594-127">This function uses the [Source Resolver](source-resolver.md) to create a media source from the URL.</span></span><br/>                                                                       |
| <span data-ttu-id="28594-128"><span id="MFCreateSourceReaderFromByteStream"></span><span id="mfcreatesourcereaderfrombytestream"></span><span id="MFCREATESOURCEREADERFROMBYTESTREAM"></span>[**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)</span><span class="sxs-lookup"><span data-stu-id="28594-128"><span id="MFCreateSourceReaderFromByteStream"></span><span id="mfcreatesourcereaderfrombytestream"></span><span id="MFCREATESOURCEREADERFROMBYTESTREAM"></span>[**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)</span></span><br/>      | <span data-ttu-id="28594-129">Prend un pointeur vers un flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="28594-129">Takes a pointer to a byte stream.</span></span> <span data-ttu-id="28594-130">Cette fonction utilise également le programme de résolution source pour créer la source du média.</span><span class="sxs-lookup"><span data-stu-id="28594-130">This function also uses the Source Resolver to create the media source.</span></span><br/>                                                                                        |
| <span data-ttu-id="28594-131"><span id="MFCreateSourceReaderFromMediaSource"></span><span id="mfcreatesourcereaderfrommediasource"></span><span id="MFCREATESOURCEREADERFROMMEDIASOURCE"></span>[**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)</span><span class="sxs-lookup"><span data-stu-id="28594-131"><span id="MFCreateSourceReaderFromMediaSource"></span><span id="mfcreatesourcereaderfrommediasource"></span><span id="MFCREATESOURCEREADERFROMMEDIASOURCE"></span>[**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)</span></span><br/> | <span data-ttu-id="28594-132">Prend un pointeur vers une source multimédia qui a déjà été créée.</span><span class="sxs-lookup"><span data-stu-id="28594-132">Takes a pointer to a media source that has already been created.</span></span> <span data-ttu-id="28594-133">Cette fonction est utile pour les sources multimédias que le programme de résolution source ne peut pas créer, telles que les périphériques de capture ou les sources de média personnalisées.</span><span class="sxs-lookup"><span data-stu-id="28594-133">This function is useful for media sources that the Source Resolver cannot create, such capture devices or custom media sources.</span></span><br/> |



 

<span data-ttu-id="28594-134">En général, pour les fichiers multimédias, utilisez [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl).</span><span class="sxs-lookup"><span data-stu-id="28594-134">Typically, for media files, use [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl).</span></span> <span data-ttu-id="28594-135">Pour les appareils, tels que les webcams, utilisez [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource).</span><span class="sxs-lookup"><span data-stu-id="28594-135">For devices, such as webcams, use [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource).</span></span> <span data-ttu-id="28594-136">(Pour plus d’informations sur les appareils de capture dans Microsoft Media Foundation, consultez [capture audio/vidéo](audio-video-capture.md).)</span><span class="sxs-lookup"><span data-stu-id="28594-136">(For more information about capture devices in Microsoft Media Foundation, see [Audio/Video Capture](audio-video-capture.md).)</span></span>

<span data-ttu-id="28594-137">Chacune de ces fonctions prend un pointeur [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) facultatif, qui est utilisé pour définir différentes options sur le lecteur source, comme décrit dans les rubriques de référence pour ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="28594-137">Each of these functions takes an optional [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer, which is used to set various options on the Source Reader, as described in the reference topics for these functions.</span></span> <span data-ttu-id="28594-138">Pour connaître le comportement par défaut, affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="28594-138">To get the default behavior, set this parameter to **NULL**.</span></span> <span data-ttu-id="28594-139">Chaque fonction retourne un pointeur [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) comme paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="28594-139">Each function returns an [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) pointer as an output parameter.</span></span> <span data-ttu-id="28594-140">Vous devez appeler la fonction **CoInitialize (ex)** et [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) avant d’appeler l’une de ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="28594-140">You must call **CoInitialize(Ex)** and [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function before calling any of these functions.</span></span>

<span data-ttu-id="28594-141">Le code suivant crée le lecteur source à partir d’une URL.</span><span class="sxs-lookup"><span data-stu-id="28594-141">The following code creates the Source Reader from a URL.</span></span>


```C++
int __cdecl wmain(int argc, __in_ecount(argc) PCWSTR* argv)
{
    if (argc < 2)
    {
        return 1;
    }

    const WCHAR *pszURL = argv[1];

    // Initialize the COM runtime.
    HRESULT hr = CoInitializeEx(0, COINIT_MULTITHREADED);
    if (SUCCEEDED(hr))
    {
        // Initialize the Media Foundation platform.
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            // Create the source reader.
            IMFSourceReader *pReader;
            hr = MFCreateSourceReaderFromURL(pszURL, NULL, &pReader);
            if (SUCCEEDED(hr))
            {
                ReadMediaFile(pReader);
                pReader->Release();
            }
            // Shut down Media Foundation.
            MFShutdown();
        }
        CoUninitialize();
    }
}
```



## <a name="enumerating-output-formats"></a><span data-ttu-id="28594-142">Énumération des formats de sortie</span><span class="sxs-lookup"><span data-stu-id="28594-142">Enumerating Output Formats</span></span>

<span data-ttu-id="28594-143">Chaque source multimédia a au moins un flux.</span><span class="sxs-lookup"><span data-stu-id="28594-143">Every media source has at least one stream.</span></span> <span data-ttu-id="28594-144">Par exemple, un fichier vidéo peut contenir un flux vidéo et un flux audio.</span><span class="sxs-lookup"><span data-stu-id="28594-144">For example, a video file might contain a video stream and an audio stream.</span></span> <span data-ttu-id="28594-145">Le format de chaque flux est décrit à l’aide d’un type de média, représenté par l’interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="28594-145">The format of each stream is described using a media type, represented by the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface.</span></span> <span data-ttu-id="28594-146">Pour plus d’informations sur les types de médias, consultez [types de médias](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="28594-146">For more information about media types, see [Media Types](media-types.md).</span></span> <span data-ttu-id="28594-147">Vous devez examiner le type de média pour comprendre le format des données que vous récupérez à partir du lecteur source.</span><span class="sxs-lookup"><span data-stu-id="28594-147">You must examine the media type to understand the format of the data that you get from the Source Reader.</span></span>

<span data-ttu-id="28594-148">Initialement, chaque flux a un format par défaut, que vous pouvez trouver en appelant la méthode [**IMFSourceReader :: GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) :</span><span class="sxs-lookup"><span data-stu-id="28594-148">Initially, every stream has a default format, which you can find by calling the [**IMFSourceReader::GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) method:</span></span>

<span data-ttu-id="28594-149">Pour chaque flux, la source du média offre une liste de types de média possibles pour ce flux.</span><span class="sxs-lookup"><span data-stu-id="28594-149">For each stream, the media source offers a list of possible media types for that stream.</span></span> <span data-ttu-id="28594-150">Le nombre de types dépend de la source.</span><span class="sxs-lookup"><span data-stu-id="28594-150">The number of types depends on the source.</span></span> <span data-ttu-id="28594-151">Si la source représente un fichier multimédia, il n’y a généralement qu’un seul type par flux.</span><span class="sxs-lookup"><span data-stu-id="28594-151">If the source represents a media file, there is typically only one type per stream.</span></span> <span data-ttu-id="28594-152">Une webcam, en revanche, peut être en mesure de diffuser des vidéos dans différents formats.</span><span class="sxs-lookup"><span data-stu-id="28594-152">A webcam, on the other hand, might be able to stream video in several different formats.</span></span> <span data-ttu-id="28594-153">Dans ce cas, l’application peut sélectionner le format à utiliser dans la liste des types de médias.</span><span class="sxs-lookup"><span data-stu-id="28594-153">In that case, the application can select which format to use from the list of media types.</span></span>

<span data-ttu-id="28594-154">Pour obtenir l’un des types de média pour un flux, appelez la méthode [**IMFSourceReader :: GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) .</span><span class="sxs-lookup"><span data-stu-id="28594-154">To get one of the media types for a stream, call the [**IMFSourceReader::GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) method.</span></span> <span data-ttu-id="28594-155">Cette méthode prend deux paramètres d’index : l’index du flux et un index dans la liste des types de média pour le flux.</span><span class="sxs-lookup"><span data-stu-id="28594-155">This method takes two index parameters: The index of the stream, and an index into the list of media types for the stream.</span></span> <span data-ttu-id="28594-156">Pour énumérer tous les types d’un flux, incrémentez l’index de la liste tout en conservant la constante d’index de flux.</span><span class="sxs-lookup"><span data-stu-id="28594-156">To enumerate all the types for a stream, increment the list index while keeping the stream index constant.</span></span> <span data-ttu-id="28594-157">Lorsque l’index de liste est hors limites, **GetNativeMediaType** retourne **MF E plus de \_ \_ \_ \_ types**.</span><span class="sxs-lookup"><span data-stu-id="28594-157">When the list index goes out of bounds, **GetNativeMediaType** returns **MF\_E\_NO\_MORE\_TYPES**.</span></span>


```C++
HRESULT EnumerateTypesForStream(IMFSourceReader *pReader, DWORD dwStreamIndex)
{
    HRESULT hr = S_OK;
    DWORD dwMediaTypeIndex = 0;

    while (SUCCEEDED(hr))
    {
        IMFMediaType *pType = NULL;
        hr = pReader->GetNativeMediaType(dwStreamIndex, dwMediaTypeIndex, &pType);
        if (hr == MF_E_NO_MORE_TYPES)
        {
            hr = S_OK;
            break;
        }
        else if (SUCCEEDED(hr))
        {
            // Examine the media type. (Not shown.)

            pType->Release();
        }
        ++dwMediaTypeIndex;
    }
    return hr;
}
```



<span data-ttu-id="28594-158">Pour énumérer les types de média pour chaque flux, incrémentez l’index de flux.</span><span class="sxs-lookup"><span data-stu-id="28594-158">To enumerate the media types for every stream, increment the stream index.</span></span> <span data-ttu-id="28594-159">Lorsque l’index de flux sort des limites, [**GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) retourne **MF \_ E \_ INVALIDSTREAMNUMBER**.</span><span class="sxs-lookup"><span data-stu-id="28594-159">When the stream index goes out of bounds, [**GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) returns **MF\_E\_INVALIDSTREAMNUMBER**.</span></span>


```C++
HRESULT EnumerateTypesForStream(IMFSourceReader *pReader, DWORD dwStreamIndex)
{
    HRESULT hr = S_OK;
    DWORD dwMediaTypeIndex = 0;

    while (SUCCEEDED(hr))
    {
        IMFMediaType *pType = NULL;
        hr = pReader->GetNativeMediaType(dwStreamIndex, dwMediaTypeIndex, &pType);
        if (hr == MF_E_NO_MORE_TYPES)
        {
            hr = S_OK;
            break;
        }
        else if (SUCCEEDED(hr))
        {
            // Examine the media type. (Not shown.)

            pType->Release();
        }
        ++dwMediaTypeIndex;
    }
    return hr;
}
```



## <a name="setting-output-formats"></a><span data-ttu-id="28594-160">Définition des formats de sortie</span><span class="sxs-lookup"><span data-stu-id="28594-160">Setting Output Formats</span></span>

<span data-ttu-id="28594-161">Pour modifier le format de sortie, appelez la méthode [**IMFSourceReader :: SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) .</span><span class="sxs-lookup"><span data-stu-id="28594-161">To change the output format, call the [**IMFSourceReader::SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) method.</span></span> <span data-ttu-id="28594-162">Cette méthode prend l’index de flux et un type de média :</span><span class="sxs-lookup"><span data-stu-id="28594-162">This method takes the stream index and a media type:</span></span>

``` syntax
hr = pReader->SetCurrentMediaType(dwStreamIndex, pMediaType);
```

<span data-ttu-id="28594-163">Pour le type de média, cela dépend de l’insertion ou non d’un décodeur.</span><span class="sxs-lookup"><span data-stu-id="28594-163">For the media type, it depends on whether you want to insert a decoder.</span></span>

-   <span data-ttu-id="28594-164">Pour récupérer les données directement à partir de la source sans les décoder, utilisez l’un des types retournés par [**GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype).</span><span class="sxs-lookup"><span data-stu-id="28594-164">To get data directly from the source without decoding it, use one of the types returned by [**GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype).</span></span>
-   <span data-ttu-id="28594-165">Pour décoder le flux, créez un nouveau type de média qui décrit le format non compressé souhaité.</span><span class="sxs-lookup"><span data-stu-id="28594-165">To decode the stream, create a new media type that describes the desired uncompressed format.</span></span>

<span data-ttu-id="28594-166">Dans le cas du décodeur, créez le type de média comme suit :</span><span class="sxs-lookup"><span data-stu-id="28594-166">In the case of the decoder, create the media type as follows:</span></span>

1.  <span data-ttu-id="28594-167">Appelez [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) pour créer un type de média.</span><span class="sxs-lookup"><span data-stu-id="28594-167">Call [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) to create a new media type.</span></span>
2.  <span data-ttu-id="28594-168">Définissez l’attribut de [**\_ \_ \_ type principal MF MT**](mf-mt-major-type-attribute.md) pour spécifier audio ou Video.</span><span class="sxs-lookup"><span data-stu-id="28594-168">Set the [**MF\_MT\_MAJOR\_TYPE**](mf-mt-major-type-attribute.md) attribute to specify audio or video.</span></span>
3.  <span data-ttu-id="28594-169">Définissez l’attribut de [**\_ sous- \_ type MF MT**](mf-mt-subtype-attribute.md) pour spécifier le sous-type du format de décodage.</span><span class="sxs-lookup"><span data-stu-id="28594-169">Set the [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md) attribute to specify the subtype of the decoding format.</span></span> <span data-ttu-id="28594-170">(Consultez [GUID de sous-type audio](audio-subtype-guids.md) et [GUID de sous-type de vidéo](video-subtype-guids.md).)</span><span class="sxs-lookup"><span data-stu-id="28594-170">(See [Audio Subtype GUIDs](audio-subtype-guids.md) and [Video Subtype GUIDs](video-subtype-guids.md).)</span></span>
4.  <span data-ttu-id="28594-171">Appelez [**IMFSourceReader :: SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype).</span><span class="sxs-lookup"><span data-stu-id="28594-171">Call [**IMFSourceReader::SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype).</span></span>

<span data-ttu-id="28594-172">Le lecteur source chargera automatiquement le décodeur.</span><span class="sxs-lookup"><span data-stu-id="28594-172">The Source Reader will automatically load the decoder.</span></span> <span data-ttu-id="28594-173">Pour obtenir des informations complètes sur le format décodé, appelez [**IMFSourceReader :: GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) après l’appel à [**SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype)</span><span class="sxs-lookup"><span data-stu-id="28594-173">To get the complete details of the decoded format, call [**IMFSourceReader::GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) after the call to [**SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype)</span></span>

<span data-ttu-id="28594-174">Le code suivant configure le flux vidéo pour RGB-32 et le flux audio pour le fichier audio PCM.</span><span class="sxs-lookup"><span data-stu-id="28594-174">The following code configures the video stream for RGB-32 and the audio stream for PCM audio.</span></span>


```C++
HRESULT ConfigureDecoder(IMFSourceReader *pReader, DWORD dwStreamIndex)
{
    IMFMediaType *pNativeType = NULL;
    IMFMediaType *pType = NULL;

    // Find the native format of the stream.
    HRESULT hr = pReader->GetNativeMediaType(dwStreamIndex, 0, &pNativeType);
    if (FAILED(hr))
    {
        return hr;
    }

    GUID majorType, subtype;

    // Find the major type.
    hr = pNativeType->GetGUID(MF_MT_MAJOR_TYPE, &majorType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Define the output type.
    hr = MFCreateMediaType(&pType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetGUID(MF_MT_MAJOR_TYPE, majorType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Select a subtype.
    if (majorType == MFMediaType_Video)
    {
        subtype= MFVideoFormat_RGB32;
    }
    else if (majorType == MFMediaType_Audio)
    {
        subtype = MFAudioFormat_PCM;
    }
    else
    {
        // Unrecognized type. Skip.
        goto done;
    }

    hr = pType->SetGUID(MF_MT_SUBTYPE, subtype);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the uncompressed format.
    hr = pReader->SetCurrentMediaType(dwStreamIndex, NULL, pType);
    if (FAILED(hr))
    {
        goto done;
    }

done:
    SafeRelease(&pNativeType);
    SafeRelease(&pType);
    return hr;
}
```



## <a name="processing-media-data"></a><span data-ttu-id="28594-175">Traitement des données multimédias</span><span class="sxs-lookup"><span data-stu-id="28594-175">Processing Media Data</span></span>

<span data-ttu-id="28594-176">Pour récupérer les données du média à partir de la source, appelez la méthode [**IMFSourceReader :: ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) , comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="28594-176">To get media data from the source, call the [**IMFSourceReader::ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method, as shown in the following code.</span></span>


```C++
        DWORD streamIndex, flags;
        LONGLONG llTimeStamp;

        hr = pReader->ReadSample(
            MF_SOURCE_READER_ANY_STREAM,    // Stream index.
            0,                              // Flags.
            &streamIndex,                   // Receives the actual stream index. 
            &flags,                         // Receives status flags.
            &llTimeStamp,                   // Receives the time stamp.
            &pSample                        // Receives the sample or NULL.
            );
```



<span data-ttu-id="28594-177">Le premier paramètre est l’index du flux pour lequel vous souhaitez obtenir des données.</span><span class="sxs-lookup"><span data-stu-id="28594-177">The first parameter is the index of the stream for which you want to get data.</span></span> <span data-ttu-id="28594-178">Vous pouvez également spécifier **\_ \_ un lecteur source MF \_ n’importe quel \_ flux** pour récupérer les données disponibles suivantes à partir de n’importe quel flux.</span><span class="sxs-lookup"><span data-stu-id="28594-178">You can also specify **MF\_SOURCE\_READER\_ANY\_STREAM** to get the next available data from any stream.</span></span> <span data-ttu-id="28594-179">Le deuxième paramètre contient des indicateurs facultatifs ; pour obtenir une liste de ces, consultez [**\_ indicateur de \_ \_ contrôle \_ du lecteur source MF**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_control_flag) .</span><span class="sxs-lookup"><span data-stu-id="28594-179">The second parameter contains optional flags; see [**MF\_SOURCE\_READER\_CONTROL\_FLAG**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_control_flag) for a list of these.</span></span> <span data-ttu-id="28594-180">Le troisième paramètre reçoit l’index du flux qui produit réellement les données.</span><span class="sxs-lookup"><span data-stu-id="28594-180">The third parameter receives the index of the stream that actually produces the data.</span></span> <span data-ttu-id="28594-181">Vous aurez besoin de ces informations si vous définissez le premier paramètre sur le **\_ lecteur source MF \_ \_ n’importe quel \_ flux**.</span><span class="sxs-lookup"><span data-stu-id="28594-181">You will need this information if you set the first parameter to **MF\_SOURCE\_READER\_ANY\_STREAM**.</span></span> <span data-ttu-id="28594-182">Le quatrième paramètre reçoit des indicateurs d’État, indiquant les différents événements qui peuvent se produire lors de la lecture des données, telles que les modifications de format dans le flux.</span><span class="sxs-lookup"><span data-stu-id="28594-182">The fourth parameter receives status flags, indicating various events that can occur while reading the data, such as format changes in the stream.</span></span> <span data-ttu-id="28594-183">Pour obtenir la liste des indicateurs d’État, consultez [**\_ \_ \_ indicateur de lecteur source MF**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag).</span><span class="sxs-lookup"><span data-stu-id="28594-183">For a list of status flags, see [**MF\_SOURCE\_READER\_FLAG**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag).</span></span>

<span data-ttu-id="28594-184">Si la source du média est en mesure de produire des données pour le flux demandé, le dernier paramètre de [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) reçoit un pointeur vers l’interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) d’un objet d’exemple de support.</span><span class="sxs-lookup"><span data-stu-id="28594-184">If the media source is able to produce data for the requested stream, the last parameter of [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) receives a pointer to the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface of a media sample object.</span></span> <span data-ttu-id="28594-185">Utilisez l’exemple de support pour :</span><span class="sxs-lookup"><span data-stu-id="28594-185">Use the media sample to:</span></span>

-   <span data-ttu-id="28594-186">Obtient un pointeur vers les données multimédia.</span><span class="sxs-lookup"><span data-stu-id="28594-186">Get a pointer to the media data.</span></span>
-   <span data-ttu-id="28594-187">Obtient l’heure de présentation et la durée de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="28594-187">Get the presentation time and sample duration.</span></span>
-   <span data-ttu-id="28594-188">Obtient des attributs qui décrivent l’entrelacement, la dominance des champs et d’autres aspects de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="28594-188">Get attributes that describe interlacing, field dominance, and other aspects of the sample.</span></span>

<span data-ttu-id="28594-189">Le contenu des données multimédias dépend du format du flux.</span><span class="sxs-lookup"><span data-stu-id="28594-189">The contents of the media data depend on the format of the stream.</span></span> <span data-ttu-id="28594-190">Pour un flux vidéo non compressé, chaque exemple de support contient une seule image vidéo.</span><span class="sxs-lookup"><span data-stu-id="28594-190">For an uncompressed video stream, each media sample contains a single video frame.</span></span> <span data-ttu-id="28594-191">Pour un flux audio non compressé, chaque exemple de support contient une séquence de trames audio.</span><span class="sxs-lookup"><span data-stu-id="28594-191">For an uncompressed audio stream, each media sample contains a sequence of audio frames.</span></span>

<span data-ttu-id="28594-192">La méthode [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) peut retourner **S \_ OK** et ne pas retourner un exemple de support dans le paramètre *pSample* .</span><span class="sxs-lookup"><span data-stu-id="28594-192">The [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method can return **S\_OK** and yet not return a media sample in the *pSample* parameter.</span></span> <span data-ttu-id="28594-193">Par exemple, lorsque vous atteignez la fin du fichier, **ReadSample** définit l' **indicateur \_ \_ \_ ENDOFSTREAM de READERF source MF** dans *dwFlags* et affecte à *pSample* la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="28594-193">For example, when you reach the end of the file, **ReadSample** sets the **MF\_SOURCE\_READERF\_ENDOFSTREAM** flag in *dwFlags* and sets *pSample* to **NULL**.</span></span> <span data-ttu-id="28594-194">Dans ce cas, la méthode **ReadSample** retourne **S \_ OK** , car aucune erreur n’est survenue, même si le paramètre *pSample* est défini sur **null**.</span><span class="sxs-lookup"><span data-stu-id="28594-194">In this case, the **ReadSample** method returns **S\_OK** because no error has occurred, even though the *pSample* parameter is set to **NULL**.</span></span> <span data-ttu-id="28594-195">Par conséquent, vérifiez toujours la valeur de *pSample* avant de le déréférencer.</span><span class="sxs-lookup"><span data-stu-id="28594-195">Therefore, always check the value of *pSample* before you dereference it.</span></span>

<span data-ttu-id="28594-196">Le code suivant montre comment appeler [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) dans une boucle et vérifier les informations retournées par la méthode, jusqu’à ce que la fin du fichier multimédia soit atteinte.</span><span class="sxs-lookup"><span data-stu-id="28594-196">The following code shows how to call [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) in a loop and check the information returned by the method, until the end of the media file is reached.</span></span>


```C++
HRESULT ProcessSamples(IMFSourceReader *pReader)
{
    HRESULT hr = S_OK;
    IMFSample *pSample = NULL;
    size_t  cSamples = 0;

    bool quit = false;
    while (!quit)
    {
        DWORD streamIndex, flags;
        LONGLONG llTimeStamp;

        hr = pReader->ReadSample(
            MF_SOURCE_READER_ANY_STREAM,    // Stream index.
            0,                              // Flags.
            &streamIndex,                   // Receives the actual stream index. 
            &flags,                         // Receives status flags.
            &llTimeStamp,                   // Receives the time stamp.
            &pSample                        // Receives the sample or NULL.
            );

        if (FAILED(hr))
        {
            break;
        }

        wprintf(L"Stream %d (%I64d)\n", streamIndex, llTimeStamp);
        if (flags & MF_SOURCE_READERF_ENDOFSTREAM)
        {
            wprintf(L"\tEnd of stream\n");
            quit = true;
        }
        if (flags & MF_SOURCE_READERF_NEWSTREAM)
        {
            wprintf(L"\tNew stream\n");
        }
        if (flags & MF_SOURCE_READERF_NATIVEMEDIATYPECHANGED)
        {
            wprintf(L"\tNative type changed\n");
        }
        if (flags & MF_SOURCE_READERF_CURRENTMEDIATYPECHANGED)
        {
            wprintf(L"\tCurrent type changed\n");
        }
        if (flags & MF_SOURCE_READERF_STREAMTICK)
        {
            wprintf(L"\tStream tick\n");
        }

        if (flags & MF_SOURCE_READERF_NATIVEMEDIATYPECHANGED)
        {
            // The format changed. Reconfigure the decoder.
            hr = ConfigureDecoder(pReader, streamIndex);
            if (FAILED(hr))
            {
                break;
            }
        }

        if (pSample)
        {
            ++cSamples;
        }

        SafeRelease(&pSample);
    }

    if (FAILED(hr))
    {
        wprintf(L"ProcessSamples FAILED, hr = 0x%x\n", hr);
    }
    else
    {
        wprintf(L"Processed %d samples\n", cSamples);
    }
    SafeRelease(&pSample);
    return hr;
}
```



## <a name="draining-the-data-pipeline"></a><span data-ttu-id="28594-197">Drainage du pipeline de données</span><span class="sxs-lookup"><span data-stu-id="28594-197">Draining the Data Pipeline</span></span>

<span data-ttu-id="28594-198">Pendant le traitement des données, un décodeur ou une autre transformation peut mettre en mémoire tampon des exemples d’entrée.</span><span class="sxs-lookup"><span data-stu-id="28594-198">During data processing, a decoder or other transform might buffer input samples.</span></span> <span data-ttu-id="28594-199">Dans le diagramme suivant, l’application appelle [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) et reçoit un exemple avec une durée de présentation égale à *T1*.</span><span class="sxs-lookup"><span data-stu-id="28594-199">In the following diagram, the application calls [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) and receives a sample with a presentation time equal to *t1*.</span></span> <span data-ttu-id="28594-200">Le décodeur contient des exemples pour *T2* et *T3*.</span><span class="sxs-lookup"><span data-stu-id="28594-200">The decoder is holding samples for *t2* and *t3*.</span></span>

![illustration qui montre la mise en mémoire tampon dans un décodeur.](images/sourcereader02.png)

<span data-ttu-id="28594-202">Lors du prochain appel à [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample), le lecteur source peut donner à *T4* le décodeur et retourner *T2* à l’application.</span><span class="sxs-lookup"><span data-stu-id="28594-202">On the next call to [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample), the Source Reader might give *t4* to the decoder and return *t2* to the application.</span></span>

<span data-ttu-id="28594-203">Si vous souhaitez décoder tous les exemples actuellement mis en mémoire tampon dans le décodeur, sans passer de nouveaux exemples au décodeur, définissez l’indicateur de **\_ \_ \_ \_ drainage CONTROLF du lecteur source MF** dans le paramètre *dwControlFlags* de [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample).</span><span class="sxs-lookup"><span data-stu-id="28594-203">If you want to decode all of the samples that are currently buffered in the decoder, without passing any new samples to the decoder, set the **MF\_SOURCE\_READER\_CONTROLF\_DRAIN** flag in the *dwControlFlags* parameter of [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample).</span></span> <span data-ttu-id="28594-204">Continuez à effectuer cette opération dans une boucle jusqu’à ce que **ReadSample** retourne un exemple de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="28594-204">Continue to do this in a loop until **ReadSample** returns a **NULL** sample pointer.</span></span> <span data-ttu-id="28594-205">Selon la façon dont le décodeur met en mémoire tampon les exemples, qui peuvent se produire immédiatement ou après plusieurs appels à **ReadSample**.</span><span class="sxs-lookup"><span data-stu-id="28594-205">Depending on how the decoder buffers samples, that might happen immediately or after several calls to **ReadSample**.</span></span>

## <a name="getting-the-file-duration"></a><span data-ttu-id="28594-206">Obtention de la durée du fichier</span><span class="sxs-lookup"><span data-stu-id="28594-206">Getting the File Duration</span></span>

<span data-ttu-id="28594-207">Pour obtenir la durée d’un fichier multimédia, appelez la méthode [**IMFSourceReader :: GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) et demandez l’attribut de [**\_ \_ durée MF PD**](mf-pd-duration-attribute.md) , comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="28594-207">To get the duration of a media file, call the [**IMFSourceReader::GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) method and request the [**MF\_PD\_DURATION**](mf-pd-duration-attribute.md) attribute, as shown in the following code.</span></span>


```C++
HRESULT GetDuration(IMFSourceReader *pReader, LONGLONG *phnsDuration)
{
    PROPVARIANT var;
    HRESULT hr = pReader->GetPresentationAttribute(MF_SOURCE_READER_MEDIASOURCE, 
        MF_PD_DURATION, &var);
    if (SUCCEEDED(hr))
    {
        hr = PropVariantToInt64(var, phnsDuration);
        PropVariantClear(&var);
    }
    return hr;
}
```



<span data-ttu-id="28594-208">La fonction illustrée ici obtient la durée en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="28594-208">The function shown here gets the duration in 100-nanosecond units.</span></span> <span data-ttu-id="28594-209">Divisez par 10 millions pour connaître la durée en secondes.</span><span class="sxs-lookup"><span data-stu-id="28594-209">Divide by 10,000,000 to get the duration in seconds.</span></span>

## <a name="seeking"></a><span data-ttu-id="28594-210">Cherche</span><span class="sxs-lookup"><span data-stu-id="28594-210">Seeking</span></span>

<span data-ttu-id="28594-211">Une source multimédia qui obtient des données à partir d’un fichier local peut généralement Rechercher des positions arbitraires dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="28594-211">A media source that gets data from a local file can usually seek to arbitrary positions in the file.</span></span> <span data-ttu-id="28594-212">Les périphériques de capture tels que les webcams ne peuvent généralement pas être recherchés, car les données sont actives.</span><span class="sxs-lookup"><span data-stu-id="28594-212">Capture devices such as webcams generally cannot seek, because the data is live.</span></span> <span data-ttu-id="28594-213">Une source qui diffuse des données sur un réseau peut être en mesure de rechercher, selon le protocole de streaming réseau.</span><span class="sxs-lookup"><span data-stu-id="28594-213">A source that streams data over a network might be able to seek, depending on the network streaming protocol.</span></span>

<span data-ttu-id="28594-214">Pour déterminer si une source de média peut effectuer une recherche, appelez [**IMFSourceReader :: GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) et demandez l’attribut de [ \_ \_ \_ \_ caractéristiques de lecteur de source MF](mf-source-reader-mediasource-characteristics.md) , comme indiqué dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="28594-214">To find out whether a media source can seek, call [**IMFSourceReader::GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) and request the [MF\_SOURCE\_READER\_MEDIASOURCE\_CHARACTERISTICS](mf-source-reader-mediasource-characteristics.md) attribute, as shown in the following code:</span></span>


```C++
HRESULT GetSourceFlags(IMFSourceReader *pReader, ULONG *pulFlags)
{
    ULONG flags = 0;

    PROPVARIANT var;
    PropVariantInit(&var);

    HRESULT hr = pReader->GetPresentationAttribute(
        MF_SOURCE_READER_MEDIASOURCE, 
        MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS, 
        &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt32(var, &flags);
    }
    if (SUCCEEDED(hr))
    {
        *pulFlags = flags;
    }

    PropVariantClear(&var);
    return hr;
}
```



<span data-ttu-id="28594-215">Cette fonction obtient un jeu d’indicateurs de fonctionnalités à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="28594-215">This function gets a set of capabilities flags from the source.</span></span> <span data-ttu-id="28594-216">Ces indicateurs sont définis dans l’énumération des [**\_ caractéristiques MFMEDIASOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) .</span><span class="sxs-lookup"><span data-stu-id="28594-216">These flags are defined in the [**MFMEDIASOURCE\_CHARACTERISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) enumeration.</span></span> <span data-ttu-id="28594-217">Deux indicateurs sont liés à la recherche :</span><span class="sxs-lookup"><span data-stu-id="28594-217">Two flags relate to seeking:</span></span>



| <span data-ttu-id="28594-218">Indicateur</span><span class="sxs-lookup"><span data-stu-id="28594-218">Flag</span></span>                                                                                                                                      | <span data-ttu-id="28594-219">Description</span><span class="sxs-lookup"><span data-stu-id="28594-219">Description</span></span>                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28594-220"><span id="MFMEDIASOURCE_CAN_SEEK"></span><span id="mfmediasource_can_seek"></span>**MFMEDIASOURCE \_ peut \_ Rechercher**</span><span class="sxs-lookup"><span data-stu-id="28594-220"><span id="MFMEDIASOURCE_CAN_SEEK"></span><span id="mfmediasource_can_seek"></span>**MFMEDIASOURCE\_CAN\_SEEK**</span></span><br/>                 | <span data-ttu-id="28594-221">La source peut effectuer une recherche.</span><span class="sxs-lookup"><span data-stu-id="28594-221">The source can seek.</span></span><br/>                                                                                                                                                                            |
| <span data-ttu-id="28594-222"><span id="MFMEDIASOURCE_HAS_SLOW_SEEK"></span><span id="mfmediasource_has_slow_seek"></span>**MFMEDIASOURCE \_ a \_ une \_ recherche lente**</span><span class="sxs-lookup"><span data-stu-id="28594-222"><span id="MFMEDIASOURCE_HAS_SLOW_SEEK"></span><span id="mfmediasource_has_slow_seek"></span>**MFMEDIASOURCE\_HAS\_SLOW\_SEEK**</span></span><br/> | <span data-ttu-id="28594-223">La recherche peut prendre beaucoup de temps.</span><span class="sxs-lookup"><span data-stu-id="28594-223">Seeking might take a long time to complete.</span></span> <span data-ttu-id="28594-224">Par exemple, la source doit peut-être télécharger l’intégralité du fichier avant de pouvoir effectuer une recherche.</span><span class="sxs-lookup"><span data-stu-id="28594-224">For example, the source might need to download the entire file before it can seek.</span></span> <span data-ttu-id="28594-225">(Il n’existe aucun critère strict pour qu’une source retourne cet indicateur.)</span><span class="sxs-lookup"><span data-stu-id="28594-225">(There are no strict criteria for a source to return this flag.)</span></span><br/> |



 

<span data-ttu-id="28594-226">Les tests de code suivants pour le **MFMEDIASOURCE \_ peuvent \_ Rechercher** l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="28594-226">The following code tests for the **MFMEDIASOURCE\_CAN\_SEEK** flag.</span></span>


```C++
BOOL SourceCanSeek(IMFSourceReader *pReader)
{
    BOOL bCanSeek = FALSE;
    ULONG flags;
    if (SUCCEEDED(GetSourceFlags(pReader, &flags)))
    {
        bCanSeek = ((flags & MFMEDIASOURCE_CAN_SEEK) == MFMEDIASOURCE_CAN_SEEK);
    }
    return bCanSeek;
}
```



<span data-ttu-id="28594-227">Pour effectuer une recherche, appelez la méthode [**IMFSourceReader :: SetCurrentPosition**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentposition) , comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="28594-227">To seek, call the [**IMFSourceReader::SetCurrentPosition**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentposition) method, as shown in the following code.</span></span>


```C++
HRESULT SetPosition(IMFSourceReader *pReader, const LONGLONG& hnsPosition)
{
    PROPVARIANT var;
    HRESULT hr = InitPropVariantFromInt64(hnsPosition, &var);
    if (SUCCEEDED(hr))
    {
        hr = pReader->SetCurrentPosition(GUID_NULL, var);
        PropVariantClear(&var);
    }
    return hr;
}
```



<span data-ttu-id="28594-228">Le premier paramètre indique le format d’heure que vous utilisez pour spécifier la position de recherche.</span><span class="sxs-lookup"><span data-stu-id="28594-228">The first parameter gives the time format that you are using to specify the seek position.</span></span> <span data-ttu-id="28594-229">Toutes les sources de média dans Media Foundation sont requises pour prendre en charge des unités de 100 nanosecondes, indiquées par la valeur **GUID \_ null**.</span><span class="sxs-lookup"><span data-stu-id="28594-229">All media sources in Media Foundation are required to support 100-nanosecond units, indicated by the value **GUID\_NULL**.</span></span> <span data-ttu-id="28594-230">Le deuxième paramètre est un **PROPVARIANT** qui contient la position de recherche.</span><span class="sxs-lookup"><span data-stu-id="28594-230">The second parameter is a **PROPVARIANT** that contains the seek position.</span></span> <span data-ttu-id="28594-231">Pour les unités de temps de 100 nanosecondes, le type de données est **LongLong**.</span><span class="sxs-lookup"><span data-stu-id="28594-231">For 100-nanosecond time units, the data type is **LONGLONG**.</span></span>

<span data-ttu-id="28594-232">N’oubliez pas que chaque source de média ne fournit pas de recherche de trame précise.</span><span class="sxs-lookup"><span data-stu-id="28594-232">Be aware that not every media source provides frame-accurate seeking.</span></span> <span data-ttu-id="28594-233">La précision de la recherche dépend de plusieurs facteurs, tels que l’intervalle d’image clé, le fait que le fichier multimédia contient un index et si les données ont une vitesse de transmission constante ou variable.</span><span class="sxs-lookup"><span data-stu-id="28594-233">The accuracy of seeking depends on several factors, such as the key frame interval, whether the media file contains an index, and whether the data has a constant or variable bit rate.</span></span> <span data-ttu-id="28594-234">Par conséquent, une fois que vous avez effectué une recherche sur une position dans un fichier, il n’y a aucune garantie que l’horodatage sur l’échantillon suivant correspond exactement à la position demandée.</span><span class="sxs-lookup"><span data-stu-id="28594-234">Therefore, after you seek to a position in a file, there is no guarantee that the time stamp on the next sample will exactly match the requested position.</span></span> <span data-ttu-id="28594-235">En règle générale, la position réelle n’est pas postérieure à la position demandée. vous pouvez donc ignorer des échantillons jusqu’à ce que vous atteigniez le point souhaité dans le flux.</span><span class="sxs-lookup"><span data-stu-id="28594-235">Generally, the actual position will not be later than the requested position, so you can discard samples until you reach the desired point in the stream.</span></span>

## <a name="playback-rate"></a><span data-ttu-id="28594-236">Vitesse de lecture</span><span class="sxs-lookup"><span data-stu-id="28594-236">Playback Rate</span></span>

<span data-ttu-id="28594-237">Bien que vous puissiez définir la vitesse de lecture à l’aide du lecteur source, cela n’est généralement pas très utile pour les raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="28594-237">Although you can set the playback rate using the Source Reader, doing is typically not very useful, for the following reasons:</span></span>

-   <span data-ttu-id="28594-238">Le lecteur source ne prend pas en charge la lecture inversée, même si la source du média le fait.</span><span class="sxs-lookup"><span data-stu-id="28594-238">The Source Reader does not support reverse playback, even if the media source does.</span></span>
-   <span data-ttu-id="28594-239">L’application contrôle les durées de présentation, de sorte que l’application peut implémenter une lecture rapide ou lente sans définir la vitesse sur la source.</span><span class="sxs-lookup"><span data-stu-id="28594-239">The application controls the presentation times, so the application can implement fast or slow play without setting the rate on the source.</span></span>
-   <span data-ttu-id="28594-240">Certaines sources multimédias prennent en charge le mode de réglage de l' *épaisseur* , où la source fournit moins d’échantillons, en général uniquement les images clés.</span><span class="sxs-lookup"><span data-stu-id="28594-240">Some media sources support *thinning* mode, where the source delivers fewer samples—typically just the key frames.</span></span> <span data-ttu-id="28594-241">Toutefois, si vous souhaitez supprimer des images non-clés, vous pouvez vérifier chaque exemple pour l’attribut [MFSampleExtension \_ CleanPoint](mfsampleextension-cleanpoint-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="28594-241">However, if you want to drop non-key frames, you can check each sample for the [MFSampleExtension\_CleanPoint](mfsampleextension-cleanpoint-attribute.md) attribute.</span></span>

<span data-ttu-id="28594-242">Pour définir la vitesse de lecture à l’aide du lecteur source, appelez la méthode [**IMFSourceReader :: GetServiceForStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getserviceforstream) pour récupérer les interfaces [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) et [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) à partir de la source du média.</span><span class="sxs-lookup"><span data-stu-id="28594-242">To set the playback rate using the Source Reader, call the [**IMFSourceReader::GetServiceForStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getserviceforstream) method to get the [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) and [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) interfaces from the media source.</span></span>

## <a name="hardware-acceleration"></a><span data-ttu-id="28594-243">Accélération matérielle</span><span class="sxs-lookup"><span data-stu-id="28594-243">Hardware Acceleration</span></span>

<span data-ttu-id="28594-244">Le lecteur source est compatible avec Microsoft DirectX Video Acceleration (DXVA) 2,0 pour le décodage vidéo à accélération matérielle.</span><span class="sxs-lookup"><span data-stu-id="28594-244">The Source Reader is compatible with Microsoft DirectX Video Acceleration (DXVA) 2.0 for hardware accelerated video decoding.</span></span> <span data-ttu-id="28594-245">Pour utiliser DXVA avec le lecteur source, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="28594-245">To use DXVA with the Source Reader, perform the following steps.</span></span>

1.  <span data-ttu-id="28594-246">Créez un appareil Microsoft Direct3D.</span><span class="sxs-lookup"><span data-stu-id="28594-246">Create a Microsoft Direct3D device.</span></span>
2.  <span data-ttu-id="28594-247">Appelez la fonction [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9) pour créer le gestionnaire de périphériques Direct3D.</span><span class="sxs-lookup"><span data-stu-id="28594-247">Call the [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9) function to create the Direct3D device manager.</span></span> <span data-ttu-id="28594-248">Cette fonction obtient un pointeur vers l’interface [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) .</span><span class="sxs-lookup"><span data-stu-id="28594-248">This function gets a pointer to the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface.</span></span>
3.  <span data-ttu-id="28594-249">Appelez la méthode [**IDirect3DDeviceManager9 :: ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) avec un pointeur vers le périphérique Direct3D.</span><span class="sxs-lookup"><span data-stu-id="28594-249">Call the [**IDirect3DDeviceManager9::ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) method with a pointer to the Direct3D device.</span></span>
4.  <span data-ttu-id="28594-250">Créez un magasin d’attributs en appelant la fonction [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) .</span><span class="sxs-lookup"><span data-stu-id="28594-250">Create an attribute store by calling the [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) function.</span></span>
5.  <span data-ttu-id="28594-251">Créez le lecteur source.</span><span class="sxs-lookup"><span data-stu-id="28594-251">Create the Source Reader.</span></span> <span data-ttu-id="28594-252">Transmettez le magasin d’attributs dans le paramètre *pAttributes* de la fonction de création.</span><span class="sxs-lookup"><span data-stu-id="28594-252">Pass the attribute store in the *pAttributes* parameter of the creation function.</span></span>

<span data-ttu-id="28594-253">Lorsque vous fournissez un appareil Direct3D, le lecteur source alloue des exemples vidéo compatibles avec l’API de processeur vidéo DXVA.</span><span class="sxs-lookup"><span data-stu-id="28594-253">When you provide a Direct3D device, the Source Reader allocates video samples that are compatible with the DXVA video processor API.</span></span> <span data-ttu-id="28594-254">Vous pouvez utiliser le traitement vidéo DXVA pour effectuer la désentrelacement du matériel ou le mixage vidéo.</span><span class="sxs-lookup"><span data-stu-id="28594-254">You can use DXVA video processing to perform hardware deinterlacing or video mixing.</span></span> <span data-ttu-id="28594-255">Pour plus d’informations, consultez la page [traitement vidéo DXVA](dxva-video-processing.md).</span><span class="sxs-lookup"><span data-stu-id="28594-255">For more information, see [DXVA Video Processing](dxva-video-processing.md).</span></span> <span data-ttu-id="28594-256">En outre, si le décodeur prend en charge la 2,0 DXVA, il utilisera le périphérique Direct3D pour effectuer un décodage accéléré par le matériel.</span><span class="sxs-lookup"><span data-stu-id="28594-256">Also, if the decoder supports DXVA 2.0, it will use the Direct3D device to perform hardware-accelerated decoding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="28594-257">À compter de Windows 8, [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) peut être utilisé à la place de [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9).</span><span class="sxs-lookup"><span data-stu-id="28594-257">Beginning in Windows 8, [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) can be used instead of the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9).</span></span> <span data-ttu-id="28594-258">Pour les applications du Windows Store, vous devez utiliser **IMFDXGIDeviceManager**.</span><span class="sxs-lookup"><span data-stu-id="28594-258">For Windows Store apps, you must use **IMFDXGIDeviceManager**.</span></span> <span data-ttu-id="28594-259">Pour plus d’informations, consultez les [API vidéo Direct3D 11](direct3d-11-video-apis.md).</span><span class="sxs-lookup"><span data-stu-id="28594-259">For more info, see the [Direct3D 11 Video APIs](direct3d-11-video-apis.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="28594-260">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="28594-260">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28594-261">Lecteur source</span><span class="sxs-lookup"><span data-stu-id="28594-261">Source Reader</span></span>](source-reader.md)
</dt> </dl>

 

 




