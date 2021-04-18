---
title: Configuration des profils et des autres propriétés de fichier (QASF)
description: Configuration des profils et des autres propriétés de fichier (QASF)
ms.assetid: a462fc8b-5a2e-4c93-828d-177d1965b734
keywords:
- Windows Media Format SDK, configuration des profils (QASF)
- Windows Media Format SDK, configuration des propriétés de fichier (QASF)
- Windows Media Format SDK, Metadata (QASF)
- ASF (Advanced Systems Format), configuration des profils (QASF)
- ASF (format des systèmes avancés), configuration des profils (QASF)
- ASF (Advanced Systems Format), configuration des propriétés de fichier (QASF)
- ASF (format des systèmes avancés), configuration des propriétés de fichier (QASF)
- ASF (Advanced Systems Format), métadonnées (QASF)
- ASF (format des systèmes avancés), métadonnées (QASF)
- Windows Media Format SDK, QASF
- ASF (Advanced Systems Format), QASF
- ASF (format avancé des systèmes), QASF
- métadonnées, QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ebb6afedfa00813e7447e5bcaefe1f251c02575
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463455"
---
# <a name="configuring-profiles-and-other-file-properties-qasf"></a><span data-ttu-id="1a866-116">Configuration des profils et des autres propriétés de fichier (QASF)</span><span class="sxs-lookup"><span data-stu-id="1a866-116">Configuring Profiles and Other File Properties (QASF)</span></span>

<span data-ttu-id="1a866-117">Les éléments suivants décrivent comment effectuer diverses tâches liées à la création de fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="1a866-117">The following items describe how to perform various tasks related to the creation of ASF files.</span></span>

## <a name="creating-a-profile-qasf"></a><span data-ttu-id="1a866-118">Création d’un profil (QASF)</span><span class="sxs-lookup"><span data-stu-id="1a866-118">Creating a Profile (QASF)</span></span>

<span data-ttu-id="1a866-119">Pour créer un profil personnalisé, utilisez le kit de développement logiciel (SDK) de format Windows Media directement pour créer un objet de gestionnaire de profils à l’aide de la fonction [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="1a866-119">To create a custom profile, use the Windows Media Format SDK directly to create a profile manager object by using the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span> <span data-ttu-id="1a866-120">Ensuite, créez le profil et transmettez-le à l' [enregistreur WM ASF](wm-asf-writer-filter.md) à l’aide de la méthode [**IConfigASFWriter :: ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="1a866-120">Next, create the profile, and pass it to the [WM ASF Writer](wm-asf-writer-filter.md) by using the [**IConfigASFWriter::ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) method.</span></span> <span data-ttu-id="1a866-121">Il s’agit de la seule façon de configurer le filtre avec un profil qui utilise les codecs de série Windows Media Audio et Video 9.</span><span class="sxs-lookup"><span data-stu-id="1a866-121">This is the only way to configure the filter with a profile that uses the Windows Media Audio and Video 9 Series codecs.</span></span> <span data-ttu-id="1a866-122">Les profils système des versions antérieures de ces codecs peuvent être ajoutés à l’aide de la méthode [**IConfigASFWriter :: ConfigureFilterUsingProfileGuid**](iconfigasfwriter-configurefilterusingprofileguid.md) .</span><span class="sxs-lookup"><span data-stu-id="1a866-122">System profiles for earlier versions of these codecs can be added by using the [**IConfigASFWriter::ConfigureFilterUsingProfileGuid**](iconfigasfwriter-configurefilterusingprofileguid.md) method.</span></span>

## <a name="adding-metadata-qasf"></a><span data-ttu-id="1a866-123">Ajout de métadonnées (QASF)</span><span class="sxs-lookup"><span data-stu-id="1a866-123">Adding Metadata (QASF)</span></span>

<span data-ttu-id="1a866-124">Pour ajouter des métadonnées à un fichier, appelez **QueryInterface** à partir de l’interface **IBaseFilter** sur le [writer WM ASF](wm-asf-writer-filter.md) pour récupérer l’interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) .</span><span class="sxs-lookup"><span data-stu-id="1a866-124">To add metadata to a file, call **QueryInterface** from the **IBaseFilter** interface on the [WM ASF Writer](wm-asf-writer-filter.md) to retrieve the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface.</span></span> <span data-ttu-id="1a866-125">Une fois que le filtre a reçu un profil, utilisez les méthodes de l’interface **IWMHeaderInfo** pour écrire les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="1a866-125">After the filter has been given a profile, use the **IWMHeaderInfo** interface methods to write the metadata.</span></span>

