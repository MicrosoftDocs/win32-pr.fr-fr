---
title: Écriture de flux avec des pixels non carrés
description: Écriture de flux avec des pixels non carrés
ms.assetid: 4af7dedc-e2b8-4dc2-add4-84424e93c297
keywords:
- Windows Media Format SDK, écriture de flux vidéo
- Kit de développement logiciel (SDK) Windows Media format, flux vidéo
- Windows Media Format SDK, pixels non carrés
- Windows Media Format SDK, pixels (non carrés)
- ASF (Advanced Systems Format), écriture de flux vidéo
- ASF (format avancé des systèmes), écriture de flux vidéo
- ASF (Advanced Systems Format), flux vidéo
- ASF (format de systèmes avancés), flux vidéo
- ASF (Advanced Systems Format), pixels non carrés
- ASF (format des systèmes avancés), pixels non carrés
- Format de systèmes avancés (ASF), pixels (non carrés)
- ASF (format des systèmes avancés), pixels (non carrés)
- écriture de flux vidéo
- flux vidéo, écriture
- flux vidéo, pixels non carrés
- pixels non carrés
- pixels (non carrés)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1349840f151ab787ba0e0512cfab8fea08aacf1
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030797"
---
# <a name="writing-streams-with-non-square-pixels"></a><span data-ttu-id="9351c-120">Écriture de flux avec des pixels non carrés</span><span class="sxs-lookup"><span data-stu-id="9351c-120">Writing Streams with Non-Square Pixels</span></span>

<span data-ttu-id="9351c-121">Il existe deux façons de créer des flux vidéo avec des pixels non carrés qui s’affichent correctement dans le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="9351c-121">There are two ways to create video streams with non-square pixels that will be displayed correctly in Windows Media Player.</span></span> <span data-ttu-id="9351c-122">La première technique consiste à définir des attributs au niveau du flux dans l’en-tête du fichier.</span><span class="sxs-lookup"><span data-stu-id="9351c-122">The first technique involves setting stream-level attributes in the file header.</span></span> <span data-ttu-id="9351c-123">La deuxième technique implique l’ajout d’une extension d’unité de données à un flux du profil, puis la définition d’une valeur pour celle-ci dans chaque exemple écrit.</span><span class="sxs-lookup"><span data-stu-id="9351c-123">The second technique involves adding a data unit extension to a stream in the profile, and then setting a value for it in every sample that is written.</span></span>

## <a name="to-use-stream-level-header-attributes-to-set-pixel-aspect-ratio"></a><span data-ttu-id="9351c-124">Pour utiliser des attributs d’en-tête au niveau du flux pour définir les proportions de pixels</span><span class="sxs-lookup"><span data-stu-id="9351c-124">To Use Stream-level Header Attributes to Set Pixel Aspect Ratio</span></span>

