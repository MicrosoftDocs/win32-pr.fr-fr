---
description: Représentent les différences entre les échantillons au fil du temps et utilisent souvent une valeur de base pour le calcul.
ms.assetid: 613268ab-386b-421d-a5b5-aab6a065999c
ms.tgt_platform: multiple
title: Types de compteurs de l’algorithme de base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70514c10b2695aa940d48341752ef647dcca9719
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524391"
---
# <a name="basic-algorithm-counter-types"></a><span data-ttu-id="80645-103">Types de compteurs de l’algorithme de base</span><span class="sxs-lookup"><span data-stu-id="80645-103">Basic Algorithm Counter Types</span></span>

<span data-ttu-id="80645-104">Les types de compteurs de l’algorithme de base représentent généralement les différences entre les exemples au fil du temps, et utilisent souvent une valeur de base pour le calcul.</span><span class="sxs-lookup"><span data-stu-id="80645-104">Basic algorithm counter types generally represent differences between samples over time, and often use a base value for the calculation.</span></span> <span data-ttu-id="80645-105">Par exemple, la propriété **PercentFreeSpace** de la classe [**Win32 \_ PerfFormattedData \_ Perfdisk \_ PhysicalDisk**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) représente le rapport entre l’espace libre disponible sur l’unité de disque physique et l’espace total utilisable fourni par le lecteur de disque physique sélectionné.</span><span class="sxs-lookup"><span data-stu-id="80645-105">For example, the **PercentFreeSpace** property of the [**Win32\_PerfFormattedData\_PerfDisk\_PhysicalDisk**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) class represents the ratio of the free space available on the physical disk unit to the total usable space provided by the selected physical disk drive.</span></span> <span data-ttu-id="80645-106">Cette classe contient également la valeur de base, **PercentFreeSpace \_ base**.</span><span class="sxs-lookup"><span data-stu-id="80645-106">This class also contains the base value, **PercentFreeSpace\_Base**.</span></span> <span data-ttu-id="80645-107">Le pourcentage d’espace disque disponible est obtenu en divisant **PercentFreeSpace** par **PercentFreeSpace \_ base** et en multipliant par 100%.</span><span class="sxs-lookup"><span data-stu-id="80645-107">The percentage of free disk space is obtained by dividing **PercentFreeSpace** by **PercentFreeSpace\_Base** and multiplying by 100%.</span></span>

<span data-ttu-id="80645-108">Les algorithmes de base dans le tableau suivant sont fournis.</span><span class="sxs-lookup"><span data-stu-id="80645-108">The basic algorithms in the following table are provided.</span></span>



| <span data-ttu-id="80645-109">@, Constante</span><span class="sxs-lookup"><span data-stu-id="80645-109">CounterType Constant</span></span>                                                                                    | <span data-ttu-id="80645-110">Description</span><span class="sxs-lookup"><span data-stu-id="80645-110">Description</span></span>                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80645-111">[Performances \_ \_Fraction brute](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))décimale 537003008</span><span class="sxs-lookup"><span data-stu-id="80645-111">[PERF\_RAW\_FRACTION](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 537003008</span></span><br/>       | <span data-ttu-id="80645-112">Rapport entre un sous-ensemble et son ensemble sous forme de pourcentage.</span><span class="sxs-lookup"><span data-stu-id="80645-112">Ratio of a subset to its set as a percentage.</span></span> <span data-ttu-id="80645-113">Ce type de compteur affiche le pourcentage actuel uniquement, et non une moyenne dans le temps.</span><span class="sxs-lookup"><span data-stu-id="80645-113">This counter type displays the current percentage only, not an average over time.</span></span>                                    |
| <span data-ttu-id="80645-114">[Performances \_ EXEMPLE de \_ fraction](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))décimale 549585920</span><span class="sxs-lookup"><span data-stu-id="80645-114">[PERF\_SAMPLE\_FRACTION](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 549585920</span></span><br/>    | <span data-ttu-id="80645-115">Taux moyen d’accès à toutes les opérations au cours des deux derniers intervalles d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="80645-115">Average ratio of hits to all operations during the last two sample intervals.</span></span> <span data-ttu-id="80645-116">Ce type de compteur requiert une propriété de base avec \_ le \_ type de compteur de base Sample perf.</span><span class="sxs-lookup"><span data-stu-id="80645-116">This counter type requires a base property with the PERF\_SAMPLE\_BASE counter type.</span></span> |
| <span data-ttu-id="80645-117">[Performances \_ COMPTEUR \_ Delta](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))décimal 4195328</span><span class="sxs-lookup"><span data-stu-id="80645-117">[PERF\_COUNTER\_DELTA](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4195328</span></span><br/>        | <span data-ttu-id="80645-118">Ce type de compteur affiche la modification de l'attribut mesuré entre les deux derniers intervalles échantillons.</span><span class="sxs-lookup"><span data-stu-id="80645-118">This counter type shows the change in the measured attribute between the two most recent sample intervals.</span></span>                                                         |
| <span data-ttu-id="80645-119">[Performances \_ COUNTER nombre décimal \_ \_ Delta](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))4195584</span><span class="sxs-lookup"><span data-stu-id="80645-119">[PERF\_COUNTER\_LARGE\_DELTA](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4195584</span></span><br/> | <span data-ttu-id="80645-120">Identique au Delta de compteur de performances, \_ \_ mais une représentation 64 bits pour les valeurs plus élevées.</span><span class="sxs-lookup"><span data-stu-id="80645-120">Same as PERF\_COUNTER\_DELTA but a 64-bit representation for larger values.</span></span>                                                                                        |
| <span data-ttu-id="80645-121">[Performances \_ \_Temps écoulé](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))décimal 807666944</span><span class="sxs-lookup"><span data-stu-id="80645-121">[PERF\_ELAPSED\_TIME](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 807666944</span></span><br/>       | <span data-ttu-id="80645-122">Durée totale entre le démarrage du processus et l’heure à laquelle cette valeur est calculée.</span><span class="sxs-lookup"><span data-stu-id="80645-122">Total time between when the process started and the time when this value is calculated.</span></span>                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="80645-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="80645-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80645-124">Types de compteurs de performance WMI</span><span class="sxs-lookup"><span data-stu-id="80645-124">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> </dl>

 

