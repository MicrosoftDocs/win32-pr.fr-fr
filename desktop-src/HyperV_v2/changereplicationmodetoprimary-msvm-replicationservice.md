---
description: Modifie la relation de réplication étendue en relation principale pour un ordinateur virtuel de réplication. L’ordinateur virtuel de réplication doit être dans un état de basculement validé.
ms.assetid: B593A155-B5E6-44E5-8835-09DEB1FF868E
title: 'Msvm_ReplicationService :: ChangeReplicationModeToPrimary, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ChangeReplicationModeToPrimary
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0a18b3c9f1003ff7b263f5c6b7cc89abedccfd1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514153"
---
# <a name="msvm_replicationservicechangereplicationmodetoprimary-method"></a><span data-ttu-id="c218d-104">MSVM \_ ReplicationService :: ChangeReplicationModeToPrimary, méthode</span><span class="sxs-lookup"><span data-stu-id="c218d-104">Msvm\_ReplicationService::ChangeReplicationModeToPrimary method</span></span>

<span data-ttu-id="c218d-105">Modifie la relation de réplication étendue en relation principale pour un ordinateur virtuel de réplication.</span><span class="sxs-lookup"><span data-stu-id="c218d-105">Changes the extended replication relationship to the primary relationship for a replica virtual machine.</span></span> <span data-ttu-id="c218d-106">L’ordinateur virtuel de réplication doit être dans un état de basculement validé.</span><span class="sxs-lookup"><span data-stu-id="c218d-106">The replica virtual machine must be in a failover committed state.</span></span>

## <a name="syntax"></a><span data-ttu-id="c218d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c218d-107">Syntax</span></span>


```C++
uint32 ChangeReplicationModeToPrimary(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a><span data-ttu-id="c218d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c218d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c218d-109">*ComputerSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c218d-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c218d-110">Référence à une instance [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente l’ordinateur virtuel pour lequel cette méthode modifie la relation de réplication étendue en relation principale.</span><span class="sxs-lookup"><span data-stu-id="c218d-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which this method changes the extended replication relationship to the primary relationship.</span></span>

</dd> <dt>

<span data-ttu-id="c218d-111">*ReplicationRelationship* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c218d-111">*ReplicationRelationship* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c218d-112">Représentation sous forme de chaîne d’une instance incorporée de la classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) qui définit la relation de réplication étendue que cette méthode change pour la relation principale.</span><span class="sxs-lookup"><span data-stu-id="c218d-112">A string representation of an embedded instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that defines the extended replication relationship that this method changes to the primary relationship.</span></span>

</dd> <dt>

<span data-ttu-id="c218d-113">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c218d-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c218d-114">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c218d-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span> <span data-ttu-id="c218d-115">Cette référence peut être **null** si la tâche est terminée.</span><span class="sxs-lookup"><span data-stu-id="c218d-115">This reference can be **NULL** if the task is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c218d-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c218d-116">Return value</span></span>

<span data-ttu-id="c218d-117">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c218d-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="c218d-118">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="c218d-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c218d-119">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="c218d-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c218d-120">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="c218d-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="c218d-121">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="c218d-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="c218d-122">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="c218d-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="c218d-123">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="c218d-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="c218d-124">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="c218d-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="c218d-125">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="c218d-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="c218d-126">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="c218d-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="c218d-127">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="c218d-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="c218d-128">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="c218d-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="c218d-129">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="c218d-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="c218d-130">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="c218d-130">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="c218d-131">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="c218d-131">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c218d-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c218d-132">Requirements</span></span>



| <span data-ttu-id="c218d-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c218d-133">Requirement</span></span> | <span data-ttu-id="c218d-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="c218d-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c218d-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c218d-135">Minimum supported client</span></span><br/> | <span data-ttu-id="c218d-136">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c218d-136">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="c218d-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c218d-137">Minimum supported server</span></span><br/> | <span data-ttu-id="c218d-138">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c218d-138">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c218d-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c218d-139">Namespace</span></span><br/>                | <span data-ttu-id="c218d-140">\\\\\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="c218d-140">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="c218d-141">MOF</span><span class="sxs-lookup"><span data-stu-id="c218d-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c218d-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c218d-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c218d-143">DLL</span><span class="sxs-lookup"><span data-stu-id="c218d-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c218d-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c218d-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c218d-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c218d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c218d-146">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="c218d-146">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

