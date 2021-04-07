---
title: À propos de IMediaObject
description: À propos de IMediaObject
ms.assetid: c483f74a-efd8-4a9f-a719-686099755e63
keywords:
- Plug-ins du lecteur Windows Media, interfaces
- plug-ins, interfaces
- plug-ins de traitement de signal numérique, interfaces
- Plug-ins DSP, interfaces
- interfaces, plug-ins DSP
- Plug-ins du lecteur Windows Media, interface IMediaObject
- plug-ins, interface IMediaObject
- plug-ins de traitement de signal numérique, interface IMediaObject
- Plug-ins DSP, interface IMediaObject
- Interface IMediaObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbbecd749242b67bc5c8f36b3c7a2c0a5fbe461
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671565"
---
# <a name="about-imediaobject"></a><span data-ttu-id="edfe1-113">À propos de IMediaObject</span><span class="sxs-lookup"><span data-stu-id="edfe1-113">About IMediaObject</span></span>

<span data-ttu-id="edfe1-114">L’interface **IMediaObject** est l’interface requise pour DMOs.</span><span class="sxs-lookup"><span data-stu-id="edfe1-114">The **IMediaObject** interface is the required interface for DMOs.</span></span> <span data-ttu-id="edfe1-115">**IMediaObject** contient les méthodes qu’un plug-in Windows Media Player utilise pour obtenir des données à partir du lecteur Windows Media, pour traiter les données et pour retourner les données traitées au lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="edfe1-115">**IMediaObject** contains the methods that a Windows Media Player DSP plug-in uses to get data from Windows Media Player, to process the data, and to return the processed data to Windows Media Player.</span></span> <span data-ttu-id="edfe1-116">Pour obtenir la documentation complète de l’interface **IMediaObject** , consultez la section DirectShow de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="edfe1-116">For complete documentation of the **IMediaObject** interface, see the DirectShow section of the Windows SDK.</span></span>

<span data-ttu-id="edfe1-117">Les méthodes de **IMediaObject** peuvent être classées comme suit :</span><span class="sxs-lookup"><span data-stu-id="edfe1-117">The methods of **IMediaObject** can be categorized as follows:</span></span>

## <a name="methods-that-handle-format-negotiation"></a><span data-ttu-id="edfe1-118">Méthodes qui gèrent la négociation de format</span><span class="sxs-lookup"><span data-stu-id="edfe1-118">Methods that Handle Format Negotiation</span></span>

<span data-ttu-id="edfe1-119">Il s’agit des méthodes appelées par le lecteur Windows Media pour obtenir des informations sur les formats de données pris en charge par le plug-in.</span><span class="sxs-lookup"><span data-stu-id="edfe1-119">These are the methods that Windows Media Player calls to get information about the data formats supported by the plug-in.</span></span> <span data-ttu-id="edfe1-120">Ces méthodes incluent les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="edfe1-120">These methods include:</span></span>

-   <span data-ttu-id="edfe1-121">**GetInputMaxLatency**</span><span class="sxs-lookup"><span data-stu-id="edfe1-121">**GetInputMaxLatency**</span></span>
-   <span data-ttu-id="edfe1-122">**GetInputSizeInfo**</span><span class="sxs-lookup"><span data-stu-id="edfe1-122">**GetInputSizeInfo**</span></span>
-   <span data-ttu-id="edfe1-123">**GetInputStreamInfo**</span><span class="sxs-lookup"><span data-stu-id="edfe1-123">**GetInputStreamInfo**</span></span>
-   <span data-ttu-id="edfe1-124">**GetInputType**</span><span class="sxs-lookup"><span data-stu-id="edfe1-124">**GetInputType**</span></span>
-   <span data-ttu-id="edfe1-125">**GetOutputSizeInfo**</span><span class="sxs-lookup"><span data-stu-id="edfe1-125">**GetOutputSizeInfo**</span></span>
-   <span data-ttu-id="edfe1-126">**GetOutputStreamInfo**</span><span class="sxs-lookup"><span data-stu-id="edfe1-126">**GetOutputStreamInfo**</span></span>
-   <span data-ttu-id="edfe1-127">**GetOutputType**</span><span class="sxs-lookup"><span data-stu-id="edfe1-127">**GetOutputType**</span></span>
-   <span data-ttu-id="edfe1-128">**GetStreamCount**</span><span class="sxs-lookup"><span data-stu-id="edfe1-128">**GetStreamCount**</span></span>
-   <span data-ttu-id="edfe1-129">**SetInputMaxLatency**</span><span class="sxs-lookup"><span data-stu-id="edfe1-129">**SetInputMaxLatency**</span></span>
-   <span data-ttu-id="edfe1-130">**SetInputType**</span><span class="sxs-lookup"><span data-stu-id="edfe1-130">**SetInputType**</span></span>
-   <span data-ttu-id="edfe1-131">**SetOutputType**</span><span class="sxs-lookup"><span data-stu-id="edfe1-131">**SetOutputType**</span></span>

