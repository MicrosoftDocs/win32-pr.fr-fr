---
description: Réinitialise les statistiques de réplication associées à la relation de réplication spécifiée de l’ordinateur virtuel spécifié.
ms.assetid: 6E49A7C0-2F60-444E-964E-420470EE1538
title: 'Msvm_ReplicationService :: ResetReplicationStatisticsEx, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ResetReplicationStatisticsEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c1acb234660e71636b4a69a697b11385d65cf1ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866385"
---
# <a name="msvm_replicationserviceresetreplicationstatisticsex-method"></a><span data-ttu-id="e447e-103">MSVM \_ ReplicationService :: ResetReplicationStatisticsEx, méthode</span><span class="sxs-lookup"><span data-stu-id="e447e-103">Msvm\_ReplicationService::ResetReplicationStatisticsEx method</span></span>

<span data-ttu-id="e447e-104">Réinitialise les statistiques de réplication associées à la relation de réplication spécifiée de l’ordinateur virtuel spécifié.</span><span class="sxs-lookup"><span data-stu-id="e447e-104">Resets replication statistics that are associated with the specified replication relationship of the specified virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="e447e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e447e-105">Syntax</span></span>


```C++
uint32 ResetReplicationStatisticsEx(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a><span data-ttu-id="e447e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e447e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e447e-107">*ComputerSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e447e-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e447e-108">Référence à une instance [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente l’ordinateur virtuel prenant en charge les réplicas.</span><span class="sxs-lookup"><span data-stu-id="e447e-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the replica-enabled virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="e447e-109">*ReplicationRelationship* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e447e-109">*ReplicationRelationship* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e447e-110">Représentation sous forme de chaîne d’une instance incorporée de la classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) qui définit la relation de réplication pour laquelle réinitialiser les statistiques de réplication.</span><span class="sxs-lookup"><span data-stu-id="e447e-110">A string representation of an embedded instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that defines the replication relationship for which to reset the replication statistics.</span></span>

</dd> <dt>

<span data-ttu-id="e447e-111">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e447e-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e447e-112">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e447e-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span> <span data-ttu-id="e447e-113">Cette référence peut être **null** si la tâche est terminée.</span><span class="sxs-lookup"><span data-stu-id="e447e-113">This reference can be **NULL** if the task is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e447e-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e447e-114">Return value</span></span>

<span data-ttu-id="e447e-115">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e447e-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e447e-116">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="e447e-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e447e-117">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="e447e-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e447e-118">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="e447e-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e447e-119">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="e447e-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e447e-120">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="e447e-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e447e-121">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="e447e-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e447e-122">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="e447e-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e447e-123">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="e447e-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e447e-124">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="e447e-124">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e447e-125">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="e447e-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e447e-126">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="e447e-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e447e-127">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="e447e-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e447e-128">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="e447e-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="e447e-129">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="e447e-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e447e-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e447e-130">Requirements</span></span>



| <span data-ttu-id="e447e-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e447e-131">Requirement</span></span> | <span data-ttu-id="e447e-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="e447e-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e447e-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e447e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e447e-134">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e447e-134">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="e447e-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e447e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e447e-136">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e447e-136">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e447e-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e447e-137">Namespace</span></span><br/>                | <span data-ttu-id="e447e-138">\\\\\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="e447e-138">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="e447e-139">MOF</span><span class="sxs-lookup"><span data-stu-id="e447e-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e447e-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e447e-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e447e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="e447e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e447e-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e447e-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e447e-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e447e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e447e-144">**GetReplicationStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="e447e-144">**GetReplicationStatisticsEx**</span></span>](getreplicationstatisticsex-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="e447e-145">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="e447e-145">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

