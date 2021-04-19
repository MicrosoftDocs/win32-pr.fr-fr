---
description: Valide l’instantané de récupération utilisé par la méthode InitiateFailover pour un basculement.
ms.assetid: 05c27211-adc7-400a-83e2-81792ae7577f
title: Méthode CommitFailover de la classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.CommitFailover
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 04687ea29f39645c2407de44faf6bba6ecc75832
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536679"
---
# <a name="commitfailover-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="685ab-103">Méthode CommitFailover de la \_ classe ReplicationService MSVM</span><span class="sxs-lookup"><span data-stu-id="685ab-103">CommitFailover method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="685ab-104">Valide l’instantané de récupération utilisé par la méthode [**InitiateFailover**](initiatefailover-msvm-replicationservice.md) pour un basculement.</span><span class="sxs-lookup"><span data-stu-id="685ab-104">Commits the recovery snapshot that the [**InitiateFailover**](initiatefailover-msvm-replicationservice.md) method has used for a failover.</span></span>

<span data-ttu-id="685ab-105">Cette méthode aplatit les points de récupération sur l’ordinateur virtuel de récupération en appliquant l’instantané de récupération.</span><span class="sxs-lookup"><span data-stu-id="685ab-105">This method flattens the recovery points on the recovery virtual machine by applying the recovery snapshot.</span></span> <span data-ttu-id="685ab-106">Une fois cette opération effectuée, l’opération de basculement ne peut pas être annulée.</span><span class="sxs-lookup"><span data-stu-id="685ab-106">After this is done, the failover operation cannot be canceled.</span></span> <span data-ttu-id="685ab-107">Les utilisateurs effectuent généralement cette opération lorsque le point de réplication utilisé pour le basculement est satisfaisant et que l’ordinateur virtuel de récupération peut changer le rôle en principal.</span><span class="sxs-lookup"><span data-stu-id="685ab-107">Users will typically perform this when the replication point used for failover is satisfactory and the recovery virtual machine can change role to be primary.</span></span>

## <a name="syntax"></a><span data-ttu-id="685ab-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="685ab-108">Syntax</span></span>


```mof
uint32 CommitFailover(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="685ab-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="685ab-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="685ab-110">*ComputerSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="685ab-110">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="685ab-111">Référence à une instance [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente l’ordinateur virtuel pour lequel valider le basculement.</span><span class="sxs-lookup"><span data-stu-id="685ab-111">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to commit the failover.</span></span>

</dd> <dt>

<span data-ttu-id="685ab-112">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="685ab-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="685ab-113">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="685ab-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="685ab-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="685ab-114">Return value</span></span>

<span data-ttu-id="685ab-115">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="685ab-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="685ab-116">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="685ab-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="685ab-117">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="685ab-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="685ab-118">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="685ab-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="685ab-119">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="685ab-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="685ab-120">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="685ab-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="685ab-121">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="685ab-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="685ab-122">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="685ab-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="685ab-123">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="685ab-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="685ab-124">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="685ab-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="685ab-125">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="685ab-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="685ab-126">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="685ab-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="685ab-127">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="685ab-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="685ab-128">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="685ab-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="685ab-129">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="685ab-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="685ab-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="685ab-130">Requirements</span></span>



| <span data-ttu-id="685ab-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="685ab-131">Requirement</span></span> | <span data-ttu-id="685ab-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="685ab-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="685ab-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="685ab-133">Minimum supported client</span></span><br/> | <span data-ttu-id="685ab-134">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="685ab-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="685ab-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="685ab-135">Minimum supported server</span></span><br/> | <span data-ttu-id="685ab-136">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="685ab-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="685ab-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="685ab-137">Namespace</span></span><br/>                | <span data-ttu-id="685ab-138">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="685ab-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="685ab-139">MOF</span><span class="sxs-lookup"><span data-stu-id="685ab-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="685ab-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="685ab-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="685ab-141">DLL</span><span class="sxs-lookup"><span data-stu-id="685ab-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="685ab-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="685ab-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="685ab-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="685ab-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="685ab-144">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="685ab-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

