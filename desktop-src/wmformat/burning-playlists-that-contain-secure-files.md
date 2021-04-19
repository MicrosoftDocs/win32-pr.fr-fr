---
title: Gravure de playlists contenant des fichiers sécurisés
description: Gravure de playlists contenant des fichiers sécurisés
ms.assetid: 0d9415a1-a154-4fe4-af4c-cce4cb05ade5
keywords:
- Windows Media Format SDK, gravure de playlists avec des fichiers sécurisés
- Windows Media Format SDK, playlists avec des fichiers sécurisés
- ASF (Advanced Systems Format), gravure de playlists avec des fichiers sécurisés
- ASF (format de systèmes avancés), gravage de sélections avec des fichiers sécurisés
- ASF (Advanced Systems Format), sélections avec des fichiers sécurisés
- ASF (format de systèmes avancés), playlists avec des fichiers sécurisés
- gestion des droits numériques (DRM), gravure de playlists avec des fichiers sécurisés
- DRM (Digital Rights Management), gravure de playlists avec des fichiers sécurisés
- gestion des droits numériques (DRM), listes de diffusion avec fichiers sécurisés
- DRM (gestion des droits numériques), sélections avec des fichiers sécurisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214c1dbd4ee08f90b3e5e8aa6186508af5044f29
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/21/2020
ms.locfileid: "106511275"
---
# <a name="burning-playlists-that-contain-secure-files"></a><span data-ttu-id="696da-113">Gravure de playlists contenant des fichiers sécurisés</span><span class="sxs-lookup"><span data-stu-id="696da-113">Burning Playlists That Contain Secure Files</span></span>

<span data-ttu-id="696da-114">Les licences créées à l’aide des objets du kit de développement logiciel (SDK) Windows Media Rights Manager 10 peuvent spécifier le droit de copier un fichier vers un CD-ROM dans le cadre d’une sélection.</span><span class="sxs-lookup"><span data-stu-id="696da-114">Licenses created by using the objects of the Windows Media Rights Manager 10 SDK can specify the right to copy a file to compact disc as part of a playlist.</span></span> <span data-ttu-id="696da-115">Cette fonctionnalité, appelée « gravure de playlist », requiert que vous vérifiiez les licences de tous les fichiers de la sélection avant de commencer à copier les données.</span><span class="sxs-lookup"><span data-stu-id="696da-115">This feature, called playlist burning, requires that you verify the licenses of all of the files in the playlist before starting to copy data.</span></span> <span data-ttu-id="696da-116">Le kit de développement logiciel (SDK) Windows Media Format fournit l’interface [**IWMReaderPlaylistBurn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) pour effectuer la vérification des fichiers.</span><span class="sxs-lookup"><span data-stu-id="696da-116">The Windows Media Format SDK provides the [**IWMReaderPlaylistBurn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) interface to perform file verification for you.</span></span>

<span data-ttu-id="696da-117">Pour implémenter la gravure de playlist, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="696da-117">To implement playlist burning, perform the following steps:</span></span>

