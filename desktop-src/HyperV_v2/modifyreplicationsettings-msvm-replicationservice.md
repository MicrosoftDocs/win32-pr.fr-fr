---
description: Modifie les paramètres de réplication pour un ordinateur virtuel. Lorsqu’un client appelle cette méthode pour un ordinateur virtuel de réplication, il modifie les paramètres de réplication de la relation de réplication avec le réplica étendu.
ms.assetid: e68514a5-f508-4047-8dcc-6a95f3e3353e
title: Méthode ModifyReplicationSettings de la classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ModifyReplicationSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d1c932f06350324e0d84559724f7ba0412dfb3e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520661"
---
# <a name="modifyreplicationsettings-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="16698-104">Méthode ModifyReplicationSettings de la \_ classe ReplicationService MSVM</span><span class="sxs-lookup"><span data-stu-id="16698-104">ModifyReplicationSettings method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="16698-105">Modifie les paramètres de réplication pour un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="16698-105">Modifies the replication settings for a virtual machine.</span></span> <span data-ttu-id="16698-106">Lorsqu’un client appelle cette méthode pour un ordinateur virtuel de réplication, il modifie les paramètres de réplication de la relation de réplication avec le réplica étendu.</span><span class="sxs-lookup"><span data-stu-id="16698-106">When a client calls this method for a replica virtual machine, it modifies the replication settings of the replication relationship with the extended replica.</span></span>

## <a name="syntax"></a><span data-ttu-id="16698-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16698-107">Syntax</span></span>


