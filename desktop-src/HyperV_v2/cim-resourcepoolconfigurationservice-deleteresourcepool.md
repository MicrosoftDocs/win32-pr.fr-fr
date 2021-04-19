---
description: Démarrer un travail pour supprimer un pool de ressources.
ms.assetid: af3d9c7c-a825-4568-822d-044b3d92d144
title: Méthode DeleteResourcePool de la classe CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.DeleteResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9cab27df07a6a3a9679cb5e6595b6ba558d8b05e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516496"
---
# <a name="deleteresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="970d2-103">Méthode DeleteResourcePool de la \_ classe CIM ResourcePoolConfigurationService</span><span class="sxs-lookup"><span data-stu-id="970d2-103">DeleteResourcePool method of the CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="970d2-104">Démarrer un travail pour supprimer un pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="970d2-104">Start a job to delete a resource pool.</span></span> <span data-ttu-id="970d2-105">Aucune allocation n’est en suspens, ou la suppression échoue avec « en cours d’utilisation ».</span><span class="sxs-lookup"><span data-stu-id="970d2-105">No allocations may be outstanding or the delete will fail with "In Use."</span></span> <span data-ttu-id="970d2-106">Si le pool de ressources est un pool de ressources racine, toutes les ressources de l’ordinateur hôte sont renvoyées au système sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="970d2-106">If the resource pool is a root resource pool, any host resources are returned back to the underlying system.</span></span>

## <a name="syntax"></a><span data-ttu-id="970d2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="970d2-107">Syntax</span></span>


```mof
uint32 DeleteResourcePool(
  [in]  CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="970d2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="970d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="970d2-109">*Pool* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="970d2-109">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="970d2-110">[**\_ ResourcePool CIM**](cim-resourcepool.md) qui fait référence au pool à supprimer.</span><span class="sxs-lookup"><span data-stu-id="970d2-110">A [**CIM\_ResourcePool**](cim-resourcepool.md) that references to the pool to delete.</span></span>

</dd> <dt>

<span data-ttu-id="970d2-111">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="970d2-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="970d2-112">[**\_ ConcreteJob CIM**](cim-concretejob.md) qui référence le travail (peut être **null** si le travail est terminé).</span><span class="sxs-lookup"><span data-stu-id="970d2-112">A [**CIM\_ConcreteJob**](cim-concretejob.md) that references the job (may be **null** if job completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="970d2-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="970d2-113">Return value</span></span>

<span data-ttu-id="970d2-114">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="970d2-114">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="970d2-115">**Tâche terminée sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="970d2-115">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="970d2-116">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="970d2-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="970d2-117">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="970d2-117">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="970d2-118">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="970d2-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="970d2-119">**Échec** (4)</span><span class="sxs-lookup"><span data-stu-id="970d2-119">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="970d2-120">**Paramètre non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="970d2-120">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="970d2-121">**En cours d’utilisation** (6)</span><span class="sxs-lookup"><span data-stu-id="970d2-121">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="970d2-122">**ResourceType incorrect pour le pool** (7)</span><span class="sxs-lookup"><span data-stu-id="970d2-122">**Incorrect ResourceType for the Pool** (7)</span></span>
</dt> <dt>

<span data-ttu-id="970d2-123">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="970d2-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="970d2-124">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="970d2-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="970d2-125">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="970d2-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="970d2-126">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="970d2-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="970d2-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="970d2-127">Requirements</span></span>



| <span data-ttu-id="970d2-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="970d2-128">Requirement</span></span> | <span data-ttu-id="970d2-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="970d2-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="970d2-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="970d2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="970d2-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="970d2-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="970d2-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="970d2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="970d2-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="970d2-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="970d2-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="970d2-134">Namespace</span></span><br/>                | <span data-ttu-id="970d2-135">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="970d2-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="970d2-136">MOF</span><span class="sxs-lookup"><span data-stu-id="970d2-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="970d2-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="970d2-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="970d2-138">DLL</span><span class="sxs-lookup"><span data-stu-id="970d2-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="970d2-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="970d2-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="970d2-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="970d2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="970d2-141">**\_RESOURCEPOOLCONFIGURATIONSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="970d2-141">**CIM\_ResourcePoolConfigurationService**</span></span>](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




