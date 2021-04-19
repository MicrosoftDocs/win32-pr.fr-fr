---
description: Demande que l’état de la tâche de migration passe à l’état spécifié.
ms.assetid: f0be5ea8-7e21-407e-b84d-8bd4ca5a6a2c
title: Méthode RequestStateChange de la classe Msvm_MigrationJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MigrationJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 31011de619780ae36f390ee87038300a3b42fef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524210"
---
# <a name="requeststatechange-method-of-the-msvm_migrationjob-class"></a><span data-ttu-id="75ad4-103">Méthode RequestStateChange de la \_ classe MSVM MigrationJob</span><span class="sxs-lookup"><span data-stu-id="75ad4-103">RequestStateChange method of the Msvm\_MigrationJob class</span></span>

<span data-ttu-id="75ad4-104">Demande que l’état de la tâche de migration passe à l’état spécifié.</span><span class="sxs-lookup"><span data-stu-id="75ad4-104">Requests that the state of the migration job be changed to the specified state.</span></span> <span data-ttu-id="75ad4-105">L’appel de la méthode **RequestStateChange** plusieurs fois peut entraîner le remplacement ou la perte des demandes antérieures.</span><span class="sxs-lookup"><span data-stu-id="75ad4-105">Invoking the **RequestStateChange** method multiple times can result in earlier requests being overwritten or lost.</span></span> <span data-ttu-id="75ad4-106">Si la valeur 0 est retournée, la tâche s’est terminée correctement.</span><span class="sxs-lookup"><span data-stu-id="75ad4-106">If 0 is returned, then the task completed successfully.</span></span> <span data-ttu-id="75ad4-107">Tout autre code de retour indique une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="75ad4-107">Any other return code indicates an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="75ad4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75ad4-108">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="75ad4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75ad4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75ad4-110">*RequestedState* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="75ad4-110">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75ad4-111">Nouvel état d’un travail.</span><span class="sxs-lookup"><span data-stu-id="75ad4-111">The new state of a job.</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="75ad4-112"><span id="Start"></span><span id="start"></span><span id="START"></span>**Démarrer** (2)</span><span class="sxs-lookup"><span data-stu-id="75ad4-112"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="75ad4-113">Passe l’État à « en cours d’exécution ».</span><span class="sxs-lookup"><span data-stu-id="75ad4-113">Changes the state to "Running".</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="75ad4-114"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspendre** (3)</span><span class="sxs-lookup"><span data-stu-id="75ad4-114"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="75ad4-115">Arrête temporairement le travail.</span><span class="sxs-lookup"><span data-stu-id="75ad4-115">Stops the job temporarily.</span></span> <span data-ttu-id="75ad4-116">L’objectif est de redémarrer ensuite le travail avec « Start ».</span><span class="sxs-lookup"><span data-stu-id="75ad4-116">The intention is to subsequently restart the job with "Start".</span></span> <span data-ttu-id="75ad4-117">Il peut être possible d’entrer dans l’État « service » en suspens.</span><span class="sxs-lookup"><span data-stu-id="75ad4-117">It might be possible to enter the "Service" state while suspended.</span></span> <span data-ttu-id="75ad4-118">(Il s’agit d’un travail spécifique.)</span><span class="sxs-lookup"><span data-stu-id="75ad4-118">(This is job specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="75ad4-119"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminer** (4)</span><span class="sxs-lookup"><span data-stu-id="75ad4-119"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="75ad4-120">Arrête le travail proprement dit, en enregistrant les données, en conservant l’État et en arrêtant tous les processus sous-jacents de manière ordonnée.</span><span class="sxs-lookup"><span data-stu-id="75ad4-120">Stops the job cleanly, saving data, preserving the state, and shutting down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="75ad4-121"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="75ad4-121"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="75ad4-122">Met immédiatement fin à la tâche, sans qu’il soit nécessaire d’enregistrer les données ou de conserver l’État.</span><span class="sxs-lookup"><span data-stu-id="75ad4-122">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="75ad4-123"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span><span class="sxs-lookup"><span data-stu-id="75ad4-123"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="75ad4-124">Place le travail dans un état de service spécifique au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="75ad4-124">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="75ad4-125">Il peut être possible de redémarrer le travail.</span><span class="sxs-lookup"><span data-stu-id="75ad4-125">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="75ad4-126"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF, réservé**</span><span class="sxs-lookup"><span data-stu-id="75ad4-126"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved**</span></span>


</dt> <dd>

<span data-ttu-id="75ad4-127">Réservé.</span><span class="sxs-lookup"><span data-stu-id="75ad4-127">Reserved.</span></span>

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="75ad4-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé**</span><span class="sxs-lookup"><span data-stu-id="75ad4-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved**</span></span>


