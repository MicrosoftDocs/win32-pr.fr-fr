---
description: Les types de compteurs d’algorithmes de longueur de file d’attente incrémentent le nombre d’éléments dans une file d’attente à chaque intervalle d’échantillonnage, comme spécifié par la propriété de fréquence appropriée&\# 8212 ; Fréquence \_ PerfTime, et ainsi de suite.
ms.assetid: 514b1a79-ed9d-4ec6-a6ea-b3490291ce18
ms.tgt_platform: multiple
title: Types de compteurs d’algorithmes de longueur de file d’attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06665c2fb8fca014c7d722f0ea22cf7e86833ab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202182"
---
# <a name="queue-length-algorithm-counter-types"></a><span data-ttu-id="2726a-103">Types de compteurs d’algorithmes de longueur de file d’attente</span><span class="sxs-lookup"><span data-stu-id="2726a-103">Queue-length Algorithm Counter Types</span></span>

<span data-ttu-id="2726a-104">Les types de compteurs d’algorithmes de longueur de file d’attente incrémentent le nombre d’éléments dans une file d’attente à chaque intervalle d’échantillonnage, comme spécifié par la fréquence de propriété de fréquence appropriée \_ PerfTime, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="2726a-104">Queue-length algorithm counter types increment the number of items in a queue at each sample interval as specified by the appropriate frequency property Frequency\_PerfTime, and so on.</span></span> <span data-ttu-id="2726a-105">Le résultat de la préproduction est divisé par le nombre d’échantillons pour produire la longueur moyenne de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="2726a-105">The cooked result divides by the number of samples to produce the average queue length.</span></span>

<span data-ttu-id="2726a-106">Par exemple, la propriété **AvgDiskQueueLength** dans le [**\_ \_ \_ disque logique Win32 PerfRawData Perfdisk**](./retrieving-raw-and-formatted-performance-data.md) qui utilise le \_ type de \_ compteur type de compteur de performances 100 NS \_ QUEUELEN \_ .</span><span class="sxs-lookup"><span data-stu-id="2726a-106">An example is the **AvgDiskQueueLength** property in the [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) that uses the PERF\_COUNTER\_100NS\_QUEUELEN\_TYPE counter type.</span></span>



| <span data-ttu-id="2726a-107">@, Constante</span><span class="sxs-lookup"><span data-stu-id="2726a-107">CounterType Constant</span></span>                                                                                                 | <span data-ttu-id="2726a-108">Description</span><span class="sxs-lookup"><span data-stu-id="2726a-108">Description</span></span>                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2726a-109">[Performances \_ COUNTER \_ QUEUELEN \_ TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4523008</span><span class="sxs-lookup"><span data-stu-id="2726a-109">[PERF\_COUNTER\_QUEUELEN\_TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4523008</span></span><br/>            | <span data-ttu-id="2726a-110">Longueur moyenne d’une file d’attente vers une ressource dans le temps.</span><span class="sxs-lookup"><span data-stu-id="2726a-110">Average length of a queue to a resource over time.</span></span> <span data-ttu-id="2726a-111">Il affiche la différence entre les longueurs de file d'attente observées au cours des deux derniers intervalles échantillons divisée par la durée de l'intervalle.</span><span class="sxs-lookup"><span data-stu-id="2726a-111">It shows the difference between the queue lengths observed during the last two sample intervals divided by the duration of the interval.</span></span>                       |
| <span data-ttu-id="2726a-112">[Performances \_ COMPTEUR \_ \_ QUEUELEN de \_ type grand](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))nombre décimal 4523264</span><span class="sxs-lookup"><span data-stu-id="2726a-112">[PERF\_COUNTER\_LARGE\_QUEUELEN\_TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4523264</span></span><br/>     | <span data-ttu-id="2726a-113">Longueur moyenne d’une file d’attente vers une ressource dans le temps.</span><span class="sxs-lookup"><span data-stu-id="2726a-113">Average length of a queue to a resource over time.</span></span> <span data-ttu-id="2726a-114">Les compteurs de ce type affichent la différence entre les longueurs de file d'attente observées au cours des deux derniers intervalles échantillons divisée par la durée de l'intervalle.</span><span class="sxs-lookup"><span data-stu-id="2726a-114">Counters of this type display the difference between the queue lengths observed during the last two sample intervals, divided by the duration of the interval.</span></span> |
| <span data-ttu-id="2726a-115">[Performances \_ COUNTER \_ 100 NS \_ QUEUELEN \_ type](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 5571840</span><span class="sxs-lookup"><span data-stu-id="2726a-115">[PERF\_COUNTER\_100NS\_QUEUELEN\_TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 5571840</span></span><br/>     | <span data-ttu-id="2726a-116">Longueur moyenne d’une file d’attente vers une ressource dans le temps en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="2726a-116">Average length of a queue to a resource over time in 100 nanosecond units.</span></span>                                                                                                                                        |
| <span data-ttu-id="2726a-117">[Performances \_ COUNTER \_ obj \_ Time \_ QUEUELEN \_ type](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 6620416</span><span class="sxs-lookup"><span data-stu-id="2726a-117">[PERF\_COUNTER\_OBJ\_TIME\_QUEUELEN\_TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 6620416</span></span><br/> | <span data-ttu-id="2726a-118">Heure à laquelle un objet se trouve dans une file d’attente.</span><span class="sxs-lookup"><span data-stu-id="2726a-118">Time an object is in a queue.</span></span>                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="2726a-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2726a-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2726a-120">Types de compteurs de performance WMI</span><span class="sxs-lookup"><span data-stu-id="2726a-120">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> </dl>

 

