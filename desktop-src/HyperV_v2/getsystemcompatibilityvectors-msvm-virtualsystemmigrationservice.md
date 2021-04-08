---
description: Obtient une liste d' \_ instances MSVM CompatibilityVector qui peuvent être utilisées pour vérifier la compatibilité de l’ordinateur virtuel (VM).
ms.assetid: 3881D9A0-07C2-4275-925D-F3C3A36B79B4
title: 'Msvm_VirtualSystemMigrationService :: GetSystemCompatibilityVectors, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.GetSystemCompatibilityVectors
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8ef8a374d992468247f6dc8f914d7252e7cd2829
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950998"
---
# <a name="msvm_virtualsystemmigrationservicegetsystemcompatibilityvectors-method"></a><span data-ttu-id="e2e6f-103">MSVM \_ VirtualSystemMigrationService :: GetSystemCompatibilityVectors, méthode</span><span class="sxs-lookup"><span data-stu-id="e2e6f-103">Msvm\_VirtualSystemMigrationService::GetSystemCompatibilityVectors method</span></span>

<span data-ttu-id="e2e6f-104">Obtient une liste d’instances [**MSVM \_ CompatibilityVector**](msvm-compatibilityvector.md) qui peuvent être utilisées pour vérifier la compatibilité de l’ordinateur virtuel (VM).</span><span class="sxs-lookup"><span data-stu-id="e2e6f-104">Gets a list of [**Msvm\_CompatibilityVector**](msvm-compatibilityvector.md) instances that can be used to check for virtual machine (VM) to host compatibility.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2e6f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e2e6f-105">Syntax</span></span>


```C++
uint32 GetSystemCompatibilityVectors(
  [in]  CIM_ComputerSystem   ComputerSystem,
  [out] Msvm_CompatibilityVector CompatibilityVectors[]
);
```



## <a name="parameters"></a><span data-ttu-id="e2e6f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e2e6f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2e6f-107">*ComputerSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e2e6f-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2e6f-108">Référence à une classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) qui représente la machine virtuelle pour laquelle récupérer des vecteurs de compatibilité.</span><span class="sxs-lookup"><span data-stu-id="e2e6f-108">A reference to a [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the VM to retrieve compatibility vectors for.</span></span> <span data-ttu-id="e2e6f-109">Si ce paramètre fait référence au système de l’ordinateur hôte, les données retournées dans le paramètre *CompatibilityVectors* peuvent être utilisées pour déterminer si l’une des machines virtuelles sur le système de l’ordinateur hôte peut être rapidement migrée vers un autre système informatique d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="e2e6f-109">If this parameter refers to the hosting computer system, the data returned in the *CompatibilityVectors* parameter can be used to determine whether any of the VMs on the hosting computer system can be quickly migrated to another hosting computer system.</span></span>

</dd> <dt>

<span data-ttu-id="e2e6f-110">*CompatibilityVectors* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e2e6f-110">*CompatibilityVectors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2e6f-111">Tableau d’instances [**MSVM \_ CompatibilityVector**](msvm-compatibilityvector.md) qui contiennent les informations de compatibilité pour les machines virtuelles ou le système informatique d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="e2e6f-111">An array of [**Msvm\_CompatibilityVector**](msvm-compatibilityvector.md) instances that contain the compatibility info for the VMs or hosting computer system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2e6f-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e2e6f-112">Return value</span></span>

<span data-ttu-id="e2e6f-113">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e2e6f-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e2e6f-114">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="e2e6f-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e2e6f-115">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="e2e6f-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e2e6f-116">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="e2e6f-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e2e6f-117">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="e2e6f-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e2e6f-118">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="e2e6f-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e2e6f-119">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="e2e6f-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e2e6f-120">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="e2e6f-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e2e6f-121">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="e2e6f-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e2e6f-122">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="e2e6f-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e2e6f-123">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="e2e6f-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e2e6f-124">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="e2e6f-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e2e6f-125">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="e2e6f-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e2e6f-126">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="e2e6f-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="e2e6f-127">Notes</span><span class="sxs-lookup"><span data-stu-id="e2e6f-127">Remarks</span></span>

<span data-ttu-id="e2e6f-128">**GetSystemCompatibilityVectors** obtient les informations de compatibilité d’un ordinateur virtuel (en cas d’exécution sur un système informatique d’ordinateur virtuel) ou d’un ordinateur hôte (en cas d’exécution sur un système d’ordinateur hôte).</span><span class="sxs-lookup"><span data-stu-id="e2e6f-128">**GetSystemCompatibilityVectors** gets compatibility info for a virtual machine (VM) (when run on a VM computer system) or a host (when run on a host computer system).</span></span> <span data-ttu-id="e2e6f-129">Les informations de compatibilité restent opaques pour le client, tandis que les informations permettent de comparer les informations de compatibilité de l’ordinateur hôte avec celles de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="e2e6f-129">The compatibility info remains opaque to the client while the info provides a way to compare the host compatibility info with that of the VM.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2e6f-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2e6f-130">Requirements</span></span>



| <span data-ttu-id="e2e6f-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2e6f-131">Requirement</span></span> | <span data-ttu-id="e2e6f-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2e6f-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2e6f-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2e6f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e2e6f-134">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2e6f-134">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="e2e6f-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2e6f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e2e6f-136">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2e6f-136">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e2e6f-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e2e6f-137">Namespace</span></span><br/>                | <span data-ttu-id="e2e6f-138">\\\\\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="e2e6f-138">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="e2e6f-139">MOF</span><span class="sxs-lookup"><span data-stu-id="e2e6f-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2e6f-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2e6f-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2e6f-141">DLL</span><span class="sxs-lookup"><span data-stu-id="e2e6f-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2e6f-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e2e6f-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e2e6f-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2e6f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2e6f-144">**MSVM \_ CompatibilityVector**</span><span class="sxs-lookup"><span data-stu-id="e2e6f-144">**Msvm\_CompatibilityVector**</span></span>](msvm-compatibilityvector.md)
</dt> <dt>

[<span data-ttu-id="e2e6f-145">**MSVM \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="e2e6f-145">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




