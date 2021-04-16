---
title: Nouveautés du moniteur système
description: Le tableau suivant identifie les nouveautés de chaque version du moniteur système (SYSMON).
ms.assetid: 9cb0e0db-0933-4993-a995-74a36a24eccb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b3662e83954630232e3fe30c26a3f6d94aa9cc7
ms.sourcegitcommit: 780d4b1601c45658ef0b799b80d13f45a53d808d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/26/2020
ms.locfileid: "104381620"
---
# <a name="whats-new-in-system-monitor"></a><span data-ttu-id="6e844-103">Nouveautés du moniteur système</span><span class="sxs-lookup"><span data-stu-id="6e844-103">What's New in System Monitor</span></span>

<span data-ttu-id="6e844-104">Le tableau suivant identifie les nouveautés de chaque version du moniteur système (SYSMON).</span><span class="sxs-lookup"><span data-stu-id="6e844-104">The following table identifies what is new for each release of System Monitor (SYSMON).</span></span>



| <span data-ttu-id="6e844-105">Version</span><span class="sxs-lookup"><span data-stu-id="6e844-105">Version</span></span>     | <span data-ttu-id="6e844-106">Description des fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="6e844-106">Description of features</span></span>                                                                                                                                                                                                                                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e844-107">Version 3.7</span><span class="sxs-lookup"><span data-stu-id="6e844-107">Version 3.7</span></span> | <span data-ttu-id="6e844-108">Cette version ajoute de nouveaux types de graphiques, la possibilité de sélectionner plusieurs compteurs, de récupérer des valeurs de compteur à partir d’un point sur le graphique, d’enregistrer les valeurs de compteur sous forme de graphique dans un fichier journal, et l’option permettant de faire défiler continuellement un graphique linéaire dans la fenêtre du graphique au lieu de s’habiller sur lui-même. Inclus dans Windows Server 2008 et Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6e844-108">This version adds new graph types, the ability to select multiple counters, retrieve counter values from a point on the graph, save graphed counter values to a log file, and the option to have a line graph continuously scroll in the graph window instead of wrap-around on itself.Included in Windows Server 2008 and Windows Vista.</span></span><br/> |



 

## <a name="version-37"></a><span data-ttu-id="6e844-109">Version 3.7</span><span class="sxs-lookup"><span data-stu-id="6e844-109">Version 3.7</span></span>

<span data-ttu-id="6e844-110">Nouvelles propriétés et méthodes qui ont été ajoutées à [**CounterItem**](counteritem.md).</span><span class="sxs-lookup"><span data-stu-id="6e844-110">New properties and methods that were added to [**CounterItem**](counteritem.md).</span></span>

-   [<span data-ttu-id="6e844-111">**GetDataAt**</span><span class="sxs-lookup"><span data-stu-id="6e844-111">**GetDataAt**</span></span>](counteritem-getdataat.md)
-   [<span data-ttu-id="6e844-112">**Sélectionné**</span><span class="sxs-lookup"><span data-stu-id="6e844-112">**Selected**</span></span>](counteritem-selected.md)
-   [<span data-ttu-id="6e844-113">**Parent**</span><span class="sxs-lookup"><span data-stu-id="6e844-113">**Visible**</span></span>](counteritem-visible.md)
-   <span data-ttu-id="6e844-114">Plage de valeurs valides modifiées pour [ **CounterItem. Width**](counteritem-width.md)</span><span class="sxs-lookup"><span data-stu-id="6e844-114">Range of valid values changed for [**CounterItem.Width**](counteritem-width.md)</span></span>

<span data-ttu-id="6e844-115">Nouvelles propriétés et méthodes qui ont été ajoutées à [**systemmonitor**](systemmonitor.md).</span><span class="sxs-lookup"><span data-stu-id="6e844-115">New properties and methods that were added to [**SystemMonitor**](systemmonitor.md).</span></span>

