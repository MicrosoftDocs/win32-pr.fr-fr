---
title: SystemMonitor. UpdateInterval, propriété
description: Récupère ou définit la durée d’attente de l’exécution de SYSMON avant la prochaine collecte des données de compteur et met à jour le graphique ou le rapport.
ms.assetid: 297931e4-23ae-4384-a04a-9c1fa8aa1239
keywords:
- Propriété UpdateInterval SysMon
- Propriété UpdateInterval SysMon, classe SystemMonitor
- SystemMonitor classe SysMon, propriété UpdateInterval
topic_type:
- apiref
api_name:
- SystemMonitor.UpdateInterval
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5872f870e831896ff37157a4a0f47584e77d93c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942051"
---
# <a name="systemmonitorupdateinterval-property"></a><span data-ttu-id="34d35-106">SystemMonitor. UpdateInterval, propriété</span><span class="sxs-lookup"><span data-stu-id="34d35-106">SystemMonitor.UpdateInterval property</span></span>

<span data-ttu-id="34d35-107">Récupère ou définit la durée d’attente de l’exécution de SYSMON avant la prochaine collecte des données de compteur et met à jour le graphique ou le rapport.</span><span class="sxs-lookup"><span data-stu-id="34d35-107">Retrieves or sets the length of time that SYSMON waits before the next time it collects counter data and updates the graph or report.</span></span>

<span data-ttu-id="34d35-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="34d35-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="34d35-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="34d35-109">Syntax</span></span>


```VB
Property UpdateInterval As Single
```



## <a name="property-value"></a><span data-ttu-id="34d35-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="34d35-110">Property value</span></span>

<span data-ttu-id="34d35-111">Durée, en secondes, pendant laquelle SYSMON attend la prochaine fois qu’il collecte des données de compteur et met à jour le graphique ou le rapport.</span><span class="sxs-lookup"><span data-stu-id="34d35-111">Length of time, in seconds, that SYSMON waits before the next time it collects counter data and updates the graph or report.</span></span> <span data-ttu-id="34d35-112">L’intervalle minimal est de 1 seconde (il s’agit également de la valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="34d35-112">The minimum interval is 1 second (this is also the default value).</span></span> <span data-ttu-id="34d35-113">La valeur maximale est 1 million.</span><span class="sxs-lookup"><span data-stu-id="34d35-113">The maximum value is 1,000,000.</span></span>

## <a name="remarks"></a><span data-ttu-id="34d35-114">Notes</span><span class="sxs-lookup"><span data-stu-id="34d35-114">Remarks</span></span>

<span data-ttu-id="34d35-115">Cette propriété s’applique uniquement lorsque [**systemmonitor. ManualUpdate**](systemmonitor-manualupdate.md) est défini sur false.</span><span class="sxs-lookup"><span data-stu-id="34d35-115">This property is relevant only when [**SystemMonitor.ManualUpdate**](systemmonitor-manualupdate.md) is set to False.</span></span>

## <a name="requirements"></a><span data-ttu-id="34d35-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="34d35-116">Requirements</span></span>



| <span data-ttu-id="34d35-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="34d35-117">Requirement</span></span> | <span data-ttu-id="34d35-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="34d35-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="34d35-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="34d35-119">Minimum supported client</span></span><br/> | <span data-ttu-id="34d35-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="34d35-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="34d35-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="34d35-121">Minimum supported server</span></span><br/> | <span data-ttu-id="34d35-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="34d35-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="34d35-123">DLL</span><span class="sxs-lookup"><span data-stu-id="34d35-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34d35-124"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="34d35-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34d35-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34d35-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34d35-126">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="34d35-126">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





