---
title: Énumération BG_JOB_STATE (Deliveryoptimization. h)
description: L’énumération BG_JOB_STATE définit des valeurs constantes pour les différents États d’un travail.
ms.assetid: DB4806BD-08BC-4F0B-A7F4-BA0719112811
keywords:
- Énumération BG_JOB_STATE
- Énumération BG_JOB_STATE
topic_type:
- apiref
api_name:
- BG_JOB_STATE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 113e0b1ecc995a0a452f22835ad8717041b44d10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510735"
---
# <a name="bg_job_state-enumeration"></a><span data-ttu-id="8dce5-105">Énumération BG_JOB_STATE</span><span class="sxs-lookup"><span data-stu-id="8dce5-105">BG_JOB_STATE enumeration</span></span>

<span data-ttu-id="8dce5-106">L’énumération **BG_JOB_STATE** définit des valeurs constantes pour les différents États d’un travail.</span><span class="sxs-lookup"><span data-stu-id="8dce5-106">The **BG_JOB_STATE** enumeration defines constant values for the different states of a job.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dce5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8dce5-107">Syntax</span></span>


```C++
typedef enum  { 
  BG_JOB_STATE_QUEUED,
  BG_JOB_STATE_CONNECTING,
  BG_JOB_STATE_TRANSFERRING,
  BG_JOB_STATE_SUSPENDED,
  BG_JOB_STATE_ERROR,
  BG_JOB_STATE_TRANSIENT_ERROR,
  BG_JOB_STATE_TRANSFERRED,
  BG_JOB_STATE_ACKNOWLEDGED,
  BG_JOB_STATE_CANCELLED
} BG_JOB_STATE;
```



## <a name="constants"></a><span data-ttu-id="8dce5-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="8dce5-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8dce5-109"><span id="BG_JOB_STATE_QUEUED"></span><span id="bg_job_state_queued"></span>**BG_JOB_STATE_QUEUED**</span><span class="sxs-lookup"><span data-stu-id="8dce5-109"><span id="BG_JOB_STATE_QUEUED"></span><span id="bg_job_state_queued"></span>**BG_JOB_STATE_QUEUED**</span></span>
</dt> <dd>

<span data-ttu-id="8dce5-110">Spécifie que le travail se trouve dans la file d’attente et qu’il est en attente d’exécution.</span><span class="sxs-lookup"><span data-stu-id="8dce5-110">Specifies that the job is in the queue and waiting to run.</span></span> <span data-ttu-id="8dce5-111">Si un utilisateur se déconnecte pendant le transfert de son travail, le travail passe à l’État en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="8dce5-111">If a user logs off while their job is transferring, the job transitions to the queued state.</span></span>

</dd> <dt>

<span data-ttu-id="8dce5-112"><span id="BG_JOB_STATE_CONNECTING"></span><span id="bg_job_state_connecting"></span>**BG_JOB_STATE_CONNECTING**</span><span class="sxs-lookup"><span data-stu-id="8dce5-112"><span id="BG_JOB_STATE_CONNECTING"></span><span id="bg_job_state_connecting"></span>**BG_JOB_STATE_CONNECTING**</span></span>
</dt> <dd>

<span data-ttu-id="8dce5-113">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="8dce5-113">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="8dce5-114"><span id="BG_JOB_STATE_TRANSFERRING"></span><span id="bg_job_state_transferring"></span>**BG_JOB_STATE_TRANSFERRING**</span><span class="sxs-lookup"><span data-stu-id="8dce5-114"><span id="BG_JOB_STATE_TRANSFERRING"></span><span id="bg_job_state_transferring"></span>**BG_JOB_STATE_TRANSFERRING**</span></span>
</dt> <dd>

<span data-ttu-id="8dce5-115">Spécifie que effectue le transfert des données pour le travail.</span><span class="sxs-lookup"><span data-stu-id="8dce5-115">Specifies that DO is transferring data for the job.</span></span>

</dd> <dt>

<span data-ttu-id="8dce5-116"><span id="BG_JOB_STATE_SUSPENDED"></span><span id="bg_job_state_suspended"></span>**BG_JOB_STATE_SUSPENDED**</span><span class="sxs-lookup"><span data-stu-id="8dce5-116"><span id="BG_JOB_STATE_SUSPENDED"></span><span id="bg_job_state_suspended"></span>**BG_JOB_STATE_SUSPENDED**</span></span>
</dt> <dd>

