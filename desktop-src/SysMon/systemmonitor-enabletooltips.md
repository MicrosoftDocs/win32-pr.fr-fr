---
title: SystemMonitor. EnableToolTips, propriété
description: Récupère ou définit une valeur qui détermine si une info-bulle est affichée lorsque la souris pointe sur un compteur dans l’une des vues de graphique (non prise en charge pour la vue rapport).
ms.assetid: af9a78ea-a9de-4343-8978-4316769a5f30
keywords:
- Propriété EnableToolTips SysMon
- Propriété EnableToolTips SysMon, objet SystemMonitor
- Objet SystemMonitor SysMon, propriété EnableToolTips
topic_type:
- apiref
api_name:
- SystemMonitor.EnableToolTips
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 757cdd8a54bf6e5ae6e70b82dfc30865c796f944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510966"
---
# <a name="systemmonitorenabletooltips-property"></a><span data-ttu-id="5dcff-106">SystemMonitor. EnableToolTips, propriété</span><span class="sxs-lookup"><span data-stu-id="5dcff-106">SystemMonitor.EnableToolTips property</span></span>

<span data-ttu-id="5dcff-107">Récupère ou définit une valeur qui détermine si une info-bulle est affichée lorsque la souris pointe sur un compteur dans l’une des vues de graphique (non prise en charge pour la vue rapport).</span><span class="sxs-lookup"><span data-stu-id="5dcff-107">Retrieves or sets a value that determines if a tool tip is shown when the mouse hovers over a counter in one of the graph views (not supported for report view).</span></span>

## <a name="syntax"></a><span data-ttu-id="5dcff-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5dcff-108">Syntax</span></span>


```VB
Property EnableToolTips As Boolean
```



## <a name="property-value"></a><span data-ttu-id="5dcff-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="5dcff-109">Property value</span></span>

<span data-ttu-id="5dcff-110">True affiche une info-bulle avec les informations de compteur. Sinon, false.</span><span class="sxs-lookup"><span data-stu-id="5dcff-110">True displays a tool tip with the counter information in it; otherwise, False.</span></span>

## <a name="remarks"></a><span data-ttu-id="5dcff-111">Notes</span><span class="sxs-lookup"><span data-stu-id="5dcff-111">Remarks</span></span>

<span data-ttu-id="5dcff-112">Pour les graphiques linéaires, l’info-bulle est ancrée au point de données le plus proche de la souris.</span><span class="sxs-lookup"><span data-stu-id="5dcff-112">For line graphs, the tool tip is anchored to the data point that is closest to the mouse.</span></span> <span data-ttu-id="5dcff-113">Pour les graphiques à barres et les histogrammes, l’info-bulle représente la valeur totale des données de la barre, et non un point dans la barre.</span><span class="sxs-lookup"><span data-stu-id="5dcff-113">For bar charts and histograms, the tool tip represents the total data value of the bar, not a point within the bar.</span></span>

<span data-ttu-id="5dcff-114">L’info-bulle contient différentes informations basées sur la source de données.</span><span class="sxs-lookup"><span data-stu-id="5dcff-114">The tool tip contains different information based upon the data source.</span></span> <span data-ttu-id="5dcff-115">Pour les fichiers journaux, l’info-bulle contient le chemin de compteur, la valeur de compteur, l’horodatage, le nombre d’échantillons de données inclus dans le point de données, ainsi que les valeurs de données minimale et maximale.</span><span class="sxs-lookup"><span data-stu-id="5dcff-115">For log files, the tool tip contains the counter path, counter value, time stamp, number of data samples included in the data point, and the minimum and maximum data values.</span></span>

<span data-ttu-id="5dcff-116">Pour une activité en temps réel, l’info-bulle contient le chemin de compteur, la valeur de compteur et l’horodatage.</span><span class="sxs-lookup"><span data-stu-id="5dcff-116">For real time activity, the tool tip contains the counter path, counter value, and time stamp.</span></span>

## <a name="requirements"></a><span data-ttu-id="5dcff-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5dcff-117">Requirements</span></span>



| <span data-ttu-id="5dcff-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5dcff-118">Requirement</span></span> | <span data-ttu-id="5dcff-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="5dcff-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5dcff-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5dcff-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5dcff-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5dcff-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5dcff-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5dcff-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5dcff-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5dcff-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5dcff-124">DLL</span><span class="sxs-lookup"><span data-stu-id="5dcff-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5dcff-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="5dcff-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





