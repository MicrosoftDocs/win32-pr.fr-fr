---
title: Pour rechercher par numéro de frame à l’aide du lecteur asynchrone
description: Pour rechercher par numéro de frame à l’aide du lecteur asynchrone
ms.assetid: faab6344-3afc-47ff-9107-d2ce36c0a2b8
keywords:
- ASF (Advanced Systems Format), recherche par numéro de trame
- ASF (format avancé des systèmes), recherche par numéro de trame
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), lecteurs asynchrones
- lecteurs asynchrones, recherche par numéros de frame
- flux vidéo, recherche par numéros de frame
- flux vidéo, lecteurs asynchrones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 169f5e1ac1e6034bc1db6f610e80af50dd3a0215
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030787"
---
# <a name="to-seek-by-frame-number-using-the-asynchronous-reader"></a><span data-ttu-id="20635-110">Pour rechercher par numéro de frame à l’aide du lecteur asynchrone</span><span class="sxs-lookup"><span data-stu-id="20635-110">To Seek By Frame Number Using the Asynchronous Reader</span></span>

<span data-ttu-id="20635-111">L’objet lecteur asynchrone peut être utilisé pour rechercher le nombre de trames des flux vidéo dans un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="20635-111">The asynchronous reader object can be used to seek to the frame numbers of video streams in an ASF file.</span></span> <span data-ttu-id="20635-112">Pour utiliser la recherche basée sur des frames, le fichier chargé dans le lecteur doit être indexé par frame.</span><span class="sxs-lookup"><span data-stu-id="20635-112">To use frame-based seeking, the file loaded in the reader must be indexed by frame.</span></span> <span data-ttu-id="20635-113">Chaque flux vidéo individuel peut être indexé.</span><span class="sxs-lookup"><span data-stu-id="20635-113">Each individual video stream can be indexed.</span></span> <span data-ttu-id="20635-114">Pour déterminer si un flux a été indexé par Frame, vous pouvez vérifier l’attribut g \_ wszWMNumberOfFrames dans l’en-tête du fichier en appelant [**IWMHeaderInfo :: GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).</span><span class="sxs-lookup"><span data-stu-id="20635-114">To determine whether a stream has been indexed by frame, you can check the g\_wszWMNumberOfFrames attribute in the header of the file by calling [**IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).</span></span>

<span data-ttu-id="20635-115">Pour rechercher des données dans un fichier ASF par numéro de trame à l’aide du lecteur asynchrone, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="20635-115">To seek data in an ASF file by frame number using the asynchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="20635-116">Obtenez un pointeur vers l’interface [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) de l’objet lecteur en appelant **IWMReader :: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="20635-116">Obtain a pointer to the [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
2.  <span data-ttu-id="20635-117">Définissez le numéro et la durée du frame de départ en appelant [**IWMReaderAdvanced3 :: StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition).</span><span class="sxs-lookup"><span data-stu-id="20635-117">Set the starting frame number and duration by calling [**IWMReaderAdvanced3::StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition).</span></span> <span data-ttu-id="20635-118">Vous devez spécifier le numéro de flux d’un flux vidéo indexé par une image.</span><span class="sxs-lookup"><span data-stu-id="20635-118">You must specify the stream number of a frame-indexed video stream.</span></span> <span data-ttu-id="20635-119">Le lecteur synchronise le reste des sorties avec l’heure de présentation du frame spécifié du flux spécifié et commence à fournir des exemples de sortie.</span><span class="sxs-lookup"><span data-stu-id="20635-119">The reader will synchronize the rest of the outputs to the presentation time of the specified frame of the specified stream and begin delivering output samples.</span></span>
3.  <span data-ttu-id="20635-120">Gérez les exemples comme vous le feriez normalement dans votre implémentation de la méthode **IWMReaderCallback :: OnSample** .</span><span class="sxs-lookup"><span data-stu-id="20635-120">Handle the samples as you normally would in your implementation of the **IWMReaderCallback::OnSample** method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="20635-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="20635-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20635-122">**Lecture des fichiers avec le lecteur asynchrone**</span><span class="sxs-lookup"><span data-stu-id="20635-122">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="20635-123">**Lecture des métadonnées lors de la lecture**</span><span class="sxs-lookup"><span data-stu-id="20635-123">**Reading Metadata at Playback**</span></span>](reading-metadata-at-playback.md)
</dt> <dt>

[<span data-ttu-id="20635-124">**Utilisation des index**</span><span class="sxs-lookup"><span data-stu-id="20635-124">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




