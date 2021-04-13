---
description: Effectue une opération de resynchronisation sur l’ordinateur virtuel spécifié.
ms.assetid: a3d06780-f43b-45c4-a186-a3544f9c7963
title: Resynchroniser la méthode de la classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.Resynchronize
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: dcd4865d110843de27f0a242b31253310439e1c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319518"
---
# <a name="resynchronize-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="2ae68-103">Resynchroniser la méthode de la \_ classe MSVM ReplicationService</span><span class="sxs-lookup"><span data-stu-id="2ae68-103">Resynchronize method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="2ae68-104">Effectue une opération de resynchronisation sur l’ordinateur virtuel spécifié.</span><span class="sxs-lookup"><span data-stu-id="2ae68-104">Performs a resynchronization operation on the specified virtual machine.</span></span> <span data-ttu-id="2ae68-105">Lorsqu’un client appelle cette méthode pour un ordinateur virtuel de réplication, il se resynchronise avec le réplica étendu.</span><span class="sxs-lookup"><span data-stu-id="2ae68-105">When a client calls this method for a replica virtual machine, it resynchronizes with extended replica.</span></span>

<span data-ttu-id="2ae68-106">Cette méthode compare les disques de réplication activés sur les ordinateurs virtuels principaux et de récupération et résout les problèmes d’intégrité des données de réplication en répliquant les différents blocs du serveur principal vers la récupération.</span><span class="sxs-lookup"><span data-stu-id="2ae68-106">This methods compares the replication enabled disks on the primary and recovery virtual machines, and fixes any replication data integrity issues by replicating the different blocks from the primary to the recovery.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ae68-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2ae68-107">Syntax</span></span>


```mof
uint32 Resynchronize(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  datetime               StartTime,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="2ae68-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2ae68-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ae68-109">*ComputerSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ae68-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ae68-110">Référence à une instance [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente l’ordinateur virtuel à resynchroniser.</span><span class="sxs-lookup"><span data-stu-id="2ae68-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine to be resynchronized.</span></span>

</dd> <dt>

<span data-ttu-id="2ae68-111">*StartTime* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ae68-111">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ae68-112">Heure de début planifiée pour le début de l’opération de resynchronisation.</span><span class="sxs-lookup"><span data-stu-id="2ae68-112">The scheduled start time for the resynchronization operation to begin.</span></span> <span data-ttu-id="2ae68-113">Si ce paramètre a la **valeur null**, l’opération de resynchronisation démarre immédiatement.</span><span class="sxs-lookup"><span data-stu-id="2ae68-113">If this parameter is **Null**, the resynchronization operation starts immediately.</span></span>

</dd> <dt>

<span data-ttu-id="2ae68-114">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2ae68-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ae68-115">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2ae68-115">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ae68-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2ae68-116">Return value</span></span>

<span data-ttu-id="2ae68-117">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="2ae68-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="2ae68-118">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="2ae68-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2ae68-119">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="2ae68-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2ae68-120">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="2ae68-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="2ae68-121">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="2ae68-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="2ae68-122">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="2ae68-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="2ae68-123">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="2ae68-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="2ae68-124">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="2ae68-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="2ae68-125">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="2ae68-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="2ae68-126">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="2ae68-126">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="2ae68-127">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="2ae68-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="2ae68-128">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="2ae68-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="2ae68-129">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="2ae68-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="2ae68-130">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="2ae68-130">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="2ae68-131">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="2ae68-131">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2ae68-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2ae68-132">Requirements</span></span>



| <span data-ttu-id="2ae68-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2ae68-133">Requirement</span></span> | <span data-ttu-id="2ae68-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ae68-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ae68-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ae68-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2ae68-136">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2ae68-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2ae68-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ae68-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2ae68-138">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2ae68-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2ae68-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2ae68-139">Namespace</span></span><br/>                | <span data-ttu-id="2ae68-140">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="2ae68-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2ae68-141">MOF</span><span class="sxs-lookup"><span data-stu-id="2ae68-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2ae68-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2ae68-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2ae68-143">DLL</span><span class="sxs-lookup"><span data-stu-id="2ae68-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ae68-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2ae68-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2ae68-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ae68-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ae68-146">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="2ae68-146">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

