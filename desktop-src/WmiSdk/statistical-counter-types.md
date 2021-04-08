---
description: Le Fournisseur de données performances au format de performances élevées de WMI calcule les types de compteurs statistiques sur un nombre spécifié d’exemples de données de compteurs brutes.
ms.assetid: a7e32ef2-fad1-449c-beee-07db4b93e3fe
ms.tgt_platform: multiple
title: Types de compteurs statistiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb97224b06881cbc3c8b1375c04a4df5be1095f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034839"
---
# <a name="statistical-counter-types"></a><span data-ttu-id="9bf15-103">Types de compteurs statistiques</span><span class="sxs-lookup"><span data-stu-id="9bf15-103">Statistical Counter Types</span></span>

<span data-ttu-id="9bf15-104">Le [fournisseur de données performances au format](formatted-performance-data-provider.md) de performances élevées de WMI calcule les types de compteurs statistiques sur un nombre spécifié d’exemples de données de compteurs brutes.</span><span class="sxs-lookup"><span data-stu-id="9bf15-104">The WMI high-performance [Formatted Performance Data Provider](formatted-performance-data-provider.md) calculates the statistical counter types on a specified number of raw counter data samples.</span></span> <span data-ttu-id="9bf15-105">Les algorithmes pour les types de compteurs ne requièrent pas de propriétés timestamp ou Frequency héritées (telles que **timestamp \_ PerfTime** ou **Frequency \_ PerfTime**) requises par d’autres types de compteurs.</span><span class="sxs-lookup"><span data-stu-id="9bf15-105">The algorithms for the counter types do not require inherited timestamp or frequency properties (such as **TimeStamp\_PerfTime** or **Frequency\_PerfTime**) that other counter types require.</span></span>

