---
description: Valide la configuration d’un ordinateur virtuel planifié et le convertit en ordinateur virtuel réalisé.
ms.assetid: bddbdc35-4603-45c3-96b4-04f445dbb3a6
title: Méthode RealizePlannedSystem de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RealizePlannedSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fc69cbc9be9fc72bc7c1184ec30d9e2b58ba2b6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210060"
---
# <a name="realizeplannedsystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="6b64a-103">Méthode RealizePlannedSystem de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="6b64a-103">RealizePlannedSystem method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="6b64a-104">Valide la configuration d’un ordinateur virtuel planifié et le convertit en ordinateur virtuel réalisé.</span><span class="sxs-lookup"><span data-stu-id="6b64a-104">Validates the configuration of a planned virtual machine and converts it to a realized virtual machine.</span></span> <span data-ttu-id="6b64a-105">Les fichiers d’État du runtime ou de l’état enregistré associés à l’ordinateur virtuel seront copiés du répertoire d’importation vers la racine des données de l’ordinateur virtuel, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="6b64a-105">Any runtime or saved state files associated with the virtual machine will be copied from the import directory to the virtual machine's data root, if applicable.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b64a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6b64a-106">Syntax</span></span>


```mof
uint32 RealizePlannedSystem(
  [in]  Msvm_PlannedComputerSystem REF PlannedSystem,
  [out] CIM_ComputerSystem         REF ResultingSystem,
  [out] CIM_ConcreteJob            REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="6b64a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6b64a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b64a-108">*PlannedSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6b64a-108">*PlannedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b64a-109">Référence à l’instance [**MSVM \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md) qui doit être convertie en ordinateur virtuel réalisé.</span><span class="sxs-lookup"><span data-stu-id="6b64a-109">A reference to the [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) instance which is to be converted into a realized virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="6b64a-110">*ResultingSystem* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6b64a-110">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b64a-111">Si l’opération est terminée de façon synchrone, il s’agit d’une référence à un objet [**\_ ComputerSystem CIM**](msvm-computersystem.md) qui représente l’ordinateur virtuel réalisé résultant.</span><span class="sxs-lookup"><span data-stu-id="6b64a-111">If the operation is completed synchronously, a reference to a [**CIM\_ComputerSystem**](msvm-computersystem.md) object that represents the resulting realized virtual machine.</span></span>

<span data-ttu-id="6b64a-112">Type de données mis à jour à partir de [**MSVM \_ ComputerSystem**](msvm-computersystem.md) dans Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="6b64a-112">Datatype updated from [**Msvm\_ComputerSystem**](msvm-computersystem.md) in Windows 10, version 1703.</span></span>

</dd> <dt>

<span data-ttu-id="6b64a-113">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6b64a-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b64a-114">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6b64a-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b64a-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6b64a-115">Return value</span></span>

<span data-ttu-id="6b64a-116">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="6b64a-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="6b64a-117">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="6b64a-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6b64a-118">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="6b64a-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6b64a-119">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="6b64a-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="6b64a-120">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="6b64a-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="6b64a-121">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="6b64a-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="6b64a-122">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="6b64a-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="6b64a-123">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="6b64a-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="6b64a-124">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="6b64a-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="6b64a-125">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="6b64a-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="6b64a-126">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="6b64a-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="6b64a-127">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="6b64a-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="6b64a-128">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="6b64a-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="6b64a-129">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="6b64a-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="6b64a-130">Exemples</span><span class="sxs-lookup"><span data-stu-id="6b64a-130">Examples</span></span>

<span data-ttu-id="6b64a-131">L’exemple C# suivant utilise la méthode **RealizePlannedSystem** pour réaliser un ordinateur virtuel planifié.</span><span class="sxs-lookup"><span data-stu-id="6b64a-131">The following C# sample uses the **RealizePlannedSystem** method to realize a planned virtual machine.</span></span> <span data-ttu-id="6b64a-132">Ce code est extrait de l' [exemple de machines virtuelles planifiées Hyper-V](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm).</span><span class="sxs-lookup"><span data-stu-id="6b64a-132">This code is taken from the [Hyper-V planned virtual machines sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm).</span></span> <span data-ttu-id="6b64a-133">Les utilitaires référencés se trouvent dans [les utilitaires courants pour les exemples de virtualisation (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="6b64a-133">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6b64a-134">Pour fonctionner correctement, le code suivant doit être exécuté sur le serveur hôte de l’ordinateur virtuel et doit être exécuté avec des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="6b64a-134">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
/// <summary>
/// Finds the first Planned VM matching pvmName and realizes it.
/// </summary>
/// <param name="pvmName">The name of the PVM to be realized.</param>
/// <returns>The Realized Virtual Machine.</returns>
internal static ManagementObject
RealizePvm(
    string pvmName
    )
{
    ManagementObject vm = null;
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2");

    using (ManagementObject pvm = WmiUtilities.GetPlannedVirtualMachine(pvmName, scope))
    using (ManagementObject managementService = WmiUtilities.GetVirtualMachineManagementService(scope))
    using (ManagementBaseObject inParams =
        managementService.GetMethodParameters("RealizePlannedSystem"))
    {
        inParams["PlannedSystem"] = pvm.Path;

        Console.WriteLine("Realizing Planned Virtual Machine \"{0}\" ({1})...",
                pvm["ElementName"], pvm["Name"]);

        using (ManagementBaseObject outParams =
            managementService.InvokeMethod("RealizePlannedSystem", inParams, null))
        {
            if (WmiUtilities.ValidateOutput(outParams, scope, true, true))
            {
                using (ManagementObject job =
                    new ManagementObject((string)outParams["Job"]))
                using (ManagementObjectCollection pvmCollection =
                    job.GetRelated("Msvm_ComputerSystem",
                        "Msvm_AffectedJobElement", null, null, null, null, false, null))
                {
                    vm = WmiUtilities.GetFirstObjectFromCollection(pvmCollection);
                }
            }
        }
    }

    return vm;
}
```



## <a name="requirements"></a><span data-ttu-id="6b64a-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6b64a-135">Requirements</span></span>



| <span data-ttu-id="6b64a-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6b64a-136">Requirement</span></span> | <span data-ttu-id="6b64a-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b64a-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b64a-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b64a-138">Minimum supported client</span></span><br/> | <span data-ttu-id="6b64a-139">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6b64a-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6b64a-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b64a-140">Minimum supported server</span></span><br/> | <span data-ttu-id="6b64a-141">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6b64a-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6b64a-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6b64a-142">Namespace</span></span><br/>                | <span data-ttu-id="6b64a-143">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="6b64a-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6b64a-144">MOF</span><span class="sxs-lookup"><span data-stu-id="6b64a-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b64a-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6b64a-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6b64a-146">DLL</span><span class="sxs-lookup"><span data-stu-id="6b64a-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b64a-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6b64a-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6b64a-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b64a-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b64a-149">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="6b64a-149">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

