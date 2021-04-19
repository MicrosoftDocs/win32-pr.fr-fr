---
description: Demande un changement d’État.
ms.assetid: 53c24e17-2b59-4439-a6d1-e971c189d223
title: Méthode RequestStateChange de la classe Msvm_VirtualSystemReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5612371738915b5e38657eca0773a88e31e3b0d2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106523759"
---
# <a name="requeststatechange-method-of-the-msvm_virtualsystemreferencepointexportjob-class"></a><span data-ttu-id="f3a96-103">Méthode RequestStateChange de la \_ classe MSVM VirtualSystemReferencePointExportJob</span><span class="sxs-lookup"><span data-stu-id="f3a96-103">RequestStateChange method of the Msvm\_VirtualSystemReferencePointExportJob class</span></span>

<span data-ttu-id="f3a96-104">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="f3a96-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3a96-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f3a96-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="f3a96-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f3a96-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3a96-107">*RequestedState* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f3a96-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3a96-108">Modifie l’état d’un travail.</span><span class="sxs-lookup"><span data-stu-id="f3a96-108">Changes the state of a job.</span></span> <span data-ttu-id="f3a96-109">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="f3a96-109">The possible values are as follows:</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="f3a96-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Démarrer** (2)</span><span class="sxs-lookup"><span data-stu-id="f3a96-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f3a96-111">Modifie l’État en’Running'.</span><span class="sxs-lookup"><span data-stu-id="f3a96-111">Changes the state to 'Running'.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="f3a96-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspendre** (3)</span><span class="sxs-lookup"><span data-stu-id="f3a96-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f3a96-113">Arrête temporairement le travail.</span><span class="sxs-lookup"><span data-stu-id="f3a96-113">Stops the job temporarily.</span></span> <span data-ttu-id="f3a96-114">L’objectif est de redémarrer ensuite le travail avec « Start ».</span><span class="sxs-lookup"><span data-stu-id="f3a96-114">The intention is to subsequently restart the job with 'Start'.</span></span> <span data-ttu-id="f3a96-115">Il peut être possible d’entrer dans l’État « service » en suspens.</span><span class="sxs-lookup"><span data-stu-id="f3a96-115">It might be possible to enter the 'Service' state while suspended.</span></span> <span data-ttu-id="f3a96-116">(Ceci est spécifique à un travail.)</span><span class="sxs-lookup"><span data-stu-id="f3a96-116">(This is job-specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="f3a96-117"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminer** (4)</span><span class="sxs-lookup"><span data-stu-id="f3a96-117"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f3a96-118">Arrête le travail proprement dit, enregistre les données, conserve l’État et arrête tous les processus sous-jacents de manière ordonnée.</span><span class="sxs-lookup"><span data-stu-id="f3a96-118">Stops the job cleanly, saves data, preserves the state, and shuts down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="f3a96-119"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="f3a96-119"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f3a96-120">Met immédiatement fin à la tâche, sans qu’il soit nécessaire d’enregistrer les données ou de conserver l’État.</span><span class="sxs-lookup"><span data-stu-id="f3a96-120">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f3a96-121"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span><span class="sxs-lookup"><span data-stu-id="f3a96-121"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f3a96-122">Place le travail dans un état de service spécifique au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="f3a96-122">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="f3a96-123">Il peut être possible de redémarrer le travail.</span><span class="sxs-lookup"><span data-stu-id="f3a96-123">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f3a96-124"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="f3a96-124"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="f3a96-125"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="f3a96-125"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="f3a96-126">*TimeoutPeriod* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f3a96-126">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3a96-127">Délai d’attente qui spécifie la durée maximale pendant laquelle le client attend la transition vers le nouvel État.</span><span class="sxs-lookup"><span data-stu-id="f3a96-127">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="f3a96-128">Le format d’intervalle doit être utilisé pour spécifier le délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="f3a96-128">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="f3a96-129">La valeur 0 ou **null** indique que le client n’a aucune exigence de temps pour la transition.</span><span class="sxs-lookup"><span data-stu-id="f3a96-129">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="f3a96-130">Si cette propriété ne contient pas 0 ou **null** et que l’implémentation ne prend pas en charge ce paramètre, un code de retour de 4098 (**utilisation du paramètre timeout non pris en charge**) doit être retourné.</span><span class="sxs-lookup"><span data-stu-id="f3a96-130">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3a96-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f3a96-131">Return value</span></span>

<span data-ttu-id="f3a96-132">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="f3a96-132">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

 <span data-ttu-id="f3a96-133"> (0)</span><span class="sxs-lookup"><span data-stu-id="f3a96-133">(0)</span></span>
</dt> <dt>

 <span data-ttu-id="f3a96-134">(32768)</span><span class="sxs-lookup"><span data-stu-id="f3a96-134">(32768)</span></span>
</dt> <dt>

 <span data-ttu-id="f3a96-135">(32769)</span><span class="sxs-lookup"><span data-stu-id="f3a96-135">(32769)</span></span>
</dt> <dt>

 <span data-ttu-id="f3a96-136">(32770)</span><span class="sxs-lookup"><span data-stu-id="f3a96-136">(32770)</span></span>
</dt> <dt>

 <span data-ttu-id="f3a96-137">(32771)</span><span class="sxs-lookup"><span data-stu-id="f3a96-137">(32771)</span></span>
</dt> <dt>

 <span data-ttu-id="f3a96-138">(32772)</span><span class="sxs-lookup"><span data-stu-id="f3a96-138">(32772)</span></span>
</dt> <dt>

 <span data-ttu-id="f3a96-139">(32773)</span><span class="sxs-lookup"><span data-stu-id="f3a96-139">(32773)</span></span>
</dt> <dt>

 <span data-ttu-id="f3a96-140">(32774)</span><span class="sxs-lookup"><span data-stu-id="f3a96-140">(32774)</span></span>
</dt> <dt>

 <span data-ttu-id="f3a96-141">(32775)</span><span class="sxs-lookup"><span data-stu-id="f3a96-141">(32775)</span></span>
</dt> <dt>

 <span data-ttu-id="f3a96-142">(32776)</span><span class="sxs-lookup"><span data-stu-id="f3a96-142">(32776)</span></span>
</dt> <dt>

 <span data-ttu-id="f3a96-143">(32777)</span><span class="sxs-lookup"><span data-stu-id="f3a96-143">(32777)</span></span>
</dt> <dt>

 <span data-ttu-id="f3a96-144">(32778)</span><span class="sxs-lookup"><span data-stu-id="f3a96-144">(32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f3a96-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f3a96-145">Requirements</span></span>



| <span data-ttu-id="f3a96-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f3a96-146">Requirement</span></span> | <span data-ttu-id="f3a96-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3a96-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3a96-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3a96-148">Minimum supported client</span></span><br/> | <span data-ttu-id="f3a96-149">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f3a96-149">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f3a96-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3a96-150">Minimum supported server</span></span><br/> | <span data-ttu-id="f3a96-151">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f3a96-151">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f3a96-152">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f3a96-152">Namespace</span></span><br/>                | <span data-ttu-id="f3a96-153">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="f3a96-153">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f3a96-154">MOF</span><span class="sxs-lookup"><span data-stu-id="f3a96-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3a96-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f3a96-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f3a96-156">DLL</span><span class="sxs-lookup"><span data-stu-id="f3a96-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3a96-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f3a96-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f3a96-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3a96-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3a96-159">**MSVM \_ VirtualSystemReferencePointExportJob**</span><span class="sxs-lookup"><span data-stu-id="f3a96-159">**Msvm\_VirtualSystemReferencePointExportJob**</span></span>](msvm-virtualsystemreferencepointexportjob.md)
</dt> </dl>

 

 




