---
description: Déplace, migre ou déplace un système virtuel vers un système cible.
ms.assetid: 3a0be791-4514-4ce2-b4e8-3735bd6ea1d7
title: Méthode MigrateVirtualSystemToSystem de la classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.MigrateVirtualSystemToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a346596b094b60456af8e2b63865bec1171d99ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318965"
---
# <a name="migratevirtualsystemtosystem-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="64d35-103">Méthode MigrateVirtualSystemToSystem de la \_ classe VirtualSystemMigrationService MSVM</span><span class="sxs-lookup"><span data-stu-id="64d35-103">MigrateVirtualSystemToSystem method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="64d35-104">Déplace, migre ou déplace un système virtuel vers un système cible.</span><span class="sxs-lookup"><span data-stu-id="64d35-104">Moves, migrates, or relocates a virtual system to a target system.</span></span>

## <a name="syntax"></a><span data-ttu-id="64d35-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="64d35-105">Syntax</span></span>


```mof
uint32 MigrateVirtualSystemToSystem(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  CIM_System         REF DestinationSystem,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] CIM_ComputerSystem REF NewComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="64d35-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="64d35-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64d35-107">*ComputerSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="64d35-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64d35-108">Référence à une instance de la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) qui représente le système d’ordinateur virtuel à migrer.</span><span class="sxs-lookup"><span data-stu-id="64d35-108">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="64d35-109">*DestinationSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="64d35-109">*DestinationSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64d35-110">Référence à une instance de la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) qui représente le système à migrer vers.</span><span class="sxs-lookup"><span data-stu-id="64d35-110">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the system to be migrated to.</span></span>

</dd> <dt>

<span data-ttu-id="64d35-111">*MigrationSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="64d35-111">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64d35-112">Une instance incorporée de la classe [**MSVM \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) qui représente les paramètres de l’opération de migration.</span><span class="sxs-lookup"><span data-stu-id="64d35-112">An embedded instance of the [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) class that represents settings for the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="64d35-113">*NewSystemSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="64d35-113">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64d35-114">Une instance incorporée de la classe [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) qui représente les nouvelles propriétés applicables au système virtuel après sa migration.</span><span class="sxs-lookup"><span data-stu-id="64d35-114">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="64d35-115">*NewResourceSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="64d35-115">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64d35-116">Tableau de chaînes qui contient une instance incorporée de la classe [**MSVM \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) qui représente les nouvelles propriétés applicables aux ressources virtuelles du système virtuel après qu’il a été migré.</span><span class="sxs-lookup"><span data-stu-id="64d35-116">An array of strings that contain an embedded instance of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that represents the new properties applicable to virtual resources of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="64d35-117">*NewComputerSystem* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="64d35-117">*NewComputerSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64d35-118">Référence à une instance de la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) qui représente le nouveau système migré.</span><span class="sxs-lookup"><span data-stu-id="64d35-118">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the new migrated system.</span></span>

</dd> <dt>

<span data-ttu-id="64d35-119">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="64d35-119">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64d35-120">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="64d35-120">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64d35-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="64d35-121">Return value</span></span>

<span data-ttu-id="64d35-122">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="64d35-122">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="64d35-123">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="64d35-123">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="64d35-124">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="64d35-124">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="64d35-125">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="64d35-125">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="64d35-126">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="64d35-126">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="64d35-127">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="64d35-127">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="64d35-128">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="64d35-128">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="64d35-129">**Paramètres incompatibles** (6)</span><span class="sxs-lookup"><span data-stu-id="64d35-129">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="64d35-130">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="64d35-130">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="64d35-131">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="64d35-131">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="64d35-132">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="64d35-132">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="64d35-133">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="64d35-133">**Vendor Specific** (32768..65535 )</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="64d35-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64d35-134">Requirements</span></span>



| <span data-ttu-id="64d35-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="64d35-135">Requirement</span></span> | <span data-ttu-id="64d35-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="64d35-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64d35-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="64d35-137">Minimum supported client</span></span><br/> | <span data-ttu-id="64d35-138">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="64d35-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="64d35-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="64d35-139">Minimum supported server</span></span><br/> | <span data-ttu-id="64d35-140">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="64d35-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="64d35-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="64d35-141">Namespace</span></span><br/>                | <span data-ttu-id="64d35-142">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="64d35-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="64d35-143">MOF</span><span class="sxs-lookup"><span data-stu-id="64d35-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64d35-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="64d35-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="64d35-145">DLL</span><span class="sxs-lookup"><span data-stu-id="64d35-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64d35-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="64d35-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="64d35-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64d35-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64d35-148">**MSVM \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="64d35-148">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

