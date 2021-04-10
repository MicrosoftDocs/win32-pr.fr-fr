---
title: Obtention d’informations de profil lors de la lecture
description: Obtention d’informations de profil lors de la lecture
ms.assetid: 4ea6c063-fd53-4b5e-ac01-9e2790322ace
keywords:
- Windows Media Format SDK, profils
- ASF (Advanced Systems Format), profils
- ASF (format des systèmes avancés), profils
- ASF (Advanced Systems Format), exclusion mutuelle
- ASF (format des systèmes avancés), exclusion mutuelle
- ASF (Advanced Systems Format), partage de bande passante
- ASF (format de systèmes avancés), partage de bande passante
- flux, obtention des informations de profil lors de la lecture
- profils, obtention d’informations lors de la lecture
- exclusion mutuelle, obtention des informations de profil lors de la lecture
- partage de bande passante, obtention des informations de profil lors de la lecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a5c7083f7bf9e986e8a23ba2c78dfe4404942a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104101277"
---
# <a name="getting-profile-information-at-playback"></a><span data-ttu-id="a7f0e-114">Obtention d’informations de profil lors de la lecture</span><span class="sxs-lookup"><span data-stu-id="a7f0e-114">Getting Profile Information at Playback</span></span>

<span data-ttu-id="a7f0e-115">Les informations du profil utilisé pour créer un fichier sont stockées dans la section d’en-tête du fichier.</span><span class="sxs-lookup"><span data-stu-id="a7f0e-115">Information from the profile used to create a file is stored in the header section of the file.</span></span> <span data-ttu-id="a7f0e-116">Les deux objets Reader peuvent accéder aux informations de profil à partir de l’en-tête de fichier.</span><span class="sxs-lookup"><span data-stu-id="a7f0e-116">Both reader objects can access the profile information from the file header.</span></span> <span data-ttu-id="a7f0e-117">Il existe plusieurs raisons pour lesquelles vous pouvez souhaiter accéder aux données de profil à partir du lecteur.</span><span class="sxs-lookup"><span data-stu-id="a7f0e-117">There are several reasons why you might want to access profile data from the reader.</span></span> <span data-ttu-id="a7f0e-118">En règle générale, vous devez récupérer des informations sur les flux, les objets d’exclusion mutuelle et les objets de partage de bande passante.</span><span class="sxs-lookup"><span data-stu-id="a7f0e-118">Most commonly, you will need to retrieve information about streams, mutual exclusion objects, and bandwidth sharing objects.</span></span>

