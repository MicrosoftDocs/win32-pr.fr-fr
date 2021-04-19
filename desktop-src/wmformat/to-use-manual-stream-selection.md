---
title: Pour utiliser la sélection manuelle de flux
description: Pour utiliser la sélection manuelle de flux
ms.assetid: 49ec283f-670a-4a0e-9477-c60a80919a1e
keywords:
- ASF (Advanced Systems Format), sélection manuelle des flux
- ASF (format des systèmes avancés), sélection manuelle des flux
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), sélection de flux
- ASF (format de systèmes avancés), sélection de flux
- ASF (Advanced Systems Format), exclusion mutuelle
- ASF (format des systèmes avancés), exclusion mutuelle
- lecteurs asynchrones, sélection manuelle de flux
- lecteurs asynchrones, sélection de flux
- flux, sélection manuelle
- exclusion mutuelle, sélection de flux manuelle
- flux, lecteurs asynchrones
- exclusion mutuelle, lecteurs asynchrones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87c493bc8f41bc2a03ba15832ed402939adbeff
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106513510"
---
# <a name="to-use-manual-stream-selection"></a><span data-ttu-id="ef4f6-117">Pour utiliser la sélection manuelle de flux</span><span class="sxs-lookup"><span data-stu-id="ef4f6-117">To Use Manual Stream Selection</span></span>

<span data-ttu-id="ef4f6-118">Lorsque vous fournissez des exemples non compressés avec l’objet Reader, vous pouvez les remettre uniquement par numéro de sortie.</span><span class="sxs-lookup"><span data-stu-id="ef4f6-118">When delivering uncompressed samples with the reader object, you can deliver them only by output number.</span></span> <span data-ttu-id="ef4f6-119">Dans le cas de flux mutuellement exclusifs, cela signifie que vous ne pouvez recevoir des exemples qu’à partir d’un flux de l’exclusion mutuelle à la fois.</span><span class="sxs-lookup"><span data-stu-id="ef4f6-119">In the case of mutually exclusive streams, this means that you can receive samples only from one stream in the mutual exclusion at a time.</span></span> <span data-ttu-id="ef4f6-120">Le processus qui consiste à choisir le flux mutuellement exclusif à remettre est appelé « sélection de flux ».</span><span class="sxs-lookup"><span data-stu-id="ef4f6-120">The process of choosing which mutually exclusive stream to deliver is called stream selection.</span></span>

<span data-ttu-id="ef4f6-121">Pour l’exclusion mutuelle de la vitesse de transmission, le lecteur effectue automatiquement des sélections de flux en fonction des conditions sur l’ordinateur hôte lors de la lecture.</span><span class="sxs-lookup"><span data-stu-id="ef4f6-121">For bit-rate mutual exclusion, the reader makes stream selections automatically based on the conditions on the host machine at playback.</span></span> <span data-ttu-id="ef4f6-122">Pour les autres types d’exclusion mutuelle, le lecteur fournit des exemples à partir du flux par défaut, sauf si vous sélectionnez manuellement un autre flux.</span><span class="sxs-lookup"><span data-stu-id="ef4f6-122">For other types of mutual exclusion, the reader will deliver samples from the default stream unless you manually select a different stream yourself.</span></span> <span data-ttu-id="ef4f6-123">Il peut également y avoir des instances lorsque vous souhaitez sélectionner un flux manuellement à partir d’une exclusion mutuelle à vitesse de transmission.</span><span class="sxs-lookup"><span data-stu-id="ef4f6-123">There may also be instances when you want to select a stream manually from a bit-rate mutual exclusion.</span></span>

<span data-ttu-id="ef4f6-124">La sélection manuelle des flux est activée ou désactivée pour l’ensemble du fichier.</span><span class="sxs-lookup"><span data-stu-id="ef4f6-124">Manual stream selection is either on or off for the entire file.</span></span> <span data-ttu-id="ef4f6-125">Si un fichier contient une exclusion mutuelle à vitesse de transmission et d’autres types d’exclusion mutuelle, vous devez sélectionner manuellement les flux basés sur la vitesse de transmission.</span><span class="sxs-lookup"><span data-stu-id="ef4f6-125">If a file contains bit-rate mutual exclusion and some other mutual exclusion type, you must select the bit rate based streams manually.</span></span>

<span data-ttu-id="ef4f6-126">Pour sélectionner manuellement un flux qui s’exclue mutuellement, vous devez effectuer les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="ef4f6-126">To select a mutually exclusive stream manually, you must perform the following steps.</span></span>

1.  <span data-ttu-id="ef4f6-127">Récupérez un pointeur vers l’interface [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) de l’objet lecteur en appelant **IWMReader :: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="ef4f6-127">Retrieve a pointer to the [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
2.  <span data-ttu-id="ef4f6-128">Activez la sélection manuelle des flux en appelant [**IWMReaderAdvanced :: SetManualStreamSelection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection).</span><span class="sxs-lookup"><span data-stu-id="ef4f6-128">Enable manual stream selection by calling [**IWMReaderAdvanced::SetManualStreamSelection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection).</span></span>
3.  <span data-ttu-id="ef4f6-129">Pour déterminer si un flux particulier est sélectionné, appelez [**IWMReaderAdvanced :: GetStreamSelected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstreamselected).</span><span class="sxs-lookup"><span data-stu-id="ef4f6-129">To find out if a particular stream is selected, call [**IWMReaderAdvanced::GetStreamSelected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstreamselected).</span></span> <span data-ttu-id="ef4f6-130">Vous devez passer un pointeur vers une variable du type d’énumération de la [**\_ \_ sélection de flux WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_stream_selection) .</span><span class="sxs-lookup"><span data-stu-id="ef4f6-130">You must pass a pointer to a variable of the [**WMT\_STREAM\_SELECTION**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_stream_selection) enumeration type.</span></span> <span data-ttu-id="ef4f6-131">Lorsque l’appel est retourné, la valeur dans la variable décrit le type de sélection actuel du flux.</span><span class="sxs-lookup"><span data-stu-id="ef4f6-131">When the call returns, the value in the variable will describe the current selection type of the stream.</span></span>
4.  <span data-ttu-id="ef4f6-132">Pour sélectionner un flux, appelez [**IWMReaderAdvanced :: SetStreamsSelected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setstreamsselected).</span><span class="sxs-lookup"><span data-stu-id="ef4f6-132">To select a stream, call [**IWMReaderAdvanced::SetStreamsSelected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setstreamsselected).</span></span> <span data-ttu-id="ef4f6-133">Cette méthode vous permet de spécifier plusieurs flux en même temps pour le basculement de flux synchronisé.</span><span class="sxs-lookup"><span data-stu-id="ef4f6-133">This method enables you to specify multiple streams at the same time for synchronized stream switching.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef4f6-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ef4f6-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef4f6-135">**Lecture des fichiers avec le lecteur asynchrone**</span><span class="sxs-lookup"><span data-stu-id="ef4f6-135">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




