---
description: Supprime un pool de ressources.
ms.assetid: bc3111a4-9687-49ec-890e-190358230c53
title: Méthode DeletePool de la classe Msvm_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.DeletePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 84273daa0aa30dca8722d90d4fcec22b88325bad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541895"
---
# <a name="deletepool-method-of-the-msvm_resourcepoolconfigurationservice-class"></a><span data-ttu-id="c7b6d-103">Méthode DeletePool de la \_ classe ResourcePoolConfigurationService MSVM</span><span class="sxs-lookup"><span data-stu-id="c7b6d-103">DeletePool method of the Msvm\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="c7b6d-104">Supprime un pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="c7b6d-104">Deletes a resource pool.</span></span> <span data-ttu-id="c7b6d-105">Pour supprimer correctement un pool de ressources, aucune allocation ne peut être en suspens ou la suppression échouera avec 32774 (en cours d’utilisation).</span><span class="sxs-lookup"><span data-stu-id="c7b6d-105">To successfully delete a resource pool, no allocations can be outstanding or the delete will fail with 32774 (In Use).</span></span> <span data-ttu-id="c7b6d-106">Si le pool de ressources est un pool de ressources racine, toutes les ressources de l’ordinateur hôte sont renvoyées au système sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="c7b6d-106">If the resource pool is a root resource pool, any host resources are returned back to the underlying system.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7b6d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7b6d-107">Syntax</span></span>


```mof
uint32 DeletePool(
  [in]  CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="c7b6d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c7b6d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7b6d-109">*Pool* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c7b6d-109">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7b6d-110">Référence à une instance de la classe [**\_ ResourcePool CIM**](cim-resourcepool.md) qui représente le pool à supprimer.</span><span class="sxs-lookup"><span data-stu-id="c7b6d-110">A reference to an instance of the [**CIM\_ResourcePool**](cim-resourcepool.md) class that represents the pool to delete.</span></span>

</dd> <dt>

<span data-ttu-id="c7b6d-111">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c7b6d-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7b6d-112">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c7b6d-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7b6d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c7b6d-113">Return value</span></span>

<span data-ttu-id="c7b6d-114">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c7b6d-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="c7b6d-115">**Tâche terminée sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="c7b6d-115">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c7b6d-116">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="c7b6d-116">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c7b6d-117">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="c7b6d-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c7b6d-118">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="c7b6d-118">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="c7b6d-119">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="c7b6d-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="c7b6d-120">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="c7b6d-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="c7b6d-121">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="c7b6d-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="c7b6d-122">**Inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="c7b6d-122">**Unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="c7b6d-123">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="c7b6d-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="c7b6d-124">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="c7b6d-124">**Invalid Parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="c7b6d-125">**En cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="c7b6d-125">**In Use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="c7b6d-126">**État non valide** (32775)</span><span class="sxs-lookup"><span data-stu-id="c7b6d-126">**Invalid State** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="c7b6d-127">**Type de ressource incorrect pour le pool** (32776)</span><span class="sxs-lookup"><span data-stu-id="c7b6d-127">**Incorrect Resource Type for the Pool** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="c7b6d-128">**Non disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="c7b6d-128">**Unavailable** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="c7b6d-129">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="c7b6d-129">**Out of Memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="c7b6d-130">**Fournisseur réservé** (32779)</span><span class="sxs-lookup"><span data-stu-id="c7b6d-130">**Vendor Reserved** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="c7b6d-131">**Ressources insuffisantes** (32780)</span><span class="sxs-lookup"><span data-stu-id="c7b6d-131">**Insufficient Resources** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="c7b6d-132">**Objet introuvable** (32781.. 32787)</span><span class="sxs-lookup"><span data-stu-id="c7b6d-132">**Object Not Found** (32781..32787)</span></span>
</dt> <dt>

<span data-ttu-id="c7b6d-133">L' **objet existe** (32788)</span><span class="sxs-lookup"><span data-stu-id="c7b6d-133">**Object Exists** (32788)</span></span>
</dt> <dt>

<span data-ttu-id="c7b6d-134">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="c7b6d-134">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c7b6d-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7b6d-135">Requirements</span></span>



| <span data-ttu-id="c7b6d-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7b6d-136">Requirement</span></span> | <span data-ttu-id="c7b6d-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7b6d-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7b6d-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7b6d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="c7b6d-139">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c7b6d-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c7b6d-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7b6d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="c7b6d-141">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c7b6d-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c7b6d-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c7b6d-142">Namespace</span></span><br/>                | <span data-ttu-id="c7b6d-143">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="c7b6d-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c7b6d-144">MOF</span><span class="sxs-lookup"><span data-stu-id="c7b6d-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7b6d-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c7b6d-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7b6d-146">DLL</span><span class="sxs-lookup"><span data-stu-id="c7b6d-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7b6d-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c7b6d-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c7b6d-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7b6d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7b6d-149">**MSVM \_ ResourcePoolConfigurationService**</span><span class="sxs-lookup"><span data-stu-id="c7b6d-149">**Msvm\_ResourcePoolConfigurationService**</span></span>](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

