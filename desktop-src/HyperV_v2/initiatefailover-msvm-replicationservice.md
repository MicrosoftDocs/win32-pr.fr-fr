---
description: Lance un basculement d’une machine virtuelle vers une image de point de réplication standard ou d’application.
ms.assetid: cd7e9398-c234-4637-906d-69b46ebf3f51
title: Méthode InitiateFailover de la classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.InitiateFailover
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0f05a9b126028b741782d253ac12b79f9f88e1e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318793"
---
# <a name="initiatefailover-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="fd6cc-103">Méthode InitiateFailover de la \_ classe ReplicationService MSVM</span><span class="sxs-lookup"><span data-stu-id="fd6cc-103">InitiateFailover method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="fd6cc-104">Lance un basculement d’une machine virtuelle vers une image de point de réplication standard ou d’application.</span><span class="sxs-lookup"><span data-stu-id="fd6cc-104">Initiates a failover for a virtual machine to an application or standard replication point image.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd6cc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd6cc-105">Syntax</span></span>


```mof
uint32 InitiateFailover(
  [in]  CIM_ComputerSystem           REF ComputerSystem,
  [in]  CIM_VirtualSystemSettingData REF SnapshotSettingData,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="fd6cc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd6cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd6cc-107">*ComputerSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fd6cc-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6cc-108">Référence à une instance [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente l’ordinateur virtuel pour lequel un basculement doit être initié.</span><span class="sxs-lookup"><span data-stu-id="fd6cc-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to initiate a failover.</span></span>

</dd> <dt>

<span data-ttu-id="fd6cc-109">*SnapshotSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fd6cc-109">*SnapshotSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6cc-110">Référence à une instance [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)) qui représente l’instantané utilisé pour le basculement.</span><span class="sxs-lookup"><span data-stu-id="fd6cc-110">A reference to a [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) instance that represents the snapshot used for the failover.</span></span> <span data-ttu-id="fd6cc-111">Si ce paramètre a la **valeur null**, le basculement doit être effectué au dernier point dans le temps.</span><span class="sxs-lookup"><span data-stu-id="fd6cc-111">If this parameter is **Null**, the failover is to be performed to the latest point in time.</span></span>

</dd> <dt>

<span data-ttu-id="fd6cc-112">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fd6cc-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6cc-113">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fd6cc-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd6cc-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fd6cc-114">Return value</span></span>

<span data-ttu-id="fd6cc-115">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="fd6cc-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="fd6cc-116">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="fd6cc-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fd6cc-117">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="fd6cc-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="fd6cc-118">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="fd6cc-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="fd6cc-119">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="fd6cc-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="fd6cc-120">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="fd6cc-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="fd6cc-121">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="fd6cc-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="fd6cc-122">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="fd6cc-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="fd6cc-123">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="fd6cc-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="fd6cc-124">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="fd6cc-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="fd6cc-125">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="fd6cc-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="fd6cc-126">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="fd6cc-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="fd6cc-127">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="fd6cc-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="fd6cc-128">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="fd6cc-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="fd6cc-129">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="fd6cc-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="fd6cc-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd6cc-130">Requirements</span></span>



| <span data-ttu-id="fd6cc-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd6cc-131">Requirement</span></span> | <span data-ttu-id="fd6cc-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd6cc-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd6cc-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd6cc-133">Minimum supported client</span></span><br/> | <span data-ttu-id="fd6cc-134">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd6cc-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fd6cc-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd6cc-135">Minimum supported server</span></span><br/> | <span data-ttu-id="fd6cc-136">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd6cc-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fd6cc-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fd6cc-137">Namespace</span></span><br/>                | <span data-ttu-id="fd6cc-138">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="fd6cc-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fd6cc-139">MOF</span><span class="sxs-lookup"><span data-stu-id="fd6cc-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd6cc-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd6cc-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd6cc-141">DLL</span><span class="sxs-lookup"><span data-stu-id="fd6cc-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd6cc-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fd6cc-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fd6cc-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd6cc-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd6cc-144">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="fd6cc-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="fd6cc-145">**RevertFailover**</span><span class="sxs-lookup"><span data-stu-id="fd6cc-145">**RevertFailover**</span></span>](revertfailover-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="fd6cc-146">**SetFailoverNetworkAdapterSettings**</span><span class="sxs-lookup"><span data-stu-id="fd6cc-146">**SetFailoverNetworkAdapterSettings**</span></span>](setfailovernetworkadaptersettings-msvm-replicationservice.md)
</dt> </dl>

 

