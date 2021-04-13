---
title: Méthode SystemMonitor. GetLogViewRange
description: Récupère la date de début utilisée pour récupérer les valeurs de compteur à partir des fichiers journaux.
ms.assetid: c74c3a5b-d2ec-43d8-b715-e399f42e8ae5
keywords:
- Méthode GetLogViewRange SysMon
- Méthode GetLogViewRange SysMon, objet SystemMonitor
- Objet SystemMonitor SysMon, méthode GetLogViewRange
topic_type:
- apiref
api_name:
- SystemMonitor.GetLogViewRange
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d494a5861ff9c0d2c076abe2bdad749d21653500
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508589"
---
# <a name="systemmonitorgetlogviewrange-method"></a><span data-ttu-id="470d5-106">Méthode SystemMonitor. GetLogViewRange</span><span class="sxs-lookup"><span data-stu-id="470d5-106">SystemMonitor.GetLogViewRange method</span></span>

<span data-ttu-id="470d5-107">Récupère la date de début utilisée pour récupérer les valeurs de compteur à partir des fichiers journaux.</span><span class="sxs-lookup"><span data-stu-id="470d5-107">Retrieves the starting date used to retrieve counter values from the log files.</span></span>

## <a name="syntax"></a><span data-ttu-id="470d5-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="470d5-108">Syntax</span></span>


```VB
SystemMonitor.GetLogViewRange( _
  ByRef StartTime As Date, _
  ByRef StopTime As Date _
)
```



## <a name="parameters"></a><span data-ttu-id="470d5-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="470d5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="470d5-110">*StartTime* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="470d5-110">*StartTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="470d5-111">Date de début utilisée pour récupérer les valeurs de compteur à partir des fichiers journaux.</span><span class="sxs-lookup"><span data-stu-id="470d5-111">Starting date used to retrieve counter values from the log files.</span></span>

</dd> <dt>

<span data-ttu-id="470d5-112">*StopTime* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="470d5-112">*StopTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="470d5-113">Date de fin utilisée pour récupérer les valeurs de compteur à partir des fichiers journaux.</span><span class="sxs-lookup"><span data-stu-id="470d5-113">Ending date used to retrieve counter values from the log files.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="470d5-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="470d5-114">Return value</span></span>

<span data-ttu-id="470d5-115">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="470d5-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="470d5-116">Notes</span><span class="sxs-lookup"><span data-stu-id="470d5-116">Remarks</span></span>

<span data-ttu-id="470d5-117">SYSMON récupère les valeurs de compteur à partir des fichiers journaux qui se trouvent dans les dates de début et de fin, inclus.</span><span class="sxs-lookup"><span data-stu-id="470d5-117">SYSMON retrieves counter values from the log files that falls within the start and stop dates, inclusively.</span></span>

<span data-ttu-id="470d5-118">L’utilisation de cette méthode revient à accéder aux propriétés [**systemmonitor. LogViewStart**](systemmonitor-logviewstart.md) et [**systemmonitor. LogViewStop**](systemmonitor-logviewstop.md) .</span><span class="sxs-lookup"><span data-stu-id="470d5-118">Using this method is the same as accessing the [**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md) and [**SystemMonitor.LogViewStop**](systemmonitor-logviewstop.md) properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="470d5-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="470d5-119">Requirements</span></span>



| <span data-ttu-id="470d5-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="470d5-120">Requirement</span></span> | <span data-ttu-id="470d5-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="470d5-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="470d5-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="470d5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="470d5-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="470d5-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="470d5-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="470d5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="470d5-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="470d5-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="470d5-126">DLL</span><span class="sxs-lookup"><span data-stu-id="470d5-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="470d5-127"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="470d5-127"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="470d5-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="470d5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="470d5-129">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="470d5-129">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="470d5-130">**SystemMonitor.SetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="470d5-130">**SystemMonitor.SetLogViewRange**</span></span>](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