1.  <span data-ttu-id="696da-118">Créez une instance de l’objet Reader ou de l’objet lecteur synchrone.</span><span class="sxs-lookup"><span data-stu-id="696da-118">Create an instance of the reader object, or the synchronous reader object.</span></span> <span data-ttu-id="696da-119">Pour plus d’informations, consultez [lecture de fichiers ASF](reading-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="696da-119">For more information, see [Reading ASF Files](reading-asf-files.md).</span></span>
2.  <span data-ttu-id="696da-120">Appelez la méthode **QueryInterface** de l’interface du lecteur ([**IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader) ou [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)) pour obtenir un pointeur vers l’interface [**IWMReaderPlaylistBurn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) .</span><span class="sxs-lookup"><span data-stu-id="696da-120">Call the **QueryInterface** method of the reader interface ([**IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader) or [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)) to obtain a pointer to the [**IWMReaderPlaylistBurn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) interface.</span></span>
3.  <span data-ttu-id="696da-121">Copiez les noms de fichiers de la sélection dans un tableau de chaînes de caractères larges.</span><span class="sxs-lookup"><span data-stu-id="696da-121">Copy the file names from the playlist into an array of wide-character strings.</span></span> <span data-ttu-id="696da-122">Les noms de fichiers dans le tableau doivent être dans l’ordre dans lequel ils apparaissent dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="696da-122">The file names in the array must be in the same order as they appear in the playlist.</span></span>
4.  <span data-ttu-id="696da-123">Appelez la méthode [**IWMReaderPlaylistBurn :: InitPlaylistBurn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-initplaylistburn) , en passant un pointeur vers le tableau créé à l’étape 3, pour initialiser la vérification de la licence pour les fichiers.</span><span class="sxs-lookup"><span data-stu-id="696da-123">Call the [**IWMReaderPlaylistBurn::InitPlaylistBurn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-initplaylistburn) method, passing in a pointer to the array created in step 3, to initialize the license verification for the files.</span></span>
5.  <span data-ttu-id="696da-124">Lorsque la vérification de la licence est terminée, l’objet lecteur envoie \_ un \_ message de gravure de sélection d’initialisation WMT \_ à votre implémentation de la méthode de rappel [**IWMStatusCallback :: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) .</span><span class="sxs-lookup"><span data-stu-id="696da-124">When the license verification is completed, the reader object sends a WMT\_INIT\_PLAYLIST\_BURN message to your implementation of the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method.</span></span> <span data-ttu-id="696da-125">Lorsque votre rappel reçoit ce message, appelez la méthode [**IWMReaderPlaylistBurn :: GetInitResults**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-getinitresults) pour obtenir les résultats de la vérification de licence.</span><span class="sxs-lookup"><span data-stu-id="696da-125">When your callback receives this message, call the [**IWMReaderPlaylistBurn::GetInitResults**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-getinitresults) method to get the results of the license check.</span></span> <span data-ttu-id="696da-126">Cette méthode prend un tableau de variables **HRESULT** qui correspondent aux noms de fichiers dans le tableau passé à **InitPlaylistBurn**.</span><span class="sxs-lookup"><span data-stu-id="696da-126">This method takes an array of **HRESULT** variables that correspond to the file names in the array passed to **InitPlaylistBurn**.</span></span> <span data-ttu-id="696da-127">Si toutes les valeurs du tableau de résultats sont égales à S \_ OK, vous pouvez continuer.</span><span class="sxs-lookup"><span data-stu-id="696da-127">If all of the values in the result array are equal to S\_OK, you can continue.</span></span> <span data-ttu-id="696da-128">Si un résultat est un code d’erreur, la sélection ne doit pas être copiée.</span><span class="sxs-lookup"><span data-stu-id="696da-128">If any result is an error code, the playlist must not be copied.</span></span>
6.  <span data-ttu-id="696da-129">À l’aide de la même instance du lecteur, ouvrez et lisez chaque fichier.</span><span class="sxs-lookup"><span data-stu-id="696da-129">Using the same instance of the reader, open and read each file.</span></span> <span data-ttu-id="696da-130">Vous devez ouvrir les fichiers dans l’ordre dans lequel les noms de fichiers apparaissent dans le tableau de noms de fichiers transmis à **InitPlaylistBurn**.</span><span class="sxs-lookup"><span data-stu-id="696da-130">You must open the files in the order in which the file names appeared in the file name array passed to **InitPlaylistBurn**.</span></span>
7.  <span data-ttu-id="696da-131">Une fois que vous avez copié tous les fichiers de la sélection, appelez [**IWMReaderPlaylistBurn :: EndPlaylistBurn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-endplaylistburn) pour terminer le processus de gravure de la sélection et libérer les ressources utilisées par le lecteur.</span><span class="sxs-lookup"><span data-stu-id="696da-131">When you have copied all of the files in the playlist, call the [**IWMReaderPlaylistBurn::EndPlaylistBurn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-endplaylistburn) to complete the playlist burn process and free the resources used by the reader.</span></span>

> [!Note]  
> <span data-ttu-id="696da-132">DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="696da-132">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="696da-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="696da-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="696da-134">**Activation de la prise en charge de DRM**</span><span class="sxs-lookup"><span data-stu-id="696da-134">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




