---
title: Configuration de l’enregistreur ASF de WM (QASF)
description: Configuration de l’enregistreur ASF de WM (QASF)
ms.assetid: 0f49ed5a-c228-456a-9551-8d277adccd0e
keywords:
- Windows Media Format SDK, configuration de l’enregistreur ASF de WM (QASF)
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, WM ASF Writer
- Windows Media Format SDK, QASF
- ASF (Advanced Systems Format), configuration de l’enregistreur ASF ASF (QASF)
- ASF (format avancé des systèmes), configuration de l’enregistreur ASF ASF (QASF)
- ASF (Advanced Systems Format), le rédacteur WM ASF
- ASF (format des systèmes avancés), enregistreur ASF WM
- ASF (Advanced Systems Format), DirectShow
- ASF (format avancé des systèmes), DirectShow
- ASF (Advanced Systems Format), QASF
- ASF (format avancé des systèmes), QASF
- DirectShow, configuration de l’enregistreur ASF de WM (QASF)
- DirectShow, auteur WM ASF
- DirectShow, QASF
- Rédacteur ASF WM, configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72f954522c4acae89e6f6dd001561811088c2a9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102148"
---
# <a name="configuring-the-wm-asf-writer-qasf"></a><span data-ttu-id="e4525-119">Configuration de l’enregistreur ASF de WM (QASF)</span><span class="sxs-lookup"><span data-stu-id="e4525-119">Configuring the WM ASF Writer (QASF)</span></span>

<span data-ttu-id="e4525-120">Lorsque le filtre de l' [enregistreur ASF WM](wm-asf-writer-filter.md) est créé, il est configuré automatiquement avec le \_ Profil WMProfile V80 \_ 256Video comme valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="e4525-120">When the [WM ASF Writer](wm-asf-writer-filter.md) filter is created, it is configured automatically with the WMProfile\_V80\_256Video profile as a default.</span></span> <span data-ttu-id="e4525-121">Étant donné que ce profil utilise les codecs Windows Media Audio et Windows Media Video version 8, il est recommandé de créer un profil personnalisé qui utilise les codecs de la série Windows Media 9, puis de passer son pointeur [**IWMProfile**](iwmprofile.md) au filtre à l’aide de la méthode [**IConfigAsfWriter :: ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="e4525-121">Because this profile uses the Windows Media Audio and Windows Media Video version 8 codecs, it is recommended that you create a custom profile that uses the Windows Media 9 Series codecs, and then pass its [**IWMProfile**](iwmprofile.md) pointer to the filter using the [**IConfigAsfWriter::ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) method.</span></span> <span data-ttu-id="e4525-122">Le filtre doit être ajouté au graphique pour que le filtre puisse être configuré, et il doit être configuré avant de pouvoir être connecté aux filtres en amont.</span><span class="sxs-lookup"><span data-stu-id="e4525-122">The filter must be added to the graph before the filter can be configured, and it must be configured before it can be connected to upstream filters.</span></span> <span data-ttu-id="e4525-123">Le filtre utilise le profil pour déterminer le type de fichier de format Windows Media à écrire, le nombre de broches d’entrée à configurer et les types de média que les épingles peuvent accepter.</span><span class="sxs-lookup"><span data-stu-id="e4525-123">The filter uses the profile to determine what kind of Windows Media Format file to write, how many input pins to set up, and what media types the pins can accept.</span></span>

<span data-ttu-id="e4525-124">Le filtre autorise la réinitialisation des profils lorsque leurs broches d’entrée sont connectées, tant que le nouveau profil ne nécessite pas de broches d’entrée supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="e4525-124">The filter allows profiles to be reset while its input pins are connected, as long as the new profile does not require any additional input pins.</span></span> <span data-ttu-id="e4525-125">Par exemple, si vous modifiez le profil d’un profil audio à entrée unique en un profil audio et vidéo à deux entrées, seul le code confidentiel audio sera reconnectedAll les données d’entrée doivent être horodatées et toutes les broches d’entrée doivent être connectées pour que le filtre puisse être exécuté ou suspendu.</span><span class="sxs-lookup"><span data-stu-id="e4525-125">For example, if you change the profile from a one-input audio-only profile to a two-input audio and video profile, just the audio pin will be reconnectedAll input data must be time-stamped, and all input pins must be connected before the filter can be run or paused.</span></span> <span data-ttu-id="e4525-126">Cela signifie que si vous configurez le filtre avec un profil qui a un flux audio et un flux vidéo, le filtre crée un fichier audio et une broche d’entrée vidéo, et les deux broches doivent être connectées pour que le filtre puisse être exécuté.</span><span class="sxs-lookup"><span data-stu-id="e4525-126">This means that if you configure the filter with a profile that has an audio stream and a video stream, the filter will create an audio and a video input pin, and both pins must be connected before the filter can be run.</span></span>

