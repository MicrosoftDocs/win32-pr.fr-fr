---
description: Démarre un travail pour créer un ResourcePool racine. Le ResourcePool sera étendu au même système que ce service.
ms.assetid: 357880dc-125a-452c-89f5-44cd17684436
title: Méthode CreateResourcePool de la classe CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.CreateResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ca339eb2e2a4ec0fb441c5ed1a657608d71248bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752245"
---
# <a name="createresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="93c49-104">Méthode CreateResourcePool de la \_ classe CIM ResourcePoolConfigurationService</span><span class="sxs-lookup"><span data-stu-id="93c49-104">CreateResourcePool method of the CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="93c49-105">Démarre un travail pour créer un ResourcePool racine.</span><span class="sxs-lookup"><span data-stu-id="93c49-105">Starts a job to create a root ResourcePool.</span></span> <span data-ttu-id="93c49-106">Le ResourcePool sera étendu au même système que ce service.</span><span class="sxs-lookup"><span data-stu-id="93c49-106">The ResourcePool will be scoped to the same System as this Service.</span></span>

## <a name="syntax"></a><span data-ttu-id="93c49-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="93c49-107">Syntax</span></span>


```mof
uint32 CreateResourcePool(
  [in]  string                ElementName,
  [in]  CIM_LogicalDevice REF HostResources[],
  [in]  string                ResourceType,
  [out] CIM_ResourcePool  REF Pool,
  [out] CIM_ConcreteJob   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="93c49-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="93c49-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93c49-109">*ElementName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="93c49-109">*ElementName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93c49-110">Nom approprié de l’utilisateur final pour le pool en cours de création.</span><span class="sxs-lookup"><span data-stu-id="93c49-110">A end user relevant name for the pool being created.</span></span> <span data-ttu-id="93c49-111">Si la **valeur est null**, un nom par défaut fourni par le système peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="93c49-111">If **NULL**, then a system supplied default name can be used.</span></span> <span data-ttu-id="93c49-112">La valeur sera stockée dans la propriété **ElementName** pour le pool créé.</span><span class="sxs-lookup"><span data-stu-id="93c49-112">The value will be stored in the **ElementName** property for the created pool.</span></span>

</dd> <dt>

<span data-ttu-id="93c49-113">*HostResources* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="93c49-113">*HostResources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93c49-114">Tableau de zéro ou plusieurs [**périphériques \_ LogicalDevice CIM**](cim-logicaldevice.md) utilisés pour créer le pool ou pour modifier les étendues sources.</span><span class="sxs-lookup"><span data-stu-id="93c49-114">Array of zero or more [**CIM\_LogicalDevice**](cim-logicaldevice.md) devices that are used to create the Pool or modify the source extents.</span></span> <span data-ttu-id="93c49-115">Tous les éléments du tableau doivent être du même type.</span><span class="sxs-lookup"><span data-stu-id="93c49-115">All elements in the array must be of the same type.</span></span>

</dd> <dt>

<span data-ttu-id="93c49-116">*ResourceType* \[in\]</span><span class="sxs-lookup"><span data-stu-id="93c49-116">*ResourceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93c49-117">Le type de ressources que le pool créé doit gérer.</span><span class="sxs-lookup"><span data-stu-id="93c49-117">The type of resources the created pool will manage.</span></span> <span data-ttu-id="93c49-118">Si *HostResources* contient des éléments, cette propriété doit avoir le même type.</span><span class="sxs-lookup"><span data-stu-id="93c49-118">If *HostResources* contains elements, this property must mach their type.</span></span>

</dd> <dt>

<span data-ttu-id="93c49-119">*Pool* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="93c49-119">*Pool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93c49-120">En cas de réussite, retourne une référence au [**\_ ResourcePool CIM**](cim-resourcepool.md)résultant.</span><span class="sxs-lookup"><span data-stu-id="93c49-120">On success, returns a reference to the resulting [**CIM\_ResourcePool**](cim-resourcepool.md).</span></span> <span data-ttu-id="93c49-121">Lorsqu’un travail est retourné, il peut s’agir de la **valeur null**, auquel cas le client doit utiliser le travail pour trouver le ResourcePool résultant une fois le travail terminé.</span><span class="sxs-lookup"><span data-stu-id="93c49-121">When a Job is returned, this may be **NULL**, in which case, the client must use the Job to find the resulting ResourcePool once the Job completes.</span></span>

</dd> <dt>

<span data-ttu-id="93c49-122">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="93c49-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93c49-123">Référence à un [**\_ ConcreteJob CIM**](cim-concretejob.md) qui représente le travail (peut être null si le travail est terminé).</span><span class="sxs-lookup"><span data-stu-id="93c49-123">Reference to a [**CIM\_ConcreteJob**](cim-concretejob.md) that represents the job (may be null if job completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93c49-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="93c49-124">Return value</span></span>

<span data-ttu-id="93c49-125">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="93c49-125">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="93c49-126">**Tâche terminée sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="93c49-126">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="93c49-127">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="93c49-127">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="93c49-128">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="93c49-128">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="93c49-129">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="93c49-129">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="93c49-130">**Échec** (4)</span><span class="sxs-lookup"><span data-stu-id="93c49-130">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="93c49-131">**Paramètre non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="93c49-131">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="93c49-132">**En cours d’utilisation** (6)</span><span class="sxs-lookup"><span data-stu-id="93c49-132">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="93c49-133">**ResourceType incorrect pour le pool** (7)</span><span class="sxs-lookup"><span data-stu-id="93c49-133">**Incorrect ResourceType for the Pool** (7)</span></span>
</dt> <dt>

<span data-ttu-id="93c49-134">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="93c49-134">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="93c49-135">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="93c49-135">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="93c49-136">**Taille non prise en charge** (4097)</span><span class="sxs-lookup"><span data-stu-id="93c49-136">**Size Not Supported** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="93c49-137">**Méthode réservée** (4098.. 32767)</span><span class="sxs-lookup"><span data-stu-id="93c49-137">**Method Reserved** (4098..32767)</span></span>
</dt> <dt>

<span data-ttu-id="93c49-138">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="93c49-138">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="93c49-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="93c49-139">Requirements</span></span>



| <span data-ttu-id="93c49-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="93c49-140">Requirement</span></span> | <span data-ttu-id="93c49-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="93c49-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93c49-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93c49-142">Minimum supported client</span></span><br/> | <span data-ttu-id="93c49-143">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="93c49-143">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="93c49-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93c49-144">Minimum supported server</span></span><br/> | <span data-ttu-id="93c49-145">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="93c49-145">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="93c49-146">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="93c49-146">Namespace</span></span><br/>                | <span data-ttu-id="93c49-147">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="93c49-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="93c49-148">MOF</span><span class="sxs-lookup"><span data-stu-id="93c49-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93c49-149"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="93c49-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="93c49-150">DLL</span><span class="sxs-lookup"><span data-stu-id="93c49-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93c49-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="93c49-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="93c49-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93c49-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93c49-153">**\_RESOURCEPOOLCONFIGURATIONSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="93c49-153">**CIM\_ResourcePoolConfigurationService**</span></span>](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




