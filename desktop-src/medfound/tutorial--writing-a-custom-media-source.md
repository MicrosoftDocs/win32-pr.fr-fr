---
description: Cette rubrique présente en détail l’exemple du kit de développement logiciel (SDK) source de média MPEG-1.
ms.assetid: d392f30c-c963-4eb3-add2-1bb986919c0b
title: 'Étude de cas : source de média MPEG-1'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87e1f72cc6ae6df119439bdae1942732bf8d2fa2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104042926"
---
# <a name="case-study-mpeg-1-media-source"></a><span data-ttu-id="03cea-103">Étude de cas : source de média MPEG-1</span><span class="sxs-lookup"><span data-stu-id="03cea-103">Case Study: MPEG-1 Media Source</span></span>

<span data-ttu-id="03cea-104">Dans Microsoft Media Foundation, l’objet qui introduit les données multimédias dans le pipeline de données est appelé une *source de média*.</span><span class="sxs-lookup"><span data-stu-id="03cea-104">In Microsoft Media Foundation, the object that introduces media data into the data pipeline is called a *media source*.</span></span> <span data-ttu-id="03cea-105">Cette rubrique présente en détail l’exemple du kit de développement logiciel (SDK) [source de média MPEG-1](mpeg1source-sample.md) .</span><span class="sxs-lookup"><span data-stu-id="03cea-105">This topic takes an in-depth look at the [MPEG-1 Media Source](mpeg1source-sample.md) SDK Sample.</span></span>

