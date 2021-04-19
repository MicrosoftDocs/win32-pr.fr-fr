---
description: Le récepteur de fichiers ASF est une implémentation de IMFMediaSink fournie par Media Foundation qu’une application peut utiliser pour archiver des données de média ASF dans un fichier. Pour plus d’informations sur le modèle objet des récepteurs de média ASF et l’utilisation générale, consultez récepteurs de média ASF.
ms.assetid: 21cbde27-a2ca-4298-9197-43bcaf05588d
title: Ajout d’informations de flux au récepteur de fichiers ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e08c6997d9c77836f379d4ca7b75720ddea245
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513402"
---
# <a name="adding-stream-information-to-the-asf-file-sink"></a><span data-ttu-id="80ada-104">Ajout d’informations de flux au récepteur de fichiers ASF</span><span class="sxs-lookup"><span data-stu-id="80ada-104">Adding Stream Information to the ASF File Sink</span></span>

<span data-ttu-id="80ada-105">Le récepteur de fichiers ASF est une implémentation de [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) fournie par Media Foundation qu’une application peut utiliser pour archiver des données de média ASF dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="80ada-105">The ASF file sink is an implementation of [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) provided by Media Foundation that an application can use to archive ASF media data to a file.</span></span> <span data-ttu-id="80ada-106">Pour plus d’informations sur le modèle objet et l’utilisation générale des récepteurs de média ASF, consultez [récepteurs de média ASF](asf-media-sinks.md).</span><span class="sxs-lookup"><span data-stu-id="80ada-106">For information about ASF Media Sinks' object model and general usage, see [ASF Media Sinks](asf-media-sinks.md).</span></span>

<span data-ttu-id="80ada-107">Après avoir instancié le récepteur de fichiers, vous devez le configurer avant de générer la topologie.</span><span class="sxs-lookup"><span data-stu-id="80ada-107">After instantiating the file sink, it must be configured before building the topology.</span></span> <span data-ttu-id="80ada-108">Le récepteur de fichiers doit connaître les flux de données dans le fichier de sortie, les informations sur le mode d’encodage et les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="80ada-108">The file sink needs to know about the streams in the output file, the encoding mode information, and the metadata.</span></span> <span data-ttu-id="80ada-109">Cette rubrique décrit le processus d’ajout de flux dans le récepteur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="80ada-109">This topic describes the process of adding stream in the file sink.</span></span>

