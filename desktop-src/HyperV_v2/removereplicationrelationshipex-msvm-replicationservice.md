---
description: Supprime la relation de réplication d’ordinateur virtuel spécifiée.
ms.assetid: 0D5013CE-7BAE-4A99-ABF2-F1ECC644A1B2
title: 'Msvm_ReplicationService :: RemoveReplicationRelationshipEx, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.RemoveReplicationRelationshipEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c57ed7f9a88789d04a20de0fd199d460b47c1eb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516034"
---
# <a name="msvm_replicationserviceremovereplicationrelationshipex-method"></a><span data-ttu-id="54cf9-103">MSVM \_ ReplicationService :: RemoveReplicationRelationshipEx, méthode</span><span class="sxs-lookup"><span data-stu-id="54cf9-103">Msvm\_ReplicationService::RemoveReplicationRelationshipEx method</span></span>

<span data-ttu-id="54cf9-104">Supprime la relation de réplication d’ordinateur virtuel spécifiée.</span><span class="sxs-lookup"><span data-stu-id="54cf9-104">Removes the specified virtual machine replication relationship.</span></span>

## <a name="syntax"></a><span data-ttu-id="54cf9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="54cf9-105">Syntax</span></span>


```C++
uint32 RemoveReplicationRelationshipEx(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a><span data-ttu-id="54cf9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54cf9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54cf9-107">*ComputerSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="54cf9-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54cf9-108">Référence à une instance [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente l’ordinateur virtuel pour lequel supprimer la réplication.</span><span class="sxs-lookup"><span data-stu-id="54cf9-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to remove the replication.</span></span>

</dd> <dt>

<span data-ttu-id="54cf9-109">*ReplicationRelationship* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="54cf9-109">*ReplicationRelationship* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54cf9-110">Représentation sous forme de chaîne d’une instance incorporée de la classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) qui définit la relation de réplication à supprimer.</span><span class="sxs-lookup"><span data-stu-id="54cf9-110">A string representation of an embedded instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that defines the replication relationship to remove.</span></span>

</dd> <dt>

<span data-ttu-id="54cf9-111">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="54cf9-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54cf9-112">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="54cf9-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span> <span data-ttu-id="54cf9-113">Cette référence peut être **null** si la tâche est terminée.</span><span class="sxs-lookup"><span data-stu-id="54cf9-113">This reference can be **NULL** if the task is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54cf9-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="54cf9-114">Return value</span></span>

<span data-ttu-id="54cf9-115">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="54cf9-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="54cf9-116">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="54cf9-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="54cf9-117">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="54cf9-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="54cf9-118">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="54cf9-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="54cf9-119">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="54cf9-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="54cf9-120">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="54cf9-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="54cf9-121">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="54cf9-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="54cf9-122">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="54cf9-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="54cf9-123">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="54cf9-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="54cf9-124">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="54cf9-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="54cf9-125">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="54cf9-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="54cf9-126">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="54cf9-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="54cf9-127">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="54cf9-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="54cf9-128">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="54cf9-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="54cf9-129">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="54cf9-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="54cf9-130">Notes</span><span class="sxs-lookup"><span data-stu-id="54cf9-130">Remarks</span></span>

<span data-ttu-id="54cf9-131">Pour un ordinateur virtuel de réplication, la réplication principale ne peut pas être supprimée si la réplication étendue est activée.</span><span class="sxs-lookup"><span data-stu-id="54cf9-131">For a replica virtual machine, primary replication can't be removed if extended replication is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="54cf9-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="54cf9-132">Requirements</span></span>



| <span data-ttu-id="54cf9-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="54cf9-133">Requirement</span></span> | <span data-ttu-id="54cf9-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="54cf9-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54cf9-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54cf9-135">Minimum supported client</span></span><br/> | <span data-ttu-id="54cf9-136">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54cf9-136">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="54cf9-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54cf9-137">Minimum supported server</span></span><br/> | <span data-ttu-id="54cf9-138">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54cf9-138">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="54cf9-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="54cf9-139">Namespace</span></span><br/>                | <span data-ttu-id="54cf9-140">\\\\\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="54cf9-140">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="54cf9-141">MOF</span><span class="sxs-lookup"><span data-stu-id="54cf9-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="54cf9-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="54cf9-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="54cf9-143">DLL</span><span class="sxs-lookup"><span data-stu-id="54cf9-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54cf9-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="54cf9-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="54cf9-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54cf9-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54cf9-146">**CreateReplicationRelationship**</span><span class="sxs-lookup"><span data-stu-id="54cf9-146">**CreateReplicationRelationship**</span></span>](createreplicationrelationship-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="54cf9-147">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="54cf9-147">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

