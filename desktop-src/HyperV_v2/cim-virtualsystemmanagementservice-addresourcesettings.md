---
description: Ajoute des ressources à une configuration de système virtuel.
ms.assetid: c2541571-74f0-48f8-997c-56c152980eea
title: Méthode AddResourceSettings de la classe CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.AddResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9563b1e8421dfa6724971450b117780435f6f39e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517643"
---
# <a name="addresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="0bd4a-103">Méthode AddResourceSettings de la \_ classe CIM VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="0bd4a-103">AddResourceSettings method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="0bd4a-104">Ajoute des ressources à une configuration de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="0bd4a-104">Adds resources to a virtual system configuration.</span></span>

<span data-ttu-id="0bd4a-105">En cas d’application à une configuration de système virtuel « État », des ressources d’effet secondaire sont ajoutées au système virtuel actif.</span><span class="sxs-lookup"><span data-stu-id="0bd4a-105">When applied to a "state" virtual system configuration, as a side effect resources are added to the active virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bd4a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0bd4a-106">Syntax</span></span>


```mof
uint32 AddResourceSettings(
  [in]  CIM_VirtualSystemSettingData      REF AffectedConfiguration,
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="0bd4a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0bd4a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bd4a-108">*AffectedConfiguration* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0bd4a-108">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bd4a-109">Référence [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) à la configuration du système virtuel affecté.</span><span class="sxs-lookup"><span data-stu-id="0bd4a-109">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) reference to the affected virtual system configuration.</span></span>

</dd> <dt>

<span data-ttu-id="0bd4a-110">*ResourceSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0bd4a-110">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bd4a-111">Tableau de chaînes contenant chacune une instance incorporée de la classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) qui décrit les aspects virtuels d’une ressource virtuelle à ajouter au système virtuel.</span><span class="sxs-lookup"><span data-stu-id="0bd4a-111">Array of strings each containing one embedded instance of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that describes the virtual aspects of a virtual resource to be added to the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="0bd4a-112">*ResultingResourceSettings* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0bd4a-112">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0bd4a-113">Tableau de références aux instances de la [**classe \_ ResourceAllocationSettingData CIM**](cim-resourceallocationsettingdata.md) représentant les aspects virtuels des ressources virtuelles ajoutées.</span><span class="sxs-lookup"><span data-stu-id="0bd4a-113">Array of references to instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) representing virtual aspects of the added virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="0bd4a-114">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0bd4a-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0bd4a-115">Si l’opération est exécutée à long terme, vous pouvez éventuellement retourner un travail.</span><span class="sxs-lookup"><span data-stu-id="0bd4a-115">If the operation is long running, then optionally a job may be returned.</span></span> <span data-ttu-id="0bd4a-116">Dans ce cas, les instances de la classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) représentant les paramètres de ressource ajoutés sont disponibles par le biais de l’Association **CIM \_ ConreteComponent** à partir de l’instance de la classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) représentant la configuration du système virtuel concerné.</span><span class="sxs-lookup"><span data-stu-id="0bd4a-116">In this case, the instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) representing the added resource settings are available via association **CIM\_ConreteComponent** from the instance of class [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) representing the affected virtual system configuration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bd4a-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0bd4a-117">Return value</span></span>

<span data-ttu-id="0bd4a-118">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="0bd4a-118">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="0bd4a-119">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="0bd4a-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0bd4a-120">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="0bd4a-120">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0bd4a-121">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="0bd4a-121">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0bd4a-122">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="0bd4a-122">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0bd4a-123">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="0bd4a-123">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0bd4a-124">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="0bd4a-124">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0bd4a-125">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="0bd4a-125">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="0bd4a-126">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="0bd4a-126">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="0bd4a-127">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="0bd4a-127">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="0bd4a-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0bd4a-128">Requirements</span></span>



| <span data-ttu-id="0bd4a-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0bd4a-129">Requirement</span></span> | <span data-ttu-id="0bd4a-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="0bd4a-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bd4a-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0bd4a-131">Minimum supported client</span></span><br/> | <span data-ttu-id="0bd4a-132">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0bd4a-132">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="0bd4a-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0bd4a-133">Minimum supported server</span></span><br/> | <span data-ttu-id="0bd4a-134">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="0bd4a-134">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="0bd4a-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0bd4a-135">Namespace</span></span><br/>                | <span data-ttu-id="0bd4a-136">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="0bd4a-136">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0bd4a-137">MOF</span><span class="sxs-lookup"><span data-stu-id="0bd4a-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0bd4a-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0bd4a-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0bd4a-139">DLL</span><span class="sxs-lookup"><span data-stu-id="0bd4a-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0bd4a-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0bd4a-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0bd4a-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0bd4a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bd4a-142">**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="0bd4a-142">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




