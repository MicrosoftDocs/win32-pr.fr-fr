---
description: Demande un changement d’État.
ms.assetid: 2960bc44-f2af-49c6-9c33-5d9e1ad8056c
title: Méthode RequestStateChange de la classe Msvm_StorageJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1ce563fdae2e73ba2e6994afc3d70c8d4d6fe34a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866394"
---
# <a name="requeststatechange-method-of-the-msvm_storagejob-class"></a><span data-ttu-id="9eecb-103">Méthode RequestStateChange de la \_ classe MSVM StorageJob</span><span class="sxs-lookup"><span data-stu-id="9eecb-103">RequestStateChange method of the Msvm\_StorageJob class</span></span>

<span data-ttu-id="9eecb-104">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="9eecb-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="9eecb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9eecb-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="9eecb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9eecb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9eecb-107">*RequestedState* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9eecb-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eecb-108">RequestStateChange modifie l’état d’un travail.</span><span class="sxs-lookup"><span data-stu-id="9eecb-108">RequestStateChange changes the state of a job.</span></span> <span data-ttu-id="9eecb-109">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9eecb-109">The possible values are as follows:</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="9eecb-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Démarrer** (2)</span><span class="sxs-lookup"><span data-stu-id="9eecb-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9eecb-111">Modifie l’État en’Running'.</span><span class="sxs-lookup"><span data-stu-id="9eecb-111">Changes the state to 'Running'.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="9eecb-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspendre** (3)</span><span class="sxs-lookup"><span data-stu-id="9eecb-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9eecb-113">Arrête temporairement le travail.</span><span class="sxs-lookup"><span data-stu-id="9eecb-113">Stops the job temporarily.</span></span> <span data-ttu-id="9eecb-114">L’objectif est de redémarrer ensuite le travail avec « Start ».</span><span class="sxs-lookup"><span data-stu-id="9eecb-114">The intention is to subsequently restart the job with 'Start'.</span></span> <span data-ttu-id="9eecb-115">Il peut être possible d’entrer dans l’État « service » en suspens.</span><span class="sxs-lookup"><span data-stu-id="9eecb-115">It might be possible to enter the 'Service' state while suspended.</span></span> <span data-ttu-id="9eecb-116">(Ceci est spécifique à un travail.)</span><span class="sxs-lookup"><span data-stu-id="9eecb-116">(This is job-specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="9eecb-117"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminer** (4)</span><span class="sxs-lookup"><span data-stu-id="9eecb-117"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9eecb-118">Arrête le travail proprement dit, enregistre les données, conserve l’État et arrête tous les processus sous-jacents de manière ordonnée.</span><span class="sxs-lookup"><span data-stu-id="9eecb-118">Stops the job cleanly, saves data, preserves the state, and shuts down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="9eecb-119"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="9eecb-119"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="9eecb-120">Met immédiatement fin à la tâche, sans qu’il soit nécessaire d’enregistrer les données ou de conserver l’État.</span><span class="sxs-lookup"><span data-stu-id="9eecb-120">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9eecb-121"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span><span class="sxs-lookup"><span data-stu-id="9eecb-121"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="9eecb-122">Place le travail dans un état de service spécifique au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="9eecb-122">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="9eecb-123">Il peut être possible de redémarrer le travail.</span><span class="sxs-lookup"><span data-stu-id="9eecb-123">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="9eecb-124"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="9eecb-124"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="9eecb-125"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="9eecb-125"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="9eecb-126">*TimeoutPeriod* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9eecb-126">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eecb-127">Délai d’attente qui spécifie la durée maximale pendant laquelle le client attend la transition vers le nouvel État.</span><span class="sxs-lookup"><span data-stu-id="9eecb-127">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="9eecb-128">Le format d’intervalle doit être utilisé pour spécifier le délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="9eecb-128">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="9eecb-129">La valeur 0 ou **null** indique que le client n’a aucune exigence de temps pour la transition.</span><span class="sxs-lookup"><span data-stu-id="9eecb-129">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="9eecb-130">Si cette propriété ne contient pas 0 ou **null** et que l’implémentation ne prend pas en charge ce paramètre, un code de retour de 4098 (**utilisation du paramètre timeout non pris en charge**) doit être retourné.</span><span class="sxs-lookup"><span data-stu-id="9eecb-130">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9eecb-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9eecb-131">Return value</span></span>

<span data-ttu-id="9eecb-132">La méthode retourne l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="9eecb-132">This method returns one of the following values:</span></span>

<dl> <dt>

 <span data-ttu-id="9eecb-133"> (0)</span><span class="sxs-lookup"><span data-stu-id="9eecb-133">(0)</span></span>
</dt> <dt>

 <span data-ttu-id="9eecb-134">(32768)</span><span class="sxs-lookup"><span data-stu-id="9eecb-134">(32768)</span></span>
</dt> <dt>

 <span data-ttu-id="9eecb-135">(32769)</span><span class="sxs-lookup"><span data-stu-id="9eecb-135">(32769)</span></span>
</dt> <dt>

 <span data-ttu-id="9eecb-136">(32770)</span><span class="sxs-lookup"><span data-stu-id="9eecb-136">(32770)</span></span>
</dt> <dt>

 <span data-ttu-id="9eecb-137">(32771)</span><span class="sxs-lookup"><span data-stu-id="9eecb-137">(32771)</span></span>
</dt> <dt>

 <span data-ttu-id="9eecb-138">(32772)</span><span class="sxs-lookup"><span data-stu-id="9eecb-138">(32772)</span></span>
</dt> <dt>

 <span data-ttu-id="9eecb-139">(32773)</span><span class="sxs-lookup"><span data-stu-id="9eecb-139">(32773)</span></span>
</dt> <dt>

 <span data-ttu-id="9eecb-140">(32774)</span><span class="sxs-lookup"><span data-stu-id="9eecb-140">(32774)</span></span>
</dt> <dt>

 <span data-ttu-id="9eecb-141">(32775)</span><span class="sxs-lookup"><span data-stu-id="9eecb-141">(32775)</span></span>
</dt> <dt>

 <span data-ttu-id="9eecb-142">(32776)</span><span class="sxs-lookup"><span data-stu-id="9eecb-142">(32776)</span></span>
</dt> <dt>

 <span data-ttu-id="9eecb-143">(32777)</span><span class="sxs-lookup"><span data-stu-id="9eecb-143">(32777)</span></span>
</dt> <dt>

 <span data-ttu-id="9eecb-144">(32778)</span><span class="sxs-lookup"><span data-stu-id="9eecb-144">(32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="9eecb-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9eecb-145">Requirements</span></span>



| <span data-ttu-id="9eecb-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9eecb-146">Requirement</span></span> | <span data-ttu-id="9eecb-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="9eecb-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9eecb-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9eecb-148">Minimum supported client</span></span><br/> | <span data-ttu-id="9eecb-149">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9eecb-149">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="9eecb-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9eecb-150">Minimum supported server</span></span><br/> | <span data-ttu-id="9eecb-151">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="9eecb-151">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="9eecb-152">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9eecb-152">Namespace</span></span><br/>                | <span data-ttu-id="9eecb-153">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="9eecb-153">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9eecb-154">MOF</span><span class="sxs-lookup"><span data-stu-id="9eecb-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9eecb-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9eecb-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9eecb-156">DLL</span><span class="sxs-lookup"><span data-stu-id="9eecb-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9eecb-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9eecb-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9eecb-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9eecb-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eecb-159">**MSVM \_ StorageJob**</span><span class="sxs-lookup"><span data-stu-id="9eecb-159">**Msvm\_StorageJob**</span></span>](msvm-storagejob.md)
</dt> </dl>

 

 




