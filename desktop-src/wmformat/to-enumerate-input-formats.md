---
title: Pour énumérer les formats d’entrée
description: Pour énumérer les formats d’entrée
ms.assetid: 482adfc4-d9ed-403d-912b-1a5a70baf04c
keywords:
- ASF (Advanced Systems Format), énumération des formats d’entrée
- ASF (format avancé des systèmes), énumération des formats d’entrée
- profils, énumération des formats d’entrée
- codecs, énumération des formats d’entrée
- ASF (Advanced Systems Format), énumérations de format d’entrée
- ASF (format des systèmes avancés), énumérations de format d’entrée
- profils, énumérations de format d’entrée
- codecs, énumérations de format d’entrée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18360d3172af785fd1c00648ba0c9e869fb7fbc6
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104030935"
---
# <a name="to-enumerate-input-formats"></a><span data-ttu-id="b5516-111">Pour énumérer les formats d’entrée</span><span class="sxs-lookup"><span data-stu-id="b5516-111">To Enumerate Input Formats</span></span>

<span data-ttu-id="b5516-112">Chacun des codecs Windows Media accepte un ou plusieurs types de média d’entrée pour la compression.</span><span class="sxs-lookup"><span data-stu-id="b5516-112">Each of the Windows Media codecs accepts one or more types of input media for compression.</span></span> <span data-ttu-id="b5516-113">Le kit de développement logiciel (SDK) Windows Media format vous permet d’entrer une plus grande variété de formats que ceux pris en charge par les codecs.</span><span class="sxs-lookup"><span data-stu-id="b5516-113">The Windows Media Format SDK enables you to input a wider variety of formats than those supported by the codecs.</span></span> <span data-ttu-id="b5516-114">Le kit de développement logiciel (SDK) effectue cette opération en effectuant des transformations de prétraitement sur les entrées, le cas échéant, comme le redimensionnement des images vidéo ou le rééchantillonnage de l’audio.</span><span class="sxs-lookup"><span data-stu-id="b5516-114">The SDK does this by performing pre-processing transformations on the inputs when necessary, such as resizing video frames or resampling audio.</span></span> <span data-ttu-id="b5516-115">Dans tous les cas, vous devez vous assurer que les formats d’entrée pour les fichiers que vous écrivez correspondent aux données que vous envoyez au writer.</span><span class="sxs-lookup"><span data-stu-id="b5516-115">In any case, you must ensure that the input formats for the files you write match the data you send to the writer.</span></span> <span data-ttu-id="b5516-116">Chaque codec a un format de média d’entrée par défaut qui est défini dans le writer lors du chargement du profil.</span><span class="sxs-lookup"><span data-stu-id="b5516-116">Each codec has a default input media format that is set in the writer when the profile is loaded.</span></span> <span data-ttu-id="b5516-117">Vous pouvez examiner le format d’entrée par défaut en appelant [**IWMWriter :: GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).</span><span class="sxs-lookup"><span data-stu-id="b5516-117">You can examine the default input format by calling [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).</span></span>

<span data-ttu-id="b5516-118">Les codecs vidéo prennent en charge les formats suivants : IYUV, I420, YV12, YUY2, UYVY, YVYU, YVU9, RGB 32, RGB 24, RGB 565, RVB 555 et RVB 8.</span><span class="sxs-lookup"><span data-stu-id="b5516-118">The video codecs support the following formats: IYUV, I420, YV12, YUY2, UYVY, YVYU, YVU9, RGB 32, RGB 24, RGB 565, RGB 555, and RGB 8.</span></span> <span data-ttu-id="b5516-119">Les codecs audio prennent en charge le PCM audio.</span><span class="sxs-lookup"><span data-stu-id="b5516-119">The audio codecs support PCM audio.</span></span>

<span data-ttu-id="b5516-120">Pour énumérer les formats d’entrée pris en charge par un codec, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="b5516-120">To enumerate the input formats supported by a codec, perform the following steps:</span></span>

