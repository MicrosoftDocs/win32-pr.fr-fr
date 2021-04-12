---
title: SystemMonitor. MinimumScale, propriété
description: Récupère ou définit la valeur minimale de l’axe vertical (Y) du graphique.
ms.assetid: 22dacfbf-27bb-48fe-b646-4cf17645a131
keywords:
- Propriété MinimumScale SysMon
- MinimumScale, propriété SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, propriété MinimumScale
topic_type:
- apiref
api_name:
- SystemMonitor.MinimumScale
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24f675e96ecdd4e547ca4a93b248556fd8c0539a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465214"
---
# <a name="systemmonitorminimumscale-property"></a><span data-ttu-id="5dd5c-106">SystemMonitor. MinimumScale, propriété</span><span class="sxs-lookup"><span data-stu-id="5dd5c-106">SystemMonitor.MinimumScale property</span></span>

<span data-ttu-id="5dd5c-107">Récupère ou définit la valeur minimale de l’axe vertical (Y) du graphique.</span><span class="sxs-lookup"><span data-stu-id="5dd5c-107">Retrieves or sets the minimum value of the vertical (Y) axis of the graph.</span></span>

<span data-ttu-id="5dd5c-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="5dd5c-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dd5c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5dd5c-109">Syntax</span></span>


```VB
Property MinimumScale As Long
```



## <a name="property-value"></a><span data-ttu-id="5dd5c-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="5dd5c-110">Property value</span></span>

<span data-ttu-id="5dd5c-111">Valeur minimale positive de l’axe vertical du graphique.</span><span class="sxs-lookup"><span data-stu-id="5dd5c-111">Positive minimum value of the vertical axis of the graph.</span></span> <span data-ttu-id="5dd5c-112">La valeur minimale par défaut de l’échelle verticale est 0.</span><span class="sxs-lookup"><span data-stu-id="5dd5c-112">The default minimum value of the vertical scale is 0.</span></span> <span data-ttu-id="5dd5c-113">La valeur la plus élevée que vous pouvez affecter à la valeur minimale est égale à une valeur inférieure à [**MaximumScale**](systemmonitor-maximumscale.md) .</span><span class="sxs-lookup"><span data-stu-id="5dd5c-113">The highest value that you can set the minimum value to is one less than [**MaximumScale**](systemmonitor-maximumscale.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5dd5c-114">Notes</span><span class="sxs-lookup"><span data-stu-id="5dd5c-114">Remarks</span></span>

<span data-ttu-id="5dd5c-115">Le contrôle ajuste automatiquement la position des nombres d’échelle affichés sur l’échelle verticale en fonction de la taille du contrôle affiché.</span><span class="sxs-lookup"><span data-stu-id="5dd5c-115">The control automatically adjusts the position of the scale numbers displayed on the vertical scale according to the size of the displayed control.</span></span>

## <a name="requirements"></a><span data-ttu-id="5dd5c-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5dd5c-116">Requirements</span></span>



| <span data-ttu-id="5dd5c-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5dd5c-117">Requirement</span></span> | <span data-ttu-id="5dd5c-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="5dd5c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5dd5c-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5dd5c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5dd5c-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5dd5c-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="5dd5c-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5dd5c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5dd5c-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5dd5c-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5dd5c-123">DLL</span><span class="sxs-lookup"><span data-stu-id="5dd5c-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5dd5c-124"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="5dd5c-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5dd5c-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5dd5c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dd5c-126">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="5dd5c-126">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="5dd5c-127">**SystemMonitor. MaximumScale**</span><span class="sxs-lookup"><span data-stu-id="5dd5c-127">**SystemMonitor.MaximumScale**</span></span>](systemmonitor-maximumscale.md)
</dt> <dt>

[<span data-ttu-id="5dd5c-128">**SystemMonitor.ShowScaleLabels**</span><span class="sxs-lookup"><span data-stu-id="5dd5c-128">**SystemMonitor.ShowScaleLabels**</span></span>](systemmonitor-showscalelabels.md)
</dt> </dl>

 

 





