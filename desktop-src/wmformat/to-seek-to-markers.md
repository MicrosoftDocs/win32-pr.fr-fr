---
title: Pour rechercher des marqueurs
description: Pour rechercher des marqueurs
ms.assetid: 2d5efebf-dcbd-4fb8-933e-cc6d3a99adf8
keywords:
- ASF (Advanced Systems Format), recherche de marqueurs
- ASF (format de systèmes avancés), recherche de marqueurs
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), marqueurs
- ASF (format des systèmes avancés), marqueurs
- lecteurs asynchrones, recherche de marqueurs
- lecteurs asynchrones, marqueurs
- marqueurs, recherche
- marqueurs, lecteurs asynchrones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16cb4fef99a5c735a12f03f8d2e962d6caf9c2a
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "106511672"
---
# <a name="to-seek-to-markers"></a><span data-ttu-id="73cb5-113">Pour rechercher des marqueurs</span><span class="sxs-lookup"><span data-stu-id="73cb5-113">To Seek to Markers</span></span>

<span data-ttu-id="73cb5-114">Un marqueur est un emplacement nommé dans un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="73cb5-114">A marker is a named location in an ASF file.</span></span> <span data-ttu-id="73cb5-115">Vous pouvez démarrer la lecture uniquement à partir de l’emplacement d’un marqueur en utilisant le lecteur asynchrone.</span><span class="sxs-lookup"><span data-stu-id="73cb5-115">You can only start playback from the location of a marker by using the asynchronous reader.</span></span> <span data-ttu-id="73cb5-116">Vous pouvez commencer la lecture sur un marqueur en procédant comme suit.</span><span class="sxs-lookup"><span data-stu-id="73cb5-116">You can begin playback at a marker by following these steps.</span></span>

1.  <span data-ttu-id="73cb5-117">Appelez **IWMReader :: QueryInterface** pour obtenir un pointeur vers l’interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) .</span><span class="sxs-lookup"><span data-stu-id="73cb5-117">Call **IWMReader::QueryInterface** to obtain a pointer to the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface.</span></span>
2.  <span data-ttu-id="73cb5-118">Récupérez le nombre total de marqueurs dans le fichier en appelant [**IWMHeaderInfo :: GetMarkerCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount).</span><span class="sxs-lookup"><span data-stu-id="73cb5-118">Retrieve the total number of markers in the file by calling [**IWMHeaderInfo::GetMarkerCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount).</span></span>
3.  <span data-ttu-id="73cb5-119">Parcourez les marqueurs à l’aide du nombre de marqueurs récupérés à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="73cb5-119">Loop through the markers, using the marker count retrieved in step 2.</span></span> <span data-ttu-id="73cb5-120">Récupérez le nom et l’heure de chaque marqueur en appelant [**IWMHeaderInfo :: GetMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) pour chacun d’entre eux.</span><span class="sxs-lookup"><span data-stu-id="73cb5-120">Retrieve the name and time of each marker by calling [**IWMHeaderInfo::GetMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) for each.</span></span> <span data-ttu-id="73cb5-121">Enregistrez l’index du marqueur souhaité.</span><span class="sxs-lookup"><span data-stu-id="73cb5-121">Save the index of the desired marker.</span></span>
4.  <span data-ttu-id="73cb5-122">Appelez **IWMReader :: QueryInterface** pour obtenir un pointeur vers l’interface [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) .</span><span class="sxs-lookup"><span data-stu-id="73cb5-122">Call **IWMReader::QueryInterface** to obtain a pointer to the [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) interface.</span></span>
5.  <span data-ttu-id="73cb5-123">Spécifiez le marqueur à partir duquel démarrer la lecture en appelant [**IWMReaderAdvanced2 :: StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker).</span><span class="sxs-lookup"><span data-stu-id="73cb5-123">Specify the marker at which to start playback by calling [**IWMReaderAdvanced2::StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker).</span></span> <span data-ttu-id="73cb5-124">Vous devez passer l’index du marqueur souhaité, que vous avez enregistré à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="73cb5-124">You must pass the index of the desired marker, which you saved in step 3.</span></span>
6.  <span data-ttu-id="73cb5-125">Gérez les exemples comme vous le feriez normalement dans votre implémentation de la méthode [**IWMReaderCallback :: OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) .</span><span class="sxs-lookup"><span data-stu-id="73cb5-125">Handle the samples as you normally would in your implementation of the [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="73cb5-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="73cb5-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73cb5-127">**Marqueurs**</span><span class="sxs-lookup"><span data-stu-id="73cb5-127">**Markers**</span></span>](markers.md)
</dt> <dt>

[<span data-ttu-id="73cb5-128">**Lecture des fichiers avec le lecteur asynchrone**</span><span class="sxs-lookup"><span data-stu-id="73cb5-128">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="73cb5-129">**Utilisation des index**</span><span class="sxs-lookup"><span data-stu-id="73cb5-129">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




