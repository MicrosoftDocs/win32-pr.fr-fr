---
description: Démarre la réplication d’un ordinateur virtuel.
ms.assetid: 58e89329-1ad4-4473-856d-ebfd7a863fa8
title: Méthode StartReplication de la classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.StartReplication
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4702b5b73a989e2889bf1da9e4d284afdfe5e916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318241"
---
# <a name="startreplication-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="21943-103">Méthode StartReplication de la \_ classe ReplicationService MSVM</span><span class="sxs-lookup"><span data-stu-id="21943-103">StartReplication method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="21943-104">Démarre la réplication d’un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="21943-104">Starts the replication of a virtual machine.</span></span> <span data-ttu-id="21943-105">Lorsqu’un client appelle cette méthode pour un ordinateur virtuel de réplication, il démarre la réplication avec le réplica étendu.</span><span class="sxs-lookup"><span data-stu-id="21943-105">When a client calls this method for a replica virtual machine, it starts the replication with extended replica.</span></span>

## <a name="syntax"></a><span data-ttu-id="21943-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="21943-106">Syntax</span></span>


```mof
uint32 StartReplication(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  uint16                 InitialReplicationType,
  [in]  string                 InitialReplicationExportLocation,
  [in]  datetime               StartTime,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="21943-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="21943-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21943-108">*ComputerSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="21943-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21943-109">Référence à une instance [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente l’ordinateur virtuel pour lequel la réplication doit être démarrée.</span><span class="sxs-lookup"><span data-stu-id="21943-109">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication should be started.</span></span>

</dd> <dt>

<span data-ttu-id="21943-110">*InitialReplicationType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="21943-110">*InitialReplicationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21943-111">Type de transfert à utiliser pour effectuer la réplication initiale.</span><span class="sxs-lookup"><span data-stu-id="21943-111">The type of transfer to be used for performing the initial replication.</span></span>

<dt>

<span id="Network_Transfer"></span><span id="network_transfer"></span><span id="NETWORK_TRANSFER"></span>

<span data-ttu-id="21943-112"><span id="Network_Transfer"></span><span id="network_transfer"></span><span id="NETWORK_TRANSFER"></span>**Transfert réseau** (1)</span><span class="sxs-lookup"><span data-stu-id="21943-112"><span id="Network_Transfer"></span><span id="network_transfer"></span><span id="NETWORK_TRANSFER"></span>**Network Transfer** (1)</span></span>


</dt> <dd>

<span data-ttu-id="21943-113">Transfert réseau.</span><span class="sxs-lookup"><span data-stu-id="21943-113">Network transfer.</span></span>

</dd> <dt>

<span id="Export"></span><span id="export"></span><span id="EXPORT"></span>

<span data-ttu-id="21943-114"><span id="Export"></span><span id="export"></span><span id="EXPORT"></span>**Exporter** (2)</span><span class="sxs-lookup"><span data-stu-id="21943-114"><span id="Export"></span><span id="export"></span><span id="EXPORT"></span>**Export** (2)</span></span>


</dt> <dd>

<span data-ttu-id="21943-115">exportation.</span><span class="sxs-lookup"><span data-stu-id="21943-115">Export.</span></span>

</dd> <dt>

<span id="Seeded_Network_Transfer"></span><span id="seeded_network_transfer"></span><span id="SEEDED_NETWORK_TRANSFER"></span>

<span data-ttu-id="21943-116"><span id="Seeded_Network_Transfer"></span><span id="seeded_network_transfer"></span><span id="SEEDED_NETWORK_TRANSFER"></span>**Transfert réseau amorcé** (3)</span><span class="sxs-lookup"><span data-stu-id="21943-116"><span id="Seeded_Network_Transfer"></span><span id="seeded_network_transfer"></span><span id="SEEDED_NETWORK_TRANSFER"></span>**Seeded Network Transfer** (3)</span></span>


</dt> <dd>

<span data-ttu-id="21943-117">Transfert réseau amorcé.</span><span class="sxs-lookup"><span data-stu-id="21943-117">Seeded network transfer.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="21943-118">*InitialReplicationExportLocation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="21943-118">*InitialReplicationExportLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21943-119">Si *InitialReplicationType* a la valeur 2 (exporter), ce paramètre contient le chemin d’accès complet du répertoire dans lequel la réplication initiale doit être exportée.</span><span class="sxs-lookup"><span data-stu-id="21943-119">If *InitialReplicationType* is 2 (Export), this parameter contains the fully qualified path of the directory to which the initial replication is to be exported.</span></span> <span data-ttu-id="21943-120">Ce paramètre n’est pas utilisé pour d’autres valeurs de *InitialReplicationType* et peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="21943-120">This parameter is not used for other values of *InitialReplicationType*, and can be **Null**.</span></span> <span data-ttu-id="21943-121">Ce répertoire peut être réutilisé pour l’exportation de plusieurs réplications de machines virtuelles.</span><span class="sxs-lookup"><span data-stu-id="21943-121">This directory can be reused for exporting multiple virtual machine replication.</span></span> <span data-ttu-id="21943-122">Cette méthode place chaque réplication de machine virtuelle dans un sous-répertoire distinct sous ce chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="21943-122">This method places each virtual machine replication in a separate subdirectory under this path.</span></span>

</dd> <dt>

<span data-ttu-id="21943-123">*StartTime* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="21943-123">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21943-124">Heure de début planifiée pour la réplication initiale sur la connexion réseau au serveur de récupération.</span><span class="sxs-lookup"><span data-stu-id="21943-124">The scheduled start time for the initial replication over the network connection to recovery server.</span></span> <span data-ttu-id="21943-125">Ce paramètre est ignoré lorsque *InitialReplicationType* est 2 (exportation).</span><span class="sxs-lookup"><span data-stu-id="21943-125">This parameter is ignored when *InitialReplicationType* is 2 (Export).</span></span> <span data-ttu-id="21943-126">Si ce paramètre a la **valeur null**, la réplication initiale démarre immédiatement.</span><span class="sxs-lookup"><span data-stu-id="21943-126">If this parameter is **Null**, the initial replication starts immediately.</span></span>

</dd> <dt>

<span data-ttu-id="21943-127">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="21943-127">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21943-128">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="21943-128">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21943-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="21943-129">Return value</span></span>

<span data-ttu-id="21943-130">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="21943-130">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="21943-131">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="21943-131">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="21943-132">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="21943-132">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="21943-133">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="21943-133">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="21943-134">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="21943-134">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="21943-135">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="21943-135">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="21943-136">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="21943-136">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="21943-137">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="21943-137">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="21943-138">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="21943-138">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="21943-139">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="21943-139">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="21943-140">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="21943-140">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="21943-141">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="21943-141">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="21943-142">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="21943-142">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="21943-143">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="21943-143">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="21943-144">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="21943-144">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="21943-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21943-145">Requirements</span></span>



| <span data-ttu-id="21943-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21943-146">Requirement</span></span> | <span data-ttu-id="21943-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="21943-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21943-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21943-148">Minimum supported client</span></span><br/> | <span data-ttu-id="21943-149">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21943-149">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="21943-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21943-150">Minimum supported server</span></span><br/> | <span data-ttu-id="21943-151">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21943-151">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="21943-152">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="21943-152">Namespace</span></span><br/>                | <span data-ttu-id="21943-153">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="21943-153">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="21943-154">MOF</span><span class="sxs-lookup"><span data-stu-id="21943-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="21943-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="21943-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="21943-156">DLL</span><span class="sxs-lookup"><span data-stu-id="21943-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21943-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="21943-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="21943-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21943-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21943-159">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="21943-159">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