</dt> <dd>

<span data-ttu-id="75ad4-129">Réservé.</span><span class="sxs-lookup"><span data-stu-id="75ad4-129">Reserved.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="75ad4-130">*TimeoutPeriod* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="75ad4-130">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75ad4-131">Délai d’attente qui spécifie la durée maximale pendant laquelle le client attend la transition vers le nouvel État.</span><span class="sxs-lookup"><span data-stu-id="75ad4-131">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="75ad4-132">Le format d’intervalle doit être utilisé pour spécifier le délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="75ad4-132">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="75ad4-133">La valeur 0 ou **null** indique que le client n’a aucune exigence de temps pour la transition.</span><span class="sxs-lookup"><span data-stu-id="75ad4-133">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="75ad4-134">Si cette propriété ne contient pas 0 ou **null** et que l’implémentation ne prend pas en charge ce paramètre, un code de retour de 4098 (utilisation du paramètre timeout non pris en charge) doit être retourné.</span><span class="sxs-lookup"><span data-stu-id="75ad4-134">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (Use Of Timeout Parameter Not Supported) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75ad4-135">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="75ad4-135">Return value</span></span>

<dl> <dt>

 <span data-ttu-id="75ad4-136"> (0)</span><span class="sxs-lookup"><span data-stu-id="75ad4-136">(0)</span></span>
</dt> <dt>

 <span data-ttu-id="75ad4-137">(32768)</span><span class="sxs-lookup"><span data-stu-id="75ad4-137">(32768)</span></span>
</dt> <dt>

 <span data-ttu-id="75ad4-138">(32769)</span><span class="sxs-lookup"><span data-stu-id="75ad4-138">(32769)</span></span>
</dt> <dt>

 <span data-ttu-id="75ad4-139">(32770)</span><span class="sxs-lookup"><span data-stu-id="75ad4-139">(32770)</span></span>
</dt> <dt>

 <span data-ttu-id="75ad4-140">(32771)</span><span class="sxs-lookup"><span data-stu-id="75ad4-140">(32771)</span></span>
</dt> <dt>

 <span data-ttu-id="75ad4-141">(32772)</span><span class="sxs-lookup"><span data-stu-id="75ad4-141">(32772)</span></span>
</dt> <dt>

 <span data-ttu-id="75ad4-142">(32773)</span><span class="sxs-lookup"><span data-stu-id="75ad4-142">(32773)</span></span>
</dt> <dt>

 <span data-ttu-id="75ad4-143">(32774)</span><span class="sxs-lookup"><span data-stu-id="75ad4-143">(32774)</span></span>
</dt> <dt>

 <span data-ttu-id="75ad4-144">(32775)</span><span class="sxs-lookup"><span data-stu-id="75ad4-144">(32775)</span></span>
</dt> <dt>

 <span data-ttu-id="75ad4-145">(32776)</span><span class="sxs-lookup"><span data-stu-id="75ad4-145">(32776)</span></span>
</dt> <dt>

 <span data-ttu-id="75ad4-146">(32777)</span><span class="sxs-lookup"><span data-stu-id="75ad4-146">(32777)</span></span>
</dt> <dt>

 <span data-ttu-id="75ad4-147">(32778)</span><span class="sxs-lookup"><span data-stu-id="75ad4-147">(32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="75ad4-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75ad4-148">Requirements</span></span>



| <span data-ttu-id="75ad4-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="75ad4-149">Requirement</span></span> | <span data-ttu-id="75ad4-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="75ad4-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75ad4-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75ad4-151">Minimum supported client</span></span><br/> | <span data-ttu-id="75ad4-152">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75ad4-152">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="75ad4-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75ad4-153">Minimum supported server</span></span><br/> | <span data-ttu-id="75ad4-154">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75ad4-154">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="75ad4-155">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="75ad4-155">Namespace</span></span><br/>                | <span data-ttu-id="75ad4-156">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="75ad4-156">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="75ad4-157">MOF</span><span class="sxs-lookup"><span data-stu-id="75ad4-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75ad4-158"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="75ad4-158"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="75ad4-159">DLL</span><span class="sxs-lookup"><span data-stu-id="75ad4-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75ad4-160"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="75ad4-160"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="75ad4-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75ad4-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75ad4-162">**MSVM \_ MigrationJob**</span><span class="sxs-lookup"><span data-stu-id="75ad4-162">**Msvm\_MigrationJob**</span></span>](msvm-migrationjob.md)
</dt> </dl>

 

 




