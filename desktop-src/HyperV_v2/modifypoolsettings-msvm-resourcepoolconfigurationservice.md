---
description: Modifie les paramètres d’un pool enfant qui ne sont pas liés à l’allocation.
ms.assetid: f60068e0-f333-41e2-8f11-78aa48dfa260
title: Méthode ModifyPoolSettings de la classe Msvm_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.ModifyPoolSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: edc5f48dabfb84554954cc80d9c4e8a20678d34f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204023"
---
# <a name="modifypoolsettings-method-of-the-msvm_resourcepoolconfigurationservice-class"></a><span data-ttu-id="3ffab-103">Méthode ModifyPoolSettings de la \_ classe ResourcePoolConfigurationService MSVM</span><span class="sxs-lookup"><span data-stu-id="3ffab-103">ModifyPoolSettings method of the Msvm\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="3ffab-104">Modifie les paramètres d’un pool enfant qui ne sont pas liés à l’allocation.</span><span class="sxs-lookup"><span data-stu-id="3ffab-104">Changes the settings of a child pool that are not allocation related.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ffab-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3ffab-105">Syntax</span></span>


```mof
uint32 ModifyPoolSettings(
  [in]  CIM_ResourcePool REF ChildPool,
  [in]  string               PoolSettings,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="3ffab-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3ffab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ffab-107">*ChildPool* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3ffab-107">*ChildPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ffab-108">Référence à une instance de la classe [**\_ ResourcePool CIM**](cim-resourcepool.md) qui représente le pool enfant à modifier.</span><span class="sxs-lookup"><span data-stu-id="3ffab-108">A reference to an instance of the [**CIM\_ResourcePool**](cim-resourcepool.md) class that represents the child pool to modify.</span></span>

</dd> <dt>

<span data-ttu-id="3ffab-109">*PoolSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3ffab-109">*PoolSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ffab-110">Une instance incorporée de la classe [**MSVM \_ ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md) utilisée pour spécifier les nouveaux paramètres pour le pool.</span><span class="sxs-lookup"><span data-stu-id="3ffab-110">An embedded instance of the [**Msvm\_ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md) class that is used to specify the new settings for the pool.</span></span>

</dd> <dt>

<span data-ttu-id="3ffab-111">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3ffab-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ffab-112">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3ffab-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ffab-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3ffab-113">Return value</span></span>

<span data-ttu-id="3ffab-114">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="3ffab-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="3ffab-115">**Tâche terminée sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="3ffab-115">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3ffab-116">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="3ffab-116">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3ffab-117">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="3ffab-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3ffab-118">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="3ffab-118">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="3ffab-119">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="3ffab-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="3ffab-120">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="3ffab-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="3ffab-121">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="3ffab-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="3ffab-122">**Inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="3ffab-122">**Unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="3ffab-123">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="3ffab-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="3ffab-124">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="3ffab-124">**Invalid Parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="3ffab-125">**En cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="3ffab-125">**In Use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="3ffab-126">**État non valide** (32775)</span><span class="sxs-lookup"><span data-stu-id="3ffab-126">**Invalid State** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="3ffab-127">**Type de ressource incorrect pour le pool** (32776)</span><span class="sxs-lookup"><span data-stu-id="3ffab-127">**Incorrect Resource Type for the Pool** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="3ffab-128">**Non disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="3ffab-128">**Unavailable** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="3ffab-129">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="3ffab-129">**Out of Memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="3ffab-130">**Fournisseur réservé** (32779)</span><span class="sxs-lookup"><span data-stu-id="3ffab-130">**Vendor Reserved** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="3ffab-131">**Ressources insuffisantes** (32780)</span><span class="sxs-lookup"><span data-stu-id="3ffab-131">**Insufficient Resources** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="3ffab-132">**Objet introuvable** (32781.. 32787)</span><span class="sxs-lookup"><span data-stu-id="3ffab-132">**Object Not Found** (32781..32787)</span></span>
</dt> <dt>

<span data-ttu-id="3ffab-133">L' **objet existe** (32788)</span><span class="sxs-lookup"><span data-stu-id="3ffab-133">**Object Exists** (32788)</span></span>
</dt> <dt>

<span data-ttu-id="3ffab-134">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="3ffab-134">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3ffab-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3ffab-135">Requirements</span></span>



| <span data-ttu-id="3ffab-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3ffab-136">Requirement</span></span> | <span data-ttu-id="3ffab-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ffab-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ffab-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ffab-138">Minimum supported client</span></span><br/> | <span data-ttu-id="3ffab-139">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3ffab-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3ffab-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ffab-140">Minimum supported server</span></span><br/> | <span data-ttu-id="3ffab-141">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3ffab-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3ffab-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3ffab-142">Namespace</span></span><br/>                | <span data-ttu-id="3ffab-143">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="3ffab-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3ffab-144">MOF</span><span class="sxs-lookup"><span data-stu-id="3ffab-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ffab-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3ffab-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ffab-146">DLL</span><span class="sxs-lookup"><span data-stu-id="3ffab-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ffab-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3ffab-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3ffab-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ffab-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ffab-149">**MSVM \_ ResourcePoolConfigurationService**</span><span class="sxs-lookup"><span data-stu-id="3ffab-149">**Msvm\_ResourcePoolConfigurationService**</span></span>](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

