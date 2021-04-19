---
description: Génère un blob opaque de données qui contient des informations de compatibilité pour le système spécifié.
ms.assetid: 5cfb50c4-d695-4867-ac6a-234ce5120a6d
title: Méthode GetSystemCompatibilityInfo de la classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.GetSystemCompatibilityInfo
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9b0326dfb39123e508e9c5fefbd0404288cb97b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514582"
---
# <a name="getsystemcompatibilityinfo-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="738d3-103">Méthode GetSystemCompatibilityInfo de la \_ classe VirtualSystemMigrationService MSVM</span><span class="sxs-lookup"><span data-stu-id="738d3-103">GetSystemCompatibilityInfo method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="738d3-104">Génère un blob opaque de données qui contient des informations de compatibilité pour le système spécifié.</span><span class="sxs-lookup"><span data-stu-id="738d3-104">Generates an opaque blob of data that contains compatibility information for the specified system.</span></span> <span data-ttu-id="738d3-105">Cette méthode est utilisée conjointement avec la méthode [**CheckSystemCompatibilityInfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) pour déterminer si une migration rapide ou dynamique d’un ordinateur virtuel vers un autre système d’ordinateur d’hébergement est possible sans réellement tenter la migration.</span><span class="sxs-lookup"><span data-stu-id="738d3-105">This method is used in conjunction with the [**CheckSystemCompatibilityInfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) method to determine whether a quick or live migration of a virtual machine to another hosting computer system is possible without actually attempting the migration.</span></span>

## <a name="syntax"></a><span data-ttu-id="738d3-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="738d3-106">Syntax</span></span>


```mof
uint32 GetSystemCompatibilityInfo(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] uint8                  CompatibilityInfo[]
);
```



## <a name="parameters"></a><span data-ttu-id="738d3-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="738d3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="738d3-108">*ComputerSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="738d3-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="738d3-109">Référence à une classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) qui représente l’ordinateur virtuel pour lequel récupérer des informations de compatibilité.</span><span class="sxs-lookup"><span data-stu-id="738d3-109">A reference to a [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine to retrieve compatibility information for.</span></span> <span data-ttu-id="738d3-110">Si ce paramètre fait référence au système de l’ordinateur hôte, les données retournées dans le paramètre *CompatibilityInfo* peuvent être utilisées pour déterminer si l’un des ordinateurs virtuels sur le système informatique d’hébergement peut être rapidement migré vers un autre système informatique d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="738d3-110">If this parameter refers to the hosting computer system, the data returned in the *CompatibilityInfo* parameter can be used to determine whether any of the virtual machines on the hosting computer system can be quickly migrated to another hosting computer system.</span></span>

</dd> <dt>

<span data-ttu-id="738d3-111">*CompatibilityInfo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="738d3-111">*CompatibilityInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="738d3-112">Un blob de données opaque qui peut être passé à la méthode [**CheckSystemCompatibilityInfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) sur un autre système d’ordinateur hôte pour confirmer la compatibilité.</span><span class="sxs-lookup"><span data-stu-id="738d3-112">An opaque blob of data that can be passed to the [**CheckSystemCompatibilityInfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) method on another hosting computer system to confirm compatibility.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="738d3-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="738d3-113">Return value</span></span>

<span data-ttu-id="738d3-114">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="738d3-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="738d3-115">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="738d3-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="738d3-116">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="738d3-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="738d3-117">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="738d3-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="738d3-118">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="738d3-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="738d3-119">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="738d3-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="738d3-120">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="738d3-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="738d3-121">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="738d3-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="738d3-122">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="738d3-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="738d3-123">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="738d3-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="738d3-124">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="738d3-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="738d3-125">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="738d3-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="738d3-126">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="738d3-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="738d3-127">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="738d3-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="738d3-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="738d3-128">Requirements</span></span>



| <span data-ttu-id="738d3-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="738d3-129">Requirement</span></span> | <span data-ttu-id="738d3-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="738d3-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="738d3-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="738d3-131">Minimum supported client</span></span><br/> | <span data-ttu-id="738d3-132">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="738d3-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="738d3-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="738d3-133">Minimum supported server</span></span><br/> | <span data-ttu-id="738d3-134">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="738d3-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="738d3-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="738d3-135">Namespace</span></span><br/>                | <span data-ttu-id="738d3-136">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="738d3-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="738d3-137">MOF</span><span class="sxs-lookup"><span data-stu-id="738d3-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="738d3-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="738d3-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="738d3-139">DLL</span><span class="sxs-lookup"><span data-stu-id="738d3-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="738d3-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="738d3-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="738d3-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="738d3-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="738d3-142">**MSVM \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="738d3-142">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




