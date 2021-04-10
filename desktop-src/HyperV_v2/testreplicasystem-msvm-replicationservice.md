---
description: Crée un réplica d’une machine virtuelle avec la capture instantanée spécifiée à des fins de test.
ms.assetid: 447f3c8f-8c57-4874-9466-91c6aea533bc
title: Méthode TestReplicaSystem de la classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.TestReplicaSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 029130e619aa36d0aa9b9c1c85a877fb26e1b22b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867953"
---
# <a name="testreplicasystem-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="42db3-103">Méthode TestReplicaSystem de la \_ classe ReplicationService MSVM</span><span class="sxs-lookup"><span data-stu-id="42db3-103">TestReplicaSystem method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="42db3-104">Crée un réplica d’une machine virtuelle avec la capture instantanée spécifiée à des fins de test.</span><span class="sxs-lookup"><span data-stu-id="42db3-104">Creates a new replica of a virtual machine with the specified snapshot for testing purposes.</span></span>

## <a name="syntax"></a><span data-ttu-id="42db3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="42db3-105">Syntax</span></span>


```mof
uint32 TestReplicaSystem(
  [in]  CIM_ComputerSystem           REF ComputerSystem,
  [in]  CIM_VirtualSystemSettingData REF SnapshotSettingData,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="42db3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="42db3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42db3-107">*ComputerSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="42db3-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42db3-108">Référence à une instance [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente l’ordinateur virtuel pour lequel la réplication doit être testée.</span><span class="sxs-lookup"><span data-stu-id="42db3-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication should be tested.</span></span>

</dd> <dt>

<span data-ttu-id="42db3-109">*SnapshotSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="42db3-109">*SnapshotSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42db3-110">Référence à une instance [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)) qui représente l’instantané utilisé pour créer le système de basculement de test.</span><span class="sxs-lookup"><span data-stu-id="42db3-110">A reference to a [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) instance that represents the snapshot used to create the test failover system.</span></span> <span data-ttu-id="42db3-111">Si ce paramètre a la **valeur null**, le basculement doit être effectué à partir du dernier point dans le temps.</span><span class="sxs-lookup"><span data-stu-id="42db3-111">If this parameter is **Null**, the failover is to be performed off the latest point in time.</span></span>

</dd> <dt>

<span data-ttu-id="42db3-112">*ResultingSystem* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="42db3-112">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42db3-113">Si une machine virtuelle est définie avec succès, reçoit une référence à une instance de [**la \_ classe CIM CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente la machine virtuelle de test nouvellement définie.</span><span class="sxs-lookup"><span data-stu-id="42db3-113">If a virtual machine is successfully defined, receives a reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the newly defined test virtual machine.</span></span> <span data-ttu-id="42db3-114">Quand ce système n’est plus nécessaire, détruisez-le en appelant la méthode [**DestroySystem**](destroysystem-msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="42db3-114">When this system is no longer needed, destroy it by calling the [**DestroySystem**](destroysystem-msvm-virtualsystemmanagementservice.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="42db3-115">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="42db3-115">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42db3-116">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="42db3-116">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42db3-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="42db3-117">Return value</span></span>

<span data-ttu-id="42db3-118">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="42db3-118">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="42db3-119">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="42db3-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="42db3-120">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="42db3-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="42db3-121">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="42db3-121">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="42db3-122">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="42db3-122">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="42db3-123">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="42db3-123">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="42db3-124">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="42db3-124">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="42db3-125">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="42db3-125">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="42db3-126">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="42db3-126">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="42db3-127">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="42db3-127">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="42db3-128">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="42db3-128">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="42db3-129">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="42db3-129">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="42db3-130">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="42db3-130">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="42db3-131">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="42db3-131">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="42db3-132">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="42db3-132">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="42db3-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="42db3-133">Requirements</span></span>



| <span data-ttu-id="42db3-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42db3-134">Requirement</span></span> | <span data-ttu-id="42db3-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="42db3-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42db3-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42db3-136">Minimum supported client</span></span><br/> | <span data-ttu-id="42db3-137">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42db3-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="42db3-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42db3-138">Minimum supported server</span></span><br/> | <span data-ttu-id="42db3-139">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42db3-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="42db3-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="42db3-140">Namespace</span></span><br/>                | <span data-ttu-id="42db3-141">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="42db3-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="42db3-142">MOF</span><span class="sxs-lookup"><span data-stu-id="42db3-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="42db3-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="42db3-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="42db3-144">DLL</span><span class="sxs-lookup"><span data-stu-id="42db3-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42db3-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="42db3-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="42db3-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42db3-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42db3-147">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="42db3-147">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

