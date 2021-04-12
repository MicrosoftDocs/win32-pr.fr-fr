---
description: Demande que l’état du travail soit remplacé par la valeur spécifiée dans le paramètre RequestedState. L’appel de la méthode RequestStateChange plusieurs fois peut entraîner le remplacement ou la perte des demandes antérieures.
ms.assetid: 64a9d63e-8af4-4ab1-8343-9a0418b951e2
title: Méthode RequestStateChange de la classe CIM_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6e3efcea0f7ed7d6ecbfef7b543a0e82d90a15b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318629"
---
# <a name="requeststatechange-method-of-the-cim_concretejob-class"></a><span data-ttu-id="2e585-104">Méthode RequestStateChange de la \_ classe CIM ConcreteJob</span><span class="sxs-lookup"><span data-stu-id="2e585-104">RequestStateChange method of the CIM\_ConcreteJob class</span></span>

<span data-ttu-id="2e585-105">Demande que l’état du travail soit remplacé par la valeur spécifiée dans le paramètre RequestedState.</span><span class="sxs-lookup"><span data-stu-id="2e585-105">Requests that the state of the job be changed to the value specified in the RequestedState parameter.</span></span> <span data-ttu-id="2e585-106">L’appel de la méthode RequestStateChange plusieurs fois peut entraîner le remplacement ou la perte des demandes antérieures.</span><span class="sxs-lookup"><span data-stu-id="2e585-106">Invoking the RequestStateChange method multiple times could result in earlier requests being overwritten or lost.</span></span>

