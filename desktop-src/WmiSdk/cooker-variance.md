---
description: La formule de type de compteur de variance de cuiseur \_ fournit la variabilité qui utilise pour caractériser la dispersion d’un jeu d’observations brutes d’une propriété dans une \_ instance de PerfRawData Win32.
ms.assetid: 6b184a36-7d22-41ab-98e7-b185d1063bcb
ms.tgt_platform: multiple
title: COOKER_VARIANCE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef0f9de6c5241ccd486e4da76864139e3e54f5a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034312"
---
# <a name="cooker_variance"></a><span data-ttu-id="19024-103">VARIANCE de la cuiseur \_</span><span class="sxs-lookup"><span data-stu-id="19024-103">COOKER\_VARIANCE</span></span>

<span data-ttu-id="19024-104">La formule de type de compteur de variance de cuiseur \_ fournit la variabilité qui utilise pour caractériser la dispersion d’un jeu d’observations brutes d’une propriété dans une instance de [**\_ PerfRawData Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .</span><span class="sxs-lookup"><span data-stu-id="19024-104">The COOKER\_VARIANCE counter type formula provides variability that use to characterize dispersion for a set of raw observations of one property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) instance.</span></span> <span data-ttu-id="19024-105">La variance est calculée en divisant la somme du carré de l’écart par la moyenne de chaque compteur par le nombre de compteurs.</span><span class="sxs-lookup"><span data-stu-id="19024-105">The variance is calculated by dividing the sum of the square of the deviation from the mean of each counter by the number of counters.</span></span> <span data-ttu-id="19024-106">En d’autres termes, la variance est la moyenne des écarts au carré de la moyenne pour chaque compteur.</span><span class="sxs-lookup"><span data-stu-id="19024-106">In other words, the variance is the average of the squared deviations from the mean for each counter.</span></span> <span data-ttu-id="19024-107">Ce type de compteur est défini uniquement dans WMI et n’est pas disponible pour les technologies d’analyse des performances, telles que les [compteurs de performance Version 6,0](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="19024-107">This counter type is defined only within WMI, and it is not available to the performance monitoring technologies, such as [Performance Counters Version 6.0](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

<span data-ttu-id="19024-108">Pour plus d’informations sur la formule de type de compteur, consultez [types de compteurs](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="19024-108">For more information about the counter type formula, see [Counter Types](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)).</span></span>

<span data-ttu-id="19024-109">Pour plus d’informations sur les fournisseurs et les scripts à hautes performances, consultez [types de compteurs de performance WMI](wmi-performance-counter-types.md).</span><span class="sxs-lookup"><span data-stu-id="19024-109">For more information about high-performance providers and scripting, see [WMI Performance Counter Types](wmi-performance-counter-types.md).</span></span>

## <a name="example-code"></a><span data-ttu-id="19024-110">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="19024-110">Example Code</span></span>

<span data-ttu-id="19024-111">Pour obtenir des exemples de code, consultez [obtention de données de performances statistiques](obtaining-statistical-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="19024-111">For code examples, see [Obtaining Statistical Performance Data](obtaining-statistical-performance-data.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="19024-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="19024-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19024-113">Types de compteurs statistiques</span><span class="sxs-lookup"><span data-stu-id="19024-113">Statistical Counter Types</span></span>](statistical-counter-types.md)
</dt> <dt>

[<span data-ttu-id="19024-114">Analyse des données de performances</span><span class="sxs-lookup"><span data-stu-id="19024-114">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