## <a name="indexing-a-file-qasf"></a><span data-ttu-id="1a866-126">Indexation d’un fichier (QASF)</span><span class="sxs-lookup"><span data-stu-id="1a866-126">Indexing a File (QASF)</span></span>

<span data-ttu-id="1a866-127">L’enregistreur ASF WM crée par défaut des fichiers indexés de façon temporelle.</span><span class="sxs-lookup"><span data-stu-id="1a866-127">The WM ASF Writer creates temporally indexed files by default.</span></span> <span data-ttu-id="1a866-128">Pour créer un fichier d’index de frames, utilisez la méthode [**IConfigAsfWriter :: SetIndexMode**](iconfigasfwriter-setindexmode.md) pour désactiver l’indexation, puis créez le fichier.</span><span class="sxs-lookup"><span data-stu-id="1a866-128">To create a frame-indexed file, use the [**IConfigAsfWriter::SetIndexMode**](iconfigasfwriter-setindexmode.md) method to disable all indexing, then create the file.</span></span> <span data-ttu-id="1a866-129">Une fois l’opération terminée, utilisez le kit de développement logiciel (SDK) de format Windows Media directement pour créer un index basé sur des frames pour le fichier.</span><span class="sxs-lookup"><span data-stu-id="1a866-129">When it is complete, use the Windows Media Format SDK directly to create a frame-based index for the file.</span></span>

## <a name="performing-two-pass-encoding-qasf"></a><span data-ttu-id="1a866-130">Exécution de l’encodage Two-Pass (QASF)</span><span class="sxs-lookup"><span data-stu-id="1a866-130">Performing Two-Pass Encoding (QASF)</span></span>

<span data-ttu-id="1a866-131">L’encodage en deux passes est pris en charge uniquement sur les codecs Windows Media version 8 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1a866-131">Two-pass encoding is supported only on Windows Media codecs of version 8 and later.</span></span> <span data-ttu-id="1a866-132">Placez le writer WM ASF en mode prétraitement en appelant [**IConfigAsfWriter2 :: setParam**](iconfigasfwriter2-setparam.md) et en spécifiant am \_ CONFIGASFWRITER \_ param \_ Multipass dans le paramètre *DwParam* et **true** dans le paramètre *dwParam1* .</span><span class="sxs-lookup"><span data-stu-id="1a866-132">Put the WM ASF Writer into preprocess mode by calling [**IConfigAsfWriter2::SetParam**](iconfigasfwriter2-setparam.md) and specifying AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS in the *dwParam* parameter and **TRUE** in the *dwParam1* parameter.</span></span>

