---
description: Exemple ASFParser
ms.assetid: 6be1e12f-7d4a-4564-88ae-14fd71fd2cf9
title: Exemple ASFParser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c159b481e22d77b0bee9adccbbb74073398c12b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201182"
---
# <a name="asfparser-sample"></a><span data-ttu-id="b6efc-103">Exemple ASFParser</span><span class="sxs-lookup"><span data-stu-id="b6efc-103">ASFParser Sample</span></span>

<span data-ttu-id="b6efc-104">Montre comment analyser les données à partir d’un fichier ASF (Advanced Systems Format) à l’aide des composants ASF de bas niveau dans Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="b6efc-104">Shows how to parse data from an Advanced Systems Format (ASF) file by using the low-level ASF components in Media Foundation.</span></span> <span data-ttu-id="b6efc-105">L’exemple illustre les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="b6efc-105">The sample demonstrates the following tasks:</span></span>

-   <span data-ttu-id="b6efc-106">Énumération des flux audio et vidéo dans un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="b6efc-106">Enumerating the audio and video streams in an ASF file.</span></span>
-   <span data-ttu-id="b6efc-107">Sélection d’un flux audio ou vidéo pour l’analyse.</span><span class="sxs-lookup"><span data-stu-id="b6efc-107">Selecting an audio or a video stream for parsing.</span></span>
-   <span data-ttu-id="b6efc-108">Recherche d’un paquet à une heure de lecture souhaitée.</span><span class="sxs-lookup"><span data-stu-id="b6efc-108">Seeking to a packet at a desired playback time.</span></span>
-   <span data-ttu-id="b6efc-109">Génération d’exemples compressés pour le flux sélectionné.</span><span class="sxs-lookup"><span data-stu-id="b6efc-109">Generating compressed samples for the selected stream.</span></span>
-   <span data-ttu-id="b6efc-110">Décodage des échantillons audio et vidéo.</span><span class="sxs-lookup"><span data-stu-id="b6efc-110">Decoding audio and video samples.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="b6efc-111">API illustrées</span><span class="sxs-lookup"><span data-stu-id="b6efc-111">APIs Demonstrated</span></span>

<span data-ttu-id="b6efc-112">Cet exemple illustre les interfaces de Microsoft Media Foundation suivantes :</span><span class="sxs-lookup"><span data-stu-id="b6efc-112">This sample demonstrates the following Microsoft Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="b6efc-113">**IMFASFContentInfo**</span><span class="sxs-lookup"><span data-stu-id="b6efc-113">**IMFASFContentInfo**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)
-   [<span data-ttu-id="b6efc-114">**IMFASFIndexer**</span><span class="sxs-lookup"><span data-stu-id="b6efc-114">**IMFASFIndexer**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer)
-   [<span data-ttu-id="b6efc-115">**IMFASFSplitter**</span><span class="sxs-lookup"><span data-stu-id="b6efc-115">**IMFASFSplitter**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter)

## <a name="usage"></a><span data-ttu-id="b6efc-116">Utilisation</span><span class="sxs-lookup"><span data-stu-id="b6efc-116">Usage</span></span>

1.  <span data-ttu-id="b6efc-117">Pour ouvrir un fichier ASF, cliquez sur le bouton **ouvrir le fichier multimédia..** ..</span><span class="sxs-lookup"><span data-stu-id="b6efc-117">To open an ASF file, click the **Open Media File...** button.</span></span>
2.  <span data-ttu-id="b6efc-118">Sélectionnez un fichier ASF, puis cliquez sur **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="b6efc-118">Select an ASF file and click **Open**.</span></span> <span data-ttu-id="b6efc-119">Les informations relatives au fichier s’affichent dans le volet d' **informations** .</span><span class="sxs-lookup"><span data-stu-id="b6efc-119">Information about the file is shown on the **Information** pane.</span></span>
3.  <span data-ttu-id="b6efc-120">Sous **configuration de l’analyseur**, sélectionnez un flux à analyser.</span><span class="sxs-lookup"><span data-stu-id="b6efc-120">Under **Parser Configuration**, select a stream to parse.</span></span>
4.  <span data-ttu-id="b6efc-121">Pour générer des exemples en sens inverse, sélectionnez **inverser**.</span><span class="sxs-lookup"><span data-stu-id="b6efc-121">To generate samples in reverse, select **Reverse**.</span></span>
5.  <span data-ttu-id="b6efc-122">Pour spécifier le point de départ, faites glisser le curseur vers l’emplacement souhaité.</span><span class="sxs-lookup"><span data-stu-id="b6efc-122">To specify the start point, drag the slider to the desired location.</span></span>
6.  <span data-ttu-id="b6efc-123">Pour commencer l’analyse, cliquez sur le bouton **générer des exemples** .</span><span class="sxs-lookup"><span data-stu-id="b6efc-123">To begin parsing, click the **Generate Samples** button.</span></span> <span data-ttu-id="b6efc-124">Les informations sur les exemples s’affichent dans le volet d' **informations** .</span><span class="sxs-lookup"><span data-stu-id="b6efc-124">Information about the samples is shown on the **Information** pane.</span></span>
7.  <span data-ttu-id="b6efc-125">Pour tester les exemples du flux audio, cliquez sur le bouton **tester l’audio** .</span><span class="sxs-lookup"><span data-stu-id="b6efc-125">To test the samples for the audio stream, click the **Test Audio** button.</span></span>
8.  <span data-ttu-id="b6efc-126">Pour tester les exemples du flux vidéo, cliquez sur le bouton **afficher la bitmap** .</span><span class="sxs-lookup"><span data-stu-id="b6efc-126">To test the samples for the video stream, click the **Show Bitmap** button.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6efc-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6efc-127">Requirements</span></span>



| <span data-ttu-id="b6efc-128">Produit</span><span class="sxs-lookup"><span data-stu-id="b6efc-128">Product</span></span>                                                        | <span data-ttu-id="b6efc-129">Version</span><span class="sxs-lookup"><span data-stu-id="b6efc-129">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="b6efc-130">SDK Windows</span><span class="sxs-lookup"><span data-stu-id="b6efc-130">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="b6efc-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b6efc-131">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="b6efc-132">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="b6efc-132">Downloading the Sample</span></span>

<span data-ttu-id="b6efc-133">Cet exemple est disponible dans le [référentiel GitHub des exemples classiques Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/asfparser).</span><span class="sxs-lookup"><span data-stu-id="b6efc-133">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/asfparser).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6efc-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b6efc-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6efc-135">Exemples du kit de développement logiciel Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b6efc-135">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="b6efc-136">Prise en charge ASF dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b6efc-136">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="b6efc-137">Didacticiel : lecture d’un fichier ASF</span><span class="sxs-lookup"><span data-stu-id="b6efc-137">Tutorial: Reading an ASF File</span></span>](tutorial--reading-an-asf-file.md)
</dt> <dt>

[<span data-ttu-id="b6efc-138">Composants WMContainer ASF</span><span class="sxs-lookup"><span data-stu-id="b6efc-138">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> </dl>

 

 



