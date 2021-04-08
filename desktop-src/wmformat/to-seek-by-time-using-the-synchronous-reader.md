---
title: Pour effectuer une recherche par heure à l’aide du lecteur synchrone
description: Pour effectuer une recherche par heure à l’aide du lecteur synchrone
ms.assetid: 143f72b0-9d71-4efa-b8d4-5cde53a2aa2a
keywords:
- ASF (Advanced Systems Format), recherche par heure
- ASF (format de systèmes avancés), recherche par heure
- ASF (Advanced Systems Format), lecteurs synchrones
- ASF (format des systèmes avancés), lecteurs synchrones
- lecteurs synchrones, recherche par heure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4a43e914a6fc0d320860db61f4747cbee3033e9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723562"
---
# <a name="to-seek-by-time-using-the-synchronous-reader"></a><span data-ttu-id="07739-108">Pour effectuer une recherche par heure à l’aide du lecteur synchrone</span><span class="sxs-lookup"><span data-stu-id="07739-108">To Seek By Time Using the Synchronous Reader</span></span>

<span data-ttu-id="07739-109">Pour rechercher des données à l’aide du lecteur synchrone, vous spécifiez une plage pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="07739-109">To seek for data using the synchronous reader, you specify a range for playback.</span></span> <span data-ttu-id="07739-110">Une plage est définie par une heure de début de présentation et une durée, à la fois en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="07739-110">A range is defined by a starting presentation time and a duration, both in 100-nanosecond units.</span></span>

<span data-ttu-id="07739-111">Pour rechercher des données dans un fichier ASF par heure de présentation à l’aide du lecteur synchrone, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="07739-111">To seek data in an ASF file by presentation time using the synchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="07739-112">Spécifiez une heure de début et une durée pour l’exemple de remise en appelant [**IWMSyncReader :: SetRange**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrange).</span><span class="sxs-lookup"><span data-stu-id="07739-112">Specify a starting time and duration for sample delivery by calling [**IWMSyncReader::SetRange**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrange).</span></span> <span data-ttu-id="07739-113">Cette méthode ne vous oblige pas à spécifier un numéro de flux, car les durées de présentation de chaque flux doivent déjà être synchronisées.</span><span class="sxs-lookup"><span data-stu-id="07739-113">This method does not require you to specify a stream number because the presentation times of each stream should already be synchronized.</span></span>
2.  <span data-ttu-id="07739-114">Commencez la récupération des exemples avec des appels à [**IWMSyncReader :: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span><span class="sxs-lookup"><span data-stu-id="07739-114">Begin retrieving samples with calls to [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span></span> <span data-ttu-id="07739-115">Procédez comme vous le feriez normalement avec le lecteur synchrone.</span><span class="sxs-lookup"><span data-stu-id="07739-115">Proceed as you normally would with the synchronous reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07739-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="07739-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07739-117">**Interface IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="07739-117">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="07739-118">**Lecture des fichiers avec le lecteur synchrone**</span><span class="sxs-lookup"><span data-stu-id="07739-118">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




