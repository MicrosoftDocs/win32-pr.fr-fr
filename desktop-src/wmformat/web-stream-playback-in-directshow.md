---
title: Lecture de flux Web dans DirectShow
description: Lecture de flux Web dans DirectShow
ms.assetid: cc307c24-2bd2-43de-ba81-1cf5b05524b2
keywords:
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, lecture de flux Web
- ASF (Advanced Systems Format), DirectShow
- ASF (format avancé des systèmes), DirectShow
- ASF (Advanced Systems Format), lecture de flux Web
- ASF (format de systèmes avancés), lecture de flux Web
- DirectShow, lecture de flux Web
- Flux Web, DirectShow
- Flux Web, lecture dans DirectShow
- flux, lecture de flux Web dans DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a696e8184554195cf6e9c841b2fb59c4281e377a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939785"
---
# <a name="web-stream-playback-in-directshow"></a><span data-ttu-id="97e95-113">Lecture de flux Web dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="97e95-113">Web Stream Playback in DirectShow</span></span>

<span data-ttu-id="97e95-114">Microsoft DirectShow prend en charge les flux Web (pour plus d’informations, consultez [flux Web](web-streams.md) ) dans les scénarios de lecture de fichiers via le filtre de [lecteur ASF WM](wm-asf-reader-filter.md) , mais vous devez écrire votre propre filtre DirectShow pour capturer et conserver le flux.</span><span class="sxs-lookup"><span data-stu-id="97e95-114">Microsoft DirectShow supports Web streams (see [Web Streams](web-streams.md) for more information) in file playback scenarios through the [WM ASF Reader](wm-asf-reader-filter.md) filter, but you must write your own DirectShow filter to capture and persist the stream.</span></span>

> [!Note]  
> <span data-ttu-id="97e95-115">Pour lire des flux Web dans du contenu diffusé en continu à partir d’un serveur exécutant Windows Media Services, utilisez le contrôle® ActiveX de Windows Media Player 9 Series dans une page Web.</span><span class="sxs-lookup"><span data-stu-id="97e95-115">To play back Web streams in content that is being streamed from a server running Windows Media Services, use the Windows Media Player 9 Series ActiveX® control embedded in a Web page.</span></span>

 

<span data-ttu-id="97e95-116">Lorsqu’un fichier contenant des flux de type WMMEDIATYPE \_ filetransfer est donné, le lecteur ASF WM crée une broche de sortie pour celui-ci.</span><span class="sxs-lookup"><span data-stu-id="97e95-116">When given a file containing streams of type WMMEDIATYPE\_FileTransfer, the WM ASF Reader will create an output pin for it.</span></span> <span data-ttu-id="97e95-117">Le bloc de format sera une structure de [**\_ \_ format webstream WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) .</span><span class="sxs-lookup"><span data-stu-id="97e95-117">The format block will be a [**WMT\_WEBSTREAM\_FORMAT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) structure.</span></span> <span data-ttu-id="97e95-118">Si aucun filtre en aval ne peut gérer ce type de média, le code confidentiel restera non connecté, mais le fichier continuera de lire les flux audio et/ou vidéo.</span><span class="sxs-lookup"><span data-stu-id="97e95-118">If no downstream filter is available that can handle that media type, then the pin will remain unconnected, but the file will still play the audio and/or video streams.</span></span>

<span data-ttu-id="97e95-119">Il est important de comprendre que chaque échantillon de média dans un flux Web contient une structure d' [**\_ \_ \_ en-tête d’exemple de flux d’en-tête WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header) , qui a une longueur variable en fonction de la longueur de son membre **wszURL** .</span><span class="sxs-lookup"><span data-stu-id="97e95-119">It is important to understand that each media sample in a Web stream contains a [**WMT\_WEBSTREAM\_SAMPLE\_HEADER**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header) structure, which has a variable length depending on the length of its **wszURL** member.</span></span> <span data-ttu-id="97e95-120">Le pointeur vers les exemples de données pointe initialement vers cette structure, et vous devez avancer le pointeur au-delà de la structure afin d’accéder aux données réelles dans le flux.</span><span class="sxs-lookup"><span data-stu-id="97e95-120">The pointer to the sample data initially points to this structure, and you must advance the pointer past the structure in order to access the actual data in the stream.</span></span> <span data-ttu-id="97e95-121">Le filtre de votre gestionnaire de flux Web doit être basé sur la classe **CBaseRenderer** .</span><span class="sxs-lookup"><span data-stu-id="97e95-121">Your Web stream handler filter should be based on the **CBaseRenderer** class.</span></span> <span data-ttu-id="97e95-122">Dans la méthode **DoRenderSample** , le filtre doit analyser la structure pour obtenir des informations sur le flux Web, puis exécuter l’action appropriée.</span><span class="sxs-lookup"><span data-stu-id="97e95-122">In the **DoRenderSample** method, the filter will need to parse the structure for information about the Web stream, and then perform the appropriate action.</span></span> <span data-ttu-id="97e95-123">En général, cela implique l’enregistrement du fichier sur le disque, puis l’appel de **CommitUrlCacheEntry** et **CreateUrlCacheEntry** pour placer les fichiers dans le cache Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="97e95-123">Typically, this will involve saving the file to disk, and then calling **CommitUrlCacheEntry** and **CreateUrlCacheEntry** to place the files into the Internet Explorer cache.</span></span> <span data-ttu-id="97e95-124">Le filtre doit gérer des fichiers à parties multiples, autrement dit, des fichiers qui sont plus grands qu’un exemple, et doivent également gérer les commandes de rendu, qui sont spécifiées par le membre d' **\_ \_ en-tête de l’exemple d' \_ en-tête webstream WMT.**</span><span class="sxs-lookup"><span data-stu-id="97e95-124">The filter must handle multipart files, that is, files that are larger than one sample, and also must handle render commands, which are specified by the **WMT\_WEBSTREAM\_SAMPLE\_HEADER.wSampleType** member.</span></span> <span data-ttu-id="97e95-125">Le filtre envoie un **\_ \_ événement OLE EC** à l’application, ainsi que le texte de l' **exemple d' \_ \_ \_ en-tête d’exemple webstream WMT. wszURL** qui contient le nom du fichier à restituer.</span><span class="sxs-lookup"><span data-stu-id="97e95-125">The filter sends an **EC\_OLE\_EVENT** to the application, along with the text of the **WMT\_WEBSTREAM\_SAMPLE\_HEADER.wszURL** string which contains the name of the file to be rendered.</span></span> <span data-ttu-id="97e95-126">L’application fait ensuite en sorte que le navigateur affiche la page spécifiée.</span><span class="sxs-lookup"><span data-stu-id="97e95-126">The application then causes the browser to display the specified page.</span></span> <span data-ttu-id="97e95-127">Si le flux Web a été créé correctement, le fichier doit déjà être dans le cache.</span><span class="sxs-lookup"><span data-stu-id="97e95-127">If the Web stream has been authored correctly, the file should already be in the cache.</span></span>

<span data-ttu-id="97e95-128">Pour plus d’informations sur les événements **CBaseRenderer**, **DoRenderSample** et **EC \_ OLE \_**, consultez la documentation du kit de développement logiciel (SDK) DirectShow.</span><span class="sxs-lookup"><span data-stu-id="97e95-128">For more information on **CBaseRenderer**, **DoRenderSample**, and **EC\_OLE\_EVENT**, see the DirectShow SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97e95-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="97e95-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97e95-130">**Flux Web**</span><span class="sxs-lookup"><span data-stu-id="97e95-130">**Web Streams**</span></span>](web-streams.md)
</dt> </dl>

 

 




