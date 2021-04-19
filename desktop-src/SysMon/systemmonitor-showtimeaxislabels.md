---
title: SystemMonitor. ShowTimeAxisLabels, propriété
description: Récupère ou définit une valeur qui détermine si l’axe horizontal (X) de la vue du graphique contient des étiquettes.
ms.assetid: 9e9d2d2c-f053-4afe-85de-25242842498f
keywords:
- Propriété ShowTimeAxisLabels SysMon
- Propriété ShowTimeAxisLabels SysMon, objet SystemMonitor
- Objet SystemMonitor SysMon, propriété ShowTimeAxisLabels
topic_type:
- apiref
api_name:
- SystemMonitor.ShowTimeAxisLabels
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06569dcd4702ae687b09bfae88c84482a49afb71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106538808"
---
# <a name="systemmonitorshowtimeaxislabels-property"></a><span data-ttu-id="a804e-106">SystemMonitor. ShowTimeAxisLabels, propriété</span><span class="sxs-lookup"><span data-stu-id="a804e-106">SystemMonitor.ShowTimeAxisLabels property</span></span>

<span data-ttu-id="a804e-107">Récupère ou définit une valeur qui détermine si l’axe horizontal (X) de la vue du graphique contient des étiquettes.</span><span class="sxs-lookup"><span data-stu-id="a804e-107">Retrieves or sets a value that determines if the horizontal (X) axis of the graph view contains labels.</span></span>

## <a name="syntax"></a><span data-ttu-id="a804e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a804e-108">Syntax</span></span>


```VB
Property ShowTimeAxisLabels As Boolean
```



## <a name="property-value"></a><span data-ttu-id="a804e-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a804e-109">Property value</span></span>

<span data-ttu-id="a804e-110">La valeur true applique des étiquettes à l’axe des x.</span><span class="sxs-lookup"><span data-stu-id="a804e-110">A value of True will apply labels to the x-axis.</span></span> <span data-ttu-id="a804e-111">La valeur false ne l’est pas.</span><span class="sxs-lookup"><span data-stu-id="a804e-111">A value of False will not.</span></span> <span data-ttu-id="a804e-112">La valeur par défaut est False.</span><span class="sxs-lookup"><span data-stu-id="a804e-112">The default is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="a804e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="a804e-113">Remarks</span></span>

<span data-ttu-id="a804e-114">SYSMON ignore cette propriété pour les graphiques à barres, les rapports et les histogrammes.</span><span class="sxs-lookup"><span data-stu-id="a804e-114">SYSMON ignores this property for bar graphs, reports and histograms.</span></span>

<span data-ttu-id="a804e-115">Pour les graphiques linéaires, SYSMON utilise l’heure à laquelle la valeur de compteur a été échantillonnée comme étiquette.</span><span class="sxs-lookup"><span data-stu-id="a804e-115">For line graphs, SYSMON uses the time that the counter value was sampled as the label.</span></span>

## <a name="requirements"></a><span data-ttu-id="a804e-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a804e-116">Requirements</span></span>



| <span data-ttu-id="a804e-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a804e-117">Requirement</span></span> | <span data-ttu-id="a804e-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="a804e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a804e-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a804e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a804e-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a804e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a804e-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a804e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a804e-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a804e-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a804e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="a804e-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a804e-124"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="a804e-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





