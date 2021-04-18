---
description: Demande que l’état de réplication de la relation de réplication de l’ordinateur virtuel soit remplacé par la valeur spécifiée.
ms.assetid: 8EC78CCC-2997-4239-A20C-BA56F848ECB6
title: 'Msvm_ComputerSystem :: RequestReplicationStateChangeEx, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.RequestReplicationStateChangeEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d77db9dff90f985991c8e9013ea4f239cb6479f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526128"
---
# <a name="msvm_computersystemrequestreplicationstatechangeex-method"></a><span data-ttu-id="695f3-103">MSVM \_ ComputerSystem :: RequestReplicationStateChangeEx, méthode</span><span class="sxs-lookup"><span data-stu-id="695f3-103">Msvm\_ComputerSystem::RequestReplicationStateChangeEx method</span></span>

<span data-ttu-id="695f3-104">Demande que l’état de réplication de la relation de réplication de l’ordinateur virtuel soit remplacé par la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="695f3-104">Requests that the replication state of the replication relationship of the virtual machine be changed to the specified value.</span></span> <span data-ttu-id="695f3-105">Pendant que le changement d’État est en cours, la propriété **ReplicationState** est remplacée par la valeur du paramètre *RequestedState* .</span><span class="sxs-lookup"><span data-stu-id="695f3-105">While the state change is in progress, the **ReplicationState** property is changed to the value of the *RequestedState* parameter.</span></span> <span data-ttu-id="695f3-106">Cette méthode est prise en charge uniquement pour les instances de la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) qui représentent un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="695f3-106">This method is only supported for instances of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represent a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="695f3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="695f3-107">Syntax</span></span>


