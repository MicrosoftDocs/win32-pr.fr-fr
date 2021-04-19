---
description: Crée un pool de ressources enfant.
ms.assetid: 30a70231-f1b7-4f0e-ac47-cf5a79ddb8ab
title: Méthode CreatePool de la classe Msvm_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.CreatePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fb29a4b5a47d88232a6b0df6a828d482030b3f1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534616"
---
# <a name="createpool-method-of-the-msvm_resourcepoolconfigurationservice-class"></a><span data-ttu-id="badbc-103">Méthode CreatePool de la \_ classe ResourcePoolConfigurationService MSVM</span><span class="sxs-lookup"><span data-stu-id="badbc-103">CreatePool method of the Msvm\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="badbc-104">Crée un pool de ressources enfant.</span><span class="sxs-lookup"><span data-stu-id="badbc-104">Creates a child resource pool.</span></span> <span data-ttu-id="badbc-105">Le pool de ressources sera étendu au même système que ce service.</span><span class="sxs-lookup"><span data-stu-id="badbc-105">The resource pool will be scoped to the same System as this Service.</span></span> <span data-ttu-id="badbc-106">Le pool résultant sera un pool enfant.</span><span class="sxs-lookup"><span data-stu-id="badbc-106">The resulting pool will be a child pool.</span></span>

## <a name="syntax"></a><span data-ttu-id="badbc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="badbc-107">Syntax</span></span>