-   [<span data-ttu-id="6e844-116">**BatchingLock**</span><span class="sxs-lookup"><span data-stu-id="6e844-116">**BatchingLock**</span></span>](systemmonitor-batchinglock.md)
-   [<span data-ttu-id="6e844-117">**ChartScroll**</span><span class="sxs-lookup"><span data-stu-id="6e844-117">**ChartScroll**</span></span>](systemmonitor-chartscroll.md)
-   [<span data-ttu-id="6e844-118">**ClearData**</span><span class="sxs-lookup"><span data-stu-id="6e844-118">**ClearData**</span></span>](systemmonitor-cleardata.md)
-   [<span data-ttu-id="6e844-119">**DataPointCount**</span><span class="sxs-lookup"><span data-stu-id="6e844-119">**DataPointCount**</span></span>](systemmonitor-datapointcount.md)
-   [<span data-ttu-id="6e844-120">**EnableDigitGrouping**</span><span class="sxs-lookup"><span data-stu-id="6e844-120">**EnableDigitGrouping**</span></span>](systemmonitor-enabledigitgrouping.md)
-   [<span data-ttu-id="6e844-121">**EnableToolTips**</span><span class="sxs-lookup"><span data-stu-id="6e844-121">**EnableToolTips**</span></span>](systemmonitor-enabletooltips.md)
-   [<span data-ttu-id="6e844-122">**GetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="6e844-122">**GetLogViewRange**</span></span>](systemmonitor-getlogviewrange.md)
-   [<span data-ttu-id="6e844-123">**LoadSettings**</span><span class="sxs-lookup"><span data-stu-id="6e844-123">**LoadSettings**</span></span>](systemmonitor-loadsettings.md)
-   [<span data-ttu-id="6e844-124">**LogSourceStartTime**</span><span class="sxs-lookup"><span data-stu-id="6e844-124">**LogSourceStartTime**</span></span>](systemmonitor-logsourcestarttime.md)
-   [<span data-ttu-id="6e844-125">**LogSourceStopTime**</span><span class="sxs-lookup"><span data-stu-id="6e844-125">**LogSourceStopTime**</span></span>](systemmonitor-logsourcestoptime.md)
-   [<span data-ttu-id="6e844-126">**Rejournaliser**</span><span class="sxs-lookup"><span data-stu-id="6e844-126">**Relog**</span></span>](systemmonitor-relog.md)
-   [<span data-ttu-id="6e844-127">**SaveAs**</span><span class="sxs-lookup"><span data-stu-id="6e844-127">**SaveAs**</span></span>](systemmonitor-saveas.md)
-   [<span data-ttu-id="6e844-128">**ScaleToFit**</span><span class="sxs-lookup"><span data-stu-id="6e844-128">**ScaleToFit**</span></span>](systemmonitor-scaletofit.md)
-   [<span data-ttu-id="6e844-129">**SetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="6e844-129">**SetLogViewRange**</span></span>](systemmonitor-setlogviewrange.md)
-   [<span data-ttu-id="6e844-130">**ShowTimeAxisLables**</span><span class="sxs-lookup"><span data-stu-id="6e844-130">**ShowTimeAxisLables**</span></span>](systemmonitor-showtimeaxislabels.md)

<span data-ttu-id="6e844-131">Nouvelles énumérations qui ont été ajoutées.</span><span class="sxs-lookup"><span data-stu-id="6e844-131">New enumerations that were added.</span></span>

-   [<span data-ttu-id="6e844-132">**SysmonDataType**</span><span class="sxs-lookup"><span data-stu-id="6e844-132">**SysmonDataType**</span></span>](/windows/win32/api/isysmon/ne-isysmon-sysmondatatype)
-   [<span data-ttu-id="6e844-133">**SysmonFileType**</span><span class="sxs-lookup"><span data-stu-id="6e844-133">**SysmonFileType**</span></span>](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype)
-   <span data-ttu-id="6e844-134">De nouvelles valeurs de type d’affichage ont été ajoutées à [ **DisplayTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants)</span><span class="sxs-lookup"><span data-stu-id="6e844-134">New display type values were added to [**DisplayTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants)</span></span>

 

 





