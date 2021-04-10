---
description: Supprime l’ordinateur virtuel précédemment défini de l’étendue de gestion du système hôte.
ms.assetid: 16E6EEB0-CB29-4FFC-AEFF-872E099337FA
title: Méthode DestroySystem de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DestroySystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1caf4e4a590bdbfe2f7543e23d5ca00018300fb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867074"
---
# <a name="destroysystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="dbd6d-103">Méthode DestroySystem de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="dbd6d-103">DestroySystem method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="dbd6d-104">Supprime l’ordinateur virtuel précédemment défini de l’étendue de gestion du système hôte.</span><span class="sxs-lookup"><span data-stu-id="dbd6d-104">Removes the previously defined virtual machine from the management scope of the host system.</span></span> <span data-ttu-id="dbd6d-105">Toutes les définitions de ressources associées seront également supprimées.</span><span class="sxs-lookup"><span data-stu-id="dbd6d-105">Any associated resource definitions will also be removed.</span></span> <span data-ttu-id="dbd6d-106">L’ordinateur virtuel doit être dans l’État mis hors tension ou enregistré avant d’appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="dbd6d-106">The virtual machine must be in the powered off or saved state prior to calling this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbd6d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dbd6d-107">Syntax</span></span>


```mof
uint32 DestroySystem(
  [in]  CIM_ComputerSystem REF AffectedSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="dbd6d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dbd6d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbd6d-109">*AffectedSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dbd6d-109">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbd6d-110">Type : **CIM \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="dbd6d-110">Type: **CIM\_ComputerSystem**</span></span>

<span data-ttu-id="dbd6d-111">Référence à une instance du [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente l’instance de machine virtuelle à détruire.</span><span class="sxs-lookup"><span data-stu-id="dbd6d-111">A reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) that represents the virtual machine instance to be destroyed.</span></span>

</dd> <dt>

<span data-ttu-id="dbd6d-112">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="dbd6d-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dbd6d-113">Type : **CIM \_ ConcreteJob**</span><span class="sxs-lookup"><span data-stu-id="dbd6d-113">Type: **CIM\_ConcreteJob**</span></span>

<span data-ttu-id="dbd6d-114">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dbd6d-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbd6d-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dbd6d-115">Return value</span></span>

<span data-ttu-id="dbd6d-116">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dbd6d-116">Type: **uint32**</span></span>

<span data-ttu-id="dbd6d-117">Si cette méthode est exécutée de façon synchrone, elle retourne 0 si elle réussit.</span><span class="sxs-lookup"><span data-stu-id="dbd6d-117">If this method is executed synchronously, it returns 0 if it succeeds.</span></span> <span data-ttu-id="dbd6d-118">Si cette méthode est exécutée de façon asynchrone, elle retourne 4096 et le paramètre de sortie de la *tâche* peut être utilisé pour suivre la progression de l’opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="dbd6d-118">If this method is executed asynchronously, it returns 4096 and the *Job* output parameter can be used to track the progress of the asynchronous operation.</span></span> <span data-ttu-id="dbd6d-119">Toute autre valeur de retour indique une erreur.</span><span class="sxs-lookup"><span data-stu-id="dbd6d-119">Any other return value indicates an error.</span></span>

<dl> <dt>

<span data-ttu-id="dbd6d-120">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="dbd6d-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dbd6d-121">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="dbd6d-121">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="dbd6d-122">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="dbd6d-122">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dbd6d-123">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="dbd6d-123">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="dbd6d-124">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="dbd6d-124">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="dbd6d-125">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="dbd6d-125">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="dbd6d-126">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="dbd6d-126">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="dbd6d-127">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="dbd6d-127">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="dbd6d-128">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="dbd6d-128">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="dbd6d-129">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="dbd6d-129">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="dbd6d-130">Notes</span><span class="sxs-lookup"><span data-stu-id="dbd6d-130">Remarks</span></span>

<span data-ttu-id="dbd6d-131">L’accès à la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="dbd6d-131">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="dbd6d-132">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="dbd6d-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="dbd6d-133">Exemples</span><span class="sxs-lookup"><span data-stu-id="dbd6d-133">Examples</span></span>

<span data-ttu-id="dbd6d-134">L’exemple C# suivant utilise la méthode **DestroySystem** pour supprimer un ordinateur virtuel planifié.</span><span class="sxs-lookup"><span data-stu-id="dbd6d-134">The following C# sample uses the **DestroySystem** method to remove a planned virtual machine.</span></span> <span data-ttu-id="dbd6d-135">Ce code est extrait de l' [exemple de machines virtuelles planifiées Hyper-V](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm).</span><span class="sxs-lookup"><span data-stu-id="dbd6d-135">This code is taken from the [Hyper-V planned virtual machines sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm).</span></span> <span data-ttu-id="dbd6d-136">Les utilitaires référencés se trouvent dans [les utilitaires courants pour les exemples de virtualisation (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="dbd6d-136">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dbd6d-137">Pour fonctionner correctement, le code suivant doit être exécuté sur le serveur hôte de l’ordinateur virtuel et doit être exécuté avec des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="dbd6d-137">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
/// <summary>
/// Finds the first Planned VM matching pvmName and removes it.
/// </summary>
/// <param name="pvmName">The name of the PVM to be removed.</param>
internal static void
RemovePvm(
    string pvmName
    )
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2");

    using (ManagementObject pvm = WmiUtilities.GetPlannedVirtualMachine(pvmName, scope))
    using (ManagementObject managementService = WmiUtilities.GetVirtualMachineManagementService(scope))
    using (ManagementBaseObject inParams =
        managementService.GetMethodParameters("DestroySystem"))
    {
        inParams["AffectedSystem"] = pvm.Path;

        Console.WriteLine("Removing Planned Virtual Machine \"{0}\" ({1})...",
                pvm["ElementName"], pvm["Name"]);

        using (ManagementBaseObject outParams =
            managementService.InvokeMethod("DestroySystem", inParams, null))
        {
            WmiUtilities.ValidateOutput(outParams, scope);
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="dbd6d-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dbd6d-138">Requirements</span></span>



| <span data-ttu-id="dbd6d-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dbd6d-139">Requirement</span></span> | <span data-ttu-id="dbd6d-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="dbd6d-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbd6d-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dbd6d-141">Minimum supported client</span></span><br/> | <span data-ttu-id="dbd6d-142">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dbd6d-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="dbd6d-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dbd6d-143">Minimum supported server</span></span><br/> | <span data-ttu-id="dbd6d-144">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dbd6d-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dbd6d-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="dbd6d-145">Namespace</span></span><br/>                | <span data-ttu-id="dbd6d-146">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="dbd6d-146">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="dbd6d-147">MOF</span><span class="sxs-lookup"><span data-stu-id="dbd6d-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dbd6d-148"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dbd6d-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dbd6d-149">DLL</span><span class="sxs-lookup"><span data-stu-id="dbd6d-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbd6d-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dbd6d-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dbd6d-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbd6d-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbd6d-152">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="dbd6d-152">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