<span data-ttu-id="edfe1-132">Plusieurs de ces méthodes, telles que **GetInputType** et **SetInputType**, utilisent la structure de **\_ \_ type de média DMO** pour décrire le format des données utilisées par un flux.</span><span class="sxs-lookup"><span data-stu-id="edfe1-132">Several of these methods, such as **GetInputType** and **SetInputType**, use the **DMO\_MEDIA\_TYPE** structure to describe the format of the data used by a stream.</span></span> <span data-ttu-id="edfe1-133">Lorsque le lecteur Windows Media appelle ces méthodes, il fournit un pointeur vers une structure de **\_ \_ type de média DMO** .</span><span class="sxs-lookup"><span data-stu-id="edfe1-133">When Windows Media Player calls these methods, it provides a pointer to a **DMO\_MEDIA\_TYPE** structure.</span></span> <span data-ttu-id="edfe1-134">Si une méthode telle que **SetInputType** spécifie les informations sur le type de média, le plug-in doit copier la structure de **\_ \_ type de média DMO** sur une variable membre et inspecter ses membres de données pour déterminer le type de données que le lecteur Windows Media fournira dans la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="edfe1-134">If a method such as **SetInputType** specifies the media type information, the plug-in should copy the **DMO\_MEDIA\_TYPE** structure to a member variable and inspect its data members to determine the type of data that Windows Media Player will provide in the input buffer.</span></span> <span data-ttu-id="edfe1-135">Si une méthode telle que **GetInputType** récupère les informations sur le type de média, le plug-in doit copier l’adresse de la variable membre contenant la structure de **\_ \_ type de média DMO** vers le pointeur fourni par le lecteur Windows Media dans la liste de paramètres.</span><span class="sxs-lookup"><span data-stu-id="edfe1-135">If a method such as **GetInputType** retrieves the media type information, the plug-in should copy the address of the member variable containing the **DMO\_MEDIA\_TYPE** structure to the pointer provided by Windows Media Player in the parameter list.</span></span>

<span data-ttu-id="edfe1-136">Le lecteur Windows Media utilise principalement deux membres de la structure de **\_ \_ type de média DMO** :</span><span class="sxs-lookup"><span data-stu-id="edfe1-136">Windows Media Player mainly uses two members of the **DMO\_MEDIA\_TYPE** structure:</span></span>

-   <span data-ttu-id="edfe1-137">**MajorType**: identificateur global unique (Guid) qui spécifie la catégorie globale des médias, tels que l’audio ou la vidéo.</span><span class="sxs-lookup"><span data-stu-id="edfe1-137">**majortype**: A globally unique identifier (GUID) that specifies the overall category of the media, such as audio or video.</span></span>
-   <span data-ttu-id="edfe1-138">**SubType**: GUID qui spécifie une description plus détaillée du média, telle que l’audio PCM.</span><span class="sxs-lookup"><span data-stu-id="edfe1-138">**subtype**: A GUID that specifies a more detailed description of the media, such as PCM audio.</span></span>

<span data-ttu-id="edfe1-139">Ces GUID se trouvent dans l’en-tête nommé UUID. h, qui est inclus avec le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="edfe1-139">These GUIDs can be found in the header named uuids.h, which is included with the Windows SDK.</span></span>

<span data-ttu-id="edfe1-140">Des méthodes telles que **GetInputSizeInfo** fournissent des informations au lecteur Windows Media quant à la quantité de mémoire requise pour allouer les tampons de traitement.</span><span class="sxs-lookup"><span data-stu-id="edfe1-140">Methods such as **GetInputSizeInfo** provide information to Windows Media Player about how much memory is required to allocate the processing buffers.</span></span> <span data-ttu-id="edfe1-141">Les méthodes telles que **GetStreamCount** et **GetOutputStreamInfo** fournissent des informations au lecteur Windows Media sur le nombre et le caractère des flux pris en charge par le plug-in DSP.</span><span class="sxs-lookup"><span data-stu-id="edfe1-141">Methods such as **GetStreamCount** and **GetOutputStreamInfo** provide information to Windows Media Player about the number and character of the streams supported by the DSP plug-in.</span></span>

<span data-ttu-id="edfe1-142">**GetInputMaxLatency** et **SetInputMaxLatency** sont implémentés par DMOs dans des cas spéciaux.</span><span class="sxs-lookup"><span data-stu-id="edfe1-142">**GetInputMaxLatency** and **SetInputMaxLatency** are implemented by DMOs in special cases.</span></span> <span data-ttu-id="edfe1-143">Les plug-ins du lecteur Windows Media DSP doivent retourner E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="edfe1-143">Windows Media Player DSP plug-ins should return E\_NOTIMPL.</span></span>

