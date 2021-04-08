---
title: SystemMonitor. LogViewStop, propriété
description: Récupère ou définit la date de fin utilisée pour récupérer les valeurs de compteur à partir des fichiers journaux.
ms.assetid: 5dabfb26-fa33-4fb5-a075-ed8955a56f1e
keywords:
- Propriété LogViewStop SysMon
- Propriété LogViewStop SysMon, objet SystemMonitor
- Objet SystemMonitor SysMon, propriété LogViewStop
topic_type:
- apiref
api_name:
- SystemMonitor.LogViewStop
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b725ee2efba22453d44f1e15fb9ce231b07cdb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942088"
---
# <a name="systemmonitorlogviewstop-property"></a><span data-ttu-id="9e6fe-106">SystemMonitor. LogViewStop, propriété</span><span class="sxs-lookup"><span data-stu-id="9e6fe-106">SystemMonitor.LogViewStop property</span></span>

<span data-ttu-id="9e6fe-107">Récupère ou définit la date de fin utilisée pour récupérer les valeurs de compteur à partir des fichiers journaux.</span><span class="sxs-lookup"><span data-stu-id="9e6fe-107">Retrieves or sets the ending date used to retrieve counter values from the log files.</span></span>

<span data-ttu-id="9e6fe-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9e6fe-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e6fe-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e6fe-109">Syntax</span></span>


```VB
Property LogViewStop As Date
```



## <a name="property-value"></a><span data-ttu-id="9e6fe-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="9e6fe-110">Property value</span></span>

<span data-ttu-id="9e6fe-111">Date de fin utilisée pour récupérer les valeurs de compteur à partir des fichiers journaux.</span><span class="sxs-lookup"><span data-stu-id="9e6fe-111">Ending date used to retrieve counter values from the log files.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e6fe-112">Notes</span><span class="sxs-lookup"><span data-stu-id="9e6fe-112">Remarks</span></span>

<span data-ttu-id="9e6fe-113">SYSMON récupère les valeurs de compteur à partir des fichiers journaux qui se trouvent dans les dates [**systemmonitor. LogViewStart**](systemmonitor-logviewstart.md) et Stop, inclus.</span><span class="sxs-lookup"><span data-stu-id="9e6fe-113">SYSMON retrieves counter values from the log files that falls within the [**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md) and stop dates, inclusively.</span></span>

<span data-ttu-id="9e6fe-114">Si vous ne spécifiez pas de valeur d’arrêt ou si vous affectez à cette propriété une valeur de date postérieure à la dernière date contenue dans le fichier journal, SYSMON remplace la valeur par la valeur de date la plus récente trouvée dans les fichiers journaux.</span><span class="sxs-lookup"><span data-stu-id="9e6fe-114">If you do not specify a stop value or you set this property to a date value that is later than the last date contained in the log file, SYSMON changes the value to the latest date value found in the log files.</span></span>

<span data-ttu-id="9e6fe-115">Si cette propriété est définie sur une valeur de date inférieure à [**LogViewStart**](systemmonitor-logviewstart.md), SYSMON remplace la valeur par la valeur de **LogViewStart**.</span><span class="sxs-lookup"><span data-stu-id="9e6fe-115">If this property is set to a date value that is less than [**LogViewStart**](systemmonitor-logviewstart.md), SYSMON changes the value to the value of **LogViewStart**.</span></span>

<span data-ttu-id="9e6fe-116">Vous devez définir la date de début avant de définir la date d’arrêt. Sinon, les deux valeurs sont définies sur date. MinValue et, si vous définissez les dates après le paramètre [**systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md), seule la première valeur de compteur est récupérée à partir du fichier journal.</span><span class="sxs-lookup"><span data-stu-id="9e6fe-116">You must set the start date before you set the stop date; otherwise, both values are set to Date.MinValue, and if you set the dates after setting [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md), then only the first counter value is retrieved from the log file.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e6fe-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e6fe-117">Requirements</span></span>



| <span data-ttu-id="9e6fe-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e6fe-118">Requirement</span></span> | <span data-ttu-id="9e6fe-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e6fe-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9e6fe-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e6fe-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9e6fe-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9e6fe-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="9e6fe-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e6fe-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9e6fe-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9e6fe-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9e6fe-124">DLL</span><span class="sxs-lookup"><span data-stu-id="9e6fe-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e6fe-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="9e6fe-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e6fe-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e6fe-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e6fe-127">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="9e6fe-127">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="9e6fe-128">**SystemMonitor.GetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="9e6fe-128">**SystemMonitor.GetLogViewRange**</span></span>](systemmonitor-getlogviewrange.md)
</dt> <dt>

[<span data-ttu-id="9e6fe-129">**SystemMonitor.LogSourceStopTime**</span><span class="sxs-lookup"><span data-stu-id="9e6fe-129">**SystemMonitor.LogSourceStopTime**</span></span>](systemmonitor-logsourcestoptime.md)
</dt> <dt>

[<span data-ttu-id="9e6fe-130">**SystemMonitor.LogViewStart**</span><span class="sxs-lookup"><span data-stu-id="9e6fe-130">**SystemMonitor.LogViewStart**</span></span>](systemmonitor-logviewstart.md)
</dt> <dt>

[<span data-ttu-id="9e6fe-131">**SystemMonitor.SetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="9e6fe-131">**SystemMonitor.SetLogViewRange**</span></span>](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





