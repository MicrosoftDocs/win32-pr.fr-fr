---
description: Configuration de profils et autres propriétés de fichier ASF
ms.assetid: c43df556-9d8a-4010-9ed6-f84d8ac6d9bc
title: Configuration de profils et autres propriétés de fichier ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e26dcbb49cb5ff8309dccafc3f1d8d66397871
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392728"
---
# <a name="configuring-profiles-and-other-asf-file-properties"></a><span data-ttu-id="863dc-103">Configuration de profils et autres propriétés de fichier ASF</span><span class="sxs-lookup"><span data-stu-id="863dc-103">Configuring Profiles and Other ASF File Properties</span></span>

<span data-ttu-id="863dc-104">Les éléments suivants décrivent comment effectuer diverses tâches liées à la création de fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="863dc-104">The following items describe how to perform various tasks related to the creation of ASF files.</span></span> <span data-ttu-id="863dc-105">Certaines des interfaces mentionnées dans cette rubrique sont documentées dans la documentation du kit de développement logiciel (SDK) Windows Media format.</span><span class="sxs-lookup"><span data-stu-id="863dc-105">Some of the interfaces mentioned in this topic are documented in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="863dc-106">Création d’un profil</span><span class="sxs-lookup"><span data-stu-id="863dc-106">Creating a Profile</span></span>

<span data-ttu-id="863dc-107">Les profils ASF sont présentés en détail dans le kit de développement logiciel (SDK) de format Windows Media. Fondamentalement, ils décrivent les attributs d’un fichier au format Windows Media, tels que la vitesse de transmission, le nombre et le type de flux, ainsi que la qualité de compression.</span><span class="sxs-lookup"><span data-stu-id="863dc-107">ASF profiles are discussed in detail in the Windows Media Format SDK; essentially, they describe attributes of a Windows Media Format file such as bit rate, number and type of streams, and compression quality.</span></span> <span data-ttu-id="863dc-108">Le filtre utilise le profil pour déterminer le type de fichier de format Windows Media à écrire, le nombre de broches d’entrée qu’il doit configurer et les types de médias qu’il peut accepter.</span><span class="sxs-lookup"><span data-stu-id="863dc-108">The filter uses the profile to determine what kind of Windows Media Format file to write, how many input pins it must set up, and what media types they can accept.</span></span>

<span data-ttu-id="863dc-109">Pour créer un profil personnalisé, utilisez le kit de développement logiciel (SDK) de format Windows Media directement pour créer un objet de gestionnaire de profils à l’aide de la fonction **WMCreateProfileManager** .</span><span class="sxs-lookup"><span data-stu-id="863dc-109">To create a custom profile, use the Windows Media Format SDK directly to create a profile manager object by using the **WMCreateProfileManager** function.</span></span> <span data-ttu-id="863dc-110">Ensuite, créez le profil et transmettez-le à l' [enregistreur WM ASF](wm-asf-writer-filter.md) à l’aide de la méthode [**IConfigASFWriter :: ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) .</span><span class="sxs-lookup"><span data-stu-id="863dc-110">Next, create the profile, and pass it to the [WM ASF Writer](wm-asf-writer-filter.md) by using the [**IConfigASFWriter::ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) method.</span></span> <span data-ttu-id="863dc-111">Il s’agit de la seule façon de configurer le filtre avec un profil qui utilise les codecs de série Windows Media Audio et Video 9.</span><span class="sxs-lookup"><span data-stu-id="863dc-111">This is the only way to configure the filter with a profile that uses the Windows Media Audio and Video 9 Series codecs.</span></span> <span data-ttu-id="863dc-112">Les profils système des versions antérieures de ces codecs peuvent être ajoutés à l’aide de la méthode [**IConfigASFWriter :: ConfigureFilterUsingProfileGuid**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofileguid) .</span><span class="sxs-lookup"><span data-stu-id="863dc-112">System profiles for earlier versions of these codecs can be added by using the [**IConfigASFWriter::ConfigureFilterUsingProfileGuid**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofileguid) method.</span></span>