1.  <span data-ttu-id="9351c-125">Configurez l’objet Writer.</span><span class="sxs-lookup"><span data-stu-id="9351c-125">Set up the writer object.</span></span> <span data-ttu-id="9351c-126">Pour plus d’informations, consultez [écriture de fichiers ASF](writing-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="9351c-126">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span>
2.  <span data-ttu-id="9351c-127">Créez ou chargez un profil avec un ou plusieurs flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="9351c-127">Create or load a profile with one or more video streams.</span></span> <span data-ttu-id="9351c-128">Pour plus d’informations, consultez [pour utiliser des profils avec le writer](to-use-profiles-with-the-writer.md).</span><span class="sxs-lookup"><span data-stu-id="9351c-128">For more information, see [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md).</span></span>
3.  <span data-ttu-id="9351c-129">Appelez [**IWMWriter :: SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).</span><span class="sxs-lookup"><span data-stu-id="9351c-129">Call [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).</span></span> <span data-ttu-id="9351c-130">(Appelez toujours cette méthode avant de définir des attributs d’en-tête.)</span><span class="sxs-lookup"><span data-stu-id="9351c-130">(Always call this method before setting any header attributes.)</span></span>
4.  <span data-ttu-id="9351c-131">Appelez **QueryInterface** pour obtenir l’interface [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) et appelez [**AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) à deux reprises pour ajouter [**AspectRatioX**](aspectratiox.md) et [**AspectRatioY**](aspectratioy.md) en tant qu’attributs de niveau flux du flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="9351c-131">Call **QueryInterface** to obtain the [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) interface and call [**AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) twice to add [**AspectRatioX**](aspectratiox.md) and [**AspectRatioY**](aspectratioy.md) as stream-level attributes of the video stream.</span></span> <span data-ttu-id="9351c-132">Ces attributs sont des valeurs **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="9351c-132">These attributes are **DWORD** values.</span></span>
5.  <span data-ttu-id="9351c-133">Écrivez le fichier.</span><span class="sxs-lookup"><span data-stu-id="9351c-133">Write the file.</span></span>

## <a name="to-use-data-unit-extensions-to-set-pixel-aspect-ratio"></a><span data-ttu-id="9351c-134">Pour utiliser les extensions d’unité de données pour définir les proportions de pixels</span><span class="sxs-lookup"><span data-stu-id="9351c-134">To Use Data Unit Extensions to Set Pixel Aspect Ratio</span></span>

<span data-ttu-id="9351c-135">**Avant d’écrire :**</span><span class="sxs-lookup"><span data-stu-id="9351c-135">**Before writing:**</span></span>

1.  <span data-ttu-id="9351c-136">Configurez l’objet Writer.</span><span class="sxs-lookup"><span data-stu-id="9351c-136">Set up the writer object.</span></span> <span data-ttu-id="9351c-137">Pour plus d’informations, consultez [écriture de fichiers ASF](writing-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="9351c-137">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span>
2.  <span data-ttu-id="9351c-138">Créez ou chargez un profil avec un ou plusieurs flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="9351c-138">Create or load a profile with one or more video streams.</span></span> <span data-ttu-id="9351c-139">Pour plus d’informations, consultez [pour utiliser des profils avec le writer](to-use-profiles-with-the-writer.md).</span><span class="sxs-lookup"><span data-stu-id="9351c-139">For more information, see [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md).</span></span>
3.  <span data-ttu-id="9351c-140">Pour chaque flux (de n’importe quel type de média) dans le profil, appelez [**IWMStreamConfig :: SetStreamName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname) pour spécifier un nom unique de votre choix.</span><span class="sxs-lookup"><span data-stu-id="9351c-140">For each stream (of any media type) in the profile, call [**IWMStreamConfig::SetStreamName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname) to specify a unique name of your choice.</span></span> <span data-ttu-id="9351c-141">Ne donnez pas le même nom à deux flux.</span><span class="sxs-lookup"><span data-stu-id="9351c-141">Do not give two streams the same name.</span></span>
4.  <span data-ttu-id="9351c-142">Utilisez [**IWMStreamConfig2 :: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) sur le flux vidéo pour ajouter une extension d’unité de données pour les proportions de pixels.</span><span class="sxs-lookup"><span data-stu-id="9351c-142">Use [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) on the video stream to add a data unit extension for pixel aspect ratio.</span></span>
5.  <span data-ttu-id="9351c-143">Appelez [**IWMWriter :: SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).</span><span class="sxs-lookup"><span data-stu-id="9351c-143">Call [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).</span></span>
6.  <span data-ttu-id="9351c-144">Écrivez le fichier.</span><span class="sxs-lookup"><span data-stu-id="9351c-144">Write the file.</span></span>

<span data-ttu-id="9351c-145">**Lors de l’écriture :**</span><span class="sxs-lookup"><span data-stu-id="9351c-145">**While writing:**</span></span>

-   <span data-ttu-id="9351c-146">Pour chaque exemple, appelez [**INSSBuffer3 :: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) et spécifiez la \_ propriété WM SampleExtensionGUID \_ PixelAspectRatio, ainsi que la valeur correcte.</span><span class="sxs-lookup"><span data-stu-id="9351c-146">For each sample, call [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) and specify the WM\_SampleExtensionGUID\_PixelAspectRatio property along with the correct value.</span></span> <span data-ttu-id="9351c-147">Les valeurs de proportions sont écrites sous la forme de deux valeurs concaténées à deux chiffres.</span><span class="sxs-lookup"><span data-stu-id="9351c-147">Aspect ratio values are written as two concatenated two-digit values.</span></span> <span data-ttu-id="9351c-148">Par exemple, 16:9 est écrit sous la forme 1609 ou 0x0649.</span><span class="sxs-lookup"><span data-stu-id="9351c-148">For example, 16:9 is written as 1609 or 0x0649.</span></span> <span data-ttu-id="9351c-149">Il s’agit toujours d’une valeur de 2 octets.</span><span class="sxs-lookup"><span data-stu-id="9351c-149">This is always a 2-byte value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9351c-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9351c-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9351c-151">**Pour lire et écrire des flux vidéo avec des pixels non carrés**</span><span class="sxs-lookup"><span data-stu-id="9351c-151">**To Read and Write Video Streams with Non-Square Pixels**</span></span>](to-read-and-write-video-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