-   [<span data-ttu-id="03cea-106">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="03cea-106">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="03cea-107">Classes C++ utilisées dans la source MPEG-1</span><span class="sxs-lookup"><span data-stu-id="03cea-107">C++ Classes Used in the MPEG-1 Source</span></span>](#c-classes-used-in-the-mpeg-1-source)
-   [<span data-ttu-id="03cea-108">Gestionnaire de flux d’octets</span><span class="sxs-lookup"><span data-stu-id="03cea-108">Byte-Stream Handler</span></span>](#byte-stream-handler)
-   [<span data-ttu-id="03cea-109">Descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="03cea-109">Presentation Descriptor</span></span>](#presentation-descriptor)
-   [<span data-ttu-id="03cea-110">États de streaming</span><span class="sxs-lookup"><span data-stu-id="03cea-110">Streaming States</span></span>](#streaming-states)
    -   [<span data-ttu-id="03cea-111">Start</span><span class="sxs-lookup"><span data-stu-id="03cea-111">Start</span></span>](#start)
    -   [<span data-ttu-id="03cea-112">Pause</span><span class="sxs-lookup"><span data-stu-id="03cea-112">Pause</span></span>](#pause)
    -   [<span data-ttu-id="03cea-113">Stop</span><span class="sxs-lookup"><span data-stu-id="03cea-113">Stop</span></span>](#stop)
-   [<span data-ttu-id="03cea-114">Exemples de demandes</span><span class="sxs-lookup"><span data-stu-id="03cea-114">Sample Requests</span></span>](#sample-requests)
-   [<span data-ttu-id="03cea-115">Fin de flux</span><span class="sxs-lookup"><span data-stu-id="03cea-115">End of Stream</span></span>](#end-of-stream)
-   [<span data-ttu-id="03cea-116">Opérations asynchrones</span><span class="sxs-lookup"><span data-stu-id="03cea-116">Asynchronous Operations</span></span>](#asynchronous-operations)
    -   [<span data-ttu-id="03cea-117">File d’attente des opérations</span><span class="sxs-lookup"><span data-stu-id="03cea-117">Operation Queue</span></span>](#operation-queue)
-   [<span data-ttu-id="03cea-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="03cea-118">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="03cea-119">Prérequis</span><span class="sxs-lookup"><span data-stu-id="03cea-119">Prerequisites</span></span>

<span data-ttu-id="03cea-120">Avant de lire cette rubrique, vous devez comprendre les concepts de Media Foundation suivants :</span><span class="sxs-lookup"><span data-stu-id="03cea-120">Before reading this topic you should understand the following Media Foundation concepts:</span></span>

-   [<span data-ttu-id="03cea-121">Modèle d’objet de source multimédia</span><span class="sxs-lookup"><span data-stu-id="03cea-121">Media Source Object Model</span></span>](media-source-object-model.md)
-   <span data-ttu-id="03cea-122">[Méthodes de rappel asynchrones](asynchronous-callback-methods.md).</span><span class="sxs-lookup"><span data-stu-id="03cea-122">[Asynchronous Callback Methods](asynchronous-callback-methods.md).</span></span>
-   [<span data-ttu-id="03cea-123">Files d’attente de travail</span><span class="sxs-lookup"><span data-stu-id="03cea-123">Work Queues</span></span>](work-queues.md)
-   [<span data-ttu-id="03cea-124">Générateurs d’événements de média</span><span class="sxs-lookup"><span data-stu-id="03cea-124">Media Event Generators</span></span>](media-event-generators.md)
-   [<span data-ttu-id="03cea-125">Mémoires tampons de média</span><span class="sxs-lookup"><span data-stu-id="03cea-125">Media Buffers</span></span>](media-buffers.md)
-   [<span data-ttu-id="03cea-126">Exemples de supports</span><span class="sxs-lookup"><span data-stu-id="03cea-126">Media Samples</span></span>](media-samples.md)
-   [<span data-ttu-id="03cea-127">Types de médias</span><span class="sxs-lookup"><span data-stu-id="03cea-127">Media Types</span></span>](media-types.md)

<span data-ttu-id="03cea-128">Vous devez également avoir une compréhension de base de l’architecture Media Foundation, en particulier le rôle des sources multimédias dans le pipeline.</span><span class="sxs-lookup"><span data-stu-id="03cea-128">You should also have a basic understanding of the Media Foundation architecture, particularly the role of media sources in the pipeline.</span></span> <span data-ttu-id="03cea-129">(Pour plus d’informations, consultez [sources multimédias](media-sources.md).)</span><span class="sxs-lookup"><span data-stu-id="03cea-129">(For more information, see [Media Sources](media-sources.md).)</span></span>

<span data-ttu-id="03cea-130">En outre, vous souhaiterez peut-être lire la rubrique [écriture d’une source de média personnalisée](writing-a-custom-media-source.md), qui donne une vue d’ensemble plus générale des étapes décrites ici.</span><span class="sxs-lookup"><span data-stu-id="03cea-130">In addition, you may want to read the topic [Writing a Custom Media Source](writing-a-custom-media-source.md), which gives a more general overview of the steps described here.</span></span>

<span data-ttu-id="03cea-131">Cette rubrique ne reproduit pas l’intégralité du code de l’exemple du kit de développement logiciel (SDK), car l’exemple est relativement volumineux.</span><span class="sxs-lookup"><span data-stu-id="03cea-131">This topic does not reproduce all of the code from the SDK sample, because the sample is fairly large.</span></span>

## <a name="c-classes-used-in-the-mpeg-1-source"></a><span data-ttu-id="03cea-132">Classes C++ utilisées dans la source MPEG-1</span><span class="sxs-lookup"><span data-stu-id="03cea-132">C++ Classes Used in the MPEG-1 Source</span></span>

<span data-ttu-id="03cea-133">L’exemple de source MPEG-1 est implémenté avec les classes C++ suivantes :</span><span class="sxs-lookup"><span data-stu-id="03cea-133">The sample MPEG-1 source is implemented with the following C++ classes:</span></span>

-   <span data-ttu-id="03cea-134">`MPEG1ByteStreamHandler`.</span><span class="sxs-lookup"><span data-stu-id="03cea-134">`MPEG1ByteStreamHandler`.</span></span> <span data-ttu-id="03cea-135">Implémente le gestionnaire de flux d’octets pour la source du média.</span><span class="sxs-lookup"><span data-stu-id="03cea-135">Implements the byte-stream handler for the media source.</span></span> <span data-ttu-id="03cea-136">Pour un flux d’octets donné, le gestionnaire de flux d’octets crée une instance de la source.</span><span class="sxs-lookup"><span data-stu-id="03cea-136">Given a byte stream, the byte-stream handler creates an instance of the source.</span></span>
-   <span data-ttu-id="03cea-137">`MPEG1Source`.</span><span class="sxs-lookup"><span data-stu-id="03cea-137">`MPEG1Source`.</span></span> <span data-ttu-id="03cea-138">Implémente la source du média.</span><span class="sxs-lookup"><span data-stu-id="03cea-138">Implements the media source.</span></span>
-   <span data-ttu-id="03cea-139">`MPEG1Stream`.</span><span class="sxs-lookup"><span data-stu-id="03cea-139">`MPEG1Stream`.</span></span> <span data-ttu-id="03cea-140">Implémente les objets de flux de média.</span><span class="sxs-lookup"><span data-stu-id="03cea-140">Implements the media stream objects.</span></span> <span data-ttu-id="03cea-141">La source du média crée un `MPEG1Stream` objet pour chaque flux audio ou vidéo dans le flux de données MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="03cea-141">The media source creates one `MPEG1Stream` object for every audio or video stream in the MPEG-1 bitstream.</span></span>
-   <span data-ttu-id="03cea-142">`Parser`.</span><span class="sxs-lookup"><span data-stu-id="03cea-142">`Parser`.</span></span> <span data-ttu-id="03cea-143">Analyse le flux de bits MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="03cea-143">Parses the MPEG-1 bitstream.</span></span> <span data-ttu-id="03cea-144">Pour l’essentiel, les détails de cette classe ne sont pas pertinents pour les API Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="03cea-144">For the most part, the details of this class are not relevant to the Media Foundation APIs.</span></span>
-   <span data-ttu-id="03cea-145">SourceOp, OpQueue : ces deux classes gèrent les opérations asynchrones dans la source du média.</span><span class="sxs-lookup"><span data-stu-id="03cea-145">SourceOp, OpQueue: These two classes manage asynchronous operations in the media source.</span></span> <span data-ttu-id="03cea-146">(Voir [opérations asynchrones](#asynchronous-operations)).</span><span class="sxs-lookup"><span data-stu-id="03cea-146">(See [Asynchronous Operations](#asynchronous-operations)).</span></span>

<span data-ttu-id="03cea-147">D’autres classes d’assistance diverses sont décrites plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="03cea-147">Other miscellaneous helper classes are described later in the topic.</span></span>

## <a name="byte-stream-handler"></a><span data-ttu-id="03cea-148">Gestionnaire de Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="03cea-148">Byte-Stream Handler</span></span>

<span data-ttu-id="03cea-149">Le gestionnaire *de flux d’octets* est l’objet qui crée la source du média.</span><span class="sxs-lookup"><span data-stu-id="03cea-149">The *byte-stream* handler is the object that creates the media source.</span></span> <span data-ttu-id="03cea-150">Le gestionnaire de flux d’octets est créé par le programme de résolution source ; les applications n’interagissent pas directement avec le gestionnaire de flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="03cea-150">The byte-stream handler is created by the source resolver; applications do not interact directly with the byte-stream handler.</span></span> <span data-ttu-id="03cea-151">Le programme de résolution source Découvre le gestionnaire de flux d’octets en recherchant dans le registre.</span><span class="sxs-lookup"><span data-stu-id="03cea-151">The source resolver discovers the byte-stream handler by looking in the registry.</span></span> <span data-ttu-id="03cea-152">Le gestionnaire est inscrit par une extension de nom de fichier ou un type MIME.</span><span class="sxs-lookup"><span data-stu-id="03cea-152">Handler are registered by file name extension or MIME type.</span></span> <span data-ttu-id="03cea-153">Pour la source MPEG-1, le gestionnaire de flux d’octets est inscrit pour l’extension de nom de fichier « . mpg ».</span><span class="sxs-lookup"><span data-stu-id="03cea-153">For the MPEG-1 source, the byte-stream handler is registered for the ".mpg" file name extension.</span></span>

> [!Note]  
> <span data-ttu-id="03cea-154">Si vous souhaitez prendre en charge des schémas d’URL personnalisés, vous pouvez également écrire un *Gestionnaire de schéma*.</span><span class="sxs-lookup"><span data-stu-id="03cea-154">If you want to support custom URL schemes, you can also write a *scheme handler*.</span></span> <span data-ttu-id="03cea-155">La source MPEG-1 est conçue pour les fichiers locaux et Media Foundation fournit déjà un gestionnaire de schéma pour les URL « file:// ».</span><span class="sxs-lookup"><span data-stu-id="03cea-155">The MPEG-1 source is designed for local files, and Media Foundation already provides a scheme handler for "file://" URLs.</span></span>

 

<span data-ttu-id="03cea-156">Le gestionnaire de flux d’octets implémente l’interface [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) .</span><span class="sxs-lookup"><span data-stu-id="03cea-156">The byte-stream handler implements the [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) interface.</span></span> <span data-ttu-id="03cea-157">Cette interface a deux méthodes les plus importantes qui doivent être implémentées :</span><span class="sxs-lookup"><span data-stu-id="03cea-157">This interface has two most important methods that must be implemented:</span></span>

-   <span data-ttu-id="03cea-158">[**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject).</span><span class="sxs-lookup"><span data-stu-id="03cea-158">[**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject).</span></span> <span data-ttu-id="03cea-159">Démarre une opération asynchrone pour créer la source du média.</span><span class="sxs-lookup"><span data-stu-id="03cea-159">Starts an asynchronous operation to create the media source.</span></span>
-   <span data-ttu-id="03cea-160">[**EndCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject).</span><span class="sxs-lookup"><span data-stu-id="03cea-160">[**EndCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject).</span></span> <span data-ttu-id="03cea-161">Termine l’appel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="03cea-161">Completes the asynchronous call.</span></span>

<span data-ttu-id="03cea-162">Deux autres méthodes sont facultatives et ne sont pas implémentées dans l’exemple du kit de développement logiciel (SDK) :</span><span class="sxs-lookup"><span data-stu-id="03cea-162">Two other methods are optional and not implemented in the SDK sample:</span></span>

-   <span data-ttu-id="03cea-163">[**CancelObjectCreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation).</span><span class="sxs-lookup"><span data-stu-id="03cea-163">[**CancelObjectCreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation).</span></span> <span data-ttu-id="03cea-164">Annule la méthode [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) .</span><span class="sxs-lookup"><span data-stu-id="03cea-164">Cancels the [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) method.</span></span> <span data-ttu-id="03cea-165">Cette méthode est utile pour une source réseau qui peut avoir une latence élevée au démarrage.</span><span class="sxs-lookup"><span data-stu-id="03cea-165">This method is useful for a network source that might have a high latency at startup.</span></span>
-   <span data-ttu-id="03cea-166">[**GetMaxNumberOfBytesRequiredForResolution**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-getmaxnumberofbytesrequiredforresolution).</span><span class="sxs-lookup"><span data-stu-id="03cea-166">[**GetMaxNumberOfBytesRequiredForResolution**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-getmaxnumberofbytesrequiredforresolution).</span></span> <span data-ttu-id="03cea-167">Obtient le nombre maximal d’octets que le gestionnaire lira à partir du flux source.</span><span class="sxs-lookup"><span data-stu-id="03cea-167">Gets the maximum number of bytes that the handler will read from the source stream.</span></span> <span data-ttu-id="03cea-168">Implémentez cette méthode si vous savez combien de données le gestionnaire de flux d’octets avant de pouvoir créer la source du média.</span><span class="sxs-lookup"><span data-stu-id="03cea-168">Implement this method if you know how much data the byte-stream handler before it can create the media source.</span></span> <span data-ttu-id="03cea-169">Dans le cas contraire, renvoyez simplement **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="03cea-169">Otherwise, simply return **E\_NOTIMPL**.</span></span>

<span data-ttu-id="03cea-170">Voici l’implémentation de la méthode [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) :</span><span class="sxs-lookup"><span data-stu-id="03cea-170">Here is the implementation of the [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) method:</span></span>


```C++
HRESULT MPEG1ByteStreamHandler::BeginCreateObject(
        /* [in] */ IMFByteStream *pByteStream,
        /* [in] */ LPCWSTR pwszURL,
        /* [in] */ DWORD dwFlags,
        /* [in] */ IPropertyStore *pProps,
        /* [out] */ IUnknown **ppIUnknownCancelCookie,  // Can be NULL
        /* [in] */ IMFAsyncCallback *pCallback,
        /* [in] */ IUnknown *punkState                  // Can be NULL
        )
{
    if (pByteStream == NULL)
    {
        return E_POINTER;
    }

    if (pCallback == NULL)
    {
        return E_POINTER;
    }

    if ((dwFlags & MF_RESOLUTION_MEDIASOURCE) == 0)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_OK;

    IMFAsyncResult *pResult = NULL;
    MPEG1Source    *pSource = NULL;

    // Create an instance of the media source.
    hr = MPEG1Source::CreateInstance(&pSource);

    // Create a result object for the caller's async callback.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateAsyncResult(NULL, pCallback, punkState, &pResult);
    }

    // Start opening the source. This is an async operation.
    // When it completes, the source will invoke our callback
    // and then we will invoke the caller's callback.
    if (SUCCEEDED(hr))
    {
        hr = pSource->BeginOpen(pByteStream, this, NULL);
    }

    if (SUCCEEDED(hr))
    {
        if (ppIUnknownCancelCookie)
        {
            *ppIUnknownCancelCookie = NULL;
        }

        m_pSource = pSource;
        m_pSource->AddRef();

        m_pResult = pResult;
        m_pResult->AddRef();
    }

// cleanup
    SafeRelease(&pSource);
    SafeRelease(&pResult);
    return hr;
}
```



<span data-ttu-id="03cea-171">La méthode effectue les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="03cea-171">The method performs the following steps:</span></span>

1.  <span data-ttu-id="03cea-172">Crée une nouvelle instance de l'objet `MPEG1Source`.</span><span class="sxs-lookup"><span data-stu-id="03cea-172">Creates a new instance of the `MPEG1Source` object.</span></span>
2.  <span data-ttu-id="03cea-173">Créez un objet de résultat asynchrone.</span><span class="sxs-lookup"><span data-stu-id="03cea-173">Create an asynchronous result object.</span></span> <span data-ttu-id="03cea-174">Cet objet est utilisé ultérieurement pour appeler la méthode de rappel de l’outil de résolution source.</span><span class="sxs-lookup"><span data-stu-id="03cea-174">This object is used later to invoke the source resolver's callback method.</span></span>
3.  <span data-ttu-id="03cea-175">Appelle `MPEG1Source::BeginOpen` , une méthode asynchrone définie dans la `MPEG1Source` classe.</span><span class="sxs-lookup"><span data-stu-id="03cea-175">Calls `MPEG1Source::BeginOpen`, an asynchronous method defined in the `MPEG1Source` class.</span></span>
4.  <span data-ttu-id="03cea-176">Affecte la **valeur null** à *ppIUnknownCancelCookie* , ce qui indique à l’appelant que [**CancelObjectCreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation) n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="03cea-176">Sets *ppIUnknownCancelCookie* to **NULL**, which informs the caller that [**CancelObjectCreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation) is not supported.</span></span>

<span data-ttu-id="03cea-177">La `MPEG1Source::BeginOpen` méthode effectue le travail réel de lecture du flux d’octets et d’initialisation de l' `MPEG1Source` objet.</span><span class="sxs-lookup"><span data-stu-id="03cea-177">The `MPEG1Source::BeginOpen` method does the actual work of reading the byte stream and initializing the `MPEG1Source` object.</span></span> <span data-ttu-id="03cea-178">Cette méthode ne fait pas partie de l’API publique.</span><span class="sxs-lookup"><span data-stu-id="03cea-178">This method is not part of the public API.</span></span> <span data-ttu-id="03cea-179">Vous pouvez définir n’importe quel mécanisme entre le gestionnaire et la source du média qui répond à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="03cea-179">You can define any mechanism between the handler and the media source that suits your needs.</span></span> <span data-ttu-id="03cea-180">Le fait de placer la majeure partie de la logique dans la source du média permet de conserver un gestionnaire de flux d’octets relativement simple.</span><span class="sxs-lookup"><span data-stu-id="03cea-180">Putting most of the logic into the media source keeps the byte-stream handler relatively simple.</span></span>

<span data-ttu-id="03cea-181">En bref, `BeginOpen` effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="03cea-181">Briefly, `BeginOpen` does the following:</span></span>

1.  <span data-ttu-id="03cea-182">Appelle [**IMFByteStream :: GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) pour vérifier que le flux d’octets source est à la fois lisible et pouvant être recherché.</span><span class="sxs-lookup"><span data-stu-id="03cea-182">Calls [**IMFByteStream::GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) to verify that the source byte stream is both readable and seekable.</span></span>
2.  <span data-ttu-id="03cea-183">Appelle [**IMFByteStream :: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) pour démarrer une requête d’e/s asynchrone.</span><span class="sxs-lookup"><span data-stu-id="03cea-183">Calls [**IMFByteStream::BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) to start an asynchronous I/O request.</span></span>

<span data-ttu-id="03cea-184">Le reste de l’initialisation se produit de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="03cea-184">The rest of the initialization occurs asynchronously.</span></span> <span data-ttu-id="03cea-185">La source du média lit suffisamment de données à partir du flux pour analyser les en-têtes de séquence MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="03cea-185">The media source reads enough data from the stream to parse the MPEG-1 sequence headers.</span></span> <span data-ttu-id="03cea-186">Ensuite, il crée un *descripteur de présentation*, qui est l’objet utilisé pour décrire les flux audio et vidéo dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="03cea-186">Then it creates a *presentation descriptor*, which is the object used to describe the audio and video streams in the file.</span></span> <span data-ttu-id="03cea-187">(Pour plus d’informations, consultez [descripteur de présentation](#presentation-descriptor).) Lorsque l' `BeginOpen` opération est terminée, le gestionnaire de flux d’octets appelle la méthode de rappel de l’outil de résolution source.</span><span class="sxs-lookup"><span data-stu-id="03cea-187">(For more information, see [Presentation Descriptor](#presentation-descriptor).) When the `BeginOpen` operation completes, the byte-stream handler invokes the source resolver's callback method.</span></span> <span data-ttu-id="03cea-188">À ce stade, le programme de résolution source appelle [**IMFByteStreamHandler :: EndCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject).</span><span class="sxs-lookup"><span data-stu-id="03cea-188">At that point, the source resolver calls [**IMFByteStreamHandler::EndCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject).</span></span> <span data-ttu-id="03cea-189">La méthode **EndCreateObject** retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="03cea-189">The **EndCreateObject** method returns the status of the operation.</span></span>


```C++
HRESULT MPEG1ByteStreamHandler::EndCreateObject(
        /* [in] */ IMFAsyncResult *pResult,
        /* [out] */ MF_OBJECT_TYPE *pObjectType,
        /* [out] */ IUnknown **ppObject)
{
    if (pResult == NULL || pObjectType == NULL || ppObject == NULL)
    {
        return E_POINTER;
    }

    HRESULT hr = S_OK;

    *pObjectType = MF_OBJECT_INVALID;
    *ppObject = NULL;

    hr = pResult->GetStatus();

    if (SUCCEEDED(hr))
    {
        *pObjectType = MF_OBJECT_MEDIASOURCE;

        assert(m_pSource != NULL);

        hr = m_pSource->QueryInterface(IID_PPV_ARGS(ppObject));
    }

    SafeRelease(&m_pSource);
    SafeRelease(&m_pResult);
    return hr;
}
```



<span data-ttu-id="03cea-190">Si une erreur se produit à tout moment pendant ce processus, le rappel est appelé avec un code d’état d’erreur.</span><span class="sxs-lookup"><span data-stu-id="03cea-190">If an error occurs at any time during this process, the callback is invoked with an error status code.</span></span>

## <a name="presentation-descriptor"></a><span data-ttu-id="03cea-191">Descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="03cea-191">Presentation Descriptor</span></span>

<span data-ttu-id="03cea-192">Le descripteur de présentation décrit le contenu du fichier MPEG-1, y compris les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="03cea-192">The presentation descriptor describes the contents of the MPEG-1 file, including the following information:</span></span>

-   <span data-ttu-id="03cea-193">Nombre de flux.</span><span class="sxs-lookup"><span data-stu-id="03cea-193">The number of the streams.</span></span>
-   <span data-ttu-id="03cea-194">Format de chaque flux.</span><span class="sxs-lookup"><span data-stu-id="03cea-194">The format of each stream.</span></span>
-   <span data-ttu-id="03cea-195">Identificateurs de flux.</span><span class="sxs-lookup"><span data-stu-id="03cea-195">Stream identifiers.</span></span>
-   <span data-ttu-id="03cea-196">État de sélection de chaque flux (sélectionné ou désélectionné).</span><span class="sxs-lookup"><span data-stu-id="03cea-196">The selection status of each stream (selected or deselected).</span></span>

<span data-ttu-id="03cea-197">En termes d’architecture Media Foundation, le descripteur de présentation contient un ou plusieurs *descripteurs de flux*.</span><span class="sxs-lookup"><span data-stu-id="03cea-197">In terms of the Media Foundation architecture, the presentation descriptor contains one or more *stream descriptors*.</span></span> <span data-ttu-id="03cea-198">Chaque descripteur de flux contient un *Gestionnaire de type de média* qui est utilisé pour obtenir ou définir des types de média sur le flux.</span><span class="sxs-lookup"><span data-stu-id="03cea-198">Each stream descriptor contains a *media type handler*, which is used to get or set media types on the stream.</span></span> <span data-ttu-id="03cea-199">Media Foundation fournit des implémentations de stock pour le descripteur de présentation et le descripteur de flux ; celles-ci conviennent à la plupart des sources multimédias.</span><span class="sxs-lookup"><span data-stu-id="03cea-199">Media Foundation provides stock implementations for the presentation descriptor and stream descriptor; these are suitable for most media sources.</span></span>

<span data-ttu-id="03cea-200">Pour créer un descripteur de présentation, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="03cea-200">To create a presentation descriptor, perform the following steps:</span></span>

1.  <span data-ttu-id="03cea-201">Pour chaque flux :</span><span class="sxs-lookup"><span data-stu-id="03cea-201">For each stream:</span></span>
    1.  <span data-ttu-id="03cea-202">Fournissez un ID de flux et un tableau de types de média possibles.</span><span class="sxs-lookup"><span data-stu-id="03cea-202">Provide a stream ID and an array of possible media types.</span></span> <span data-ttu-id="03cea-203">Si le flux prend en charge plusieurs types de média, classez la liste des types de médias par préférence, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="03cea-203">If the stream supports more than one media type, order the list of media types by preference, if any.</span></span> <span data-ttu-id="03cea-204">(Placez d’abord le type optimal et le type le moins optimal).</span><span class="sxs-lookup"><span data-stu-id="03cea-204">(Put the optimal type first, and the least optimal type last.)</span></span>
    2.  <span data-ttu-id="03cea-205">Appelez [**MFCreateStreamDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatestreamdescriptor) pour créer le descripteur de flux.</span><span class="sxs-lookup"><span data-stu-id="03cea-205">Call [**MFCreateStreamDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatestreamdescriptor) to create the stream descriptor.</span></span>
    3.  <span data-ttu-id="03cea-206">Appelez [**IMFStreamDescriptor :: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) sur le descripteur de flux que vous venez de créer.</span><span class="sxs-lookup"><span data-stu-id="03cea-206">Call [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) on the newly created stream descriptor.</span></span>
    4.  <span data-ttu-id="03cea-207">Appelez [**IMFMediaTypeHandler :: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) pour définir le format par défaut du flux.</span><span class="sxs-lookup"><span data-stu-id="03cea-207">Call [**IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) to set the default format for the stream.</span></span> <span data-ttu-id="03cea-208">S’il existe plusieurs types de média, vous devez généralement définir le premier type dans la liste.</span><span class="sxs-lookup"><span data-stu-id="03cea-208">If there is more than one media type, you should generally set the first type in the list.</span></span>
2.  <span data-ttu-id="03cea-209">Appelez [**MFCreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) et transmettez le tableau de pointeurs de descripteur de flux.</span><span class="sxs-lookup"><span data-stu-id="03cea-209">Call [**MFCreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) and pass in the array of stream descriptor pointers.</span></span>
3.  <span data-ttu-id="03cea-210">Pour chaque flux, appelez [**IMFPresentationDescriptor :: SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) ou [**DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) pour définir l’état de sélection par défaut.</span><span class="sxs-lookup"><span data-stu-id="03cea-210">For each stream, call [**IMFPresentationDescriptor::SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) or [**DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) to set the default selection state.</span></span> <span data-ttu-id="03cea-211">S’il existe plusieurs flux du même type (audio ou vidéo), un seul doit être sélectionné par défaut.</span><span class="sxs-lookup"><span data-stu-id="03cea-211">If there is more than one stream of the same type (audio or video), only one should be selected by default.</span></span>

<span data-ttu-id="03cea-212">L' `MPEG1Source` objet crée le descripteur de présentation dans sa `InitPresentationDescriptor` méthode :</span><span class="sxs-lookup"><span data-stu-id="03cea-212">The `MPEG1Source` object creates the presentation descriptor in its `InitPresentationDescriptor` method:</span></span>


```C++
HRESULT MPEG1Source::InitPresentationDescriptor()
{
    HRESULT hr = S_OK;
    DWORD cStreams = 0;

    assert(m_pPresentationDescriptor == NULL);
    assert(m_state == STATE_OPENING);

    if (m_pHeader == NULL)
    {
        return E_FAIL;
    }

    // Get the number of streams, as declared in the MPEG-1 header, skipping
    // any streams with an unsupported format.
    for (DWORD i = 0; i < m_pHeader->cStreams; i++)
    {
        if (IsStreamTypeSupported(m_pHeader->streams[i].type))
        {
            cStreams++;
        }
    }

    // How many streams do we actually have?
    if (cStreams > m_streams.GetCount())
    {
        // Keep reading data until we have seen a packet for each stream.
        return S_OK;
    }

    // We should never create a stream we don't support.
    assert(cStreams == m_streams.GetCount());

    // Ready to create the presentation descriptor.

    // Create an array of IMFStreamDescriptor pointers.
    IMFStreamDescriptor **ppSD =
            new (std::nothrow) IMFStreamDescriptor*[cStreams];

    if (ppSD == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    ZeroMemory(ppSD, cStreams * sizeof(IMFStreamDescriptor*));

    // Fill the array by getting the stream descriptors from the streams.
    for (DWORD i = 0; i < cStreams; i++)
    {
        hr = m_streams[i]->GetStreamDescriptor(&ppSD[i]);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Create the presentation descriptor.
    hr = MFCreatePresentationDescriptor(cStreams, ppSD,
        &m_pPresentationDescriptor);

    if (FAILED(hr))
    {
        goto done;
    }

    // Select the first video stream (if any).
    for (DWORD i = 0; i < cStreams; i++)
    {
        GUID majorType = GUID_NULL;

        hr = GetStreamMajorType(ppSD[i], &majorType);
        if (FAILED(hr))
        {
            goto done;
        }

        if (majorType == MFMediaType_Video)
        {
            hr = m_pPresentationDescriptor->SelectStream(i);
            if (FAILED(hr))
            {
                goto done;
            }
            break;
        }
    }

    // Switch state from "opening" to stopped.
    m_state = STATE_STOPPED;

    // Invoke the async callback to complete the BeginOpen operation.
    hr = CompleteOpen(S_OK);

done:
    // clean up:
    if (ppSD)
    {
        for (DWORD i = 0; i < cStreams; i++)
        {
            SafeRelease(&ppSD[i]);
        }
        delete [] ppSD;
    }
    return hr;
}
```



<span data-ttu-id="03cea-213">L’application obtient le descripteur de présentation en appelant [**IMFMediaSource :: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="03cea-213">The application gets the presentation descriptor by calling [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span> <span data-ttu-id="03cea-214">Cette méthode crée une copie superficielle du descripteur de présentation en appelant [**IMFPresentationDescriptor :: Clone**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-clone).</span><span class="sxs-lookup"><span data-stu-id="03cea-214">This method creates a shallow copy of the presentation descriptor by calling [**IMFPresentationDescriptor::Clone**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-clone).</span></span> <span data-ttu-id="03cea-215">(La copie contient des pointeurs vers les descripteurs de flux d’origine.) L’application peut utiliser le descripteur de présentation pour définir le type de média, sélectionner un flux ou désélectionner un flux.</span><span class="sxs-lookup"><span data-stu-id="03cea-215">(The copy contains pointers to the original stream descriptors.) The application can use the presentation descriptor to set the media type, select a stream, or deselect a stream.</span></span>

<span data-ttu-id="03cea-216">Si vous le souhaitez, les descripteurs de présentation et les descripteurs de flux peuvent contenir des attributs qui fournissent des informations supplémentaires sur la source.</span><span class="sxs-lookup"><span data-stu-id="03cea-216">Optionally, presentation descriptors and stream descriptors can contain attributes that give additional information about the source.</span></span> <span data-ttu-id="03cea-217">Pour obtenir la liste de ces attributs, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="03cea-217">For a list such attributes, see the following topics:</span></span>

-   [<span data-ttu-id="03cea-218">Attributs du descripteur de présentation</span><span class="sxs-lookup"><span data-stu-id="03cea-218">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
-   [<span data-ttu-id="03cea-219">Attributs du descripteur de flux</span><span class="sxs-lookup"><span data-stu-id="03cea-219">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)

<span data-ttu-id="03cea-220">Un attribut mérite une mention spéciale : l’attribut de [**\_ \_ durée MF PD**](mf-pd-duration-attribute.md) contient la durée totale de la source.</span><span class="sxs-lookup"><span data-stu-id="03cea-220">One attribute deserves special mention: The [**MF\_PD\_DURATION**](mf-pd-duration-attribute.md) attribute contains the total duration of the source.</span></span> <span data-ttu-id="03cea-221">Définissez cet attribut si vous connaissez la durée en amont ; par exemple, la durée peut être spécifiée dans les en-têtes de fichier, selon le format de fichier.</span><span class="sxs-lookup"><span data-stu-id="03cea-221">Set this attribute if you know the duration up front; for example, the duration might be specified in the file headers, depending on the file format.</span></span> <span data-ttu-id="03cea-222">L’application peut afficher cette valeur ou l’utiliser pour définir une barre de progression ou une barre de recherche.</span><span class="sxs-lookup"><span data-stu-id="03cea-222">The application might display this value, or use it to set a progress bar or seek bar.</span></span>

## <a name="streaming-states"></a><span data-ttu-id="03cea-223">États de streaming</span><span class="sxs-lookup"><span data-stu-id="03cea-223">Streaming States</span></span>

<span data-ttu-id="03cea-224">Une source de média définit les États suivants :</span><span class="sxs-lookup"><span data-stu-id="03cea-224">A media source defines the following states:</span></span>



| <span data-ttu-id="03cea-225">State</span><span class="sxs-lookup"><span data-stu-id="03cea-225">State</span></span>    | <span data-ttu-id="03cea-226">Description</span><span class="sxs-lookup"><span data-stu-id="03cea-226">Description</span></span>                                                                                                     |
|----------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03cea-227">Démarré</span><span class="sxs-lookup"><span data-stu-id="03cea-227">Started</span></span>  | <span data-ttu-id="03cea-228">La source accepte et traite les exemples de demandes.</span><span class="sxs-lookup"><span data-stu-id="03cea-228">The source accepts and processes sample requests.</span></span>                                                               |
| <span data-ttu-id="03cea-229">Suspendu</span><span class="sxs-lookup"><span data-stu-id="03cea-229">Paused</span></span>   | <span data-ttu-id="03cea-230">La source accepte les exemples de demandes, mais ne les traite pas.</span><span class="sxs-lookup"><span data-stu-id="03cea-230">The source accepts sample requests, but does not process them.</span></span> <span data-ttu-id="03cea-231">Les demandes sont mises en file d’attente jusqu’au démarrage de la source.</span><span class="sxs-lookup"><span data-stu-id="03cea-231">Requests are queued until the source is started.</span></span> |
| <span data-ttu-id="03cea-232">Arrêté.</span><span class="sxs-lookup"><span data-stu-id="03cea-232">Stopped.</span></span> | <span data-ttu-id="03cea-233">La source rejette les exemples de demandes.</span><span class="sxs-lookup"><span data-stu-id="03cea-233">The source rejects sample requests.</span></span>                                                                             |



 

### <a name="start"></a><span data-ttu-id="03cea-234">Démarrer</span><span class="sxs-lookup"><span data-stu-id="03cea-234">Start</span></span>

<span data-ttu-id="03cea-235">La méthode [**IMFMediaSource :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) démarre la source du média.</span><span class="sxs-lookup"><span data-stu-id="03cea-235">The [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method starts the media source.</span></span> <span data-ttu-id="03cea-236">Les paramètres suivants sont pris en compte :</span><span class="sxs-lookup"><span data-stu-id="03cea-236">It takes the following parameters:</span></span>

-   <span data-ttu-id="03cea-237">Descripteur de présentation.</span><span class="sxs-lookup"><span data-stu-id="03cea-237">A presentation descriptor.</span></span>
-   <span data-ttu-id="03cea-238">GUID de format d’heure.</span><span class="sxs-lookup"><span data-stu-id="03cea-238">A time-format GUID.</span></span>
-   <span data-ttu-id="03cea-239">Position de départ.</span><span class="sxs-lookup"><span data-stu-id="03cea-239">A start position.</span></span>

<span data-ttu-id="03cea-240">L’application doit obtenir le descripteur de présentation en appelant [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) sur la source.</span><span class="sxs-lookup"><span data-stu-id="03cea-240">The application must obtain the presentation descriptor by calling [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) on the source.</span></span> <span data-ttu-id="03cea-241">Il n’existe aucun mécanisme défini pour valider un descripteur de présentation.</span><span class="sxs-lookup"><span data-stu-id="03cea-241">There is no defined mechanism for validating a presentation descriptor.</span></span> <span data-ttu-id="03cea-242">Si l’application spécifie un descripteur de présentation incorrect, les résultats ne sont pas définis.</span><span class="sxs-lookup"><span data-stu-id="03cea-242">If the application specifies the wrong presentation descriptor, the results are undefined.</span></span>

<span data-ttu-id="03cea-243">Le GUID de format de temps spécifie comment interpréter la position de départ.</span><span class="sxs-lookup"><span data-stu-id="03cea-243">The time-format GUID specifies how to interpret the starting position.</span></span> <span data-ttu-id="03cea-244">Le format standard est de 100-nanosecondes (NS) unités, indiquées par la \_ valeur Guid null.</span><span class="sxs-lookup"><span data-stu-id="03cea-244">The standard format is 100-nanosecond (ns) units, indicated by GUID\_NULL.</span></span> <span data-ttu-id="03cea-245">Chaque source de média doit prendre en charge les unités 100-ns.</span><span class="sxs-lookup"><span data-stu-id="03cea-245">Every media source must support 100-ns units.</span></span> <span data-ttu-id="03cea-246">Éventuellement, une source peut prendre en charge d’autres unités de temps, telles que le nombre d’images ou le code de temps.</span><span class="sxs-lookup"><span data-stu-id="03cea-246">Optionally, a source can support other units of time, such as frame number or time code.</span></span> <span data-ttu-id="03cea-247">Toutefois, il n’existe pas de méthode standard pour interroger une source de média pour obtenir la liste des formats de temps qu’elle prend en charge.</span><span class="sxs-lookup"><span data-stu-id="03cea-247">However, there is no standard way to query a media source for the list of time formats it supports.</span></span>

<span data-ttu-id="03cea-248">La position de début est fournie en tant que **PROPVARIANT**, ce qui permet d’obtenir des types de données différents en fonction du format d’heure.</span><span class="sxs-lookup"><span data-stu-id="03cea-248">The start position is given as a **PROPVARIANT**, allowing for different data types depending on the time format.</span></span> <span data-ttu-id="03cea-249">Pour 100-ns, le type **PROPVARIANT** est à la fois **VT \_ i8** ou **VT \_ vide**.</span><span class="sxs-lookup"><span data-stu-id="03cea-249">For 100-ns, the **PROPVARIANT** type is either **VT\_I8** or **VT\_EMPTY**.</span></span> <span data-ttu-id="03cea-250">Si **VT \_ i8**, **PROPVARIANT** contient la position de début dans les unités 100-ns.</span><span class="sxs-lookup"><span data-stu-id="03cea-250">If **VT\_I8**, the **PROPVARIANT** contains the start position in 100-ns units.</span></span> <span data-ttu-id="03cea-251">La valeur « **VT \_ vide** » a la signification spéciale « démarrer à la position actuelle ».</span><span class="sxs-lookup"><span data-stu-id="03cea-251">The value **VT\_EMPTY** has the special meaning "start at the current position."</span></span>

<span data-ttu-id="03cea-252">Implémentez la méthode [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) comme suit :</span><span class="sxs-lookup"><span data-stu-id="03cea-252">Implement the [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method as follows:</span></span>

1.  <span data-ttu-id="03cea-253">Valider les paramètres et l’État :</span><span class="sxs-lookup"><span data-stu-id="03cea-253">Validate parameters and state:</span></span>
    -   <span data-ttu-id="03cea-254">Recherchez les paramètres **null** .</span><span class="sxs-lookup"><span data-stu-id="03cea-254">Check for **NULL** parameters.</span></span>
    -   <span data-ttu-id="03cea-255">Vérifiez le GUID de format de l’heure.</span><span class="sxs-lookup"><span data-stu-id="03cea-255">Check the time-format GUID.</span></span> <span data-ttu-id="03cea-256">Si la valeur n’est pas valide, retourne le **\_ format d’heure MF E non \_ pris en \_ \_ charge**.</span><span class="sxs-lookup"><span data-stu-id="03cea-256">If the value is invalid, return **MF\_E\_UNSUPPORTED\_TIME\_FORMAT**.</span></span>
    -   <span data-ttu-id="03cea-257">Vérifiez le type de données du **PROPVARIANT** qui contient la position de début.</span><span class="sxs-lookup"><span data-stu-id="03cea-257">Check the data type of the **PROPVARIANT** that holds the start position.</span></span>
    -   <span data-ttu-id="03cea-258">Validez la position de départ.</span><span class="sxs-lookup"><span data-stu-id="03cea-258">Validate the start position.</span></span> <span data-ttu-id="03cea-259">Si ce n’est pas le cas, retournez **MF \_ E \_ INVALIDREQUEST**.</span><span class="sxs-lookup"><span data-stu-id="03cea-259">If invalid, return **MF\_E\_INVALIDREQUEST**.</span></span>
    -   <span data-ttu-id="03cea-260">Si la source a été arrêtée, retourne **MF \_ E \_ Shutdown**.</span><span class="sxs-lookup"><span data-stu-id="03cea-260">If the source has been shut down, return **MF\_E\_SHUTDOWN**.</span></span>
2.  <span data-ttu-id="03cea-261">Si aucune erreur ne se produit à l’étape 1, met en file d’attente une opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="03cea-261">If no error occurs in step 1, queue an asynchronous operation.</span></span> <span data-ttu-id="03cea-262">Tout après cette étape se produit sur un thread de file d’attente de travail.</span><span class="sxs-lookup"><span data-stu-id="03cea-262">Everything after this step occurs on a work-queue thread.</span></span>
3.  <span data-ttu-id="03cea-263">Pour chaque flux :</span><span class="sxs-lookup"><span data-stu-id="03cea-263">For each stream:</span></span>
    1.  <span data-ttu-id="03cea-264">Vérifiez si le flux est déjà actif à partir d’une demande de [**démarrage**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) précédente.</span><span class="sxs-lookup"><span data-stu-id="03cea-264">Check if the stream is already active from a previous [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) request.</span></span>
    2.  <span data-ttu-id="03cea-265">Appelez [**IMFPresentationDescriptor :: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) pour vérifier si l’application a sélectionné ou désélectionné le flux.</span><span class="sxs-lookup"><span data-stu-id="03cea-265">Call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) to check whether the application selected or deselected the stream.</span></span>
    3.  <span data-ttu-id="03cea-266">Si un flux précédemment sélectionné est désélectionné, videz les exemples non remis pour ce flux.</span><span class="sxs-lookup"><span data-stu-id="03cea-266">If a previously selected stream is now deselected, flush any undelivered samples for that stream.</span></span>
    4.  <span data-ttu-id="03cea-267">Si le flux est actif, la source du média (pas le flux) envoie l’un des événements suivants :</span><span class="sxs-lookup"><span data-stu-id="03cea-267">If the stream is active, the media source (not the stream) sends one of the following events:</span></span>
        -   <span data-ttu-id="03cea-268">Elle envoie [MEUpdatedStream](meupdatedstream.md) si le flux était précédemment actif.</span><span class="sxs-lookup"><span data-stu-id="03cea-268">It sends [MEUpdatedStream](meupdatedstream.md) if the stream was previously active.</span></span>
        -   <span data-ttu-id="03cea-269">Sinon, elle envoie [MENewStream](menewstream.md).</span><span class="sxs-lookup"><span data-stu-id="03cea-269">Otherwise, it sends [MENewStream](menewstream.md).</span></span>

        <span data-ttu-id="03cea-270">Pour les deux événements, les données d’événement sont le pointeur [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) pour le flux.</span><span class="sxs-lookup"><span data-stu-id="03cea-270">For both events, the event data is the [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) pointer for the stream.</span></span>
    5.  <span data-ttu-id="03cea-271">Si la source redémarre à partir de l’état suspendu, des exemples de demandes sont peut-être en attente.</span><span class="sxs-lookup"><span data-stu-id="03cea-271">If the source is restarting from the paused state, there might be pending sample requests.</span></span> <span data-ttu-id="03cea-272">Si c’est le cas, fournissez-les maintenant.</span><span class="sxs-lookup"><span data-stu-id="03cea-272">If so, deliver these now.</span></span>
    6.  <span data-ttu-id="03cea-273">Si la source recherche une nouvelle position, chaque objet de flux envoie un événement [MEStreamSeeked](mestreamseeked.md) .</span><span class="sxs-lookup"><span data-stu-id="03cea-273">If the source is seeking to a new position, each stream object sends an [MEStreamSeeked](mestreamseeked.md) event.</span></span> <span data-ttu-id="03cea-274">Dans le cas contraire, chaque flux envoie un événement [MEStreamStarted](mestreamstarted.md) .</span><span class="sxs-lookup"><span data-stu-id="03cea-274">Otherwise, each stream sends an [MEStreamStarted](mestreamstarted.md) event.</span></span>
4.  <span data-ttu-id="03cea-275">Si la source recherche une nouvelle position, la source du média envoie un événement [MESourceSeeked](mesourceseeked.md) .</span><span class="sxs-lookup"><span data-stu-id="03cea-275">If the source is seeking to a new position, the media source sends an [MESourceSeeked](mesourceseeked.md) event.</span></span> <span data-ttu-id="03cea-276">Sinon, elle envoie un événement [MESourceStarted](mesourcestarted.md) .</span><span class="sxs-lookup"><span data-stu-id="03cea-276">Otherwise, it sends an [MESourceStarted](mesourcestarted.md) event.</span></span>

<span data-ttu-id="03cea-277">Si une erreur se produit à tout moment après l’étape 2, la source envoie un événement [MESourceStarted](mesourcestarted.md) avec un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="03cea-277">If an error occurs at any time after step 2, the source sends an [MESourceStarted](mesourcestarted.md) event with an error code.</span></span> <span data-ttu-id="03cea-278">Cette alerte signale à l’application que la méthode [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) a échoué de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="03cea-278">This alerts the application that the [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method failed asynchronously.</span></span>

<span data-ttu-id="03cea-279">Le code suivant illustre les étapes 1 à 2 :</span><span class="sxs-lookup"><span data-stu-id="03cea-279">The following code shows steps 1–2:</span></span>


```C++
HRESULT MPEG1Source::Start(
        IMFPresentationDescriptor* pPresentationDescriptor,
        const GUID* pguidTimeFormat,
        const PROPVARIANT* pvarStartPos
    )
{

    HRESULT hr = S_OK;
    SourceOp *pAsyncOp = NULL;

    // Check parameters.

    // Start position and presentation descriptor cannot be NULL.
    if (pvarStartPos == NULL || pPresentationDescriptor == NULL)
    {
        return E_INVALIDARG;
    }

    // Check the time format.
    if ((pguidTimeFormat != NULL) && (*pguidTimeFormat != GUID_NULL))
    {
        // Unrecognized time format GUID.
        return MF_E_UNSUPPORTED_TIME_FORMAT;
    }

    // Check the data type of the start position.
    if ((pvarStartPos->vt != VT_I8) && (pvarStartPos->vt != VT_EMPTY))
    {
        return MF_E_UNSUPPORTED_TIME_FORMAT;
    }

    EnterCriticalSection(&m_critSec);

    // Check if this is a seek request. This sample does not support seeking.

    if (pvarStartPos->vt == VT_I8)
    {
        // If the current state is STOPPED, then position 0 is valid.
        // Otherwise, the start position must be VT_EMPTY (current position).

        if ((m_state != STATE_STOPPED) || (pvarStartPos->hVal.QuadPart != 0))
        {
            hr = MF_E_INVALIDREQUEST;
            goto done;
        }
    }

    // Fail if the source is shut down.
    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    // Fail if the source was not initialized yet.
    hr = IsInitialized();
    if (FAILED(hr))
    {
        goto done;
    }

    // Perform a basic check on the caller's presentation descriptor.
    hr = ValidatePresentationDescriptor(pPresentationDescriptor);
    if (FAILED(hr))
    {
        goto done;
    }

    // The operation looks OK. Complete the operation asynchronously.
    hr = SourceOp::CreateStartOp(pPresentationDescriptor, &pAsyncOp);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAsyncOp->SetData(*pvarStartPos);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = QueueOperation(pAsyncOp);

done:
    SafeRelease(&pAsyncOp);
    LeaveCriticalSection(&m_critSec);
    return hr;
}
```



<span data-ttu-id="03cea-280">Les étapes restantes sont présentées dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="03cea-280">The remaining steps are shown in the next example:</span></span>


```C++
HRESULT MPEG1Source::DoStart(StartOp *pOp)
{
    assert(pOp->Op() == SourceOp::OP_START);

    IMFPresentationDescriptor *pPD = NULL;
    IMFMediaEvent  *pEvent = NULL;

    HRESULT     hr = S_OK;
    LONGLONG    llStartOffset = 0;
    BOOL        bRestartFromCurrentPosition = FALSE;
    BOOL        bSentEvents = FALSE;

    hr = BeginAsyncOp(pOp);

    // Get the presentation descriptor from the SourceOp object.
    // This is the PD that the caller passed into the Start() method.
    // The PD has already been validated.
    if (SUCCEEDED(hr))
    {
        hr = pOp->GetPresentationDescriptor(&pPD);
    }

    // Because this sample does not support seeking, the start
    // position must be 0 (from stopped) or "current position."

    // If the sample supported seeking, we would need to get the
    // start position from the PROPVARIANT data contained in pOp.

    if (SUCCEEDED(hr))
    {
        // Select/deselect streams, based on what the caller set in the PD.
        // This method also sends the MENewStream/MEUpdatedStream events.
        hr = SelectStreams(pPD, pOp->Data());
    }

    if (SUCCEEDED(hr))
    {
        m_state = STATE_STARTED;

        // Queue the "started" event. The event data is the start position.
        hr = m_pEventQueue->QueueEventParamVar(
            MESourceStarted,
            GUID_NULL,
            S_OK,
            &pOp->Data()
            );
    }

    if (FAILED(hr))
    {
        // Failure. Send the error code to the application.

        // Note: It's possible that QueueEvent itself failed, in which case it
        // is likely to fail again. But there is no good way to recover in
        // that case.

        (void)m_pEventQueue->QueueEventParamVar(
            MESourceStarted, GUID_NULL, hr, NULL);
    }

    CompleteAsyncOp(pOp);

    SafeRelease(&pEvent);
    SafeRelease(&pPD);
    return hr;
}
```



### <a name="pause"></a><span data-ttu-id="03cea-281">Suspendre</span><span class="sxs-lookup"><span data-stu-id="03cea-281">Pause</span></span>

<span data-ttu-id="03cea-282">La méthode [**IMFMediaSource ::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) interrompt la source du média.</span><span class="sxs-lookup"><span data-stu-id="03cea-282">The [**IMFMediaSource::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) method pauses the media source.</span></span> <span data-ttu-id="03cea-283">Implémentez cette méthode comme suit :</span><span class="sxs-lookup"><span data-stu-id="03cea-283">Implement this method as follows:</span></span>

1.  <span data-ttu-id="03cea-284">Met en file d’attente une opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="03cea-284">Queue an asynchronous operation.</span></span>
2.  <span data-ttu-id="03cea-285">Chaque flux actif envoie un événement [MEStreamPaused](mestreampaused.md) .</span><span class="sxs-lookup"><span data-stu-id="03cea-285">Each active stream sends an [MEStreamPaused](mestreampaused.md) event.</span></span>
3.  <span data-ttu-id="03cea-286">La source du média envoie un événement [MESourcePaused](mesourcepaused.md) .</span><span class="sxs-lookup"><span data-stu-id="03cea-286">The media source sends an [MESourcePaused](mesourcepaused.md) event.</span></span>

<span data-ttu-id="03cea-287">Pendant la suspension, la source met en file d’attente les exemples de demandes sans les traiter.</span><span class="sxs-lookup"><span data-stu-id="03cea-287">While paused, the source queues sample requests without processing them.</span></span> <span data-ttu-id="03cea-288">(Consultez [exemples de demandes](#sample-requests).)</span><span class="sxs-lookup"><span data-stu-id="03cea-288">(See [Sample Requests](#sample-requests).)</span></span>

### <a name="stop"></a><span data-ttu-id="03cea-289">Arrêter</span><span class="sxs-lookup"><span data-stu-id="03cea-289">Stop</span></span>

<span data-ttu-id="03cea-290">La méthode [**IMFMediaSource :: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) arrête la source du média.</span><span class="sxs-lookup"><span data-stu-id="03cea-290">The [**IMFMediaSource::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) method stops the media source.</span></span> <span data-ttu-id="03cea-291">Implémentez cette méthode comme suit :</span><span class="sxs-lookup"><span data-stu-id="03cea-291">Implement this method as follows:</span></span>

1.  <span data-ttu-id="03cea-292">Met en file d’attente une opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="03cea-292">Queue an asynchronous operation.</span></span>
2.  <span data-ttu-id="03cea-293">Chaque flux actif envoie un événement [MEStreamStopped](mestreamstopped.md) .</span><span class="sxs-lookup"><span data-stu-id="03cea-293">Each active stream sends an [MEStreamStopped](mestreamstopped.md) event.</span></span>
3.  <span data-ttu-id="03cea-294">Effacez tous les échantillons en file d’attente et les exemples de demandes.</span><span class="sxs-lookup"><span data-stu-id="03cea-294">Clear all queued samples and sample requests.</span></span>
4.  <span data-ttu-id="03cea-295">La source du média envoie un événement [MESourceStopped](mesourcestopped.md) .</span><span class="sxs-lookup"><span data-stu-id="03cea-295">The media source sends an [MESourceStopped](mesourcestopped.md) event.</span></span>

<span data-ttu-id="03cea-296">Lorsqu’il est arrêté, la source rejette toutes les demandes pour les exemples.</span><span class="sxs-lookup"><span data-stu-id="03cea-296">While stopped, the source rejects all requests for samples.</span></span>

<span data-ttu-id="03cea-297">Si la source est arrêtée alors qu’une demande d’e/s est en cours, la requête d’e/s peut se terminer une fois que la source passe à l’état arrêté.</span><span class="sxs-lookup"><span data-stu-id="03cea-297">If the source is stopped while an I/O request is in progress, the I/O request might complete after the source enters the stopped state.</span></span> <span data-ttu-id="03cea-298">Dans ce cas, la source doit ignorer le résultat de cette requête d’e/s.</span><span class="sxs-lookup"><span data-stu-id="03cea-298">In that case, the source should discard the result of that I/O request.</span></span>

## <a name="sample-requests"></a><span data-ttu-id="03cea-299">Exemple de demande</span><span class="sxs-lookup"><span data-stu-id="03cea-299">Sample Requests</span></span>

<span data-ttu-id="03cea-300">Media Foundation utiliser un modèle d' *extraction* , dans lequel le pipeline demande des exemples à partir de la source du média.</span><span class="sxs-lookup"><span data-stu-id="03cea-300">Media Foundation use a *pull* model, in which the pipeline requests samples from the media source.</span></span> <span data-ttu-id="03cea-301">Cela diffère du modèle utilisé par DirectShow, dans lequel les « push » sont des exemples.</span><span class="sxs-lookup"><span data-stu-id="03cea-301">This differs from the model used by DirectShow, in which the sources "pushes" samples.</span></span>

<span data-ttu-id="03cea-302">Pour demander un nouvel exemple, le pipeline Media Foundation appelle [**IMFMediaStream :: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample).</span><span class="sxs-lookup"><span data-stu-id="03cea-302">To request a new sample, the Media Foundation pipeline calls [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample).</span></span> <span data-ttu-id="03cea-303">Cette méthode prend un pointeur **IUnknown** qui représente un objet de *jeton* .</span><span class="sxs-lookup"><span data-stu-id="03cea-303">This method takes an **IUnknown** pointer that represents a *token* object.</span></span> <span data-ttu-id="03cea-304">L’implémentation de l’objet de jeton est jusqu’à l’appelant ; Il permet simplement à l’appelant de suivre les exemples de demandes.</span><span class="sxs-lookup"><span data-stu-id="03cea-304">The implementation of the token object is up to the caller; it simply provides a way for the caller to track sample requests.</span></span> <span data-ttu-id="03cea-305">Le paramètre token peut également avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="03cea-305">The token parameter can also be **NULL**.</span></span>

<span data-ttu-id="03cea-306">En supposant que la source utilise des demandes d’e/s asynchrones pour lire les données, l’exemple de génération ne sera pas synchronisé avec les exemples de demandes.</span><span class="sxs-lookup"><span data-stu-id="03cea-306">Assuming the source uses asynchronous I/O requests to read data, sample generation will not be synchronized with sample requests.</span></span> <span data-ttu-id="03cea-307">Pour synchroniser les exemples de demandes avec l’exemple de génération, une source de média effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="03cea-307">To synchronize sample requests with sample generation, a media source does the following:</span></span>

1.  <span data-ttu-id="03cea-308">Les jetons de demande sont placés dans une file d’attente.</span><span class="sxs-lookup"><span data-stu-id="03cea-308">Request tokens are placed on a queue.</span></span>
2.  <span data-ttu-id="03cea-309">À mesure que des exemples sont générés, ils sont placés sur une deuxième file d’attente.</span><span class="sxs-lookup"><span data-stu-id="03cea-309">As samples are generated, they are placed on a second queue.</span></span>
3.  <span data-ttu-id="03cea-310">La source du média termine un exemple de demande en extrayant un jeton de demande de la première file d’attente et un échantillon de la deuxième file d’attente.</span><span class="sxs-lookup"><span data-stu-id="03cea-310">The media source completes a sample request by pulling a request token from the first queue and a sample from the second queue.</span></span>
4.  <span data-ttu-id="03cea-311">La source du média envoie un événement MEMediaSample.</span><span class="sxs-lookup"><span data-stu-id="03cea-311">The media source sends an MEMediaSample event.</span></span> <span data-ttu-id="03cea-312">L’événement contient un pointeur vers l’exemple et l’exemple contient un pointeur vers le jeton.</span><span class="sxs-lookup"><span data-stu-id="03cea-312">The event contains a pointer to the sample, and the sample contains a pointer to the token.</span></span>

<span data-ttu-id="03cea-313">Le diagramme suivant montre la relation entre l’événement [MEMediaSample](memediasample.md) , l’exemple et le jeton de demande.</span><span class="sxs-lookup"><span data-stu-id="03cea-313">The following diagram shows the relationship between the [MEMediaSample](memediasample.md) event, the sample, and the request token.</span></span>

![Diagramme montrant memediasample et un exemple de file d’attente pointant vers imfsample ; imfsample et la file d’attente de demandes pointent vers IUnknown](images/mediasourceimpl01.png)

<span data-ttu-id="03cea-315">L’exemple de source MPEG-1 implémente ce processus comme suit :</span><span class="sxs-lookup"><span data-stu-id="03cea-315">The example MPEG-1 source implements this process as follows:</span></span>

1.  <span data-ttu-id="03cea-316">La méthode [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) place la demande sur une file d’attente FIFO.</span><span class="sxs-lookup"><span data-stu-id="03cea-316">The [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method puts the request on a FIFO queue.</span></span>
2.  <span data-ttu-id="03cea-317">À mesure que les demandes d’e/s sont terminées, la source du média crée de nouveaux exemples et les place dans une deuxième file d’attente FIFO.</span><span class="sxs-lookup"><span data-stu-id="03cea-317">As I/O requests are completed, the media source creates new samples and puts them on a second FIFO queue.</span></span> <span data-ttu-id="03cea-318">(Cette file d’attente a une taille maximale, afin d’éviter que la source ne lise trop loin.)</span><span class="sxs-lookup"><span data-stu-id="03cea-318">(This queue has a maximum size, to prevent the source from reading too far ahead.)</span></span>
3.  <span data-ttu-id="03cea-319">Lorsque ces deux files d’attente ont au moins un élément (une demande et un exemple), la source du média termine la première requête de la file d’attente de demandes en envoyant le premier échantillon de la file d’attente de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="03cea-319">Whenever both of these queues have at least one item (one request and one sample), the media source completes the first request from the request queue by sending out the first sample from the sample queue.</span></span>
4.  <span data-ttu-id="03cea-320">Pour remettre un exemple, l’objet de flux (et non l’objet source) envoie un événement [MEMediaSample](memediasample.md) .</span><span class="sxs-lookup"><span data-stu-id="03cea-320">To deliver a sample, the stream object (not the source object) sends an [MEMediaSample](memediasample.md) event.</span></span>
    -   <span data-ttu-id="03cea-321">Les données d’événement sont un pointeur vers l’interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="03cea-321">The event data is a pointer to the sample's [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface.</span></span>
    -   <span data-ttu-id="03cea-322">Si la demande incluait un jeton, attachez le jeton à l’exemple en définissant l’attribut de [**\_ jeton MFSampleExtension**](mfsampleextension-token-attribute.md) sur l’exemple.</span><span class="sxs-lookup"><span data-stu-id="03cea-322">If the request included a token, attach the token to the sample by setting the [**MFSampleExtension\_Token**](mfsampleextension-token-attribute.md) attribute on the sample.</span></span>

<span data-ttu-id="03cea-323">À ce stade, il existe trois possibilités :</span><span class="sxs-lookup"><span data-stu-id="03cea-323">At this point, there are three possibilities:</span></span>

-   <span data-ttu-id="03cea-324">Il existe un autre échantillon dans la file d’attente de l’exemple, mais aucune demande correspondante.</span><span class="sxs-lookup"><span data-stu-id="03cea-324">There is another sample in the sample queue, but no matching request.</span></span>
-   <span data-ttu-id="03cea-325">Il existe une demande, mais pas d’exemple.</span><span class="sxs-lookup"><span data-stu-id="03cea-325">There is a request, but no sample.</span></span>
-   <span data-ttu-id="03cea-326">Les deux files d’attente sont vides ; Il n’y a aucun échantillon et aucune demande.</span><span class="sxs-lookup"><span data-stu-id="03cea-326">Both queues are empty; there are no samples and no requests.</span></span>

<span data-ttu-id="03cea-327">Si la file d’attente de l’exemple est vide, la source vérifie la fin du flux (voir la [fin du flux](#end-of-stream)).</span><span class="sxs-lookup"><span data-stu-id="03cea-327">If the sample queue is empty, the source checks for the end of the stream (see [End of Stream](#end-of-stream)).</span></span> <span data-ttu-id="03cea-328">Dans le cas contraire, elle démarre une autre demande d’e/s de données.</span><span class="sxs-lookup"><span data-stu-id="03cea-328">Otherwise, it starts another I/O request for data.</span></span> <span data-ttu-id="03cea-329">Si une erreur se produit pendant ce processus, le flux envoie un événement [MEError](meerror.md) .</span><span class="sxs-lookup"><span data-stu-id="03cea-329">If any error occurs during this process, the stream sends an [MEError](meerror.md) event.</span></span>

<span data-ttu-id="03cea-330">Le code suivant implémente la méthode [**IMFMediaStream :: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) :</span><span class="sxs-lookup"><span data-stu-id="03cea-330">The following code implements the [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method:</span></span>


```C++
HRESULT MPEG1Stream::RequestSample(IUnknown* pToken)
{
    HRESULT hr = S_OK;
    IMFMediaSource *pSource = NULL;

    // Hold the media source object's critical section.
    SourceLock lock(m_pSource);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    if (m_state == STATE_STOPPED)
    {
        hr = MF_E_INVALIDREQUEST;
        goto done;
    }

    if (!m_bActive)
    {
        // If the stream is not active, it should not get sample requests.
        hr = MF_E_INVALIDREQUEST;
        goto done;
    }

    if (m_bEOS && m_Samples.IsEmpty())
    {
        // This stream has already reached the end of the stream, and the
        // sample queue is empty.
        hr = MF_E_END_OF_STREAM;
        goto done;
    }

    hr = m_Requests.InsertBack(pToken);
    if (FAILED(hr))
    {
        goto done;
    }

    // Dispatch the request.
    hr = DispatchSamples();
    if (FAILED(hr))
    {
        goto done;
    }

done:
    if (FAILED(hr) && (m_state != STATE_SHUTDOWN))
    {
        // An error occurred. Send an MEError even from the source,
        // unless the source is already shut down.
        hr = m_pSource->QueueEvent(MEError, GUID_NULL, hr, NULL);
    }
    return hr;
}
```



<span data-ttu-id="03cea-331">La `DispatchSamples` méthode extrait des exemples de la file d’attente de l’exemple, les met en correspondance avec des exemples de demandes en attente et met en file d’attente les événements [MEMediaSample](memediasample.md) :</span><span class="sxs-lookup"><span data-stu-id="03cea-331">The `DispatchSamples` method pulls samples from the sample queue, matches them with pending sample requests, and queues [MEMediaSample](memediasample.md) events:</span></span>


```C++
HRESULT MPEG1Stream::DispatchSamples()
{
    HRESULT hr = S_OK;
    BOOL bNeedData = FALSE;
    BOOL bEOS = FALSE;

    SourceLock lock(m_pSource);

    // An I/O request can complete after the source is paused, stopped, or
    // shut down. Do not deliver samples unless the source is running.
    if (m_state != STATE_STARTED)
    {
        return S_OK;
    }

    IMFSample *pSample = NULL;
    IUnknown  *pToken = NULL;

    // Deliver as many samples as we can.
    while (!m_Samples.IsEmpty() && !m_Requests.IsEmpty())
    {
        // Pull the next sample from the queue.
        hr = m_Samples.RemoveFront(&pSample);
        if (FAILED(hr))
        {
            goto done;
        }

        // Pull the next request token from the queue. Tokens can be NULL.
        hr = m_Requests.RemoveFront(&pToken);
        if (FAILED(hr))
        {
            goto done;
        }

        if (pToken)
        {
            // Set the token on the sample.
            hr = pSample->SetUnknown(MFSampleExtension_Token, pToken);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        // Send an MEMediaSample event with the sample.
        hr = m_pEventQueue->QueueEventParamUnk(
            MEMediaSample, GUID_NULL, S_OK, pSample);

        if (FAILED(hr))
        {
            goto done;
        }

        SafeRelease(&pSample);
        SafeRelease(&pToken);
    }

    if (m_Samples.IsEmpty() && m_bEOS)
    {
        // The sample queue is empty AND we have reached the end of the source
        // stream. Notify the pipeline by sending the end-of-stream event.

        hr = m_pEventQueue->QueueEventParamVar(
            MEEndOfStream, GUID_NULL, S_OK, NULL);

        if (FAILED(hr))
        {
            goto done;
        }

        // Notify the source. It will send the end-of-presentation event.
        hr = m_pSource->QueueAsyncOperation(SourceOp::OP_END_OF_STREAM);
        if (FAILED(hr))
        {
            goto done;
        }
    }
    else if (NeedsData())
    {
        // The sample queue is empty; the request queue is not empty; and we
        // have not reached the end of the stream. Ask for more data.
        hr = m_pSource->QueueAsyncOperation(SourceOp::OP_REQUEST_DATA);
        if (FAILED(hr))
        {
            goto done;
        }
    }

done:
    if (FAILED(hr) && (m_state != STATE_SHUTDOWN))
    {
        // An error occurred. Send an MEError even from the source,
        // unless the source is already shut down.
        m_pSource->QueueEvent(MEError, GUID_NULL, hr, NULL);
    }

    SafeRelease(&pSample);
    SafeRelease(&pToken);
    return S_OK;
}
```



<span data-ttu-id="03cea-332">La `DispatchSamples` méthode est appelée dans les circonstances suivantes :</span><span class="sxs-lookup"><span data-stu-id="03cea-332">The `DispatchSamples` method is called in the following circumstances:</span></span>

-   <span data-ttu-id="03cea-333">À l’intérieur de la méthode [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .</span><span class="sxs-lookup"><span data-stu-id="03cea-333">Inside the [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method.</span></span>
-   <span data-ttu-id="03cea-334">Lorsque la source du média redémarre à partir de l’état suspendu.</span><span class="sxs-lookup"><span data-stu-id="03cea-334">When the media source restarts from the paused state.</span></span>
-   <span data-ttu-id="03cea-335">Quand une demande d’e/s se termine.</span><span class="sxs-lookup"><span data-stu-id="03cea-335">When an I/O request completes.</span></span>

## <a name="end-of-stream"></a><span data-ttu-id="03cea-336">Fin de flux</span><span class="sxs-lookup"><span data-stu-id="03cea-336">End of Stream</span></span>

<span data-ttu-id="03cea-337">Lorsqu’un flux ne contient plus de données et que tous les exemples de ce flux ont été remis, les objets de flux envoient un événement [MEEndOfStream](meendofstream.md) .</span><span class="sxs-lookup"><span data-stu-id="03cea-337">When a stream has no more data, and all of the samples for that stream have been delivered, the stream objects sends an [MEEndOfStream](meendofstream.md) event.</span></span>

<span data-ttu-id="03cea-338">Lorsque tous les flux actifs sont terminés, la source du média envoie un événement [MEEndOfPresentation](meendofpresentation.md) .</span><span class="sxs-lookup"><span data-stu-id="03cea-338">When all of the active streams are done, the media source sends an [MEEndOfPresentation](meendofpresentation.md) event.</span></span>

## <a name="asynchronous-operations"></a><span data-ttu-id="03cea-339">Opérations asynchrones</span><span class="sxs-lookup"><span data-stu-id="03cea-339">Asynchronous Operations</span></span>

<span data-ttu-id="03cea-340">La partie la plus difficile de l’écriture d’une source de média est peut-être la compréhension du modèle asynchrone Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="03cea-340">Perhaps the hardest part of writing a media source is understanding the Media Foundation asynchronous model.</span></span>

<span data-ttu-id="03cea-341">Toutes les méthodes sur une source multimédia qui contrôlent la diffusion en continu sont asynchrones.</span><span class="sxs-lookup"><span data-stu-id="03cea-341">All of the methods on a media source that control streaming are asynchronous.</span></span> <span data-ttu-id="03cea-342">Dans chaque cas, la méthode effectue une validation initiale, telle que la vérification des paramètres.</span><span class="sxs-lookup"><span data-stu-id="03cea-342">In each case, the method does some initial validation, such as checking parameters.</span></span> <span data-ttu-id="03cea-343">La source distribue ensuite le reste du travail à une file d’attente de travail.</span><span class="sxs-lookup"><span data-stu-id="03cea-343">The source then dispatches the rest of the work to a work queue.</span></span> <span data-ttu-id="03cea-344">Une fois l’opération terminée, la source du média renvoie un événement à l’appelant, via l’interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) de la source du média.</span><span class="sxs-lookup"><span data-stu-id="03cea-344">After the operation completes, the media source sends an event back to the caller, through the media source's [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="03cea-345">Il est donc important de comprendre les files d’attente de travail.</span><span class="sxs-lookup"><span data-stu-id="03cea-345">It is therefore important to understand work queues.</span></span>

<span data-ttu-id="03cea-346">Pour placer un élément dans une file d’attente de travail, vous pouvez appeler [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) ou [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex).</span><span class="sxs-lookup"><span data-stu-id="03cea-346">To put an item on a work queue, you can call either [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) or [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex).</span></span> <span data-ttu-id="03cea-347">La source MPEG-1 utilise **MFPutWorkItem**, mais les deux fonctions font la même chose.</span><span class="sxs-lookup"><span data-stu-id="03cea-347">The MPEG-1 source happens to use **MFPutWorkItem**, but the two functions do the same thing.</span></span> <span data-ttu-id="03cea-348">La fonction **MFPutWorkItem** accepte les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="03cea-348">The **MFPutWorkItem** function takes the following parameters:</span></span>

-   <span data-ttu-id="03cea-349">Valeur **DWORD** qui identifie la file d’attente de travail.</span><span class="sxs-lookup"><span data-stu-id="03cea-349">A **DWORD** value that identifies the work queue.</span></span> <span data-ttu-id="03cea-350">Vous pouvez créer une file d’attente de travail privée ou utiliser la **\_ \_ \_ norme de file d’attente de rappel MFASYNC**.</span><span class="sxs-lookup"><span data-stu-id="03cea-350">You can create a private work queue or use **MFASYNC\_CALLBACK\_QUEUE\_STANDARD**.</span></span>
-   <span data-ttu-id="03cea-351">Pointeur vers l’interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="03cea-351">A pointer to the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span> <span data-ttu-id="03cea-352">Cette interface de rappel est appelée pour effectuer le travail.</span><span class="sxs-lookup"><span data-stu-id="03cea-352">This callback interface is invoked to perform the work.</span></span>
-   <span data-ttu-id="03cea-353">Objet d’État facultatif, qui doit implémenter **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="03cea-353">An optional state object, which must implement **IUnknown**.</span></span>

<span data-ttu-id="03cea-354">La file d’attente de travail est desservie par un ou plusieurs threads de travail qui extraient en permanence l’élément de travail suivant de la file d’attente et appellent la méthode [**IMFAsyncCallback :: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) de l’interface de rappel.</span><span class="sxs-lookup"><span data-stu-id="03cea-354">The work queue is serviced by one or more worker threads that continuously pull the next work item from the queue and invoke the [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method of the callback interface.</span></span>

<span data-ttu-id="03cea-355">Il n’est pas garanti que les éléments de travail s’exécutent dans le même ordre que celui dans lequel ils sont placés dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="03cea-355">Work items are not guaranteed to execute in the same order that you put them on the queue.</span></span> <span data-ttu-id="03cea-356">N’oubliez pas que plusieurs threads peuvent traiter la même file d’attente de travail, de sorte que les appels [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) peuvent se chevaucher ou se produire dans le désordre.</span><span class="sxs-lookup"><span data-stu-id="03cea-356">Remember that more than one thread can service the same work queue, so [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) calls can overlap or occur out of order.</span></span> <span data-ttu-id="03cea-357">Par conséquent, il revient à la source du média de conserver l’état interne correct, en envoyant les éléments de la file d’attente de travail dans le bon ordre.</span><span class="sxs-lookup"><span data-stu-id="03cea-357">Therefore, it is up to the media source to maintain the correct internal state, by submitting work queue items in the right order.</span></span> <span data-ttu-id="03cea-358">La source démarre l’opération suivante uniquement lorsque l’opération précédente est terminée.</span><span class="sxs-lookup"><span data-stu-id="03cea-358">Only when the previous operation is complete does the source start the next operation.</span></span>

<span data-ttu-id="03cea-359">Pour représenter des opérations en attente, la source MPEG-1 définit une classe nommée `SourceOp` :</span><span class="sxs-lookup"><span data-stu-id="03cea-359">To represent pending operations, the MPEG-1 source defines a class named `SourceOp`:</span></span>


```C++
// Represents a request for an asynchronous operation.

class SourceOp : public IUnknown
{
public:

    enum Operation
    {
        OP_START,
        OP_PAUSE,
        OP_STOP,
        OP_REQUEST_DATA,
        OP_END_OF_STREAM
    };

    static HRESULT CreateOp(Operation op, SourceOp **ppOp);
    static HRESULT CreateStartOp(IMFPresentationDescriptor *pPD, SourceOp **ppOp);

    // IUnknown
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    SourceOp(Operation op);
    virtual ~SourceOp();

    HRESULT SetData(const PROPVARIANT& var);

    Operation Op() const { return m_op; }
    const PROPVARIANT& Data() { return m_data;}

protected:
    long        m_cRef;     // Reference count.
    Operation   m_op;
    PROPVARIANT m_data;     // Data for the operation.
};
```



<span data-ttu-id="03cea-360">L' `Operation` énumération identifie l’opération en attente.</span><span class="sxs-lookup"><span data-stu-id="03cea-360">The `Operation` enumeration identifies which operation is pending.</span></span> <span data-ttu-id="03cea-361">La classe contient également un **PROPVARIANT** pour transmettre des données supplémentaires pour l’opération.</span><span class="sxs-lookup"><span data-stu-id="03cea-361">The class also contains a **PROPVARIANT** to convey any additional data for the operation.</span></span>

### <a name="operation-queue"></a><span data-ttu-id="03cea-362">File d’attente des opérations</span><span class="sxs-lookup"><span data-stu-id="03cea-362">Operation Queue</span></span>

<span data-ttu-id="03cea-363">Pour sérialiser des opérations, la source du média gère une file d’attente d' `SourceOp` objets.</span><span class="sxs-lookup"><span data-stu-id="03cea-363">To serialize operations, the media source maintains a queue of `SourceOp` objects.</span></span> <span data-ttu-id="03cea-364">Elle utilise une classe d’assistance pour gérer la file d’attente :</span><span class="sxs-lookup"><span data-stu-id="03cea-364">It uses a helper class to manage the queue:</span></span>


```C++
template <class OP_TYPE>
class OpQueue : public IUnknown
{
public:

    typedef ComPtrList<OP_TYPE>   OpList;

    HRESULT QueueOperation(OP_TYPE *pOp);

protected:

    HRESULT ProcessQueue();
    HRESULT ProcessQueueAsync(IMFAsyncResult *pResult);

    virtual HRESULT DispatchOperation(OP_TYPE *pOp) = 0;
    virtual HRESULT ValidateOperation(OP_TYPE *pOp) = 0;

    OpQueue(CRITICAL_SECTION& critsec)
        : m_OnProcessQueue(this, &OpQueue::ProcessQueueAsync),
          m_critsec(critsec)
    {
    }

    virtual ~OpQueue()
    {
    }

protected:
    OpList                  m_OpQueue;         // Queue of operations.
    CRITICAL_SECTION&       m_critsec;         // Protects the queue state.
    AsyncCallback<OpQueue>  m_OnProcessQueue;  // ProcessQueueAsync callback.
};
```



<span data-ttu-id="03cea-365">La `OpQueue` classe est conçue pour être héritée par le composant qui exécute des éléments de travail asynchrones.</span><span class="sxs-lookup"><span data-stu-id="03cea-365">The `OpQueue` class is designed to be inherited by the component that performs asynchronous work items.</span></span> <span data-ttu-id="03cea-366">Le paramètre de modèle de *\_ type op* est le type d’objet utilisé pour représenter les éléments de travail dans la file d’attente. dans ce cas, le *\_ type d’opération* est `SourceOp` .</span><span class="sxs-lookup"><span data-stu-id="03cea-366">The *OP\_TYPE* template parameter is the object type used to represent work items in the queue—in this case, *OP\_TYPE* will be `SourceOp`.</span></span> <span data-ttu-id="03cea-367">La `OpQueue` classe implémente les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="03cea-367">The `OpQueue` class implements the following methods:</span></span>

-   <span data-ttu-id="03cea-368">`QueueOperation` place un nouvel élément dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="03cea-368">`QueueOperation` puts a new item on the queue.</span></span>
-   <span data-ttu-id="03cea-369">`ProcessQueue` distribue l’opération suivante à partir de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="03cea-369">`ProcessQueue` dispatches the next operation from the queue.</span></span> <span data-ttu-id="03cea-370">Cette méthode est asynchrone.</span><span class="sxs-lookup"><span data-stu-id="03cea-370">This method is asynchronous.</span></span>
-   <span data-ttu-id="03cea-371">`ProcessQueueAsync` termine la `ProcessQueue` méthode asynchrone.</span><span class="sxs-lookup"><span data-stu-id="03cea-371">`ProcessQueueAsync` completes the asynchronous `ProcessQueue` method.</span></span>

<span data-ttu-id="03cea-372">Les deux autres méthodes doivent être implémentées par la classe dérivée :</span><span class="sxs-lookup"><span data-stu-id="03cea-372">Another two methods must be implemented by the derived class:</span></span>

-   <span data-ttu-id="03cea-373">`ValidateOperation` vérifie s’il est valide d’effectuer une opération spécifiée, en fonction de l’état actuel de la source du média.</span><span class="sxs-lookup"><span data-stu-id="03cea-373">`ValidateOperation` checks whether it is valid to perform a specified operation, given the current state of the media source.</span></span>
-   <span data-ttu-id="03cea-374">`DispatchOperation` exécute l’élément de travail asynchrone.</span><span class="sxs-lookup"><span data-stu-id="03cea-374">`DispatchOperation` carries out the asynchronous work item.</span></span>

<span data-ttu-id="03cea-375">La file d’attente des opérations est utilisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="03cea-375">The operation queue is used as follows:</span></span>

1.  <span data-ttu-id="03cea-376">Le pipeline Media Foundation appelle une méthode asynchrone sur la source du média, par exemple [**IMFMediaSource :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span><span class="sxs-lookup"><span data-stu-id="03cea-376">The Media Foundation pipeline calls an asynchronous method on the media source, such as [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span></span>
2.  <span data-ttu-id="03cea-377">La méthode asynchrone appelle `QueueOperation` , qui place l’opération [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) sur la file d’attente et appelle `ProcessQueue` (sous la forme d’un `SourceOp` objet).</span><span class="sxs-lookup"><span data-stu-id="03cea-377">The asynchronous method calls `QueueOperation`, which puts the [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) operation on the queue and calls `ProcessQueue` (in the form of a `SourceOp` object).</span></span>
3.  <span data-ttu-id="03cea-378">`ProcessQueue` appelle [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem).</span><span class="sxs-lookup"><span data-stu-id="03cea-378">`ProcessQueue` calls [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem).</span></span>
4.  <span data-ttu-id="03cea-379">Le thread de file d’attente de travail appelle `ProcessQueueAsync` .</span><span class="sxs-lookup"><span data-stu-id="03cea-379">The work-queue thread calls `ProcessQueueAsync`.</span></span>
5.  <span data-ttu-id="03cea-380">La `ProcessQueueAsync` méthode appelle `ValidateOperation` et `DispatchOperation` .</span><span class="sxs-lookup"><span data-stu-id="03cea-380">The `ProcessQueueAsync` method calls `ValidateOperation` and `DispatchOperation`.</span></span>

<span data-ttu-id="03cea-381">Le code suivant met en file d’attente une nouvelle opération sur la source MPEG-1 :</span><span class="sxs-lookup"><span data-stu-id="03cea-381">The following code queues a new operation on the MPEG-1 source:</span></span>


```C++
template <class OP_TYPE>
HRESULT OpQueue<OP_TYPE>::QueueOperation(OP_TYPE *pOp)
{
    HRESULT hr = S_OK;

    EnterCriticalSection(&m_critsec);

    hr = m_OpQueue.InsertBack(pOp);
    if (SUCCEEDED(hr))
    {
        hr = ProcessQueue();
    }

    LeaveCriticalSection(&m_critsec);
    return hr;
}
```



<span data-ttu-id="03cea-382">Le code suivant traite la file d’attente :</span><span class="sxs-lookup"><span data-stu-id="03cea-382">The following code processes the queue:</span></span>


```C++
template <class OP_TYPE>
HRESULT OpQueue<OP_TYPE>::ProcessQueue()
{
    HRESULT hr = S_OK;
    if (m_OpQueue.GetCount() > 0)
    {
        hr = MFPutWorkItem(
            MFASYNC_CALLBACK_QUEUE_STANDARD,    // Use the standard work queue.
            &m_OnProcessQueue,                  // Callback method.
            NULL                                // State object.
            );
    }
    return hr;
}
```



<span data-ttu-id="03cea-383">La `ValidateOperation` méthode vérifie si la source MPEG-1 peut distribuer la prochaine opération dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="03cea-383">The `ValidateOperation` method checks whether the MPEG-1 source can dispatch the next operation in the queue.</span></span> <span data-ttu-id="03cea-384">Si une autre opération est en cours, `ValidateOperation` retourne **MF \_ E \_ NOTACCEPTING**.</span><span class="sxs-lookup"><span data-stu-id="03cea-384">If another operation is in progress, `ValidateOperation` returns **MF\_E\_NOTACCEPTING**.</span></span> <span data-ttu-id="03cea-385">Cela permet de `DispatchOperation` s’assurer que n’est pas appelé alors qu’une autre opération est en attente.</span><span class="sxs-lookup"><span data-stu-id="03cea-385">This ensures that `DispatchOperation` is not called while there is another operation pending.</span></span>


```C++
HRESULT MPEG1Source::ValidateOperation(SourceOp *pOp)
{
    if (m_pCurrentOp != NULL)
    {
        return MF_E_NOTACCEPTING;
    }
    return S_OK;
}
```



<span data-ttu-id="03cea-386">La méthode DispatchOperation bascule sur le type d’opération :</span><span class="sxs-lookup"><span data-stu-id="03cea-386">The DispatchOperation method switches on the operation type:</span></span>


```C++
//-------------------------------------------------------------------
// DispatchOperation
//
// Performs the asynchronous operation indicated by pOp.
//
// NOTE:
// This method implements the pure-virtual OpQueue::DispatchOperation
// method. It is always called from a work-queue thread.
//-------------------------------------------------------------------

HRESULT MPEG1Source::DispatchOperation(SourceOp *pOp)
{
    EnterCriticalSection(&m_critSec);

    HRESULT hr = S_OK;

    if (m_state == STATE_SHUTDOWN)
    {
        LeaveCriticalSection(&m_critSec);

        return S_OK; // Already shut down, ignore the request.
    }

    switch (pOp->Op())
    {

    // IMFMediaSource methods:

    case SourceOp::OP_START:
        hr = DoStart((StartOp*)pOp);
        break;

    case SourceOp::OP_STOP:
        hr = DoStop(pOp);
        break;

    case SourceOp::OP_PAUSE:
        hr = DoPause(pOp);
        break;

    // Operations requested by the streams:

    case SourceOp::OP_REQUEST_DATA:
        hr = OnStreamRequestSample(pOp);
        break;

    case SourceOp::OP_END_OF_STREAM:
        hr = OnEndOfStream(pOp);
        break;

    default:
        hr = E_UNEXPECTED;
    }

    if (FAILED(hr))
    {
        StreamingError(hr);
    }

    LeaveCriticalSection(&m_critSec);
    return hr;
}
```



<span data-ttu-id="03cea-387">Pour récapituler :</span><span class="sxs-lookup"><span data-stu-id="03cea-387">To summarize:</span></span>

1.  <span data-ttu-id="03cea-388">Le pipeline appelle une méthode asynchrone, telle que [**IMFMediaSource :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span><span class="sxs-lookup"><span data-stu-id="03cea-388">The pipeline calls an asynchronous method, such as [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span></span>
2.  <span data-ttu-id="03cea-389">La méthode asynchrone appelle `OpQueue::QueueOperation` , en passant un pointeur vers un `SourceOp` objet.</span><span class="sxs-lookup"><span data-stu-id="03cea-389">The asynchronous method calls `OpQueue::QueueOperation`, passing in a pointer to a `SourceOp` object.</span></span>
3.  <span data-ttu-id="03cea-390">La `QueueOperation` méthode place l’opération sur la file d’attente *m \_ OpQueue* et appelle `OpQueue::ProcessQueue` .</span><span class="sxs-lookup"><span data-stu-id="03cea-390">The `QueueOperation` method puts the operation on the *m\_OpQueue* queue and calls `OpQueue::ProcessQueue`.</span></span>
4.  <span data-ttu-id="03cea-391">La `ProcessQueue` méthode appelle [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem).</span><span class="sxs-lookup"><span data-stu-id="03cea-391">The `ProcessQueue` method calls [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem).</span></span> <span data-ttu-id="03cea-392">À partir de ce stade, tout se produit sur un thread de file d’attente de travail Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="03cea-392">From this point, everything happens on a Media Foundation work-queue thread.</span></span> <span data-ttu-id="03cea-393">La méthode asynchrone retourne à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="03cea-393">The asynchronous method returns to the caller.</span></span>
5.  <span data-ttu-id="03cea-394">Le thread de file d’attente de travail appelle la `OpQueue::ProcessQueueAsync` méthode.</span><span class="sxs-lookup"><span data-stu-id="03cea-394">The work-queue thread calls the `OpQueue::ProcessQueueAsync` method.</span></span>
6.  <span data-ttu-id="03cea-395">La `ProcessQueueAsync` méthode appelle `MPEG1Source:ValidateOperation` pour valider l’opération.</span><span class="sxs-lookup"><span data-stu-id="03cea-395">The `ProcessQueueAsync` method calls `MPEG1Source:ValidateOperation` to validate the operation.</span></span>
7.  <span data-ttu-id="03cea-396">La `ProcessQueueAsync` méthode appelle `MPEG1Source::DispatchOperation` pour traiter l’opération.</span><span class="sxs-lookup"><span data-stu-id="03cea-396">The `ProcessQueueAsync` method calls `MPEG1Source::DispatchOperation` to process the operation.</span></span>

<span data-ttu-id="03cea-397">Cette conception présente plusieurs avantages :</span><span class="sxs-lookup"><span data-stu-id="03cea-397">There are several benefits to this design:</span></span>

-   <span data-ttu-id="03cea-398">Les méthodes étant asynchrones, elles ne bloquent pas le thread de l’application appelante.</span><span class="sxs-lookup"><span data-stu-id="03cea-398">Methods are asynchronous, so they do not block the calling application's thread.</span></span>
-   <span data-ttu-id="03cea-399">Les opérations sont distribuées sur un thread de file d’attente de travail Media Foundation, qui est partagé entre les composants de pipeline.</span><span class="sxs-lookup"><span data-stu-id="03cea-399">Operations are dispatched on a Media Foundation work-queue thread, which is shared among pipeline components.</span></span> <span data-ttu-id="03cea-400">Par conséquent, la source du média ne crée pas son propre thread, ce qui réduit le nombre total de threads créés.</span><span class="sxs-lookup"><span data-stu-id="03cea-400">Therefore, the media source does not create its own thread, reducing the total number of threads that are created.</span></span>
-   <span data-ttu-id="03cea-401">La source du média n’est pas bloquée en attendant la fin des opérations.</span><span class="sxs-lookup"><span data-stu-id="03cea-401">The media source does not block while waiting for operations to complete.</span></span> <span data-ttu-id="03cea-402">Cela réduit le risque qu’une source de média provoque accidentellement un blocage et contribue à réduire le basculement de contexte.</span><span class="sxs-lookup"><span data-stu-id="03cea-402">This reduces the chance that a media source will accidentally cause a deadlock, and helps to reduce context switching.</span></span>
-   <span data-ttu-id="03cea-403">La source du média peut utiliser des e/s asynchrones pour lire le fichier source (en appelant [**IMFByteStream :: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread)).</span><span class="sxs-lookup"><span data-stu-id="03cea-403">The media source can use asynchronous I/O to read the source file (by calling [**IMFByteStream::BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread)).</span></span> <span data-ttu-id="03cea-404">La source du média n’a pas besoin d’être bloquée en attendant la fin de la routine d’e/s.</span><span class="sxs-lookup"><span data-stu-id="03cea-404">The media source does not need to block while waiting for I/O routine complete.</span></span>

<span data-ttu-id="03cea-405">Si vous suivez le modèle présenté dans l’exemple du kit de développement logiciel (SDK), vous pouvez vous concentrer sur les détails spécifiques de la source du média.</span><span class="sxs-lookup"><span data-stu-id="03cea-405">If you follow the pattern shown in the SDK sample, you can focus on the particular details of your media source.</span></span>

## <a name="related-topics"></a><span data-ttu-id="03cea-406">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="03cea-406">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03cea-407">Sources multimédias</span><span class="sxs-lookup"><span data-stu-id="03cea-407">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="03cea-408">Écriture d’une source de média personnalisée</span><span class="sxs-lookup"><span data-stu-id="03cea-408">Writing a Custom Media Source</span></span>](writing-a-custom-media-source.md)
</dt> </dl>

 

 



