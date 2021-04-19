---
description: Restaure le basculement en cours pour un ordinateur virtuel en ignorant le disque de basculement actuel.
ms.assetid: 99d3a3d3-49e4-4410-b979-47b62ebc6aa6
title: Méthode RevertFailover de la classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.RevertFailover
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: db20abf34fdad2e0eba499fd1b4cc390bf93b754
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532320"
---
# <a name="revertfailover-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="82078-103">Méthode RevertFailover de la \_ classe ReplicationService MSVM</span><span class="sxs-lookup"><span data-stu-id="82078-103">RevertFailover method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="82078-104">Restaure le basculement en cours pour un ordinateur virtuel en ignorant le disque de basculement actuel.</span><span class="sxs-lookup"><span data-stu-id="82078-104">Reverts the current failover for a virtual machine by discarding the current failover disk.</span></span> <span data-ttu-id="82078-105">Après cette opération, [**InitiateFailover**](initiatefailover-msvm-replicationservice.md) peut être appelé à nouveau.</span><span class="sxs-lookup"><span data-stu-id="82078-105">After this operation, [**InitiateFailover**](initiatefailover-msvm-replicationservice.md) can be called again.</span></span>

## <a name="syntax"></a><span data-ttu-id="82078-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82078-106">Syntax</span></span>


```mof
uint32 RevertFailover(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="82078-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="82078-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82078-108">*ComputerSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="82078-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82078-109">Référence à une instance [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente l’ordinateur virtuel pour lequel annuler le basculement.</span><span class="sxs-lookup"><span data-stu-id="82078-109">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to revert the failover.</span></span>

</dd> <dt>

<span data-ttu-id="82078-110">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="82078-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82078-111">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="82078-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82078-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="82078-112">Return value</span></span>

<span data-ttu-id="82078-113">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="82078-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="82078-114">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="82078-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="82078-115">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="82078-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="82078-116">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="82078-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="82078-117">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="82078-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="82078-118">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="82078-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="82078-119">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="82078-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="82078-120">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="82078-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="82078-121">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="82078-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="82078-122">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="82078-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="82078-123">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="82078-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="82078-124">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="82078-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="82078-125">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="82078-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="82078-126">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="82078-126">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="82078-127">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="82078-127">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="82078-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="82078-128">Requirements</span></span>



| <span data-ttu-id="82078-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="82078-129">Requirement</span></span> | <span data-ttu-id="82078-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="82078-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82078-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="82078-131">Minimum supported client</span></span><br/> | <span data-ttu-id="82078-132">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="82078-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="82078-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="82078-133">Minimum supported server</span></span><br/> | <span data-ttu-id="82078-134">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="82078-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="82078-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="82078-135">Namespace</span></span><br/>                | <span data-ttu-id="82078-136">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="82078-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="82078-137">MOF</span><span class="sxs-lookup"><span data-stu-id="82078-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="82078-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="82078-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="82078-139">DLL</span><span class="sxs-lookup"><span data-stu-id="82078-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82078-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="82078-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="82078-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82078-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82078-142">**InitiateFailover**</span><span class="sxs-lookup"><span data-stu-id="82078-142">**InitiateFailover**</span></span>](initiatefailover-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="82078-143">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="82078-143">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="82078-144">**SetFailoverNetworkAdapterSettings**</span><span class="sxs-lookup"><span data-stu-id="82078-144">**SetFailoverNetworkAdapterSettings**</span></span>](setfailovernetworkadaptersettings-msvm-replicationservice.md)
</dt> </dl>

 

