---
description: Importe la réplication initiale d’un ordinateur virtuel.
ms.assetid: 151211fe-e58e-4fd4-87cd-cdb2ad55c0b1
title: Méthode ImportInitialReplica de la classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ImportInitialReplica
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b60ab10c6387127c294a472c9e1e86be7fd84146
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114586"
---
# <a name="importinitialreplica-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="fafda-103">Méthode ImportInitialReplica de la \_ classe ReplicationService MSVM</span><span class="sxs-lookup"><span data-stu-id="fafda-103">ImportInitialReplica method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="fafda-104">Importe la réplication initiale d’un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="fafda-104">Imports the initial replication for a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="fafda-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fafda-105">Syntax</span></span>


```mof
uint32 ImportInitialReplica(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 InitialReplicationImportLocation,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="fafda-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fafda-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fafda-107">*ComputerSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fafda-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fafda-108">Référence à une instance [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente l’ordinateur virtuel pour lequel la réplication initiale doit être importée.</span><span class="sxs-lookup"><span data-stu-id="fafda-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the initial replication should be imported.</span></span>

</dd> <dt>

<span data-ttu-id="fafda-109">*InitialReplicationImportLocation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fafda-109">*InitialReplicationImportLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fafda-110">Chemin d’accès complet du répertoire à partir duquel la réplication initiale doit être importée.</span><span class="sxs-lookup"><span data-stu-id="fafda-110">The fully qualified path of the directory from which the initial replication is to be imported.</span></span> <span data-ttu-id="fafda-111">La valeur ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="fafda-111">This cannot be **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="fafda-112">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fafda-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fafda-113">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fafda-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fafda-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fafda-114">Return value</span></span>

<span data-ttu-id="fafda-115">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="fafda-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="fafda-116">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="fafda-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fafda-117">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="fafda-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="fafda-118">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="fafda-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="fafda-119">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="fafda-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="fafda-120">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="fafda-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="fafda-121">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="fafda-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="fafda-122">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="fafda-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="fafda-123">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="fafda-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="fafda-124">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="fafda-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="fafda-125">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="fafda-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="fafda-126">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="fafda-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="fafda-127">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="fafda-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="fafda-128">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="fafda-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="fafda-129">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="fafda-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="fafda-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fafda-130">Requirements</span></span>



| <span data-ttu-id="fafda-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fafda-131">Requirement</span></span> | <span data-ttu-id="fafda-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="fafda-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fafda-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fafda-133">Minimum supported client</span></span><br/> | <span data-ttu-id="fafda-134">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fafda-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fafda-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fafda-135">Minimum supported server</span></span><br/> | <span data-ttu-id="fafda-136">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fafda-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fafda-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fafda-137">Namespace</span></span><br/>                | <span data-ttu-id="fafda-138">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="fafda-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fafda-139">MOF</span><span class="sxs-lookup"><span data-stu-id="fafda-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fafda-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fafda-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fafda-141">DLL</span><span class="sxs-lookup"><span data-stu-id="fafda-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fafda-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fafda-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fafda-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fafda-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fafda-144">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="fafda-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

