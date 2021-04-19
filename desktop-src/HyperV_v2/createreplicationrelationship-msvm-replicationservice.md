---
description: Crée une relation de réplication pour un ordinateur virtuel. Lorsqu’un client appelle cette méthode pour un ordinateur virtuel de réplication, il étend la relation de réplication au fournisseur spécifié.
ms.assetid: 44d3b5aa-46c2-4fe9-9a1d-6ee699d3640d
title: Méthode CreateReplicationRelationship de la classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.CreateReplicationRelationship
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c44628aef9aa278170a1292a74621419bb6256b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521812"
---
# <a name="createreplicationrelationship-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="011fe-104">Méthode CreateReplicationRelationship de la \_ classe ReplicationService MSVM</span><span class="sxs-lookup"><span data-stu-id="011fe-104">CreateReplicationRelationship method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="011fe-105">Crée une relation de réplication pour un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="011fe-105">Creates a new replication relationship for a virtual machine.</span></span> <span data-ttu-id="011fe-106">Lorsqu’un client appelle cette méthode pour un ordinateur virtuel de réplication, il étend la relation de réplication au fournisseur spécifié.</span><span class="sxs-lookup"><span data-stu-id="011fe-106">When a client calls this method for a replica virtual machine, it extends the replication relationship to the specified provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="011fe-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="011fe-107">Syntax</span></span>


