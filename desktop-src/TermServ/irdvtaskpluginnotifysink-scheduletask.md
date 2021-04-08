---
title: IRDVTaskPluginNotifySink ScheduleTask, méthode
description: Appelé par l’agent de tâche pour planifier une tâche.
ms.assetid: 06793439-cf16-40ca-8a91-08acc22c73ed
ms.tgt_platform: multiple
keywords:
- ScheduleTask, méthode Services Bureau à distance
- ScheduleTask, méthode Services Bureau à distance, IRDVTaskPluginNotifySink, interface
- IRDVTaskPluginNotifySink interface Services Bureau à distance, ScheduleTask, méthode
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.ScheduleTask
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c9bde92992eec9c4ab3d4151c59e6d687ec2f3fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844278"
---
# <a name="irdvtaskpluginnotifysinkscheduletask-method"></a><span data-ttu-id="e7043-106">IRDVTaskPluginNotifySink :: ScheduleTask, méthode</span><span class="sxs-lookup"><span data-stu-id="e7043-106">IRDVTaskPluginNotifySink::ScheduleTask method</span></span>

<span data-ttu-id="e7043-107">Appelé par l’agent de tâche pour planifier une tâche.</span><span class="sxs-lookup"><span data-stu-id="e7043-107">Called by the task agent to schedule a task.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7043-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7043-108">Syntax</span></span>


```C++
HRESULT ScheduleTask(
  [in] FILETIME        ftStartTime,
  [in] FILETIME        ftEndTime,
  [in] FILETIME        ftDeadline,
  [in] BSTR            bstrLabel,
  [in] BSTR            bstrIdentifier,
  [in] SAFEARRAY(BYTE) saContext
);
```



## <a name="parameters"></a><span data-ttu-id="e7043-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7043-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7043-110">*ftStartTime* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7043-110">*ftStartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7043-111">Type : **[ **fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span><span class="sxs-lookup"><span data-stu-id="e7043-111">Type: **[**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span></span>

<span data-ttu-id="e7043-112">Heure de début de la première tâche, en UTC.</span><span class="sxs-lookup"><span data-stu-id="e7043-112">The earliest task start time, in UTC.</span></span>

</dd> <dt>

<span data-ttu-id="e7043-113">*ftEndTime* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7043-113">*ftEndTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7043-114">Type : **[ **fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span><span class="sxs-lookup"><span data-stu-id="e7043-114">Type: **[**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span></span>

<span data-ttu-id="e7043-115">Heure de fin de la tâche, en heure UTC.</span><span class="sxs-lookup"><span data-stu-id="e7043-115">The task end time, in UTC.</span></span> <span data-ttu-id="e7043-116">Passe un [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) défini à tous les zéros si aucune heure de fin n’est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e7043-116">Pass a [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) set to all zeros if no end time is specified.</span></span>

</dd> <dt>

<span data-ttu-id="e7043-117">*ftDeadline* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7043-117">*ftDeadline* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7043-118">Type : **[ **fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span><span class="sxs-lookup"><span data-stu-id="e7043-118">Type: **[**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span></span>

<span data-ttu-id="e7043-119">Date d’échéance de la tâche, en UTC.</span><span class="sxs-lookup"><span data-stu-id="e7043-119">The task deadline, in UTC.</span></span> <span data-ttu-id="e7043-120">Cette valeur est utilisée pour définir la priorité de plusieurs tâches qui se trouvent dans leur fenêtre de démarrage.</span><span class="sxs-lookup"><span data-stu-id="e7043-120">This is used to set priority for multiple tasks that are within their start window.</span></span> <span data-ttu-id="e7043-121">Si plusieurs tâches doivent être démarrées, celle avec l’échéance la plus proche est démarrée en premier.</span><span class="sxs-lookup"><span data-stu-id="e7043-121">If more than one task should be started, the one with the earliest deadline will be started first.</span></span>

</dd> <dt>

<span data-ttu-id="e7043-122">*bstrLabel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7043-122">*bstrLabel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7043-123">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="e7043-123">Type: **BSTR**</span></span>

<span data-ttu-id="e7043-124">Étiquette de la tâche.</span><span class="sxs-lookup"><span data-stu-id="e7043-124">The label for the task.</span></span> <span data-ttu-id="e7043-125">Cette valeur est transmise à la méthode [**StartTask**](irdvtaskplugin-starttask.md) .</span><span class="sxs-lookup"><span data-stu-id="e7043-125">This is passed to the [**StartTask**](irdvtaskplugin-starttask.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="e7043-126">*bstrIdentifier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7043-126">*bstrIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7043-127">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="e7043-127">Type: **BSTR**</span></span>

<span data-ttu-id="e7043-128">Identificateur de la tâche.</span><span class="sxs-lookup"><span data-stu-id="e7043-128">The identifier of the task.</span></span> <span data-ttu-id="e7043-129">Cette valeur est transmise à la méthode [**StartTask**](irdvtaskplugin-starttask.md) .</span><span class="sxs-lookup"><span data-stu-id="e7043-129">This is passed to the [**StartTask**](irdvtaskplugin-starttask.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="e7043-130">*Sacontext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7043-130">*saContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7043-131">Type : **SAFEARRAY (Byte)**</span><span class="sxs-lookup"><span data-stu-id="e7043-131">Type: **SAFEARRAY(BYTE)**</span></span>

<span data-ttu-id="e7043-132">Données facultatives pour la tâche.</span><span class="sxs-lookup"><span data-stu-id="e7043-132">Optional data for the task.</span></span> <span data-ttu-id="e7043-133">Cette valeur est transmise à la méthode [**StartTask**](irdvtaskplugin-starttask.md) .</span><span class="sxs-lookup"><span data-stu-id="e7043-133">This is passed to the [**StartTask**](irdvtaskplugin-starttask.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7043-134">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e7043-134">Return value</span></span>

<span data-ttu-id="e7043-135">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e7043-135">Type: **HRESULT**</span></span>

<span data-ttu-id="e7043-136">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e7043-136">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e7043-137">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e7043-137">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7043-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7043-138">Requirements</span></span>



| <span data-ttu-id="e7043-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7043-139">Requirement</span></span> | <span data-ttu-id="e7043-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7043-140">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="e7043-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7043-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e7043-142">Windows 7 Entreprise</span><span class="sxs-lookup"><span data-stu-id="e7043-142">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="e7043-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7043-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e7043-144">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e7043-144">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e7043-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7043-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7043-146">**IRDVTaskPluginNotifySink**</span><span class="sxs-lookup"><span data-stu-id="e7043-146">**IRDVTaskPluginNotifySink**</span></span>](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