<span data-ttu-id="2e585-107">Si la valeur 0 est retournée, la tâche s’est terminée correctement.</span><span class="sxs-lookup"><span data-stu-id="2e585-107">If 0 is returned, then the task completed successfully.</span></span> <span data-ttu-id="2e585-108">Tout autre code de retour indique une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="2e585-108">Any other return code indicates an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e585-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e585-109">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="2e585-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2e585-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e585-111">*RequestedState* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2e585-111">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e585-112">État à demander pour un travail.</span><span class="sxs-lookup"><span data-stu-id="2e585-112">The state to request for a job.</span></span> <span data-ttu-id="2e585-113">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2e585-113">The possible values are as follows:</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="2e585-114"><span id="Start"></span><span id="start"></span><span id="START"></span>**Démarrer** (2)</span><span class="sxs-lookup"><span data-stu-id="2e585-114"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2e585-115">Modifie l’État en’Running'.</span><span class="sxs-lookup"><span data-stu-id="2e585-115">Changes the state to 'Running'.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="2e585-116"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspendre** (3)</span><span class="sxs-lookup"><span data-stu-id="2e585-116"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2e585-117">Arrête temporairement le travail.</span><span class="sxs-lookup"><span data-stu-id="2e585-117">Stops the job temporarily.</span></span> <span data-ttu-id="2e585-118">L’objectif est de redémarrer ensuite le travail avec « Start ».</span><span class="sxs-lookup"><span data-stu-id="2e585-118">The intention is to subsequently restart the job with 'Start'.</span></span> <span data-ttu-id="2e585-119">Il peut être possible d’entrer dans l’État « service » en suspens.</span><span class="sxs-lookup"><span data-stu-id="2e585-119">It might be possible to enter the 'Service' state while suspended.</span></span> <span data-ttu-id="2e585-120">(Ceci est spécifique à un travail.)</span><span class="sxs-lookup"><span data-stu-id="2e585-120">(This is job-specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="2e585-121"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminer** (4)</span><span class="sxs-lookup"><span data-stu-id="2e585-121"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2e585-122">Arrête le travail proprement dit, enregistre les données, conserve l’État et arrête tous les processus sous-jacents de manière ordonnée.</span><span class="sxs-lookup"><span data-stu-id="2e585-122">Stops the job cleanly, saves data, preserves the state, and shuts down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="2e585-123"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="2e585-123"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2e585-124">Met immédiatement fin à la tâche, sans qu’il soit nécessaire d’enregistrer les données ou de conserver l’État.</span><span class="sxs-lookup"><span data-stu-id="2e585-124">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2e585-125"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span><span class="sxs-lookup"><span data-stu-id="2e585-125"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="2e585-126">Place le travail dans un état de service spécifique au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="2e585-126">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="2e585-127">Il peut être possible de redémarrer le travail.</span><span class="sxs-lookup"><span data-stu-id="2e585-127">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="2e585-128"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="2e585-128"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="2e585-129"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="2e585-129"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="2e585-130">*TimeoutPeriod* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2e585-130">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e585-131">Délai d’attente qui spécifie la durée maximale pendant laquelle le client attend la transition vers le nouvel État.</span><span class="sxs-lookup"><span data-stu-id="2e585-131">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="2e585-132">Le format d’intervalle doit être utilisé pour spécifier le délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="2e585-132">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="2e585-133">La valeur 0 ou **null** indique que le client n’a aucune exigence de temps pour la transition.</span><span class="sxs-lookup"><span data-stu-id="2e585-133">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="2e585-134">Si cette propriété ne contient pas 0 ou **null** et que l’implémentation ne prend pas en charge ce paramètre, un code de retour de 4098 (**utilisation du paramètre timeout non pris en charge**) doit être retourné.</span><span class="sxs-lookup"><span data-stu-id="2e585-134">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e585-135">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2e585-135">Return value</span></span>

<span data-ttu-id="2e585-136">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="2e585-136">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="2e585-137">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="2e585-137">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2e585-138">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="2e585-138">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2e585-139">**Erreur inconnue/non spécifiée** (2)</span><span class="sxs-lookup"><span data-stu-id="2e585-139">**Unknown/Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2e585-140">**Impossible de se terminer dans le délai imparti** (3)</span><span class="sxs-lookup"><span data-stu-id="2e585-140">**Can NOT complete within Timeout Period** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2e585-141">**Échec** (4)</span><span class="sxs-lookup"><span data-stu-id="2e585-141">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2e585-142">**Paramètre non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="2e585-142">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2e585-143">**En cours d’utilisation** (6)</span><span class="sxs-lookup"><span data-stu-id="2e585-143">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="2e585-144">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="2e585-144">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2e585-145">**Paramètres de méthode vérifiés-transition démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="2e585-145">**Method Parameters Checked - Transition Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2e585-146">**Transition d’État non valide** (4097)</span><span class="sxs-lookup"><span data-stu-id="2e585-146">**Invalid State Transition** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="2e585-147">**Utilisation du paramètre timeout non prise en charge** (4098)</span><span class="sxs-lookup"><span data-stu-id="2e585-147">**Use of Timeout Parameter Not Supported** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="2e585-148">**Occupé** (4099)</span><span class="sxs-lookup"><span data-stu-id="2e585-148">**Busy** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="2e585-149">**Méthode réservée** (4100.. 32767)</span><span class="sxs-lookup"><span data-stu-id="2e585-149">**Method Reserved** (4100..32767)</span></span>
</dt> <dt>

<span data-ttu-id="2e585-150">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="2e585-150">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2e585-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2e585-151">Requirements</span></span>



| <span data-ttu-id="2e585-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e585-152">Requirement</span></span> | <span data-ttu-id="2e585-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e585-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e585-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e585-154">Minimum supported client</span></span><br/> | <span data-ttu-id="2e585-155">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2e585-155">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="2e585-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e585-156">Minimum supported server</span></span><br/> | <span data-ttu-id="2e585-157">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="2e585-157">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="2e585-158">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2e585-158">Namespace</span></span><br/>                | <span data-ttu-id="2e585-159">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="2e585-159">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2e585-160">MOF</span><span class="sxs-lookup"><span data-stu-id="2e585-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e585-161"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2e585-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e585-162">DLL</span><span class="sxs-lookup"><span data-stu-id="2e585-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e585-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2e585-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2e585-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e585-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e585-165">**\_CONCRETEJOB CIM**</span><span class="sxs-lookup"><span data-stu-id="2e585-165">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> </dl>

 

 




