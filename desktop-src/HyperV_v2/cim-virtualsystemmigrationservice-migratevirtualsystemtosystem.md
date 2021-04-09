---
description: Méthode permettant de déplacer, de migrer ou de déplacer un système virtuel vers un système cible.
ms.assetid: 210d31f1-093f-4fd5-afd7-5f028b4cb343
title: Méthode MigrateVirtualSystemToSystem de la classe CIM_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.MigrateVirtualSystemToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1459d80785725914cbaa5dda5b81e8d2fabad5c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864574"
---
# <a name="migratevirtualsystemtosystem-method-of-the-cim_virtualsystemmigrationservice-class"></a><span data-ttu-id="2ac44-103">Méthode MigrateVirtualSystemToSystem de la \_ classe CIM VirtualSystemMigrationService</span><span class="sxs-lookup"><span data-stu-id="2ac44-103">MigrateVirtualSystemToSystem method of the CIM\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="2ac44-104">Méthode permettant de déplacer, de migrer ou de déplacer un système virtuel vers un système cible.</span><span class="sxs-lookup"><span data-stu-id="2ac44-104">Method to move, migrate or relocate a virtual system to a target system.</span></span>

<span data-ttu-id="2ac44-105">Description du code de retour :</span><span class="sxs-lookup"><span data-stu-id="2ac44-105">Return code description:</span></span>

## <a name="syntax"></a><span data-ttu-id="2ac44-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2ac44-106">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="2ac44-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2ac44-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ac44-108">*ComputerSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ac44-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ac44-109">Système d’ordinateur virtuel source à migrer.</span><span class="sxs-lookup"><span data-stu-id="2ac44-109">Source virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="2ac44-110">*DestinationSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ac44-110">*DestinationSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ac44-111">Le système hôte de destination whereto migrer le système virtuel.</span><span class="sxs-lookup"><span data-stu-id="2ac44-111">Destination host system whereto migrate the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="2ac44-112">*MigrationSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ac44-112">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ac44-113">Chaîne contenant une instance incorporée de la classe [**CIM \_ VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) représentant les paramètres de migration applicables à l’opération de migration.</span><span class="sxs-lookup"><span data-stu-id="2ac44-113">String containing an embedded instance of the [**CIM\_VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) class representing migration settings applicable to the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="2ac44-114">*NewSystemSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ac44-114">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ac44-115">Chaîne contenant une instance incorporée de la classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) représentant les nouvelles propriétés applicables au système virtuel après sa migration.</span><span class="sxs-lookup"><span data-stu-id="2ac44-115">String containing an embedded instance of the [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) class representing new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="2ac44-116">*NewResourceSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ac44-116">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ac44-117">Tableau de chaînes contenant chacune une instance incorporée de la classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) représentant les nouvelles propriétés applicables aux ressources virtuelles dans l’étendue du système virtuel après la migration.</span><span class="sxs-lookup"><span data-stu-id="2ac44-117">Array of strings each containing an embedded instance of the [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) class representing new properties applicable to virtual resources in the scope of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="2ac44-118">*NewComputerSystem* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2ac44-118">*NewComputerSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ac44-119">Référence à une instance de la [**classe \_ CIM CIM**](cim-computersystem.md) représentant le système d’ordinateur virtuel après sa migration.</span><span class="sxs-lookup"><span data-stu-id="2ac44-119">Reference to an instance of the [**CIM\_ComputerSystem**](cim-computersystem.md) class representing the virtual computer system after it has been migrated.</span></span>

</dd> <dt>

<span data-ttu-id="2ac44-120">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2ac44-120">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ac44-121">Si l’opération est exécutée à long terme, éventuellement [**un \_ ConcreteJob CIM**](cim-concretejob.md) représentant le travail peut être retourné.</span><span class="sxs-lookup"><span data-stu-id="2ac44-121">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ac44-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2ac44-122">Return value</span></span>

<span data-ttu-id="2ac44-123">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="2ac44-123">Returns a 0 on success; otherwise, returns an error.</span></span>