<span data-ttu-id="9bf15-106">Au lieu de cela, les types de compteurs statistiques prennent en charge un **qualificateur** qui identifie le nombre d’exemples à utiliser.</span><span class="sxs-lookup"><span data-stu-id="9bf15-106">Instead, the statistical counter types support a **qualifier** that identifies how many samples to use.</span></span> <span data-ttu-id="9bf15-107">Un échantillon est collecté lorsque la méthode [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) est appelée pour l’objet de performance.</span><span class="sxs-lookup"><span data-stu-id="9bf15-107">A sample is collected when the [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method is called for the performance object.</span></span> <span data-ttu-id="9bf15-108">Pour les scripts, utilisez la méthode [**SWbemRefresher. Refresh**](swbemrefresher-refresh.md) .</span><span class="sxs-lookup"><span data-stu-id="9bf15-108">For scripts use the [**SWbemRefresher.Refresh**](swbemrefresher-refresh.md) method.</span></span> <span data-ttu-id="9bf15-109">Les données calculées contiennent le résultat du calcul effectué sur le nombre d’échantillons **SampleWindow** à partir de la propriété de données brutes.</span><span class="sxs-lookup"><span data-stu-id="9bf15-109">The calculated data contains the result of the calculation performed on the **SampleWindow** number of samples from the raw data property.</span></span> <span data-ttu-id="9bf15-110">Les données brutes du calcul sont fournies par le nom de propriété spécifié dans le qualificateur de **compteur** .</span><span class="sxs-lookup"><span data-stu-id="9bf15-110">The raw data for the calculation comes frm the property name specified in the **Counter** qualifier.</span></span>

<span data-ttu-id="9bf15-111">Pour plus d’informations, consultez [obtention de données de performances statistiques](obtaining-statistical-performance-data.md) et [accès aux classes de performances préinstallées de WMI](accessing-wmi-preinstalled-performance-classes.md).</span><span class="sxs-lookup"><span data-stu-id="9bf15-111">For more information, see [Obtaining Statistical Performance Data](obtaining-statistical-performance-data.md) and [Accessing WMI Preinstalled Performance Classes](accessing-wmi-preinstalled-performance-classes.md).</span></span>



| <span data-ttu-id="9bf15-112">@, Constante</span><span class="sxs-lookup"><span data-stu-id="9bf15-112">CounterType Constant</span></span>                    | <span data-ttu-id="9bf15-113">Description</span><span class="sxs-lookup"><span data-stu-id="9bf15-113">Description</span></span>                                                                                                                                                                                |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9bf15-114">moyenne de cuiseur \_</span><span class="sxs-lookup"><span data-stu-id="9bf15-114">COOKER\_AVERAGE</span></span>](cooker-average.md)   | <span data-ttu-id="9bf15-115">Additionne les observations répétées d’une propriété dans une classe [**\_ PerfRawData Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) et divise la somme par le nombre d’observations.</span><span class="sxs-lookup"><span data-stu-id="9bf15-115">Sums repeated observations of one property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class and divides the sum by the number of observations.</span></span>                              |
| [<span data-ttu-id="9bf15-116">maximum de cuiseur \_</span><span class="sxs-lookup"><span data-stu-id="9bf15-116">COOKER\_MAX</span></span>](cooker-max.md)           | <span data-ttu-id="9bf15-117">Plus grande valeur d’un ensemble d’observations d’une propriété dans une classe [**\_ PerfRawData Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .</span><span class="sxs-lookup"><span data-stu-id="9bf15-117">Largest value from a set of observations of a property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class.</span></span>                                                                    |
| [<span data-ttu-id="9bf15-118">minimum de cuiseur \_</span><span class="sxs-lookup"><span data-stu-id="9bf15-118">COOKER\_MIN</span></span>](cooker-min.md)           | <span data-ttu-id="9bf15-119">Plus petite valeur d’un ensemble d’observations d’une propriété dans une [**classe \_ PerfRawData Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .</span><span class="sxs-lookup"><span data-stu-id="9bf15-119">Smallest value from a set of observations of a property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class.</span></span>                                                                   |
| [<span data-ttu-id="9bf15-120">plage de cuiseur \_</span><span class="sxs-lookup"><span data-stu-id="9bf15-120">COOKER\_RANGE</span></span>](cooker-range.md)       | <span data-ttu-id="9bf15-121">Différence entre les valeurs [minimale](cooker-min.md) et [maximale](cooker-max.md) pour un ensemble d’observations brutes d’une propriété dans une classe [**\_ PerfRawData Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .</span><span class="sxs-lookup"><span data-stu-id="9bf15-121">Difference between the [Min](cooker-min.md) and [Max](cooker-max.md) values for a set of raw observations of a property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class.</span></span> |
| [<span data-ttu-id="9bf15-122">VARIANCE de la cuiseur \_</span><span class="sxs-lookup"><span data-stu-id="9bf15-122">COOKER\_VARIANCE</span></span>](cooker-variance.md) | <span data-ttu-id="9bf15-123">Mesure de variabilité qui peut être utilisée pour caractériser la dispersion d’un jeu d’observations brutes d’une propriété dans une classe [**\_ PerfRawData Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .</span><span class="sxs-lookup"><span data-stu-id="9bf15-123">Measure of variability that can be used to characterize dispersion for a set of raw observations of a property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="9bf15-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9bf15-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bf15-125">Types de compteurs de performance WMI</span><span class="sxs-lookup"><span data-stu-id="9bf15-125">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> <dt>

[<span data-ttu-id="9bf15-126">Analyse des données de performances</span><span class="sxs-lookup"><span data-stu-id="9bf15-126">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> <dt>

[<span data-ttu-id="9bf15-127">Actualisation des données WMI dans les scripts</span><span class="sxs-lookup"><span data-stu-id="9bf15-127">Refreshing WMI Data in Scripts</span></span>](refreshing-wmi-data-in-scripts.md)
</dt> <dt>

[<span data-ttu-id="9bf15-128">Accès aux données de performances dans le script</span><span class="sxs-lookup"><span data-stu-id="9bf15-128">Accessing Performance Data in Script</span></span>](accessing-performance-data-in-script.md)
</dt> <dt>

[<span data-ttu-id="9bf15-129">Accès aux données de performances en C++</span><span class="sxs-lookup"><span data-stu-id="9bf15-129">Accessing Performance Data in C++</span></span>](accessing-performance-data-in-c--.md)
</dt> </dl>

 

 
