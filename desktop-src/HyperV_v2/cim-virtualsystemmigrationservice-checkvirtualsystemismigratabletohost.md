---
description: Méthode pour effectuer une prévérification afin de déterminer si un système virtuel est susceptible d’être correctement migré vers un ordinateur hôte cible spécifié par un nom de réseau ou une adresse IP.
ms.assetid: bfcd4063-30fe-4d18-9df9-7b84a680814c
title: Méthode CheckVirtualSystemIsMigratableToHost de la classe CIM_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToHost
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5769691a792b8f74225b640b0058ad4bd0e27c3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524618"
---
# <a name="checkvirtualsystemismigratabletohost-method-of-the-cim_virtualsystemmigrationservice-class"></a><span data-ttu-id="1e2dd-103">Méthode CheckVirtualSystemIsMigratableToHost de la \_ classe CIM VirtualSystemMigrationService</span><span class="sxs-lookup"><span data-stu-id="1e2dd-103">CheckVirtualSystemIsMigratableToHost method of the CIM\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="1e2dd-104">Méthode pour effectuer une prévérification afin de déterminer si un système virtuel est susceptible d’être correctement migré vers un ordinateur hôte cible spécifié par un nom de réseau ou une adresse IP.</span><span class="sxs-lookup"><span data-stu-id="1e2dd-104">Method to perform a pre-check to determine whether a virtual system is likely to be successfully migrated to a target host specified by a network name or IP address.</span></span> <span data-ttu-id="1e2dd-105">Cette méthode ne garantit pas qu’une migration suivante échouera toujours, en raison de la disponibilité dynamique des ressources.</span><span class="sxs-lookup"><span data-stu-id="1e2dd-105">This method does not guarantee that a subsequent migration will always succeed, due to dynamic resource availability.</span></span>

<span data-ttu-id="1e2dd-106">Description du code de retour :</span><span class="sxs-lookup"><span data-stu-id="1e2dd-106">Return code description:</span></span>

<span data-ttu-id="1e2dd-107">Remarque : cette méthode est destinée à une solution transitoire uniquement jusqu’à ce que la modélisation de la prise en charge des clusters soit disponible.</span><span class="sxs-lookup"><span data-stu-id="1e2dd-107">Note: This method is intended as a transitional solution only until modeling of cluster support is available.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e2dd-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e2dd-108">Syntax</span></span>


```mof
uint32 CheckVirtualSystemIsMigratableToHost(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 DestinationHost,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] boolean                IsMigratable
);
```



## <a name="parameters"></a><span data-ttu-id="1e2dd-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e2dd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e2dd-110">*ComputerSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e2dd-110">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e2dd-111">Référence [**CIM \_ CIM**](cim-computersystem.md) au système d’ordinateur virtuel source à migrer.</span><span class="sxs-lookup"><span data-stu-id="1e2dd-111">A [**CIM\_ComputerSystem**](cim-computersystem.md) reference to the source virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="1e2dd-112">*DestinationHost* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e2dd-112">*DestinationHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e2dd-113">Système hôte cible pour la migration.</span><span class="sxs-lookup"><span data-stu-id="1e2dd-113">Target host system for the migration.</span></span>

