---
description: Modifie les paramètres de ressource virtuelle.
ms.assetid: 4942f167-0e53-4ae2-b973-4a06b636b44a
title: Méthode ModifyResourceSettings de la classe CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.ModifyResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e27729429d02c2412e05344779cc40461dbd9dfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485361"
---
# <a name="modifyresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="c9dd3-103">Méthode ModifyResourceSettings de la \_ classe CIM VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="c9dd3-103">ModifyResourceSettings method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="c9dd3-104">Modifie les paramètres de ressource virtuelle.</span><span class="sxs-lookup"><span data-stu-id="c9dd3-104">Modifies virtual resource settings.</span></span>

<span data-ttu-id="c9dd3-105">En cas d’application à des parties d’une configuration de système virtuel « en cours », les ressources d’effets secondaires du système virtuel actif peuvent être modifiées.</span><span class="sxs-lookup"><span data-stu-id="c9dd3-105">When applied to parts of a "current" virtual system configuration, as a side effect resources of the active virtual system may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9dd3-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9dd3-106">Syntax</span></span>


```mof
uint32 ModifyResourceSettings(
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="c9dd3-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9dd3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9dd3-108">*ResourceSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9dd3-108">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9dd3-109">Tableau de chaînes contenant chacune une instance incorporée de la classe [**\_ ResourceAllocationSettingData CIM**](cim-resourceallocationsettingdata.md) qui décrit les modifications apportées aux aspects virtuels d’une ressource virtuelle existante.</span><span class="sxs-lookup"><span data-stu-id="c9dd3-109">Array of strings each containing an embedded instance of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that describes modifications to the virtual aspects of an existing virtual resource.</span></span> <span data-ttu-id="c9dd3-110">Toutes les instances doivent avoir un **InstanceID** valide afin d’identifier le paramètre de ressource virtuelle à modifier.</span><span class="sxs-lookup"><span data-stu-id="c9dd3-110">All instances must have a valid **InstanceID** in order to identify the virtual resource setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="c9dd3-111">*ResultingResourceSettings* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c9dd3-111">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9dd3-112">Tableau de références aux instances de la [**classe \_ ResourceAllocationSettingData CIM**](cim-resourceallocationsettingdata.md) représentant les aspects virtuels des ressources virtuelles modifiées.</span><span class="sxs-lookup"><span data-stu-id="c9dd3-112">Array of references to instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) representing virtual aspects of the modified virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="c9dd3-113">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c9dd3-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9dd3-114">Si l’opération est exécutée à long terme, le cas échéant, une tâche est retournée.</span><span class="sxs-lookup"><span data-stu-id="c9dd3-114">If the operation is long running, then optionally a job be returned.</span></span> <span data-ttu-id="c9dd3-115">Dans ce cas, les instances de la classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) représentant les paramètres de ressource modifiés sont disponibles via l’Association **CIM \_ ConreteComponent** à partir de l’instance de la classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) représentant la configuration du système virtuel affecté.</span><span class="sxs-lookup"><span data-stu-id="c9dd3-115">In this case, the instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) representing the modified resource settings are available via association **CIM\_ConreteComponent** from the instance of class [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) representing the affected virtual system configuration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9dd3-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c9dd3-116">Return value</span></span>

<span data-ttu-id="c9dd3-117">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="c9dd3-117">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="c9dd3-118">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="c9dd3-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c9dd3-119">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="c9dd3-119">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c9dd3-120">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="c9dd3-120">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c9dd3-121">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="c9dd3-121">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c9dd3-122">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="c9dd3-122">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c9dd3-123">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="c9dd3-123">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c9dd3-124">**Paramètres incompatibles** (6)</span><span class="sxs-lookup"><span data-stu-id="c9dd3-124">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="c9dd3-125">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="c9dd3-125">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c9dd3-126">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="c9dd3-126">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c9dd3-127">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="c9dd3-127">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="c9dd3-128">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="c9dd3-128">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c9dd3-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9dd3-129">Requirements</span></span>



| <span data-ttu-id="c9dd3-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9dd3-130">Requirement</span></span> | <span data-ttu-id="c9dd3-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9dd3-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9dd3-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9dd3-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c9dd3-133">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c9dd3-133">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="c9dd3-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9dd3-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c9dd3-135">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c9dd3-135">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="c9dd3-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c9dd3-136">Namespace</span></span><br/>                | <span data-ttu-id="c9dd3-137">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="c9dd3-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c9dd3-138">MOF</span><span class="sxs-lookup"><span data-stu-id="c9dd3-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9dd3-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c9dd3-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c9dd3-140">DLL</span><span class="sxs-lookup"><span data-stu-id="c9dd3-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9dd3-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c9dd3-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c9dd3-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9dd3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9dd3-143">**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="c9dd3-143">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




