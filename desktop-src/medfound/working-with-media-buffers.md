---
description: Utilisation des mémoires tampons de média
ms.assetid: c7e079e0-99f3-4bff-9163-1c5a022c14ae
title: Utilisation des mémoires tampons de média (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db63843ded32be6b1baa9c62e21a33f6563a43d5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103869545"
---
# <a name="working-with-media-buffers-microsoft-media-foundation"></a><span data-ttu-id="7b3ce-103">Utilisation des mémoires tampons de média (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="7b3ce-103">Working with Media Buffers (Microsoft Media Foundation)</span></span>

<span data-ttu-id="7b3ce-104">Cette rubrique explique comment utiliser l’interface [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) pour accéder aux données dans une mémoire tampon de média.</span><span class="sxs-lookup"><span data-stu-id="7b3ce-104">This topic describes how to use the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface to access the data in a media buffer.</span></span> <span data-ttu-id="7b3ce-105">Toutes les mémoires tampons de média exposent **IMFMediaBuffer**, qui est conçu pour tout type de données.</span><span class="sxs-lookup"><span data-stu-id="7b3ce-105">All media buffers expose **IMFMediaBuffer**, which is designed for any type of data.</span></span> <span data-ttu-id="7b3ce-106">Les images vidéo non compressées sont un cas particulier, décrit dans la rubrique [mémoires tampons vidéo non compressées](uncompressed-video-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="7b3ce-106">Uncompressed video frames are a special case, described in the topic [Uncompressed Video Buffers](uncompressed-video-buffers.md).</span></span>

## <a name="buffer-size"></a><span data-ttu-id="7b3ce-107">Taille de la mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="7b3ce-107">Buffer Size</span></span>

<span data-ttu-id="7b3ce-108">Une mémoire tampon de support est associée à deux tailles :</span><span class="sxs-lookup"><span data-stu-id="7b3ce-108">A media buffer has two sizes associated with it:</span></span>

-   <span data-ttu-id="7b3ce-109">La *longueur maximale* est la taille physique de la mémoire allouée pour la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="7b3ce-109">The *maximum length* is the physical size of the memory that is allocated for the buffer.</span></span> <span data-ttu-id="7b3ce-110">Cette valeur est définie lorsque la mémoire tampon est créée et ne change pas pendant la durée de vie de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="7b3ce-110">This value is set when the buffer is created and does not change during the lifetime of the buffer.</span></span> <span data-ttu-id="7b3ce-111">La longueur maximale indique la quantité de données pouvant être stockées dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="7b3ce-111">The maximum length indicates how much data can be stored in the buffer.</span></span> <span data-ttu-id="7b3ce-112">Pour trouver la taille maximale, appelez [**IMFMediaBuffer :: GetMaxLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getmaxlength).</span><span class="sxs-lookup"><span data-stu-id="7b3ce-112">To find the maximum size, call [**IMFMediaBuffer::GetMaxLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getmaxlength).</span></span>

-   <span data-ttu-id="7b3ce-113">La *longueur actuelle* correspond à la quantité de données valides actuellement dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="7b3ce-113">The *current length* is the amount of valid data that is currently in the buffer.</span></span> <span data-ttu-id="7b3ce-114">Lorsque la mémoire tampon est allouée pour la première fois, la longueur actuelle est égale à zéro, car il n’y a pas de données valides dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="7b3ce-114">When the buffer is first allocated, the current length is zero, because there is no valid data in the buffer.</span></span> <span data-ttu-id="7b3ce-115">Si vous écrivez des données dans la mémoire tampon, vous devez mettre à jour la longueur actuelle en appelant [**IMFMediaBuffer :: SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength).</span><span class="sxs-lookup"><span data-stu-id="7b3ce-115">If you write any data to the buffer, you must update the current length by calling [**IMFMediaBuffer::SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength).</span></span> <span data-ttu-id="7b3ce-116">Par exemple, si vous écrivez 100 octets de données dans la mémoire tampon, appelez **SetCurrentLength** avec la valeur 100.</span><span class="sxs-lookup"><span data-stu-id="7b3ce-116">For example, if you write 100 bytes of data into the buffer, call **SetCurrentLength** with the value 100.</span></span> <span data-ttu-id="7b3ce-117">Si vous lisez des données à partir d’une mémoire tampon de média, appelez [**IMFMediaBuffer :: GetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) pour connaître la quantité de données actuellement dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="7b3ce-117">If you read data from a media buffer, call [**IMFMediaBuffer::GetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) to find out how much data is currently in the buffer.</span></span> <span data-ttu-id="7b3ce-118">Ne pas lire au-delà de la longueur actuelle.</span><span class="sxs-lookup"><span data-stu-id="7b3ce-118">Do not read past the current length.</span></span> <span data-ttu-id="7b3ce-119">La longueur actuelle ne peut jamais dépasser la longueur maximale de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="7b3ce-119">The current length can never exceed the maximum length of the buffer.</span></span>

## <a name="accessing-the-buffer-memory"></a><span data-ttu-id="7b3ce-120">Accès à la mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="7b3ce-120">Accessing the Buffer Memory</span></span>

<span data-ttu-id="7b3ce-121">Pour accéder à la mémoire dans la mémoire tampon, appelez [**IMFMediaBuffer :: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock).</span><span class="sxs-lookup"><span data-stu-id="7b3ce-121">To access the memory in the buffer, call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock).</span></span> <span data-ttu-id="7b3ce-122">Cette méthode retourne un pointeur vers le début du bloc de mémoire.</span><span class="sxs-lookup"><span data-stu-id="7b3ce-122">This method returns a pointer to the start of the memory block.</span></span> <span data-ttu-id="7b3ce-123">Elle retourne également la longueur maximale et la longueur actuelle.</span><span class="sxs-lookup"><span data-stu-id="7b3ce-123">It also returns the maximum length and the current length.</span></span> <span data-ttu-id="7b3ce-124">Quand vous avez fini d’utiliser le pointeur, appelez [**IMFMediaBuffer :: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock).</span><span class="sxs-lookup"><span data-stu-id="7b3ce-124">When you are done using the pointer, call [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock).</span></span>

<span data-ttu-id="7b3ce-125">Pour écrire des données dans une mémoire tampon de média :</span><span class="sxs-lookup"><span data-stu-id="7b3ce-125">To write data into a media buffer:</span></span>

1.  <span data-ttu-id="7b3ce-126">Appelez [**IMFMediaBuffer :: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) pour obtenir un pointeur vers la mémoire.</span><span class="sxs-lookup"><span data-stu-id="7b3ce-126">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to get a pointer to the memory.</span></span> <span data-ttu-id="7b3ce-127">La méthode retourne également la longueur maximale de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="7b3ce-127">The method also returns the buffer's maximum length.</span></span>
2.  <span data-ttu-id="7b3ce-128">Écrivez vos données dans la mémoire, jusqu’à la longueur maximale de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="7b3ce-128">Write your data into the memory, up to the buffer's maximum length.</span></span>
3.  <span data-ttu-id="7b3ce-129">Appelez [**IMFMediaBuffer :: SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) pour mettre à jour la longueur actuelle.</span><span class="sxs-lookup"><span data-stu-id="7b3ce-129">Call [**IMFMediaBuffer::SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) to update the current length.</span></span> <span data-ttu-id="7b3ce-130">Définissez la longueur actuelle égale à la quantité de données que vous avez écrites à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="7b3ce-130">Set the current length equal to the amount of data that you wrote in step 2.</span></span>
4.  <span data-ttu-id="7b3ce-131">Appelez [**IMFMediaBuffer :: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) pour déverrouiller la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="7b3ce-131">Call [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) to unlock the buffer.</span></span>

<span data-ttu-id="7b3ce-132">Pour lire des données à partir d’une mémoire tampon de média :</span><span class="sxs-lookup"><span data-stu-id="7b3ce-132">To read data from a media buffer:</span></span>

1.  <span data-ttu-id="7b3ce-133">Appelez [**IMFMediaBuffer :: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) pour obtenir un pointeur vers la mémoire.</span><span class="sxs-lookup"><span data-stu-id="7b3ce-133">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to get a pointer to the memory.</span></span> <span data-ttu-id="7b3ce-134">La méthode retourne également la longueur actuelle de la mémoire tampon (la quantité de données valides dans la mémoire tampon).</span><span class="sxs-lookup"><span data-stu-id="7b3ce-134">The method also returns the buffer's current length (the amount of valid data in the buffer).</span></span>
2.  <span data-ttu-id="7b3ce-135">Lire le contenu de la mémoire, jusqu’à la longueur actuelle.</span><span class="sxs-lookup"><span data-stu-id="7b3ce-135">Read the contents of the memory, up to the current length.</span></span>
3.  <span data-ttu-id="7b3ce-136">Appelez [**IMFMediaBuffer :: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) pour déverrouiller la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="7b3ce-136">Call [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) to unlock the buffer.</span></span>

## <a name="creating-system-memory-buffers"></a><span data-ttu-id="7b3ce-137">Création de mémoires tampons système</span><span class="sxs-lookup"><span data-stu-id="7b3ce-137">Creating System Memory Buffers</span></span>

<span data-ttu-id="7b3ce-138">La mémoire tampon système est une mémoire tampon de média qui gère un bloc de mémoire système.</span><span class="sxs-lookup"><span data-stu-id="7b3ce-138">The system memory buffer is a media buffer that manages a block of system memory.</span></span> <span data-ttu-id="7b3ce-139">Pour créer une instance de cet objet, appelez [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) ou [**MFCreateAlignedMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatealignedmemorybuffer) et spécifiez une taille de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="7b3ce-139">To create an instance of this object, call [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) or [**MFCreateAlignedMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatealignedmemorybuffer) and specify a buffer size.</span></span> <span data-ttu-id="7b3ce-140">Les deux fonctions allouent un bloc de mémoire et retournent un pointeur [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .</span><span class="sxs-lookup"><span data-stu-id="7b3ce-140">Both functions allocate a block of memory and return an [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) pointer.</span></span> <span data-ttu-id="7b3ce-141">La mémoire est automatiquement libérée lorsque le nombre de références de la mémoire tampon du média atteint zéro et que l’objet est détruit.</span><span class="sxs-lookup"><span data-stu-id="7b3ce-141">The memory is automatically released when the media buffer's reference count reaches zero and the object is destroyed.</span></span>

<span data-ttu-id="7b3ce-142">L’exemple suivant montre comment créer une mémoire tampon système et écrire dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="7b3ce-142">The following example shows how to create a system memory buffer and write to the buffer.</span></span>


```C++
HRESULT CreateSystemMemoryBuffer(
    BYTE *pSrc, 
    DWORD cbData, 
    IMFMediaBuffer **ppBuffer
    )
{
    HRESULT hr = S_OK;
    BYTE *pData = NULL;

    IMFMediaBuffer *pBuffer = NULL;

    // Create the media buffer.
    hr = MFCreateMemoryBuffer(
        cbData,   // Amount of memory to allocate, in bytes.
        &pBuffer        
        );

    // Lock the buffer to get a pointer to the memory.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }

    if (SUCCEEDED(hr))
    {
        memcpy_s(pData, cbData, pSrc, cbData);
    }

    // Update the current length.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbData);
    }

    // Unlock the buffer.
    if (pData)
    {
        hr = pBuffer->Unlock();
    }

    if (SUCCEEDED(hr))
    {
        *ppBuffer = pBuffer;
        (*ppBuffer)->AddRef();
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="7b3ce-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7b3ce-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b3ce-144">Mémoires tampons de média</span><span class="sxs-lookup"><span data-stu-id="7b3ce-144">Media Buffers</span></span>](media-buffers.md)
</dt> <dt>

[<span data-ttu-id="7b3ce-145">API de plateforme Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7b3ce-145">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 