<span data-ttu-id="1a866-133">Exécutez ensuite le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="1a866-133">Then run the filter graph.</span></span> <span data-ttu-id="1a866-134">Lorsque toutes les étapes de prétraitement sont effectuées (en général, une seule passe de prétraitement est effectuée), l’application reçoit un événement de **\_ \_ fin de prétraitement EC** du filtre.</span><span class="sxs-lookup"><span data-stu-id="1a866-134">When all the preprocessing passes are done (typically only one preprocessing pass will be performed), the application will receive an **EC\_PREPROCESS\_COMPLETE** event from the filter.</span></span> <span data-ttu-id="1a866-135">Lorsque cet événement est reçu, utilisez **IMediaSeeking :: SetPositions** pour réinitialiser le pointeur de flux jusqu’au début, puis exécutez à nouveau le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="1a866-135">When this event is received, use **IMediaSeeking::SetPositions** to reset the stream pointer back to the beginning, and run the filter graph again.</span></span> <span data-ttu-id="1a866-136">Après la dernière passe (en général, la deuxième passe), l’application reçoit un événement **EC \_ Complete** pour signifier que le processus d’encodage est terminé.</span><span class="sxs-lookup"><span data-stu-id="1a866-136">After the last pass (typically the second pass), the application will receive an **EC\_COMPLETE** event to signify that the encoding process is complete.</span></span> <span data-ttu-id="1a866-137">Si une passe de prétraitement est annulée avant la réception de l’événement de **\_ prétraitement \_** de l’UE, appelez [**IConfigAsfWriter2 :: ResetMultiPassState**](iconfigasfwriter2-resetmultipassstate.md) pour réinitialiser le filtre avant de tenter une autre exécution de prétraitement.</span><span class="sxs-lookup"><span data-stu-id="1a866-137">If a preprocessing pass is canceled before the **EC\_PREPROCESS\_COMPLETE** event is received, call [**IConfigAsfWriter2::ResetMultiPassState**](iconfigasfwriter2-resetmultipassstate.md) to reset the filter before attempting another preprocessing run.</span></span>

<span data-ttu-id="1a866-138">Il est uniquement nécessaire d’appeler **IConfigAsfWriter :: setParam**(am \_ CONFIGASFWRITER \_ param \_ Multipass, **false**) si vous souhaitez que le filtre soit complètement en mode de prétraitement.</span><span class="sxs-lookup"><span data-stu-id="1a866-138">It is only necessary to call **IConfigAsfWriter::SetParam**(AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS, **FALSE**) if you want to put the filter out of preprocessing mode completely.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1a866-139">Il incombe à l’application d’activer le mode de prétraitement en fonction du profil qui sera utilisé pour l’encodage.</span><span class="sxs-lookup"><span data-stu-id="1a866-139">It is the application's responsibility to enable preprocessing mode based on the profile that will be used for encoding.</span></span> <span data-ttu-id="1a866-140">Certains profils nécessitent un encodage en deux passes ; Si vous tentez d’encoder un fichier à l’aide d’un profil de ce type et que vous ne définissez pas AM \_ CONFIGASFWRITER \_ param \_ Multipass sur **true**, une \_ erreur EC USERABORT est générée.</span><span class="sxs-lookup"><span data-stu-id="1a866-140">Some profiles require two-pass encoding; if you attempt to encode a file with such a profile, and do not set AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS to **TRUE**, an EC\_USERABORT error will result.</span></span> <span data-ttu-id="1a866-141">Pour plus d’informations sur la façon de déterminer si un profil donné requiert un encodage en deux passes, consultez [utilisation de l’encodage Two-Pass](using-two-pass-encoding.md) ou [écriture de flux de vitesse de transmission variable](writing-variable-bit-rate-streams.md).</span><span class="sxs-lookup"><span data-stu-id="1a866-141">For more information on how to determine whether a given profile requires two-pass encoding, see [Using Two-Pass Encoding](using-two-pass-encoding.md) or [Writing Variable Bit Rate Streams](writing-variable-bit-rate-streams.md).</span></span>

 

## <a name="getting-and-setting-buffer-properties-at-run-time-qasf"></a><span data-ttu-id="1a866-142">Obtention et définition des propriétés de la mémoire tampon au moment de l’exécution (QASF)</span><span class="sxs-lookup"><span data-stu-id="1a866-142">Getting and Setting Buffer Properties at Run Time (QASF)</span></span>

