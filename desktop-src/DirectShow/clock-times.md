---
description: Heures d’horloge
ms.assetid: ff964f7f-a084-4de3-8b2b-8efb6c9f4a9f
title: Heures d’horloge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e0639fd2b38e312f30f932fcf508427cd71c054
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392404"
---
# <a name="clock-times"></a><span data-ttu-id="514bc-103">Heures d’horloge</span><span class="sxs-lookup"><span data-stu-id="514bc-103">Clock Times</span></span>

<span data-ttu-id="514bc-104">DirectShow définit deux heures d’horloge associées : le temps de référence et le temps de flux.</span><span class="sxs-lookup"><span data-stu-id="514bc-104">DirectShow defines two related clock times: reference time and stream time.</span></span>

-   <span data-ttu-id="514bc-105">Le *temps de référence* est l’heure absolue retournée par l’horloge de référence.</span><span class="sxs-lookup"><span data-stu-id="514bc-105">*Reference time* is the absolute time returned by the reference clock.</span></span> <span data-ttu-id="514bc-106">(Voir [horloges de référence](reference-clocks.md).)</span><span class="sxs-lookup"><span data-stu-id="514bc-106">(See [Reference Clocks](reference-clocks.md).)</span></span>
-   <span data-ttu-id="514bc-107">Le *temps de flux* est défini par rapport au moment où l’exécution du dernier graphique a commencé.</span><span class="sxs-lookup"><span data-stu-id="514bc-107">*Stream time* is defined relative to when the graph last started running.</span></span>
    -   <span data-ttu-id="514bc-108">Pendant que le graphique est en cours d’exécution, le temps de flux est égal à l’heure de référence moins l’heure de début.</span><span class="sxs-lookup"><span data-stu-id="514bc-108">While the graph is running, stream time equals reference time minus start time.</span></span>
    -   <span data-ttu-id="514bc-109">Lorsque le graphique est suspendu, le temps de flux reste à l’heure du flux lorsqu’il a été suspendu.</span><span class="sxs-lookup"><span data-stu-id="514bc-109">While the graph is paused, stream time remains at the stream time when it was paused.</span></span>
    -   <span data-ttu-id="514bc-110">Après une opération de recherche, le temps de flux se réinitialise à zéro.</span><span class="sxs-lookup"><span data-stu-id="514bc-110">After a seek operation, stream time resets to zero.</span></span>
    -   <span data-ttu-id="514bc-111">Lorsque le graphique est arrêté, le temps de flux n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="514bc-111">While the graph is stopped, stream time is undefined.</span></span>

<span data-ttu-id="514bc-112">Quand un échantillon de média a un horodatage *t*, cela signifie que l’exemple doit être rendu au temps de flux *t*.</span><span class="sxs-lookup"><span data-stu-id="514bc-112">When a media sample has a time stamp *t*, it means the sample should be rendered at stream time *t*.</span></span> <span data-ttu-id="514bc-113">C’est la raison pour laquelle le temps de flux est également appelé *heure de présentation*.</span><span class="sxs-lookup"><span data-stu-id="514bc-113">For this reason, stream time is also called *presentation time*.</span></span>

<span data-ttu-id="514bc-114">Quand une application appelle [**IMediaControl :: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) pour exécuter le graphique de filtre, le gestionnaire de graphique de filtre appelle [**IMediaFilter :: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) sur chaque filtre.</span><span class="sxs-lookup"><span data-stu-id="514bc-114">When an application calls [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) to run the filter graph, the Filter Graph Manager calls [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) on each filter.</span></span> <span data-ttu-id="514bc-115">Pour compenser le temps de démarrage de l’exécution des filtres, le gestionnaire de graphes de filtres spécifie une heure de début légèrement à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="514bc-115">To compensate for the slight amount of time it takes for the filters to start running, the Filter Graph Manager specifies a start time slightly in the future.</span></span>

## <a name="related-topics"></a><span data-ttu-id="514bc-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="514bc-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="514bc-117">Temps et horloges dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="514bc-117">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="514bc-118">Horodatages</span><span class="sxs-lookup"><span data-stu-id="514bc-118">Time Stamps</span></span>](time-stamps.md)
</dt> </dl>

 

 