<span data-ttu-id="8dce5-117">Spécifie que le travail est suspendu (suspendu).</span><span class="sxs-lookup"><span data-stu-id="8dce5-117">Specifies that the job is suspended (paused).</span></span> <span data-ttu-id="8dce5-118">Pour interrompre un travail, appelez la méthode [**méthode ibackgroundcopyjob :: suspend**](ibackgroundcopyjob-suspend.md) .</span><span class="sxs-lookup"><span data-stu-id="8dce5-118">To suspend a job, call the [**IBackgroundCopyJob::Suspend**](ibackgroundcopyjob-suspend.md) method.</span></span> <span data-ttu-id="8dce5-119">Le travail reste suspendu jusqu’à ce que vous appeliez la méthode [**méthode ibackgroundcopyjob :: Resume**](ibackgroundcopyjob-resume.md), [**méthode ibackgroundcopyjob :: Complete**](ibackgroundcopyjob-complete.md)ou [**méthode ibackgroundcopyjob :: Cancel**](ibackgroundcopyjob-cancel.md) .</span><span class="sxs-lookup"><span data-stu-id="8dce5-119">The job remains suspended until you call the [**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md), [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md), or [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="8dce5-120"><span id="BG_JOB_STATE_ERROR"></span><span id="bg_job_state_error"></span>**BG_JOB_STATE_ERROR**</span><span class="sxs-lookup"><span data-stu-id="8dce5-120"><span id="BG_JOB_STATE_ERROR"></span><span id="bg_job_state_error"></span>**BG_JOB_STATE_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="8dce5-121">Spécifie qu’une erreur irrécupérable s’est produite (le service n’est pas en mesure de transférer le fichier).</span><span class="sxs-lookup"><span data-stu-id="8dce5-121">Specifies that a nonrecoverable error occurred (the service is unable to transfer the file).</span></span> <span data-ttu-id="8dce5-122">Si l’erreur, telle qu’une erreur d’accès refusé, peut être corrigée, appelez la méthode [**méthode ibackgroundcopyjob :: Resume**](ibackgroundcopyjob-resume.md) une fois l’erreur corrigée.</span><span class="sxs-lookup"><span data-stu-id="8dce5-122">If the error, such as an access-denied error, can be corrected, call the [**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md) method after the error is fixed.</span></span> <span data-ttu-id="8dce5-123">Toutefois, si l’erreur ne peut pas être corrigée, appelez la méthode [**méthode ibackgroundcopyjob :: Cancel**](ibackgroundcopyjob-cancel.md) pour annuler le travail, ou appelez la méthode [**méthode ibackgroundcopyjob :: Complete**](ibackgroundcopyjob-complete.md) pour accepter la partie d’une tâche de téléchargement qui a été transférée avec succès.</span><span class="sxs-lookup"><span data-stu-id="8dce5-123">However, if the error cannot be corrected, call the [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method to cancel the job, or call the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method to accept the portion of a download job that transferred successfully.</span></span>

</dd> <dt>

<span data-ttu-id="8dce5-124"><span id="BG_JOB_STATE_TRANSIENT_ERROR"></span><span id="bg_job_state_transient_error"></span>**BG_JOB_STATE_TRANSIENT_ERROR**</span><span class="sxs-lookup"><span data-stu-id="8dce5-124"><span id="BG_JOB_STATE_TRANSIENT_ERROR"></span><span id="bg_job_state_transient_error"></span>**BG_JOB_STATE_TRANSIENT_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="8dce5-125">Spécifie qu’une erreur récupérable s’est produite.</span><span class="sxs-lookup"><span data-stu-id="8dce5-125">Specifies that a recoverable error occurred.</span></span> <span data-ttu-id="8dce5-126">Effectuez une nouvelle tentative de travaux dans l’état d’erreur temporaire en fonction de la configuration de nouvelle tentative interne.</span><span class="sxs-lookup"><span data-stu-id="8dce5-126">DO will retry jobs in the transient error state based on the internal retry configuration.</span></span> <span data-ttu-id="8dce5-127">L’état du travail devient **BG_JOB_STATE_ERROR** si le travail échoue pour progresser (voir [**méthode ibackgroundcopyjob :: SetNoProgressTimeout**](ibackgroundcopyjob-setnoprogresstimeout.md)).</span><span class="sxs-lookup"><span data-stu-id="8dce5-127">The state of the job changes to **BG_JOB_STATE_ERROR** if the job fails to make progress (see [**IBackgroundCopyJob::SetNoProgressTimeout**](ibackgroundcopyjob-setnoprogresstimeout.md)).</span></span>

</dd> <dt>

<span data-ttu-id="8dce5-128"><span id="BG_JOB_STATE_TRANSFERRED"></span><span id="bg_job_state_transferred"></span>**BG_JOB_STATE_TRANSFERRED**</span><span class="sxs-lookup"><span data-stu-id="8dce5-128"><span id="BG_JOB_STATE_TRANSFERRED"></span><span id="bg_job_state_transferred"></span>**BG_JOB_STATE_TRANSFERRED**</span></span>
</dt> <dd>

<span data-ttu-id="8dce5-129">Spécifie que votre travail a été traité avec succès.</span><span class="sxs-lookup"><span data-stu-id="8dce5-129">Specifies that your job was successfully processed.</span></span> <span data-ttu-id="8dce5-130">Vous devez appeler la méthode [**méthode ibackgroundcopyjob :: Complete**](ibackgroundcopyjob-complete.md) pour accuser réception de la tâche et rendre les fichiers accessibles au client.</span><span class="sxs-lookup"><span data-stu-id="8dce5-130">You must call the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method to acknowledge completion of the job and to make the files available to the client.</span></span>

</dd> <dt>

<span data-ttu-id="8dce5-131"><span id="BG_JOB_STATE_ACKNOWLEDGED"></span><span id="bg_job_state_acknowledged"></span>**BG_JOB_STATE_ACKNOWLEDGED**</span><span class="sxs-lookup"><span data-stu-id="8dce5-131"><span id="BG_JOB_STATE_ACKNOWLEDGED"></span><span id="bg_job_state_acknowledged"></span>**BG_JOB_STATE_ACKNOWLEDGED**</span></span>
</dt> <dd>

<span data-ttu-id="8dce5-132">Spécifie que vous avez appelé la méthode [**méthode ibackgroundcopyjob :: Complete**](ibackgroundcopyjob-complete.md) pour confirmer que votre travail s’est terminé avec succès.</span><span class="sxs-lookup"><span data-stu-id="8dce5-132">Specifies that you called the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method to acknowledge that your job completed successfully.</span></span>

</dd> <dt>

<span data-ttu-id="8dce5-133"><span id="BG_JOB_STATE_CANCELLED"></span><span id="bg_job_state_cancelled"></span>**BG_JOB_STATE_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="8dce5-133"><span id="BG_JOB_STATE_CANCELLED"></span><span id="bg_job_state_cancelled"></span>**BG_JOB_STATE_CANCELLED**</span></span>
</dt> <dd>

<span data-ttu-id="8dce5-134">Spécifie que vous avez appelé la méthode [**méthode ibackgroundcopyjob :: Cancel**](ibackgroundcopyjob-cancel.md) pour annuler le travail (supprimer la tâche de la file d’attente de transfert).</span><span class="sxs-lookup"><span data-stu-id="8dce5-134">Specifies that you called the [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method to cancel the job (remove the job from the transfer queue).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8dce5-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8dce5-135">Requirements</span></span>



| <span data-ttu-id="8dce5-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8dce5-136">Requirement</span></span> | <span data-ttu-id="8dce5-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="8dce5-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8dce5-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8dce5-138">Minimum supported client</span></span><br/> | <span data-ttu-id="8dce5-139">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8dce5-139">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8dce5-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8dce5-140">Minimum supported server</span></span><br/> | <span data-ttu-id="8dce5-141">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8dce5-141">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8dce5-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="8dce5-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="8dce5-143"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="8dce5-143"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8dce5-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8dce5-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dce5-145">**Méthode ibackgroundcopyjob :: GetState**</span><span class="sxs-lookup"><span data-stu-id="8dce5-145">**IBackgroundCopyJob::GetState**</span></span>](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