## <a name="methods-that-specify-or-retrieve-state-information"></a><span data-ttu-id="edfe1-144">Méthodes qui spécifient ou récupèrent les informations d’État</span><span class="sxs-lookup"><span data-stu-id="edfe1-144">Methods that Specify or Retrieve State Information</span></span>

<span data-ttu-id="edfe1-145">Il s’agit des méthodes que le lecteur Windows Media appelle pour récupérer ou définir les valeurs relatives à l’état actuel du plug-in.</span><span class="sxs-lookup"><span data-stu-id="edfe1-145">These are the methods that Windows Media Player calls to get or set values related to the current state of the plug-in.</span></span> <span data-ttu-id="edfe1-146">Ces méthodes incluent les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="edfe1-146">These methods include:</span></span>

-   <span data-ttu-id="edfe1-147">**GetInputCurrentType**</span><span class="sxs-lookup"><span data-stu-id="edfe1-147">**GetInputCurrentType**</span></span>
-   <span data-ttu-id="edfe1-148">**GetInputStatus**</span><span class="sxs-lookup"><span data-stu-id="edfe1-148">**GetInputStatus**</span></span>
-   <span data-ttu-id="edfe1-149">**GetOutputCurrentType**</span><span class="sxs-lookup"><span data-stu-id="edfe1-149">**GetOutputCurrentType**</span></span>

<span data-ttu-id="edfe1-150">**GetInputCurrentType** et **GetOutputCurrentType** utilisent la structure de **\_ \_ type de média DMO** pour retourner au lecteur Windows Media des informations sur les types de médias précédemment définis pour les flux d’entrée et de sortie.</span><span class="sxs-lookup"><span data-stu-id="edfe1-150">**GetInputCurrentType** and **GetOutputCurrentType** use the **DMO\_MEDIA\_TYPE** structure to return information to Windows Media Player about the media types previously set for the input and output streams.</span></span> <span data-ttu-id="edfe1-151">**GetInputStatus** retourne un indicateur qui indique à Windows Media Player si le plug-in DSP peut accepter des données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="edfe1-151">**GetInputStatus** returns a flag that tells Windows Media Player whether the DSP plug-in can accept input data.</span></span>

## <a name="methods-that-handle-buffering-and-processing-data"></a><span data-ttu-id="edfe1-152">Méthodes qui gèrent la mise en mémoire tampon et le traitement des données</span><span class="sxs-lookup"><span data-stu-id="edfe1-152">Methods that Handle Buffering and Processing Data</span></span>

<span data-ttu-id="edfe1-153">Il s’agit des méthodes que le lecteur Windows Media appelle pour initier les différents processus que le plug-in effectue pour effectuer le traitement du signal numérique.</span><span class="sxs-lookup"><span data-stu-id="edfe1-153">These are the methods that Windows Media Player calls to initiate the various processes that the plug-in performs to do the digital signal processing.</span></span> <span data-ttu-id="edfe1-154">Ces méthodes incluent les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="edfe1-154">These methods include:</span></span>

-   <span data-ttu-id="edfe1-155">**AllocateStreamingResources**</span><span class="sxs-lookup"><span data-stu-id="edfe1-155">**AllocateStreamingResources**</span></span>
-   <span data-ttu-id="edfe1-156">**Discontinuité**</span><span class="sxs-lookup"><span data-stu-id="edfe1-156">**Discontinuity**</span></span>
-   <span data-ttu-id="edfe1-157">**Purge**</span><span class="sxs-lookup"><span data-stu-id="edfe1-157">**Flush**</span></span>
-   <span data-ttu-id="edfe1-158">**FreeStreamingResources**</span><span class="sxs-lookup"><span data-stu-id="edfe1-158">**FreeStreamingResources**</span></span>
-   <span data-ttu-id="edfe1-159">**Verrou**</span><span class="sxs-lookup"><span data-stu-id="edfe1-159">**Lock**</span></span>
-   <span data-ttu-id="edfe1-160">**ProcessInput**</span><span class="sxs-lookup"><span data-stu-id="edfe1-160">**ProcessInput**</span></span>
-   <span data-ttu-id="edfe1-161">**ProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="edfe1-161">**ProcessOutput**</span></span>

