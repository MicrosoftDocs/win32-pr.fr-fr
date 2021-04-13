---
title: Pour transcoder du contenu avec la recompression intelligente
description: Pour transcoder du contenu avec la recompression intelligente
ms.assetid: 02398462-b0a4-4a17-84e3-4c6f9f26639f
keywords:
- Kit de développement logiciel (SDK) Windows Media format, transcodage de contenu
- Windows Media Format SDK, recompression intelligente
- Windows Media Format SDK, recompression
- Windows Media Format SDK, Windows Media Audio codecs
- ASF (Advanced Systems Format), contenu de transcodage
- ASF (format des systèmes avancés), transcodage du contenu
- Format de systèmes avancés (ASF), recompression intelligente
- ASF (format de systèmes avancés), recompression intelligente
- Format de systèmes avancés (ASF), recompression
- ASF (format des systèmes avancés), recompression
- Formats ASF (Advanced Systems Format), Windows Media Audio les codecs
- ASF (format des systèmes avancés), Windows Media Audio codecs
- contenu de transcodage
- recompression intelligente
- recompression
- Codecs Windows Media Audio, contenu de transcodage
- codecs, Windows Media Audio les codecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1317989ea9384d4a9747d712af1ce5c61d484c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314293"
---
# <a name="to-transcode-content-with-smart-recompression"></a><span data-ttu-id="a8c60-120">Pour transcoder du contenu avec la recompression intelligente</span><span class="sxs-lookup"><span data-stu-id="a8c60-120">To Transcode Content with Smart Recompression</span></span>

<span data-ttu-id="a8c60-121">Vous pouvez transcoder du contenu d’une vitesse de transmission à une autre à l’aide du kit de développement logiciel (SDK) Windows Media format.</span><span class="sxs-lookup"><span data-stu-id="a8c60-121">You can transcode content from one bit rate to another using the Windows Media Format SDK.</span></span> <span data-ttu-id="a8c60-122">Normalement, cela implique simplement le décodage du contenu et son encodage à la vitesse de transmission souhaitée.</span><span class="sxs-lookup"><span data-stu-id="a8c60-122">Normally, this involves simply decoding the content and encoding it again to the desired bit rate.</span></span> <span data-ttu-id="a8c60-123">Le codec Windows Media Audio 9 prend en charge la recompression intelligente, qui permet le transcodage qui atteint une qualité supérieure à la normale.</span><span class="sxs-lookup"><span data-stu-id="a8c60-123">The Windows Media Audio 9 codec supports smart recompression, which enables transcoding that achieves better quality than normal.</span></span>

<span data-ttu-id="a8c60-124">Pour la recompression intelligente, le flux audio d’origine doit être encodé avec le codec Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="a8c60-124">For smart recompression, the original audio stream must be encoded with the Windows Media Audio codec.</span></span> <span data-ttu-id="a8c60-125">Toutes les versions du codec sont prises en charge, mais les codecs audio spécialisés (Windows Media Audio 9 Professional et Windows Media Audio 9 Voice) ne le sont pas.</span><span class="sxs-lookup"><span data-stu-id="a8c60-125">All versions of the codec are supported, but the specialized audio codecs (Windows Media Audio 9 Professional and Windows Media Audio 9 Voice) are not.</span></span> <span data-ttu-id="a8c60-126">Si l’audio d’origine a été encodé avec le codec Windows Media Audio 9 Lossless, il n’est pas nécessaire d’utiliser la recompression intelligente, car aucune information n’a été perdue dans l’encodage d’origine.</span><span class="sxs-lookup"><span data-stu-id="a8c60-126">If the original audio was encoded with the Windows Media Audio 9 Lossless codec, there is no need to use smart recompression, because no information was lost in the original encoding.</span></span>

<span data-ttu-id="a8c60-127">Pour utiliser la recompression intelligente, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="a8c60-127">To use smart recompression, perform the following steps.</span></span>

