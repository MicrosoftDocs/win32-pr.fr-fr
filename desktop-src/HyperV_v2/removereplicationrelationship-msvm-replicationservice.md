---
description: Supprime une relation de réplication d’ordinateur virtuel et agit sur la relation de réplication principale de la machine virtuelle.
ms.assetid: a9a20aa1-378d-4a2a-9ebc-9786ab2dfda7
title: Méthode RemoveReplicationRelationship de la classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.RemoveReplicationRelationship
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bb897ff72cd927390362f076114fc8757baa6c5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862930"
---
# <a name="removereplicationrelationship-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="5fd04-103">Méthode RemoveReplicationRelationship de la \_ classe ReplicationService MSVM</span><span class="sxs-lookup"><span data-stu-id="5fd04-103">RemoveReplicationRelationship method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="5fd04-104">Supprime une relation de réplication d’ordinateur virtuel et agit sur la relation de réplication principale de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="5fd04-104">Removes a virtual machine replication relationship and acts on the primary replication relationship of the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="5fd04-105">À partir de Windows 8.1, nous vous recommandons de ne pas utiliser **RemoveReplicationRelationship** plus pour supprimer une relation de réplication de machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="5fd04-105">Starting with Windows 8.1, we recommend not to use **RemoveReplicationRelationship** anymore to remove a virtual machine replication relationship.</span></span> <span data-ttu-id="5fd04-106">Utilisez plutôt [**RemoveReplicationRelationshipEx**](removereplicationrelationshipex-msvm-replicationservice.md).</span><span class="sxs-lookup"><span data-stu-id="5fd04-106">Instead, use [**RemoveReplicationRelationshipEx**](removereplicationrelationshipex-msvm-replicationservice.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="5fd04-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5fd04-107">Syntax</span></span>


```mof
uint32 RemoveReplicationRelationship(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="5fd04-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5fd04-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fd04-109">*ComputerSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5fd04-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fd04-110">Référence à une instance [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente l’ordinateur virtuel pour lequel la relation de réplication doit être supprimée.</span><span class="sxs-lookup"><span data-stu-id="5fd04-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication relationship should be removed.</span></span>

</dd> <dt>

<span data-ttu-id="5fd04-111">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5fd04-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5fd04-112">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5fd04-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fd04-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5fd04-113">Return value</span></span>

<span data-ttu-id="5fd04-114">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="5fd04-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="5fd04-115">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="5fd04-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5fd04-116">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="5fd04-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="5fd04-117">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="5fd04-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="5fd04-118">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="5fd04-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="5fd04-119">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="5fd04-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="5fd04-120">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="5fd04-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="5fd04-121">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="5fd04-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="5fd04-122">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="5fd04-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="5fd04-123">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="5fd04-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="5fd04-124">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="5fd04-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="5fd04-125">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="5fd04-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="5fd04-126">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="5fd04-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="5fd04-127">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="5fd04-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="5fd04-128">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="5fd04-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="5fd04-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5fd04-129">Requirements</span></span>



| <span data-ttu-id="5fd04-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5fd04-130">Requirement</span></span> | <span data-ttu-id="5fd04-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="5fd04-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fd04-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5fd04-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5fd04-133">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5fd04-133">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5fd04-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5fd04-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5fd04-135">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5fd04-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5fd04-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5fd04-136">Namespace</span></span><br/>                | <span data-ttu-id="5fd04-137">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="5fd04-137">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5fd04-138">MOF</span><span class="sxs-lookup"><span data-stu-id="5fd04-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5fd04-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5fd04-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5fd04-140">DLL</span><span class="sxs-lookup"><span data-stu-id="5fd04-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5fd04-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5fd04-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5fd04-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5fd04-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fd04-143">**CreateReplicationRelationship**</span><span class="sxs-lookup"><span data-stu-id="5fd04-143">**CreateReplicationRelationship**</span></span>](createreplicationrelationship-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="5fd04-144">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="5fd04-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

