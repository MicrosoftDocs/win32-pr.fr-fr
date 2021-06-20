---
description: Utilisez cet exemple pour comprendre comment l’encodeur RLE peut implémenter la méthode dans le cadre de l’écriture d’un filtre de transformation.
ms.assetid: b7d878ab-523f-4b52-b98d-c9d4fa18ce8a
title: Étape 5. Transformer l’image
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ac9d32e48ba438f8bde2d8d4d9aca3b827ebc0c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406782"
---
# <a name="step-5-transform-the-image"></a><span data-ttu-id="fb061-104">Étape 5.</span><span class="sxs-lookup"><span data-stu-id="fb061-104">Step 5.</span></span> <span data-ttu-id="fb061-105">Transformer l’image</span><span class="sxs-lookup"><span data-stu-id="fb061-105">Transform the Image</span></span>

<span data-ttu-id="fb061-106">Il s’agit de l’étape 5 du didacticiel [écriture de filtres de transformation](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="fb061-106">This is step 5 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="fb061-107">Le filtre en amont remet des échantillons de médias au filtre de transformation en appelant la méthode [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) sur la broche d’entrée du filtre de transformation.</span><span class="sxs-lookup"><span data-stu-id="fb061-107">The upstream filter delivers media samples to the transform filter by calling the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method on the transform filter's input pin.</span></span> <span data-ttu-id="fb061-108">Pour traiter les données, le filtre de transformation appelle la méthode de **transformation** , qui est virtuelle pure.</span><span class="sxs-lookup"><span data-stu-id="fb061-108">To process the data, the transform filter calls the **Transform** method, which is pure virtual.</span></span> <span data-ttu-id="fb061-109">Les classes **CTransformFilter** et **CTransInPlaceFilter** utilisent deux versions différentes de cette méthode :</span><span class="sxs-lookup"><span data-stu-id="fb061-109">The **CTransformFilter** and **CTransInPlaceFilter** classes use two different versions of this method:</span></span>

-   <span data-ttu-id="fb061-110">[**CTransformFilter :: Transform**](ctransformfilter-transform.md) accepte un pointeur vers l’exemple d’entrée et un pointeur vers l’exemple de sortie.</span><span class="sxs-lookup"><span data-stu-id="fb061-110">[**CTransformFilter::Transform**](ctransformfilter-transform.md) takes a pointer to the input sample and a pointer to the output sample.</span></span> <span data-ttu-id="fb061-111">Avant que le filtre appelle la méthode, il copie les exemples de propriétés de l’exemple d’entrée dans l’exemple de sortie, y compris les horodatages.</span><span class="sxs-lookup"><span data-stu-id="fb061-111">Before the filter calls the method, it copies the sample properties from the input sample to the output sample, including the time stamps.</span></span>
-   <span data-ttu-id="fb061-112">[**CTransInPlaceFilter :: Transform**](ctransinplacefilter-transform.md) accepte un pointeur vers l’exemple d’entrée.</span><span class="sxs-lookup"><span data-stu-id="fb061-112">[**CTransInPlaceFilter::Transform**](ctransinplacefilter-transform.md) takes a pointer to the input sample.</span></span> <span data-ttu-id="fb061-113">Le filtre modifie les données sur place.</span><span class="sxs-lookup"><span data-stu-id="fb061-113">The filter modifies the data in place.</span></span>

<span data-ttu-id="fb061-114">Si la méthode **Transform** retourne \_ la valeur OK, le filtre remet l’exemple en aval.</span><span class="sxs-lookup"><span data-stu-id="fb061-114">If the **Transform** method returns S\_OK, the filter delivers the sample downstream.</span></span> <span data-ttu-id="fb061-115">Pour ignorer un frame, renvoyez la \_ valeur false.</span><span class="sxs-lookup"><span data-stu-id="fb061-115">To skip a frame, return S\_FALSE.</span></span> <span data-ttu-id="fb061-116">En cas d’erreur de diffusion en continu, retourne un code d’échec.</span><span class="sxs-lookup"><span data-stu-id="fb061-116">If there is a streaming error, return a failure code.</span></span>

<span data-ttu-id="fb061-117">L’exemple suivant montre comment l’encodeur RLE peut implémenter cette méthode.</span><span class="sxs-lookup"><span data-stu-id="fb061-117">The following example shows how the RLE encoder might implement this method.</span></span> <span data-ttu-id="fb061-118">Votre propre implémentation peut varier considérablement, en fonction de ce que fait votre filtre.</span><span class="sxs-lookup"><span data-stu-id="fb061-118">Your own implementation might differ considerably, depending on what your filter does.</span></span>


```C++
HRESULT CRleFilter::Transform(IMediaSample *pSource, IMediaSample *pDest)
{
    // Get pointers to the underlying buffers.
    BYTE *pBufferIn, *pBufferOut;
    hr = pSource->GetPointer(&pBufferIn);
    if (FAILED(hr))
    {
        return hr;
    }
    hr = pDest->GetPointer(&pBufferOut);
    if (FAILED(hr))
    {
        return hr;
    }
    // Process the data.
    DWORD cbDest = EncodeFrame(pBufferIn, pBufferOut);
    KASSERT((long)cbDest <= pDest->GetSize());

    pDest->SetActualDataLength(cbDest);
    pDest->SetSyncPoint(TRUE);
    return S_OK;
}
```



<span data-ttu-id="fb061-119">Cet exemple suppose que EncodeFrame est une méthode privée qui implémente l’encodage RLE.</span><span class="sxs-lookup"><span data-stu-id="fb061-119">This example assumes that EncodeFrame is a private method that implements the RLE encoding.</span></span> <span data-ttu-id="fb061-120">L’algorithme d’encodage lui-même n’est pas décrit ici ; Pour plus d’informations, consultez la rubrique « compression bitmap » dans la documentation du kit de développement Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="fb061-120">The encoding algorithm itself is not described here; for details, see the topic "Bitmap Compression" in the Platform SDK documentation.</span></span>

<span data-ttu-id="fb061-121">Tout d’abord, l’exemple appelle [**IMediaSample :: GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) pour récupérer les adresses des mémoires tampons sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="fb061-121">First, the example calls [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) to retrieve the addresses of the underlying buffers.</span></span> <span data-ttu-id="fb061-122">Elle les transmet à la méthode EncoderFrame privée.</span><span class="sxs-lookup"><span data-stu-id="fb061-122">It passes these to the private EncoderFrame method.</span></span> <span data-ttu-id="fb061-123">Ensuite, il appelle [**IMediaSample :: SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) pour spécifier la longueur des données encodées.</span><span class="sxs-lookup"><span data-stu-id="fb061-123">Then it calls [**IMediaSample::SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) to specify the length of the encoded data.</span></span> <span data-ttu-id="fb061-124">Le filtre en aval a besoin de ces informations pour pouvoir gérer correctement la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="fb061-124">The downstream filter needs this information so that it can manage the buffer properly.</span></span> <span data-ttu-id="fb061-125">Enfin, la méthode appelle [**IMediaSample :: SetSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) pour définir l’indicateur d’image clé sur **true**.</span><span class="sxs-lookup"><span data-stu-id="fb061-125">Finally, the method calls [**IMediaSample::SetSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) to set the key frame flag to **TRUE**.</span></span> <span data-ttu-id="fb061-126">L’encodage de longueur d’exécution n’utilise pas d’images Delta, donc chaque frame est une image clé.</span><span class="sxs-lookup"><span data-stu-id="fb061-126">Run-length encoding does not use any delta frames, so every frame is a key frame.</span></span> <span data-ttu-id="fb061-127">Pour les images Delta, définissez la valeur sur **false**.</span><span class="sxs-lookup"><span data-stu-id="fb061-127">For delta frames, set the value to **FALSE**.</span></span>

<span data-ttu-id="fb061-128">Les autres problèmes que vous devez prendre en compte sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="fb061-128">Other issues that you must consider include:</span></span>

-   <span data-ttu-id="fb061-129">Horodatages.</span><span class="sxs-lookup"><span data-stu-id="fb061-129">Time stamps.</span></span> <span data-ttu-id="fb061-130">La classe **CTransformFilter** horodate l’exemple de sortie avant d’appeler la méthode **Transform** .</span><span class="sxs-lookup"><span data-stu-id="fb061-130">The **CTransformFilter** class timestamps the output sample before calling the **Transform** method.</span></span> <span data-ttu-id="fb061-131">Elle copie les valeurs d’horodatage de l’exemple d’entrée, sans les modifier.</span><span class="sxs-lookup"><span data-stu-id="fb061-131">It copies the time stamp values from the input sample, without modifying them.</span></span> <span data-ttu-id="fb061-132">Si votre filtre doit modifier les horodatages, appelez [**IMediaSample :: setTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) sur l’exemple de sortie.</span><span class="sxs-lookup"><span data-stu-id="fb061-132">If your filter needs to change the time stamps, call [**IMediaSample::SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) on the output sample.</span></span>
-   <span data-ttu-id="fb061-133">Modifications de format.</span><span class="sxs-lookup"><span data-stu-id="fb061-133">Format changes.</span></span> <span data-ttu-id="fb061-134">Le filtre amont peut modifier les formats Mid-Stream en attachant un type de média à l’exemple.</span><span class="sxs-lookup"><span data-stu-id="fb061-134">The upstream filter can change formats mid-stream by attaching a media type to the sample.</span></span> <span data-ttu-id="fb061-135">Avant cela, il appelle [**IPIN :: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sur la broche d’entrée de votre filtre.</span><span class="sxs-lookup"><span data-stu-id="fb061-135">Before doing so, it calls [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) on your filter's input pin.</span></span> <span data-ttu-id="fb061-136">Dans la classe **CTransformFilter** , cela entraîne un appel à **CheckInputType** suivi de **CheckTransform**.</span><span class="sxs-lookup"><span data-stu-id="fb061-136">In the **CTransformFilter** class, this results in a call to **CheckInputType** followed by **CheckTransform**.</span></span> <span data-ttu-id="fb061-137">Le filtre en aval peut également modifier les types de médias à l’aide du même mécanisme.</span><span class="sxs-lookup"><span data-stu-id="fb061-137">The downstream filter can also change media types, using the same mechanism.</span></span> <span data-ttu-id="fb061-138">Dans votre propre filtre, il y a deux choses à surveiller :</span><span class="sxs-lookup"><span data-stu-id="fb061-138">In your own filter, there are two things to watch for:</span></span>

    -   <span data-ttu-id="fb061-139">Assurez-vous que **QueryAccept** ne retourne pas les fausses acceptations.</span><span class="sxs-lookup"><span data-stu-id="fb061-139">Make sure that **QueryAccept** does not return false acceptances.</span></span>
    -   <span data-ttu-id="fb061-140">Si votre filtre accepte les modifications de format, vérifiez-les à l’intérieur de la méthode **Transform** en appelant [**IMediaSample :: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype).</span><span class="sxs-lookup"><span data-stu-id="fb061-140">If your filter does accept format changes, check for them inside the **Transform** method by calling [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype).</span></span> <span data-ttu-id="fb061-141">Si cette méthode retourne \_ la valeur OK, votre filtre doit répondre au changement de format.</span><span class="sxs-lookup"><span data-stu-id="fb061-141">If that method returns S\_OK, your filter must respond to the format change.</span></span>

    <span data-ttu-id="fb061-142">Pour plus d’informations, consultez [modifications de format dynamique](dynamic-format-changes.md).</span><span class="sxs-lookup"><span data-stu-id="fb061-142">For more information, see [Dynamic Format Changes](dynamic-format-changes.md).</span></span>

-   <span data-ttu-id="fb061-143">Thèmes.</span><span class="sxs-lookup"><span data-stu-id="fb061-143">Threads.</span></span> <span data-ttu-id="fb061-144">Dans **CTransformFilter** et **CTransInPlaceFilter**, le filtre de transformation remet les exemples de sortie de façon synchrone à l’intérieur de la méthode **Receive** .</span><span class="sxs-lookup"><span data-stu-id="fb061-144">In both **CTransformFilter** and **CTransInPlaceFilter**, the transform filter delivers output samples synchronously inside the **Receive** method.</span></span> <span data-ttu-id="fb061-145">Le filtre ne crée pas de threads de travail pour traiter les données.</span><span class="sxs-lookup"><span data-stu-id="fb061-145">The filter does not create any worker threads to process the data.</span></span> <span data-ttu-id="fb061-146">En règle générale, il n’y a aucune raison pour qu’un filtre de transformation crée des threads de travail.</span><span class="sxs-lookup"><span data-stu-id="fb061-146">Typically, there is no reason for a transform filter to create worker threads.</span></span>

<span data-ttu-id="fb061-147">Suivant : [étape 6. Ajoutez la prise en charge de COM](step-6--add-support-for-com.md).</span><span class="sxs-lookup"><span data-stu-id="fb061-147">Next: [Step 6. Add Support for COM](step-6--add-support-for-com.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb061-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fb061-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb061-149">Écriture de filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="fb061-149">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



