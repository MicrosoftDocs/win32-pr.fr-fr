---
description: Modifie les paramètres de ressource du pool parent pour les ressources affectées à un pool enfant.
ms.assetid: 419fca70-5f15-4593-80ac-ef2af2c3dde5
title: Méthode ModifyPoolResources de la classe Msvm_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.ModifyPoolResources
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2efffdbcc34577f675556874c4153eea2670768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867070"
---
# <a name="modifypoolresources-method-of-the-msvm_resourcepoolconfigurationservice-class"></a><span data-ttu-id="fa62c-103">Méthode ModifyPoolResources de la \_ classe ResourcePoolConfigurationService MSVM</span><span class="sxs-lookup"><span data-stu-id="fa62c-103">ModifyPoolResources method of the Msvm\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="fa62c-104">Modifie les paramètres de ressource du pool parent pour les ressources affectées à un pool enfant.</span><span class="sxs-lookup"><span data-stu-id="fa62c-104">Changes the parent pool resource settings for resources assigned to a child pool.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa62c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa62c-105">Syntax</span></span>


```mof
uint32 ModifyPoolResources(
  [in]  CIM_ResourcePool REF ChildPool,
  [in]  CIM_ResourcePool REF ParentPools[],
  [in]  string               AllocationSettings[],
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="fa62c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa62c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa62c-107">*ChildPool* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fa62c-107">*ChildPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa62c-108">Référence à une instance de la classe [**\_ ResourcePool CIM**](cim-resourcepool.md) qui représente le pool enfant à modifier.</span><span class="sxs-lookup"><span data-stu-id="fa62c-108">A reference to an instance of the [**CIM\_ResourcePool**](cim-resourcepool.md) class that represents the child pool to modify.</span></span>

</dd> <dt>

<span data-ttu-id="fa62c-109">*ParentPools* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fa62c-109">*ParentPools* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa62c-110">Tableau de références [**\_ ResourcePool CIM**](cim-resourcepool.md) qui représentent les nouveaux pools parents à assigner au pool enfant.</span><span class="sxs-lookup"><span data-stu-id="fa62c-110">An array of [**CIM\_ResourcePool**](cim-resourcepool.md) references that represent the new parent pools to assign to the child pool.</span></span>

</dd> <dt>

<span data-ttu-id="fa62c-111">*AllocationSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fa62c-111">*AllocationSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa62c-112">Tableau facultatif d’une ou plusieurs instances incorporées de la classe [**MSVM \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) qui sont utilisées pour spécifier les paramètres liés à l’allocation du pool.</span><span class="sxs-lookup"><span data-stu-id="fa62c-112">An optional array of one or more embedded instances of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that are used to specify the pool allocation related settings.</span></span>

</dd> <dt>

<span data-ttu-id="fa62c-113">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fa62c-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa62c-114">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fa62c-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa62c-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fa62c-115">Return value</span></span>

<span data-ttu-id="fa62c-116">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="fa62c-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="fa62c-117">**Tâche terminée sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="fa62c-117">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fa62c-118">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="fa62c-118">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="fa62c-119">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="fa62c-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="fa62c-120">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="fa62c-120">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="fa62c-121">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="fa62c-121">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="fa62c-122">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="fa62c-122">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="fa62c-123">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="fa62c-123">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="fa62c-124">**Inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="fa62c-124">**Unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="fa62c-125">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="fa62c-125">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="fa62c-126">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="fa62c-126">**Invalid Parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="fa62c-127">**En cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="fa62c-127">**In Use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="fa62c-128">**État non valide** (32775)</span><span class="sxs-lookup"><span data-stu-id="fa62c-128">**Invalid State** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="fa62c-129">**Type de ressource incorrect pour le pool** (32776)</span><span class="sxs-lookup"><span data-stu-id="fa62c-129">**Incorrect Resource Type for the Pool** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="fa62c-130">**Non disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="fa62c-130">**Unavailable** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="fa62c-131">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="fa62c-131">**Out of Memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="fa62c-132">**Fournisseur réservé** (32779)</span><span class="sxs-lookup"><span data-stu-id="fa62c-132">**Vendor Reserved** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="fa62c-133">**Ressources insuffisantes** (32780)</span><span class="sxs-lookup"><span data-stu-id="fa62c-133">**Insufficient Resources** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="fa62c-134">**Objet introuvable** (32781.. 32787)</span><span class="sxs-lookup"><span data-stu-id="fa62c-134">**Object Not Found** (32781..32787)</span></span>
</dt> <dt>

<span data-ttu-id="fa62c-135">L' **objet existe** (32788)</span><span class="sxs-lookup"><span data-stu-id="fa62c-135">**Object Exists** (32788)</span></span>
</dt> <dt>

<span data-ttu-id="fa62c-136">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="fa62c-136">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="fa62c-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa62c-137">Requirements</span></span>



| <span data-ttu-id="fa62c-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa62c-138">Requirement</span></span> | <span data-ttu-id="fa62c-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa62c-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa62c-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa62c-140">Minimum supported client</span></span><br/> | <span data-ttu-id="fa62c-141">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa62c-141">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fa62c-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa62c-142">Minimum supported server</span></span><br/> | <span data-ttu-id="fa62c-143">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa62c-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fa62c-144">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fa62c-144">Namespace</span></span><br/>                | <span data-ttu-id="fa62c-145">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="fa62c-145">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fa62c-146">MOF</span><span class="sxs-lookup"><span data-stu-id="fa62c-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa62c-147"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fa62c-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa62c-148">DLL</span><span class="sxs-lookup"><span data-stu-id="fa62c-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa62c-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fa62c-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fa62c-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa62c-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa62c-151">**MSVM \_ ResourcePoolConfigurationService**</span><span class="sxs-lookup"><span data-stu-id="fa62c-151">**Msvm\_ResourcePoolConfigurationService**</span></span>](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

