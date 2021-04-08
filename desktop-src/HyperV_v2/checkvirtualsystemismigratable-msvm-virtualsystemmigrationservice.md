---
description: Détermine si le système virtuel spécifié peut être migré.
ms.assetid: 1bf1b385-162e-41c9-a408-f7ee755a9646
title: Méthode CheckVirtualSystemIsMigratable de la classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckVirtualSystemIsMigratable
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1aed843f3f0f4c6c30eb6125cdd5859cdba902d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862078"
---
# <a name="checkvirtualsystemismigratable-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="1f138-103">Méthode CheckVirtualSystemIsMigratable de la \_ classe VirtualSystemMigrationService MSVM</span><span class="sxs-lookup"><span data-stu-id="1f138-103">CheckVirtualSystemIsMigratable method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="1f138-104">Détermine si le système virtuel spécifié peut être migré.</span><span class="sxs-lookup"><span data-stu-id="1f138-104">Determines whether the specified virtual system can be migrated.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f138-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f138-105">Syntax</span></span>


```mof
uint32 CheckVirtualSystemIsMigratable(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 DestinationHost,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="1f138-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1f138-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f138-107">*ComputerSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1f138-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f138-108">Référence à une instance de la classe [**CIM \_ CIM**](cim-computersystem.md) qui représente l’ordinateur virtuel pour tester la capacité de migration de.</span><span class="sxs-lookup"><span data-stu-id="1f138-108">A reference to an instance of the [**CIM\_ComputerSystem**](cim-computersystem.md) class that represents the virtual machine to test the migration ability of.</span></span>

</dd> <dt>

<span data-ttu-id="1f138-109">*DestinationHost* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1f138-109">*DestinationHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f138-110">Nom du système hôte pour la migration.</span><span class="sxs-lookup"><span data-stu-id="1f138-110">The name of the host system for the migration.</span></span> <span data-ttu-id="1f138-111">Le format de ce nom est spécifié par la propriété **DestinationHostFormatsSupported** de la [**classe \_ VirtualSystemMigrationCapabilities MSVM**](msvm-virtualsystemmigrationcapabilities.md) associée à cette classe.</span><span class="sxs-lookup"><span data-stu-id="1f138-111">The format of this name is specified by the **DestinationHostFormatsSupported** property of the [**Msvm\_VirtualSystemMigrationCapabilities**](msvm-virtualsystemmigrationcapabilities.md) class associated with this class.</span></span>

</dd> <dt>

<span data-ttu-id="1f138-112">*MigrationSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1f138-112">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f138-113">Une instance incorporée de la classe [**MSVM \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) qui représente les paramètres de l’opération de migration.</span><span class="sxs-lookup"><span data-stu-id="1f138-113">An embedded instance of the [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) class that represents settings for the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="1f138-114">*NewSystemSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1f138-114">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f138-115">Une instance incorporée de la classe [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) qui représente les nouvelles propriétés applicables au système virtuel après sa migration.</span><span class="sxs-lookup"><span data-stu-id="1f138-115">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="1f138-116">*NewResourceSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1f138-116">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f138-117">Tableau de chaînes qui contient une instance incorporée de la classe [**MSVM \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) qui représente les nouvelles propriétés applicables aux ressources virtuelles du système virtuel après qu’il a été migré.</span><span class="sxs-lookup"><span data-stu-id="1f138-117">An array of strings that contain an embedded instance of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that represents the new properties applicable to virtual resources of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="1f138-118">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1f138-118">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f138-119">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1f138-119">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f138-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1f138-120">Return value</span></span>

<span data-ttu-id="1f138-121">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1f138-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="1f138-122">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="1f138-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="1f138-123">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="1f138-123">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="1f138-124">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="1f138-124">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="1f138-125">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="1f138-125">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="1f138-126">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="1f138-126">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="1f138-127">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="1f138-127">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="1f138-128">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="1f138-128">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="1f138-129">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="1f138-129">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="1f138-130">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="1f138-130">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="1f138-131">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="1f138-131">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="1f138-132">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="1f138-132">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="1f138-133">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="1f138-133">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1f138-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f138-134">Requirements</span></span>



| <span data-ttu-id="1f138-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f138-135">Requirement</span></span> | <span data-ttu-id="1f138-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f138-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f138-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f138-137">Minimum supported client</span></span><br/> | <span data-ttu-id="1f138-138">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f138-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1f138-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f138-139">Minimum supported server</span></span><br/> | <span data-ttu-id="1f138-140">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f138-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1f138-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1f138-141">Namespace</span></span><br/>                | <span data-ttu-id="1f138-142">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="1f138-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1f138-143">MOF</span><span class="sxs-lookup"><span data-stu-id="1f138-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1f138-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1f138-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1f138-145">DLL</span><span class="sxs-lookup"><span data-stu-id="1f138-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f138-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1f138-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1f138-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f138-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f138-148">**MSVM \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="1f138-148">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

