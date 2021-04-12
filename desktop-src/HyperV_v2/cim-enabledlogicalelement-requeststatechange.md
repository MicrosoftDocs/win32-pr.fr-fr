---
description: Demande que l’état de l’élément soit remplacé par la valeur spécifiée dans le paramètre RequestedState.
ms.assetid: 6d0061ad-ca14-400a-b813-af920f231eeb
title: Méthode RequestStateChange de la classe CIM_EnabledLogicalElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EnabledLogicalElement.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5b28a2c33b61893be24eacc882b29b5a2be18b14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319294"
---
# <a name="requeststatechange-method-of-the-cim_enabledlogicalelement-class"></a><span data-ttu-id="59613-103">Méthode RequestStateChange de la \_ classe CIM EnabledLogicalElement</span><span class="sxs-lookup"><span data-stu-id="59613-103">RequestStateChange method of the CIM\_EnabledLogicalElement class</span></span>

<span data-ttu-id="59613-104">Demande que l’état de l’élément soit remplacé par la valeur spécifiée dans le paramètre RequestedState.</span><span class="sxs-lookup"><span data-stu-id="59613-104">Requests that the state of the element be changed to the value specified in the RequestedState parameter.</span></span> <span data-ttu-id="59613-105">Lorsque la modification d’État demandée a lieu, l’EnabledState et l’RequestedState de l’élément sont identiques.</span><span class="sxs-lookup"><span data-stu-id="59613-105">When the requested state change takes place, the EnabledState and RequestedState of the element will be the same.</span></span> <span data-ttu-id="59613-106">L’appel de la méthode RequestStateChange plusieurs fois peut entraîner le remplacement ou la perte des demandes antérieures.</span><span class="sxs-lookup"><span data-stu-id="59613-106">Invoking the RequestStateChange method multiple times could result in earlier requests being overwritten or lost.</span></span>

## <a name="syntax"></a><span data-ttu-id="59613-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59613-107">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="59613-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59613-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59613-109">*RequestedState* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="59613-109">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59613-110">État demandé pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="59613-110">The state requested for the element.</span></span> <span data-ttu-id="59613-111">Ces informations seront placées dans la propriété **RequestedState** de l’instance si le code de retour de la méthode **RequestStateChange** est 0 (terminé sans erreur») ou 4096 (0X1000) ('Job Started').</span><span class="sxs-lookup"><span data-stu-id="59613-111">This information will be placed into the **RequestedState** property of the instance if the return code of the **RequestStateChange** method is 0 ('Completed with No Error'), or 4096 (0x1000) ('Job Started').</span></span> <span data-ttu-id="59613-112">Reportez-vous à la description des propriétés **EnabledState** et **RequestedState** pour obtenir des explications détaillées sur les valeurs de **RequestedState** .</span><span class="sxs-lookup"><span data-stu-id="59613-112">Refer to the description of the **EnabledState** and **RequestedState** properties for the detailed explanations of the **RequestedState** values.</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="59613-113"><span id="Start"></span><span id="start"></span><span id="START"></span>**Démarrer** (2)</span><span class="sxs-lookup"><span data-stu-id="59613-113"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="59613-114">Modifie l’État en’Running'.</span><span class="sxs-lookup"><span data-stu-id="59613-114">Changes the state to 'Running'.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="59613-115"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspendre** (3)</span><span class="sxs-lookup"><span data-stu-id="59613-115"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="59613-116">Arrête temporairement le travail.</span><span class="sxs-lookup"><span data-stu-id="59613-116">Stops the job temporarily.</span></span> <span data-ttu-id="59613-117">L’objectif est de redémarrer ensuite le travail avec « Start ».</span><span class="sxs-lookup"><span data-stu-id="59613-117">The intention is to subsequently restart the job with 'Start'.</span></span> <span data-ttu-id="59613-118">Il peut être possible d’entrer dans l’État « service » en suspens.</span><span class="sxs-lookup"><span data-stu-id="59613-118">It might be possible to enter the 'Service' state while suspended.</span></span> <span data-ttu-id="59613-119">(Ceci est spécifique à un travail.)</span><span class="sxs-lookup"><span data-stu-id="59613-119">(This is job-specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="59613-120"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminer** (4)</span><span class="sxs-lookup"><span data-stu-id="59613-120"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="59613-121">Arrête le travail proprement dit, enregistre les données, conserve l’État et arrête tous les processus sous-jacents de manière ordonnée.</span><span class="sxs-lookup"><span data-stu-id="59613-121">Stops the job cleanly, saves data, preserves the state, and shuts down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="59613-122"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="59613-122"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="59613-123">Met immédiatement fin à la tâche, sans qu’il soit nécessaire d’enregistrer les données ou de conserver l’État.</span><span class="sxs-lookup"><span data-stu-id="59613-123">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="59613-124"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span><span class="sxs-lookup"><span data-stu-id="59613-124"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="59613-125">Place le travail dans un état de service spécifique au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="59613-125">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="59613-126">Il peut être possible de redémarrer le travail.</span><span class="sxs-lookup"><span data-stu-id="59613-126">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="59613-127"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="59613-127"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="59613-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="59613-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="59613-129">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="59613-129">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59613-130">Peut contenir une référence au [**\_ ConcreteJob CIM**](cim-concretejob.md) créé pour effectuer le suivi de la transition d’État initiée par l’appel de méthode.</span><span class="sxs-lookup"><span data-stu-id="59613-130">May contain a reference to the [**CIM\_ConcreteJob**](cim-concretejob.md) created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="59613-131">*TimeoutPeriod* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="59613-131">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59613-132">Délai d’attente qui spécifie la durée maximale pendant laquelle le client attend la transition vers le nouvel État.</span><span class="sxs-lookup"><span data-stu-id="59613-132">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="59613-133">Le format d’intervalle doit être utilisé pour spécifier le délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="59613-133">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="59613-134">La valeur 0 ou **null** indique que le client n’a aucune exigence de temps pour la transition.</span><span class="sxs-lookup"><span data-stu-id="59613-134">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="59613-135">Si cette propriété ne contient pas 0 ou **null** et que l’implémentation ne prend pas en charge ce paramètre, un code de retour de 4098 (**utilisation du paramètre timeout non pris en charge**) doit être retourné.</span><span class="sxs-lookup"><span data-stu-id="59613-135">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59613-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="59613-136">Return value</span></span>