<span data-ttu-id="1a866-143">Dans certains scénarios, par exemple, si vous souhaitez forcer l’insertion d’une image clé lors de l’écriture d’un fichier, une application peut avoir besoin d’obtenir ou de définir des informations sur un tampon Windows Media au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="1a866-143">In some scenarios, for example if you want to force key-frame insertion when writing a file, an application may need to get or set information about a Windows Media buffer at run time.</span></span> <span data-ttu-id="1a866-144">Le [lecteur ASF WM](wm-asf-reader-filter.md) et les filtres d' [enregistreur ASF WM](wm-asf-writer-filter.md) prennent tous deux en charge un mécanisme de rappel qui permet à une application d’accéder à l’interface [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) sur chaque mémoire tampon de média individuelle lors de la lecture ou de l’écriture de fichiers.</span><span class="sxs-lookup"><span data-stu-id="1a866-144">The [WM ASF Reader](wm-asf-reader-filter.md) and [WM ASF Writer](wm-asf-writer-filter.md) filters both support a callback mechanism that enables an application to access the [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) interface on each individual media buffer during file reading or file writing.</span></span> <span data-ttu-id="1a866-145">Les applications peuvent utiliser cette interface pour désigner des exemples spécifiques en tant qu’images clés, ou [*cleanpoints*](wmformat-glossary.md), pour définir des codes temporels SMPTE, pour spécifier des paramètres d’entrelacement ou pour ajouter n’importe quel type de données privées à un flux.</span><span class="sxs-lookup"><span data-stu-id="1a866-145">Applications can use this interface to designate specific samples as key frames, or [*cleanpoints*](wmformat-glossary.md), to set SMPTE time codes, to specify interlace settings, or add any type of private data to a stream.</span></span>

<span data-ttu-id="1a866-146">Utilisez l’interface [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass) pour vous inscrire aux rappels à partir du code confidentiel qui gère le flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="1a866-146">Use the [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass) interface to register for callbacks from the pin that is handling the video stream.</span></span> <span data-ttu-id="1a866-147">Lorsque le code PIN appelle votre méthode [**IAMWMBufferPassCallback :: Notify**](iamwmbufferpasscallback-notify.md) , examinez les horodatages sur la mémoire tampon et, le cas échéant, appelez [**INSSBuffer3 :: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) pour définir la propriété de **\_ \_ OutputCleanPoint WM SampleExtensionGUID** sur la mémoire tampon sur **true**.</span><span class="sxs-lookup"><span data-stu-id="1a866-147">When the pin calls your [**IAMWMBufferPassCallback::Notify**](iamwmbufferpasscallback-notify.md) method, examine the time stamps on the buffer and, if appropriate, call [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) to set the **WM\_SampleExtensionGUID\_OutputCleanPoint** property on the buffer to **TRUE**.</span></span>

## <a name="non-square-pixel-support-qasf"></a><span data-ttu-id="1a866-148">Prise en charge des pixels non carrés (QASF)</span><span class="sxs-lookup"><span data-stu-id="1a866-148">Non-Square Pixel Support (QASF)</span></span>

<span data-ttu-id="1a866-149">L’enregistreur ASF WM se connecte à un filtre en amont, tel que le décodeur DV, qui génère des informations sur les proportions en pixels.</span><span class="sxs-lookup"><span data-stu-id="1a866-149">The WM ASF Writer connects to an upstream filter, such as the DV Decoder, that outputs pixel aspect ratio information.</span></span> <span data-ttu-id="1a866-150">L’enregistreur ASF WM écrira ces informations en tant qu’extensions d’unité de données pour chaque exemple dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="1a866-150">The WM ASF Writer will write this information as data unit extensions for every sample in the file.</span></span>

<span data-ttu-id="1a866-151">Lorsque le lecteur ASF WM rencontre des informations sur les proportions de pixels dans l’en-tête de fichier ou dans les extensions d’unité de données pour les exemples, il propose un type de média **VIDEOINFOHEADER2** comme premier choix sur sa broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="1a866-151">When the WM ASF Reader encounters pixel aspect ratio information in the file header or in data unit extensions for the samples, it will offer a **VIDEOINFOHEADER2** media type as a first choice on its output pin.</span></span> <span data-ttu-id="1a866-152">Les membres **dwPictAspectRatioX** et **dwPictAspectRatioY** de la structure, qui décrivent les proportions du rectangle vidéo, sont correctement ajustés pour prendre en compte les proportions en pixels.</span><span class="sxs-lookup"><span data-stu-id="1a866-152">The **dwPictAspectRatioX** and **dwPictAspectRatioY** members of the structure, which describe the video rectangle's aspect ratio, will be correctly adjusted to account for the pixel aspect ratio.</span></span>