```mof
uint32 CreatePool(
  [in]  string               PoolSettings,
  [in]  CIM_ResourcePool REF ParentPools[],
  [in]  string               AllocationSettings[],
  [out] CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="badbc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="badbc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="badbc-109">*PoolSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="badbc-109">*PoolSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="badbc-110">Une instance incorporée de la classe [**MSVM \_ ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md) utilisée pour spécifier les paramètres du pool qui ne sont pas liés à l’allocation.</span><span class="sxs-lookup"><span data-stu-id="badbc-110">An embedded instance of the [**Msvm\_ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md) class that is used to specify the pool settings that are not allocation related.</span></span>

</dd> <dt>

<span data-ttu-id="badbc-111">*ParentPools* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="badbc-111">*ParentPools* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="badbc-112">Tableau de références [**\_ ResourcePool MSVM**](msvm-resourcepool.md) qui représentent le ou les pools à partir desquels créer le pool.</span><span class="sxs-lookup"><span data-stu-id="badbc-112">An array of [**Msvm\_ResourcePool**](msvm-resourcepool.md) references that represent the pool or pools from which to create the new pool.</span></span>

</dd> <dt>

<span data-ttu-id="badbc-113">*AllocationSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="badbc-113">*AllocationSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="badbc-114">Tableau d’une ou de plusieurs instances incorporées de la classe [**MSVM \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) qui sont utilisées pour spécifier les paramètres liés à l’allocation du pool.</span><span class="sxs-lookup"><span data-stu-id="badbc-114">An array of one or more embedded instances of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that are used to specify the pool allocation related settings.</span></span> <span data-ttu-id="badbc-115">Ce tableau doit contenir un élément pour chaque élément dans le tableau *ParentPools* ou exactement un élément.</span><span class="sxs-lookup"><span data-stu-id="badbc-115">This array must contain either one element for each element in the *ParentPools* array, or exactly one element.</span></span> <span data-ttu-id="badbc-116">Si ce tableau contient un élément et que *ParentPools* contient plusieurs éléments, *AlllocationSettings* spécifie une allocation de capacité partagée qui peut être satisfaite par l’un des pools parents.</span><span class="sxs-lookup"><span data-stu-id="badbc-116">If this array contains one element and *ParentPools* contains more than one element, *AlllocationSettings* specifies a shared capacity allocation that can be satisfied by any of the parent pools.</span></span>

<span data-ttu-id="badbc-117">Cela permet de restreindre les ressources qui peuvent être allouées de l’enfant au pool à une limite inférieure à la capacité d’agrégation fournie par ses parents.</span><span class="sxs-lookup"><span data-stu-id="badbc-117">This is used to restrict the resources that can be allocated from the child to the pool to a lower limit than the aggregate capacity provided by its parents.</span></span> <span data-ttu-id="badbc-118">Cette option n’est pas prise en charge par tous les types de ressources.</span><span class="sxs-lookup"><span data-stu-id="badbc-118">This option is not supported by all resource types.</span></span> <span data-ttu-id="badbc-119">Si un type de ressource ne prend pas en charge l’allocation de capacité partagée, cette méthode retourne 32770 (non pris en charge).</span><span class="sxs-lookup"><span data-stu-id="badbc-119">If a resource type does not support shared capacity allocation, this method will return 32770 (Not Supported).</span></span>

</dd> <dt>

<span data-ttu-id="badbc-120">*Pool* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="badbc-120">*Pool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="badbc-121">Référence au pool résultant.</span><span class="sxs-lookup"><span data-stu-id="badbc-121">A reference to the resulting pool.</span></span>

</dd> <dt>

<span data-ttu-id="badbc-122">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="badbc-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="badbc-123">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="badbc-123">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="badbc-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="badbc-124">Return value</span></span>

<span data-ttu-id="badbc-125">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="badbc-125">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="badbc-126">**Tâche terminée sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="badbc-126">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="badbc-127">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="badbc-127">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="badbc-128">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="badbc-128">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="badbc-129">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="badbc-129">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="badbc-130">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="badbc-130">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="badbc-131">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="badbc-131">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="badbc-132">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="badbc-132">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="badbc-133">**Inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="badbc-133">**Unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="badbc-134">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="badbc-134">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="badbc-135">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="badbc-135">**Invalid Parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="badbc-136">**En cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="badbc-136">**In Use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="badbc-137">**État non valide** (32775)</span><span class="sxs-lookup"><span data-stu-id="badbc-137">**Invalid State** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="badbc-138">**Type de ressource incorrect pour le pool** (32776)</span><span class="sxs-lookup"><span data-stu-id="badbc-138">**Incorrect Resource Type for the Pool** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="badbc-139">**Non disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="badbc-139">**Unavailable** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="badbc-140">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="badbc-140">**Out of Memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="badbc-141">**Fournisseur réservé** (32779)</span><span class="sxs-lookup"><span data-stu-id="badbc-141">**Vendor Reserved** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="badbc-142">**Ressources insuffisantes** (32780)</span><span class="sxs-lookup"><span data-stu-id="badbc-142">**Insufficient Resources** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="badbc-143">**Objet introuvable** (32781.. 32787)</span><span class="sxs-lookup"><span data-stu-id="badbc-143">**Object Not Found** (32781..32787)</span></span>
</dt> <dt>

<span data-ttu-id="badbc-144">L' **objet existe** (32788)</span><span class="sxs-lookup"><span data-stu-id="badbc-144">**Object Exists** (32788)</span></span>
</dt> <dt>

<span data-ttu-id="badbc-145">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="badbc-145">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="badbc-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="badbc-146">Requirements</span></span>



| <span data-ttu-id="badbc-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="badbc-147">Requirement</span></span> | <span data-ttu-id="badbc-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="badbc-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="badbc-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="badbc-149">Minimum supported client</span></span><br/> | <span data-ttu-id="badbc-150">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="badbc-150">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="badbc-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="badbc-151">Minimum supported server</span></span><br/> | <span data-ttu-id="badbc-152">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="badbc-152">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="badbc-153">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="badbc-153">Namespace</span></span><br/>                | <span data-ttu-id="badbc-154">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="badbc-154">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="badbc-155">MOF</span><span class="sxs-lookup"><span data-stu-id="badbc-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="badbc-156"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="badbc-156"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="badbc-157">DLL</span><span class="sxs-lookup"><span data-stu-id="badbc-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="badbc-158"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="badbc-158"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="badbc-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="badbc-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="badbc-160">**MSVM \_ ResourcePoolConfigurationService**</span><span class="sxs-lookup"><span data-stu-id="badbc-160">**Msvm\_ResourcePoolConfigurationService**</span></span>](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

