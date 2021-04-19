---
description: 'En savoir plus sur : méthode CheckVirtualSystemIsMigratableToSystem de la classe CIM_VirtualSystemMigrationService'
ms.assetid: d3f7c926-804f-4c7c-8964-a8e464155417
title: Méthode CheckVirtualSystemIsMigratableToSystem de la classe CIM_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: be85c51cb507fea3cea14f1706ffa8f67af06c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544812"
---
# <a name="checkvirtualsystemismigratabletosystem-method-of-the-cim_virtualsystemmigrationservice-class"></a><span data-ttu-id="7e4f7-103">Méthode CheckVirtualSystemIsMigratableToSystem de la \_ classe CIM VirtualSystemMigrationService</span><span class="sxs-lookup"><span data-stu-id="7e4f7-103">CheckVirtualSystemIsMigratableToSystem method of the CIM\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="7e4f7-104">Méthode permettant d’effectuer une vérification préalable pour déterminer si un système virtuel est susceptible d’être migré vers un système cible.</span><span class="sxs-lookup"><span data-stu-id="7e4f7-104">Method to perform a pre-check to determine whether a virtual system is likely to be successfully migrated to a target system.</span></span> <span data-ttu-id="7e4f7-105">Cette méthode ne garantit pas qu’une migration suivante échouera toujours, en raison de la disponibilité dynamique des ressources.</span><span class="sxs-lookup"><span data-stu-id="7e4f7-105">This method does not guarantee that a subsequent migration will always succeed, due to dynamic resource availability.</span></span> <span data-ttu-id="7e4f7-106">Description du code de retour :</span><span class="sxs-lookup"><span data-stu-id="7e4f7-106">Return code description:</span></span>

## <a name="syntax"></a><span data-ttu-id="7e4f7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7e4f7-107">Syntax</span></span>


```mof
uint32 CheckVirtualSystemIsMigratableToSystem(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  CIM_System         REF DestinationSystem,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] boolean                IsMigratable
);
```



## <a name="parameters"></a><span data-ttu-id="7e4f7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7e4f7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e4f7-109">*ComputerSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7e4f7-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e4f7-110">[**CIM \_ Instance ComputerSystem**](cim-computersystem.md) référençant le système d’ordinateur virtuel source à migrer.</span><span class="sxs-lookup"><span data-stu-id="7e4f7-110">[**CIM\_ComputerSystem**](cim-computersystem.md) instance referencing the source virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="7e4f7-111">*DestinationSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7e4f7-111">*DestinationSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e4f7-112">[**CIM \_ Instance système**](cim-system.md) référençant le système de destination sur lequel migrer le système virtuel.</span><span class="sxs-lookup"><span data-stu-id="7e4f7-112">[**CIM\_System**](cim-system.md) instance referencing the destination system onto which to migrate the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="7e4f7-113">*MigrationSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7e4f7-113">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e4f7-114">Chaîne contenant une instance incorporée de la classe [**CIM \_ VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) représentant les paramètres de migration applicables à l’opération de migration.</span><span class="sxs-lookup"><span data-stu-id="7e4f7-114">String containing an embedded instance of the [**CIM\_VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) class representing migration settings applicable to the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="7e4f7-115">*NewSystemSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7e4f7-115">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e4f7-116">Chaîne contenant une instance incorporée de la classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) représentant les nouvelles propriétés applicables au système virtuel après sa migration.</span><span class="sxs-lookup"><span data-stu-id="7e4f7-116">String containing an embedded instance of the [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) class representing new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="7e4f7-117">*NewResourceSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7e4f7-117">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e4f7-118">Tableau de chaînes contenant chacune une instance incorporée de la classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) représentant les nouvelles propriétés applicables aux ressources virtuelles dans l’étendue du système virtuel après la migration.</span><span class="sxs-lookup"><span data-stu-id="7e4f7-118">Array of strings each containing an embedded instance of the [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) class representing new properties applicable to virtual resources in the scope of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="7e4f7-119">*IsMigratable* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7e4f7-119">*IsMigratable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e4f7-120">Résultat de la vérification de la migration indiquant si la migration du système virtuel est réussie ou non.</span><span class="sxs-lookup"><span data-stu-id="7e4f7-120">The migration check result indicating whether or not the virtual system can be successfully migrated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e4f7-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7e4f7-121">Return value</span></span>

<span data-ttu-id="7e4f7-122">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="7e4f7-122">Returns a 0 on success; otherwise, returns an error.</span></span>



