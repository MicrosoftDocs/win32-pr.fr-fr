---
title: Pour accéder aux statistiques de performances des lecteurs
description: Pour accéder aux statistiques de performances des lecteurs
ms.assetid: 996abfe6-1444-48ab-8c34-ba923c4cd511
keywords:
- ASF (Advanced Systems Format), statistiques de performances des lecteurs
- ASF (format des systèmes avancés), statistiques des performances du lecteur
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), statistiques de performances
- ASF (format de systèmes avancés), statistiques de performances
- lecteurs asynchrones, statistiques de performances
- performances, statistiques sur les lecteurs
- performances, lecteurs asynchrones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5484b211f2c2d1e9ad4cf9aac3773c7946757c2
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103841889"
---
# <a name="to-get-reader-performance-statistics"></a><span data-ttu-id="72cf0-112">Pour accéder aux statistiques de performances des lecteurs</span><span class="sxs-lookup"><span data-stu-id="72cf0-112">To Get Reader Performance Statistics</span></span>

<span data-ttu-id="72cf0-113">Lors de la lecture de fichiers localement avec le lecteur asynchrone, il n’est pas nécessaire de vérifier les performances des opérations de lecture.</span><span class="sxs-lookup"><span data-stu-id="72cf0-113">When reading files locally with the asynchronous reader, it is not necessary to check the performance of reading operations.</span></span> <span data-ttu-id="72cf0-114">Toutefois, si votre application lit à partir d’une source de streaming, les statistiques de performances peuvent être très importantes.</span><span class="sxs-lookup"><span data-stu-id="72cf0-114">If your application is reading from a streaming source however, performance statistics can be very important.</span></span> <span data-ttu-id="72cf0-115">Votre application peut répondre aux modifications des performances de lecture pour garantir la meilleure expérience possible pour l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="72cf0-115">Your application can respond to changes in playback performance to ensure the best possible end-user experience.</span></span>

<span data-ttu-id="72cf0-116">Les informations de performances que vous pouvez récupérer à partir du lecteur incluent les statistiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="72cf0-116">The performance information you can retrieve from the reader includes the following statistics:</span></span>

-   <span data-ttu-id="72cf0-117">Bande passante actuelle de la connexion.</span><span class="sxs-lookup"><span data-stu-id="72cf0-117">The current bandwidth of the connection.</span></span>
-   <span data-ttu-id="72cf0-118">Nombre de paquets reçus à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="72cf0-118">The number of packets received from the server.</span></span>
-   <span data-ttu-id="72cf0-119">Nombre de paquets perdus qui ont été récupérés.</span><span class="sxs-lookup"><span data-stu-id="72cf0-119">The number of lost packets that were recovered.</span></span>
-   <span data-ttu-id="72cf0-120">Nombre de paquets perdus qui n’ont pas été récupérés.</span><span class="sxs-lookup"><span data-stu-id="72cf0-120">The number of lost packets that were not recovered.</span></span>
-   <span data-ttu-id="72cf0-121">Pourcentage du nombre total de paquets envoyés qui ont été reçus.</span><span class="sxs-lookup"><span data-stu-id="72cf0-121">The percentage of the total number of packets sent that have been received.</span></span>

<span data-ttu-id="72cf0-122">Pour accéder aux statistiques de performances des lecteurs, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="72cf0-122">To get reader performance statistics, perform the following steps.</span></span>

1.  <span data-ttu-id="72cf0-123">Avant de commencer la lecture, créez une structure de [**\_ \_ statistiques WM Reader**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) .</span><span class="sxs-lookup"><span data-stu-id="72cf0-123">Before starting playback, create a [**WM\_READER\_STATISTICS**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) structure.</span></span> <span data-ttu-id="72cf0-124">Vous devez définir le membre **cbSize** sur sizeof ( \_ statistiques du lecteur WM \_ ).</span><span class="sxs-lookup"><span data-stu-id="72cf0-124">You must set the **cbSize** member to sizeof(WM\_READER\_STATISTICS).</span></span>
2.  <span data-ttu-id="72cf0-125">Obtenez un pointeur vers l’interface [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) de l’objet lecteur en appelant **IWMReader :: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="72cf0-125">Obtain a pointer to the [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
3.  <span data-ttu-id="72cf0-126">Pendant la lecture, effectuez fréquemment des appels à [**IWMReaderAdvanced :: GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics) pour surveiller les performances.</span><span class="sxs-lookup"><span data-stu-id="72cf0-126">During playback, make calls to [**IWMReaderAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics) frequently to monitor performance.</span></span> <span data-ttu-id="72cf0-127">Transmettez votre structure de **\_ \_ statistiques de lecteur WM** avec chaque appel et examinez les membres appropriés.</span><span class="sxs-lookup"><span data-stu-id="72cf0-127">Pass your **WM\_READER\_STATISTICS** structure with each call and examine the appropriate members.</span></span>

## <a name="related-topics"></a><span data-ttu-id="72cf0-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="72cf0-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72cf0-129">**Lecture des fichiers avec le lecteur asynchrone**</span><span class="sxs-lookup"><span data-stu-id="72cf0-129">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




