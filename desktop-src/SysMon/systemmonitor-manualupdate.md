---
title: SystemMonitor. ManualUpdate, propriété
description: Récupère ou définit une valeur indiquant si le contenu du moniteur système est mis à jour manuellement ou automatiquement à des intervalles spécifiés.
ms.assetid: e068a955-ec1d-4f93-9261-25ba87773913
keywords:
- Propriété ManualUpdate SysMon
- Propriété ManualUpdate SysMon, classe SystemMonitor
- SystemMonitor classe SysMon, propriété ManualUpdate
topic_type:
- apiref
api_name:
- SystemMonitor.ManualUpdate
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d1ecb426b47ba9cb7ec50b737f4f32d5ce274eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512388"
---
# <a name="systemmonitormanualupdate-property"></a><span data-ttu-id="eb8df-106">SystemMonitor. ManualUpdate, propriété</span><span class="sxs-lookup"><span data-stu-id="eb8df-106">SystemMonitor.ManualUpdate property</span></span>

<span data-ttu-id="eb8df-107">Récupère ou définit une valeur indiquant si le contenu du moniteur système est mis à jour manuellement ou automatiquement à des intervalles spécifiés.</span><span class="sxs-lookup"><span data-stu-id="eb8df-107">Retrieves or sets a value indicating whether the contents of the System Monitor will be updated manually, or automatically at specified intervals.</span></span>

<span data-ttu-id="eb8df-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="eb8df-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb8df-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb8df-109">Syntax</span></span>


```VB
Property ManualUpdate As Boolean
```



## <a name="property-value"></a><span data-ttu-id="eb8df-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="eb8df-110">Property value</span></span>

<span data-ttu-id="eb8df-111">La valeur true indique que le graphique est mis à jour manuellement.</span><span class="sxs-lookup"><span data-stu-id="eb8df-111">True indicates that graph is updated manually.</span></span> <span data-ttu-id="eb8df-112">False indique que le graphique est mis à jour automatiquement en fonction de l’intervalle de mise à jour spécifié dans [**systemmonitor. UpdateInterval**](systemmonitor-updateinterval.md).</span><span class="sxs-lookup"><span data-stu-id="eb8df-112">False indicates that the graph is updated automatically based on the update interval specified in [**SystemMonitor.UpdateInterval**](systemmonitor-updateinterval.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="eb8df-113">Notes</span><span class="sxs-lookup"><span data-stu-id="eb8df-113">Remarks</span></span>

<span data-ttu-id="eb8df-114">Par défaut, le graphique est mis à jour automatiquement.</span><span class="sxs-lookup"><span data-stu-id="eb8df-114">By default, the graph is updated automatically.</span></span>

<span data-ttu-id="eb8df-115">Pour mettre à jour le graphique manuellement, appelez la méthode [**systemmonitor. CollectSample**](systemmonitor-collectsample.md) .</span><span class="sxs-lookup"><span data-stu-id="eb8df-115">To update the graph manually, call the [**SystemMonitor.CollectSample**](systemmonitor-collectsample.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb8df-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb8df-116">Requirements</span></span>



| <span data-ttu-id="eb8df-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb8df-117">Requirement</span></span> | <span data-ttu-id="eb8df-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb8df-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eb8df-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb8df-119">Minimum supported client</span></span><br/> | <span data-ttu-id="eb8df-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eb8df-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="eb8df-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb8df-121">Minimum supported server</span></span><br/> | <span data-ttu-id="eb8df-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eb8df-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eb8df-123">DLL</span><span class="sxs-lookup"><span data-stu-id="eb8df-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb8df-124"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="eb8df-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb8df-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb8df-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb8df-126">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="eb8df-126">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="eb8df-127">**SystemMonitor.CollectSample**</span><span class="sxs-lookup"><span data-stu-id="eb8df-127">**SystemMonitor.CollectSample**</span></span>](systemmonitor-collectsample.md)
</dt> <dt>

[<span data-ttu-id="eb8df-128">**SystemMonitor.UpdateGraph**</span><span class="sxs-lookup"><span data-stu-id="eb8df-128">**SystemMonitor.UpdateGraph**</span></span>](systemmonitor-updategraph.md)
</dt> </dl>

 

 