1.  <span data-ttu-id="a8c60-128">Configurez un objet lecteur avec le fichier source pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="a8c60-128">Set up a reader object with the source file for reading.</span></span> <span data-ttu-id="a8c60-129">Pour plus d’informations, consultez [lecture de fichiers ASF](reading-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="a8c60-129">For more information, see [Reading ASF Files](reading-asf-files.md).</span></span>
2.  <span data-ttu-id="a8c60-130">Configurez un objet Writer à utiliser pour le transcodage du fichier.</span><span class="sxs-lookup"><span data-stu-id="a8c60-130">Set up a writer object to use for transcoding the file.</span></span> <span data-ttu-id="a8c60-131">Définissez le nom de fichier du nouveau fichier.</span><span class="sxs-lookup"><span data-stu-id="a8c60-131">Set the file name for the new file.</span></span> <span data-ttu-id="a8c60-132">Sélectionnez un profil à utiliser pour le nouveau fichier.</span><span class="sxs-lookup"><span data-stu-id="a8c60-132">Select a profile to use for the new file.</span></span> <span data-ttu-id="a8c60-133">Définissez le profil sélectionné dans l’objet Writer.</span><span class="sxs-lookup"><span data-stu-id="a8c60-133">Set the selected profile in the writer object.</span></span> <span data-ttu-id="a8c60-134">Pour plus d’informations, consultez [écriture de fichiers ASF](writing-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="a8c60-134">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span>
3.  <span data-ttu-id="a8c60-135">Obtenir un pointeur vers l’interface [**IWMProfile**](iwmprofile.md) de l’objet lecteur en appelant **IWMReader :: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="a8c60-135">Get a pointer to the [**IWMProfile**](iwmprofile.md) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
4.  <span data-ttu-id="a8c60-136">Récupérez l’interface [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) pour le flux audio à transcoder en appelant [**IWMProfile :: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream).</span><span class="sxs-lookup"><span data-stu-id="a8c60-136">Retrieve the [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) interface for the audio stream to be transcoded by calling [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream).</span></span>
5.  <span data-ttu-id="a8c60-137">Obtenir l’interface [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops) pour l’objet de configuration de flux en appelant **IWMStreamConfig :: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="a8c60-137">Get the [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops) interface for the stream configuration object by calling **IWMStreamConfig::QueryInterface**.</span></span>
6.  <span data-ttu-id="a8c60-138">Récupérez la structure du [**\_ \_ type de média WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) pour le flux en effectuant deux appels à [**IWMMediaProps :: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype).</span><span class="sxs-lookup"><span data-stu-id="a8c60-138">Retrieve the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure for the stream by making two calls to [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype).</span></span> <span data-ttu-id="a8c60-139">Obtenir la taille de la structure sur le premier appel et allouer de la mémoire pour qu’une mémoire tampon passe au deuxième appel.</span><span class="sxs-lookup"><span data-stu-id="a8c60-139">Get the size of the structure on the first call, and allocate memory for a buffer to pass on the second call.</span></span>
7.  <span data-ttu-id="a8c60-140">Obtenir un pointeur vers l’interface [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) pour l’entrée dans le writer en appelant [**IWMWriter :: GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).</span><span class="sxs-lookup"><span data-stu-id="a8c60-140">Get a pointer to the [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) interface for the input in the writer by calling [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).</span></span>
8.  <span data-ttu-id="a8c60-141">Obtenir l’interface [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) pour l’objet de propriétés de média d’entrée en appelant **IWMInputMediaProps :: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="a8c60-141">Get the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface for the input media properties object by calling **IWMInputMediaProps::QueryInterface**.</span></span>
9.  <span data-ttu-id="a8c60-142">Utilisez la méthode [**IWMPropertyVault :: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) pour définir la \_ propriété g wszOriginalWaveFormat.</span><span class="sxs-lookup"><span data-stu-id="a8c60-142">Use the [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) method to set the g\_wszOriginalWaveFormat property.</span></span> <span data-ttu-id="a8c60-143">Utilisez la structure **WAVEFORMATEX** obtenue à l’étape 6 comme valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="a8c60-143">Use the **WAVEFORMATEX** structure obtained in step 6 as the value of the property.</span></span>
10. <span data-ttu-id="a8c60-144">Incluez les modifications apportées aux propriétés du média d’entrée en appelant [**IWMWriter :: SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) et en lui transmettant un pointeur vers l’interface **IWMInputMediaProps** .</span><span class="sxs-lookup"><span data-stu-id="a8c60-144">Include changes made to the input media properties by calling [**IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) and passing it a pointer to the **IWMInputMediaProps** interface.</span></span>
11. <span data-ttu-id="a8c60-145">Commencez la lecture des exemples à partir du fichier d’origine et transmettez-les au writer avec des appels à [**IWMWriter :: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample).</span><span class="sxs-lookup"><span data-stu-id="a8c60-145">Begin reading samples from the original file and passing them to the writer with calls to [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8c60-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a8c60-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8c60-147">**Rubriques avancées**</span><span class="sxs-lookup"><span data-stu-id="a8c60-147">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="a8c60-148">**Interface IWMInputMediaProps**</span><span class="sxs-lookup"><span data-stu-id="a8c60-148">**IWMInputMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops)
</dt> <dt>

[<span data-ttu-id="a8c60-149">**Interface IWMMediaProps**</span><span class="sxs-lookup"><span data-stu-id="a8c60-149">**IWMMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[<span data-ttu-id="a8c60-150">**Interface IWMProfile**</span><span class="sxs-lookup"><span data-stu-id="a8c60-150">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="a8c60-151">**Interface IWMPropertyVault**</span><span class="sxs-lookup"><span data-stu-id="a8c60-151">**IWMPropertyVault Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)
</dt> <dt>

[<span data-ttu-id="a8c60-152">**Interface IWMStreamConfig**</span><span class="sxs-lookup"><span data-stu-id="a8c60-152">**IWMStreamConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> </dl>

 

 




