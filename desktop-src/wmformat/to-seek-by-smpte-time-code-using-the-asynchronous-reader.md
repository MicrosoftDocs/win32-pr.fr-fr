---
title: Pour effectuer une recherche par code temporel SMPTE à l’aide du lecteur asynchrone
description: Pour effectuer une recherche par code temporel SMPTE à l’aide du lecteur asynchrone
ms.assetid: 5c618f04-3761-418c-b75a-70c7bf7fa5be
keywords:
- ASF (Advanced Systems Format), recherche par les codes temporels SMPTE
- ASF (format des systèmes avancés), recherche par les codes temporels SMPTE
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), codes temporels SMPTE
- ASF (format des systèmes avancés), codes temporels SMPTE
- lecteurs asynchrones, recherche par les codes temporels SMPTE
- lecteurs asynchrones, codes temporels SMPTE
- Codes temporels SMPTE, recherche
- Codes temporels SMPTE, lecteurs asynchrones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42bb90e899db9820ccbd14e42b9699a5f99c7434
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381475"
---
# <a name="to-seek-by-smpte-time-code-using-the-asynchronous-reader"></a><span data-ttu-id="527e4-113">Pour effectuer une recherche par code temporel SMPTE à l’aide du lecteur asynchrone</span><span class="sxs-lookup"><span data-stu-id="527e4-113">To Seek By SMPTE Time Code Using the Asynchronous Reader</span></span>

<span data-ttu-id="527e4-114">L’objet lecteur peut rechercher un point dans un fichier en fonction du code temporel SMPTE associé à un flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="527e4-114">The reader object can seek to a point in a file based on the SMPTE time code associated with a video stream.</span></span> <span data-ttu-id="527e4-115">Les données de code d’heure sont encapsulées dans les structures de [**\_ données d' \_ extension \_ du code**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) d’erreur WMT qui sont attachées à des exemples vidéo en tant qu’extensions d’unité de données.</span><span class="sxs-lookup"><span data-stu-id="527e4-115">Time code data is encapsulated in [**WMT\_TIMECODE\_EXTENSION\_DATA**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) structures that are attached to video samples as data unit extensions.</span></span>

<span data-ttu-id="527e4-116">Les codes temporels SMPTE sont définis par une plage et un code horaire dans cette plage.</span><span class="sxs-lookup"><span data-stu-id="527e4-116">SMPTE time codes are defined by a range and a time code within that range.</span></span> <span data-ttu-id="527e4-117">Une plage est une série continue de codes temporels.</span><span class="sxs-lookup"><span data-stu-id="527e4-117">A range is a continuous series of time codes.</span></span> <span data-ttu-id="527e4-118">Chaque code de temps est défini par les heures, les minutes, les secondes et les frames.</span><span class="sxs-lookup"><span data-stu-id="527e4-118">Each time code is defined by hours, minutes, seconds, and frames.</span></span>

<span data-ttu-id="527e4-119">Pour rechercher des données dans un fichier ASF par code temporel SMPTE à l’aide du lecteur asynchrone, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="527e4-119">To seek data in an ASF file by SMPTE time code using the asynchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="527e4-120">Obtenez un pointeur vers l’interface [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) de l’objet lecteur en appelant **IWMReader :: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="527e4-120">Obtain a pointer to the [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
2.  <span data-ttu-id="527e4-121">Définissez le code et la durée de l’heure de début en appelant [**IWMReaderAdvanced3 :: StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition).</span><span class="sxs-lookup"><span data-stu-id="527e4-121">Set the starting time code and duration by calling [**IWMReaderAdvanced3::StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition).</span></span> <span data-ttu-id="527e4-122">Vous devez spécifier le numéro de flux d’un flux vidéo qui est indexé par code de temps.</span><span class="sxs-lookup"><span data-stu-id="527e4-122">You must specify the stream number of a video stream that is indexed by time code.</span></span> <span data-ttu-id="527e4-123">Le lecteur synchronise le reste des sorties avec l’heure de présentation du frame spécifié du flux spécifié et commence à fournir des exemples de sortie.</span><span class="sxs-lookup"><span data-stu-id="527e4-123">The reader will synchronize the rest of the outputs to the presentation time of the specified frame of the specified stream and begin delivering output samples.</span></span>
3.  <span data-ttu-id="527e4-124">Gérez les exemples comme vous le feriez normalement dans votre implémentation de la méthode **IWMReaderCallback :: OnSample** .</span><span class="sxs-lookup"><span data-stu-id="527e4-124">Handle the samples as you normally would in your implementation of the **IWMReaderCallback::OnSample** method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="527e4-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="527e4-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="527e4-126">**Lecture des fichiers avec le lecteur asynchrone**</span><span class="sxs-lookup"><span data-stu-id="527e4-126">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="527e4-127">**Utilisation des index**</span><span class="sxs-lookup"><span data-stu-id="527e4-127">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> <dt>

[<span data-ttu-id="527e4-128">**Prise en charge des codes temporels SMPTE**</span><span class="sxs-lookup"><span data-stu-id="527e4-128">**SMPTE Time Code Support**</span></span>](smpte-time-code-support.md)
</dt> </dl>

 

 