1.  <span data-ttu-id="b5516-121">Créez un objet Writer et définissez un profil à utiliser.</span><span class="sxs-lookup"><span data-stu-id="b5516-121">Create a writer object and set a profile to use.</span></span> <span data-ttu-id="b5516-122">Pour plus d’informations sur la définition des profils dans le writer, consultez [pour utiliser des profils avec le writer](to-use-profiles-with-the-writer.md).</span><span class="sxs-lookup"><span data-stu-id="b5516-122">For more information about setting profiles in the writer, see [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md).</span></span>
2.  <span data-ttu-id="b5516-123">Identifiez le nombre d’entrées pour lequel vous souhaitez vérifier les formats.</span><span class="sxs-lookup"><span data-stu-id="b5516-123">Identify the input number for which you want to check the formats.</span></span> <span data-ttu-id="b5516-124">Pour plus d’informations sur l’identification des numéros d’entrée, consultez [pour identifier les entrées par numéro](to-identify-inputs-by-number.md).</span><span class="sxs-lookup"><span data-stu-id="b5516-124">For more information about identifying input numbers, see [To Identify Inputs By Number](to-identify-inputs-by-number.md).</span></span>
3.  <span data-ttu-id="b5516-125">Récupérez le nombre total de formats d’entrée pris en charge par l’entrée souhaitée en appelant [**IWMWriter :: GetInputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount).</span><span class="sxs-lookup"><span data-stu-id="b5516-125">Retrieve the total number of input formats supported by the desired input by calling [**IWMWriter::GetInputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount).</span></span>
4.  <span data-ttu-id="b5516-126">Parcourez tous les formats d’entrée pris en charge, en effectuant les étapes suivantes pour chacun d’entre eux.</span><span class="sxs-lookup"><span data-stu-id="b5516-126">Loop through all of the supported input formats, performing the following steps for each.</span></span>
    -   <span data-ttu-id="b5516-127">Récupérez l’interface [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) pour le format d’entrée en appelant [**IWMWriter :: GetInputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat).</span><span class="sxs-lookup"><span data-stu-id="b5516-127">Retrieve the [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) interface for the input format by calling [**IWMWriter::GetInputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat).</span></span>
    -   <span data-ttu-id="b5516-128">Récupérez la structure du [**\_ \_ type de média WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) pour le format d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b5516-128">Retrieve the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure for the input format.</span></span> <span data-ttu-id="b5516-129">Appelez [**IWMMediaProps :: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype), en passant la **valeur null** pour le paramètre *PTYPE* afin d’obtenir la taille de la structure.</span><span class="sxs-lookup"><span data-stu-id="b5516-129">Call [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype), passing **NULL** for the *pType* parameter to get the size of the structure.</span></span> <span data-ttu-id="b5516-130">Allouez ensuite de la mémoire pour contenir la structure et rappelez **GetMediaType** pour récupérer la structure.</span><span class="sxs-lookup"><span data-stu-id="b5516-130">Then allocate memory to hold the structure and call **GetMediaType** again to get the structure.</span></span> <span data-ttu-id="b5516-131">[**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) hérite de [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops). vous pouvez donc effectuer les appels à **GetMediaType** à partir de l’instance de **IWMInputMediaProps** Récupérée à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="b5516-131">[**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) inherits from [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops), so you can make the calls to **GetMediaType** from the instance of **IWMInputMediaProps** retrieved in the previous step.</span></span>
    -   <span data-ttu-id="b5516-132">Le format décrit dans la structure de [**\_ \_ type de média WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) contient toutes les informations pertinentes sur le format d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b5516-132">The format described in the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure contains all of the pertinent information about the input format.</span></span> <span data-ttu-id="b5516-133">Le format de base du support est identifié par **WM \_ Media \_ type. SubType**.</span><span class="sxs-lookup"><span data-stu-id="b5516-133">The basic format of the media is identified by **WM\_MEDIA\_TYPE.subtype**.</span></span> <span data-ttu-id="b5516-134">Pour les flux vidéo, le membre **pbFormat** pointe vers une structure [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) allouée dynamiquement qui contient des détails supplémentaires sur le flux, y compris la taille du rectangle.</span><span class="sxs-lookup"><span data-stu-id="b5516-134">For video streams, the **pbFormat** member points to a dynamically allocated [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) structure which contains further details about the stream, including rectangle size.</span></span> <span data-ttu-id="b5516-135">La taille des frames d’entrée n’est pas obligatoire pour correspondre exactement à une taille prise en charge par le codec.</span><span class="sxs-lookup"><span data-stu-id="b5516-135">The size of the input frames is not required to match exactly a size supported by the codec.</span></span> <span data-ttu-id="b5516-136">Si elles ne correspondent pas, les composants d’exécution du kit de développement logiciel (SDK), dans de nombreux cas, redimensionnent automatiquement les trames vidéo d’entrée pour qu’elles puissent être acceptées par le codec.</span><span class="sxs-lookup"><span data-stu-id="b5516-136">If they do not match, the SDK run-time components, in many cases, will automatically resize the input video frames to something the codec can accept.</span></span>

