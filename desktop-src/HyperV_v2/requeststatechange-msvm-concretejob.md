---
description: Demande que l’état du travail passe à l’état spécifié.
ms.assetid: 5D7D7D20-4BB9-4375-BBBF-7AA64FEE6D13
title: Méthode RequestStateChange de la classe Msvm_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0e7abf5f4bf78ac469e528ab72bb5786130e9cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521038"
---
# <a name="requeststatechange-method-of-the-msvm_concretejob-class"></a><span data-ttu-id="08bde-103">Méthode RequestStateChange de la \_ classe MSVM ConcreteJob</span><span class="sxs-lookup"><span data-stu-id="08bde-103">RequestStateChange method of the Msvm\_ConcreteJob class</span></span>

<span data-ttu-id="08bde-104">Demande que l’état du travail passe à l’état spécifié.</span><span class="sxs-lookup"><span data-stu-id="08bde-104">Requests that the state of the job be changed to the specified state.</span></span> <span data-ttu-id="08bde-105">L’appel de la méthode **RequestStateChange** plusieurs fois peut entraîner le remplacement ou la perte des demandes antérieures.</span><span class="sxs-lookup"><span data-stu-id="08bde-105">Invoking the **RequestStateChange** method multiple times can result in earlier requests being overwritten or lost.</span></span> <span data-ttu-id="08bde-106">Si la valeur 0 est retournée, la tâche s’est terminée correctement.</span><span class="sxs-lookup"><span data-stu-id="08bde-106">If 0 is returned, then the task completed successfully.</span></span> <span data-ttu-id="08bde-107">Tout autre code de retour indique une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="08bde-107">Any other return code indicates an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="08bde-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08bde-108">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="08bde-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="08bde-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08bde-110">*RequestedState* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="08bde-110">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08bde-111">Type : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08bde-111">Type: **uint16**</span></span>

