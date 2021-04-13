---
title: Énumération VMTaskResult (VPCCOMInterfaces. h)
description: Spécifie le résultat d’une tâche.
ms.assetid: 34aa193a-466d-492e-8648-467c286a8c11
keywords:
- Virtual PC de l’énumération VMTaskResult
topic_type:
- apiref
api_name:
- VMTaskResult
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 903425ca8036e1862df7042f16946fc0f2e9cc7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509329"
---
# <a name="vmtaskresult-enumeration"></a><span data-ttu-id="26d88-104">Énumération VMTaskResult</span><span class="sxs-lookup"><span data-stu-id="26d88-104">VMTaskResult enumeration</span></span>

<span data-ttu-id="26d88-105">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="26d88-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="26d88-106">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="26d88-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="26d88-107">Spécifie le résultat d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="26d88-107">Specifies the result of a task.</span></span>

## <a name="syntax"></a><span data-ttu-id="26d88-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26d88-108">Syntax</span></span>


```C++
typedef enum  { 
  vmTaskResult_Success                      = 0,
  vmTaskResult_Cancelled                    = 1,
  vmTaskResult_UnexpectedError              = 2,
  vmTaskResult_OutOfMemoryError             = 3,
  vmTaskResult_DiskRelatedError             = 4,
  vmTaskResult_IncompatibleSavedStateError  = 5,
  vmTaskResult_TimeOutError                 = 6,
  vmTaskResult_IllegalValueError            = 7,
  vmTaskResult_ThreadCrashError             = 8,
  vmTaskResult_ShutdownAbort                = 9
} VMTaskResult;
```



## <a name="constants"></a><span data-ttu-id="26d88-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="26d88-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="26d88-110"><span id="vmTaskResult_Success"></span><span id="vmtaskresult_success"></span><span id="VMTASKRESULT_SUCCESS"></span>**réussite de vmTaskResult \_**</span><span class="sxs-lookup"><span data-stu-id="26d88-110"><span id="vmTaskResult_Success"></span><span id="vmtaskresult_success"></span><span id="VMTASKRESULT_SUCCESS"></span>**vmTaskResult\_Success**</span></span>
</dt> <dd>

<span data-ttu-id="26d88-111">La tâche a réussi.</span><span class="sxs-lookup"><span data-stu-id="26d88-111">The task was successful.</span></span>

</dd> <dt>

<span data-ttu-id="26d88-112"><span id="vmTaskResult_Cancelled"></span><span id="vmtaskresult_cancelled"></span><span id="VMTASKRESULT_CANCELLED"></span>**vmTaskResult \_ annulé**</span><span class="sxs-lookup"><span data-stu-id="26d88-112"><span id="vmTaskResult_Cancelled"></span><span id="vmtaskresult_cancelled"></span><span id="VMTASKRESULT_CANCELLED"></span>**vmTaskResult\_Cancelled**</span></span>
</dt> <dd>

<span data-ttu-id="26d88-113">La tâche a été annulée.</span><span class="sxs-lookup"><span data-stu-id="26d88-113">The task was canceled.</span></span>

</dd> <dt>

<span data-ttu-id="26d88-114"><span id="vmTaskResult_UnexpectedError"></span><span id="vmtaskresult_unexpectederror"></span><span id="VMTASKRESULT_UNEXPECTEDERROR"></span>**vmTaskResult \_ UnexpectedError**</span><span class="sxs-lookup"><span data-stu-id="26d88-114"><span id="vmTaskResult_UnexpectedError"></span><span id="vmtaskresult_unexpectederror"></span><span id="VMTASKRESULT_UNEXPECTEDERROR"></span>**vmTaskResult\_UnexpectedError**</span></span>
</dt> <dd>

<span data-ttu-id="26d88-115">La tâche a rencontré une erreur inattendue.</span><span class="sxs-lookup"><span data-stu-id="26d88-115">The task had an unexpected error.</span></span>

</dd> <dt>

<span data-ttu-id="26d88-116"><span id="vmTaskResult_OutOfMemoryError"></span><span id="vmtaskresult_outofmemoryerror"></span><span id="VMTASKRESULT_OUTOFMEMORYERROR"></span>**vmTaskResult \_ OutOfMemoryError**</span><span class="sxs-lookup"><span data-stu-id="26d88-116"><span id="vmTaskResult_OutOfMemoryError"></span><span id="vmtaskresult_outofmemoryerror"></span><span id="VMTASKRESULT_OUTOFMEMORYERROR"></span>**vmTaskResult\_OutOfMemoryError**</span></span>
</dt> <dd>

<span data-ttu-id="26d88-117">La mémoire est insuffisante pour terminer la tâche.</span><span class="sxs-lookup"><span data-stu-id="26d88-117">There was not enough memory for the task to complete.</span></span>

</dd> <dt>

<span data-ttu-id="26d88-118"><span id="vmTaskResult_DiskRelatedError"></span><span id="vmtaskresult_diskrelatederror"></span><span id="VMTASKRESULT_DISKRELATEDERROR"></span>**vmTaskResult \_ DiskRelatedError**</span><span class="sxs-lookup"><span data-stu-id="26d88-118"><span id="vmTaskResult_DiskRelatedError"></span><span id="vmtaskresult_diskrelatederror"></span><span id="VMTASKRESULT_DISKRELATEDERROR"></span>**vmTaskResult\_DiskRelatedError**</span></span>
</dt> <dd>