```mof
uint32 CreateReplicationRelationship(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="011fe-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="011fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="011fe-109">*ComputerSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="011fe-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="011fe-110">Référence à une instance [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente l’ordinateur virtuel pour lequel la réplication doit être activée.</span><span class="sxs-lookup"><span data-stu-id="011fe-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication should be enabled.</span></span>

</dd> <dt>

<span data-ttu-id="011fe-111">*ReplicationSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="011fe-111">*ReplicationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="011fe-112">Représentation sous forme de chaîne d’une instance de la classe [**MSVM \_ ReplicationSettingData**](msvm-replicationsettingdata.md) qui définit les paramètres de réplication pour la nouvelle relation de réplication à créer pour l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="011fe-112">A string representation of an instance of the [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) class that defines the replication settings for the new replication relationship to be created for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="011fe-113">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="011fe-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="011fe-114">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="011fe-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="011fe-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="011fe-115">Return value</span></span>

<span data-ttu-id="011fe-116">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="011fe-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="011fe-117">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="011fe-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="011fe-118">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="011fe-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="011fe-119">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="011fe-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="011fe-120">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="011fe-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="011fe-121">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="011fe-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="011fe-122">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="011fe-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="011fe-123">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="011fe-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="011fe-124">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="011fe-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="011fe-125">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="011fe-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="011fe-126">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="011fe-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="011fe-127">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="011fe-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="011fe-128">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="011fe-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="011fe-129">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="011fe-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="011fe-130">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="011fe-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="011fe-131">Notes</span><span class="sxs-lookup"><span data-stu-id="011fe-131">Remarks</span></span>

<span data-ttu-id="011fe-132">**CreateReplicationRelationship** prend une instance [**MSVM \_ ReplicationSettingData**](msvm-replicationsettingdata.md) (FRSD) comme entrée.</span><span class="sxs-lookup"><span data-stu-id="011fe-132">**CreateReplicationRelationship** takes an [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) instance (FRSD) as input.</span></span> <span data-ttu-id="011fe-133">Le FRSD associé à l’ordinateur virtuel en tant que fournisseur hôte à hôte est le choix par défaut.</span><span class="sxs-lookup"><span data-stu-id="011fe-133">The associated FRSD for the virtual machine as host-to-host provider is the default choice.</span></span> <span data-ttu-id="011fe-134">L’entrée FRSD est validée pour les paramètres valides pour chaque propriété du fournisseur par défaut.</span><span class="sxs-lookup"><span data-stu-id="011fe-134">Input FRSD is validated for valid settings for each property for the default provider.</span></span> <span data-ttu-id="011fe-135">Ce tableau résume les différences de validation par rapport au fournisseur externe.</span><span class="sxs-lookup"><span data-stu-id="011fe-135">This table summarizes the validation differences with respect to the external provider.</span></span>



| <span data-ttu-id="011fe-136">Propriété</span><span class="sxs-lookup"><span data-stu-id="011fe-136">Property</span></span>                                             | <span data-ttu-id="011fe-137">Fournisseurs externes</span><span class="sxs-lookup"><span data-stu-id="011fe-137">External providers</span></span>                                 |
|------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="011fe-138">ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="011fe-138">ReplicationProvider</span></span>                                  | <span data-ttu-id="011fe-139">Identique au fournisseur par défaut</span><span class="sxs-lookup"><span data-stu-id="011fe-139">Same as default provider</span></span>                           |
| <span data-ttu-id="011fe-140">AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="011fe-140">AuthenticationType</span></span>                                   | <span data-ttu-id="011fe-141">Ignoré</span><span class="sxs-lookup"><span data-stu-id="011fe-141">Ignored</span></span>                                            |
| <span data-ttu-id="011fe-142">CertificateThumbPrint</span><span class="sxs-lookup"><span data-stu-id="011fe-142">CertificateThumbPrint</span></span>                                | <span data-ttu-id="011fe-143">Ignoré</span><span class="sxs-lookup"><span data-stu-id="011fe-143">Ignored</span></span>                                            |
| <span data-ttu-id="011fe-144">RootCertificateThumbPrint (RO)</span><span class="sxs-lookup"><span data-stu-id="011fe-144">RootCertificateThumbPrint (RO)</span></span>                       | <span data-ttu-id="011fe-145">Ignoré</span><span class="sxs-lookup"><span data-stu-id="011fe-145">Ignored</span></span>                                            |
| <span data-ttu-id="011fe-146">CompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="011fe-146">CompressionEnabled</span></span>                                   | <span data-ttu-id="011fe-147">Identique au fournisseur par défaut</span><span class="sxs-lookup"><span data-stu-id="011fe-147">Same as default provider</span></span>                           |
| <span data-ttu-id="011fe-148">BypassProxyServer</span><span class="sxs-lookup"><span data-stu-id="011fe-148">BypassProxyServer</span></span>                                    | <span data-ttu-id="011fe-149">Identique au fournisseur par défaut</span><span class="sxs-lookup"><span data-stu-id="011fe-149">Same as default provider</span></span>                           |
| <span data-ttu-id="011fe-150">RecoveryConnectionPoint</span><span class="sxs-lookup"><span data-stu-id="011fe-150">RecoveryConnectionPoint</span></span>                              | <span data-ttu-id="011fe-151">Ignoré \* (peut changer si le fournisseur a besoin)</span><span class="sxs-lookup"><span data-stu-id="011fe-151">Ignored\* (may change if provider has requirement)</span></span> |
| <span data-ttu-id="011fe-152">RecoveryHostSystem (RO)</span><span class="sxs-lookup"><span data-stu-id="011fe-152">RecoveryHostSystem (RO)</span></span>                              | <span data-ttu-id="011fe-153">Ignoré</span><span class="sxs-lookup"><span data-stu-id="011fe-153">Ignored</span></span>                                            |
| <span data-ttu-id="011fe-154">PrimaryConnectionPoint (RO)</span><span class="sxs-lookup"><span data-stu-id="011fe-154">PrimaryConnectionPoint (RO)</span></span>                          | <span data-ttu-id="011fe-155">Identique au fournisseur par défaut</span><span class="sxs-lookup"><span data-stu-id="011fe-155">Same as default provider</span></span>                           |
| <span data-ttu-id="011fe-156">PrimaryHostSystem (RO)</span><span class="sxs-lookup"><span data-stu-id="011fe-156">PrimaryHostSystem (RO)</span></span>                               | <span data-ttu-id="011fe-157">Identique au fournisseur par défaut</span><span class="sxs-lookup"><span data-stu-id="011fe-157">Same as default provider</span></span>                           |
| <span data-ttu-id="011fe-158">RecoveryServerPortNumber</span><span class="sxs-lookup"><span data-stu-id="011fe-158">RecoveryServerPortNumber</span></span>                             | <span data-ttu-id="011fe-159">Ignoré \* (peut changer si le fournisseur a besoin)</span><span class="sxs-lookup"><span data-stu-id="011fe-159">Ignored\* (may change if provider has requirement)</span></span> |
| <span data-ttu-id="011fe-160">ReplicateHostKvpItems</span><span class="sxs-lookup"><span data-stu-id="011fe-160">ReplicateHostKvpItems</span></span>                                | <span data-ttu-id="011fe-161">Ignoré</span><span class="sxs-lookup"><span data-stu-id="011fe-161">Ignored</span></span>                                            |
| <span data-ttu-id="011fe-162">ApplicationConsistentSnapshotInterval</span><span class="sxs-lookup"><span data-stu-id="011fe-162">ApplicationConsistentSnapshotInterval</span></span>                | <span data-ttu-id="011fe-163">Identique au fournisseur par défaut</span><span class="sxs-lookup"><span data-stu-id="011fe-163">Same as default provider</span></span>                           |
| <span data-ttu-id="011fe-164">RecoveryHistory</span><span class="sxs-lookup"><span data-stu-id="011fe-164">RecoveryHistory</span></span>                                      | <span data-ttu-id="011fe-165">Identique au fournisseur par défaut</span><span class="sxs-lookup"><span data-stu-id="011fe-165">Same as default provider</span></span>                           |
| <span data-ttu-id="011fe-166">IncludedDisks\[\]</span><span class="sxs-lookup"><span data-stu-id="011fe-166">IncludedDisks\[\]</span></span>                                    | <span data-ttu-id="011fe-167">Identique au fournisseur par défaut</span><span class="sxs-lookup"><span data-stu-id="011fe-167">Same as default provider</span></span>                           |
| <span data-ttu-id="011fe-168">AutoResynchronizeEnabled</span><span class="sxs-lookup"><span data-stu-id="011fe-168">AutoResynchronizeEnabled</span></span>                             | <span data-ttu-id="011fe-169">Identique au fournisseur par défaut</span><span class="sxs-lookup"><span data-stu-id="011fe-169">Same as default provider</span></span>                           |
| <span data-ttu-id="011fe-170">AutoResynchronizeIntervalStart</span><span class="sxs-lookup"><span data-stu-id="011fe-170">AutoResynchronizeIntervalStart</span></span>                       | <span data-ttu-id="011fe-171">Identique au fournisseur par défaut</span><span class="sxs-lookup"><span data-stu-id="011fe-171">Same as default provider</span></span>                           |
| <span data-ttu-id="011fe-172">AutoResynchronizeIntervalEnd</span><span class="sxs-lookup"><span data-stu-id="011fe-172">AutoResynchronizeIntervalEnd</span></span>                         | <span data-ttu-id="011fe-173">Identique au fournisseur par défaut</span><span class="sxs-lookup"><span data-stu-id="011fe-173">Same as default provider</span></span>                           |
| <span data-ttu-id="011fe-174">EnableWriteOrderPreservationAcrossDisks (déconseillée)</span><span class="sxs-lookup"><span data-stu-id="011fe-174">EnableWriteOrderPreservationAcrossDisks (Deprecated)</span></span> | <span data-ttu-id="011fe-175">Identique au fournisseur par défaut</span><span class="sxs-lookup"><span data-stu-id="011fe-175">Same as default provider</span></span>                           |
| <span data-ttu-id="011fe-176">ReplicationInterval</span><span class="sxs-lookup"><span data-stu-id="011fe-176">ReplicationInterval</span></span>                                  | <span data-ttu-id="011fe-177">Identique au fournisseur par défaut</span><span class="sxs-lookup"><span data-stu-id="011fe-177">Same as default provider</span></span>                           |



 

## <a name="requirements"></a><span data-ttu-id="011fe-178">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="011fe-178">Requirements</span></span>



| <span data-ttu-id="011fe-179">Condition requise</span><span class="sxs-lookup"><span data-stu-id="011fe-179">Requirement</span></span> | <span data-ttu-id="011fe-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="011fe-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="011fe-181">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="011fe-181">Minimum supported client</span></span><br/> | <span data-ttu-id="011fe-182">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="011fe-182">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="011fe-183">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="011fe-183">Minimum supported server</span></span><br/> | <span data-ttu-id="011fe-184">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="011fe-184">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="011fe-185">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="011fe-185">Namespace</span></span><br/>                | <span data-ttu-id="011fe-186">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="011fe-186">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="011fe-187">MOF</span><span class="sxs-lookup"><span data-stu-id="011fe-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="011fe-188"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="011fe-188"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="011fe-189">DLL</span><span class="sxs-lookup"><span data-stu-id="011fe-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="011fe-190"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="011fe-190"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="011fe-191">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="011fe-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="011fe-192">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="011fe-192">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="011fe-193">**RemoveReplicationRelationshipEx**</span><span class="sxs-lookup"><span data-stu-id="011fe-193">**RemoveReplicationRelationshipEx**</span></span>](removereplicationrelationshipex-msvm-replicationservice.md)
</dt> </dl>

 

