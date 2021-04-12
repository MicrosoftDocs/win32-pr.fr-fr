---
description: Les types de compteurs d’algorithmes de compteur peuvent calculer des taux ou des moyennes d’octets pour un échantillon ou sur une période de temps pour une opération particulière.
ms.assetid: 4423e35e-2a93-4f68-8494-89df05268cc9
ms.tgt_platform: multiple
title: Types de compteurs d’algorithmes de compteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12bd55a2a9cc9cc9193a86ffe740ebfa856c0ffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319674"
---
# <a name="counter-algorithm-counter-types"></a><span data-ttu-id="1898c-103">Types de compteurs d’algorithmes de compteur</span><span class="sxs-lookup"><span data-stu-id="1898c-103">Counter Algorithm Counter Types</span></span>

<span data-ttu-id="1898c-104">Les types de compteurs d’algorithmes de compteur peuvent calculer des taux ou des moyennes d’octets pour un échantillon ou sur une période de temps pour une opération particulière.</span><span class="sxs-lookup"><span data-stu-id="1898c-104">Counter algorithm counter types may calculate rates or averages bytes for a sample or over a time period for a particular operation.</span></span>

<span data-ttu-id="1898c-105">La propriété **AvgDiskBytesPerTransfer** de la classe [**Win32 \_ PerfRawData \_ Perfdisk \_ PHYSICALDISK**](/previous-versions//aa394308(v=vs.85)) utilise le nombre \_ moyen de performances \_ .</span><span class="sxs-lookup"><span data-stu-id="1898c-105">The **AvgDiskBytesPerTransfer** property in the [**Win32\_PerfRawData\_PerfDisk\_PhysicalDisk**](/previous-versions//aa394308(v=vs.85)) class uses the PERF\_AVERAGE\_BULK countertype.</span></span> <span data-ttu-id="1898c-106">Dans ce cas, le transfert est l’opération et le nombre cumulé d’octets envoyés correspond aux données du compteur.</span><span class="sxs-lookup"><span data-stu-id="1898c-106">In this case, the transfer is the operation, and the accumulating number of bytes that are sent is the counter data.</span></span> <span data-ttu-id="1898c-107">Pour les deux exemples, la Division de la différence entre les octets cumulés par la différence dans l’accumulation de transferts produira le nombre moyen d’octets par transfert pendant la période entre les exemples.</span><span class="sxs-lookup"><span data-stu-id="1898c-107">For any two samples, dividing the difference of accumulated bytes by the difference in accumulating transfers will produce the average number of bytes per transfer during the period between the samples.</span></span>

<span data-ttu-id="1898c-108">Les algorithmes de compteur suivants sont fournis :</span><span class="sxs-lookup"><span data-stu-id="1898c-108">The following counter algorithms are provided:</span></span>



| <span data-ttu-id="1898c-109">CounterType</span><span class="sxs-lookup"><span data-stu-id="1898c-109">CounterType</span></span>                                                                                              | <span data-ttu-id="1898c-110">Description</span><span class="sxs-lookup"><span data-stu-id="1898c-110">Description</span></span>                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1898c-111">[Performances \_ Décimale \_ en bloc moyenne](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))1073874176</span><span class="sxs-lookup"><span data-stu-id="1898c-111">[PERF\_AVERAGE\_BULK](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 1073874176</span></span><br/>       | <span data-ttu-id="1898c-112">Nombre d’éléments traités, en moyenne, au cours d’une opération.</span><span class="sxs-lookup"><span data-stu-id="1898c-112">Number of items processed, on average, during an operation.</span></span> <span data-ttu-id="1898c-113">Ce type de compteur affiche un rapport entre les éléments traités (tels que les octets envoyés) et le nombre d’opérations terminées, et requiert une propriété de base avec une \_ base moyenne de performances \_ comme type de compteur.</span><span class="sxs-lookup"><span data-stu-id="1898c-113">This counter type displays a ratio of the items processed (such as bytes sent) to the number of operations completed, and requires a base property with PERF\_AVERAGE\_BASE as the counter type.</span></span> |
| <span data-ttu-id="1898c-114">[Performances \_ Compteur \_ -nombre décimal](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))272696320</span><span class="sxs-lookup"><span data-stu-id="1898c-114">[PERF\_COUNTER\_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 272696320</span></span><br/>     | <span data-ttu-id="1898c-115">Nombre moyen d’opérations effectuées au cours de chaque seconde de l’intervalle échantillon.</span><span class="sxs-lookup"><span data-stu-id="1898c-115">Average number of operations completed during each second of the sample interval.</span></span> <span data-ttu-id="1898c-116">.</span><span class="sxs-lookup"><span data-stu-id="1898c-116">.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="1898c-117">[Performances \_ EXEMPLE de \_ compteur](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))décimal 4260864</span><span class="sxs-lookup"><span data-stu-id="1898c-117">[PERF\_SAMPLE\_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4260864</span></span><br/>        | <span data-ttu-id="1898c-118">Nombre moyen d’opérations exécutées en une seconde.</span><span class="sxs-lookup"><span data-stu-id="1898c-118">Average number of operations completed in one second.</span></span> <span data-ttu-id="1898c-119">Ce type de compteur requiert une propriété de base avec l’exemple de base PERF de type de compteur \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1898c-119">This counter type requires a base property with the counter type PERF\_SAMPLE\_BASE.</span></span>                                                                                                                   |
| <span data-ttu-id="1898c-120">[Performances \_ COMPTEUR \_ \_ nombre de blocs](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))décimal 272696576</span><span class="sxs-lookup"><span data-stu-id="1898c-120">[PERF\_COUNTER\_BULK\_COUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 272696576</span></span><br/> | <span data-ttu-id="1898c-121">Nombre moyen d’opérations effectuées au cours de chaque seconde de l’intervalle échantillon.</span><span class="sxs-lookup"><span data-stu-id="1898c-121">Average number of operations completed during each second of the sample interval.</span></span> <span data-ttu-id="1898c-122">Ce type de compteur est identique au type de \_ compteur de compteur \_ de performances, mais il utilise des champs plus étendus pour prendre en charge des valeurs plus élevées.</span><span class="sxs-lookup"><span data-stu-id="1898c-122">This counter type is the same as the PERF\_COUNTER\_COUNTER type, but it uses larger fields to accommodate larger values.</span></span>                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="1898c-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1898c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1898c-124">Types de compteurs de performance WMI</span><span class="sxs-lookup"><span data-stu-id="1898c-124">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> </dl>

 

