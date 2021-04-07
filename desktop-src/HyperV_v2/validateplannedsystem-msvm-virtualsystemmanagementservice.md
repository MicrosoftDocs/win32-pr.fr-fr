---
description: Valide le système planifié spécifié.
ms.assetid: cb969b38-f36d-4c70-b234-590f1c219d22
title: Méthode ValidatePlannedSystem de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ValidatePlannedSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 96137c3774291e06bfffdea3843658a427e36950
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759046"
---
# <a name="validateplannedsystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="8a5d2-103">Méthode ValidatePlannedSystem de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="8a5d2-103">ValidatePlannedSystem method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="8a5d2-104">Valide le système planifié spécifié.</span><span class="sxs-lookup"><span data-stu-id="8a5d2-104">Validates the specified planned system.</span></span> <span data-ttu-id="8a5d2-105">Cela implique des vérifications de la configuration de l’ordinateur virtuel, des appareils, de la configuration de l’instantané, des appareils de capture instantanée, des fichiers d’État enregistrés et des fichiers de stockage.</span><span class="sxs-lookup"><span data-stu-id="8a5d2-105">This involves checks of the virtual machine configuration, devices, snapshot configuration, snapshot devices, saved state files and storage files.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a5d2-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a5d2-106">Syntax</span></span>


```mof
uint32 ValidatePlannedSystem(
  [in]  Msvm_PlannedComputerSystem REF PlannedSystem,
  [out] CIM_ConcreteJob            REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="8a5d2-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8a5d2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a5d2-108">*PlannedSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8a5d2-108">*PlannedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a5d2-109">Référence à un objet [**MSVM \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md) qui représente le système planifié à valider.</span><span class="sxs-lookup"><span data-stu-id="8a5d2-109">A reference to an [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) object that represents the planned system to be validated.</span></span>

</dd> <dt>

<span data-ttu-id="8a5d2-110">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8a5d2-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a5d2-111">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8a5d2-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a5d2-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8a5d2-112">Return value</span></span>

<span data-ttu-id="8a5d2-113">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="8a5d2-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="8a5d2-114">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="8a5d2-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8a5d2-115">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="8a5d2-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="8a5d2-116">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="8a5d2-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="8a5d2-117">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="8a5d2-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="8a5d2-118">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="8a5d2-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="8a5d2-119">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="8a5d2-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="8a5d2-120">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="8a5d2-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="8a5d2-121">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="8a5d2-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="8a5d2-122">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="8a5d2-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="8a5d2-123">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="8a5d2-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="8a5d2-124">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="8a5d2-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="8a5d2-125">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="8a5d2-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="8a5d2-126">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="8a5d2-126">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="8a5d2-127">**Fichier en cours d’utilisation** (32779)</span><span class="sxs-lookup"><span data-stu-id="8a5d2-127">**File in Use** (32779)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="8a5d2-128">Exemples</span><span class="sxs-lookup"><span data-stu-id="8a5d2-128">Examples</span></span>

<span data-ttu-id="8a5d2-129">L’exemple C# suivant utilise la méthode **ValidatePlannedSystem** pour valider un ordinateur virtuel planifié.</span><span class="sxs-lookup"><span data-stu-id="8a5d2-129">The following C# sample uses the **ValidatePlannedSystem** method to validate a planned virtual machine.</span></span> <span data-ttu-id="8a5d2-130">Ce code est extrait de l' [exemple de machines virtuelles planifiées Hyper-V](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm).</span><span class="sxs-lookup"><span data-stu-id="8a5d2-130">This code is taken from the [Hyper-V planned virtual machines sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm).</span></span> <span data-ttu-id="8a5d2-131">Les utilitaires référencés se trouvent dans [les utilitaires courants pour les exemples de virtualisation (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="8a5d2-131">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8a5d2-132">Pour fonctionner correctement, le code suivant doit être exécuté sur le serveur hôte de l’ordinateur virtuel et doit être exécuté avec des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="8a5d2-132">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
/// <summary>
/// Finds the first Planned VM matching pvmName and validates it, displaying
/// any warnings produced.
/// </summary>
/// <param name="pvmName">The name of the PVM to be validated.</param>
internal static void
ValidatePvm(
    string pvmName
    )
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2");

    using (ManagementObject pvm = WmiUtilities.GetPlannedVirtualMachine(pvmName, scope))
    using (ManagementObject managementService = WmiUtilities.GetVirtualMachineManagementService(scope))
    using (ManagementBaseObject inParams = 
        managementService.GetMethodParameters("ValidatePlannedSystem"))
    {
        inParams["PlannedSystem"] = pvm.Path;

        Console.WriteLine("Validating Planned Virtual Machine \"{0}\" ({1})...",
                pvm["ElementName"], pvm["Name"]);

        using (ManagementBaseObject outParams = 
            managementService.InvokeMethod("ValidatePlannedSystem", inParams, null))
        {
            if (WmiUtilities.ValidateOutput(outParams, scope))
            {
                using (ManagementObject job = 
                    new ManagementObject((string)outParams["Job"]))
                {
                    WmiUtilities.PrintMsvmErrors(job);
                }
            }
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="8a5d2-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8a5d2-133">Requirements</span></span>



| <span data-ttu-id="8a5d2-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8a5d2-134">Requirement</span></span> | <span data-ttu-id="8a5d2-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a5d2-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a5d2-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a5d2-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8a5d2-137">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a5d2-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8a5d2-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a5d2-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8a5d2-139">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a5d2-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8a5d2-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8a5d2-140">Namespace</span></span><br/>                | <span data-ttu-id="8a5d2-141">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="8a5d2-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8a5d2-142">MOF</span><span class="sxs-lookup"><span data-stu-id="8a5d2-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a5d2-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8a5d2-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8a5d2-144">DLL</span><span class="sxs-lookup"><span data-stu-id="8a5d2-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a5d2-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8a5d2-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8a5d2-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a5d2-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a5d2-147">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="8a5d2-147">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

