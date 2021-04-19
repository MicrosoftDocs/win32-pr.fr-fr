---
description: Demande un changement d’État.
ms.assetid: 34d70ff2-4545-4ab7-8c84-6532c342768b
title: Méthode RequestStateChange de la classe Msvm_CollectionReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a3e8b3f3a7249896f023734d049fa3fa772514f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521147"
---
# <a name="requeststatechange-method-of-the-msvm_collectionreferencepointexportjob-class"></a><span data-ttu-id="1bb37-103">Méthode RequestStateChange de la \_ classe MSVM CollectionReferencePointExportJob</span><span class="sxs-lookup"><span data-stu-id="1bb37-103">RequestStateChange method of the Msvm\_CollectionReferencePointExportJob class</span></span>

<span data-ttu-id="1bb37-104">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="1bb37-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bb37-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1bb37-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="1bb37-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1bb37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bb37-107">*RequestedState* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1bb37-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bb37-108">RequestStateChange modifie l’état d’un travail.</span><span class="sxs-lookup"><span data-stu-id="1bb37-108">RequestStateChange changes the state of a job.</span></span> <span data-ttu-id="1bb37-109">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="1bb37-109">The possible values are as follows:</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="1bb37-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Démarrer** (2)</span><span class="sxs-lookup"><span data-stu-id="1bb37-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1bb37-111">Modifie l’État en’Running'.</span><span class="sxs-lookup"><span data-stu-id="1bb37-111">Changes the state to 'Running'.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="1bb37-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspendre** (3)</span><span class="sxs-lookup"><span data-stu-id="1bb37-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1bb37-113">Arrête temporairement le travail.</span><span class="sxs-lookup"><span data-stu-id="1bb37-113">Stops the job temporarily.</span></span> <span data-ttu-id="1bb37-114">L’objectif est de redémarrer ensuite le travail avec « Start ».</span><span class="sxs-lookup"><span data-stu-id="1bb37-114">The intention is to subsequently restart the job with 'Start'.</span></span> <span data-ttu-id="1bb37-115">Il peut être possible d’entrer dans l’État « service » en suspens.</span><span class="sxs-lookup"><span data-stu-id="1bb37-115">It might be possible to enter the 'Service' state while suspended.</span></span> <span data-ttu-id="1bb37-116">(Ceci est spécifique à un travail.)</span><span class="sxs-lookup"><span data-stu-id="1bb37-116">(This is job-specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="1bb37-117"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminer** (4)</span><span class="sxs-lookup"><span data-stu-id="1bb37-117"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="1bb37-118">Arrête le travail proprement dit, enregistre les données, conserve l’État et arrête tous les processus sous-jacents de manière ordonnée.</span><span class="sxs-lookup"><span data-stu-id="1bb37-118">Stops the job cleanly, saves data, preserves the state, and shuts down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="1bb37-119"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="1bb37-119"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="1bb37-120">Met immédiatement fin à la tâche, sans qu’il soit nécessaire d’enregistrer les données ou de conserver l’État.</span><span class="sxs-lookup"><span data-stu-id="1bb37-120">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="1bb37-121"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span><span class="sxs-lookup"><span data-stu-id="1bb37-121"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="1bb37-122">Place le travail dans un état de service spécifique au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="1bb37-122">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="1bb37-123">Il peut être possible de redémarrer le travail.</span><span class="sxs-lookup"><span data-stu-id="1bb37-123">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="1bb37-124"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="1bb37-124"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="1bb37-125"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="1bb37-125"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="1bb37-126">*TimeoutPeriod* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1bb37-126">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bb37-127">Délai d’attente qui spécifie la durée maximale pendant laquelle le client attend la transition vers le nouvel État.</span><span class="sxs-lookup"><span data-stu-id="1bb37-127">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="1bb37-128">Le format d’intervalle doit être utilisé pour spécifier le délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="1bb37-128">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="1bb37-129">La valeur 0 ou **null** indique que le client n’a aucune exigence de temps pour la transition.</span><span class="sxs-lookup"><span data-stu-id="1bb37-129">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="1bb37-130">Si cette propriété ne contient pas 0 ou **null** et que l’implémentation ne prend pas en charge ce paramètre, un code de retour de 4098 (**utilisation du paramètre timeout non pris en charge**) doit être retourné.</span><span class="sxs-lookup"><span data-stu-id="1bb37-130">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bb37-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1bb37-131">Return value</span></span>

<span data-ttu-id="1bb37-132">Retourne 0 en cas de réussite ; Sinon, retourne l’une des erreurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1bb37-132">Returns 0 on success; otherwise, returns one of the following errors.</span></span>

<dl> <dt>

 <span data-ttu-id="1bb37-133"> (0)</span><span class="sxs-lookup"><span data-stu-id="1bb37-133">(0)</span></span>
</dt> <dt>

 <span data-ttu-id="1bb37-134">(32768)</span><span class="sxs-lookup"><span data-stu-id="1bb37-134">(32768)</span></span>
</dt> <dt>

 <span data-ttu-id="1bb37-135">(32769)</span><span class="sxs-lookup"><span data-stu-id="1bb37-135">(32769)</span></span>
</dt> <dt>

 <span data-ttu-id="1bb37-136">(32770)</span><span class="sxs-lookup"><span data-stu-id="1bb37-136">(32770)</span></span>
</dt> <dt>

 <span data-ttu-id="1bb37-137">(32771)</span><span class="sxs-lookup"><span data-stu-id="1bb37-137">(32771)</span></span>
</dt> <dt>

 <span data-ttu-id="1bb37-138">(32772)</span><span class="sxs-lookup"><span data-stu-id="1bb37-138">(32772)</span></span>
</dt> <dt>

 <span data-ttu-id="1bb37-139">(32773)</span><span class="sxs-lookup"><span data-stu-id="1bb37-139">(32773)</span></span>
</dt> <dt>

 <span data-ttu-id="1bb37-140">(32774)</span><span class="sxs-lookup"><span data-stu-id="1bb37-140">(32774)</span></span>
</dt> <dt>

 <span data-ttu-id="1bb37-141">(32775)</span><span class="sxs-lookup"><span data-stu-id="1bb37-141">(32775)</span></span>
</dt> <dt>

 <span data-ttu-id="1bb37-142">(32776)</span><span class="sxs-lookup"><span data-stu-id="1bb37-142">(32776)</span></span>
</dt> <dt>

 <span data-ttu-id="1bb37-143">(32777)</span><span class="sxs-lookup"><span data-stu-id="1bb37-143">(32777)</span></span>
</dt> <dt>

 <span data-ttu-id="1bb37-144">(32778)</span><span class="sxs-lookup"><span data-stu-id="1bb37-144">(32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1bb37-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1bb37-145">Requirements</span></span>



| <span data-ttu-id="1bb37-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1bb37-146">Requirement</span></span> | <span data-ttu-id="1bb37-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="1bb37-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bb37-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1bb37-148">Minimum supported client</span></span><br/> | <span data-ttu-id="1bb37-149">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1bb37-149">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1bb37-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1bb37-150">Minimum supported server</span></span><br/> | <span data-ttu-id="1bb37-151">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="1bb37-151">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="1bb37-152">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1bb37-152">Namespace</span></span><br/>                | <span data-ttu-id="1bb37-153">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="1bb37-153">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1bb37-154">MOF</span><span class="sxs-lookup"><span data-stu-id="1bb37-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1bb37-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1bb37-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1bb37-156">DLL</span><span class="sxs-lookup"><span data-stu-id="1bb37-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1bb37-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1bb37-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1bb37-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1bb37-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bb37-159">**MSVM \_ CollectionReferencePointExportJob**</span><span class="sxs-lookup"><span data-stu-id="1bb37-159">**Msvm\_CollectionReferencePointExportJob**</span></span>](msvm-collectionreferencepointexportjob.md)
</dt> </dl>

 

 