<span data-ttu-id="e4525-127">Ajout d’extensions d’unité de données</span><span class="sxs-lookup"><span data-stu-id="e4525-127">Adding Data Unit Extensions</span></span>

<span data-ttu-id="e4525-128">Vous pouvez configurer un flux de profil pour les extensions d’unité de données, telles que les codes temporels SMPTE, avant ou après la connexion du filtre, à condition que vous suiviez cet ordre d’opérations :</span><span class="sxs-lookup"><span data-stu-id="e4525-128">You can configure a profile stream for data unit extensions, such as SMPTE time codes, either before or after the filter is connected, as long as you follow this order of operations:</span></span>

1.  <span data-ttu-id="e4525-129">Ajoutez une ou plusieurs extensions d’unité de données au flux à l’aide de [**IWMStreamConfig2 :: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension).</span><span class="sxs-lookup"><span data-stu-id="e4525-129">Add one or more data unit extensions to the stream using [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension).</span></span>
2.  <span data-ttu-id="e4525-130">Appelez [**WMProfile :: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) pour mettre à jour le profil.</span><span class="sxs-lookup"><span data-stu-id="e4525-130">Call [**WMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) to update the profile.</span></span>
3.  <span data-ttu-id="e4525-131">Appelez [**IConfigAsfWriter :: ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) avec l’objet de profil mis à jour.</span><span class="sxs-lookup"><span data-stu-id="e4525-131">Call [**IConfigAsfWriter::ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) with the updated profile object.</span></span>
4.  <span data-ttu-id="e4525-132">Recherchez la broche d’entrée vidéo et appelez sa méthode [**IAMWMBufferPass :: SetNotify**](iamwmbufferpass-setnotify.md) pour inscrire votre interface [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="e4525-132">Find the video input pin, and call its [**IAMWMBufferPass::SetNotify**](iamwmbufferpass-setnotify.md) method to register your application-defined [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) interface.</span></span>

<span data-ttu-id="e4525-133">Lorsque le graphique est exécuté, votre méthode [**IAMWMBufferPassCallback :: Notify**](iamwmbufferpasscallback-notify.md) est appelée pour chaque frame, et vous pouvez obtenir et définir des propriétés sur l’exemple à l’aide de ses méthodes d’interface [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) .</span><span class="sxs-lookup"><span data-stu-id="e4525-133">When the graph runs, your [**IAMWMBufferPassCallback::Notify**](iamwmbufferpasscallback-notify.md) method will be called for each frame, and you will be able to get and set properties on the sample using its [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) interface methods.</span></span>

> [!Note]  
> <span data-ttu-id="e4525-134">Dans certains scénarios nécessitant beaucoup de ressources processeur, comme inverse telecine, le rédacteur WM ASF peut nécessiter plus de tampons de sortie que certains filtres en aval peuvent prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="e4525-134">In some processor-intensive scenarios such as inverse telecine, the WM ASF Writer may require more output buffers than some downstream filters can support.</span></span> <span data-ttu-id="e4525-135">Par exemple, le décodeur DV n’acceptera pas plus d’une mémoire tampon pour sa broche de sortie et c’est le cas pour le décompresseur AVI dans certaines conditions.</span><span class="sxs-lookup"><span data-stu-id="e4525-135">The DV Decoder, for example, will not accept more than one buffer for its output pin and the same is true for the AVI Decompressor in certain conditions.</span></span> <span data-ttu-id="e4525-136">Si vous rencontrez des problèmes lors de la tentative de connexion à ces filtres, ou éventuellement lors de l’exécution du graphique, il peut être nécessaire d’écrire un filtre intermédiaire qui accepte un nombre quelconque de mémoires tampons sur sa broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="e4525-136">If you encounter problems when attempting to connect to these filters, or possibly when running the graph, it may be necessary to write an intermediary filter that accepts any number of buffers on its output pin.</span></span>

 

 

 