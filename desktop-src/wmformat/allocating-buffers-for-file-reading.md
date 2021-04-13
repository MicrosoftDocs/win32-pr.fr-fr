---
title: Allocation de tampons pour la lecture de fichiers
description: Allocation de tampons pour la lecture de fichiers
ms.assetid: da66ef5b-ec92-445c-90ba-5ee89e0def36
keywords:
- Windows Media Format SDK, lire des fichiers ASF
- Fichiers ASF (Advanced Systems Format), lecture des fichiers
- ASF (format des systèmes avancés), lire les fichiers
- Windows Media Format SDK, allouer des tampons
- ASF (Advanced Systems Format), allouer des tampons
- ASF (format de systèmes avancés), allouer des tampons
- ASF (Advanced Systems Format), allocation de mémoire tampon
- ASF (format de systèmes avancés), allocation de mémoire tampon
- allocation de mémoire tampon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecdf9ba0a333bbe25c94ec087911237b68f38f74
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381467"
---
# <a name="allocating-buffers-for-file-reading"></a><span data-ttu-id="90ea2-112">Allocation de tampons pour la lecture de fichiers</span><span class="sxs-lookup"><span data-stu-id="90ea2-112">Allocating Buffers for File Reading</span></span>

<span data-ttu-id="90ea2-113">Dans le scénario de lecture de fichiers le plus basique, les mémoires tampons utilisées pour fournir des exemples sont allouées par l’objet de lecture (l’objet lecteur ou l’objet lecteur synchrone).</span><span class="sxs-lookup"><span data-stu-id="90ea2-113">In the most basic file-reading scenario, the buffers used to deliver samples are allocated by the reading object (the reader object or the synchronous reader object).</span></span> <span data-ttu-id="90ea2-114">Toutefois, vous pouvez allouer vous-même des tampons.</span><span class="sxs-lookup"><span data-stu-id="90ea2-114">You can, however, allocate buffers yourself.</span></span> <span data-ttu-id="90ea2-115">Pour plus d’informations sur les avantages de l’allocation de vos propres tampons, consultez [prise en charge de l’exemple alloué](user-allocated-sample-support.md)par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="90ea2-115">For more information about the benefits of allocating your own buffers, see [User Allocated Sample Support](user-allocated-sample-support.md).</span></span>

<span data-ttu-id="90ea2-116">Pour utiliser vos propres mémoires tampons pour la lecture de fichiers, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="90ea2-116">To use your own buffers for file reading, perform the following steps.</span></span>

1.  <span data-ttu-id="90ea2-117">Implémentez un rappel ou des rappels pour que le lecteur appelle lorsqu’il a besoin d’une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="90ea2-117">Implement a callback or callbacks for the reader to call when it needs a buffer.</span></span> <span data-ttu-id="90ea2-118">Si vous lisez des exemples de sortie, utilisez [**IWMReaderAllocatorEx :: AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex).</span><span class="sxs-lookup"><span data-stu-id="90ea2-118">If you are reading output samples, use [**IWMReaderAllocatorEx::AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex).</span></span> <span data-ttu-id="90ea2-119">Si vous lisez des exemples de flux, utilisez [**IWMReaderAllocatorEx :: AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex).</span><span class="sxs-lookup"><span data-stu-id="90ea2-119">If you are reading stream samples, use [**IWMReaderAllocatorEx::AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex).</span></span> <span data-ttu-id="90ea2-120">Incluez la logique de gestion des mémoires tampon adaptée à votre application.</span><span class="sxs-lookup"><span data-stu-id="90ea2-120">Include whatever logic for managing buffers that suits your application.</span></span>
2.  <span data-ttu-id="90ea2-121">Allouez un pool de mémoires tampons que vous allez utiliser pour la lecture de fichiers.</span><span class="sxs-lookup"><span data-stu-id="90ea2-121">Allocate a pool of buffers that you will use for file reading.</span></span>
    -   <span data-ttu-id="90ea2-122">Recherchez la taille requise pour vos mémoires tampons en appelant [**IWMReaderAdvanced :: GetMaxOutputSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxoutputsamplesize) ou [**IWMReaderAdvanced :: GetMaxStreamSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxstreamsamplesize) pour chaque sortie et/ou flux pour lequel la mémoire tampon est utilisée.</span><span class="sxs-lookup"><span data-stu-id="90ea2-122">Find the size required for your buffers by calling [**IWMReaderAdvanced::GetMaxOutputSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxoutputsamplesize) or [**IWMReaderAdvanced::GetMaxStreamSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxstreamsamplesize) for each output and/or stream for which the buffer is used.</span></span> <span data-ttu-id="90ea2-123">Si vous utilisez le lecteur synchrone, utilisez [**IWMSyncReader :: GetMaxOutputSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxoutputsamplesize) ou [**IWMSyncReader :: GetMaxStreamSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxstreamsamplesize) à la place.</span><span class="sxs-lookup"><span data-stu-id="90ea2-123">If using the synchronous reader, use [**IWMSyncReader::GetMaxOutputSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxoutputsamplesize) or [**IWMSyncReader::GetMaxStreamSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxstreamsamplesize) instead.</span></span>
    -   <span data-ttu-id="90ea2-124">Créez chaque mémoire tampon pour le pool.</span><span class="sxs-lookup"><span data-stu-id="90ea2-124">Create each buffer for the pool.</span></span>