<span data-ttu-id="08bde-112">Nouvel état d’un travail.</span><span class="sxs-lookup"><span data-stu-id="08bde-112">The new state of a job.</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="08bde-113"><span id="Start"></span><span id="start"></span><span id="START"></span>**Démarrer** (2)</span><span class="sxs-lookup"><span data-stu-id="08bde-113"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="08bde-114">Passe l’État à « en cours d’exécution ».</span><span class="sxs-lookup"><span data-stu-id="08bde-114">Changes the state to "Running".</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="08bde-115"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspendre** (3)</span><span class="sxs-lookup"><span data-stu-id="08bde-115"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="08bde-116">Arrête temporairement le travail.</span><span class="sxs-lookup"><span data-stu-id="08bde-116">Stops the job temporarily.</span></span> <span data-ttu-id="08bde-117">L’objectif est de redémarrer ensuite le travail avec « Start ».</span><span class="sxs-lookup"><span data-stu-id="08bde-117">The intention is to subsequently restart the job with "Start".</span></span> <span data-ttu-id="08bde-118">Il peut être possible d’entrer dans l’État « service » en suspens.</span><span class="sxs-lookup"><span data-stu-id="08bde-118">It might be possible to enter the "Service" state while suspended.</span></span> <span data-ttu-id="08bde-119">(Il s’agit d’un travail spécifique.)</span><span class="sxs-lookup"><span data-stu-id="08bde-119">(This is job specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="08bde-120"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminer** (4)</span><span class="sxs-lookup"><span data-stu-id="08bde-120"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="08bde-121">Arrête le travail proprement dit, en enregistrant les données, en conservant l’État et en arrêtant tous les processus sous-jacents de manière ordonnée.</span><span class="sxs-lookup"><span data-stu-id="08bde-121">Stops the job cleanly, saving data, preserving the state, and shutting down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="08bde-122"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="08bde-122"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="08bde-123">Met immédiatement fin à la tâche, sans qu’il soit nécessaire d’enregistrer les données ou de conserver l’État.</span><span class="sxs-lookup"><span data-stu-id="08bde-123">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="08bde-124"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span><span class="sxs-lookup"><span data-stu-id="08bde-124"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="08bde-125">Place le travail dans un état de service spécifique au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="08bde-125">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="08bde-126">Il peut être possible de redémarrer le travail.</span><span class="sxs-lookup"><span data-stu-id="08bde-126">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="08bde-127"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF, réservé**</span><span class="sxs-lookup"><span data-stu-id="08bde-127"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved**</span></span>


</dt> <dd>

<span data-ttu-id="08bde-128">Réservé.</span><span class="sxs-lookup"><span data-stu-id="08bde-128">Reserved.</span></span>

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="08bde-129"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé**</span><span class="sxs-lookup"><span data-stu-id="08bde-129"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved**</span></span>


</dt> <dd>

<span data-ttu-id="08bde-130">Réservé.</span><span class="sxs-lookup"><span data-stu-id="08bde-130">Reserved.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="08bde-131">*TimeoutPeriod* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="08bde-131">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08bde-132">Type : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="08bde-132">Type: **datetime**</span></span>

<span data-ttu-id="08bde-133">Délai d’attente qui spécifie la durée maximale pendant laquelle le client attend la transition vers le nouvel État.</span><span class="sxs-lookup"><span data-stu-id="08bde-133">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="08bde-134">Le format d’intervalle doit être utilisé pour spécifier le délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="08bde-134">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="08bde-135">La valeur 0 ou **null** indique que le client n’a aucune exigence de temps pour la transition.</span><span class="sxs-lookup"><span data-stu-id="08bde-135">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="08bde-136">Si cette propriété ne contient pas 0 ou **null** et que l’implémentation ne prend pas en charge ce paramètre, un code de retour de 4098 (utilisation du paramètre timeout non pris en charge) doit être retourné.</span><span class="sxs-lookup"><span data-stu-id="08bde-136">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (Use Of Timeout Parameter Not Supported) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08bde-137">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="08bde-137">Return value</span></span>

<span data-ttu-id="08bde-138">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08bde-138">Type: **uint32**</span></span>

<span data-ttu-id="08bde-139">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="08bde-139">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="08bde-140">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="08bde-140">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="08bde-141">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="08bde-141">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="08bde-142">**Erreur inconnue/non spécifiée** (2)</span><span class="sxs-lookup"><span data-stu-id="08bde-142">**Unknown/Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="08bde-143">**Impossible de se terminer dans le délai imparti** (3)</span><span class="sxs-lookup"><span data-stu-id="08bde-143">**Cannot complete within Timeout Period** (3)</span></span>
</dt> <dt>

<span data-ttu-id="08bde-144">**Échec** (4)</span><span class="sxs-lookup"><span data-stu-id="08bde-144">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="08bde-145">**Paramètre non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="08bde-145">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="08bde-146">**En cours d’utilisation** (6)</span><span class="sxs-lookup"><span data-stu-id="08bde-146">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="08bde-147">**DMTF réservé** (7 4095)</span><span class="sxs-lookup"><span data-stu-id="08bde-147">**DMTF Reserved** (7 4095)</span></span>
</dt> <dt>

<span data-ttu-id="08bde-148">**Paramètres de méthode vérifiés-transition démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="08bde-148">**Method Parameters Checked - Transition Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="08bde-149">**Transition d’État non valide** (4097)</span><span class="sxs-lookup"><span data-stu-id="08bde-149">**Invalid State Transition** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="08bde-150">**Utilisation du paramètre timeout non prise en charge** (4098)</span><span class="sxs-lookup"><span data-stu-id="08bde-150">**Use of Timeout Parameter Not Supported** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="08bde-151">**Occupé** (4099)</span><span class="sxs-lookup"><span data-stu-id="08bde-151">**Busy** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="08bde-152">**Méthode réservée** (4100 32767)</span><span class="sxs-lookup"><span data-stu-id="08bde-152">**Method Reserved** (4100 32767)</span></span>
</dt> <dt>

<span data-ttu-id="08bde-153">**Spécifique au fournisseur** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="08bde-153">**Vendor Specific** (32768 65535)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="08bde-154">Notes</span><span class="sxs-lookup"><span data-stu-id="08bde-154">Remarks</span></span>

<span data-ttu-id="08bde-155">L’accès à la classe [**MSVM \_ ConcreteJob**](msvm-concretejob.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="08bde-155">Access to the [**Msvm\_ConcreteJob**](msvm-concretejob.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="08bde-156">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="08bde-156">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="08bde-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08bde-157">Requirements</span></span>



| <span data-ttu-id="08bde-158">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08bde-158">Requirement</span></span> | <span data-ttu-id="08bde-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="08bde-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08bde-160">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08bde-160">Minimum supported client</span></span><br/> | <span data-ttu-id="08bde-161">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08bde-161">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="08bde-162">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08bde-162">Minimum supported server</span></span><br/> | <span data-ttu-id="08bde-163">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08bde-163">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="08bde-164">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="08bde-164">Namespace</span></span><br/>                | <span data-ttu-id="08bde-165">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="08bde-165">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="08bde-166">MOF</span><span class="sxs-lookup"><span data-stu-id="08bde-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08bde-167"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="08bde-167"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="08bde-168">DLL</span><span class="sxs-lookup"><span data-stu-id="08bde-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08bde-169"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="08bde-169"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="08bde-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08bde-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08bde-171">**MSVM \_ ConcreteJob**</span><span class="sxs-lookup"><span data-stu-id="08bde-171">**Msvm\_ConcreteJob**</span></span>](msvm-concretejob.md)
</dt> </dl>

 