| <span data-ttu-id="2ac44-124">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="2ac44-124">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="2ac44-125">Description</span><span class="sxs-lookup"><span data-stu-id="2ac44-125">Description</span></span>                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2ac44-126"><dt>**Terminé sans erreur**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2ac44-126"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="2ac44-127">Le système virtuel a été migré.</span><span class="sxs-lookup"><span data-stu-id="2ac44-127">Virtual system was migrated.</span></span><br/>                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="2ac44-128"><dt>**Non pris en charge**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2ac44-128"><dt>**Not Supported**</dt> <dt>1</dt></span></span> </dl>                              | <span data-ttu-id="2ac44-129">Méthode non prise en charge par l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="2ac44-129">Method not supported by implementation.</span></span><br/>                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="2ac44-130"><dt>**Échec**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2ac44-130"><dt>**Failed**</dt> <dt>2</dt></span></span> </dl>                                     | <span data-ttu-id="2ac44-131">Échec de la migration du système virtuel pour des raisons non spécifiées.</span><span class="sxs-lookup"><span data-stu-id="2ac44-131">Virtual system migration failed for unspecified reasons.</span></span><br/>                                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="2ac44-132"><dt>**Délai d’expiration**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2ac44-132"><dt>**Timeout**</dt> <dt>3</dt></span></span> </dl>                                    | <span data-ttu-id="2ac44-133">Délai d’expiration de la migration du système virtuel ; l’état du système virtuel est inconnu.</span><span class="sxs-lookup"><span data-stu-id="2ac44-133">Virtual system migration time out; the virtual system state is unknown.</span></span><br/>                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="2ac44-134"><dt>**Paramètre non valide**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="2ac44-134"><dt>**Invalid Parameter**</dt> <dt>4</dt></span></span> </dl>                          | <span data-ttu-id="2ac44-135">Un ou plusieurs paramètres ne sont pas valides, par exemple, la valeur du paramètre système de destination ne contient pas de chemin d’accès d’objet valide.</span><span class="sxs-lookup"><span data-stu-id="2ac44-135">One or more parameters are formally invalid For example, the value of the Destination System parameter does not contain a valid object path.</span></span><br/>                                                                                                                                                    |
| <dl> <span data-ttu-id="2ac44-136"><dt>**État non valide**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="2ac44-136"><dt>**Invalid State**</dt> <dt>5</dt></span></span> </dl>                              | <span data-ttu-id="2ac44-137">Le système virtuel source, le système hôte source ou le système hôte cible sont dans un État qui permet le lancement de la migration du système virtuel demandée ; Il peut s’agir d’une condition temporaire.</span><span class="sxs-lookup"><span data-stu-id="2ac44-137">The source virtual system, the source host system or the target host system are in a state that does allow initiation of the requested virtual system migration; this may be a temporary condition.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="2ac44-138"><dt>**Paramètres incompatibles**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="2ac44-138"><dt>**Incompatible Parameters**</dt> <dt>6</dt></span></span> </dl>                    | <span data-ttu-id="2ac44-139">Un ou plusieurs paramètres d’entrée sont incompatibles en tant que jeu ou par rapport à l’hôte cible.</span><span class="sxs-lookup"><span data-stu-id="2ac44-139">One or more input parameters are incompatible as a set, or with respect to the target host.</span></span> <span data-ttu-id="2ac44-140">Par exemple, la valeur du paramètre *MigrationNewSettingData* contient des propriétés qui ne sont pas prises en charge par le système hôte cible identifié par la valeur du paramètre *DestinationSystem* .</span><span class="sxs-lookup"><span data-stu-id="2ac44-140">For example the value of the *MigrationNewSettingData* parameter contains properties that are not supported by the target host system identified by the value of the *DestinationSystem* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="2ac44-141"><dt>**DMTF réservé**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="2ac44-141"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>                             |                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="2ac44-142"><dt>**Paramètres de méthode activés-travail démarré**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="2ac44-142"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="2ac44-143"><dt>**Méthode réservée**</dt> <dt>4097.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="2ac44-143"><dt>**Method Reserved**</dt> <dt>4097..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="2ac44-144"><dt></dt> <dt>32 768.. 65535</dt> spécifiques au fournisseur</span><span class="sxs-lookup"><span data-stu-id="2ac44-144"><dt>**Vendor Specific**</dt> <dt>32768..65535</dt></span></span> </dl>                 |                                                                                                                                                                                                                                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="2ac44-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2ac44-145">Requirements</span></span>



| <span data-ttu-id="2ac44-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2ac44-146">Requirement</span></span> | <span data-ttu-id="2ac44-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ac44-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ac44-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ac44-148">Minimum supported client</span></span><br/> | <span data-ttu-id="2ac44-149">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2ac44-149">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="2ac44-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ac44-150">Minimum supported server</span></span><br/> | <span data-ttu-id="2ac44-151">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="2ac44-151">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="2ac44-152">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2ac44-152">Namespace</span></span><br/>                | <span data-ttu-id="2ac44-153">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="2ac44-153">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2ac44-154">MOF</span><span class="sxs-lookup"><span data-stu-id="2ac44-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2ac44-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2ac44-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2ac44-156">DLL</span><span class="sxs-lookup"><span data-stu-id="2ac44-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ac44-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2ac44-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2ac44-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ac44-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ac44-159">**\_VIRTUALSYSTEMMIGRATIONSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="2ac44-159">**CIM\_VirtualSystemMigrationService**</span></span>](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