<span data-ttu-id="863dc-113">Vous pouvez réinitialiser le profil alors que les broches d’entrée du filtre sont connectées, à condition que le nouveau profil ne nécessite pas de broches d’entrée supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="863dc-113">You can reset the profile while the filter's input pins are connected, as long as the new profile does not require any additional input pins.</span></span> <span data-ttu-id="863dc-114">Par exemple, si vous modifiez le profil d’un profil audio à entrée unique en un profil audio et vidéo à deux entrées, seul le code confidentiel audio sera reconnecté et aucun nouveau code confidentiel ne sera créé pour le flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="863dc-114">For example, if you change the profile from a one-input audio-only profile to a two-input audio and video profile, just the audio pin will be reconnected and no new pin will be created for the video stream.</span></span>

<span data-ttu-id="863dc-115">Ajout de métadonnées</span><span class="sxs-lookup"><span data-stu-id="863dc-115">Adding Metadata</span></span>

<span data-ttu-id="863dc-116">Pour ajouter des métadonnées à un fichier, interrogez le filtre du [writer WM ASF](wm-asf-writer-filter.md) pour l’interface **IWMHeaderInfo** .</span><span class="sxs-lookup"><span data-stu-id="863dc-116">To add metadata to a file, query the [WM ASF Writer](wm-asf-writer-filter.md) filter for the **IWMHeaderInfo** interface.</span></span> <span data-ttu-id="863dc-117">Une fois que le filtre a reçu un profil, utilisez les méthodes de l’interface **IWMHeaderInfo** pour écrire les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="863dc-117">After the filter has been given a profile, use the **IWMHeaderInfo** interface methods to write the metadata.</span></span>

<span data-ttu-id="863dc-118">Indexation d’un fichier</span><span class="sxs-lookup"><span data-stu-id="863dc-118">Indexing a File</span></span>

<span data-ttu-id="863dc-119">L’enregistreur ASF WM crée par défaut des fichiers indexés de façon temporelle.</span><span class="sxs-lookup"><span data-stu-id="863dc-119">The WM ASF Writer creates temporally indexed files by default.</span></span> <span data-ttu-id="863dc-120">Pour créer un fichier d’index de frames, utilisez la méthode [**IConfigAsfWriter :: SetIndexMode**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-setindexmode) pour désactiver l’indexation, puis créez le fichier.</span><span class="sxs-lookup"><span data-stu-id="863dc-120">To create a frame-indexed file, use the [**IConfigAsfWriter::SetIndexMode**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-setindexmode) method to disable all indexing, then create the file.</span></span> <span data-ttu-id="863dc-121">Une fois l’opération terminée, utilisez le kit de développement logiciel (SDK) de format Windows Media directement pour créer un index basé sur des frames pour le fichier.</span><span class="sxs-lookup"><span data-stu-id="863dc-121">When it is complete, use the Windows Media Format SDK directly to create a frame-based index for the file.</span></span>

<span data-ttu-id="863dc-122">Encodage Two-Pass</span><span class="sxs-lookup"><span data-stu-id="863dc-122">Two-Pass Encoding</span></span>

<span data-ttu-id="863dc-123">L’encodage en deux passes est pris en charge uniquement sur les codecs Windows Media version 8 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="863dc-123">Two-pass encoding is supported only on Windows Media codecs of version 8 and later.</span></span> <span data-ttu-id="863dc-124">Placez le writer WM ASF en mode prétraitement en appelant [**IConfigAsfWriter2 :: setParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) et en spécifiant am \_ CONFIGASFWRITER \_ param \_ Multipass dans le paramètre *DwParam* et **true** dans le paramètre *dwParam1* .</span><span class="sxs-lookup"><span data-stu-id="863dc-124">Put the WM ASF Writer into preprocess mode by calling [**IConfigAsfWriter2::SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) and specifying AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS in the *dwParam* parameter and **TRUE** in the *dwParam1* parameter.</span></span>

