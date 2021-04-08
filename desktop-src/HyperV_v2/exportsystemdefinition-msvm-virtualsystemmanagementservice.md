---
description: Exporte un ordinateur virtuel, ou un instantané d’un ordinateur virtuel, vers un fichier.
ms.assetid: b88712e4-a1a6-4188-8082-f4973f89018d
title: Méthode ExportSystemDefinition de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ExportSystemDefinition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9f6b6dc5728a4275965ccd482d851601ecd1c6e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749637"
---
# <a name="exportsystemdefinition-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="62fa6-103">Méthode ExportSystemDefinition de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="62fa6-103">ExportSystemDefinition method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="62fa6-104">Exporte un ordinateur virtuel, ou un instantané d’un ordinateur virtuel, vers un fichier.</span><span class="sxs-lookup"><span data-stu-id="62fa6-104">Exports a virtual machine, or a snapshot of a virtual machine, to a file.</span></span> <span data-ttu-id="62fa6-105">L’ordinateur virtuel doit être dans l’état « hors tension » ou « enregistré » pour être exporté.</span><span class="sxs-lookup"><span data-stu-id="62fa6-105">The virtual machine must be in the "powered off" or "saved" state to be exported.</span></span> <span data-ttu-id="62fa6-106">L’ordinateur virtuel, ses paramètres de configuration associés et les paramètres de ressources qui lui sont associés sont conservés dans le fichier résultant.</span><span class="sxs-lookup"><span data-stu-id="62fa6-106">The virtual machine, its associated configuration settings, and its associated resource settings will be preserved in the resulting file.</span></span>

## <a name="syntax"></a><span data-ttu-id="62fa6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62fa6-107">Syntax</span></span>


```mof
uint32 ExportSystemDefinition(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ExportDirectory,
  [in]  string                 ExportSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="62fa6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="62fa6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62fa6-109">*ComputerSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="62fa6-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62fa6-110">Référence à un [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente l’ordinateur virtuel à exporter.</span><span class="sxs-lookup"><span data-stu-id="62fa6-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) that represents the virtual machine to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="62fa6-111">*ExportDirectory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="62fa6-111">*ExportDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62fa6-112">Chemin d’accès complet du répertoire dans lequel l’ordinateur virtuel doit être exporté.</span><span class="sxs-lookup"><span data-stu-id="62fa6-112">The fully qualified path of the directory to which the virtual machine is to be exported.</span></span> <span data-ttu-id="62fa6-113">Si la propriété **CreateVmExportSubdirectory** de la [**classe \_ VirtualSystemExportSettingData MSVM**](msvm-virtualsystemexportsettingdata.md) dans le paramètre *ExportSettingData* est définie sur **true**, ce répertoire peut être réutilisé pour l’exportation de plusieurs ordinateurs virtuels et cette méthode place chaque définition d’ordinateur virtuel dans un sous-répertoire distinct sous ce chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="62fa6-113">If the **CreateVmExportSubdirectory** property of the [**Msvm\_VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) class in the *ExportSettingData* parameter is set to **True**, then this directory can be reused for exporting multiple virtual machines and this method places each virtual machine definition in a separate subdirectory under this path.</span></span>

</dd> <dt>

<span data-ttu-id="62fa6-114">*ExportSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="62fa6-114">*ExportSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62fa6-115">Instance incorporée de la classe [**MSVM \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) qui représente les paramètres de l’opération d’exportation.</span><span class="sxs-lookup"><span data-stu-id="62fa6-115">An embedded instance of the [**Msvm\_VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) class that represents the settings for the export operation.</span></span>

</dd> <dt>

<span data-ttu-id="62fa6-116">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="62fa6-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="62fa6-117">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="62fa6-117">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62fa6-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="62fa6-118">Return value</span></span>

<span data-ttu-id="62fa6-119">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="62fa6-119">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="62fa6-120">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="62fa6-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="62fa6-121">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="62fa6-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="62fa6-122">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="62fa6-122">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="62fa6-123">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="62fa6-123">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="62fa6-124">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="62fa6-124">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="62fa6-125">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="62fa6-125">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="62fa6-126">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="62fa6-126">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="62fa6-127">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="62fa6-127">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="62fa6-128">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="62fa6-128">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="62fa6-129">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="62fa6-129">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="62fa6-130">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="62fa6-130">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="62fa6-131">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="62fa6-131">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="62fa6-132">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="62fa6-132">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="62fa6-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="62fa6-133">Requirements</span></span>



| <span data-ttu-id="62fa6-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="62fa6-134">Requirement</span></span> | <span data-ttu-id="62fa6-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="62fa6-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62fa6-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62fa6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="62fa6-137">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="62fa6-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="62fa6-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62fa6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="62fa6-139">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="62fa6-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="62fa6-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="62fa6-140">Namespace</span></span><br/>                | <span data-ttu-id="62fa6-141">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="62fa6-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="62fa6-142">MOF</span><span class="sxs-lookup"><span data-stu-id="62fa6-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62fa6-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="62fa6-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="62fa6-144">DLL</span><span class="sxs-lookup"><span data-stu-id="62fa6-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62fa6-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="62fa6-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="62fa6-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62fa6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62fa6-147">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="62fa6-147">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

