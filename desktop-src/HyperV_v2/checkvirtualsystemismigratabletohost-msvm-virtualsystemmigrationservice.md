---
description: Détermine si le système virtuel spécifié peut être migré vers un ordinateur hôte cible spécifié par un nom de réseau ou une adresse IP.
ms.assetid: eacc8448-4683-48df-81b9-8599292944db
title: Méthode CheckVirtualSystemIsMigratableToHost de la classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToHost
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b81f6562f892acbaa5bf7ff7f4f3c772574bd96d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518191"
---
# <a name="checkvirtualsystemismigratabletohost-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="7681d-103">Méthode CheckVirtualSystemIsMigratableToHost de la \_ classe VirtualSystemMigrationService MSVM</span><span class="sxs-lookup"><span data-stu-id="7681d-103">CheckVirtualSystemIsMigratableToHost method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="7681d-104">Détermine si le système virtuel spécifié peut être migré vers un ordinateur hôte cible spécifié par un nom de réseau ou une adresse IP.</span><span class="sxs-lookup"><span data-stu-id="7681d-104">Determines whether the specified virtual system can be migrated to a target host specified by a network name or IP address.</span></span>

## <a name="syntax"></a><span data-ttu-id="7681d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7681d-105">Syntax</span></span>


```mof
uint32 CheckVirtualSystemIsMigratableToHost(
  [in]  Msvm_ComputerSystem REF ComputerSystem,
  [in]  string                  DestinationHost,
  [in]  string                  MigrationSettingData,
  [in]  string                  NewSystemSettingData,
  [in]  string                  NewResourceSettingData[],
  [out] boolean                 IsMigratable
);
```



## <a name="parameters"></a><span data-ttu-id="7681d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7681d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7681d-107">*ComputerSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7681d-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7681d-108">Référence à une instance de la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) qui représente l’ordinateur virtuel pour tester la capacité de migration de.</span><span class="sxs-lookup"><span data-stu-id="7681d-108">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine to test the migration ability of.</span></span>

</dd> <dt>

<span data-ttu-id="7681d-109">*DestinationHost* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7681d-109">*DestinationHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7681d-110">Nom du système hôte pour la migration.</span><span class="sxs-lookup"><span data-stu-id="7681d-110">The name of the host system for the migration.</span></span> <span data-ttu-id="7681d-111">Le format de ce nom est spécifié par la propriété **DestinationHostFormatsSupported** de la [**classe \_ VirtualSystemMigrationCapabilities MSVM**](msvm-virtualsystemmigrationcapabilities.md) associée à cette classe.</span><span class="sxs-lookup"><span data-stu-id="7681d-111">The format of this name is specified by the **DestinationHostFormatsSupported** property of the [**Msvm\_VirtualSystemMigrationCapabilities**](msvm-virtualsystemmigrationcapabilities.md) class associated with this class.</span></span>

</dd> <dt>

<span data-ttu-id="7681d-112">*MigrationSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7681d-112">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7681d-113">Une instance incorporée de la classe [**MSVM \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) qui représente les paramètres de l’opération de migration.</span><span class="sxs-lookup"><span data-stu-id="7681d-113">An embedded instance of the [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) class that represents settings for the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="7681d-114">*NewSystemSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7681d-114">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7681d-115">Une instance incorporée de la classe [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) qui représente les nouvelles propriétés applicables au système virtuel après sa migration.</span><span class="sxs-lookup"><span data-stu-id="7681d-115">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="7681d-116">*NewResourceSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7681d-116">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7681d-117">Tableau de chaînes qui contient une instance incorporée de la classe [**MSVM \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) qui représente les nouvelles propriétés applicables aux ressources virtuelles du système virtuel après qu’il a été migré.</span><span class="sxs-lookup"><span data-stu-id="7681d-117">An array of strings that contain an embedded instance of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that represents the new properties applicable to virtual resources of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="7681d-118">*IsMigratable* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7681d-118">*IsMigratable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7681d-119">Reçoit le résultat de la vérification de la migration indiquant si la migration du système virtuel est réussie.</span><span class="sxs-lookup"><span data-stu-id="7681d-119">Receives the migration check result indicating whether the virtual system can be successfully migrated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7681d-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7681d-120">Return value</span></span>

<span data-ttu-id="7681d-121">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="7681d-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="7681d-122">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="7681d-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7681d-123">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="7681d-123">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7681d-124">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="7681d-124">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7681d-125">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="7681d-125">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7681d-126">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="7681d-126">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7681d-127">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="7681d-127">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7681d-128">**Paramètres incompatibles** (6)</span><span class="sxs-lookup"><span data-stu-id="7681d-128">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="7681d-129">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="7681d-129">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7681d-130">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="7681d-130">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="7681d-131">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="7681d-131">**Vendor Specific** (32768..65535 )</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="7681d-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7681d-132">Requirements</span></span>



| <span data-ttu-id="7681d-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7681d-133">Requirement</span></span> | <span data-ttu-id="7681d-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="7681d-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7681d-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7681d-135">Minimum supported client</span></span><br/> | <span data-ttu-id="7681d-136">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7681d-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7681d-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7681d-137">Minimum supported server</span></span><br/> | <span data-ttu-id="7681d-138">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7681d-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7681d-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7681d-139">Namespace</span></span><br/>                | <span data-ttu-id="7681d-140">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="7681d-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7681d-141">MOF</span><span class="sxs-lookup"><span data-stu-id="7681d-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7681d-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7681d-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7681d-143">DLL</span><span class="sxs-lookup"><span data-stu-id="7681d-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7681d-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7681d-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7681d-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7681d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7681d-146">**MSVM \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="7681d-146">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




