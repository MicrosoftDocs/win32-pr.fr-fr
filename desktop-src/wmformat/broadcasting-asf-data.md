---
title: Diffusion de données ASF
description: Diffusion de données ASF
ms.assetid: 1b04f361-8147-4f6a-8c9d-d8eeed28550a
keywords:
- Windows Media Format SDK, diffusion de données ASF
- ASF (Advanced Systems Format), diffusion des données
- ASF (format des systèmes avancés), diffusion des données
- Windows Media Format SDK, envoyer des données ASF
- ASF (Advanced Systems Format), envoi de données
- ASF (format des systèmes avancés), envoyer des données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42339b4a3e60666c1ea0cb69a07dfdc836b19409
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/21/2020
ms.locfileid: "104030915"
---
# <a name="broadcasting-asf-data"></a><span data-ttu-id="e1fd8-109">Diffusion de données ASF</span><span class="sxs-lookup"><span data-stu-id="e1fd8-109">Broadcasting ASF Data</span></span>

<span data-ttu-id="e1fd8-110">Cette rubrique explique comment envoyer des données ASF sur un réseau à l’aide du protocole HTTP.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-110">This topic describes how to send ASF data across a network using the HTTP protocol.</span></span> <span data-ttu-id="e1fd8-111">L’envoi de fichiers sur un réseau requiert l’utilisation de l’objet Writer. vous devez donc avoir une compréhension générale de cet objet avant de lire cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-111">Sending files over a network requires the use of the writer object, so you should have a general understanding of this object before reading this topic.</span></span> <span data-ttu-id="e1fd8-112">Pour plus d’informations, consultez [écriture de fichiers ASF](writing-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="e1fd8-112">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span>

<span data-ttu-id="e1fd8-113">Si vous démarrez avec des données non compressées, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="e1fd8-113">If you are starting with uncompressed data, do the following:</span></span>

1.  <span data-ttu-id="e1fd8-114">Créez l’objet writer en appelant la fonction [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) .</span><span class="sxs-lookup"><span data-stu-id="e1fd8-114">Create the writer object by calling the [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) function.</span></span> <span data-ttu-id="e1fd8-115">Cette fonction retourne un pointeur **IWMWriter** .</span><span class="sxs-lookup"><span data-stu-id="e1fd8-115">This function returns an **IWMWriter** pointer.</span></span>
    ```C++
    IWMWriter *pWriter;
    hr = WMCreateWriter(NULL, &pWriter);
    ```

    

2.  <span data-ttu-id="e1fd8-116">Créez l’objet récepteur réseau en appelant la fonction [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink) , qui retourne un pointeur **IWMWriterNetworkSink** .</span><span class="sxs-lookup"><span data-stu-id="e1fd8-116">Create the network sink object by calling the [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink) function, which returns an **IWMWriterNetworkSink** pointer.</span></span>
    ```C++
    IWMWriterNetworkSink *pNetSink;
    hr = WMCreateWriterNetworkSink(&pNetSink);
    ```

    

3.  <span data-ttu-id="e1fd8-117">Appelez [**IWMWriterNetworkSink :: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-open) sur le récepteur réseau et spécifiez le numéro de port à ouvrir. par exemple, 8080.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-117">Call [**IWMWriterNetworkSink::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-open) on the network sink and specify the port number to open; for example, 8080.</span></span> <span data-ttu-id="e1fd8-118">Vous pouvez également appeler [**IWMWriterNetworkSink :: GetHostURL**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-gethosturl) pour récupérer l’URL de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-118">Optionally, call [**IWMWriterNetworkSink::GetHostURL**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-gethosturl) to get the URL of the host.</span></span> <span data-ttu-id="e1fd8-119">Les clients accéderont au contenu à partir de cette URL.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-119">Clients will access the content from this URL.</span></span> <span data-ttu-id="e1fd8-120">Vous pouvez également appeler [**IWMWriterNetworkSink :: SetMaximumClients**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-setmaximumclients) pour restreindre le nombre de clients.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-120">You can also call [**IWMWriterNetworkSink::SetMaximumClients**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-setmaximumclients) to restrict the number of clients.</span></span>
    ```C++
    DWORD dwPortNum = 8080;
    hr = pNetSink->Open( &dwPortNum)
    ```

    

4.  <span data-ttu-id="e1fd8-121">Attachez le récepteur réseau au writer en appelant [**IWMWriterAdvanced :: AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) sur le writer, avec un pointeur vers l’interface **IWMWriterNetworkSink** du récepteur réseau.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-121">Attach the network sink to the writer by calling [**IWMWriterAdvanced::AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) on the writer, with a pointer to the network sink's **IWMWriterNetworkSink** interface.</span></span>
    ```C++
    IWMWriterAdvanced *pWriterAdvanced;
    hr = pWriter->QueryInterface(IID_IWMWriterAdvanced, ( void** ) pWriterAdvanced );
    if (SUCCEEDED(hr))
    {
        pWriterAdvanced->AddSink(pNetSink);
    }
    ```

    

5.  <span data-ttu-id="e1fd8-122">Définissez le profil ASF en appelant la méthode [**IWMWriter :: SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) sur l’objet Writer, avec un pointeur [**IWMProfile**](iwmprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="e1fd8-122">Set the ASF profile by calling the [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) method on the writer object, with an [**IWMProfile**](iwmprofile.md) pointer.</span></span> <span data-ttu-id="e1fd8-123">Pour plus d’informations sur la création d’un profil, consultez [utilisation des profils](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="e1fd8-123">For information about creating a profile, see [Working with Profiles](working-with-profiles.md).</span></span>
6.  <span data-ttu-id="e1fd8-124">Si vous le souhaitez, spécifiez des métadonnées à l’aide de l’interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) sur le writer.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-124">Optionally, specify metadata using the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface on the writer.</span></span>
7.  <span data-ttu-id="e1fd8-125">Appelez [**IWMWriter :: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting) sur le writer.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-125">Call [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting) on the writer.</span></span>
    ```C++
    hr = pWriter->BeginWriting();
    ```

    

8.  <span data-ttu-id="e1fd8-126">Pour chaque exemple, appelez la méthode [**IWMWriter :: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) .</span><span class="sxs-lookup"><span data-stu-id="e1fd8-126">For each sample, call the [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) method.</span></span> <span data-ttu-id="e1fd8-127">Spécifiez le numéro du flux, l’heure de la présentation, la durée de l’échantillon et un pointeur vers l’exemple de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-127">Specify the stream number, the presentation time, the duration of the sample, and a pointer to the sample buffer.</span></span> <span data-ttu-id="e1fd8-128">La méthode **WriteSample** compresse les exemples.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-128">The **WriteSample** method compresses the samples.</span></span>
9.  <span data-ttu-id="e1fd8-129">Lorsque vous avez terminé, appelez [**IWMWriter :: EndWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting) sur le writer.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-129">When you are done, call [**IWMWriter::EndWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting) on the writer.</span></span>
    ```C++
    hr = pWriter->EndWriting();
    ```

    

10. <span data-ttu-id="e1fd8-130">Appelez [**IWMWriterAdvanced :: RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) sur le writer pour détacher l’objet récepteur réseau.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-130">Call [**IWMWriterAdvanced::RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) on the writer to detach the network sink object.</span></span>
    ```C++
    hr = pWriterAdvanced->RemoveSink(pNetSink);
    ```

    

11. <span data-ttu-id="e1fd8-131">Appelez [**IWMWriterNetworkSink :: Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-close) sur le récepteur réseau pour libérer le port.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-131">Call [**IWMWriterNetworkSink::Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-close) on the network sink to release the port.</span></span>
    ```C++
    hr = pNetSink->Close();
    ```

    

<span data-ttu-id="e1fd8-132">Une autre façon de diffuser du contenu ASF sur un réseau consiste à le lire à partir d’un fichier ASF existant.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-132">Another way to stream ASF content over a network is to read it from an existing ASF file.</span></span> <span data-ttu-id="e1fd8-133">L’exemple WMVNetWrite fourni dans le kit de développement logiciel (SDK) illustre cette approche.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-133">The WMVNetWrite sample provided in the SDK demonstrates this approach.</span></span> <span data-ttu-id="e1fd8-134">En plus des étapes indiquées précédemment, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="e1fd8-134">In addition to the steps listed previously, do the following:</span></span>

1.  <span data-ttu-id="e1fd8-135">Créez un objet lecteur et appelez la méthode **Open** avec le nom du fichier.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-135">Create a reader object and call the **Open** method with the name of the file.</span></span>
2.  <span data-ttu-id="e1fd8-136">Appelez [**IWMReaderAdvanced :: SetManualStreamSelection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection) sur l’objet Reader, avec la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-136">Call [**IWMReaderAdvanced::SetManualStreamSelection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection) on the reader object, with the value **TRUE**.</span></span> <span data-ttu-id="e1fd8-137">Cela permet à l’application de lire chaque flux du fichier, y compris les flux avec exclusion mutuelle.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-137">This enables the application to read every stream in the file, including streams with mutual exclusion.</span></span>
3.  <span data-ttu-id="e1fd8-138">Interrogez le lecteur de l’interface [**IWMProfile**](iwmprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="e1fd8-138">Query the reader for the [**IWMProfile**](iwmprofile.md) interface.</span></span> <span data-ttu-id="e1fd8-139">Utilisez ce pointeur lorsque vous appelez [**IWMWriter :: SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) sur l’objet Writer (étape 5 de la procédure précédente).</span><span class="sxs-lookup"><span data-stu-id="e1fd8-139">Use this pointer when you call [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) on the writer object (step 5 in the previous procedure).</span></span>
4.  <span data-ttu-id="e1fd8-140">Pour chaque flux défini dans le profil, appelez [**IWMProfile :: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) pour obtenir le numéro du flux.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-140">For every stream defined in the profile, call [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) to get the stream number.</span></span> <span data-ttu-id="e1fd8-141">Transmettez ce numéro de flux à la méthode [**IWMReaderAdvanced :: SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples) du lecteur.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-141">Pass this stream number to the reader's [**IWMReaderAdvanced::SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples) method.</span></span> <span data-ttu-id="e1fd8-142">Cette méthode informe le lecteur qu’il doit remettre des exemples compressés, plutôt que de les décoder.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-142">This method informs the reader to deliver compressed samples, rather than decoding them.</span></span> <span data-ttu-id="e1fd8-143">Les exemples sont remis à l’application par le biais de la méthode de rappel [**IWMReaderCallbackAdvanced :: OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) de l’application.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-143">The samples will be delivered to the application through the application's [**IWMReaderCallbackAdvanced::OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) callback method.</span></span>

    <span data-ttu-id="e1fd8-144">Vous devez obtenir les informations de codec pour chaque flux que vous lisez non compressé et l’ajouter à l’en-tête avant la diffusion.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-144">You must obtain codec information for every stream that you read uncompressed and add it to the header before broadcast.</span></span> <span data-ttu-id="e1fd8-145">Pour obtenir les informations du codec, appelez [**IWMHeaderInfo2 :: GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) et [**IWMHeaderInfo2 :: GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) pour énumérer les codecs associés au fichier dans le lecteur.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-145">To obtain the codec information, call [**IWMHeaderInfo2::GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) and [**IWMHeaderInfo2::GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) to enumerate the codecs associated with the file in the reader.</span></span> <span data-ttu-id="e1fd8-146">Sélectionnez les informations du codec qui correspondent à la configuration du flux.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-146">Select the codec information that matches the stream configuration.</span></span> <span data-ttu-id="e1fd8-147">Définissez ensuite les informations du codec dans le writer en appelant [**IWMHeaderInfo3 :: AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), en passant les informations obtenues à partir du lecteur.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-147">Then set the codec information in the writer by calling [**IWMHeaderInfo3::AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), passing the information obtained from the reader.</span></span>

5.  <span data-ttu-id="e1fd8-148">Une fois que vous avez défini le profil sur le writer, appelez [**IWMWriter :: GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount) sur le writer pour connaître le nombre d’entrées.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-148">After you set the profile on the writer, call [**IWMWriter::GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount) on the writer to get the number of inputs.</span></span> <span data-ttu-id="e1fd8-149">Pour chaque entrée, appelez [**IWMWriter :: SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) avec la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-149">For each input, call [**IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) with the value **NULL**.</span></span> <span data-ttu-id="e1fd8-150">Cela indique à l’objet enregistreur que l’application remet les exemples compressés, de sorte que le Writer n’a pas besoin d’utiliser de codec pour compresser les données.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-150">This indicates to the writer object that the application will deliver compressed samples, so the writer does not have to use any codecs to compress the data.</span></span> <span data-ttu-id="e1fd8-151">Veillez à appeler **SetInputProps** avant d’appeler **BeginWriting**.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-151">Make sure to call **SetInputProps** before calling **BeginWriting**.</span></span>
6.  <span data-ttu-id="e1fd8-152">Éventuellement, copiez les attributs de métadonnées du lecteur vers le writer.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-152">Optionally, copy the metadata attributes from the reader to the writer</span></span>
7.  <span data-ttu-id="e1fd8-153">Étant donné que les exemples du lecteur sont déjà compressés, utilisez la méthode [**IWMWriterAdvanced :: WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) pour écrire les exemples au lieu de la méthode **WriteSample** .</span><span class="sxs-lookup"><span data-stu-id="e1fd8-153">Because the samples from the reader are already compressed, use the [**IWMWriterAdvanced::WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) method to write the samples, instead of the **WriteSample** method.</span></span> <span data-ttu-id="e1fd8-154">La méthode **WriteStreamSample** ignore les procédures de compression habituelles de l’objet Writer.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-154">The **WriteStreamSample** method bypasses the writer object's usual compression procedures.</span></span>
8.  <span data-ttu-id="e1fd8-155">Lorsque le lecteur atteint la fin du fichier, il envoie une \_ notification de EOF WMT à l’application.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-155">When the reader reaches the end of the file, it sends a WMT\_EOF notification to the application.</span></span>

<span data-ttu-id="e1fd8-156">En outre, l’application doit piloter l’horloge sur l’objet lecteur, afin que le lecteur extraie les données du fichier le plus rapidement possible.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-156">In addition, the application should drive the clock on the reader object, so that the reader pulls data from the file as quickly as possible.</span></span> <span data-ttu-id="e1fd8-157">Pour ce faire, appelez la méthode [**IWMReaderAdvanced :: SetUserProvidedClock**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setuserprovidedclock) sur le lecteur, avec la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-157">To do this, call the [**IWMReaderAdvanced::SetUserProvidedClock**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setuserprovidedclock) method on the reader, with the value **TRUE**.</span></span> <span data-ttu-id="e1fd8-158">Une fois que le lecteur a envoyé la notification de démarrage de WMT \_ , appelez [**IWMReaderAdvanced ::D elivertime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-delivertime) et spécifiez l’intervalle de temps que le lecteur doit remettre.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-158">After the reader sends the WMT\_STARTED notification, call [**IWMReaderAdvanced::DeliverTime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-delivertime) and specify the time interval that the reader should deliver.</span></span> <span data-ttu-id="e1fd8-159">Une fois que le lecteur a fini de lire cet intervalle de temps, il appelle la méthode de rappel [**IWMReaderCallbackAdvanced :: OnTime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-ontime) de l’application.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-159">After the reader is done reading this time interval, it calls the application's [**IWMReaderCallbackAdvanced::OnTime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-ontime) callback method.</span></span> <span data-ttu-id="e1fd8-160">L’application doit à nouveau appeler **DeliverTime** pour lire l’intervalle de temps suivant.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-160">The application should call **DeliverTime** again to read the next time interval.</span></span> <span data-ttu-id="e1fd8-161">Par exemple, pour lire le fichier à intervalles d’une seconde :</span><span class="sxs-lookup"><span data-stu-id="e1fd8-161">For example, to read from the file in one-second intervals:</span></span>


```C++
// Initial call to DeliverTime.
QWORD m_qwTime = 10000000; // 1 second.
hr = m_pReaderAdvanced->DeliverTime(m_qwTime);

// In the callback:
HRESULT CNetWrite::OnTime(QWORD cnsCurrentTime, void *pvContext)
{
    HRESULT hr = S_OK;
    // Continue calling DeliverTime until the end of the file.
    if(!m_bEOF)
    {
        m_qwTime += 10000000; // 1 second.
        hr = m_pReaderAdvanced->DeliverTime(m_qwTime);
    }
    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="e1fd8-162">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e1fd8-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1fd8-163">**Envoi de données ASF sur un réseau**</span><span class="sxs-lookup"><span data-stu-id="e1fd8-163">**Sending ASF Data Over a Network**</span></span>](sending-asf-data-over-a-network.md)
</dt> <dt>

[<span data-ttu-id="e1fd8-164">**Utilisation des récepteurs d’écriture**</span><span class="sxs-lookup"><span data-stu-id="e1fd8-164">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




