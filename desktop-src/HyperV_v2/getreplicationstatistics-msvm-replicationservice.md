---
description: Récupère les statistiques de réplication d’un ordinateur virtuel et agit sur la relation de réplication principale de la machine virtuelle.
ms.assetid: 24f3f572-fa85-4680-be77-7e835e6471c5
title: Méthode GetReplicationStatistics de la classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.GetReplicationStatistics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9dff711830ccdb805c362961671dff28f5bf0b73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515680"
---
# <a name="getreplicationstatistics-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="7d75b-103">Méthode GetReplicationStatistics de la \_ classe ReplicationService MSVM</span><span class="sxs-lookup"><span data-stu-id="7d75b-103">GetReplicationStatistics method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="7d75b-104">Récupère les statistiques de réplication d’un ordinateur virtuel et agit sur la relation de réplication principale de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="7d75b-104">Retrieves replication statistics for a virtual machine and acts on the primary replication relationship of the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="7d75b-105">À partir de Windows 8.1, nous vous recommandons de ne pas utiliser **GetReplicationStatistics** pour récupérer les statistiques de réplication.</span><span class="sxs-lookup"><span data-stu-id="7d75b-105">Starting with Windows 8.1, we recommend not to use **GetReplicationStatistics** anymore to retrieve replication statistics.</span></span> <span data-ttu-id="7d75b-106">Utilisez plutôt [**GetReplicationStatisticsEx**](getreplicationstatisticsex-msvm-replicationservice.md).</span><span class="sxs-lookup"><span data-stu-id="7d75b-106">Instead, use [**GetReplicationStatisticsEx**](getreplicationstatisticsex-msvm-replicationservice.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="7d75b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7d75b-107">Syntax</span></span>


```mof
uint32 GetReplicationStatistics(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] string                 ReplicationStatistics[],
  [out] string                 ReplicationHealthIssues[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="7d75b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7d75b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d75b-109">*ComputerSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7d75b-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d75b-110">Référence à une instance [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente l’ordinateur virtuel pour lequel les statistiques de réplication doivent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="7d75b-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to retrieve the replication statistics.</span></span>

</dd> <dt>

<span data-ttu-id="7d75b-111">*ReplicationStatistics* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7d75b-111">*ReplicationStatistics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d75b-112">En cas de réussite, reçoit une instance incorporée de la classe [**MSVM \_ ReplicationStatistics**](msvm-replicationstatistics.md) qui contient les statistiques de réplication pour la machine virtuelle demandée.</span><span class="sxs-lookup"><span data-stu-id="7d75b-112">If successful, receives an embedded instance of the [**Msvm\_ReplicationStatistics**](msvm-replicationstatistics.md) class that contains the replication statistics for the requested virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="7d75b-113">*ReplicationHealthIssues* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7d75b-113">*ReplicationHealthIssues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d75b-114">En cas de réussite, reçoit un tableau d’instances incorporées de la classe d' [**\_ erreur MSVM**](msvm-error.md) qui indiquent les avertissements ou erreurs de réplication pour la machine virtuelle demandée.</span><span class="sxs-lookup"><span data-stu-id="7d75b-114">If successful, receives an array of embedded instances of the [**Msvm\_Error**](msvm-error.md) class that indicate any replication warnings or errors for the requested virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="7d75b-115">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7d75b-115">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d75b-116">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7d75b-116">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d75b-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7d75b-117">Return value</span></span>

<span data-ttu-id="7d75b-118">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="7d75b-118">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="7d75b-119">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="7d75b-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7d75b-120">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="7d75b-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="7d75b-121">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="7d75b-121">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="7d75b-122">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="7d75b-122">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="7d75b-123">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="7d75b-123">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="7d75b-124">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="7d75b-124">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="7d75b-125">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="7d75b-125">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="7d75b-126">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="7d75b-126">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="7d75b-127">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="7d75b-127">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="7d75b-128">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="7d75b-128">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="7d75b-129">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="7d75b-129">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="7d75b-130">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="7d75b-130">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="7d75b-131">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="7d75b-131">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="7d75b-132">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="7d75b-132">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="7d75b-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7d75b-133">Requirements</span></span>



| <span data-ttu-id="7d75b-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7d75b-134">Requirement</span></span> | <span data-ttu-id="7d75b-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="7d75b-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d75b-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d75b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7d75b-137">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7d75b-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7d75b-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d75b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7d75b-139">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7d75b-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7d75b-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7d75b-140">Namespace</span></span><br/>                | <span data-ttu-id="7d75b-141">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="7d75b-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7d75b-142">MOF</span><span class="sxs-lookup"><span data-stu-id="7d75b-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7d75b-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7d75b-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7d75b-144">DLL</span><span class="sxs-lookup"><span data-stu-id="7d75b-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d75b-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7d75b-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7d75b-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d75b-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d75b-147">**ResetReplicationStatistics**</span><span class="sxs-lookup"><span data-stu-id="7d75b-147">**ResetReplicationStatistics**</span></span>](resetreplicationstatistics-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="7d75b-148">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="7d75b-148">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

