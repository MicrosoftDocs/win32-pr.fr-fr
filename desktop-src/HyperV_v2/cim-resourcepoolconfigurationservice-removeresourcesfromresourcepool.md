---
description: Démarre un travail pour supprimer des ressources d’un pool de ressources.
ms.assetid: 1689ccbf-a524-45b7-bf95-6341a3b28f6c
title: Méthode RemoveResourcesFromResourcePool de la classe CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.RemoveResourcesFromResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 41c8a7d1608b9c4d5ea629aa9c053e022d59d9ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526782"
---
# <a name="removeresourcesfromresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="327c8-103">Méthode RemoveResourcesFromResourcePool de la \_ classe CIM ResourcePoolConfigurationService</span><span class="sxs-lookup"><span data-stu-id="327c8-103">RemoveResourcesFromResourcePool method of the CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="327c8-104">Démarre un travail pour supprimer des ressources d’un pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="327c8-104">Starts a job to remove resources from a resource pool.</span></span>

## <a name="syntax"></a><span data-ttu-id="327c8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="327c8-105">Syntax</span></span>


```mof
uint32 RemoveResourcesFromResourcePool(
  [in]  CIM_LogicalDevice REF HostResources[],
  [in]  CIM_ResourcePool  REF Pool,
  [out] CIM_ConcreteJob   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="327c8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="327c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="327c8-107">*HostResources* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="327c8-107">*HostResources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="327c8-108">Tableau d’instances [**CIM \_ LogicalDevice**](cim-logicaldevice.md) à supprimer du pool.</span><span class="sxs-lookup"><span data-stu-id="327c8-108">Array of [**CIM\_LogicalDevice**](cim-logicaldevice.md) instances to remove from the pool.</span></span>

</dd> <dt>

<span data-ttu-id="327c8-109">*Pool* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="327c8-109">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="327c8-110">[**\_ ResourcePool CIM**](cim-resourcepool.md) représentant le pool duquel supprimer les ressources.</span><span class="sxs-lookup"><span data-stu-id="327c8-110">A [**CIM\_ResourcePool**](cim-resourcepool.md) representing the pool to remove the resources from.</span></span>

</dd> <dt>

<span data-ttu-id="327c8-111">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="327c8-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="327c8-112">[**\_ ConcreteJob CIM**](cim-concretejob.md) qui référence le travail (peut être **null** si le travail est terminé).</span><span class="sxs-lookup"><span data-stu-id="327c8-112">A [**CIM\_ConcreteJob**](cim-concretejob.md) that references the job (may be **null** if job completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="327c8-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="327c8-113">Return value</span></span>

<span data-ttu-id="327c8-114">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="327c8-114">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="327c8-115">**Tâche terminée sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="327c8-115">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="327c8-116">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="327c8-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="327c8-117">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="327c8-117">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="327c8-118">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="327c8-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="327c8-119">**Échec** (4)</span><span class="sxs-lookup"><span data-stu-id="327c8-119">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="327c8-120">**Paramètre non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="327c8-120">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="327c8-121">**En cours d’utilisation** (6)</span><span class="sxs-lookup"><span data-stu-id="327c8-121">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="327c8-122">**ResourceType incorrect pour le pool** (7)</span><span class="sxs-lookup"><span data-stu-id="327c8-122">**Incorrect ResourceType for the Pool** (7)</span></span>
</dt> <dt>

<span data-ttu-id="327c8-123">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="327c8-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="327c8-124">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="327c8-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="327c8-125">**Taille non prise en charge** (4097)</span><span class="sxs-lookup"><span data-stu-id="327c8-125">**Size Not Supported** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="327c8-126">**Méthode réservée** (4098.. 32767)</span><span class="sxs-lookup"><span data-stu-id="327c8-126">**Method Reserved** (4098..32767)</span></span>
</dt> <dt>

<span data-ttu-id="327c8-127">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="327c8-127">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="327c8-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="327c8-128">Requirements</span></span>



| <span data-ttu-id="327c8-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="327c8-129">Requirement</span></span> | <span data-ttu-id="327c8-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="327c8-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="327c8-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="327c8-131">Minimum supported client</span></span><br/> | <span data-ttu-id="327c8-132">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="327c8-132">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="327c8-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="327c8-133">Minimum supported server</span></span><br/> | <span data-ttu-id="327c8-134">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="327c8-134">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="327c8-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="327c8-135">Namespace</span></span><br/>                | <span data-ttu-id="327c8-136">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="327c8-136">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="327c8-137">MOF</span><span class="sxs-lookup"><span data-stu-id="327c8-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="327c8-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="327c8-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="327c8-139">DLL</span><span class="sxs-lookup"><span data-stu-id="327c8-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="327c8-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="327c8-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="327c8-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="327c8-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="327c8-142">**\_RESOURCEPOOLCONFIGURATIONSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="327c8-142">**CIM\_ResourcePoolConfigurationService**</span></span>](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