<span data-ttu-id="863dc-125">Exécutez ensuite le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="863dc-125">Then run the filter graph.</span></span> <span data-ttu-id="863dc-126">Lorsque toutes les étapes de prétraitement sont effectuées (en général, une seule passe de prétraitement est effectuée), l’application reçoit un événement de [**\_ \_ fin de prétraitement EC**](ec-preprocess-complete.md) du filtre.</span><span class="sxs-lookup"><span data-stu-id="863dc-126">When all the preprocessing passes are done (typically only one preprocessing pass will be performed), the application will receive an [**EC\_PREPROCESS\_COMPLETE**](ec-preprocess-complete.md) event from the filter.</span></span> <span data-ttu-id="863dc-127">Lorsque cet événement est reçu, utilisez [**IMediaSeeking :: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) pour réinitialiser le pointeur de flux jusqu’au début, puis exécutez à nouveau le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="863dc-127">When this event is received, use [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) to reset the stream pointer back to the beginning, and run the filter graph again.</span></span> <span data-ttu-id="863dc-128">Après la dernière passe (en général, la deuxième passe), l’application reçoit un événement [**EC \_ Complete**](ec-complete.md) pour signifier que le processus d’encodage est terminé.</span><span class="sxs-lookup"><span data-stu-id="863dc-128">After the last pass (typically the second pass), the application will receive an [**EC\_COMPLETE**](ec-complete.md) event to signify that the encoding process is complete.</span></span> <span data-ttu-id="863dc-129">Si une passe de prétraitement est annulée avant la réception de l’événement de **\_ prétraitement \_** de l’UE, appelez [**IConfigAsfWriter2 :: ResetMultiPassState**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-resetmultipassstate) pour réinitialiser le filtre avant de tenter une autre exécution de prétraitement.</span><span class="sxs-lookup"><span data-stu-id="863dc-129">If a preprocessing pass is canceled before the **EC\_PREPROCESS\_COMPLETE** event is received, call [**IConfigAsfWriter2::ResetMultiPassState**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-resetmultipassstate) to reset the filter before attempting another preprocessing run.</span></span>

<span data-ttu-id="863dc-130">Il est nécessaire uniquement de définir le \_ paramètre am CONFIGASFWRITER \_ param \_ Multipass sur **false** si vous souhaitez que le filtre soit complètement en mode de prétraitement.</span><span class="sxs-lookup"><span data-stu-id="863dc-130">It is only necessary to set the AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS parameter to **FALSE** if you want to put the filter out of preprocessing mode completely.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="863dc-131">Il incombe à l’application d’activer le mode de prétraitement en fonction du profil qui sera utilisé pour l’encodage.</span><span class="sxs-lookup"><span data-stu-id="863dc-131">It is the application's responsibility to enable the preprocessing mode based on the profile that will be used for encoding.</span></span> <span data-ttu-id="863dc-132">Certains profils nécessitent un encodage en deux passes ; Si vous tentez d’encoder un fichier à l’aide d’un profil de ce type et que vous ne définissez pas AM \_ CONFIGASFWRITER \_ param \_ Multipass sur **true**, une erreur [**EC \_ USERABORT**](ec-userabort.md) est générée.</span><span class="sxs-lookup"><span data-stu-id="863dc-132">Some profiles require two-pass encoding; if you attempt to encode a file with such a profile, and do not set AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS to **TRUE**, an [**EC\_USERABORT**](ec-userabort.md) error will result.</span></span> <span data-ttu-id="863dc-133">Pour plus d’informations, consultez la documentation du kit de développement logiciel (SDK) Windows Media format.</span><span class="sxs-lookup"><span data-stu-id="863dc-133">For more information, see the Windows Media Format SDK documentation.</span></span>

 

<span data-ttu-id="863dc-134">Obtention et définition des propriétés de la mémoire tampon au moment de l’exécution</span><span class="sxs-lookup"><span data-stu-id="863dc-134">Getting and Setting Buffer Properties at Run Time</span></span>