## <a name="maintaining-interlaced-format"></a><span data-ttu-id="1a866-153">Conserver le format entrelacé</span><span class="sxs-lookup"><span data-stu-id="1a866-153">Maintaining Interlaced Format</span></span>

<span data-ttu-id="1a866-154">Si vous capturez une vidéo entrelacée à partir d’une télévision ou d’une caméra DV, vous souhaiterez peut-être conserver la vidéo d’origine en tant que champs indépendants Si vous vous attendez à ce que le fichier encodé soit lu sur une télévision ou un autre périphérique d’affichage entrelacé.</span><span class="sxs-lookup"><span data-stu-id="1a866-154">If you capture interlaced video from a television or a DV camera, you might wish to preserve the original video as independent fields if you expect the encoded file to be played back on a television or other interlaced display device.</span></span> <span data-ttu-id="1a866-155">(Les moniteurs d’ordinateur sont des périphériques d’analyse progressive.) Si vous désentrelacez une vidéo, puis la réentrelacer pour la lire sur une télévision, une perte de données est générée.</span><span class="sxs-lookup"><span data-stu-id="1a866-155">(Computer monitors are progressive scanning devices.) If you deinterlace a video, and then reinterlace it for playback on a television, some loss of data will be incurred.</span></span> <span data-ttu-id="1a866-156">Dans un fichier ASF, les informations d’entrelacement sont stockées en tant qu’extensions d’unité de données que l’application applique à chaque exemple à l’aide de la méthode **IAMWMBufferPassCallback** décrite précédemment.</span><span class="sxs-lookup"><span data-stu-id="1a866-156">In an ASF file, interlacing information is stored as data unit extensions that the application applies to each sample using the **IAMWMBufferPassCallback** method described previously.</span></span> <span data-ttu-id="1a866-157">Pour encoder un fichier qui conserve les paramètres d’entrelacement d’origine, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="1a866-157">To encode a file that preserves the original interlace settings, follow these steps:</span></span>

-   <span data-ttu-id="1a866-158">Implémentez une classe qui prend en charge **IAMWMBufferPassCallback** et écrivez une fonction Notify qui définit les indicateurs entrelacés pour chaque exemple.</span><span class="sxs-lookup"><span data-stu-id="1a866-158">Implement a class that supports **IAMWMBufferPassCallback** and write a Notify function that sets the interlace flags for each sample.</span></span> <span data-ttu-id="1a866-159">Cette fonction sera appelée par l’enregistreur ASF WM avant de traiter chaque exemple.</span><span class="sxs-lookup"><span data-stu-id="1a866-159">This function will be called by the WM ASF Writer before it processes each sample.</span></span>


```C++
// Set to WM_CT_TOP_FIELD_FIRST if that is your format.
BYTE flag = WM_CT_INTERLACED | WM_CT_BOTTOM_FIELD_FIRST;
            HRESULT hr = pNSSBuffer3->SetProperty(WM_SampleExtensionGUID_ContentType, (void*) &flag, WM_SampleExtension_ContentType_Size);
           
```



-   <span data-ttu-id="1a866-160">Définissez les extensions d’unité de données sur le profil avant de passer le profil au filtre.</span><span class="sxs-lookup"><span data-stu-id="1a866-160">Set the data unit extensions on the profile before you pass the profile to the filter.</span></span>


```C++
hr = pWMStreamConfig2->AddDataUnitExtension( WM_SampleExtensionGUID_ContentType, WM_SampleExtension_ContentType_Size, NULL, 0 );
```



-   <span data-ttu-id="1a866-161">Après avoir configuré le filtre avec le profil, obtenez l’interface **IWMWriterAdvanced2** à partir de l’enregistreur ASF WM et appelez la méthode **SetInputSettings** .</span><span class="sxs-lookup"><span data-stu-id="1a866-161">After you configure the filter with the profile, obtain the **IWMWriterAdvanced2** interface from the WM ASF Writer and call the **SetInputSettings** method.</span></span>

`// Must do this first.`

`hr = pConfigAsfWriter2->ConfigureFilterUsingProfile(pProfile);`


```C++
  
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



 

 