<span data-ttu-id="edfe1-162">Le lecteur Windows Media appelle **AllocateStreamingResources** et **FreeStreamingResources** pour fournir au plug-in DSP la possibilité de configurer ou de libérer des tampons supplémentaires que le plug-in peut nécessiter pour le traitement interne.</span><span class="sxs-lookup"><span data-stu-id="edfe1-162">Windows Media Player calls **AllocateStreamingResources** and **FreeStreamingResources** to provide the DSP plug-in with an opportunity to set up or release any additional buffers the plug-in may require for internal processing.</span></span>

<span data-ttu-id="edfe1-163">Les plug-ins du lecteur Windows Media DSP n’ont pas besoin d’utiliser la méthode de **discontinuisation** DMO.</span><span class="sxs-lookup"><span data-stu-id="edfe1-163">Windows Media Player DSP plug-ins do not need to use the DMO **Discontinuity** method.</span></span>

<span data-ttu-id="edfe1-164">Le lecteur Windows Media appelle **flush** pour demander au plug-in DSP de vider toutes les données mises en mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="edfe1-164">Windows Media Player calls **Flush** to direct the DSP plug-in to flush all internally buffered data.</span></span> <span data-ttu-id="edfe1-165">Le plug-in doit libérer toutes les références aux interfaces **IMediaBuffer** , effacer toutes les valeurs qui spécifient l’horodatage ou l’exemple de longueur pour la mémoire tampon du média, et réinitialiser tous les États internes qui dépendent du contenu de l’exemple de support.</span><span class="sxs-lookup"><span data-stu-id="edfe1-165">The plug-in should release any references to **IMediaBuffer** interfaces, clear any values that specify the time stamp or sample length for the media buffer, and reinitialize any internal states that depend upon the contents of the media sample.</span></span>

<span data-ttu-id="edfe1-166">Le lecteur Windows Media appelle ProcessInput pour passer un pointeur vers une interface **IMediaBuffer** vers le plug-in DSP.</span><span class="sxs-lookup"><span data-stu-id="edfe1-166">Windows Media Player calls ProcessInput to pass a pointer to an **IMediaBuffer** interface to the DSP plug-in.</span></span> <span data-ttu-id="edfe1-167">Cette interface fournit l’accès à la mémoire tampon d’entrée allouée par le lecteur Windows Media pour fournir des données au plug-in.</span><span class="sxs-lookup"><span data-stu-id="edfe1-167">This interface provides access to the input buffer allocated by Windows Media Player to supply data to the plug-in.</span></span> <span data-ttu-id="edfe1-168">Le lecteur Windows Media appelle ensuite **ProcessOutput** pour passer un pointeur vers une interface **IMediaBuffer** qui fournit l’accès à la mémoire tampon de sortie allouée par le lecteur Windows Media pour recevoir les données traitées du plug-in DSP.</span><span class="sxs-lookup"><span data-stu-id="edfe1-168">Windows Media Player subsequently calls **ProcessOutput** to pass a pointer to an **IMediaBuffer** interface that provides access to the output buffer allocated by Windows Media Player to receive the processed data from the DSP plug-in.</span></span>

<span data-ttu-id="edfe1-169">L’interface **IMediaObject** comprend une méthode nommée **Lock**.</span><span class="sxs-lookup"><span data-stu-id="edfe1-169">The **IMediaObject** interface includes a method named **Lock**.</span></span> <span data-ttu-id="edfe1-170">Cette méthode est conçue pour acquérir ou libérer un verrou sur DMO afin de conserver la méthode DMO sérialisée lors de l’exécution de plusieurs opérations.</span><span class="sxs-lookup"><span data-stu-id="edfe1-170">This method is designed to acquire or release a lock on the DMO to keep the DMO serialized when performing multiple operations.</span></span> <span data-ttu-id="edfe1-171">La version de **IMediaObject :: Lock** dans le code de l’Assistant remplace l’implémentation ATL de **Lock**.</span><span class="sxs-lookup"><span data-stu-id="edfe1-171">The version of **IMediaObject::Lock** in the wizard code overrides the ATL implementation of **Lock**.</span></span> <span data-ttu-id="edfe1-172">Étant donné que le lecteur Windows Media sérialise les appels passés à l’interface DMO d’un plug-in DSP, l’implémentation de **Lock** retourne simplement S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="edfe1-172">Because Windows Media Player serializes calls made to the DMO interface of a DSP plug-in, the implementation of **Lock** simply returns S\_OK.</span></span> <span data-ttu-id="edfe1-173">Pour plus d’informations sur la création d’un multithread DMO, reportez-vous à la section DirectShow de l’SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="edfe1-173">For details about how to create a multithreaded DMO, refer to the DirectShow section of the Windows SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="edfe1-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="edfe1-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edfe1-175">**Interfaces requises**</span><span class="sxs-lookup"><span data-stu-id="edfe1-175">**Required Interfaces**</span></span>](required-interfaces.md)
</dt> </dl>

 

 




