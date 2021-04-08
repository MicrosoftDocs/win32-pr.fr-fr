---
title: SystemMonitor. MaximumScale, propriété
description: Récupère ou définit la valeur maximale de l’axe vertical (Y) du graphique.
ms.assetid: 305886e3-2586-47c7-a888-6e393580c456
keywords:
- Propriété MaximumScale SysMon
- Propriété MaximumScale SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, propriété MaximumScale
topic_type:
- apiref
api_name:
- SystemMonitor.MaximumScale
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37740802fac4d89bbcbe9d5c105e357b55ab481
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941995"
---
# <a name="systemmonitormaximumscale-property"></a><span data-ttu-id="a176c-106">SystemMonitor. MaximumScale, propriété</span><span class="sxs-lookup"><span data-stu-id="a176c-106">SystemMonitor.MaximumScale property</span></span>

<span data-ttu-id="a176c-107">Récupère ou définit la valeur maximale de l’axe vertical (Y) du graphique.</span><span class="sxs-lookup"><span data-stu-id="a176c-107">Retrieves or sets the maximum value of the vertical (Y) axis of the graph.</span></span>

<span data-ttu-id="a176c-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a176c-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a176c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a176c-109">Syntax</span></span>


```VB
Property MaximumScale As Long
```



## <a name="property-value"></a><span data-ttu-id="a176c-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a176c-110">Property value</span></span>

<span data-ttu-id="a176c-111">Valeur maximale positive de l’axe vertical du graphique.</span><span class="sxs-lookup"><span data-stu-id="a176c-111">Positive maximum value of the vertical axis of the graph.</span></span> <span data-ttu-id="a176c-112">La valeur maximale par défaut de l’échelle verticale est 100.</span><span class="sxs-lookup"><span data-stu-id="a176c-112">The default maximum value of the vertical scale is 100.</span></span> <span data-ttu-id="a176c-113">La valeur la plus basse que vous pouvez affecter à la valeur maximale est supérieure d’une unité à la valeur [**MinimumScale**](systemmonitor-minimumscale.md) .</span><span class="sxs-lookup"><span data-stu-id="a176c-113">The lowest value that you can set the maximum value to is one more than the [**MinimumScale**](systemmonitor-minimumscale.md) value.</span></span> <span data-ttu-id="a176c-114">La valeur la plus élevée que vous pouvez affecter à la valeur maximale est 999 999 999.</span><span class="sxs-lookup"><span data-stu-id="a176c-114">The highest value that you can set the maximum value to is 999,999,999.</span></span>

## <a name="remarks"></a><span data-ttu-id="a176c-115">Notes</span><span class="sxs-lookup"><span data-stu-id="a176c-115">Remarks</span></span>

<span data-ttu-id="a176c-116">Le contrôle ajuste automatiquement la position des nombres d’échelle affichés sur l’échelle verticale en fonction de la taille du contrôle affiché.</span><span class="sxs-lookup"><span data-stu-id="a176c-116">The control automatically adjusts the position of the scale numbers displayed on the vertical scale according to the size of the displayed control.</span></span>

## <a name="requirements"></a><span data-ttu-id="a176c-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a176c-117">Requirements</span></span>



| <span data-ttu-id="a176c-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a176c-118">Requirement</span></span> | <span data-ttu-id="a176c-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="a176c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a176c-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a176c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a176c-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a176c-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="a176c-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a176c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a176c-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a176c-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a176c-124">DLL</span><span class="sxs-lookup"><span data-stu-id="a176c-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a176c-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="a176c-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a176c-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a176c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a176c-127">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="a176c-127">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="a176c-128">**SystemMonitor. MinimumScale**</span><span class="sxs-lookup"><span data-stu-id="a176c-128">**SystemMonitor.MinimumScale**</span></span>](systemmonitor-minimumscale.md)
</dt> <dt>

[<span data-ttu-id="a176c-129">**SystemMonitor.ShowScaleLabels**</span><span class="sxs-lookup"><span data-stu-id="a176c-129">**SystemMonitor.ShowScaleLabels**</span></span>](systemmonitor-showscalelabels.md)
</dt> </dl>

 

 