<span data-ttu-id="1e2dd-114">Les formats acceptables pour ce paramètre sont transmis via les valeurs des éléments de la propriété de tableau **DestinationHostFormatsSupported** \[ \] dans l’instance du [**\_ VirtualSystemMigrationCapabilities CIM**](cim-virtualsystemmigrationcapabilities.md) qui est associée par le biais de l’Association [**CIM \_ ElementCapabilities**](cim-elementcapabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="1e2dd-114">Acceptable formats for this parameter are conveyed through values of elements of the **DestinationHostFormatsSupported**\[ \] array property in the instance of the [**CIM\_VirtualSystemMigrationCapabilities**](cim-virtualsystemmigrationcapabilities.md) that is associated through the [**CIM\_ElementCapabilities**](cim-elementcapabilities.md) association.</span></span>

</dd> <dt>

<span data-ttu-id="1e2dd-115">*MigrationSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e2dd-115">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e2dd-116">Chaîne contenant une instance incorporée de la classe [**CIM \_ VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) représentant les paramètres de migration applicables à l’opération de migration.</span><span class="sxs-lookup"><span data-stu-id="1e2dd-116">String containing an embedded instance of the [**CIM\_VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) class representing migration settings applicable to the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="1e2dd-117">*NewSystemSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e2dd-117">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e2dd-118">Chaîne contenant une instance incorporée de la classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) représentant les nouvelles propriétés applicables au système virtuel après sa migration.</span><span class="sxs-lookup"><span data-stu-id="1e2dd-118">String containing an embedded instance of the [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) class representing new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="1e2dd-119">*NewResourceSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e2dd-119">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e2dd-120">Tableau de chaînes contenant chacune une instance incorporée de la classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) représentant les nouvelles propriétés applicables aux ressources virtuelles dans l’étendue du système virtuel après la migration.</span><span class="sxs-lookup"><span data-stu-id="1e2dd-120">Array of strings each containing an embedded instance of the [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) class representing new properties applicable to virtual resources in the scope of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="1e2dd-121">*IsMigratable* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1e2dd-121">*IsMigratable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e2dd-122">Résultat de la vérification de la migration indiquant si la migration du système virtuel est réussie ou non.</span><span class="sxs-lookup"><span data-stu-id="1e2dd-122">The migration check result indicating whether or not the virtual system can be successfully migrated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e2dd-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1e2dd-123">Return value</span></span>

<span data-ttu-id="1e2dd-124">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="1e2dd-124">Returns a 0 on success; otherwise, returns an error.</span></span>