<span data-ttu-id="863dc-135">Dans certains scénarios, par exemple, si vous souhaitez forcer l’insertion d’une image clé lors de l’écriture d’un fichier, une application peut avoir besoin d’obtenir ou de définir des informations sur un tampon Windows Media au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="863dc-135">In some scenarios, for example if you want to force key-frame insertion when writing a file, an application may need to get or set information about a Windows Media buffer at run time.</span></span> <span data-ttu-id="863dc-136">Le [lecteur ASF WM](wm-asf-reader-filter.md) et les filtres d' [enregistreur ASF WM](wm-asf-writer-filter.md) prennent tous deux en charge un mécanisme de rappel qui permet à une application d’accéder à l’interface **INSSBuffer3** sur chaque mémoire tampon de média individuelle lors de la lecture ou de l’écriture de fichiers.</span><span class="sxs-lookup"><span data-stu-id="863dc-136">The [WM ASF Reader](wm-asf-reader-filter.md) and [WM ASF Writer](wm-asf-writer-filter.md) filters both support a callback mechanism that enables an application to access the **INSSBuffer3** interface on each individual media buffer during file reading or file writing.</span></span> <span data-ttu-id="863dc-137">Les applications peuvent utiliser cette interface pour désigner des exemples spécifiques en tant qu’images clés, définir des codes temporels SMPTE, spécifier des paramètres d’entrelacement ou ajouter n’importe quel type de données privées à un flux.</span><span class="sxs-lookup"><span data-stu-id="863dc-137">Applications can use this interface to designate specific samples as key frames, set SMPTE time codes, specify interlace settings, or add any type of private data to a stream.</span></span>

<span data-ttu-id="863dc-138">Utilisez l’interface [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass) pour vous inscrire aux rappels à partir du code confidentiel qui gère le flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="863dc-138">Use the [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass) interface to register for callbacks from the pin that is handling the video stream.</span></span> <span data-ttu-id="863dc-139">Le code PIN appellera votre méthode [**IAMWMBufferPassCallback :: Notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) pour chaque mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="863dc-139">The pin will call your [**IAMWMBufferPassCallback::Notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) method for each buffer.</span></span>

<span data-ttu-id="863dc-140">Pixels non carrés</span><span class="sxs-lookup"><span data-stu-id="863dc-140">Non-Square Pixels</span></span>

<span data-ttu-id="863dc-141">L’enregistreur ASF WM se connecte à un filtre en amont, tel que le décodeur DV, qui génère des informations sur les proportions en pixels.</span><span class="sxs-lookup"><span data-stu-id="863dc-141">The WM ASF Writer connects to an upstream filter, such as the DV Decoder, that outputs pixel aspect ratio information.</span></span> <span data-ttu-id="863dc-142">L’enregistreur ASF WM écrira ces informations en tant qu’extensions d’unité de données pour chaque exemple dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="863dc-142">The WM ASF Writer will write this information as data unit extensions for every sample in the file.</span></span>

<span data-ttu-id="863dc-143">Lorsque le lecteur ASF WM rencontre des informations sur les proportions de pixels dans l’en-tête de fichier ou dans les extensions d’unité de données pour les exemples, il propose un format [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) comme premier choix sur sa broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="863dc-143">When the WM ASF Reader encounters pixel aspect ratio information in the file header or in data unit extensions for the samples, it will offer a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format as a first choice on its output pin.</span></span> <span data-ttu-id="863dc-144">Les membres **dwPictAspectRatioX** et **dwPictAspectRatioY** de la structure, qui décrivent les proportions du rectangle vidéo, sont correctement ajustés pour prendre en compte les proportions en pixels.</span><span class="sxs-lookup"><span data-stu-id="863dc-144">The **dwPictAspectRatioX** and **dwPictAspectRatioY** members of the structure, which describe the video rectangle's aspect ratio, will be correctly adjusted to account for the pixel aspect ratio.</span></span>

<span data-ttu-id="863dc-145">Conserver le format entrelacé</span><span class="sxs-lookup"><span data-stu-id="863dc-145">Maintaining Interlaced Format</span></span>

