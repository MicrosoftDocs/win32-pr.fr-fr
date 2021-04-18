---
description: Modifie l’état de la tâche.
ms.assetid: 3B11CE45-63E4-43D1-AAF6-02F83C9CBB85
title: 'Msvm_CopyFileToGuestJob :: RequestStateChange, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: adf5d866989f3b3518cf53b52e073239e023e3c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520599"
---
# <a name="msvm_copyfiletoguestjobrequeststatechange-method"></a><span data-ttu-id="e99cf-103">MSVM \_ CopyFileToGuestJob :: RequestStateChange, méthode</span><span class="sxs-lookup"><span data-stu-id="e99cf-103">Msvm\_CopyFileToGuestJob::RequestStateChange method</span></span>

<span data-ttu-id="e99cf-104">Modifie l’état de la tâche.</span><span class="sxs-lookup"><span data-stu-id="e99cf-104">Changes the state of the job.</span></span>

## <a name="syntax"></a><span data-ttu-id="e99cf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e99cf-105">Syntax</span></span>


```C++
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="e99cf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e99cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e99cf-107">*RequestedState* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e99cf-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e99cf-108">Nouvel état.</span><span class="sxs-lookup"><span data-stu-id="e99cf-108">The new state.</span></span> <span data-ttu-id="e99cf-109">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e99cf-109">These are the possible values:</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="e99cf-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Démarrer** (2)</span><span class="sxs-lookup"><span data-stu-id="e99cf-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e99cf-111">Modifie l’État en’Running'.</span><span class="sxs-lookup"><span data-stu-id="e99cf-111">Changes the state to 'Running'.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="e99cf-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspendre** (3)</span><span class="sxs-lookup"><span data-stu-id="e99cf-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e99cf-113">Arrête temporairement le travail.</span><span class="sxs-lookup"><span data-stu-id="e99cf-113">Stops the job temporarily.</span></span> <span data-ttu-id="e99cf-114">Le client peut ensuite redémarrer le travail avec « Start ».</span><span class="sxs-lookup"><span data-stu-id="e99cf-114">The client can then subsequently restart the job with 'Start'.</span></span> <span data-ttu-id="e99cf-115">Le client peut éventuellement entrer l’État « service » en suspens (ce qui est spécifique à un travail).</span><span class="sxs-lookup"><span data-stu-id="e99cf-115">The client can possibly enter the 'Service' state while suspended (this is job-specific).</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="e99cf-116"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminer** (4)</span><span class="sxs-lookup"><span data-stu-id="e99cf-116"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e99cf-117">Arrête le travail proprement dit, en enregistrant les données, en conservant l’État et en arrêtant tous les processus sous-jacents de manière ordonnée.</span><span class="sxs-lookup"><span data-stu-id="e99cf-117">Stops the job cleanly, saving data, preserving the state, and shutting down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="e99cf-118"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="e99cf-118"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="e99cf-119">Met immédiatement fin à la tâche, sans qu’il soit nécessaire d’enregistrer les données ou de conserver l’État.</span><span class="sxs-lookup"><span data-stu-id="e99cf-119">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e99cf-120"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span><span class="sxs-lookup"><span data-stu-id="e99cf-120"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="e99cf-121">Place le travail dans un état de service spécifique au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="e99cf-121">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="e99cf-122">Le client peut éventuellement redémarrer le travail.</span><span class="sxs-lookup"><span data-stu-id="e99cf-122">The client can possibly restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e99cf-123"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="e99cf-123"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="e99cf-124"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="e99cf-124"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="e99cf-125">*TimeoutPeriod* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e99cf-125">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e99cf-126">Délai d’attente qui spécifie la durée maximale pendant laquelle le client attend la transition vers le nouvel État.</span><span class="sxs-lookup"><span data-stu-id="e99cf-126">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="e99cf-127">Le format d’intervalle doit être utilisé pour spécifier le délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="e99cf-127">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="e99cf-128">La valeur 0 ou **null** indique que le client n’a aucune exigence de temps pour la transition.</span><span class="sxs-lookup"><span data-stu-id="e99cf-128">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="e99cf-129">Si cette propriété ne contient pas 0 ou **null** et que l’implémentation ne prend pas en charge ce paramètre, un code de retour de 4098 (**utilisation du paramètre timeout non pris en charge**) doit être retourné.</span><span class="sxs-lookup"><span data-stu-id="e99cf-129">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e99cf-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e99cf-130">Return value</span></span>

<span data-ttu-id="e99cf-131">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e99cf-131">This method returns one of the following values.</span></span>



| <span data-ttu-id="e99cf-132">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="e99cf-132">Return code/value</span></span>                                                                                                                                                               | <span data-ttu-id="e99cf-133">Description</span><span class="sxs-lookup"><span data-stu-id="e99cf-133">Description</span></span>                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e99cf-134"><dt>**Terminé sans erreur**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e99cf-134"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                   | <span data-ttu-id="e99cf-135">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="e99cf-135">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="e99cf-136"><dt>**Utilisation du paramètre timeout non prise en charge**</dt> <dt>4098</dt></span><span class="sxs-lookup"><span data-stu-id="e99cf-136"><dt>**Use of Timeout Parameter Not Supported**</dt> <dt>4098</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="e99cf-137"><dt>**Échec**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="e99cf-137"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                |                                                                                    |
| <dl> <span data-ttu-id="e99cf-138"><dt>**Accès refusé**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="e99cf-138"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                         | <span data-ttu-id="e99cf-139">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="e99cf-139">Access denied.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="e99cf-140"><dt>**Non pris en charge**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="e99cf-140"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                         |                                                                                    |
| <dl> <span data-ttu-id="e99cf-141">L' <dt>**État est inconnu**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="e99cf-141"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                     |                                                                                    |
| <dl> <span data-ttu-id="e99cf-142"><dt>**Délai d’expiration**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="e99cf-142"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                               |                                                                                    |
| <dl> <span data-ttu-id="e99cf-143"><dt>**Paramètre non valide**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="e99cf-143"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                     |                                                                                    |
| <dl> <span data-ttu-id="e99cf-144">Le <dt>**système est en cours d’utilisation**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="e99cf-144"><dt>**System is in use**</dt> <dt>32774</dt></span></span> </dl>                      |                                                                                    |
| <dl> <span data-ttu-id="e99cf-145"><dt>**État non valide pour cette opération**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="e99cf-145"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>      | <span data-ttu-id="e99cf-146">La valeur spécifiée dans le paramètre *RequestedState* n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="e99cf-146">The value specified in the *RequestedState* parameter is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="e99cf-147"><dt>**Type de données incorrect**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="e99cf-147"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                   |                                                                                    |
| <dl> <span data-ttu-id="e99cf-148">Le <dt>**système n’est pas disponible**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="e99cf-148"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>               |                                                                                    |
| <dl> <span data-ttu-id="e99cf-149"><dt>**Mémoire Insuffisante**</dt> <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="e99cf-149"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                         |                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="e99cf-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e99cf-150">Requirements</span></span>



| <span data-ttu-id="e99cf-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e99cf-151">Requirement</span></span> | <span data-ttu-id="e99cf-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="e99cf-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e99cf-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e99cf-153">Minimum supported client</span></span><br/> | <span data-ttu-id="e99cf-154">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e99cf-154">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="e99cf-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e99cf-155">Minimum supported server</span></span><br/> | <span data-ttu-id="e99cf-156">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e99cf-156">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e99cf-157">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e99cf-157">Namespace</span></span><br/>                | <span data-ttu-id="e99cf-158">\\\\\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="e99cf-158">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="e99cf-159">MOF</span><span class="sxs-lookup"><span data-stu-id="e99cf-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e99cf-160"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e99cf-160"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e99cf-161">DLL</span><span class="sxs-lookup"><span data-stu-id="e99cf-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e99cf-162"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e99cf-162"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e99cf-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e99cf-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e99cf-164">**MSVM \_ CopyFileToGuestJob**</span><span class="sxs-lookup"><span data-stu-id="e99cf-164">**Msvm\_CopyFileToGuestJob**</span></span>](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

 




