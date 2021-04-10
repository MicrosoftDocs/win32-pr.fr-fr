---
description: Le type de compteur de performance désigne une formule requise pour obtenir des compteurs de performance calculés. Il s’agit des mêmes types de compteurs que ceux utilisés par l’analyse des performances Windows.
ms.assetid: d4a9feca-80a2-4ce5-b4d7-4e83ef951c08
ms.tgt_platform: multiple
title: Types de compteurs de performance WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12ac0d2c8afb1499fec44c983364b5e3278b864
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115031"
---
# <a name="wmi-performance-counter-types"></a><span data-ttu-id="53b66-104">Types de compteurs de performance WMI</span><span class="sxs-lookup"><span data-stu-id="53b66-104">WMI Performance Counter Types</span></span>

<span data-ttu-id="53b66-105">Le [type de compteur](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) de performance désigne une formule requise pour obtenir des compteurs de performance calculés.</span><span class="sxs-lookup"><span data-stu-id="53b66-105">The performance [counter type](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) designates a formula required to obtain calculated performance counters.</span></span> <span data-ttu-id="53b66-106">Il s’agit des mêmes types de compteurs que ceux utilisés par l' [analyse des performances](/windows/desktop/PerfCtrs/performance-counters-portal)Windows.</span><span class="sxs-lookup"><span data-stu-id="53b66-106">These are the same counter types used by Windows [Performance Monitoring](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span> <span data-ttu-id="53b66-107">Dans les classes de performance WMI, les données brutes pour la formule de type de compteur proviennent d’une classe [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) et le résultat calculé est trouvé dans la même propriété de nom d’une classe [**\_ PerfFormattedData Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) correspondante.</span><span class="sxs-lookup"><span data-stu-id="53b66-107">In WMI performance classes, the raw data for the counter type formula comes from a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class and the calculated result is found in the same-named property of a corresponding [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) class.</span></span>

<span data-ttu-id="53b66-108">Les types de compteurs s’affichent en tant **que qualificateur «** pas » pour les propriétés dans les classes [**\_ PerfRawData Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) et comme qualificateur **CookingType** pour les propriétés dans les classes [**\_ PerfFormattedData Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) .</span><span class="sxs-lookup"><span data-stu-id="53b66-108">Counter types appear as the **CounterType** qualifier for properties in [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes, and as the **CookingType** qualifier for properties in [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) classes.</span></span>

<span data-ttu-id="53b66-109">Par exemple, la propriété **AvgDiskBytesPerRead** de la [**classe \_ \_ \_ disque logique Win32 PerfRawData Perfdisk**](./retrieving-raw-and-formatted-performance-data.md) est la source de données brute pour la propriété **AvgDiskBytesPerRead** dans la classe [**\_ \_ \_ disque logique Win32 PerfFormattedData Perfdisk**](./retrieving-raw-and-formatted-performance-data.md), qui contient les mêmes données que celles affichées dans le moniteur système.</span><span class="sxs-lookup"><span data-stu-id="53b66-109">For example, the **AvgDiskBytesPerRead** property in the [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) class is the raw data source for the **AvgDiskBytesPerRead** property in the class [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md), which contains the same data as shown in System Monitor.</span></span>

<span data-ttu-id="53b66-110">La liste suivante organise les descriptions de type de compteur par type fonctionnel :</span><span class="sxs-lookup"><span data-stu-id="53b66-110">The following list organizes counter type descriptions by functional type:</span></span>

-   [<span data-ttu-id="53b66-111">Types de compteurs de base</span><span class="sxs-lookup"><span data-stu-id="53b66-111">Base Counter Types</span></span>](base-counter-types.md)
-   [<span data-ttu-id="53b66-112">Types de compteurs de l’algorithme de base</span><span class="sxs-lookup"><span data-stu-id="53b66-112">Basic Algorithm Counter Types</span></span>](basic-algorithm-counter-types.md)
-   [<span data-ttu-id="53b66-113">Types de compteurs d’algorithmes de compteur</span><span class="sxs-lookup"><span data-stu-id="53b66-113">Counter Algorithm Counter Types</span></span>](counter-algorithm-counter-types.md)
-   [<span data-ttu-id="53b66-114">Types de compteurs décalculés</span><span class="sxs-lookup"><span data-stu-id="53b66-114">Noncomputational Counter Types</span></span>](noncomputational-counter-types.md)
-   [<span data-ttu-id="53b66-115">Types de compteurs de l’algorithme du minuteur de précision</span><span class="sxs-lookup"><span data-stu-id="53b66-115">Precision Timer Algorithm Counter Types</span></span>](precision-timer-algorithm-counter-types.md)
-   [<span data-ttu-id="53b66-116">Types de compteurs d’algorithmes de longueur de file d’attente</span><span class="sxs-lookup"><span data-stu-id="53b66-116">Queue-length Algorithm Counter Types</span></span>](queue-length-algorithm-counter-types.md)
-   [<span data-ttu-id="53b66-117">Types de compteurs statistiques</span><span class="sxs-lookup"><span data-stu-id="53b66-117">Statistical Counter Types</span></span>](statistical-counter-types.md)
-   [<span data-ttu-id="53b66-118">Types de compteurs de l’algorithme Timer</span><span class="sxs-lookup"><span data-stu-id="53b66-118">Timer Algorithm Counter Types</span></span>](timer-algorithm-counter-types.md)

 

 