3.  <span data-ttu-id="90ea2-125">Configurez le lecteur ou le lecteur synchrone pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="90ea2-125">Set up the reader or synchronous reader for reading.</span></span> <span data-ttu-id="90ea2-126">Pour plus d’informations, consultez [lecture de fichiers avec le lecteur asynchrone](reading-files-with-the-asynchronous-reader.md) ou [lecture de fichiers avec le lecteur synchrone](reading-files-with-the-synchronous-reader.md).</span><span class="sxs-lookup"><span data-stu-id="90ea2-126">For more information see [Reading Files with the Asynchronous Reader](reading-files-with-the-asynchronous-reader.md) or [Reading Files with the Synchronous Reader](reading-files-with-the-synchronous-reader.md).</span></span>
4.  <span data-ttu-id="90ea2-127">Avant de commencer l’écriture, appelez [**IWMReaderAdvanced :: SetAllocateForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforoutput) ou [**IWMReaderAdvanced :: SetAllocateForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforstream) pour chaque sortie et flux pour lesquels vous allouez des tampons à l’aide de l’objet lecteur.</span><span class="sxs-lookup"><span data-stu-id="90ea2-127">Before beginning writing, call [**IWMReaderAdvanced::SetAllocateForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforoutput) or [**IWMReaderAdvanced::SetAllocateForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforstream) for each output and stream for which you are allocating buffers using the reader object.</span></span> <span data-ttu-id="90ea2-128">Pour le lecteur synchrone, appelez [**IWMSyncReader2 :: SetAllocateForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforoutput) ou [**IWMSyncReader2 :: SetAllocateForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforstream) à la place.</span><span class="sxs-lookup"><span data-stu-id="90ea2-128">For the synchronous reader, call [**IWMSyncReader2::SetAllocateForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforoutput) or [**IWMSyncReader2::SetAllocateForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforstream) instead.</span></span>
5.  <span data-ttu-id="90ea2-129">Commencez la lecture du fichier.</span><span class="sxs-lookup"><span data-stu-id="90ea2-129">Begin reading the file.</span></span>

<span data-ttu-id="90ea2-130">L’objet de lecture appelle le rappel d’allocateur approprié et récupère des exemples de votre application.</span><span class="sxs-lookup"><span data-stu-id="90ea2-130">The reading object will make calls to the appropriate allocator callback and get samples from your application.</span></span> <span data-ttu-id="90ea2-131">La logique de gestion de la mémoire tampon doit inclure un moyen de signaler qu’une mémoire tampon est libre d’être réutilisée.</span><span class="sxs-lookup"><span data-stu-id="90ea2-131">Your buffer management logic must include a way to signal that a buffer is free to be used again.</span></span> <span data-ttu-id="90ea2-132">En général, une mémoire tampon est replacée dans le pool lors du rendu de son contenu.</span><span class="sxs-lookup"><span data-stu-id="90ea2-132">Typically, a buffer is put back into the pool when its contents are rendered.</span></span> <span data-ttu-id="90ea2-133">Selon votre application, il se peut que vous ayez besoin de quelques tampons dans le pool ou un grand nombre.</span><span class="sxs-lookup"><span data-stu-id="90ea2-133">Depending upon your application, you may need just a few buffers in the pool or many.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90ea2-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="90ea2-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90ea2-135">**Lecture des fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="90ea2-135">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> </dl>

 

 




