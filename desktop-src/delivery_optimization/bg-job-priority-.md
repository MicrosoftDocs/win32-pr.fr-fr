---
title: Énumération BG_JOB_PRIORITY (Deliveryoptimization. h)
description: L’énumération BG_JOB_PRIORITY définit les valeurs constantes qui spécifient le niveau de priorité d’un travail.
ms.assetid: AF1F1F6D-473A-49E5-B24D-644A70DF304C
keywords:
- Énumération BG_JOB_PRIORITY
- Énumération BG_JOB_PRIORITY
topic_type:
- apiref
api_name:
- BG_JOB_PRIORITY
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 45b1f0f3029cc6157f2f100b3324165cfac1b03b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032725"
---
# <a name="bg_job_priority-enumeration"></a><span data-ttu-id="dea79-105">Énumération BG_JOB_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="dea79-105">BG_JOB_PRIORITY enumeration</span></span>

<span data-ttu-id="dea79-106">L’énumération **BG_JOB_PRIORITY** définit les valeurs constantes qui spécifient le niveau de priorité d’un travail.</span><span class="sxs-lookup"><span data-stu-id="dea79-106">The **BG_JOB_PRIORITY** enumeration defines the constant values that specify the priority level of a job.</span></span>

## <a name="syntax"></a><span data-ttu-id="dea79-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea79-107">Syntax</span></span>


```C++
typedef enum  { 
  BG_JOB_PRIORITY_FOREGROUND,
  BG_JOB_PRIORITY_HIGH,
  BG_JOB_PRIORITY_NORMAL,
  BG_JOB_PRIORITY_LOW
} BG_JOB_PRIORITY;
```



## <a name="constants"></a><span data-ttu-id="dea79-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="dea79-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="dea79-109"><span id="BG_JOB_PRIORITY_FOREGROUND"></span><span id="bg_job_priority_foreground"></span>**BG_JOB_PRIORITY_FOREGROUND**</span><span class="sxs-lookup"><span data-stu-id="dea79-109"><span id="BG_JOB_PRIORITY_FOREGROUND"></span><span id="bg_job_priority_foreground"></span>**BG_JOB_PRIORITY_FOREGROUND**</span></span>
</dt> <dd>

<span data-ttu-id="dea79-110">Transfère la tâche au premier plan.</span><span class="sxs-lookup"><span data-stu-id="dea79-110">Transfers the job in the foreground.</span></span> <span data-ttu-id="dea79-111">Les transferts de premier plan concurrencent la bande passante réseau avec d’autres applications, ce qui peut nuire à l’expérience réseau de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dea79-111">Foreground transfers compete for network bandwidth with other applications, which can impede the user's network experience.</span></span> <span data-ttu-id="dea79-112">Il s’agit du niveau de priorité le plus élevé.</span><span class="sxs-lookup"><span data-stu-id="dea79-112">This is the highest priority level.</span></span>

</dd> <dt>

<span data-ttu-id="dea79-113"><span id="BG_JOB_PRIORITY_HIGH"></span><span id="bg_job_priority_high"></span>**BG_JOB_PRIORITY_HIGH**</span><span class="sxs-lookup"><span data-stu-id="dea79-113"><span id="BG_JOB_PRIORITY_HIGH"></span><span id="bg_job_priority_high"></span>**BG_JOB_PRIORITY_HIGH**</span></span>
</dt> <dd>

<span data-ttu-id="dea79-114">Transfère la tâche en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="dea79-114">Transfers the job in the background.</span></span> <span data-ttu-id="dea79-115">Les transferts en arrière-plan utilisent un petit pourcentage de bande passante réseau.</span><span class="sxs-lookup"><span data-stu-id="dea79-115">Background transfers use a small percentage of network bandwidth.</span></span>

</dd> <dt>

<span data-ttu-id="dea79-116"><span id="BG_JOB_PRIORITY_NORMAL"></span><span id="bg_job_priority_normal"></span>**BG_JOB_PRIORITY_NORMAL**</span><span class="sxs-lookup"><span data-stu-id="dea79-116"><span id="BG_JOB_PRIORITY_NORMAL"></span><span id="bg_job_priority_normal"></span>**BG_JOB_PRIORITY_NORMAL**</span></span>
</dt> <dd>

<span data-ttu-id="dea79-117">Le comportement est le même pour tous les travaux qui ne sont pas au premier plan.</span><span class="sxs-lookup"><span data-stu-id="dea79-117">DO behavior is same for all non foreground job.</span></span> <span data-ttu-id="dea79-118">Pour plus d’informations, consultez les commentaires dans BG_JOB_PRIORITY_HIGH.</span><span class="sxs-lookup"><span data-stu-id="dea79-118">See comments in BG_JOB_PRIORITY_HIGH for details.</span></span>

</dd> <dt>

<span data-ttu-id="dea79-119"><span id="BG_JOB_PRIORITY_LOW"></span><span id="bg_job_priority_low"></span>**BG_JOB_PRIORITY_LOW**</span><span class="sxs-lookup"><span data-stu-id="dea79-119"><span id="BG_JOB_PRIORITY_LOW"></span><span id="bg_job_priority_low"></span>**BG_JOB_PRIORITY_LOW**</span></span>
</dt> <dd>

<span data-ttu-id="dea79-120">Le comportement est le même pour tous les travaux qui ne sont pas au premier plan.</span><span class="sxs-lookup"><span data-stu-id="dea79-120">DO behavior is same for all non foreground job.</span></span> <span data-ttu-id="dea79-121">Pour plus d’informations, consultez les commentaires dans BG_JOB_PRIORITY_HIGH.</span><span class="sxs-lookup"><span data-stu-id="dea79-121">See comments in BG_JOB_PRIORITY_HIGH for details.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dea79-122">Notes</span><span class="sxs-lookup"><span data-stu-id="dea79-122">Remarks</span></span>

<span data-ttu-id="dea79-123">Plusieurs transferts de premier plan et d’arrière-plan peuvent avoir lieu simultanément.</span><span class="sxs-lookup"><span data-stu-id="dea79-123">Multiple foreground and background transfers can take place simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="dea79-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dea79-124">Requirements</span></span>



| <span data-ttu-id="dea79-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dea79-125">Requirement</span></span> | <span data-ttu-id="dea79-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="dea79-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dea79-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dea79-127">Minimum supported client</span></span><br/> | <span data-ttu-id="dea79-128">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dea79-128">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="dea79-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dea79-129">Minimum supported server</span></span><br/> | <span data-ttu-id="dea79-130">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dea79-130">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="dea79-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="dea79-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="dea79-132"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="dea79-132"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dea79-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dea79-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dea79-134">**Méthode ibackgroundcopyjob :: getPriority,**</span><span class="sxs-lookup"><span data-stu-id="dea79-134">**IBackgroundCopyJob::GetPriority**</span></span>](ibackgroundcopyjob-getpriority.md)
</dt> <dt>

[<span data-ttu-id="dea79-135">**Méthode ibackgroundcopyjob :: SetPriority**</span><span class="sxs-lookup"><span data-stu-id="dea79-135">**IBackgroundCopyJob::SetPriority**</span></span>](ibackgroundcopyjob-setpriority.md)
</dt> </dl>

 

 





