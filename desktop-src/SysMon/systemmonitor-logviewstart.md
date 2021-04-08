---
title: SystemMonitor. LogViewStart, propriété
description: Récupère ou définit la date de début utilisée pour récupérer les valeurs de compteur à partir des fichiers journaux.
ms.assetid: f9fdef17-e8b1-4efb-86db-40ca0c499194
keywords:
- Propriété LogViewStart SysMon
- Propriété LogViewStart SysMon, classe SystemMonitor
- SystemMonitor classe SysMon, propriété LogViewStart
topic_type:
- apiref
api_name:
- SystemMonitor.LogViewStart
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 967c44940b195c4d8ddd3028e1d4f307827bbbfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941996"
---
# <a name="systemmonitorlogviewstart-property"></a><span data-ttu-id="b0a21-106">SystemMonitor. LogViewStart, propriété</span><span class="sxs-lookup"><span data-stu-id="b0a21-106">SystemMonitor.LogViewStart property</span></span>

<span data-ttu-id="b0a21-107">Récupère ou définit la date de début utilisée pour récupérer les valeurs de compteur à partir des fichiers journaux.</span><span class="sxs-lookup"><span data-stu-id="b0a21-107">Retrieves or sets the starting date used to retrieve counter values from the log files.</span></span>

<span data-ttu-id="b0a21-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b0a21-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0a21-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b0a21-109">Syntax</span></span>


```VB
Property LogViewStart As Date
```



## <a name="property-value"></a><span data-ttu-id="b0a21-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b0a21-110">Property value</span></span>

<span data-ttu-id="b0a21-111">Date de début utilisée pour récupérer les valeurs de compteur à partir des fichiers journaux.</span><span class="sxs-lookup"><span data-stu-id="b0a21-111">Starting date used to retrieve counter values from the log files.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0a21-112">Notes</span><span class="sxs-lookup"><span data-stu-id="b0a21-112">Remarks</span></span>

<span data-ttu-id="b0a21-113">SYSMON récupère les valeurs de compteur à partir des fichiers journaux qui se trouvent dans les dates Start et [**systemmonitor. LogViewStop**](systemmonitor-logviewstop.md) , inclus.</span><span class="sxs-lookup"><span data-stu-id="b0a21-113">SYSMON retrieves counter values from the log files that falls within the start and [**SystemMonitor.LogViewStop**](systemmonitor-logviewstop.md) dates, inclusively.</span></span>

<span data-ttu-id="b0a21-114">Si vous ne spécifiez pas de date de début ou si vous définissez cette propriété sur une valeur de date qui se trouve en dehors de la plage de valeurs de date trouvée dans les fichiers journaux, SYSMON remplace la valeur par la valeur de date la plus ancienne trouvée dans les fichiers journaux.</span><span class="sxs-lookup"><span data-stu-id="b0a21-114">If you do not specify a start date or if you set this property to a date value that is outside the range of date values found in the log files, SYSMON changes the value to the earliest date value found in the log files.</span></span>

<span data-ttu-id="b0a21-115">Si cette propriété est définie sur une valeur de date supérieure à [**LogViewStop**](systemmonitor-logviewstop.md), SYSMON remplace la valeur par la valeur de **LogViewStop**.</span><span class="sxs-lookup"><span data-stu-id="b0a21-115">If this property is set to a date value that is greater than [**LogViewStop**](systemmonitor-logviewstop.md), SYSMON changes the value to the value of **LogViewStop**.</span></span>

<span data-ttu-id="b0a21-116">Si vous spécifiez une date de début et de fin, vous devez spécifier les dates avant de définir [**systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md).</span><span class="sxs-lookup"><span data-stu-id="b0a21-116">If you specify a start and stop date, you should specify the dates before setting [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b0a21-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b0a21-117">Requirements</span></span>



| <span data-ttu-id="b0a21-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b0a21-118">Requirement</span></span> | <span data-ttu-id="b0a21-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="b0a21-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b0a21-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0a21-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b0a21-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b0a21-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b0a21-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0a21-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b0a21-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b0a21-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b0a21-124">DLL</span><span class="sxs-lookup"><span data-stu-id="b0a21-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0a21-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="b0a21-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0a21-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0a21-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0a21-127">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="b0a21-127">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="b0a21-128">**SystemMonitor.GetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="b0a21-128">**SystemMonitor.GetLogViewRange**</span></span>](systemmonitor-getlogviewrange.md)
</dt> <dt>

[<span data-ttu-id="b0a21-129">**SystemMonitor. LogFiles**</span><span class="sxs-lookup"><span data-stu-id="b0a21-129">**SystemMonitor.LogFiles**</span></span>](systemmonitor-logfiles.md)
</dt> <dt>

[<span data-ttu-id="b0a21-130">**SystemMonitor.LogViewStop**</span><span class="sxs-lookup"><span data-stu-id="b0a21-130">**SystemMonitor.LogViewStop**</span></span>](systemmonitor-logviewstop.md)
</dt> <dt>

[<span data-ttu-id="b0a21-131">**SystemMonitor.LogSourceStartTime**</span><span class="sxs-lookup"><span data-stu-id="b0a21-131">**SystemMonitor.LogSourceStartTime**</span></span>](systemmonitor-logsourcestarttime.md)
</dt> <dt>

[<span data-ttu-id="b0a21-132">**SystemMonitor.SetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="b0a21-132">**SystemMonitor.SetLogViewRange**</span></span>](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





