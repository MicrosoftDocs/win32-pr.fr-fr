---
description: Démarrer un travail pour créer un sous-pool à partir d’un pool parent à l’aide des paramètres d’allocation spécifiés.
ms.assetid: 9b09221a-7c4e-4648-a2a8-012df1818c3e
title: Méthode CreateChildResourcePool de la classe CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.CreateChildResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e4e709fd240c849581f6dcd343001a9b1dee7003
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533744"
---
# <a name="createchildresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="6de90-103">Méthode CreateChildResourcePool de la \_ classe CIM ResourcePoolConfigurationService</span><span class="sxs-lookup"><span data-stu-id="6de90-103">CreateChildResourcePool method of the CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="6de90-104">Démarrer un travail pour créer un sous-pool à partir d’un pool parent à l’aide des paramètres d’allocation spécifiés.</span><span class="sxs-lookup"><span data-stu-id="6de90-104">Start a job to create a sub-pool from a parent pool using the specified allocation settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="6de90-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6de90-105">Syntax</span></span>


```mof
uint32 CreateChildResourcePool(
  [in]  string               ElementName,
  [in]  string               Settings[],
  [in]  CIM_ResourcePool REF ParentPool[],
  [out] CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="6de90-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6de90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6de90-107">*ElementName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6de90-107">*ElementName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6de90-108">Nom approprié de l’utilisateur final pour le pool en cours de création.</span><span class="sxs-lookup"><span data-stu-id="6de90-108">A end user relevant name for the pool being created.</span></span> <span data-ttu-id="6de90-109">Si la **valeur est null**, un nom par défaut fourni par le système peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="6de90-109">If **NULL**, then a system supplied default name can be used.</span></span> <span data-ttu-id="6de90-110">La valeur sera stockée dans la propriété **ElementName** de l’élément créé.</span><span class="sxs-lookup"><span data-stu-id="6de90-110">The value will be stored in the **ElementName** property for the created element.</span></span>

</dd> <dt>

<span data-ttu-id="6de90-111">*Paramètres* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6de90-111">*Settings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6de90-112">Chaîne contenant une représentation d’une instance de [**\_ SettingData CIM**](cim-settingdata.md) utilisée pour spécifier les paramètres du pool enfant.</span><span class="sxs-lookup"><span data-stu-id="6de90-112">String containing a representation of a [**CIM\_SettingData**](cim-settingdata.md) instance that is used to specify the settings for the child Pool.</span></span>

</dd> <dt>

<span data-ttu-id="6de90-113">*ParentPool* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6de90-113">*ParentPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6de90-114">[**\_ ResourcePool CIM**](cim-resourcepool.md) à partir duquel créer le nouveau pool.</span><span class="sxs-lookup"><span data-stu-id="6de90-114">A [**CIM\_ResourcePool**](cim-resourcepool.md) from which to create the new Pool.</span></span>

</dd> <dt>

<span data-ttu-id="6de90-115">*Pool* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6de90-115">*Pool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6de90-116">[**\_ ResourcePool CIM**](cim-resourcepool.md) qui fait référence au pool résultant.</span><span class="sxs-lookup"><span data-stu-id="6de90-116">A [**CIM\_ResourcePool**](cim-resourcepool.md) that references the resulting pool.</span></span>

</dd> <dt>

<span data-ttu-id="6de90-117">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6de90-117">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6de90-118">Référence au travail (peut avoir la valeur null si le travail est terminé).</span><span class="sxs-lookup"><span data-stu-id="6de90-118">Reference to the job (may be null if job completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6de90-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6de90-119">Return value</span></span>

<span data-ttu-id="6de90-120">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="6de90-120">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="6de90-121">**Tâche terminée sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="6de90-121">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6de90-122">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="6de90-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6de90-123">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="6de90-123">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6de90-124">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="6de90-124">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6de90-125">**Échec** (4)</span><span class="sxs-lookup"><span data-stu-id="6de90-125">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6de90-126">**Paramètre non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="6de90-126">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="6de90-127">**En cours d’utilisation** (6)</span><span class="sxs-lookup"><span data-stu-id="6de90-127">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="6de90-128">**ResourceType incorrect pour le pool** (7)</span><span class="sxs-lookup"><span data-stu-id="6de90-128">**Incorrect ResourceType for the Pool** (7)</span></span>
</dt> <dt>

<span data-ttu-id="6de90-129">**Ressources insuffisantes** (8)</span><span class="sxs-lookup"><span data-stu-id="6de90-129">**Insufficient Resources** (8)</span></span>
</dt> <dt>

<span data-ttu-id="6de90-130">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="6de90-130">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6de90-131">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="6de90-131">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6de90-132">**Taille non prise en charge** (4097)</span><span class="sxs-lookup"><span data-stu-id="6de90-132">**Size Not Supported** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="6de90-133">**Méthode réservée** (4098.. 32767)</span><span class="sxs-lookup"><span data-stu-id="6de90-133">**Method Reserved** (4098..32767)</span></span>
</dt> <dt>

<span data-ttu-id="6de90-134">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="6de90-134">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6de90-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6de90-135">Requirements</span></span>



| <span data-ttu-id="6de90-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6de90-136">Requirement</span></span> | <span data-ttu-id="6de90-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="6de90-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6de90-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6de90-138">Minimum supported client</span></span><br/> | <span data-ttu-id="6de90-139">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="6de90-139">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="6de90-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6de90-140">Minimum supported server</span></span><br/> | <span data-ttu-id="6de90-141">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="6de90-141">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="6de90-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6de90-142">Namespace</span></span><br/>                | <span data-ttu-id="6de90-143">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="6de90-143">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6de90-144">MOF</span><span class="sxs-lookup"><span data-stu-id="6de90-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6de90-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6de90-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6de90-146">DLL</span><span class="sxs-lookup"><span data-stu-id="6de90-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6de90-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6de90-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6de90-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6de90-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6de90-149">**\_RESOURCEPOOLCONFIGURATIONSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="6de90-149">**CIM\_ResourcePoolConfigurationService**</span></span>](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




