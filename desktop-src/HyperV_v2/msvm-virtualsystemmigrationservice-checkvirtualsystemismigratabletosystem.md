---
description: Détermine si le système virtuel spécifié peut être migré vers un système de destination.
ms.assetid: 2E340737-DEE9-4853-ACD8-BEE2A8C69D6D
title: Méthode CheckVirtualSystemIsMigratableToSystem de la classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3e8f294f7e30740e3afab8987c734dbbdbd12acf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514986"
---
# <a name="checkvirtualsystemismigratabletosystem-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="d3549-103">Méthode CheckVirtualSystemIsMigratableToSystem de la \_ classe VirtualSystemMigrationService MSVM</span><span class="sxs-lookup"><span data-stu-id="d3549-103">CheckVirtualSystemIsMigratableToSystem method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="d3549-104">Détermine si le système virtuel spécifié peut être migré vers un système de destination.</span><span class="sxs-lookup"><span data-stu-id="d3549-104">Determines whether the specified virtual system can be migrated to a destination system.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3549-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d3549-105">Syntax</span></span>


```mof
uint32 CheckVirtualSystemIsMigratableToSystem(
  [in]  Msvm_ComputerSystem REF ComputerSystem,
  [in]  Msvm_ComputerSystem REF DestinationSystem,
  [in]  string                  MigrationSettingData,
  [in]  string                  NewSystemSettingData,
  [in]  string                  NewResourceSettingData[],
  [out] boolean                 IsMigratable
);
```



## <a name="parameters"></a><span data-ttu-id="d3549-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d3549-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3549-107">*ComputerSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d3549-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3549-108">Référence à une instance de la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) qui représente l’ordinateur virtuel pour tester la capacité de migration de.</span><span class="sxs-lookup"><span data-stu-id="d3549-108">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine to test the migration ability of.</span></span>

</dd> <dt>

<span data-ttu-id="d3549-109">*DestinationSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d3549-109">*DestinationSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3549-110">Référence à une instance de la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) qui représente l’ordinateur virtuel pour tester la fonctionnalité de migration.</span><span class="sxs-lookup"><span data-stu-id="d3549-110">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine to test the migration ability to.</span></span>

</dd> <dt>

<span data-ttu-id="d3549-111">*MigrationSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d3549-111">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3549-112">Une instance incorporée de la classe [**MSVM \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) qui représente les paramètres de l’opération de migration.</span><span class="sxs-lookup"><span data-stu-id="d3549-112">An embedded instance of the [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) class that represents settings for the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="d3549-113">*NewSystemSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d3549-113">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3549-114">Une instance incorporée de la classe [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) qui représente les nouvelles propriétés applicables au système virtuel après sa migration.</span><span class="sxs-lookup"><span data-stu-id="d3549-114">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="d3549-115">*NewResourceSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d3549-115">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3549-116">Tableau de chaînes qui contient une instance incorporée de la classe [**MSVM \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) qui représente les nouvelles propriétés applicables aux ressources virtuelles du système virtuel après qu’il a été migré.</span><span class="sxs-lookup"><span data-stu-id="d3549-116">An array of strings that contain an embedded instance of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that represents the new properties applicable to virtual resources of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="d3549-117">*IsMigratable* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d3549-117">*IsMigratable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3549-118">Reçoit le résultat de la vérification de la migration indiquant si la migration du système virtuel est réussie.</span><span class="sxs-lookup"><span data-stu-id="d3549-118">Receives the migration check result indicating whether the virtual system can be successfully migrated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3549-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d3549-119">Return value</span></span>

<span data-ttu-id="d3549-120">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="d3549-120">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="d3549-121">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="d3549-121">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d3549-122">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="d3549-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d3549-123">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="d3549-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d3549-124">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="d3549-124">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d3549-125">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="d3549-125">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d3549-126">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="d3549-126">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d3549-127">**Paramètres incompatibles** (6)</span><span class="sxs-lookup"><span data-stu-id="d3549-127">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d3549-128">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="d3549-128">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d3549-129">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="d3549-129">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="d3549-130">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="d3549-130">**Vendor Specific** (32768..65535 )</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d3549-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d3549-131">Requirements</span></span>



| <span data-ttu-id="d3549-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d3549-132">Requirement</span></span> | <span data-ttu-id="d3549-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3549-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3549-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3549-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d3549-135">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d3549-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="d3549-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3549-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d3549-137">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d3549-137">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d3549-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d3549-138">Namespace</span></span><br/>                | <span data-ttu-id="d3549-139">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="d3549-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d3549-140">MOF</span><span class="sxs-lookup"><span data-stu-id="d3549-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d3549-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d3549-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d3549-142">DLL</span><span class="sxs-lookup"><span data-stu-id="d3549-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3549-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d3549-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d3549-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3549-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3549-145">**MSVM \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="d3549-145">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




