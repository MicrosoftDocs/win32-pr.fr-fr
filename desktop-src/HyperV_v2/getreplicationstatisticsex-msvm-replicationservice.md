---
description: Récupère les statistiques de réplication associées à la relation de réplication spécifiée de l’ordinateur virtuel.
ms.assetid: AB46894A-CBED-40DF-86B9-B578603B0341
title: 'Msvm_ReplicationService :: GetReplicationStatisticsEx, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.GetReplicationStatisticsEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7fdb60addc94094082fe83e70af06a2f5ae11f06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519328"
---
# <a name="msvm_replicationservicegetreplicationstatisticsex-method"></a><span data-ttu-id="60f52-103">MSVM \_ ReplicationService :: GetReplicationStatisticsEx, méthode</span><span class="sxs-lookup"><span data-stu-id="60f52-103">Msvm\_ReplicationService::GetReplicationStatisticsEx method</span></span>

<span data-ttu-id="60f52-104">Récupère les statistiques de réplication associées à la relation de réplication spécifiée de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="60f52-104">Retrieves the replication statistics that are associated with the specified replication relationship of the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="60f52-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60f52-105">Syntax</span></span>


```C++
uint32 GetReplicationStatisticsEx(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] string                 ReplicationStatistics[],
  [out] string                 ReplicationHealthIssues[],
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a><span data-ttu-id="60f52-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="60f52-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60f52-107">*ComputerSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="60f52-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60f52-108">Référence à une instance [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente l’ordinateur virtuel pour lequel les statistiques de réplication doivent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="60f52-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to retrieve the replication statistics.</span></span>

</dd> <dt>

<span data-ttu-id="60f52-109">*ReplicationRelationship* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="60f52-109">*ReplicationRelationship* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60f52-110">Représentation sous forme de chaîne d’une instance incorporée de la classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) qui définit la relation de réplication dont les statistiques de réplication doivent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="60f52-110">A string representation of an embedded instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that defines the replication relationship for which to retrieve the replication statistics.</span></span>

</dd> <dt>

<span data-ttu-id="60f52-111">*ReplicationStatistics* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="60f52-111">*ReplicationStatistics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60f52-112">En cas de réussite, reçoit une instance incorporée de la classe [**MSVM \_ ReplicationStatistics**](msvm-replicationstatistics.md) qui contient les statistiques de réplication pour la relation de réplication demandée.</span><span class="sxs-lookup"><span data-stu-id="60f52-112">If successful, receives an embedded instance of the [**Msvm\_ReplicationStatistics**](msvm-replicationstatistics.md) class that contains the replication statistics for the requested replication relationship.</span></span>

</dd> <dt>

<span data-ttu-id="60f52-113">*ReplicationHealthIssues* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="60f52-113">*ReplicationHealthIssues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60f52-114">En cas de réussite, reçoit un tableau d’instances incorporées de la classe d' [**\_ erreur MSVM**](msvm-error.md) qui indiquent les avertissements ou erreurs de réplication pour la machine virtuelle demandée.</span><span class="sxs-lookup"><span data-stu-id="60f52-114">If successful, receives an array of embedded instances of the [**Msvm\_Error**](msvm-error.md) class that indicate any replication warnings or errors for the requested virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="60f52-115">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="60f52-115">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60f52-116">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="60f52-116">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span> <span data-ttu-id="60f52-117">Cette référence peut être **null** si la tâche est terminée.</span><span class="sxs-lookup"><span data-stu-id="60f52-117">This reference can be **NULL** if the task is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60f52-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="60f52-118">Return value</span></span>

<span data-ttu-id="60f52-119">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="60f52-119">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="60f52-120">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="60f52-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="60f52-121">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="60f52-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="60f52-122">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="60f52-122">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="60f52-123">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="60f52-123">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="60f52-124">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="60f52-124">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="60f52-125">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="60f52-125">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="60f52-126">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="60f52-126">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="60f52-127">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="60f52-127">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="60f52-128">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="60f52-128">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="60f52-129">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="60f52-129">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="60f52-130">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="60f52-130">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="60f52-131">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="60f52-131">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="60f52-132">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="60f52-132">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="60f52-133">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="60f52-133">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="60f52-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60f52-134">Requirements</span></span>



| <span data-ttu-id="60f52-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60f52-135">Requirement</span></span> | <span data-ttu-id="60f52-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="60f52-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60f52-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60f52-137">Minimum supported client</span></span><br/> | <span data-ttu-id="60f52-138">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="60f52-138">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="60f52-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60f52-139">Minimum supported server</span></span><br/> | <span data-ttu-id="60f52-140">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="60f52-140">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="60f52-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="60f52-141">Namespace</span></span><br/>                | <span data-ttu-id="60f52-142">\\\\\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="60f52-142">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="60f52-143">MOF</span><span class="sxs-lookup"><span data-stu-id="60f52-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60f52-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="60f52-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="60f52-145">DLL</span><span class="sxs-lookup"><span data-stu-id="60f52-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60f52-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="60f52-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="60f52-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60f52-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60f52-148">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="60f52-148">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="60f52-149">**ResetReplicationStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="60f52-149">**ResetReplicationStatisticsEx**</span></span>](resetreplicationstatisticsex-msvm-replicationservice.md)
</dt> </dl>

 

