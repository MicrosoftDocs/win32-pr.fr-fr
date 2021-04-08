---
title: Pour distribuer des exemples compressés avec le lecteur asynchrone
description: Pour distribuer des exemples compressés avec le lecteur asynchrone
ms.assetid: 488baa3c-8863-4afc-89b2-fe55823e5db9
keywords:
- ASF (Advanced Systems Format), livrant des exemples compressés
- ASF (format avancé des systèmes), diffusion d’exemples compressés
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), exemples compressés
- ASF (Advanced Systems Format), exemples compressés
- lecteurs asynchrones, diffusion d’exemples compressés
- lecteurs asynchrones, exemples compressés
- exemples compressés, diffusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ce835075f5bd760014a3b1b776ba3627adb076
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723538"
---
# <a name="to-deliver-compressed-samples-with-the-asynchronous-reader"></a><span data-ttu-id="7526e-112">Pour distribuer des exemples compressés avec le lecteur asynchrone</span><span class="sxs-lookup"><span data-stu-id="7526e-112">To Deliver Compressed Samples with the Asynchronous Reader</span></span>

<span data-ttu-id="7526e-113">Le lecteur asynchrone peut fournir des échantillons compressés à partir de flux dans des fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="7526e-113">The asynchronous reader can deliver compressed samples from streams in ASF files.</span></span> <span data-ttu-id="7526e-114">Les applications fournissent généralement des exemples compressés lors de la copie d’un flux d’un fichier vers un autre.</span><span class="sxs-lookup"><span data-stu-id="7526e-114">Applications usually deliver compressed samples when copying a stream from one file to another.</span></span> <span data-ttu-id="7526e-115">Il n’est pas recommandé de recompresser les données qui ont été reconstruites à partir d’un flux compressé, car les données sont perdues dans le processus d’encodage.</span><span class="sxs-lookup"><span data-stu-id="7526e-115">It is not advisable to recompress data that has been reconstructed from a compressed stream, because data is lost in the encoding process.</span></span> <span data-ttu-id="7526e-116">Les médias numériques qui ont été compressés plusieurs fois auront une baisse notable de la qualité.</span><span class="sxs-lookup"><span data-stu-id="7526e-116">Digital media that has been compressed more than once will have a noticeable decrease in quality.</span></span>

<span data-ttu-id="7526e-117">Le kit de développement logiciel (SDK) Windows Media format ne fournit aucune méthode pour décoder les données après leur extraction à partir d’un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="7526e-117">The Windows Media Format SDK does not provide any methods for decoding data after it has been extracted from an ASF file.</span></span> <span data-ttu-id="7526e-118">Si vous recevez des exemples compressés et que vous souhaitez les décompresser ultérieurement, vous devrez fournir votre propre code pour ce faire.</span><span class="sxs-lookup"><span data-stu-id="7526e-118">If you receive compressed samples and later want to decompress them, you will have to provide your own code to do so.</span></span> <span data-ttu-id="7526e-119">Une façon de contourner cette limitation consiste à écrire les exemples compressés dans un nouveau fichier ASF, puis à les relire dans des exemples normaux et non compressés.</span><span class="sxs-lookup"><span data-stu-id="7526e-119">One way to get around this limitation is to write the compressed samples to a new ASF file and then re-read them into normal, uncompressed samples.</span></span>

<span data-ttu-id="7526e-120">Pour recevoir des exemples compressés avec le lecteur asynchrone, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="7526e-120">To receive compressed samples with the asynchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="7526e-121">Implémentez le rappel [**IWMReaderCallbackAdvanced :: OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) .</span><span class="sxs-lookup"><span data-stu-id="7526e-121">Implement the [**IWMReaderCallbackAdvanced::OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) callback.</span></span> <span data-ttu-id="7526e-122">Ce rappel est fondamentalement identique dans la fonction de [**IWMReaderCallback :: OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) , à ceci près qu’il fournit des échantillons par numéro de flux et que les exemples sont toujours compressés.</span><span class="sxs-lookup"><span data-stu-id="7526e-122">This callback is basically identical in function to [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) except that it delivers samples by stream number and the samples are still compressed.</span></span>
2.  <span data-ttu-id="7526e-123">Avant de commencer la lecture, obtenez un pointeur vers l’interface [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) de l’objet lecteur en appelant **IWMReader :: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="7526e-123">Before starting playback, obtain a pointer to the [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
3.  <span data-ttu-id="7526e-124">Configurez le lecteur pour remettre des exemples compressés pour le flux souhaité en appelant [**IWMReaderAdvanced :: SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples).</span><span class="sxs-lookup"><span data-stu-id="7526e-124">Configure the reader to deliver compressed samples for the desired stream by calling [**IWMReaderAdvanced::SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples).</span></span>
4.  <span data-ttu-id="7526e-125">Répétez l’étape 3 pour chaque flux pour lequel l’exemple de remise compressé est souhaité.</span><span class="sxs-lookup"><span data-stu-id="7526e-125">Repeat step 3 for each stream for which compressed sample delivery is desired.</span></span>

> [!Note]  
> <span data-ttu-id="7526e-126">Les flux d’images ne sont pas valides pour la remise du flux compressé.</span><span class="sxs-lookup"><span data-stu-id="7526e-126">Image streams are not valid for compressed stream delivery.</span></span> <span data-ttu-id="7526e-127">Si vous copiez un flux d’image d’un fichier vers un autre, il ne fonctionnera pas dans le nouveau fichier.</span><span class="sxs-lookup"><span data-stu-id="7526e-127">If you copy an image stream from one file to another, it will not work in the new file.</span></span> <span data-ttu-id="7526e-128">Pour copier un flux d’image à partir d’un fichier vers un fichier, récupérez les exemples de flux d’image par numéro de sortie et incluez-les dans le nouveau fichier comme si vous incluiez un nouveau flux d’image.</span><span class="sxs-lookup"><span data-stu-id="7526e-128">To copy an image stream from file to file, retrieve the image stream samples by output number and include them in the new file as if including a new image stream.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="7526e-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7526e-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7526e-130">**Interface IWMReaderCallbackAdvanced**</span><span class="sxs-lookup"><span data-stu-id="7526e-130">**IWMReaderCallbackAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced)
</dt> <dt>

[<span data-ttu-id="7526e-131">**Lecture des fichiers avec le lecteur asynchrone**</span><span class="sxs-lookup"><span data-stu-id="7526e-131">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




