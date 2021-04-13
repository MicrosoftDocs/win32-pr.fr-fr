---
title: Pour effectuer une recherche par code temporel SMPTE à l’aide du lecteur synchrone
description: Pour effectuer une recherche par code temporel SMPTE à l’aide du lecteur synchrone
ms.assetid: 1fd8885c-a694-43fd-b2a2-23eb0ae7ed72
keywords:
- ASF (Advanced Systems Format), recherche par les codes temporels SMPTE
- ASF (format des systèmes avancés), recherche par les codes temporels SMPTE
- ASF (Advanced Systems Format), lecteurs synchrones
- ASF (format des systèmes avancés), lecteurs synchrones
- ASF (Advanced Systems Format), codes temporels SMPTE
- ASF (format des systèmes avancés), codes temporels SMPTE
- lecteurs synchrones, recherche par code de temps SMPTE
- lecteurs synchrones, codes temporels SMPTE
- Codes temporels SMPTE, recherche
- Codes temporels SMPTE, lecteurs synchrones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c843ba802272d02f1dfc885a3c65b3d124b7423
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314329"
---
# <a name="to-seek-by-smpte-time-code-using-the-synchronous-reader"></a><span data-ttu-id="e281a-113">Pour effectuer une recherche par code temporel SMPTE à l’aide du lecteur synchrone</span><span class="sxs-lookup"><span data-stu-id="e281a-113">To Seek By SMPTE Time Code Using the Synchronous Reader</span></span>

<span data-ttu-id="e281a-114">L’objet lecteur synchrone peut rechercher un point dans un fichier en fonction du code temporel SMPTE associé à un flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="e281a-114">The synchronous reader object can seek to a point in a file based on the SMPTE time code associated with a video stream.</span></span> <span data-ttu-id="e281a-115">Les données de code d’heure sont encapsulées dans les structures de [**\_ données d' \_ extension \_ du code**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) d’erreur WMT qui sont attachées à des exemples vidéo en tant qu’extensions d’unité de données.</span><span class="sxs-lookup"><span data-stu-id="e281a-115">Time code data is encapsulated in [**WMT\_TIMECODE\_EXTENSION\_DATA**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) structures that are attached to video samples as data unit extensions.</span></span>

<span data-ttu-id="e281a-116">Les codes temporels SMPTE sont définis par une plage et un code horaire dans cette plage.</span><span class="sxs-lookup"><span data-stu-id="e281a-116">SMPTE time codes are defined by a range and a time code within that range.</span></span> <span data-ttu-id="e281a-117">Une plage est une série continue de codes temporels.</span><span class="sxs-lookup"><span data-stu-id="e281a-117">A range is a continuous series of time codes.</span></span> <span data-ttu-id="e281a-118">Chaque code de temps est défini par les heures, les minutes, les secondes et les frames.</span><span class="sxs-lookup"><span data-stu-id="e281a-118">Each time code is defined by hours, minutes, seconds, and frames.</span></span>

<span data-ttu-id="e281a-119">Pour rechercher des données dans un fichier ASF par code temporel SMPTE à l’aide du lecteur synchrone, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="e281a-119">To seek data in an ASF file by SMPTE time code using the synchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="e281a-120">Définissez le code d’heure de début et le code d’heure de fin pour l’exemple de livraison en appelant [**IWMSyncReader :: SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe).</span><span class="sxs-lookup"><span data-stu-id="e281a-120">Set the starting time code and ending time code for sample delivery by calling [**IWMSyncReader::SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe).</span></span> <span data-ttu-id="e281a-121">Vous devez spécifier le numéro de flux d’un flux vidéo indexé par code de temps.</span><span class="sxs-lookup"><span data-stu-id="e281a-121">You must specify the stream number of a video stream indexed by time code.</span></span> <span data-ttu-id="e281a-122">Le lecteur synchrone synchronise le reste des sorties avec l’heure de présentation du cadre spécifié du flux spécifié.</span><span class="sxs-lookup"><span data-stu-id="e281a-122">The synchronous reader will synchronize the rest of the outputs to the presentation time of the specified frame of the specified stream.</span></span>
2.  <span data-ttu-id="e281a-123">Commencez la récupération des exemples avec des appels à [**IWMSyncReader :: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span><span class="sxs-lookup"><span data-stu-id="e281a-123">Begin retrieving samples with calls to [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span></span> <span data-ttu-id="e281a-124">Procédez comme vous le feriez normalement avec le lecteur synchrone.</span><span class="sxs-lookup"><span data-stu-id="e281a-124">Proceed as you normally would with the synchronous reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e281a-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e281a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e281a-126">**Lecture des fichiers avec le lecteur synchrone**</span><span class="sxs-lookup"><span data-stu-id="e281a-126">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="e281a-127">**Prise en charge des codes temporels SMPTE**</span><span class="sxs-lookup"><span data-stu-id="e281a-127">**SMPTE Time Code Support**</span></span>](smpte-time-code-support.md)
</dt> <dt>

[<span data-ttu-id="e281a-128">**Utilisation des index**</span><span class="sxs-lookup"><span data-stu-id="e281a-128">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




