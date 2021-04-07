---
title: Pour rechercher les numéros de flux et les numéros de sortie
description: Pour rechercher les numéros de flux et les numéros de sortie
ms.assetid: 531edd4a-a257-47cd-a367-b59cda3ea76c
keywords:
- ASF (Advanced Systems Format), numéros de diffusion
- ASF (format des systèmes avancés), création de nombres
- ASF (Advanced Systems Format), recherche des numéros de sortie
- ASF (format des systèmes avancés), recherche des numéros de sortie
- lecteurs synchrones, numéros de flux
- lecteurs synchrones, recherche des numéros de sortie
- flux, recherche de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4bdf10eaeb95f981ab2972ba56ad09b867cd99
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723466"
---
# <a name="to-find-stream-numbers-and-output-numbers"></a><span data-ttu-id="dfec3-110">Pour rechercher les numéros de flux et les numéros de sortie</span><span class="sxs-lookup"><span data-stu-id="dfec3-110">To Find Stream Numbers and Output Numbers</span></span>

<span data-ttu-id="dfec3-111">Le lecteur synchrone prend en charge un basculement plus simplifié entre le flux et les numéros de sortie pour la lecture que le lecteur asynchrone.</span><span class="sxs-lookup"><span data-stu-id="dfec3-111">The synchronous reader supports more simplified switching between stream and output numbers for playback than the asynchronous reader.</span></span> <span data-ttu-id="dfec3-112">Il est par conséquent plus important de savoir quels sont les nombres de flux qui correspondent aux numéros de sortie, ou l’inverse.</span><span class="sxs-lookup"><span data-stu-id="dfec3-112">It is therefore more important to be able to find which stream numbers equate to which output numbers, or the other way around.</span></span>

<span data-ttu-id="dfec3-113">Pour rechercher le numéro de sortie qui correspond à un numéro de flux, appelez [**IWMSyncReader :: GetOutputNumberForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputnumberforstream).</span><span class="sxs-lookup"><span data-stu-id="dfec3-113">To find the output number that corresponds to a stream number, call [**IWMSyncReader::GetOutputNumberForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputnumberforstream).</span></span>

<span data-ttu-id="dfec3-114">Pour rechercher le numéro de flux qui correspond à un numéro de sortie, appelez [ **IWMSyncReader :: GetStreamNumberForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getstreamnumberforoutput)</span><span class="sxs-lookup"><span data-stu-id="dfec3-114">To find the stream number that corresponds to an output number, call [**IWMSyncReader::GetStreamNumberForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getstreamnumberforoutput)</span></span>

## <a name="related-topics"></a><span data-ttu-id="dfec3-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dfec3-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfec3-116">**Interface IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="dfec3-116">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="dfec3-117">**Entrées, flux et sorties**</span><span class="sxs-lookup"><span data-stu-id="dfec3-117">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> <dt>

[<span data-ttu-id="dfec3-118">**Lecture des fichiers avec le lecteur synchrone**</span><span class="sxs-lookup"><span data-stu-id="dfec3-118">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