| <span data-ttu-id="7e4f7-123">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="7e4f7-123">Return code/value</span></span>                                                                                                                                                | <span data-ttu-id="7e4f7-124">Description</span><span class="sxs-lookup"><span data-stu-id="7e4f7-124">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7e4f7-125"><dt>**Terminé sans erreur**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7e4f7-125"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="7e4f7-126">Vérification effectuée ; résultat signalé par la valeur du \[ paramètre out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="7e4f7-126">Check performed; result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="7e4f7-127"><dt>**Non pris en charge**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7e4f7-127"><dt>**Not Supported**</dt> <dt>1</dt></span></span> </dl>              | <span data-ttu-id="7e4f7-128">Méthode non prise en charge par l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="7e4f7-128">Method not supported by implementation.</span></span> <span data-ttu-id="7e4f7-129">Aucun résultat n’a été signalé par la valeur du \[ paramètre out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="7e4f7-129">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="7e4f7-130"><dt>**Échec**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7e4f7-130"><dt>**Failed**</dt> <dt>2</dt></span></span> </dl>                     | <span data-ttu-id="7e4f7-131">Échec de la vérification pour des raisons non spécifiées.</span><span class="sxs-lookup"><span data-stu-id="7e4f7-131">Check failed for unspecified reasons.</span></span> <span data-ttu-id="7e4f7-132">Aucun résultat n’a été signalé par la valeur du \[ paramètre out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="7e4f7-132">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="7e4f7-133"><dt>**Délai d’expiration**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="7e4f7-133"><dt>**Timeout**</dt> <dt>3</dt></span></span> </dl>                    | <span data-ttu-id="7e4f7-134">Le contrôle a expiré. Aucun résultat n’a été signalé par la valeur du \[ paramètre out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="7e4f7-134">Check timed out. No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="7e4f7-135"><dt>**Paramètre non valide**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="7e4f7-135"><dt>**Invalid Parameter**</dt> <dt>4</dt></span></span> </dl>          | <span data-ttu-id="7e4f7-136">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="7e4f7-136">One or more parameters are formally invalid.</span></span> <span data-ttu-id="7e4f7-137">Par exemple, la valeur du paramètre *DestinationSystem* ne comprend pas de chemin d’accès d’objet valide.</span><span class="sxs-lookup"><span data-stu-id="7e4f7-137">For example, the value of the *DestinationSystem* parameter does not comprise a valid object path.</span></span> <span data-ttu-id="7e4f7-138">Aucun résultat n’a été signalé par la valeur du \[ paramètre out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="7e4f7-138">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                        |
| <dl> <span data-ttu-id="7e4f7-139"><dt>**État non valide**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="7e4f7-139"><dt>**Invalid State**</dt> <dt>5</dt></span></span> </dl>              | <span data-ttu-id="7e4f7-140">Le système virtuel source, le système hôte source ou le système hôte cible sont dans un État qui permet le lancement de la migration du système virtuel demandée ; Il peut s’agir d’une condition temporaire.</span><span class="sxs-lookup"><span data-stu-id="7e4f7-140">The source virtual system, the source host system or the target host system are in a state that does allow initiation of the requested virtual system migration; this may be a temporary condition.</span></span> <span data-ttu-id="7e4f7-141">Aucun résultat n’a été signalé par la valeur du \[ paramètre out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="7e4f7-141">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="7e4f7-142"><dt>**Paramètres incompatibles**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="7e4f7-142"><dt>**Incompatible Parameters**</dt> <dt>6</dt></span></span> </dl>    | <span data-ttu-id="7e4f7-143">Un ou plusieurs paramètres d’entrée sont incompatibles en tant que jeu ou par rapport à l’hôte cible.</span><span class="sxs-lookup"><span data-stu-id="7e4f7-143">One or more input parameters are incompatible as a set, or with respect to the target host.</span></span> <span data-ttu-id="7e4f7-144">Par exemple, la valeur du paramètre *NewSettingData* contient des propriétés qui ne sont pas prises en charge par le système hôte cible identifié par la valeur du paramètre *DestinationSystem* .</span><span class="sxs-lookup"><span data-stu-id="7e4f7-144">For example the value of the *NewSettingData* parameter contains properties that are not supported by the target host system identified by the value of the *DestinationSystem* parameter.</span></span> <span data-ttu-id="7e4f7-145">Aucun résultat n’a été signalé par la valeur du \[ paramètre out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="7e4f7-145">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="7e4f7-146"><dt>**DMTF réservé**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="7e4f7-146"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>             |                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="7e4f7-147"><dt>**Méthode réservée**</dt> <dt>4097.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="7e4f7-147"><dt>**Method Reserved**</dt> <dt>4097..32767</dt></span></span> </dl>  |                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="7e4f7-148"><dt></dt> <dt>32 768.. 65535</dt> spécifiques au fournisseur</span><span class="sxs-lookup"><span data-stu-id="7e4f7-148"><dt>**Vendor Specific**</dt> <dt>32768..65535</dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="7e4f7-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e4f7-149">Requirements</span></span>



| <span data-ttu-id="7e4f7-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e4f7-150">Requirement</span></span> | <span data-ttu-id="7e4f7-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e4f7-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e4f7-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e4f7-152">Minimum supported client</span></span><br/> | <span data-ttu-id="7e4f7-153">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7e4f7-153">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="7e4f7-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e4f7-154">Minimum supported server</span></span><br/> | <span data-ttu-id="7e4f7-155">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7e4f7-155">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="7e4f7-156">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7e4f7-156">Namespace</span></span><br/>                | <span data-ttu-id="7e4f7-157">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="7e4f7-157">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7e4f7-158">MOF</span><span class="sxs-lookup"><span data-stu-id="7e4f7-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e4f7-159"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7e4f7-159"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e4f7-160">DLL</span><span class="sxs-lookup"><span data-stu-id="7e4f7-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e4f7-161"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7e4f7-161"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7e4f7-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e4f7-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e4f7-163">**\_VIRTUALSYSTEMMIGRATIONSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="7e4f7-163">**CIM\_VirtualSystemMigrationService**</span></span>](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