| <span data-ttu-id="1e2dd-125">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="1e2dd-125">Return code/value</span></span>                                                                                                                                                | <span data-ttu-id="1e2dd-126">Description</span><span class="sxs-lookup"><span data-stu-id="1e2dd-126">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1e2dd-127"><dt>**Terminé sans erreur**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1e2dd-127"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="1e2dd-128">Vérification effectuée ; résultat signalé par la valeur du \[ paramètre out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="1e2dd-128">Check performed; result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="1e2dd-129"><dt>**Non pris en charge**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="1e2dd-129"><dt>**Not Supported**</dt> <dt>1</dt></span></span> </dl>              | <span data-ttu-id="1e2dd-130">Méthode non prise en charge par l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="1e2dd-130">Method not supported by implementation.</span></span> <span data-ttu-id="1e2dd-131">Aucun résultat n’a été signalé par la valeur du \[ paramètre out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="1e2dd-131">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="1e2dd-132"><dt>**Échec**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1e2dd-132"><dt>**Failed**</dt> <dt>2</dt></span></span> </dl>                     | <span data-ttu-id="1e2dd-133">Échec de la vérification pour des raisons non spécifiées.</span><span class="sxs-lookup"><span data-stu-id="1e2dd-133">Check failed for unspecified reasons.</span></span> <span data-ttu-id="1e2dd-134">Aucun résultat n’a été signalé par la valeur du \[ paramètre out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="1e2dd-134">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="1e2dd-135"><dt>**Délai d’expiration**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="1e2dd-135"><dt>**Timeout**</dt> <dt>3</dt></span></span> </dl>                    | <span data-ttu-id="1e2dd-136">Le contrôle a expiré. Aucun résultat n’a été signalé par la valeur du \[ paramètre out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="1e2dd-136">Check timed out. No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="1e2dd-137"><dt>**Paramètre non valide**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="1e2dd-137"><dt>**Invalid Parameter**</dt> <dt>4</dt></span></span> </dl>          | <span data-ttu-id="1e2dd-138">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="1e2dd-138">One or more parameters are formally invalid.</span></span> <span data-ttu-id="1e2dd-139">Par exemple, la valeur du paramètre *DestinationHost* peut avoir été spécifiée dans un format non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="1e2dd-139">For example, the value of the *DestinationHost* parameter could have been specified in an unsupported format.</span></span> <span data-ttu-id="1e2dd-140">Aucun résultat n’a été signalé par la valeur du \[ paramètre out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="1e2dd-140">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                    |
| <dl> <span data-ttu-id="1e2dd-141"><dt>**État non valide**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="1e2dd-141"><dt>**Invalid State**</dt> <dt>5</dt></span></span> </dl>              | <span data-ttu-id="1e2dd-142">Le système virtuel source, le système hôte source ou le système hôte cible sont dans un État qui permet le lancement de la migration du système virtuel demandée ; Il peut s’agir d’une condition temporaire.</span><span class="sxs-lookup"><span data-stu-id="1e2dd-142">The source virtual system, the source host system or the target host system are in a state that does allow initiation of the requested virtual system migration; this may be a temporary condition.</span></span> <span data-ttu-id="1e2dd-143">Aucun résultat n’a été signalé par la valeur du \[ paramètre out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="1e2dd-143">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="1e2dd-144"><dt>**Paramètres incompatibles**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="1e2dd-144"><dt>**Incompatible Parameters**</dt> <dt>6</dt></span></span> </dl>    | <span data-ttu-id="1e2dd-145">Un ou plusieurs paramètres d’entrée sont incompatibles en tant que jeu ou par rapport à l’hôte cible.</span><span class="sxs-lookup"><span data-stu-id="1e2dd-145">One or more input parameters are incompatible as a set, or with respect to the target host.</span></span> <span data-ttu-id="1e2dd-146">Par exemple, la valeur du paramètre *MigrationNewSettingData* contient des propriétés qui ne sont pas prises en charge par le système hôte cible identifié par la valeur du paramètre *DestinationHost* .</span><span class="sxs-lookup"><span data-stu-id="1e2dd-146">For example the value of the *MigrationNewSettingData* parameter contains properties that are not supported by the target host system identified by the value of the *DestinationHost* parameter.</span></span> <span data-ttu-id="1e2dd-147">Aucun résultat n’a été signalé par la valeur du \[ paramètre out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="1e2dd-147">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="1e2dd-148"><dt>**DMTF réservé**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="1e2dd-148"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>             |                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="1e2dd-149"><dt>**Méthode réservée**</dt> <dt>4097.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="1e2dd-149"><dt>**Method Reserved**</dt> <dt>4097..32767</dt></span></span> </dl>  |                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="1e2dd-150"><dt></dt> <dt>32 768.. 65535</dt> spécifiques au fournisseur</span><span class="sxs-lookup"><span data-stu-id="1e2dd-150"><dt>**Vendor Specific**</dt> <dt>32768..65535</dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="requirements"></a><span data-ttu-id="1e2dd-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e2dd-151">Requirements</span></span>



| <span data-ttu-id="1e2dd-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e2dd-152">Requirement</span></span> | <span data-ttu-id="1e2dd-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e2dd-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e2dd-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e2dd-154">Minimum supported client</span></span><br/> | <span data-ttu-id="1e2dd-155">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="1e2dd-155">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="1e2dd-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e2dd-156">Minimum supported server</span></span><br/> | <span data-ttu-id="1e2dd-157">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="1e2dd-157">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="1e2dd-158">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1e2dd-158">Namespace</span></span><br/>                | <span data-ttu-id="1e2dd-159">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="1e2dd-159">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1e2dd-160">MOF</span><span class="sxs-lookup"><span data-stu-id="1e2dd-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e2dd-161"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1e2dd-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1e2dd-162">DLL</span><span class="sxs-lookup"><span data-stu-id="1e2dd-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e2dd-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1e2dd-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1e2dd-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e2dd-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e2dd-165">**\_VIRTUALSYSTEMMIGRATIONSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="1e2dd-165">**CIM\_VirtualSystemMigrationService**</span></span>](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