<span data-ttu-id="59613-137">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="59613-137">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="59613-138">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="59613-138">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="59613-139">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="59613-139">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="59613-140">**Erreur inconnue ou non spécifiée** (2)</span><span class="sxs-lookup"><span data-stu-id="59613-140">**Unknown or Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="59613-141">**Impossible de se terminer dans le délai imparti** (3)</span><span class="sxs-lookup"><span data-stu-id="59613-141">**Cannot complete within Timeout Period** (3)</span></span>
</dt> <dt>

<span data-ttu-id="59613-142">**Échec** (4)</span><span class="sxs-lookup"><span data-stu-id="59613-142">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="59613-143">**Paramètre non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="59613-143">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="59613-144">**En cours d’utilisation** (6)</span><span class="sxs-lookup"><span data-stu-id="59613-144">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="59613-145">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="59613-145">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="59613-146">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="59613-146">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="59613-147">**Transition d’État non valide** (4097)</span><span class="sxs-lookup"><span data-stu-id="59613-147">**Invalid State Transition** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="59613-148">**Utilisation du paramètre timeout non prise en charge** (4098)</span><span class="sxs-lookup"><span data-stu-id="59613-148">**Use of Timeout Parameter Not Supported** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="59613-149">**Occupé** (4099)</span><span class="sxs-lookup"><span data-stu-id="59613-149">**Busy** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="59613-150">**Méthode réservée** (4100.. 32767)</span><span class="sxs-lookup"><span data-stu-id="59613-150">**Method Reserved** (4100..32767)</span></span>
</dt> <dt>

<span data-ttu-id="59613-151">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="59613-151">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="59613-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59613-152">Requirements</span></span>



| <span data-ttu-id="59613-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59613-153">Requirement</span></span> | <span data-ttu-id="59613-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="59613-154">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59613-155">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59613-155">Minimum supported client</span></span><br/> | <span data-ttu-id="59613-156">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="59613-156">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="59613-157">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59613-157">Minimum supported server</span></span><br/> | <span data-ttu-id="59613-158">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="59613-158">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="59613-159">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="59613-159">Namespace</span></span><br/>                | <span data-ttu-id="59613-160">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="59613-160">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="59613-161">MOF</span><span class="sxs-lookup"><span data-stu-id="59613-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="59613-162"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="59613-162"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="59613-163">DLL</span><span class="sxs-lookup"><span data-stu-id="59613-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59613-164"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="59613-164"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="59613-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59613-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59613-166">**\_ENABLEDLOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="59613-166">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

 




