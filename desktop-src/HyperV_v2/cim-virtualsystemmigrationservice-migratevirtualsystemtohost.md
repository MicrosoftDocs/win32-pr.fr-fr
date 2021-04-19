---
description: Méthode permettant de déplacer, de migrer ou de déplacer un système virtuel vers un ordinateur hôte cible spécifié par un nom de réseau ou une adresse IP.
ms.assetid: 09fdc0b2-641c-47f5-b270-e26e3acf7ea5
title: Méthode MigrateVirtualSystemToHost de la classe CIM_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.MigrateVirtualSystemToHost
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d1a90e3adadbb5efc5f9cae3b7710e07c1e05000
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106525026"
---
# <a name="migratevirtualsystemtohost-method-of-the-cim_virtualsystemmigrationservice-class"></a><span data-ttu-id="d007b-103">Méthode MigrateVirtualSystemToHost de la \_ classe CIM VirtualSystemMigrationService</span><span class="sxs-lookup"><span data-stu-id="d007b-103">MigrateVirtualSystemToHost method of the CIM\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="d007b-104">Méthode permettant de déplacer, de migrer ou de déplacer un système virtuel vers un ordinateur hôte cible spécifié par un nom de réseau ou une adresse IP.</span><span class="sxs-lookup"><span data-stu-id="d007b-104">Method to move, migrate or relocate a virtual system to a target host specified by a network name or IP address.</span></span>

> [!Note]  
> <span data-ttu-id="d007b-105">Cette méthode est destinée à une solution transitoire uniquement jusqu’à ce que la modélisation de la prise en charge des clusters soit disponible.</span><span class="sxs-lookup"><span data-stu-id="d007b-105">This method is intended as a transitional solution only until modeling of cluster support is available.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d007b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d007b-106">Syntax</span></span>


