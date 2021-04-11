---
description: Ce didacticiel montre comment utiliser l’API de transcodage pour encoder un fichier MP4 à l’aide de H. 264 pour le flux vidéo et AAC pour le flux audio.
ms.assetid: 60873aa6-46ec-4a73-94b9-0d8ac602f850
title: 'Didacticiel : encodage d’un fichier MP4'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae895ef321b35f080bf946384ee32d83c2c539fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202247"
---
# <a name="tutorial-encoding-an-mp4-file"></a><span data-ttu-id="33226-103">Didacticiel : encodage d’un fichier MP4</span><span class="sxs-lookup"><span data-stu-id="33226-103">Tutorial: Encoding an MP4 File</span></span>

<span data-ttu-id="33226-104">Ce didacticiel montre comment utiliser l' [API de transcodage](transcode-api.md) pour encoder un fichier MP4 à l’aide de H. 264 pour le flux vidéo et AAC pour le flux audio.</span><span class="sxs-lookup"><span data-stu-id="33226-104">This tutorial shows how to use the [Transcode API](transcode-api.md) to encode an MP4 file, using H.264 for the video stream and AAC for the audio stream.</span></span>

-   [<span data-ttu-id="33226-105">En-têtes et fichiers de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="33226-105">Headers and Library Files</span></span>](#headers-and-library-files)
-   [<span data-ttu-id="33226-106">Définir les profils d’encodage</span><span class="sxs-lookup"><span data-stu-id="33226-106">Define the Encoding Profiles</span></span>](#define-the-encoding-profiles)
-   [<span data-ttu-id="33226-107">Écrire la fonction wmain</span><span class="sxs-lookup"><span data-stu-id="33226-107">Write the wmain Function</span></span>](#write-the-wmain-function)
-   [<span data-ttu-id="33226-108">Encoder le fichier</span><span class="sxs-lookup"><span data-stu-id="33226-108">Encode the File</span></span>](#encode-the-file)
    -   [<span data-ttu-id="33226-109">Créer la source du média</span><span class="sxs-lookup"><span data-stu-id="33226-109">Create the Media Source</span></span>](#create-the-media-source)
    -   [<span data-ttu-id="33226-110">Obtient la durée de la source</span><span class="sxs-lookup"><span data-stu-id="33226-110">Get the Source Duration</span></span>](#get-the-source-duration)
    -   [<span data-ttu-id="33226-111">Créer le profil de transcodage</span><span class="sxs-lookup"><span data-stu-id="33226-111">Create the Transcode Profile</span></span>](#create-the-transcode-profile)
    -   [<span data-ttu-id="33226-112">Exécuter la session d’encodage</span><span class="sxs-lookup"><span data-stu-id="33226-112">Run the Encoding Session</span></span>](#run-the-encoding-session)
-   [<span data-ttu-id="33226-113">Assistance de session multimédia</span><span class="sxs-lookup"><span data-stu-id="33226-113">Media Session Helper</span></span>](#media-session-helper)
-   [<span data-ttu-id="33226-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="33226-114">Related topics</span></span>](#related-topics)

## <a name="headers-and-library-files"></a><span data-ttu-id="33226-115">En-têtes et fichiers de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="33226-115">Headers and Library Files</span></span>

<span data-ttu-id="33226-116">Incluez les fichiers d’en-tête suivants.</span><span class="sxs-lookup"><span data-stu-id="33226-116">Include the following header files.</span></span>


```C++
#include <new>
#include <iostream>
#include <windows.h>
#include <mfapi.h>
#include <Mfidl.h>
#include <shlwapi.h>
```



<span data-ttu-id="33226-117">Liez les fichiers de bibliothèque suivants.</span><span class="sxs-lookup"><span data-stu-id="33226-117">Link the following library files.</span></span>


```C++
#pragma comment(lib, "mfplat")
#pragma comment(lib, "mf")
#pragma comment(lib, "mfuuid")
#pragma comment(lib, "shlwapi")
```



## <a name="define-the-encoding-profiles"></a><span data-ttu-id="33226-118">Définir les profils d’encodage</span><span class="sxs-lookup"><span data-stu-id="33226-118">Define the Encoding Profiles</span></span>

<span data-ttu-id="33226-119">L’une des approches de l’encodage consiste à définir une liste de profils d’encodage cibles connus à l’avance.</span><span class="sxs-lookup"><span data-stu-id="33226-119">One approach to encoding is to define a list of target encoding profiles that are known in advance.</span></span> <span data-ttu-id="33226-120">Pour ce didacticiel, nous prenons une approche relativement simple et stockons une liste de formats d’encodage pour la vidéo H. 264 et l’audio AAC.</span><span class="sxs-lookup"><span data-stu-id="33226-120">For this tutorial, we take a relatively simple approach, and store a list of encoding formats for H.264 video and AAC audio.</span></span>

<span data-ttu-id="33226-121">Pour H. 264, les attributs de format les plus importants sont le profil H. 264, la fréquence d’images, la taille de trame et la vitesse de transmission encodée.</span><span class="sxs-lookup"><span data-stu-id="33226-121">For H.264, the most important format attributes are the H.264 profile, the frame rate, the frame size, and the encoded bit rate.</span></span> <span data-ttu-id="33226-122">Le tableau suivant contient une liste de formats d’encodage H. 264.</span><span class="sxs-lookup"><span data-stu-id="33226-122">The following array contains a list of H.264 encoding formats.</span></span>


```C++
struct H264ProfileInfo
{
    UINT32  profile;
    MFRatio fps;
    MFRatio frame_size;
    UINT32  bitrate;
};

H264ProfileInfo h264_profiles[] = 
{
    { eAVEncH264VProfile_Base, { 15, 1 },       { 176, 144 },   128000 },
    { eAVEncH264VProfile_Base, { 15, 1 },       { 352, 288 },   384000 },
    { eAVEncH264VProfile_Base, { 30, 1 },       { 352, 288 },   384000 },
    { eAVEncH264VProfile_Base, { 29970, 1000 }, { 320, 240 },   528560 },
    { eAVEncH264VProfile_Base, { 15, 1 },       { 720, 576 },  4000000 },
    { eAVEncH264VProfile_Main, { 25, 1 },       { 720, 576 }, 10000000 },
    { eAVEncH264VProfile_Main, { 30, 1 },       { 352, 288 }, 10000000 },
};
```



<span data-ttu-id="33226-123">Les profils H. 264 sont spécifiés à l’aide de l’énumération [**eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) .</span><span class="sxs-lookup"><span data-stu-id="33226-123">H.264 profiles are specified using the [**eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) enumeration.</span></span> <span data-ttu-id="33226-124">Vous pouvez également spécifier le niveau H. 264, mais le Microsoft Media Foundation de l' [**encodeur vidéo h. 264**](h-264-video-encoder.md) peut dériver le niveau approprié pour un flux vidéo donné. il est donc recommandé de ne pas remplacer le niveau sélectionné de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="33226-124">You could also specify the H.264 level, but the Microsoft Media Foundation [**H.264 Video Encoder**](h-264-video-encoder.md) can derive the proper level for a given video stream, so it is recommended not to override the encoder's selected level.</span></span> <span data-ttu-id="33226-125">Pour le contenu entrelacé, vous devez également spécifier le mode entrelacé (voir entrelacement de [vidéos](video-interlacing.md)).</span><span class="sxs-lookup"><span data-stu-id="33226-125">For interlaced content, you would also specify the interlace mode (see [Video Interlacing](video-interlacing.md)).</span></span>

<span data-ttu-id="33226-126">Pour l’audio AAC, les attributs de format les plus importants sont le taux d’échantillonnage audio, le nombre de canaux, le nombre de bits par échantillon et la vitesse de transmission encodée.</span><span class="sxs-lookup"><span data-stu-id="33226-126">For AAC audio, the most important format attributes are the audio sample rate, the number of channels, the number of bits per sample, and the encoded bit rate.</span></span> <span data-ttu-id="33226-127">Si vous le souhaitez, vous pouvez définir l’indication du niveau de profil audio AAC.</span><span class="sxs-lookup"><span data-stu-id="33226-127">Optionally, you can set the AAC audio profile level indication.</span></span> <span data-ttu-id="33226-128">Pour plus d’informations, consultez l' [**encodeur AAC**](aac-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="33226-128">For more information, see [**AAC Encoder**](aac-encoder.md).</span></span> <span data-ttu-id="33226-129">Le tableau suivant contient une liste de formats d’encodage AAC.</span><span class="sxs-lookup"><span data-stu-id="33226-129">The following array contains a list of AAC encoding formats.</span></span>


```C++
struct AACProfileInfo
{
    UINT32  samplesPerSec;
    UINT32  numChannels;
    UINT32  bitsPerSample;
    UINT32  bytesPerSec;
    UINT32  aacProfile;
};

AACProfileInfo aac_profiles[] = 
{
    { 96000, 2, 16, 24000, 0x29}, 
    { 48000, 2, 16, 24000, 0x29}, 
    { 44100, 2, 16, 16000, 0x29}, 
    { 44100, 2, 16, 12000, 0x29}, 
};
```



> [!Note]  
> <span data-ttu-id="33226-130">Les `H264ProfileInfo` `AACProfileInfo` structures et définies ici ne font pas partie de l’API Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="33226-130">The `H264ProfileInfo` and `AACProfileInfo` structures defined here are not part of the Media Foundation API.</span></span>

 

## <a name="write-the-wmain-function"></a><span data-ttu-id="33226-131">Écrire la fonction wmain</span><span class="sxs-lookup"><span data-stu-id="33226-131">Write the wmain Function</span></span>

<span data-ttu-id="33226-132">Le code suivant montre le point d’entrée pour l’application console.</span><span class="sxs-lookup"><span data-stu-id="33226-132">The following code shows the entry point for the console application.</span></span>


```C++
int video_profile = 0;
int audio_profile = 0;

int wmain(int argc, wchar_t* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc < 3 || argc > 5)
    {
        std::cout << "Usage:" << std::endl;
        std::cout << "input output [ audio_profile video_profile ]" << std::endl;
        return 1;
    }

    if (argc > 3)
    {
        audio_profile = _wtoi(argv[3]);
    }
    if (argc > 4)
    {
        video_profile = _wtoi(argv[4]);
    }

    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (SUCCEEDED(hr))
    {
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            hr = EncodeFile(argv[1], argv[2]);
            MFShutdown();
        }
        CoUninitialize();
    }

    if (SUCCEEDED(hr))
    {
        std::cout << "Done." << std::endl;
    }
    else
    {
        std::cout << "Error: " << std::hex << hr << std::endl;
    }

    return 0;
}
```



<span data-ttu-id="33226-133">La `wmain` fonction effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="33226-133">The `wmain` function does the following:</span></span>

1.  <span data-ttu-id="33226-134">Appelle la fonction [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) pour initialiser la bibliothèque com.</span><span class="sxs-lookup"><span data-stu-id="33226-134">Calls the [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) function to initialize the COM library.</span></span>
2.  <span data-ttu-id="33226-135">Appelle la fonction [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) pour initialiser Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="33226-135">Calls the [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function to initialize Media Foundation.</span></span>
3.  <span data-ttu-id="33226-136">Appelle la fonction définie par l’application `EncodeFile` .</span><span class="sxs-lookup"><span data-stu-id="33226-136">Calls the application-defined `EncodeFile` function.</span></span> <span data-ttu-id="33226-137">Cette fonction transcode le fichier d’entrée dans le fichier de sortie et s’affiche dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="33226-137">This function transcodes the input file to the output file, and is shown in the next section.</span></span>
4.  <span data-ttu-id="33226-138">Appelle la fonction [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) pour arrêter Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="33226-138">Calls the [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) function to shut down Media Foundation.</span></span>
5.  <span data-ttu-id="33226-139">Appelez la fonction [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) pour désinitialiser la bibliothèque com.</span><span class="sxs-lookup"><span data-stu-id="33226-139">Call the [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) function to uninitialize the COM library.</span></span>

## <a name="encode-the-file"></a><span data-ttu-id="33226-140">Encoder le fichier</span><span class="sxs-lookup"><span data-stu-id="33226-140">Encode the File</span></span>

<span data-ttu-id="33226-141">Le code suivant illustre la `EncodeFile` fonction, qui effectue le transcodage.</span><span class="sxs-lookup"><span data-stu-id="33226-141">The following code shows `EncodeFile` function, which performs the transcoding.</span></span> <span data-ttu-id="33226-142">Cette fonction se compose principalement d’appels à d’autres fonctions définies par l’application, qui sont présentées plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="33226-142">This function consists mostly of calls to other application-defined functions, which are shown later in this topic.</span></span>


```C++
HRESULT EncodeFile(PCWSTR pszInput, PCWSTR pszOutput)
{
    IMFTranscodeProfile *pProfile = NULL;
    IMFMediaSource *pSource = NULL;
    IMFTopology *pTopology = NULL;
    CSession *pSession = NULL;

    MFTIME duration = 0;

    HRESULT hr = CreateMediaSource(pszInput, &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = GetSourceDuration(pSource, &duration);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CreateTranscodeProfile(&pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateTranscodeTopology(pSource, pszOutput, pProfile, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CSession::Create(&pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSession->StartEncodingSession(pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = RunEncodingSession(pSession, duration);

done:            
    if (pSource)
    {
        pSource->Shutdown();
    }

    SafeRelease(&pSession);
    SafeRelease(&pProfile);
    SafeRelease(&pSource);
    SafeRelease(&pTopology);
    return hr;
}
```



<span data-ttu-id="33226-143">La `EncodeFile` fonction effectue les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="33226-143">The `EncodeFile` function performs the following steps.</span></span>

1.  <span data-ttu-id="33226-144">Crée une source de média pour le fichier d’entrée, à l’aide de l’URL ou du chemin d’accès du fichier d’entrée.</span><span class="sxs-lookup"><span data-stu-id="33226-144">Creates a media source for the input file, using the URL or file path of the input file.</span></span> <span data-ttu-id="33226-145">(Consultez [créer la source du média](#create-the-media-source).)</span><span class="sxs-lookup"><span data-stu-id="33226-145">(See [Create the Media Source](#create-the-media-source).)</span></span>
2.  <span data-ttu-id="33226-146">Obtient la durée du fichier d’entrée.</span><span class="sxs-lookup"><span data-stu-id="33226-146">Gets the duration of the input file.</span></span> <span data-ttu-id="33226-147">(Consultez [obtenir la durée de la source](#get-the-source-duration).)</span><span class="sxs-lookup"><span data-stu-id="33226-147">(See [Get the Source Duration](#get-the-source-duration).)</span></span>
3.  <span data-ttu-id="33226-148">Créez le profil de transcodage.</span><span class="sxs-lookup"><span data-stu-id="33226-148">Create the transcode profile.</span></span> <span data-ttu-id="33226-149">(Consultez [créer le profil de transcodage](#create-the-transcode-profile).)</span><span class="sxs-lookup"><span data-stu-id="33226-149">(See [Create the Transcode Profile](#create-the-transcode-profile).)</span></span>
4.  <span data-ttu-id="33226-150">Appelez [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) pour créer la topologie de transcodage partielle.</span><span class="sxs-lookup"><span data-stu-id="33226-150">Call [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) to create the partial transcode topology.</span></span>
5.  <span data-ttu-id="33226-151">Créez un objet d’assistance qui gère la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="33226-151">Create a helper object that manages the Media Session.</span></span> <span data-ttu-id="33226-152">(Voir Media session Helper).</span><span class="sxs-lookup"><span data-stu-id="33226-152">(See Media Session Helper).</span></span>
6.  <span data-ttu-id="33226-153">Exécutez la session d’encodage et attendez qu’elle se termine.</span><span class="sxs-lookup"><span data-stu-id="33226-153">Run the encoding session and wait for it to complete.</span></span> <span data-ttu-id="33226-154">(Consultez [exécuter la session d’encodage](#run-the-encoding-session).)</span><span class="sxs-lookup"><span data-stu-id="33226-154">(See [Run the Encoding Session](#run-the-encoding-session).)</span></span>
7.  <span data-ttu-id="33226-155">Appelez [**IMFMediaSource :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) pour arrêter la source du média.</span><span class="sxs-lookup"><span data-stu-id="33226-155">Call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) to shut down the media source.</span></span>
8.  <span data-ttu-id="33226-156">Mise en sortie des pointeurs d’interface.</span><span class="sxs-lookup"><span data-stu-id="33226-156">Release interface pointers.</span></span> <span data-ttu-id="33226-157">Ce code utilise la fonction [SafeRelease](saferelease.md) pour libérer des pointeurs d’interface.</span><span class="sxs-lookup"><span data-stu-id="33226-157">This code uses the [SafeRelease](saferelease.md) function to release interface pointers.</span></span> <span data-ttu-id="33226-158">Une autre option consiste à utiliser une classe de pointeur intelligent COM, telle que **CComPtr**.</span><span class="sxs-lookup"><span data-stu-id="33226-158">Another option is to use a COM smart pointer class, such as **CComPtr**.</span></span>

### <a name="create-the-media-source"></a><span data-ttu-id="33226-159">Créer la source du média</span><span class="sxs-lookup"><span data-stu-id="33226-159">Create the Media Source</span></span>

<span data-ttu-id="33226-160">La source du média est l’objet qui lit et analyse le fichier d’entrée.</span><span class="sxs-lookup"><span data-stu-id="33226-160">The media source is the object that reads and parses the input file.</span></span> <span data-ttu-id="33226-161">Pour créer la source du média, transmettez l’URL du fichier d’entrée au programme de [résolution source](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="33226-161">To create the media source, pass the URL of the input file to the [Source Resolver](source-resolver.md).</span></span> <span data-ttu-id="33226-162">Le code suivant montre comment procéder.</span><span class="sxs-lookup"><span data-stu-id="33226-162">The following code shows how to do this.</span></span>


```C++
HRESULT CreateMediaSource(PCWSTR pszURL, IMFMediaSource **ppSource)
{
    MF_OBJECT_TYPE ObjectType = MF_OBJECT_INVALID;

    IMFSourceResolver* pResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pResolver);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use the source resolver to create the media source
    hr = pResolver->CreateObjectFromURL(pszURL, MF_RESOLUTION_MEDIASOURCE, 
        NULL, &ObjectType, &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the IMFMediaSource interface from the media source.
    hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));

done:
    SafeRelease(&pResolver);
    SafeRelease(&pSource);
    return hr;
}
```



<span data-ttu-id="33226-163">Pour plus d’informations, consultez [utilisation du programme de résolution source](using-the-source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="33226-163">For more information, see [Using the Source Resolver](using-the-source-resolver.md).</span></span>

### <a name="get-the-source-duration"></a><span data-ttu-id="33226-164">Obtient la durée de la source</span><span class="sxs-lookup"><span data-stu-id="33226-164">Get the Source Duration</span></span>

<span data-ttu-id="33226-165">Bien que cela ne soit pas obligatoire, il est utile d’interroger la source du média pendant la durée du fichier d’entrée.</span><span class="sxs-lookup"><span data-stu-id="33226-165">Although not required, it is useful to query the media source for the duration of the input file.</span></span> <span data-ttu-id="33226-166">Cette valeur peut être utilisée pour suivre la progression de l’encodage.</span><span class="sxs-lookup"><span data-stu-id="33226-166">This value can be used to track the encoding progress.</span></span> <span data-ttu-id="33226-167">La durée est stockée dans l’attribut de [**\_ \_ durée MF PD**](mf-pd-duration-attribute.md) du descripteur de présentation.</span><span class="sxs-lookup"><span data-stu-id="33226-167">The duration is stored in the [**MF\_PD\_DURATION**](mf-pd-duration-attribute.md) attribute of the presentation descriptor.</span></span> <span data-ttu-id="33226-168">Récupérez le descripteur de présentation en appelant [**IMFMediaSource :: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="33226-168">Get the presentation descriptor by calling [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span>


```C++
HRESULT GetSourceDuration(IMFMediaSource *pSource, MFTIME *pDuration)
{
    *pDuration = 0;

    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_DURATION, (UINT64*)pDuration);
        pPD->Release();
    }
    return hr;
}
```



### <a name="create-the-transcode-profile"></a><span data-ttu-id="33226-169">Créer le profil de transcodage</span><span class="sxs-lookup"><span data-stu-id="33226-169">Create the Transcode Profile</span></span>

<span data-ttu-id="33226-170">Le profil de transcodage décrit les paramètres d’encodage.</span><span class="sxs-lookup"><span data-stu-id="33226-170">The transcode profile describes the encoding parameters.</span></span> <span data-ttu-id="33226-171">Pour plus d’informations sur la création d’un profil de transcodage, consultez [utilisation de l’API de transcodage](fast-transcode-objects.md).</span><span class="sxs-lookup"><span data-stu-id="33226-171">For more information about creating a transcode profile, see [Using the Transcode API](fast-transcode-objects.md).</span></span> <span data-ttu-id="33226-172">Pour créer le profil, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="33226-172">To create the profile, perform the following steps.</span></span>

1.  <span data-ttu-id="33226-173">Appelez [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) pour créer le profil vide.</span><span class="sxs-lookup"><span data-stu-id="33226-173">Call [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) to create the empty profile.</span></span>
2.  <span data-ttu-id="33226-174">Créez un type de média pour le flux audio AAC.</span><span class="sxs-lookup"><span data-stu-id="33226-174">Create a media type for the AAC audio stream.</span></span> <span data-ttu-id="33226-175">Ajoutez-le au profil en appelant [**IMFTranscodeProfile :: SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes).</span><span class="sxs-lookup"><span data-stu-id="33226-175">Add it to the profile by calling [**IMFTranscodeProfile::SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes).</span></span>
3.  <span data-ttu-id="33226-176">Créez un type de média pour le flux vidéo H. 264.</span><span class="sxs-lookup"><span data-stu-id="33226-176">Create a media type for the H.264 video stream.</span></span> <span data-ttu-id="33226-177">Ajoutez-le au profil en appelant [**IMFTranscodeProfile :: SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes).</span><span class="sxs-lookup"><span data-stu-id="33226-177">Add it to the profile by calling [**IMFTranscodeProfile::SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes).</span></span>
4.  <span data-ttu-id="33226-178">Appelez [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) pour créer un magasin d’attributs pour les attributs de niveau conteneur.</span><span class="sxs-lookup"><span data-stu-id="33226-178">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create an attribute store for the container-level attributes.</span></span>
5.  <span data-ttu-id="33226-179">Définissez l' [attribut \_ \_ CONTAINERTYPE de transcodage MF](mf-transcode-containertype.md) .</span><span class="sxs-lookup"><span data-stu-id="33226-179">Set the [MF\_TRANSCODE\_CONTAINERTYPE](mf-transcode-containertype.md) attribute.</span></span> <span data-ttu-id="33226-180">Il s’agit du seul attribut requis au niveau du conteneur.</span><span class="sxs-lookup"><span data-stu-id="33226-180">This is the only required container-level attribute.</span></span> <span data-ttu-id="33226-181">Pour la sortie de fichier MP4, définissez cet attribut sur **MFTranscodeContainerType \_ MPEG4**.</span><span class="sxs-lookup"><span data-stu-id="33226-181">For MP4 file output, set this attribute to **MFTranscodeContainerType\_MPEG4**.</span></span>
6.  <span data-ttu-id="33226-182">Appelez [**IMFTranscodeProfile :: SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) pour définir les attributs au niveau du conteneur.</span><span class="sxs-lookup"><span data-stu-id="33226-182">Call [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) to set the container-level attributes.</span></span>

<span data-ttu-id="33226-183">Le code suivant illustre ces étapes.</span><span class="sxs-lookup"><span data-stu-id="33226-183">The following code shows these steps.</span></span>


```C++
HRESULT CreateTranscodeProfile(IMFTranscodeProfile **ppProfile)
{
    IMFTranscodeProfile *pProfile = NULL;
    IMFAttributes *pAudio = NULL;
    IMFAttributes *pVideo = NULL;
    IMFAttributes *pContainer = NULL;

    HRESULT hr = MFCreateTranscodeProfile(&pProfile);
    if (FAILED(hr)) 
    {
        goto done;
    }

    // Audio attributes.
    hr = CreateAACProfile(audio_profile, &pAudio);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pProfile->SetAudioAttributes(pAudio);
    if (FAILED(hr)) 
    {
        goto done;
    }

    // Video attributes.
    hr = CreateH264Profile(video_profile, &pVideo);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pProfile->SetVideoAttributes(pVideo);
    if (FAILED(hr)) 
    {
        goto done;
    }

    // Container attributes.
    hr = MFCreateAttributes(&pContainer, 1);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pContainer->SetGUID(MF_TRANSCODE_CONTAINERTYPE, MFTranscodeContainerType_MPEG4);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pProfile->SetContainerAttributes(pContainer);
    if (FAILED(hr)) 
    {
        goto done;
    }

    *ppProfile = pProfile;
    (*ppProfile)->AddRef();

done:
    SafeRelease(&pProfile);
    SafeRelease(&pAudio);
    SafeRelease(&pVideo);
    SafeRelease(&pContainer);
    return hr;
}
```



<span data-ttu-id="33226-184">Pour spécifier les attributs du flux vidéo H. 264, créez un magasin d’attributs et définissez les attributs suivants :</span><span class="sxs-lookup"><span data-stu-id="33226-184">To specify the attributes for the H.264 video stream, create an attribute store and set the following attributes:</span></span>



| <span data-ttu-id="33226-185">Attribut</span><span class="sxs-lookup"><span data-stu-id="33226-185">Attribute</span></span>                                                       | <span data-ttu-id="33226-186">Description</span><span class="sxs-lookup"><span data-stu-id="33226-186">Desription</span></span>                      |
|-----------------------------------------------------------------|---------------------------------|
| [<span data-ttu-id="33226-187">**\_sous- \_ type MF MT**</span><span class="sxs-lookup"><span data-stu-id="33226-187">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)              | <span data-ttu-id="33226-188">Définissez sur **MFVideoFormat \_ H264 –**.</span><span class="sxs-lookup"><span data-stu-id="33226-188">Set to **MFVideoFormat\_H264**.</span></span> |
| [<span data-ttu-id="33226-189">**\_Profil de \_ MPEG2 \_ MT pour MF**</span><span class="sxs-lookup"><span data-stu-id="33226-189">**MF\_MT\_MPEG2\_PROFILE**</span></span>](mf-mt-mpeg2-profile-attribute.md) | <span data-ttu-id="33226-190">Profil H. 264.</span><span class="sxs-lookup"><span data-stu-id="33226-190">H.264 profile.</span></span>                  |
| [<span data-ttu-id="33226-191">**\_taille de \_ trame MF MF \_**</span><span class="sxs-lookup"><span data-stu-id="33226-191">**MF\_MT\_FRAME\_SIZE**</span></span>](mf-mt-frame-size-attribute.md)       | <span data-ttu-id="33226-192">Taille du frame.</span><span class="sxs-lookup"><span data-stu-id="33226-192">Frame size.</span></span>                     |
| [<span data-ttu-id="33226-193">**\_fréquence d' \_ images MF MF \_**</span><span class="sxs-lookup"><span data-stu-id="33226-193">**MF\_MT\_FRAME\_RATE**</span></span>](mf-mt-frame-rate-attribute.md)       | <span data-ttu-id="33226-194">Fréquence d’images.</span><span class="sxs-lookup"><span data-stu-id="33226-194">Frame rate.</span></span>                     |
| [<span data-ttu-id="33226-195">**\_vitesse de \_ \_ transmission moy. MF**</span><span class="sxs-lookup"><span data-stu-id="33226-195">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)     | <span data-ttu-id="33226-196">Vitesse de transmission encodée.</span><span class="sxs-lookup"><span data-stu-id="33226-196">Encoded bit rate.</span></span>               |



 

<span data-ttu-id="33226-197">Pour spécifier les attributs du flux audio AAC, créez un magasin d’attributs et définissez les attributs suivants :</span><span class="sxs-lookup"><span data-stu-id="33226-197">To specify the attributes for the AAC audio stream, create an attribute store and set the following attributes:</span></span>



| <span data-ttu-id="33226-198">Attribut</span><span class="sxs-lookup"><span data-stu-id="33226-198">Attribute</span></span>                                                                                      | <span data-ttu-id="33226-199">Description</span><span class="sxs-lookup"><span data-stu-id="33226-199">Desription</span></span>                               |
|------------------------------------------------------------------------------------------------|------------------------------------------|
| [<span data-ttu-id="33226-200">**\_sous- \_ type MF MT**</span><span class="sxs-lookup"><span data-stu-id="33226-200">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                             | <span data-ttu-id="33226-201">Définir sur **MFAudioFormat \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="33226-201">Set to **MFAudioFormat\_AAC**</span></span>            |
| [<span data-ttu-id="33226-202">**\_ \_ échantillons audio MF \_ MT \_ par \_ seconde**</span><span class="sxs-lookup"><span data-stu-id="33226-202">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)        | <span data-ttu-id="33226-203">Taux d’échantillonnage audio.</span><span class="sxs-lookup"><span data-stu-id="33226-203">Audio sample rate.</span></span>                       |
| [<span data-ttu-id="33226-204">**\_bits de \_ sortie audio MF \_ \_ par \_ échantillon**</span><span class="sxs-lookup"><span data-stu-id="33226-204">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)              | <span data-ttu-id="33226-205">Bits par échantillon audio.</span><span class="sxs-lookup"><span data-stu-id="33226-205">Bits per audio sample.</span></span>                   |
| [<span data-ttu-id="33226-206">**\_canaux de \_ \_ numéros audio MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="33226-206">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                     | <span data-ttu-id="33226-207">Nombre de canaux audio.</span><span class="sxs-lookup"><span data-stu-id="33226-207">Number of audio channels.</span></span>                |
| [<span data-ttu-id="33226-208">**\_octets de \_ données audio MF MT- \_ \_ octets \_ par \_ seconde**</span><span class="sxs-lookup"><span data-stu-id="33226-208">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md)   | <span data-ttu-id="33226-209">Vitesse de transmission encodée.</span><span class="sxs-lookup"><span data-stu-id="33226-209">Encoded bit rate.</span></span>                        |
| [<span data-ttu-id="33226-210">**\_alignement de \_ \_ bloc audio MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="33226-210">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)               | <span data-ttu-id="33226-211">défini sur 1.</span><span class="sxs-lookup"><span data-stu-id="33226-211">Set to 1.</span></span>                                |
| [<span data-ttu-id="33226-212">\_indication du \_ \_ niveau de \_ profil \_ audio MF MT AAC \_</span><span class="sxs-lookup"><span data-stu-id="33226-212">MF\_MT\_AAC\_AUDIO\_PROFILE\_LEVEL\_INDICATION</span></span>](mf-mt-aac-audio-profile-level-indication.md) | <span data-ttu-id="33226-213">Indication du niveau de profil AAC (facultatif).</span><span class="sxs-lookup"><span data-stu-id="33226-213">AAC profile level indication (optional).</span></span> |



 

<span data-ttu-id="33226-214">Le code suivant crée les attributs du flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="33226-214">The following code creates the video stream attributes.</span></span>


```C++
HRESULT CreateH264Profile(DWORD index, IMFAttributes **ppAttributes)
{
    if (index >= ARRAYSIZE(h264_profiles))
    {
        return E_INVALIDARG;
    }

    IMFAttributes *pAttributes = NULL;

    const H264ProfileInfo& profile = h264_profiles[index];

    HRESULT hr = MFCreateAttributes(&pAttributes, 5);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(MF_MT_SUBTYPE, MFVideoFormat_H264);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_MT_MPEG2_PROFILE, profile.profile);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(
            pAttributes, MF_MT_FRAME_SIZE, 
            profile.frame_size.Numerator, profile.frame_size.Numerator);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(
            pAttributes, MF_MT_FRAME_RATE, 
            profile.fps.Numerator, profile.fps.Denominator);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_MT_AVG_BITRATE, profile.bitrate);
    }
    if (SUCCEEDED(hr))
    {
        *ppAttributes = pAttributes;
        (*ppAttributes)->AddRef();
    }
    SafeRelease(&pAttributes);
    return hr;
}
```



<span data-ttu-id="33226-215">Le code suivant crée les attributs de flux audio.</span><span class="sxs-lookup"><span data-stu-id="33226-215">The following code creates the audio stream attributes.</span></span>


```C++
HRESULT CreateAACProfile(DWORD index, IMFAttributes **ppAttributes)
{
    if (index >= ARRAYSIZE(h264_profiles))
    {
        return E_INVALIDARG;
    }

    const AACProfileInfo& profile = aac_profiles[index];

    IMFAttributes *pAttributes = NULL;

    HRESULT hr = MFCreateAttributes(&pAttributes, 7);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(MF_MT_SUBTYPE, MFAudioFormat_AAC);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_BITS_PER_SAMPLE, profile.bitsPerSample);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_SAMPLES_PER_SECOND, profile.samplesPerSec);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_NUM_CHANNELS, profile.numChannels);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_AVG_BYTES_PER_SECOND, profile.bytesPerSec);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_MT_AUDIO_BLOCK_ALIGNMENT, 1);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION, profile.aacProfile);
    }
    if (SUCCEEDED(hr))
    {
        *ppAttributes = pAttributes;
        (*ppAttributes)->AddRef();
    }
    SafeRelease(&pAttributes);
    return hr;
}
```



<span data-ttu-id="33226-216">Notez que l’API de transcodage ne requiert pas de véritable type de média, bien qu’elle utilise des attributs de type de média.</span><span class="sxs-lookup"><span data-stu-id="33226-216">Note that the transcode API does not require a true media type, although it uses media-type attributes.</span></span> <span data-ttu-id="33226-217">En particulier, l’attribut de [**\_ \_ \_ type principal MF MT**](mf-mt-major-type-attribute.md) n’est pas obligatoire, car les méthodes [**SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes) et [**SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) impliquent le type majeur.</span><span class="sxs-lookup"><span data-stu-id="33226-217">In particular, the [**MF\_MT\_MAJOR\_TYPE**](mf-mt-major-type-attribute.md) attribute it not required, because the [**SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes) and [**SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) methods imply the major type.</span></span> <span data-ttu-id="33226-218">Toutefois, il est également valide de passer un type de média réel à ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="33226-218">However, it also valid to pass an actual media type to these methods.</span></span> <span data-ttu-id="33226-219">(L’interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) hérite de [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).)</span><span class="sxs-lookup"><span data-stu-id="33226-219">(The [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface inherits [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).)</span></span>

### <a name="run-the-encoding-session"></a><span data-ttu-id="33226-220">Exécuter la session d’encodage</span><span class="sxs-lookup"><span data-stu-id="33226-220">Run the Encoding Session</span></span>

<span data-ttu-id="33226-221">Le code suivant exécute la session d’encodage.</span><span class="sxs-lookup"><span data-stu-id="33226-221">The following code runs the encoding session.</span></span> <span data-ttu-id="33226-222">Elle utilise la classe d’assistance de session multimédia, qui est présentée dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="33226-222">It uses the Media Session helper class, which is shown in the next section.</span></span>


```C++
HRESULT RunEncodingSession(CSession *pSession, MFTIME duration)
{
    const DWORD WAIT_PERIOD = 500;
    const int   UPDATE_INCR = 5;

    HRESULT hr = S_OK;
    MFTIME pos;
    LONGLONG prev = 0;
    while (1)
    {
        hr = pSession->Wait(WAIT_PERIOD);
        if (hr == E_PENDING)
        {
            hr = pSession->GetEncodingPosition(&pos);

            LONGLONG percent = (100 * pos) / duration ;
            if (percent >= prev + UPDATE_INCR)
            {
                std::cout << percent << "% .. ";  
                prev = percent;
            }
        }
        else
        {
            std::cout << std::endl;
            break;
        }
    }
    return hr;
}
```



## <a name="media-session-helper"></a><span data-ttu-id="33226-223">Assistance de session multimédia</span><span class="sxs-lookup"><span data-stu-id="33226-223">Media Session Helper</span></span>

<span data-ttu-id="33226-224">La [session multimédia](media-session.md) est décrite plus en détail dans la section [Media Foundation architecture](media-foundation-architecture.md) de cette documentation.</span><span class="sxs-lookup"><span data-stu-id="33226-224">The [Media Session](media-session.md) is described more fully in the [Media Foundation Architecture](media-foundation-architecture.md) section of this documentation.</span></span> <span data-ttu-id="33226-225">La session multimédia utilise un modèle d’événement asynchrone.</span><span class="sxs-lookup"><span data-stu-id="33226-225">The Media Session uses an asynchronous event model.</span></span> <span data-ttu-id="33226-226">Dans une application GUI, vous devez répondre aux événements de session sans bloquer le thread d’interface utilisateur pour attendre l’événement suivant.</span><span class="sxs-lookup"><span data-stu-id="33226-226">In a GUI application, you should respond to session events without blocking the UI thread to wait for the next event.</span></span> <span data-ttu-id="33226-227">Le didacticiel [Comment lire des fichiers multimédias non protégés](how-to-play-unprotected-media-files.md) montre comment effectuer cette opération dans une application de lecture.</span><span class="sxs-lookup"><span data-stu-id="33226-227">The tutorial [How to Play Unprotected Media Files](how-to-play-unprotected-media-files.md) shows how to do this in a playback application.</span></span> <span data-ttu-id="33226-228">Pour l’encodage, le principe est le même, mais moins d’événements sont pertinents :</span><span class="sxs-lookup"><span data-stu-id="33226-228">For encoding, the principle is the same, but fewer events are relevant:</span></span>



| <span data-ttu-id="33226-229">Événement</span><span class="sxs-lookup"><span data-stu-id="33226-229">Event</span></span>                                  | <span data-ttu-id="33226-230">Description</span><span class="sxs-lookup"><span data-stu-id="33226-230">Desription</span></span>                                                                                                                                                       |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="33226-231">MESessionEnded</span><span class="sxs-lookup"><span data-stu-id="33226-231">MESessionEnded</span></span>](mesessionended.md)   | <span data-ttu-id="33226-232">Déclenché lorsque l’encodage est terminé.</span><span class="sxs-lookup"><span data-stu-id="33226-232">Raised when the encoding is complete.</span></span>                                                                                                                            |
| [<span data-ttu-id="33226-233">MESessionClosed</span><span class="sxs-lookup"><span data-stu-id="33226-233">MESessionClosed</span></span>](mesessionclosed.md) | <span data-ttu-id="33226-234">Déclenché lorsque la méthode [**IMFMediaSession :: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) se termine.</span><span class="sxs-lookup"><span data-stu-id="33226-234">Raised when the [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) method completes.</span></span> <span data-ttu-id="33226-235">Une fois cet événement déclenché, il est possible d’arrêter la session multimédia en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="33226-235">After this event is raised, it is safe to shut down the Media Session.</span></span> |



 

<span data-ttu-id="33226-236">Pour une application console, il est raisonnable de bloquer et d’attendre les événements.</span><span class="sxs-lookup"><span data-stu-id="33226-236">For a console application, it is reasonable to block and wait for events.</span></span> <span data-ttu-id="33226-237">En fonction du fichier source et des paramètres d’encodage, l’encodage peut prendre un certain temps.</span><span class="sxs-lookup"><span data-stu-id="33226-237">Depending on the source file and the encoding settings, it might take awhile to complete the encoding.</span></span> <span data-ttu-id="33226-238">Vous pouvez accéder aux mises à jour de progression comme suit :</span><span class="sxs-lookup"><span data-stu-id="33226-238">You can get progress updates as follows:</span></span>

1.  <span data-ttu-id="33226-239">Appelez [**IMFMediaSession :: GetClock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) pour afficher l’horloge de la présentation.</span><span class="sxs-lookup"><span data-stu-id="33226-239">Call [**IMFMediaSession::GetClock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) to get the presentation clock.</span></span>
2.  <span data-ttu-id="33226-240">Interrogez l’horloge de l’interface [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) .</span><span class="sxs-lookup"><span data-stu-id="33226-240">Query the clock for the [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) interface.</span></span>
3.  <span data-ttu-id="33226-241">Appelez [**IMFPresentationClock :: getTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) pour accéder à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="33226-241">Call [**IMFPresentationClock::GetTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) to get the current position.</span></span>
4.  <span data-ttu-id="33226-242">La position est donnée en unités de temps.</span><span class="sxs-lookup"><span data-stu-id="33226-242">The position is given in units of time.</span></span> <span data-ttu-id="33226-243">Pour faire en sorte que le pourcentage soit terminé, utilisez la valeur `(100 * position) / duration` .</span><span class="sxs-lookup"><span data-stu-id="33226-243">To get the percentage completed, use the value `(100 * position) / duration`.</span></span>

<span data-ttu-id="33226-244">Voici la déclaration de la `CSession` classe.</span><span class="sxs-lookup"><span data-stu-id="33226-244">Here is the declaration of the `CSession` class.</span></span>


```C++
class CSession  : public IMFAsyncCallback 
{
public:
    static HRESULT Create(CSession **ppSession);

    // IUnknown methods
    STDMETHODIMP QueryInterface(REFIID riid, void** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    // IMFAsyncCallback methods
    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }
    STDMETHODIMP Invoke(IMFAsyncResult *pResult);

    // Other methods
    HRESULT StartEncodingSession(IMFTopology *pTopology);
    HRESULT GetEncodingPosition(MFTIME *pTime);
    HRESULT Wait(DWORD dwMsec);

private:
    CSession() : m_cRef(1), m_pSession(NULL), m_pClock(NULL), m_hrStatus(S_OK), m_hWaitEvent(NULL)
    {
    }
    virtual ~CSession()
    {
        if (m_pSession)
        {
            m_pSession->Shutdown();
        }

        SafeRelease(&m_pClock);
        SafeRelease(&m_pSession);
        CloseHandle(m_hWaitEvent);
    }

    HRESULT Initialize();

private:
    IMFMediaSession      *m_pSession;
    IMFPresentationClock *m_pClock;
    HRESULT m_hrStatus;
    HANDLE  m_hWaitEvent;
    long    m_cRef;
};
```



<span data-ttu-id="33226-245">Le code suivant illustre l’implémentation complète de la `CSession` classe.</span><span class="sxs-lookup"><span data-stu-id="33226-245">The following code shows the complete implementation of the `CSession` class.</span></span>


```C++
HRESULT CSession::Create(CSession **ppSession)
{
    *ppSession = NULL;

    CSession *pSession = new (std::nothrow) CSession();
    if (pSession == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pSession->Initialize();
    if (FAILED(hr))
    {
        pSession->Release();
        return hr;
    }
    *ppSession = pSession;
    return S_OK;
}

STDMETHODIMP CSession::QueryInterface(REFIID riid, void** ppv)
{
    static const QITAB qit[] = 
    {
        QITABENT(CSession, IMFAsyncCallback),
        { 0 }
    };
    return QISearch(this, qit, riid, ppv);
}

STDMETHODIMP_(ULONG) CSession::AddRef()
{
    return InterlockedIncrement(&m_cRef);
}

STDMETHODIMP_(ULONG) CSession::Release()
{
    long cRef = InterlockedDecrement(&m_cRef);
    if (cRef == 0)
    {
        delete this;
    }
    return cRef;
}

HRESULT CSession::Initialize()
{
    IMFClock *pClock = NULL;

    HRESULT hr = MFCreateMediaSession(NULL, &m_pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = m_pSession->GetClock(&pClock);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pClock->QueryInterface(IID_PPV_ARGS(&m_pClock));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = m_pSession->BeginGetEvent(this, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    m_hWaitEvent = CreateEvent(NULL, FALSE, FALSE, NULL);  
    if (m_hWaitEvent == NULL)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }
done:
    SafeRelease(&pClock);
    return hr;
}

// Implements IMFAsyncCallback::Invoke
STDMETHODIMP CSession::Invoke(IMFAsyncResult *pResult)
{
    IMFMediaEvent* pEvent = NULL;
    MediaEventType meType = MEUnknown;
    HRESULT hrStatus = S_OK;

    HRESULT hr = m_pSession->EndGetEvent(pResult, &pEvent);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEvent->GetType(&meType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEvent->GetStatus(&hrStatus);
    if (FAILED(hr))
    {
        goto done;
    }

    if (FAILED(hrStatus))
    {
        hr = hrStatus;
        goto done;
    }

    switch (meType)
    {
    case MESessionEnded:
        hr = m_pSession->Close();
        if (FAILED(hr))
        {
            goto done;
        }
        break;

    case MESessionClosed:
        SetEvent(m_hWaitEvent);
        break;
    }

    if (meType != MESessionClosed)
    {
        hr = m_pSession->BeginGetEvent(this, NULL);
    }

done:
    if (FAILED(hr))
    {
        m_hrStatus = hr;
        m_pSession->Close();
    }

    SafeRelease(&pEvent);
    return hr;
}

HRESULT CSession::StartEncodingSession(IMFTopology *pTopology)
{
    HRESULT hr = m_pSession->SetTopology(0, pTopology);
    if (SUCCEEDED(hr))
    {
        PROPVARIANT varStart;
        PropVariantClear(&varStart);
        hr = m_pSession->Start(&GUID_NULL, &varStart);
    }
    return hr;
}

HRESULT CSession::GetEncodingPosition(MFTIME *pTime)
{
    return m_pClock->GetTime(pTime);
}

HRESULT CSession::Wait(DWORD dwMsec)
{
    HRESULT hr = S_OK;

    DWORD dwTimeoutStatus = WaitForSingleObject(m_hWaitEvent, dwMsec);
    if (dwTimeoutStatus != WAIT_OBJECT_0)
    {
        hr = E_PENDING;
    }
    else
    {
        hr = m_hrStatus;
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="33226-246">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="33226-246">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33226-247">**Encodeur AAC**</span><span class="sxs-lookup"><span data-stu-id="33226-247">**AAC Encoder**</span></span>](aac-encoder.md)
</dt> <dt>

[<span data-ttu-id="33226-248">**Encodeur vidéo H. 264**</span><span class="sxs-lookup"><span data-stu-id="33226-248">**H.264 Video Encoder**</span></span>](h-264-video-encoder.md)
</dt> <dt>

[<span data-ttu-id="33226-249">Session multimédia</span><span class="sxs-lookup"><span data-stu-id="33226-249">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="33226-250">Types de médias</span><span class="sxs-lookup"><span data-stu-id="33226-250">Media Types</span></span>](media-types.md)
</dt> <dt>

[<span data-ttu-id="33226-251">API de transcodage</span><span class="sxs-lookup"><span data-stu-id="33226-251">Transcode API</span></span>](transcode-api.md)
</dt> </dl>

 

 