-   [<span data-ttu-id="80ada-110">Ajout de flux dans le récepteur de fichiers ASF</span><span class="sxs-lookup"><span data-stu-id="80ada-110">Adding Streams in the ASF File Sink</span></span>](#adding-streams-in-the-asf-file-sink)
-   [<span data-ttu-id="80ada-111">Énumération des récepteurs de flux</span><span class="sxs-lookup"><span data-stu-id="80ada-111">Enumerating Stream Sinks</span></span>](#enumerating-stream-sinks)
-   [<span data-ttu-id="80ada-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="80ada-112">Related topics</span></span>](#related-topics)

## <a name="adding-streams-in-the-asf-file-sink"></a><span data-ttu-id="80ada-113">Ajout de flux dans le récepteur de fichiers ASF</span><span class="sxs-lookup"><span data-stu-id="80ada-113">Adding Streams in the ASF File Sink</span></span>

<span data-ttu-id="80ada-114">Le récepteur de fichiers doit connaître les flux de sortie et leurs propriétés afin de pouvoir générer des exemples de sortie en conséquence et les ajouter au fichier ASF de sortie.</span><span class="sxs-lookup"><span data-stu-id="80ada-114">The file sink must know of the output streams and their properties so that it can generate output samples accordingly and add them to the output ASF file.</span></span> <span data-ttu-id="80ada-115">Ces paramètres sont écrits dans l’objet d’en-tête ASF final.</span><span class="sxs-lookup"><span data-stu-id="80ada-115">These settings are written to the final ASF Header Object.</span></span>

<span data-ttu-id="80ada-116">Pour définir des informations de flux, vous devez avoir une référence à l’objet ASF ContentInfo du récepteur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="80ada-116">To set stream information, you must have a reference to the file sink's ASF ContentInfo object.</span></span> <span data-ttu-id="80ada-117">Pour plus d’informations, consultez [création du récepteur de fichiers ASF](creating-the-asf-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="80ada-117">For information, see [Creating the ASF File Sink](creating-the-asf-file-sink.md).</span></span>

<span data-ttu-id="80ada-118">La procédure suivante résume les étapes générales de la configuration de Stream à l’aide de l’objet de profil ASF.</span><span class="sxs-lookup"><span data-stu-id="80ada-118">The following procedure summarizes the general steps for configuring stream by using the ASF profile object.</span></span>

<span data-ttu-id="80ada-119">**Pour configurer les informations de flux dans le récepteur de fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="80ada-119">**To configure stream information in the ASF file sink**</span></span>

1.  <span data-ttu-id="80ada-120">Créez un objet de profil ASF en appelant [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile).</span><span class="sxs-lookup"><span data-stu-id="80ada-120">Create an ASF profile object by calling [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile).</span></span>
2.  <span data-ttu-id="80ada-121">Pour chaque flux du fichier de sortie, créez un type de média pour le flux cible à ajouter dans le récepteur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="80ada-121">For each stream in the output file, create a media type for the target stream to be added in the file sink.</span></span> <span data-ttu-id="80ada-122">Le type de média doit être compatible avec les types de sortie pris en charge par les encodeurs Windows Media.</span><span class="sxs-lookup"><span data-stu-id="80ada-122">The media type must be compatible with the output types supported by the Windows Media encoders.</span></span>

    <span data-ttu-id="80ada-123">Pour plus d’informations sur l’ajout de flux audio au profil, consultez Création de flux audio pour l’encodage ASF.</span><span class="sxs-lookup"><span data-stu-id="80ada-123">For information about adding audio streams to the profile, see Creating Audio Streams for ASF Encoding.</span></span>

    <span data-ttu-id="80ada-124">Pour plus d’informations sur l’ajout de flux vidéo au profil, consultez Création de flux vidéo pour l’encodage ASF.</span><span class="sxs-lookup"><span data-stu-id="80ada-124">For information about adding video streams to the profile, see Creating Video Streams for ASF Encoding.</span></span>

3.  <span data-ttu-id="80ada-125">Créez des flux basés sur les types de médias créés à l’étape 2 en appelant [**IMFASFProfile :: CreateStream,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream).</span><span class="sxs-lookup"><span data-stu-id="80ada-125">Create streams based on the media types created in step 2 by calling [**IMFASFProfile::CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream).</span></span>
4.  <span data-ttu-id="80ada-126">Assignez un numéro de flux pour le flux nouvellement créé en appelant le pointeur d’interface [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) reçu à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="80ada-126">Assign a stream number for the newly created stream by calling [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface pointer received in step 3.</span></span>
5.  <span data-ttu-id="80ada-127">Éventuellement, configurez le flux avec les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="80ada-127">Optionally configure the stream with the following information:</span></span>
    -   <span data-ttu-id="80ada-128">Paramètres de compartiment avec fuite en définissant les attributs : [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) ou [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="80ada-128">Leaky bucket parameters by setting the attributes: [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) or [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)</span></span>
    -   <span data-ttu-id="80ada-129">Extension de charge utile, exclusion mutuelle en appelant des méthodes [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .</span><span class="sxs-lookup"><span data-stu-id="80ada-129">Payload extension, mutual exclusion by calling [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) methods.</span></span>
6.  <span data-ttu-id="80ada-130">Vous pouvez également définir la taille des paquets de données pour le profil en définissant les attributs [**MF \_ ASFPROFILE \_ MINPACKETSIZE**](mf-asfprofile-minpacketsize-attribute.md) et [**MF \_ ASFPROFILE \_ MaxPacketSize**](mf-asfprofile-maxpacketsize-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="80ada-130">Optionally set data packet size for the profile by setting [**MF\_ASFPROFILE\_MINPACKETSIZE**](mf-asfprofile-minpacketsize-attribute.md) and [**MF\_ASFPROFILE\_MAXPACKETSIZE**](mf-asfprofile-maxpacketsize-attribute.md) attributes.</span></span> <span data-ttu-id="80ada-131">Le profil ASF expose l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) , à laquelle une application peut se procurer une référence en appelant **IMFASFProfile :: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="80ada-131">The ASF profile exposes the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface, which an application can get reference to by calling **IMFASFProfile::QueryInterface**.</span></span>
7.  <span data-ttu-id="80ada-132">Définissez les informations d’encodage du flux dans le récepteur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="80ada-132">Set encoding information for the stream in the file sink.</span></span> <span data-ttu-id="80ada-133">Décrit dans [définition des propriétés dans le récepteur de fichiers](setting-properties-in-the-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="80ada-133">Discussed in [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span>
8.  <span data-ttu-id="80ada-134">Ajoutez le flux au profil en appelant [**IMFASFProfile :: SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream).</span><span class="sxs-lookup"><span data-stu-id="80ada-134">Add the stream to the profile by calling [**IMFASFProfile::SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream).</span></span>
9.  <span data-ttu-id="80ada-135">Associez le profil à l’objet ContentInfo en appelant [**IMFASFContentInfo :: SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile).</span><span class="sxs-lookup"><span data-stu-id="80ada-135">Associate the profile with the ContentInfo object by calling [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile).</span></span>

<span data-ttu-id="80ada-136">Pour modifier un flux existant, l’application peut obtenir une référence à l’interface [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) du flux et la reconfigurer conformément aux exigences.</span><span class="sxs-lookup"><span data-stu-id="80ada-136">To modify an existing stream, the application can get a reference to the stream's [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface and reconfigure it according to the requirements.</span></span> <span data-ttu-id="80ada-137">Pour ajouter ou supprimer des flux, l’application doit appeler [**IMFASFProfile :: RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream).</span><span class="sxs-lookup"><span data-stu-id="80ada-137">To add or remove streams, the application must call [**IMFASFProfile::RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream).</span></span> <span data-ttu-id="80ada-138">Pour appliquer ces modifications, modifier ou supprimer le flux, vous devez redéfinir le profil dans l’objet ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="80ada-138">To apply these changes, stream modifications or removal, you must set the profile again in the ContentInfo object.</span></span> <span data-ttu-id="80ada-139">Cela remplace le profil existant qui est déjà associé à l’objet ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="80ada-139">This overwrites the existing profile that is already associated with the ContentInfo object.</span></span>


```C++
//-------------------------------------------------------------------
//  CreateVideoStream
//  Create an video stream and add it to the profile.
//
//  pProfile: A pointer to the ASF profile.
//  wStreamNumber: Stream number to assign for the new stream.
//    pType: A pointer to the source's video media type.
//-------------------------------------------------------------------

HRESULT CreateVideoStream(IMFASFProfile* pProfile, WORD wStreamNumber, IMFMediaType* pType)
{
    if (!pProfile)
    {
        return E_INVALIDARG;
    }
    if (wStreamNumber < 1 || wStreamNumber > 127 )
    {
        return MF_E_INVALIDSTREAMNUMBER;
    }

    HRESULT hr = S_OK;

    
    IMFMediaType* pVideoType = NULL;
    IMFASFStreamConfig* pVideoStream = NULL;

    UINT32 dwBitRate = 0;
        
    //Create a new video type from the source type
    hr = CreateCompressedVideoType(pType, &pVideoType);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create a new stream with the video type
    hr = pProfile->CreateStream(pVideoType, &pVideoStream);
    if (FAILED(hr))
    {
        goto done;
    }
    

    //Set a valid stream number
    hr = pVideoStream->SetStreamNumber(wStreamNumber);
    if (FAILED(hr))
    {
        goto done;
    }

    //Add the stream to the profile
    hr = pProfile->SetStream(pVideoStream);
    if (FAILED(hr))
    {
        goto done;
    }

    wprintf_s(L"Video Stream created. Stream Number: %d .\n", wStreamNumber);

done:

    SafeRelease(&pVideoStream);
    SafeRelease(&pVideoType);

    return hr;
}
```



## <a name="enumerating-stream-sinks"></a><span data-ttu-id="80ada-140">Énumération des récepteurs de flux</span><span class="sxs-lookup"><span data-stu-id="80ada-140">Enumerating Stream Sinks</span></span>

<span data-ttu-id="80ada-141">Pour chaque flux du profil dont l’objet ContentInfo est conscient, le récepteur de fichiers ASF crée et ajoute un récepteur de flux qui contient toutes les propriétés du flux encodé.</span><span class="sxs-lookup"><span data-stu-id="80ada-141">For each stream in the profile that the ContentInfo object is aware of, the ASF file sink creates and adds a stream sink that contains all the properties of the encoded stream.</span></span> <span data-ttu-id="80ada-142">Le récepteur de fichiers ASF est conçu pour contenir des flux fixes.</span><span class="sxs-lookup"><span data-stu-id="80ada-142">The ASF file sink is designed to contain fixed streams.</span></span> <span data-ttu-id="80ada-143">Cela signifie que vous ne pouvez pas ajouter ou supprimer des flux en appelant [**IMFMediaSink :: AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink) ou [**IMFMediaSink :: RemoveStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink).</span><span class="sxs-lookup"><span data-stu-id="80ada-143">This means that you cannot add or remove streams by calling [**IMFMediaSink::AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink) or [**IMFMediaSink::RemoveStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink).</span></span> <span data-ttu-id="80ada-144">Ces appels sur le récepteur de fichiers échouent avec \_ le \_ code d’erreur fixe MF E STREAMSINKS \_ .</span><span class="sxs-lookup"><span data-stu-id="80ada-144">These calls on the file sink fail with the MF\_E\_STREAMSINKS\_FIXED error code.</span></span> <span data-ttu-id="80ada-145">L’ajout ou la suppression de flux dans le profil n’ajoute pas ou ne supprime pas automatiquement les récepteurs de flux dans le récepteur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="80ada-145">Adding or removing streams in the profile does not automatically add or remove the stream sinks in the file sink.</span></span> <span data-ttu-id="80ada-146">Vous devez ignorer l’instance existante du fichier et la recréer avec les nouvelles informations de flux si vos flux du profil ont été modifiés.</span><span class="sxs-lookup"><span data-stu-id="80ada-146">You must discard the existing instance of the file and recreate it with new stream information if your streams in the profile have changed.</span></span>

<span data-ttu-id="80ada-147">La procédure suivante résume les étapes générales pour l’énumération des récepteurs de flux dans le récepteur de fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="80ada-147">The following procedure summarizes the general steps for enumerating stream sinks in the ASF file sink.</span></span>

<span data-ttu-id="80ada-148">**Pour énumérer des récepteurs de flux**</span><span class="sxs-lookup"><span data-stu-id="80ada-148">**To enumerate stream sinks**</span></span>

1.  <span data-ttu-id="80ada-149">Appelez [**IMFMediaSink :: GetStreamSinkCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkcount) pour connaître le nombre total de récepteurs de flux dans le récepteur de fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="80ada-149">Call [**IMFMediaSink::GetStreamSinkCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkcount) to get the total number of stream sinks in the ASF file sink.</span></span>
2.  <span data-ttu-id="80ada-150">Parcourez les récepteurs de flux ang pour obtenir une référence à l’interface [**GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) du récepteur de flux.</span><span class="sxs-lookup"><span data-stu-id="80ada-150">Loop through the stream sinks ang get a reference to the stream sink's [**GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) interface.</span></span>

    <span data-ttu-id="80ada-151">-ou-</span><span class="sxs-lookup"><span data-stu-id="80ada-151">-or-</span></span>

    <span data-ttu-id="80ada-152">Appelez [**IMFMediaSink :: GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) pour récupérer le récepteur de flux en spécifiant le numéro de flux.</span><span class="sxs-lookup"><span data-stu-id="80ada-152">Call [**IMFMediaSink::GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) to get the stream sink by specifying the stream number.</span></span> <span data-ttu-id="80ada-153">Chaque récepteur de flux est identifié par le numéro de flux que vous définissez lors de la création du flux dans le profil.</span><span class="sxs-lookup"><span data-stu-id="80ada-153">Each stream sink is identified with the stream number you set while creating the stream in the profile.</span></span>

<span data-ttu-id="80ada-154">Si vous générez une topologie partielle pour l’encodage d’un fichier multimédia, vous devez ajouter le récepteur de fichiers à la topologie en tant que nœud de topologie de sortie.</span><span class="sxs-lookup"><span data-stu-id="80ada-154">If you are building a partial topology for encoding a media file, you must add the file sink to the topology as an output topology node.</span></span> <span data-ttu-id="80ada-155">Vous pouvez le faire en spécifiant chaque récepteur de vapeur dans le récepteur de fichiers ou en définissant l’objet d’activation du récepteur de fichiers et les identificateurs du récepteur de flux.</span><span class="sxs-lookup"><span data-stu-id="80ada-155">You can do so either by specifying each steam sink in the file sink or by setting the file sink activation object and the stream sink identifiers.</span></span> <span data-ttu-id="80ada-156">Pour plus d’informations et pour obtenir un exemple de code, consultez [création de nœuds de sortie](creating-output-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="80ada-156">For more information and code example, see [Creating Output Nodes](creating-output-nodes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="80ada-157">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="80ada-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80ada-158">Récepteurs de média ASF</span><span class="sxs-lookup"><span data-stu-id="80ada-158">ASF Media Sinks</span></span>](asf-media-sinks.md)
</dt> <dt>

[<span data-ttu-id="80ada-159">Prise en charge ASF dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="80ada-159">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