```mof
uint32 MigrateVirtualSystemToHost(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 DestinationHost,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d007b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d007b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d007b-108">*ComputerSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d007b-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d007b-109">Système d’ordinateur virtuel source à migrer.</span><span class="sxs-lookup"><span data-stu-id="d007b-109">Source virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="d007b-110">*DestinationHost* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d007b-110">*DestinationHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d007b-111">Système hôte cible pour la migration.</span><span class="sxs-lookup"><span data-stu-id="d007b-111">Target host system for the migration.</span></span>

<span data-ttu-id="d007b-112">Les formats acceptables pour ce paramètre sont transmis via les valeurs des éléments de la propriété de tableau **DestinationHostFormatsSupported** \[ \] dans l’instance du [**\_ VirtualSystemMigrationCapabilities CIM**](cim-virtualsystemmigrationcapabilities.md) qui est associée par le biais de l’Association [**CIM \_ ElementCapabilities**](cim-elementcapabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="d007b-112">Acceptable formats for this parameter are conveyed through values of elements of the **DestinationHostFormatsSupported**\[ \] array property in the instance of the [**CIM\_VirtualSystemMigrationCapabilities**](cim-virtualsystemmigrationcapabilities.md) that is associated through the [**CIM\_ElementCapabilities**](cim-elementcapabilities.md) association.</span></span>

</dd> <dt>

<span data-ttu-id="d007b-113">*MigrationSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d007b-113">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d007b-114">Chaîne contenant une instance incorporée de la classe [**CIM \_ VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) représentant les paramètres de migration applicables à l’opération de migration.</span><span class="sxs-lookup"><span data-stu-id="d007b-114">String containing an embedded instance of the [**CIM\_VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) class representing migration settings applicable to the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="d007b-115">*NewSystemSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d007b-115">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d007b-116">Chaîne contenant une instance incorporée de la classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) représentant les nouvelles propriétés applicables au système virtuel après sa migration.</span><span class="sxs-lookup"><span data-stu-id="d007b-116">String containing an embedded instance of the [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) class representing new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="d007b-117">*NewResourceSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d007b-117">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d007b-118">Tableau de chaînes contenant chacune une instance incorporée de la classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) représentant les nouvelles propriétés applicables aux ressources virtuelles dans l’étendue du système virtuel après la migration.</span><span class="sxs-lookup"><span data-stu-id="d007b-118">Array of strings each containing an embedded instance of the [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) class representing new properties applicable to virtual resources in the scope of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="d007b-119">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d007b-119">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d007b-120">Si l’opération est exécutée à long terme, éventuellement [**un \_ ConcreteJob CIM**](cim-concretejob.md) représentant le travail peut être retourné.</span><span class="sxs-lookup"><span data-stu-id="d007b-120">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d007b-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d007b-121">Return value</span></span>

<span data-ttu-id="d007b-122">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="d007b-122">Returns a 0 on success; otherwise, returns an error.</span></span>



| <span data-ttu-id="d007b-123">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="d007b-123">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="d007b-124">Description</span><span class="sxs-lookup"><span data-stu-id="d007b-124">Description</span></span>                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d007b-125"><dt>**Terminé sans erreur**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d007b-125"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="d007b-126">Le système virtuel a été migré.</span><span class="sxs-lookup"><span data-stu-id="d007b-126">Virtual system was migrated.</span></span><br/>                                                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="d007b-127"><dt>**Non pris en charge**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="d007b-127"><dt>**Not Supported**</dt> <dt>1</dt></span></span> </dl>                              | <span data-ttu-id="d007b-128">Méthode non prise en charge par l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="d007b-128">Method not supported by implementation.</span></span><br/>                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="d007b-129"><dt>**Échec**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d007b-129"><dt>**Failed**</dt> <dt>2</dt></span></span> </dl>                                     | <span data-ttu-id="d007b-130">Échec de la migration du système virtuel pour des raisons non spécifiées.</span><span class="sxs-lookup"><span data-stu-id="d007b-130">Virtual system migration failed for unspecified reasons.</span></span><br/>                                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="d007b-131"><dt>**Délai d’expiration**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d007b-131"><dt>**Timeout**</dt> <dt>3</dt></span></span> </dl>                                    | <span data-ttu-id="d007b-132">Délai d’expiration de la migration du système virtuel ; l’état du système virtuel est inconnu.</span><span class="sxs-lookup"><span data-stu-id="d007b-132">Virtual system migration time out; the virtual system state is unknown.</span></span><br/>                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="d007b-133"><dt>**Paramètre non valide**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="d007b-133"><dt>**Invalid Parameter**</dt> <dt>4</dt></span></span> </dl>                          | <span data-ttu-id="d007b-134">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="d007b-134">One or more parameters are formally invalid.</span></span> <span data-ttu-id="d007b-135">Par exemple, la valeur du paramètre *DestinationHost* peut avoir été spécifiée dans un format non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d007b-135">For example, the value of the *DestinationHost* parameter could have been specified in an unsupported format.</span></span><br/>                                                                                                                                    |
| <dl> <span data-ttu-id="d007b-136"><dt>**État non valide**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="d007b-136"><dt>**Invalid State**</dt> <dt>5</dt></span></span> </dl>                              | <span data-ttu-id="d007b-137">Le système virtuel source, le système hôte source ou le système hôte cible sont dans un État qui permet le lancement de la migration du système virtuel demandée ; Il peut s’agir d’une condition temporaire.</span><span class="sxs-lookup"><span data-stu-id="d007b-137">The source virtual system, the source host system or the target host system are in a state that does allow initiation of the requested virtual system migration; this may be a temporary condition.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="d007b-138"><dt>**Paramètres incompatibles**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="d007b-138"><dt>**Incompatible Parameters**</dt> <dt>6</dt></span></span> </dl>                    | <span data-ttu-id="d007b-139">Un ou plusieurs paramètres d’entrée sont incompatibles en tant que jeu ou par rapport à l’hôte cible.</span><span class="sxs-lookup"><span data-stu-id="d007b-139">One or more input parameters are incompatible as a set, or with respect to the target host.</span></span> <span data-ttu-id="d007b-140">Par exemple, la valeur du paramètre *MigrationNewSettingData* contient des propriétés qui ne sont pas prises en charge par le système hôte cible identifié par la valeur du paramètre *DestinationHost* .</span><span class="sxs-lookup"><span data-stu-id="d007b-140">For example the value of the *MigrationNewSettingData* parameter contains properties that are not supported by the target host system identified by the value of the *DestinationHost* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="d007b-141"><dt>**DMTF réservé**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="d007b-141"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>                             |                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="d007b-142"><dt>**Paramètres de méthode activés-travail démarré**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="d007b-142"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="d007b-143"><dt>**Méthode réservée**</dt> <dt>4097.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="d007b-143"><dt>**Method Reserved**</dt> <dt>4097..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="d007b-144"><dt></dt> <dt>32 768.. 65535</dt> spécifiques au fournisseur</span><span class="sxs-lookup"><span data-stu-id="d007b-144"><dt>**Vendor Specific**</dt> <dt>32768..65535</dt></span></span> </dl>                 |                                                                                                                                                                                                                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="d007b-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d007b-145">Requirements</span></span>



| <span data-ttu-id="d007b-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d007b-146">Requirement</span></span> | <span data-ttu-id="d007b-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="d007b-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d007b-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d007b-148">Minimum supported client</span></span><br/> | <span data-ttu-id="d007b-149">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d007b-149">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="d007b-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d007b-150">Minimum supported server</span></span><br/> | <span data-ttu-id="d007b-151">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="d007b-151">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="d007b-152">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d007b-152">Namespace</span></span><br/>                | <span data-ttu-id="d007b-153">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="d007b-153">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d007b-154">MOF</span><span class="sxs-lookup"><span data-stu-id="d007b-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d007b-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d007b-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d007b-156">DLL</span><span class="sxs-lookup"><span data-stu-id="d007b-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d007b-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d007b-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d007b-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d007b-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d007b-159">**\_VIRTUALSYSTEMMIGRATIONSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="d007b-159">**CIM\_VirtualSystemMigrationService**</span></span>](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




