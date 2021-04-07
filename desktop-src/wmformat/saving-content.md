---
title: Enregistrement du contenu
description: Enregistrement du contenu
ms.assetid: 22f4e580-43a4-48b5-8eb3-90e1346a1093
keywords:
- Windows Media Format SDK, enregistrement du contenu
- Windows Media Format SDK, Fast cache streaming
- ASF (Advanced Systems Format), enregistrement du contenu
- ASF (format des systèmes avancés), enregistrement du contenu
- ASF (Advanced Systems Format), diffusion en continu du cache rapide
- ASF (format de systèmes avancés), diffusion en continu de cache rapide
- flux, enregistrement du contenu
- Diffusion en continu rapide du cache, enregistrement du contenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba6c215a81accef29f8943ed52ca24264f785d94
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724082"
---
# <a name="saving-content"></a><span data-ttu-id="01d34-111">Enregistrement du contenu</span><span class="sxs-lookup"><span data-stu-id="01d34-111">Saving Content</span></span>

<span data-ttu-id="01d34-112">À l’aide de ce kit de développement logiciel (SDK), une application peut enregistrer le contenu téléchargé ou diffusé sur l’ordinateur local de l’utilisateur, en appelant la méthode [**IWMReaderAdvanced2 :: SaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) sur l’objet lecteur.</span><span class="sxs-lookup"><span data-stu-id="01d34-112">By using this SDK, an application can save downloaded or streamed content to the user's local computer, by calling the [**IWMReaderAdvanced2::SaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) method on the reader object.</span></span> <span data-ttu-id="01d34-113">Pour le contenu diffusé en continu, le serveur doit utiliser Fast cache streaming, qui est décrit dans la section [activation de la diffusion en continu du cache rapide à partir du client](enabling-fast-cache-streaming-from-the-client.md).</span><span class="sxs-lookup"><span data-stu-id="01d34-113">For streamed content, the server must be using Fast Cache streaming, which is described in the section [Enabling Fast Cache Streaming from the Client](enabling-fast-cache-streaming-from-the-client.md).</span></span> <span data-ttu-id="01d34-114">Pour le contenu diffusé en continu, la méthode **SaveFileAs** crée un fichier ASX qui pointe vers un fichier ASF contenant le contenu enregistré.</span><span class="sxs-lookup"><span data-stu-id="01d34-114">For streamed content, the **SaveFileAs** method creates an ASX file that points to an ASF file containing the saved content.</span></span> <span data-ttu-id="01d34-115">Si l’objet lecteur diffuse en continu une sélection côté serveur, chaque entrée est enregistrée en tant que fichier ASF distinct, et le fichier ASX pointe vers chacun des fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="01d34-115">If the reader object is streaming a server-side playlist, each entry is saved as a separate ASF file, and the ASX file points to each of the ASF files.</span></span> <span data-ttu-id="01d34-116">Pour le contenu téléchargé, la méthode **SaveFileAs** crée simplement un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="01d34-116">For downloaded content, the **SaveFileAs** method simply creates an ASF file.</span></span>

<span data-ttu-id="01d34-117">Pour enregistrer du contenu dans un fichier local, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="01d34-117">To save content to a local file, do the following:</span></span>

1.  <span data-ttu-id="01d34-118">Appelez [**IWMReader :: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) avec l’URL.</span><span class="sxs-lookup"><span data-stu-id="01d34-118">Call [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) with the URL.</span></span> <span data-ttu-id="01d34-119">**Open** est un appel asynchrone et est retourné immédiatement.</span><span class="sxs-lookup"><span data-stu-id="01d34-119">**Open** is an asynchronous call, and returns immediately.</span></span> <span data-ttu-id="01d34-120">Attendez que l’opération se termine, comme décrit dans [pour créer un lecteur et ouvrir un fichier](to-create-a-reader-and-open-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="01d34-120">Wait for the operation to complete, as described in [To Create a Reader and Open a File](to-create-a-reader-and-open-a-file.md).</span></span>
2.  <span data-ttu-id="01d34-121">Interrogez l’objet lecteur de l’interface [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) .</span><span class="sxs-lookup"><span data-stu-id="01d34-121">Query the reader object for the [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) interface.</span></span>
3.  <span data-ttu-id="01d34-122">Vérifiez si le contenu peut être enregistré en appelant la méthode [**IWMReaderAdvanced4 :: CanSaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cansavefileas) .</span><span class="sxs-lookup"><span data-stu-id="01d34-122">Check whether the content can be saved by calling the [**IWMReaderAdvanced4::CanSaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cansavefileas) method.</span></span> <span data-ttu-id="01d34-123">Si la méthode retourne la valeur false, le contenu ne peut pas être enregistré localement.</span><span class="sxs-lookup"><span data-stu-id="01d34-123">If the method returns False, the content cannot be saved locally.</span></span> <span data-ttu-id="01d34-124">Dans le cas contraire, passez à l’étape 4.</span><span class="sxs-lookup"><span data-stu-id="01d34-124">Otherwise, proceed to step 4.</span></span>
4.  <span data-ttu-id="01d34-125">Appelez la méthode [**IWMReaderAdvanced4 :: IsUsingFastCache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-isusingfastcache) pour déterminer si le serveur utilise la diffusion en continu du cache rapide.</span><span class="sxs-lookup"><span data-stu-id="01d34-125">Call the [**IWMReaderAdvanced4::IsUsingFastCache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-isusingfastcache) method to determine whether the server is using Fast Cache streaming.</span></span>
5.  <span data-ttu-id="01d34-126">Appelez [**IWMReaderAdvanced2 :: SaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) avec un nom de fichier pour le fichier local.</span><span class="sxs-lookup"><span data-stu-id="01d34-126">Call the [**IWMReaderAdvanced2::SaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) with a file name for the local file.</span></span> <span data-ttu-id="01d34-127">Si la méthode **IsUsingFastCache** a retourné la valeur true, donnez au fichier un nom d’extension. asx.</span><span class="sxs-lookup"><span data-stu-id="01d34-127">If the **IsUsingFastCache** method returned True, give the file name an .asx extension.</span></span> <span data-ttu-id="01d34-128">Sinon, donnez au nom de fichier une extension. ASF,. WMA ou. wmv.</span><span class="sxs-lookup"><span data-stu-id="01d34-128">Otherwise, give the file name an .asf, .wma, or .wmv extension.</span></span>

<span data-ttu-id="01d34-129">L’application peut annuler l’opération d’enregistrement pendant qu’elle est en cours, en appelant la méthode [**IWMReaderAdvanced4 :: CancelSaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cancelsavefileas) .</span><span class="sxs-lookup"><span data-stu-id="01d34-129">The application can cancel the save operation while it is in progress, by calling the [**IWMReaderAdvanced4::CancelSaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cancelsavefileas) method.</span></span>

<span data-ttu-id="01d34-130">Le contenu enregistré peut être protégé par DRM, donc il n’est pas possible de lire le fichier sur un autre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="01d34-130">The saved content might be protected with DRM, so it may not be possible to play the file on another computer.</span></span> <span data-ttu-id="01d34-131">Pour plus d’informations sur la protection du contenu, consultez [fonctionnalités de Rights Management numérique](digital-rights-management-features.md).</span><span class="sxs-lookup"><span data-stu-id="01d34-131">For more information on content protection, see [Digital Rights Management Features](digital-rights-management-features.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="01d34-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="01d34-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01d34-133">**Interface IWMReader**</span><span class="sxs-lookup"><span data-stu-id="01d34-133">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="01d34-134">**Interface IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="01d34-134">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> </dl>

 

 