```C++
uint32 RequestReplicationStateChangeEx(
  [in]  string              ReplicationRelationship,
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="695f3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="695f3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="695f3-109">*ReplicationRelationship* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="695f3-109">*ReplicationRelationship* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="695f3-110">Représentation sous forme de chaîne d’une instance incorporée de la classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) qui définit la relation de réplication pour la demande de modification d’État.</span><span class="sxs-lookup"><span data-stu-id="695f3-110">A string representation of an embedded instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that defines the replication relationship for state change request.</span></span> <span data-ttu-id="695f3-111">Ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="695f3-111">This parameter is optional.</span></span> <span data-ttu-id="695f3-112">Lorsqu’elle n’est pas spécifiée, la demande s’exécute sur la relation de réplication principale.</span><span class="sxs-lookup"><span data-stu-id="695f3-112">When it's unspecified, the request runs on the primary replication relationship.</span></span>

</dd> <dt>

<span data-ttu-id="695f3-113">*RequestedState* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="695f3-113">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="695f3-114">Nouvel état de réplication.</span><span class="sxs-lookup"><span data-stu-id="695f3-114">The new replication state.</span></span> <span data-ttu-id="695f3-115">Doit avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="695f3-115">The must be one of the following values.</span></span>

<dt>

<span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>

<span data-ttu-id="695f3-116"><span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>**Prêt à démarrer la réplication initiale** (1)</span><span class="sxs-lookup"><span data-stu-id="695f3-116"><span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>**Ready to start initial replication** (1)</span></span>


</dt> <dd>

<span data-ttu-id="695f3-117">Prêt à démarrer la réplication initiale.</span><span class="sxs-lookup"><span data-stu-id="695f3-117">Ready to start initial replication.</span></span>

</dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="695f3-118"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**En attente de l’exécution de la réplication initiale** (2)</span><span class="sxs-lookup"><span data-stu-id="695f3-118"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Waiting to complete initial replication** (2)</span></span>


</dt> <dd>

<span data-ttu-id="695f3-119">En attente de l’exécution de la réplication initiale.</span><span class="sxs-lookup"><span data-stu-id="695f3-119">Waiting to complete initial replication.</span></span>

</dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="695f3-120"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Réplication** (3)</span><span class="sxs-lookup"><span data-stu-id="695f3-120"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicating** (3)</span></span>


</dt> <dd>

<span data-ttu-id="695f3-121">Réplication.</span><span class="sxs-lookup"><span data-stu-id="695f3-121">Replicating.</span></span>

</dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="695f3-122"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Réplication synchronisée terminée** (4)</span><span class="sxs-lookup"><span data-stu-id="695f3-122"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Synced replication complete** (4)</span></span>


</dt> <dd>

<span data-ttu-id="695f3-123">Réplication synchronisée terminée.</span><span class="sxs-lookup"><span data-stu-id="695f3-123">Synced replication complete.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="695f3-124"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspendre** (7)</span><span class="sxs-lookup"><span data-stu-id="695f3-124"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (7)</span></span>


</dt> <dd>

<span data-ttu-id="695f3-125">Suspend la réplication.</span><span class="sxs-lookup"><span data-stu-id="695f3-125">Suspend replication.</span></span>

</dd> <dt>

<span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>

<span data-ttu-id="695f3-126"><span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>**Annuler la resynchronisation** (9)</span><span class="sxs-lookup"><span data-stu-id="695f3-126"><span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>**Cancel Resynchronize** (9)</span></span>


</dt> <dd>

<span data-ttu-id="695f3-127">Annulez la resynchronisation.</span><span class="sxs-lookup"><span data-stu-id="695f3-127">Cancel resynchronization.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="695f3-128">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="695f3-128">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="695f3-129">Référence facultative à un objet [**\_ ConcreteJob MSVM**](msvm-concretejob.md) qui est retourné si l’opération est exécutée de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="695f3-129">An optional reference to a [**Msvm\_ConcreteJob**](msvm-concretejob.md) object that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="695f3-130">Si elle est présente, la référence retournée peut être utilisée pour surveiller la progression et obtenir le résultat de la méthode.</span><span class="sxs-lookup"><span data-stu-id="695f3-130">If present, the returned reference can be used to monitor progress and obtain the result of the method.</span></span>

</dd> <dt>

<span data-ttu-id="695f3-131">*TimeoutPeriod* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="695f3-131">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="695f3-132">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="695f3-132">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="695f3-133">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="695f3-133">Return value</span></span>

<span data-ttu-id="695f3-134">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="695f3-134">This method returns one of the following values.</span></span>



| <span data-ttu-id="695f3-135">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="695f3-135">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="695f3-136">Description</span><span class="sxs-lookup"><span data-stu-id="695f3-136">Description</span></span>                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="695f3-137"><dt>**Terminé sans erreur**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="695f3-137"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="695f3-138">Succès</span><span class="sxs-lookup"><span data-stu-id="695f3-138">Success</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="695f3-139"><dt>**Paramètres de méthode activés-travail démarré**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="695f3-139"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="695f3-140">La transition est asynchrone.</span><span class="sxs-lookup"><span data-stu-id="695f3-140">The transition is asynchronous.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="695f3-141"><dt>**Échec**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="695f3-141"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                 |                                                                                                                             |
| <dl> <span data-ttu-id="695f3-142"><dt>**Accès refusé**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="695f3-142"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="695f3-143"><dt>**Non pris en charge**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="695f3-143"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="695f3-144">L' <dt>**État est inconnu**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="695f3-144"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                      |                                                                                                                             |
| <dl> <span data-ttu-id="695f3-145"><dt>**Délai d’expiration**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="695f3-145"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                                |                                                                                                                             |
| <dl> <span data-ttu-id="695f3-146"><dt>**Paramètre non valide**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="695f3-146"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                      | <span data-ttu-id="695f3-147">La valeur spécifiée dans l’un des paramètres n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="695f3-147">The value specified in one of the parameters is not supported.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="695f3-148">Le <dt>**système est en cours d’utilisation**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="695f3-148"><dt>**System is in use**</dt> <dt>32774</dt></span></span> </dl>                       |                                                                                                                             |
| <dl> <span data-ttu-id="695f3-149"><dt>**État non valide pour cette opération**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="695f3-149"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>       | <span data-ttu-id="695f3-150">La valeur spécifiée dans le paramètre *RequestedState* n’est pas prise en charge dans le mode de réplication ou l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="695f3-150">The value specified in the *RequestedState* parameter is not supported in the current replication mode or state.</span></span><br/> |
| <dl> <span data-ttu-id="695f3-151"><dt>**Type de données incorrect**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="695f3-151"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                    |                                                                                                                             |
| <dl> <span data-ttu-id="695f3-152">Le <dt>**système n’est pas disponible**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="695f3-152"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>                |                                                                                                                             |
| <dl> <span data-ttu-id="695f3-153"><dt>**Mémoire Insuffisante**</dt> <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="695f3-153"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="695f3-154"><dt>**Fichier introuvable**</dt> <dt>32779</dt></span><span class="sxs-lookup"><span data-stu-id="695f3-154"><dt>**File not found**</dt> <dt>32779</dt></span></span> </dl>                         |                                                                                                                             |



 

## <a name="requirements"></a><span data-ttu-id="695f3-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="695f3-155">Requirements</span></span>



| <span data-ttu-id="695f3-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="695f3-156">Requirement</span></span> | <span data-ttu-id="695f3-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="695f3-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="695f3-158">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="695f3-158">Minimum supported client</span></span><br/> | <span data-ttu-id="695f3-159">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="695f3-159">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="695f3-160">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="695f3-160">Minimum supported server</span></span><br/> | <span data-ttu-id="695f3-161">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="695f3-161">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="695f3-162">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="695f3-162">Namespace</span></span><br/>                | <span data-ttu-id="695f3-163">\\\\\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="695f3-163">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="695f3-164">MOF</span><span class="sxs-lookup"><span data-stu-id="695f3-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="695f3-165"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="695f3-165"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="695f3-166">DLL</span><span class="sxs-lookup"><span data-stu-id="695f3-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="695f3-167"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="695f3-167"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="695f3-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="695f3-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="695f3-169">**MSVM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="695f3-169">**Msvm\_ComputerSystem**</span></span>](msvm-computersystem.md)
</dt> </dl>

 

 