```mof
uint32 ModifyReplicationSettings(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="16698-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="16698-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16698-109">*ComputerSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="16698-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16698-110">Référence à une instance [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente l’ordinateur virtuel pour lequel les paramètres de réplication doivent être modifiés.</span><span class="sxs-lookup"><span data-stu-id="16698-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication settings should be modified.</span></span>

</dd> <dt>

<span data-ttu-id="16698-111">*ReplicationSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="16698-111">*ReplicationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16698-112">Représentation sous forme de chaîne de la classe [**MSVM \_ ReplicationSettingData**](msvm-replicationsettingdata.md) qui définit les nouveaux paramètres de réplication.</span><span class="sxs-lookup"><span data-stu-id="16698-112">A string representation of the [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) class that defines the new replication settings.</span></span>

</dd> <dt>

<span data-ttu-id="16698-113">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="16698-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16698-114">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="16698-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16698-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="16698-115">Return value</span></span>

<span data-ttu-id="16698-116">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="16698-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="16698-117">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="16698-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="16698-118">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="16698-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="16698-119">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="16698-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="16698-120">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="16698-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="16698-121">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="16698-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="16698-122">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="16698-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="16698-123">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="16698-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="16698-124">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="16698-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="16698-125">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="16698-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="16698-126">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="16698-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="16698-127">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="16698-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="16698-128">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="16698-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="16698-129">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="16698-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="16698-130">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="16698-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="16698-131">Notes</span><span class="sxs-lookup"><span data-stu-id="16698-131">Remarks</span></span>

<span data-ttu-id="16698-132">**ModifyReplicationSettings** prend une instance [**MSVM \_ ReplicationSettingData**](msvm-replicationsettingdata.md) (FRSD) comme entrée.</span><span class="sxs-lookup"><span data-stu-id="16698-132">**ModifyReplicationSettings** takes an [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) instance (FRSD) as input.</span></span> <span data-ttu-id="16698-133">Le FRSD associé à l’ordinateur virtuel en tant que fournisseur hôte à hôte est le choix par défaut.</span><span class="sxs-lookup"><span data-stu-id="16698-133">The associated FRSD for the virtual machine as host-to-host provider is the default choice.</span></span> <span data-ttu-id="16698-134">L’entrée FRSD est validée pour les paramètres valides pour chaque propriété du fournisseur par défaut.</span><span class="sxs-lookup"><span data-stu-id="16698-134">Input FRSD is validated for valid settings for each property for the default provider.</span></span> <span data-ttu-id="16698-135">Ce tableau résume les différences de validation par rapport au fournisseur externe.</span><span class="sxs-lookup"><span data-stu-id="16698-135">This table summarizes the validation differences with respect to the external provider.</span></span>



| <span data-ttu-id="16698-136">Propriété</span><span class="sxs-lookup"><span data-stu-id="16698-136">Property</span></span>                                             | <span data-ttu-id="16698-137">Fournisseurs externes</span><span class="sxs-lookup"><span data-stu-id="16698-137">External providers</span></span>                                 |
|------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="16698-138">ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="16698-138">ReplicationProvider</span></span>                                  | <span data-ttu-id="16698-139">Identique au fournisseur par défaut</span><span class="sxs-lookup"><span data-stu-id="16698-139">Same as default provider</span></span>                           |
| <span data-ttu-id="16698-140">AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="16698-140">AuthenticationType</span></span>                                   | <span data-ttu-id="16698-141">Ignoré</span><span class="sxs-lookup"><span data-stu-id="16698-141">Ignored</span></span>                                            |
| <span data-ttu-id="16698-142">CertificateThumbPrint</span><span class="sxs-lookup"><span data-stu-id="16698-142">CertificateThumbPrint</span></span>                                | <span data-ttu-id="16698-143">Ignoré</span><span class="sxs-lookup"><span data-stu-id="16698-143">Ignored</span></span>                                            |
| <span data-ttu-id="16698-144">RootCertificateThumbPrint (RO)</span><span class="sxs-lookup"><span data-stu-id="16698-144">RootCertificateThumbPrint (RO)</span></span>                       | <span data-ttu-id="16698-145">Ignoré</span><span class="sxs-lookup"><span data-stu-id="16698-145">Ignored</span></span>                                            |
| <span data-ttu-id="16698-146">CompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="16698-146">CompressionEnabled</span></span>                                   | <span data-ttu-id="16698-147">Identique au fournisseur par défaut</span><span class="sxs-lookup"><span data-stu-id="16698-147">Same as default provider</span></span>                           |
| <span data-ttu-id="16698-148">BypassProxyServer</span><span class="sxs-lookup"><span data-stu-id="16698-148">BypassProxyServer</span></span>                                    | <span data-ttu-id="16698-149">Identique au fournisseur par défaut</span><span class="sxs-lookup"><span data-stu-id="16698-149">Same as default provider</span></span>                           |
| <span data-ttu-id="16698-150">RecoveryConnectionPoint</span><span class="sxs-lookup"><span data-stu-id="16698-150">RecoveryConnectionPoint</span></span>                              | <span data-ttu-id="16698-151">Ignoré \* (peut changer si le fournisseur a besoin)</span><span class="sxs-lookup"><span data-stu-id="16698-151">Ignored\* (may change if provider has requirement)</span></span> |
| <span data-ttu-id="16698-152">RecoveryHostSystem (RO)</span><span class="sxs-lookup"><span data-stu-id="16698-152">RecoveryHostSystem (RO)</span></span>                              | <span data-ttu-id="16698-153">Ignoré</span><span class="sxs-lookup"><span data-stu-id="16698-153">Ignored</span></span>                                            |
| <span data-ttu-id="16698-154">PrimaryConnectionPoint (RO)</span><span class="sxs-lookup"><span data-stu-id="16698-154">PrimaryConnectionPoint (RO)</span></span>                          | <span data-ttu-id="16698-155">Identique au fournisseur par défaut</span><span class="sxs-lookup"><span data-stu-id="16698-155">Same as default provider</span></span>                           |
| <span data-ttu-id="16698-156">PrimaryHostSystem (RO)</span><span class="sxs-lookup"><span data-stu-id="16698-156">PrimaryHostSystem (RO)</span></span>                               | <span data-ttu-id="16698-157">Identique au fournisseur par défaut</span><span class="sxs-lookup"><span data-stu-id="16698-157">Same as default provider</span></span>                           |
| <span data-ttu-id="16698-158">RecoveryServerPortNumber</span><span class="sxs-lookup"><span data-stu-id="16698-158">RecoveryServerPortNumber</span></span>                             | <span data-ttu-id="16698-159">Ignoré \* (peut changer si le fournisseur a besoin)</span><span class="sxs-lookup"><span data-stu-id="16698-159">Ignored\* (may change if provider has requirement)</span></span> |
| <span data-ttu-id="16698-160">ReplicateHostKvpItems</span><span class="sxs-lookup"><span data-stu-id="16698-160">ReplicateHostKvpItems</span></span>                                | <span data-ttu-id="16698-161">Ignoré</span><span class="sxs-lookup"><span data-stu-id="16698-161">Ignored</span></span>                                            |
| <span data-ttu-id="16698-162">ApplicationConsistentSnapshotInterval</span><span class="sxs-lookup"><span data-stu-id="16698-162">ApplicationConsistentSnapshotInterval</span></span>                | <span data-ttu-id="16698-163">Identique au fournisseur par défaut</span><span class="sxs-lookup"><span data-stu-id="16698-163">Same as default provider</span></span>                           |
| <span data-ttu-id="16698-164">RecoveryHistory</span><span class="sxs-lookup"><span data-stu-id="16698-164">RecoveryHistory</span></span>                                      | <span data-ttu-id="16698-165">Identique au fournisseur par défaut</span><span class="sxs-lookup"><span data-stu-id="16698-165">Same as default provider</span></span>                           |
| <span data-ttu-id="16698-166">IncludedDisks\[\]</span><span class="sxs-lookup"><span data-stu-id="16698-166">IncludedDisks\[\]</span></span>                                    | <span data-ttu-id="16698-167">Identique au fournisseur par défaut</span><span class="sxs-lookup"><span data-stu-id="16698-167">Same as default provider</span></span>                           |
| <span data-ttu-id="16698-168">AutoResynchronizeEnabled</span><span class="sxs-lookup"><span data-stu-id="16698-168">AutoResynchronizeEnabled</span></span>                             | <span data-ttu-id="16698-169">Identique au fournisseur par défaut</span><span class="sxs-lookup"><span data-stu-id="16698-169">Same as default provider</span></span>                           |
| <span data-ttu-id="16698-170">AutoResynchronizeIntervalStart</span><span class="sxs-lookup"><span data-stu-id="16698-170">AutoResynchronizeIntervalStart</span></span>                       | <span data-ttu-id="16698-171">Identique au fournisseur par défaut</span><span class="sxs-lookup"><span data-stu-id="16698-171">Same as default provider</span></span>                           |
| <span data-ttu-id="16698-172">AutoResynchronizeIntervalEnd</span><span class="sxs-lookup"><span data-stu-id="16698-172">AutoResynchronizeIntervalEnd</span></span>                         | <span data-ttu-id="16698-173">Identique au fournisseur par défaut</span><span class="sxs-lookup"><span data-stu-id="16698-173">Same as default provider</span></span>                           |
| <span data-ttu-id="16698-174">EnableWriteOrderPreservationAcrossDisks (déconseillée)</span><span class="sxs-lookup"><span data-stu-id="16698-174">EnableWriteOrderPreservationAcrossDisks (Deprecated)</span></span> | <span data-ttu-id="16698-175">Identique au fournisseur par défaut</span><span class="sxs-lookup"><span data-stu-id="16698-175">Same as default provider</span></span>                           |
| <span data-ttu-id="16698-176">ReplicationInterval</span><span class="sxs-lookup"><span data-stu-id="16698-176">ReplicationInterval</span></span>                                  | <span data-ttu-id="16698-177">Identique au fournisseur par défaut</span><span class="sxs-lookup"><span data-stu-id="16698-177">Same as default provider</span></span>                           |



 

## <a name="requirements"></a><span data-ttu-id="16698-178">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16698-178">Requirements</span></span>



| <span data-ttu-id="16698-179">Condition requise</span><span class="sxs-lookup"><span data-stu-id="16698-179">Requirement</span></span> | <span data-ttu-id="16698-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="16698-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16698-181">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="16698-181">Minimum supported client</span></span><br/> | <span data-ttu-id="16698-182">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="16698-182">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="16698-183">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="16698-183">Minimum supported server</span></span><br/> | <span data-ttu-id="16698-184">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="16698-184">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="16698-185">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="16698-185">Namespace</span></span><br/>                | <span data-ttu-id="16698-186">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="16698-186">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="16698-187">MOF</span><span class="sxs-lookup"><span data-stu-id="16698-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="16698-188"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="16698-188"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="16698-189">DLL</span><span class="sxs-lookup"><span data-stu-id="16698-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16698-190"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="16698-190"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="16698-191">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16698-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16698-192">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="16698-192">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

