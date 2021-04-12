---
title: Méthode SystemMonitor. SetLogViewRange
description: Définit la date de début utilisée pour récupérer les valeurs de compteur à partir des fichiers journaux.
ms.assetid: ced641d0-cf71-4826-8ff0-c05f20a71aaa
keywords:
- Méthode SetLogViewRange SysMon
- Méthode SetLogViewRange SysMon, objet SystemMonitor
- Objet SystemMonitor SysMon, méthode SetLogViewRange
topic_type:
- apiref
api_name:
- SystemMonitor.SetLogViewRange
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 534a7dc3bf711832ec99e4202f4f56cc347f336b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384240"
---
# <a name="systemmonitorsetlogviewrange-method"></a><span data-ttu-id="e86e2-106">Méthode SystemMonitor. SetLogViewRange</span><span class="sxs-lookup"><span data-stu-id="e86e2-106">SystemMonitor.SetLogViewRange method</span></span>

<span data-ttu-id="e86e2-107">Définit la date de début utilisée pour récupérer les valeurs de compteur à partir des fichiers journaux.</span><span class="sxs-lookup"><span data-stu-id="e86e2-107">Sets the starting date used to retrieve counter values from the log files.</span></span>

## <a name="syntax"></a><span data-ttu-id="e86e2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e86e2-108">Syntax</span></span>


```VB
SystemMonitor.SetLogViewRange( _
  ByVal StartTime As Date, _
  ByVal StopTime As Date _
)
```



## <a name="parameters"></a><span data-ttu-id="e86e2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e86e2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e86e2-110">*StartTime* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e86e2-110">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e86e2-111">Date de début utilisée pour récupérer les valeurs de compteur à partir des fichiers journaux.</span><span class="sxs-lookup"><span data-stu-id="e86e2-111">Starting date used to retrieve counter values from the log files.</span></span>

</dd> <dt>

<span data-ttu-id="e86e2-112">*StopTime* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e86e2-112">*StopTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e86e2-113">Date de fin utilisée pour récupérer les valeurs de compteur à partir des fichiers journaux.</span><span class="sxs-lookup"><span data-stu-id="e86e2-113">Ending date used to retrieve counter values from the log files.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e86e2-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e86e2-114">Return value</span></span>

<span data-ttu-id="e86e2-115">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e86e2-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e86e2-116">Notes</span><span class="sxs-lookup"><span data-stu-id="e86e2-116">Remarks</span></span>

<span data-ttu-id="e86e2-117">SYSMON récupère les valeurs de compteur à partir des fichiers journaux qui se trouvent dans les dates de début et de fin, inclus.</span><span class="sxs-lookup"><span data-stu-id="e86e2-117">SYSMON retrieves counter values from the log files that falls within the start and stop dates, inclusively.</span></span>

<span data-ttu-id="e86e2-118">Si vous ne spécifiez pas de date de début ou si vous définissez la date de début sur une valeur de date qui se trouve en dehors de la plage de valeurs de date trouvée dans les fichiers journaux, SYSMON remplace la valeur par la valeur de date la plus ancienne trouvée dans les fichiers journaux.</span><span class="sxs-lookup"><span data-stu-id="e86e2-118">If you do not specify a start date or if you set the start date to a date value that is outside the range of date values found in the log files, SYSMON changes the value to the earliest date value found in the log files.</span></span> <span data-ttu-id="e86e2-119">Si la valeur de début est supérieure à la valeur d’arrêt, SYSMON remplace la valeur de début par la même valeur que la valeur d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="e86e2-119">If the start value is greater than the stop value, SYSMON changes the start value to be the same value as the stop value.</span></span>

<span data-ttu-id="e86e2-120">Si vous ne spécifiez pas de valeur d’arrêt ou si vous définissez la valeur d’arrêt sur une valeur de date postérieure à la dernière date contenue dans le fichier journal, SYSMON remplace la valeur par la valeur de date la plus récente trouvée dans les fichiers journaux.</span><span class="sxs-lookup"><span data-stu-id="e86e2-120">If you do not specify a stop value or you set the stop value to a date value that is later than the last date contained in the log file, SYSMON changes the value to the latest date value found in the log files.</span></span> <span data-ttu-id="e86e2-121">Si la valeur d’arrêt est inférieure à la valeur d’arrêt, SYSMON change la valeur d’arrêt pour qu’elle soit de la même valeur que la valeur de début.</span><span class="sxs-lookup"><span data-stu-id="e86e2-121">If the stop value is less than the stop value, SYSMON changes the stop value to be the same value as the start value.</span></span>

<span data-ttu-id="e86e2-122">Si vous spécifiez une date de début et de fin, vous devez spécifier les dates avant de définir [**systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md).</span><span class="sxs-lookup"><span data-stu-id="e86e2-122">If you specify a start and stop date, you should specify the dates before setting [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md).</span></span> <span data-ttu-id="e86e2-123">Si vous définissez les dates après avoir défini **systemmonitor. DataSourceType**, seule la première valeur de compteur est récupérée à partir du fichier journal.</span><span class="sxs-lookup"><span data-stu-id="e86e2-123">If you set the dates after setting **SystemMonitor.DataSourceType**, then only the first counter value is retrieved from the log file.</span></span>

## <a name="requirements"></a><span data-ttu-id="e86e2-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e86e2-124">Requirements</span></span>



| <span data-ttu-id="e86e2-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e86e2-125">Requirement</span></span> | <span data-ttu-id="e86e2-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="e86e2-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e86e2-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e86e2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e86e2-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e86e2-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e86e2-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e86e2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e86e2-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e86e2-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e86e2-131">DLL</span><span class="sxs-lookup"><span data-stu-id="e86e2-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e86e2-132"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="e86e2-132"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e86e2-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e86e2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e86e2-134">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="e86e2-134">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="e86e2-135">**SystemMonitor.GetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="e86e2-135">**SystemMonitor.GetLogViewRange**</span></span>](systemmonitor-getlogviewrange.md)
</dt> </dl>

 

 





