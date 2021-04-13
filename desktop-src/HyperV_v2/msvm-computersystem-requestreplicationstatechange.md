---
description: Demande que l’état de réplication de l’ordinateur virtuel soit remplacé par la valeur spécifiée et agit sur la relation de réplication principale de la machine virtuelle.
ms.assetid: 65FCDADD-1C50-4816-B10B-A951D1FC9C3B
title: Méthode RequestReplicationStateChange de la classe Msvm_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.RequestReplicationStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 32f0136662f043627a5fad152ee0e0aaa1845e1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528533"
---
# <a name="requestreplicationstatechange-method-of-the-msvm_computersystem-class"></a><span data-ttu-id="421c1-103">Méthode RequestReplicationStateChange de la \_ classe MSVM ComputerSystem</span><span class="sxs-lookup"><span data-stu-id="421c1-103">RequestReplicationStateChange method of the Msvm\_ComputerSystem class</span></span>

<span data-ttu-id="421c1-104">Demande que l’état de réplication de l’ordinateur virtuel soit remplacé par la valeur spécifiée et agit sur la relation de réplication principale de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="421c1-104">Requests that the replication state of the virtual machine be changed to the specified value and acts on the primary replication relationship of the virtual machine.</span></span> <span data-ttu-id="421c1-105">Pendant que le changement d’État est en cours, la propriété **ReplicationState** est remplacée par la valeur du paramètre *RequestedState* .</span><span class="sxs-lookup"><span data-stu-id="421c1-105">While the state change is in progress, the **ReplicationState** property is changed to the value of the *RequestedState* parameter.</span></span> <span data-ttu-id="421c1-106">Cette méthode est prise en charge uniquement pour les instances de la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) qui représentent un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="421c1-106">This method is only supported for instances of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represent a virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="421c1-107">À partir de Windows 8.1, nous vous recommandons de ne pas utiliser **RequestReplicationStateChange** plus pour demander le changement d’état de réplication.</span><span class="sxs-lookup"><span data-stu-id="421c1-107">Starting with Windows 8.1, we recommend not to use **RequestReplicationStateChange** anymore to request changing of replication state.</span></span> <span data-ttu-id="421c1-108">Utilisez plutôt [**RequestReplicationStateChangeEx**](msvm-requestreplicationstatechangeex-computersystem.md).</span><span class="sxs-lookup"><span data-stu-id="421c1-108">Instead, use [**RequestReplicationStateChangeEx**](msvm-requestreplicationstatechangeex-computersystem.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="421c1-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="421c1-109">Syntax</span></span>


```mof
uint32 RequestReplicationStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="421c1-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="421c1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="421c1-111">*RequestedState* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="421c1-111">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="421c1-112">Nouvel état de réplication.</span><span class="sxs-lookup"><span data-stu-id="421c1-112">The new replication state.</span></span> <span data-ttu-id="421c1-113">Doit avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="421c1-113">The must be one of the following values.</span></span>

<dt>

<span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>

<span data-ttu-id="421c1-114"><span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>**Prêt à démarrer la réplication initiale** (1)</span><span class="sxs-lookup"><span data-stu-id="421c1-114"><span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>**Ready to start initial replication** (1)</span></span>


</dt> <dd>

<span data-ttu-id="421c1-115">Prêt à démarrer la réplication initiale.</span><span class="sxs-lookup"><span data-stu-id="421c1-115">Ready to start initial replication.</span></span>

</dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="421c1-116"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**En attente de l’exécution de la réplication initiale** (2)</span><span class="sxs-lookup"><span data-stu-id="421c1-116"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Waiting to complete initial replication** (2)</span></span>


</dt> <dd>

<span data-ttu-id="421c1-117">En attente de l’exécution de la réplication initiale.</span><span class="sxs-lookup"><span data-stu-id="421c1-117">Waiting to complete initial replication.</span></span>

</dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="421c1-118"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Réplication** (3)</span><span class="sxs-lookup"><span data-stu-id="421c1-118"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicating** (3)</span></span>


</dt> <dd>

<span data-ttu-id="421c1-119">Réplication.</span><span class="sxs-lookup"><span data-stu-id="421c1-119">Replicating.</span></span>

</dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="421c1-120"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Réplication synchronisée terminée** (4)</span><span class="sxs-lookup"><span data-stu-id="421c1-120"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Synced replication complete** (4)</span></span>


</dt> <dd>

<span data-ttu-id="421c1-121">Réplication synchronisée terminée.</span><span class="sxs-lookup"><span data-stu-id="421c1-121">Synced replication complete.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="421c1-122"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspendre** (7)</span><span class="sxs-lookup"><span data-stu-id="421c1-122"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (7)</span></span>


</dt> <dd>

<span data-ttu-id="421c1-123">Suspend la réplication.</span><span class="sxs-lookup"><span data-stu-id="421c1-123">Suspend replication.</span></span>

</dd> <dt>

<span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>

<span data-ttu-id="421c1-124"><span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>**Annuler la resynchronisation** (9)</span><span class="sxs-lookup"><span data-stu-id="421c1-124"><span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>**Cancel Resynchronize** (9)</span></span>


</dt> <dd>

<span data-ttu-id="421c1-125">Annulez la resynchronisation.</span><span class="sxs-lookup"><span data-stu-id="421c1-125">Cancel resynchronization.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="421c1-126">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="421c1-126">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="421c1-127">Référence facultative à un objet [**\_ ConcreteJob MSVM**](msvm-concretejob.md) qui est retourné si l’opération est exécutée de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="421c1-127">An optional reference to a [**Msvm\_ConcreteJob**](msvm-concretejob.md) object that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="421c1-128">Si elle est présente, la référence retournée peut être utilisée pour surveiller la progression et obtenir le résultat de la méthode.</span><span class="sxs-lookup"><span data-stu-id="421c1-128">If present, the returned reference can be used to monitor progress and obtain the result of the method.</span></span>

</dd> <dt>

<span data-ttu-id="421c1-129">*TimeoutPeriod* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="421c1-129">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="421c1-130">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="421c1-130">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="421c1-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="421c1-131">Return value</span></span>

<span data-ttu-id="421c1-132">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="421c1-132">This method returns one of the following values.</span></span>



| <span data-ttu-id="421c1-133">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="421c1-133">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="421c1-134">Description</span><span class="sxs-lookup"><span data-stu-id="421c1-134">Description</span></span>                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="421c1-135"><dt>**Terminé sans erreur**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="421c1-135"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="421c1-136">Succès</span><span class="sxs-lookup"><span data-stu-id="421c1-136">Success</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="421c1-137"><dt>**Paramètres de méthode activés-travail démarré**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="421c1-137"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="421c1-138">La transition est asynchrone.</span><span class="sxs-lookup"><span data-stu-id="421c1-138">The transition is asynchronous.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="421c1-139"><dt>**Échec**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="421c1-139"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                 |                                                                                                                             |
| <dl> <span data-ttu-id="421c1-140"><dt>**Accès refusé**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="421c1-140"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="421c1-141"><dt>**Non pris en charge**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="421c1-141"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="421c1-142">L' <dt>**État est inconnu**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="421c1-142"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                      |                                                                                                                             |
| <dl> <span data-ttu-id="421c1-143"><dt>**Délai d’expiration**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="421c1-143"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                                |                                                                                                                             |
| <dl> <span data-ttu-id="421c1-144"><dt>**Paramètre non valide**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="421c1-144"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                      | <span data-ttu-id="421c1-145">La valeur spécifiée dans l’un des paramètres n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="421c1-145">The value specified in one of the parameters is not supported.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="421c1-146">Le <dt>**système est en cours d’utilisation**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="421c1-146"><dt>**System is in use**</dt> <dt>32774</dt></span></span> </dl>                       |                                                                                                                             |
| <dl> <span data-ttu-id="421c1-147"><dt>**État non valide pour cette opération**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="421c1-147"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>       | <span data-ttu-id="421c1-148">La valeur spécifiée dans le paramètre *RequestedState* n’est pas prise en charge dans le mode de réplication ou l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="421c1-148">The value specified in the *RequestedState* parameter is not supported in the current replication mode or state.</span></span><br/> |
| <dl> <span data-ttu-id="421c1-149"><dt>**Type de données incorrect**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="421c1-149"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                    |                                                                                                                             |
| <dl> <span data-ttu-id="421c1-150">Le <dt>**système n’est pas disponible**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="421c1-150"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>                |                                                                                                                             |
| <dl> <span data-ttu-id="421c1-151"><dt>**Mémoire Insuffisante**</dt> <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="421c1-151"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="421c1-152"><dt>**Fichier introuvable**</dt> <dt>32779</dt></span><span class="sxs-lookup"><span data-stu-id="421c1-152"><dt>**File not found**</dt> <dt>32779</dt></span></span> </dl>                         |                                                                                                                             |



 

## <a name="requirements"></a><span data-ttu-id="421c1-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="421c1-153">Requirements</span></span>



| <span data-ttu-id="421c1-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="421c1-154">Requirement</span></span> | <span data-ttu-id="421c1-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="421c1-155">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="421c1-156">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="421c1-156">Minimum supported client</span></span><br/> | <span data-ttu-id="421c1-157">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="421c1-157">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="421c1-158">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="421c1-158">Minimum supported server</span></span><br/> | <span data-ttu-id="421c1-159">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="421c1-159">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="421c1-160">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="421c1-160">Namespace</span></span><br/>                | <span data-ttu-id="421c1-161">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="421c1-161">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="421c1-162">MOF</span><span class="sxs-lookup"><span data-stu-id="421c1-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="421c1-163"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="421c1-163"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="421c1-164">DLL</span><span class="sxs-lookup"><span data-stu-id="421c1-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="421c1-165"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="421c1-165"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="421c1-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="421c1-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="421c1-167">**MSVM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="421c1-167">**Msvm\_ComputerSystem**</span></span>](msvm-computersystem.md)
</dt> </dl>

 

 