<span data-ttu-id="a7f0e-119">L’objet lecteur asynchrone et l’objet lecteur synchrone peuvent être interrogés pour l’interface [**IWMProfile**](iwmprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="a7f0e-119">Both the asynchronous reader object and the synchronous reader object can be queried for the [**IWMProfile**](iwmprofile.md) interface.</span></span> <span data-ttu-id="a7f0e-120">Aucune modification apportée aux informations de profil ne peut avoir d’incidence sur le fichier dans le lecteur.</span><span class="sxs-lookup"><span data-stu-id="a7f0e-120">No changes made to the profile information can have any affect on the file in the reader.</span></span> <span data-ttu-id="a7f0e-121">Pour plus d’informations sur l’accès aux informations de profil, consultez [utilisation des profils](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="a7f0e-121">For more information about accessing profile information, see [Working with Profiles](working-with-profiles.md).</span></span>

## <a name="stream-information"></a><span data-ttu-id="a7f0e-122">Informations de flux</span><span class="sxs-lookup"><span data-stu-id="a7f0e-122">Stream Information</span></span>

<span data-ttu-id="a7f0e-123">Il est parfois important de savoir comment un flux est configuré.</span><span class="sxs-lookup"><span data-stu-id="a7f0e-123">It is sometimes important to know how a stream is configured.</span></span> <span data-ttu-id="a7f0e-124">Lorsque vous récupérez des propriétés de média à partir de l’un des objets Reader, vous recevez les propriétés des sorties.</span><span class="sxs-lookup"><span data-stu-id="a7f0e-124">When you retrieve media properties from the either of the reader objects, you get the properties of the outputs.</span></span> <span data-ttu-id="a7f0e-125">Les propriétés de sortie décrivent comment les données non compressées d’un flux vont être remises par le lecteur, et non la manière dont le flux est configuré dans le fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="a7f0e-125">Output properties describe how the uncompressed data from a stream is going to be delivered by the reader, not how the stream is configured within the ASF file.</span></span>

<span data-ttu-id="a7f0e-126">Lors de la réception d’exemples de flux non compressés à partir de l’un des objets Reader, vous devez utiliser les informations de profil pour identifier le format des données compressées.</span><span class="sxs-lookup"><span data-stu-id="a7f0e-126">When receiving uncompressed stream samples from either reader object, you must use the profile information to identify the format of the compressed data.</span></span> <span data-ttu-id="a7f0e-127">Cela est particulièrement important si vous envisagez d’écrire le flux compressé dans un autre fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="a7f0e-127">This is particularly important if you are going to write the compressed stream to another ASF file.</span></span>

<span data-ttu-id="a7f0e-128">Vous devez également accéder aux informations de flux lors de l’utilisation de la recompression intelligente pour transcoder un flux audio vers une vitesse de transmission inférieure.</span><span class="sxs-lookup"><span data-stu-id="a7f0e-128">You also need to access stream information when using smart recompression to transcode an audio stream to a lower bit rate.</span></span>

<span data-ttu-id="a7f0e-129">Vous pouvez déterminer si un flux a été écrit à l’aide de l’encodage VBR (variable binaire rate).</span><span class="sxs-lookup"><span data-stu-id="a7f0e-129">You may want to determine whether a stream was written using variable bit rate (VBR) encoding.</span></span> <span data-ttu-id="a7f0e-130">Vous ne pouvez pas accéder à des informations VBR à partir de l’interface **IWMProfile** de l’un des objets Reader.</span><span class="sxs-lookup"><span data-stu-id="a7f0e-130">You cannot access any VBR information from the **IWMProfile** interface of either reader object.</span></span> <span data-ttu-id="a7f0e-131">Cela est dû au fait que les informations VBR ne sont pas stockées dans le fichier après l’encodage.</span><span class="sxs-lookup"><span data-stu-id="a7f0e-131">This is because the VBR information is not stored in the file after encoding.</span></span> <span data-ttu-id="a7f0e-132">Vous pouvez déterminer si un flux a été créé à l’aide de l’encodage VBR en obtenant un pointeur vers l’interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) de l’objet lecteur et en appelant [**IWMHeaderInfo :: GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).</span><span class="sxs-lookup"><span data-stu-id="a7f0e-132">You can determine whether a stream was created using VBR encoding by obtaining a pointer to the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface of the reader object and calling [**IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).</span></span> <span data-ttu-id="a7f0e-133">Vous devez spécifier le numéro de flux et passer g \_ wszIsVBR comme nom d’attribut.</span><span class="sxs-lookup"><span data-stu-id="a7f0e-133">You must specify the stream number and pass g\_wszIsVBR as the attribute name.</span></span>

## <a name="mutual-exclusion-information"></a><span data-ttu-id="a7f0e-134">Informations d’exclusion mutuelle</span><span class="sxs-lookup"><span data-stu-id="a7f0e-134">Mutual Exclusion Information</span></span>

<span data-ttu-id="a7f0e-135">Si vous souhaitez créer une application de lecture qui utilise l’exclusion mutuelle, vous devez accéder aux informations sur les objets d’exclusion mutuelle inclus dans le profil.</span><span class="sxs-lookup"><span data-stu-id="a7f0e-135">If you want to create a reading application that uses mutual exclusion, you will want to access the information about any mutual exclusion objects included in the profile.</span></span> <span data-ttu-id="a7f0e-136">Pour tous les types d’exclusion mutuelle, à l’exception de la vitesse de transmission, l’application de lecture est responsable des basculements de flux requis.</span><span class="sxs-lookup"><span data-stu-id="a7f0e-136">For all mutual exclusion types except bit rate, the reading application is responsible for any stream switching that is required.</span></span> <span data-ttu-id="a7f0e-137">Pour basculer entre les flux, vous devez connaître les flux.</span><span class="sxs-lookup"><span data-stu-id="a7f0e-137">To switch streams, you need to know which streams are which.</span></span>

## <a name="bandwidth-sharing-information"></a><span data-ttu-id="a7f0e-138">Informations sur le partage de bande passante</span><span class="sxs-lookup"><span data-stu-id="a7f0e-138">Bandwidth Sharing Information</span></span>

<span data-ttu-id="a7f0e-139">Les objets de partage de bande passante inclus dans un profil sont inclus uniquement à titre d’information.</span><span class="sxs-lookup"><span data-stu-id="a7f0e-139">Bandwidth sharing objects that are included in a profile are included only for informational purposes.</span></span> <span data-ttu-id="a7f0e-140">Ni l’objet Writer ni l’un des deux objets Reader ne prennent d’action en raison des données de partage de bande passante.</span><span class="sxs-lookup"><span data-stu-id="a7f0e-140">Neither the writer object nor either of the reader objects takes any action as a result of bandwidth sharing data.</span></span> <span data-ttu-id="a7f0e-141">Si vous souhaitez utiliser le partage de bande passante dans votre application de lecture, vous devez accéder aux informations de partage de bande passante à partir des données de profil.</span><span class="sxs-lookup"><span data-stu-id="a7f0e-141">If you want to use bandwidth sharing in your reading application, you must access the bandwidth sharing information from the profile data.</span></span>

> [!Note]  
> <span data-ttu-id="a7f0e-142">Les informations du profil utilisé pour créer un fichier ne sont pas toutes présentes dans l’en-tête de fichier.</span><span class="sxs-lookup"><span data-stu-id="a7f0e-142">Not all of the information from the profile used to create a file is present in the file header.</span></span> <span data-ttu-id="a7f0e-143">En règle générale, les données qui sont utilisées uniquement au moment de l’encodage ne sont pas conservées dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="a7f0e-143">As a general rule, data that is used only at the time of encoding is not persisted in the file.</span></span> <span data-ttu-id="a7f0e-144">Cela comprend les paramètres d’entrée qui ont été définis à l’aide de la méthode [**IWMWriterAdvanced2 :: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) , ainsi que les propriétés définies à l’aide de la méthode [**IWMPropertyVault :: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) .</span><span class="sxs-lookup"><span data-stu-id="a7f0e-144">This includes input settings that were set using the [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) method, as well as properties set using the [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) method.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a7f0e-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a7f0e-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7f0e-146">**Interface IWMProfile**</span><span class="sxs-lookup"><span data-stu-id="a7f0e-146">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="a7f0e-147">**Lecture des fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="a7f0e-147">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> </dl>

 

 