<span data-ttu-id="b5516-137">L’exemple de code suivant recherche le format d’entrée du sous-type passé comme paramètre.</span><span class="sxs-lookup"><span data-stu-id="b5516-137">The following example code finds the input format of the subtype passed as a parameter.</span></span> <span data-ttu-id="b5516-138">Pour plus d’informations sur l’utilisation de ce code, consultez [utilisation des exemples de code](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="b5516-138">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT FindInputFormat(IWMWriter* pWriter, 
                       DWORD dwInput,
                       GUID guidSubType,
                       IWMInputMediaProps** ppProps)
{
    DWORD   cFormats = 0;
    DWORD   cbSize   = 0;

    WM_MEDIA_TYPE*      pType  = NULL;
    IWMInputMediaProps* pProps = NULL;

    // Set the ppProps parameter to point to NULL. This will
    //  be used to check the results of the function later.
    *ppProps = NULL;

    // Find the number of formats supported by this input.
    HRESULT hr = pWriter->GetInputFormatCount(dwInput, &cFormats);
    if (FAILED(hr))
    {
        goto Exit;
    }
    // Loop through all of the supported formats.
    for (DWORD formatIndex = 0; formatIndex < cFormats; formatIndex++)
    {
        // Get the input media properties for the input format.
        hr = pWriter->GetInputFormat(dwInput, formatIndex, &pProps);
        if (FAILED(hr))
        {
            goto Exit;
        }
        // Get the size of the media type structure.
        hr = pProps->GetMediaType(NULL, &cbSize);
        if (FAILED(hr))
        {
            goto Exit;
        }
        // Allocate memory for the media type structure.
        pType = (WM_MEDIA_TYPE*) new (std::nothrow) BYTE[cbSize];
        if (pType == NULL)
        {
            hr = E_OUTOFMEMORY;
            goto Exit;
        }
        
        // Get the media type structure.
        hr = pProps->GetMediaType(pType, &cbSize);
        if (FAILED(hr))
        {
            goto Exit;
        }

        if(pType->subtype == guidSubType)
        {
            *ppProps = pProps;
            (*ppProps)->AddRef();
            goto Exit;
        }

        // Clean up for next iteration.
        delete [] pType;
        pType = NULL;
        SAFE_RELEASE(pProps);
    } // End for formatIndex.

    // If execution made it to this point, no matching format was found.
    hr = NS_E_INVALID_INPUT_FORMAT;

Exit:
    delete [] pType;
    SAFE_RELEASE(pProps);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="b5516-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b5516-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5516-140">**Interface IWMWriter**</span><span class="sxs-lookup"><span data-stu-id="b5516-140">**IWMWriter Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[<span data-ttu-id="b5516-141">**Écriture de fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="b5516-141">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




