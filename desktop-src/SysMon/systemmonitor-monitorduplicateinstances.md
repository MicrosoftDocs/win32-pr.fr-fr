---
title: SystemMonitor. MonitorDuplicateInstances, propriété
description: Récupère ou définit une valeur qui détermine si plusieurs instances d’un compteur peuvent être surveillées.
ms.assetid: fe8d6074-eb29-4093-9f79-39e6171a3a3f
keywords:
- Propriété MonitorDuplicateInstances SysMon
- Propriété MonitorDuplicateInstances SysMon, classe SystemMonitor
- SystemMonitor classe SysMon, propriété MonitorDuplicateInstances
topic_type:
- apiref
api_name:
- SystemMonitor.MonitorDuplicateInstances
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f6ae53d0a1dcf3f67a43dab7959bb42619ace6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384455"
---
# <a name="systemmonitormonitorduplicateinstances-property"></a><span data-ttu-id="f2490-106">SystemMonitor. MonitorDuplicateInstances, propriété</span><span class="sxs-lookup"><span data-stu-id="f2490-106">SystemMonitor.MonitorDuplicateInstances property</span></span>

<span data-ttu-id="f2490-107">Récupère ou définit une valeur qui détermine si plusieurs instances d’un compteur peuvent être surveillées.</span><span class="sxs-lookup"><span data-stu-id="f2490-107">Retrieves or sets a value that determines whether multiple instances of a counter can be monitored.</span></span>

<span data-ttu-id="f2490-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f2490-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2490-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2490-109">Syntax</span></span>


```VB
Property MonitorDuplicateInstances As Boolean
```



## <a name="property-value"></a><span data-ttu-id="f2490-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f2490-110">Property value</span></span>

<span data-ttu-id="f2490-111">True indique que plusieurs instances d’un compteur peuvent être surveillées (true est la valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="f2490-111">True indicates that multiple instances of a counter can be monitored (True is the default).</span></span> <span data-ttu-id="f2490-112">La valeur false indique qu’une seule instance d’un compteur peut être surveillée.</span><span class="sxs-lookup"><span data-stu-id="f2490-112">False indicates that only one instance of a counter can be monitored.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2490-113">Notes</span><span class="sxs-lookup"><span data-stu-id="f2490-113">Remarks</span></span>

<span data-ttu-id="f2490-114">Le moniteur système ajoute \# n à chaque nom d’instance, sauf le premier, si plusieurs instances existent.</span><span class="sxs-lookup"><span data-stu-id="f2490-114">System Monitor appends \#n to every instance name, except the first, if multiple instances exist.</span></span> <span data-ttu-id="f2490-115">Le numéro de série, n, commence par un et est incrémenté d’une unité pour chaque nouvelle instance.</span><span class="sxs-lookup"><span data-stu-id="f2490-115">The serial number, n, begins with one and is incremented by one for each new instance.</span></span> <span data-ttu-id="f2490-116">Par exemple, si vous spécifiez « \\ Process ( \* ) \\ % Processor Time », la collection de compteurs doit contenir plusieurs instances de svchost.</span><span class="sxs-lookup"><span data-stu-id="f2490-116">For example, if you specify "\\Process(\*)\\% Processor Time", the counter collection should contain multiple instances of svchost.</span></span> <span data-ttu-id="f2490-117">La première occurrence est svchost, l’occurrence suivante est svchost \# 1, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="f2490-117">The first occurrence will be svchost, the next occurrence will be svchost\#1, and so on.</span></span>

<span data-ttu-id="f2490-118">Les instances dupliquées sont analysées uniquement si vous utilisez le caractère générique ( \* ) pour le nom de l’instance.</span><span class="sxs-lookup"><span data-stu-id="f2490-118">Duplicate instances are monitored only if you use the wildcard character (\*) for the instance name.</span></span> <span data-ttu-id="f2490-119">Si vous avez spécifié « \\ Process (svchost) \\ % Processor Time », seule la première instance de svchost est surveillée, pas toutes les instances de svchost.</span><span class="sxs-lookup"><span data-stu-id="f2490-119">If you specified "\\Process(svchost)\\% Processor Time" only the first instance found of svchost is monitored, not all instances of svchost.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2490-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2490-120">Requirements</span></span>



| <span data-ttu-id="f2490-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2490-121">Requirement</span></span> | <span data-ttu-id="f2490-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2490-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f2490-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2490-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f2490-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2490-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f2490-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2490-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f2490-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2490-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f2490-127">DLL</span><span class="sxs-lookup"><span data-stu-id="f2490-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2490-128"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="f2490-128"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2490-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2490-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2490-130">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="f2490-130">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