<span data-ttu-id="863dc-146">Si vous capturez une vidéo entrelacée à partir d’une télévision ou d’une caméra DV, vous souhaiterez peut-être conserver la vidéo d’origine en tant que champs indépendants Si vous vous attendez à ce que le fichier encodé soit lu sur une télévision ou un autre périphérique d’affichage entrelacé.</span><span class="sxs-lookup"><span data-stu-id="863dc-146">If you capture interlaced video from a television or a DV camera, you might wish to preserve the original video as independent fields if you expect the encoded file to be played back on a television or other interlaced display device.</span></span> <span data-ttu-id="863dc-147">(Les moniteurs d’ordinateur sont des périphériques d’analyse progressive.) Si vous désentrelacez une vidéo, puis la réentrelacer pour la lire sur une télévision, une perte de données est générée.</span><span class="sxs-lookup"><span data-stu-id="863dc-147">(Computer monitors are progressive scanning devices.) If you deinterlace a video, and then reinterlace it for playback on a television, some loss of data will be incurred.</span></span> <span data-ttu-id="863dc-148">Dans un fichier ASF, les informations d’entrelacement sont stockées en tant qu’extensions d’unité de données que l’application applique à chaque exemple à l’aide de la méthode [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) décrite précédemment.</span><span class="sxs-lookup"><span data-stu-id="863dc-148">In an ASF file, interlacing information is stored as data unit extensions that the application applies to each sample using the [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) method described previously.</span></span> <span data-ttu-id="863dc-149">Pour encoder un fichier qui conserve les paramètres d’entrelacement d’origine, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="863dc-149">To encode a file that preserves the original interlace settings, follow these steps:</span></span>

1.  <span data-ttu-id="863dc-150">Implémentez une classe qui prend en charge **IAMWMBufferPassCallback** et écrivez une fonction Notify qui définit les indicateurs entrelacés pour chaque exemple.</span><span class="sxs-lookup"><span data-stu-id="863dc-150">Implement a class that supports **IAMWMBufferPassCallback** and write a Notify function that sets the interlace flags for each sample.</span></span> <span data-ttu-id="863dc-151">Cette fonction sera appelée par l’enregistreur ASF WM avant de traiter chaque exemple.</span><span class="sxs-lookup"><span data-stu-id="863dc-151">This function will be called by the WM ASF Writer before it processes each sample.</span></span>
    ```C++
    // Set to WM_CT_TOP_FIELD_FIRST if that is your format.
    BYTE flag = WM_CT_INTERLACED | WM_CT_BOTTOM_FIELD_FIRST;
    HRESULT hr = S_OK;

    hr = pNSSBuffer3->SetProperty(
        WM_SampleExtensionGUID_ContentType, 
        (void*) &flag, 
        WM_SampleExtension_ContentType_Size
        );         
    ```

    

2.  <span data-ttu-id="863dc-152">Définissez les extensions d’unité de données sur le profil avant de passer le profil au filtre.</span><span class="sxs-lookup"><span data-stu-id="863dc-152">Set the data unit extensions on the profile before you pass the profile to the filter.</span></span>
    ```C++
    hr = pWMStreamConfig2->AddDataUnitExtension(
        WM_SampleExtensionGUID_ContentType, 
        WM_SampleExtension_ContentType_Size, 
        NULL, 
        0 
        );
    ```

    

3.  <span data-ttu-id="863dc-153">Après avoir configuré le filtre avec le profil, obtenez l’interface **IWMWriterAdvanced2** à partir de l’enregistreur ASF WM et appelez la méthode **SetInputSettings** .</span><span class="sxs-lookup"><span data-stu-id="863dc-153">After you configure the filter with the profile, obtain the **IWMWriterAdvanced2** interface from the WM ASF Writer and call the **SetInputSettings** method.</span></span>

    ``

    ``

    ```C++
    // Must do this first.
    hr = pConfigAsfWriter2->ConfigureFilterUsingProfile(pProfile);
      
    CComPtr<IServiceProvider> pProvider;
    CComPtr<IWMWriterAdvanced2> pWMWA2;

    hr = pConfigAsfWriter2->QueryInterface( __uuidof(IServiceProvider),
                                             (void**)&pProvider);
    if (SUCCEEDED(hr))
    {
        hr = pProvider->QueryService(IID_IWMWriterAdvanced2,
            IID_IWMWriterAdvanced2,
            (void**)&pWMWA2);
    }

    BOOL pValue = TRUE;

    // Set the first parameter to your actual input number.
    hr = pWMWA2->SetInputSetting(0, g_wszInterlacedCoding,
        WMT_TYPE_BOOL, (BYTE*) &pValue, sizeof(WMT_TYPE_BOOL));
                
    ```

    

## <a name="related-topics"></a><span data-ttu-id="863dc-154">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="863dc-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="863dc-155">Création de fichiers ASF dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="863dc-155">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