<span data-ttu-id="26d88-119">La tâche a rencontré une erreur lors de l’écriture sur le disque (Vérifiez que l’espace disque est suffisant).</span><span class="sxs-lookup"><span data-stu-id="26d88-119">The task had an error while writing to disk (make sure there is enough disk space).</span></span>

</dd> <dt>

<span data-ttu-id="26d88-120"><span id="vmTaskResult_IncompatibleSavedStateError"></span><span id="vmtaskresult_incompatiblesavedstateerror"></span><span id="VMTASKRESULT_INCOMPATIBLESAVEDSTATEERROR"></span>**vmTaskResult \_ IncompatibleSavedStateError**</span><span class="sxs-lookup"><span data-stu-id="26d88-120"><span id="vmTaskResult_IncompatibleSavedStateError"></span><span id="vmtaskresult_incompatiblesavedstateerror"></span><span id="VMTASKRESULT_INCOMPATIBLESAVEDSTATEERROR"></span>**vmTaskResult\_IncompatibleSavedStateError**</span></span>
</dt> <dd>

<span data-ttu-id="26d88-121">Impossible de restaurer l’ordinateur virtuel, car l’état enregistré était incompatible.</span><span class="sxs-lookup"><span data-stu-id="26d88-121">The virtual machine could not restore because the saved state was incompatible.</span></span>

</dd> <dt>

<span data-ttu-id="26d88-122"><span id="vmTaskResult_TimeOutError"></span><span id="vmtaskresult_timeouterror"></span><span id="VMTASKRESULT_TIMEOUTERROR"></span>**vmTaskResult \_ TimeOutError**</span><span class="sxs-lookup"><span data-stu-id="26d88-122"><span id="vmTaskResult_TimeOutError"></span><span id="vmtaskresult_timeouterror"></span><span id="VMTASKRESULT_TIMEOUTERROR"></span>**vmTaskResult\_TimeOutError**</span></span>
</dt> <dd>

<span data-ttu-id="26d88-123">La tâche a expiré.</span><span class="sxs-lookup"><span data-stu-id="26d88-123">The task timed out.</span></span>

</dd> <dt>

<span data-ttu-id="26d88-124"><span id="vmTaskResult_IllegalValueError"></span><span id="vmtaskresult_illegalvalueerror"></span><span id="VMTASKRESULT_ILLEGALVALUEERROR"></span>**vmTaskResult \_ IllegalValueError**</span><span class="sxs-lookup"><span data-stu-id="26d88-124"><span id="vmTaskResult_IllegalValueError"></span><span id="vmtaskresult_illegalvalueerror"></span><span id="VMTASKRESULT_ILLEGALVALUEERROR"></span>**vmTaskResult\_IllegalValueError**</span></span>
</dt> <dd>

<span data-ttu-id="26d88-125">Une valeur de préférence non conforme a été lue pendant le traitement de la tâche.</span><span class="sxs-lookup"><span data-stu-id="26d88-125">An illegal preference value was read while the task was processing.</span></span>

</dd> <dt>

<span data-ttu-id="26d88-126"><span id="vmTaskResult_ThreadCrashError"></span><span id="vmtaskresult_threadcrasherror"></span><span id="VMTASKRESULT_THREADCRASHERROR"></span>**vmTaskResult \_ ThreadCrashError**</span><span class="sxs-lookup"><span data-stu-id="26d88-126"><span id="vmTaskResult_ThreadCrashError"></span><span id="vmtaskresult_threadcrasherror"></span><span id="VMTASKRESULT_THREADCRASHERROR"></span>**vmTaskResult\_ThreadCrashError**</span></span>
</dt> <dd>

<span data-ttu-id="26d88-127">Un thread associé à la tâche s’est bloqué.</span><span class="sxs-lookup"><span data-stu-id="26d88-127">A thread associated with the task crashed.</span></span>

</dd> <dt>

<span data-ttu-id="26d88-128"><span id="vmTaskResult_ShutdownAbort"></span><span id="vmtaskresult_shutdownabort"></span><span id="VMTASKRESULT_SHUTDOWNABORT"></span>**vmTaskResult \_ ShutdownAbort**</span><span class="sxs-lookup"><span data-stu-id="26d88-128"><span id="vmTaskResult_ShutdownAbort"></span><span id="vmtaskresult_shutdownabort"></span><span id="VMTASKRESULT_SHUTDOWNABORT"></span>**vmTaskResult\_ShutdownAbort**</span></span>
</dt> <dd>

<span data-ttu-id="26d88-129">L’arrêt demandé a été abandonné.</span><span class="sxs-lookup"><span data-stu-id="26d88-129">The shutdown requested was aborted.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="26d88-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26d88-130">Requirements</span></span>



| <span data-ttu-id="26d88-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26d88-131">Requirement</span></span> | <span data-ttu-id="26d88-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="26d88-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="26d88-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26d88-133">Minimum supported client</span></span><br/> | <span data-ttu-id="26d88-134">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26d88-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="26d88-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26d88-135">Minimum supported server</span></span><br/> | <span data-ttu-id="26d88-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="26d88-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="26d88-137">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="26d88-137">End of client support</span></span><br/>    | <span data-ttu-id="26d88-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="26d88-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="26d88-139">Produit</span><span class="sxs-lookup"><span data-stu-id="26d88-139">Product</span></span><br/>                  | <span data-ttu-id="26d88-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="26d88-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="26d88-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="26d88-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="26d88-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="26d88-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26d88-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26d88-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26d88-144">**IVMTask :: result**</span><span class="sxs-lookup"><span data-stu-id="26d88-144">**IVMTask::Result**</span></span>](ivmtask-result.md)
</dt> </dl>

 

