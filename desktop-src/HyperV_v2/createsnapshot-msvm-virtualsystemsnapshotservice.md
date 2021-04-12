---
description: Crée une capture instantanée d’un ordinateur virtuel.
ms.assetid: 2de12fe7-5ec2-49d0-87ff-cd48c34fec46
title: Méthode CreateSnapshot de la classe Msvm_VirtualSystemSnapshotService (Dbdaoint. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.CreateSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c62b4abf60e367da1c4ac4b176e5f5d70f547c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319522"
---
# <a name="createsnapshot-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="7e1ff-103">Méthode CreateSnapshot de la \_ classe VirtualSystemSnapshotService MSVM</span><span class="sxs-lookup"><span data-stu-id="7e1ff-103">CreateSnapshot method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="7e1ff-104">Crée une capture instantanée d’un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7e1ff-104">Creates a snapshot of a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e1ff-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7e1ff-105">Syntax</span></span>


```mof
uint32 CreateSnapshot(
  [in]      CIM_ComputerSystem           REF AffectedSystem,
  [in]      string                           SnapshotSettings,
  [in]      uint16                           SnapshotType,
  [in, out] CIM_VirtualSystemSettingData REF ResultingSnapshot,
  [out]     CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="7e1ff-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7e1ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e1ff-107">*AffectedSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7e1ff-107">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e1ff-108">Référence à une classe [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente l’ordinateur virtuel pour lequel créer un instantané.</span><span class="sxs-lookup"><span data-stu-id="7e1ff-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the virtual machine to create a snapshot of.</span></span>

</dd> <dt>

<span data-ttu-id="7e1ff-109">*SnapshotSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7e1ff-109">*SnapshotSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e1ff-110">Chaîne qui contient une instance incorporée d’une classe [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) qui contient les paramètres de l’instantané.</span><span class="sxs-lookup"><span data-stu-id="7e1ff-110">A string that contains an embedded instance of a [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) class that contains the parameter settings for the snapshot.</span></span> <span data-ttu-id="7e1ff-111">Ce paramètre est facultatif et peut être une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="7e1ff-111">This parameter is optional and may be an empty string.</span></span>

</dd> <dt>

<span data-ttu-id="7e1ff-112">*SnapshotType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7e1ff-112">*SnapshotType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e1ff-113">Spécifie le type d’instantané demandé.</span><span class="sxs-lookup"><span data-stu-id="7e1ff-113">Specifies the type of snapshot requested.</span></span> <span data-ttu-id="7e1ff-114">Il doit s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="7e1ff-114">This must be one of the following values.</span></span>

<dt>

<span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>

<span data-ttu-id="7e1ff-115"><span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**Instantané complet** (2)</span><span class="sxs-lookup"><span data-stu-id="7e1ff-115"><span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**Full Snapshot** (2)</span></span>


</dt> <dd>

<span data-ttu-id="7e1ff-116">Capture instantanée complète de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="7e1ff-116">Complete snapshot of the virtual machine.</span></span>

</dd> <dt>

<span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>

<span data-ttu-id="7e1ff-117"><span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>**Capture instantanée de disque** (3)</span><span class="sxs-lookup"><span data-stu-id="7e1ff-117"><span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>**Disk Snapshot** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7e1ff-118">Capture instantanée des disques de machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="7e1ff-118">Snapshot of virtual machine disks.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="7e1ff-119"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="7e1ff-119"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="7e1ff-120"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="7e1ff-120"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="7e1ff-121">*ResultingSnapshot* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7e1ff-121">*ResultingSnapshot* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e1ff-122">Référence à un objet [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)) qui représente l’instantané d’ordinateur virtuel résultant.</span><span class="sxs-lookup"><span data-stu-id="7e1ff-122">A reference to a [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) object that represents the resulting virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="7e1ff-123">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7e1ff-123">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e1ff-124">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7e1ff-124">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e1ff-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7e1ff-125">Return value</span></span>

<span data-ttu-id="7e1ff-126">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="7e1ff-126">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="7e1ff-127">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="7e1ff-127">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7e1ff-128">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="7e1ff-128">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7e1ff-129">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="7e1ff-129">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7e1ff-130">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="7e1ff-130">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7e1ff-131">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="7e1ff-131">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7e1ff-132">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="7e1ff-132">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7e1ff-133">**Type non valide** (6)</span><span class="sxs-lookup"><span data-stu-id="7e1ff-133">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="7e1ff-134">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="7e1ff-134">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7e1ff-135">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="7e1ff-135">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="7e1ff-136">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="7e1ff-136">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="7e1ff-137">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="7e1ff-137">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="7e1ff-138">Exemples</span><span class="sxs-lookup"><span data-stu-id="7e1ff-138">Examples</span></span>

<span data-ttu-id="7e1ff-139">L’exemple de code C# suivant crée une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="7e1ff-139">The following C# example code creates a virtual machine.</span></span> <span data-ttu-id="7e1ff-140">Les utilitaires référencés se trouvent dans [les utilitaires courants pour les exemples de virtualisation (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="7e1ff-140">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7e1ff-141">Pour fonctionner correctement, le code suivant doit être exécuté sur le serveur hôte de l’ordinateur virtuel et doit être exécuté avec des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="7e1ff-141">To function correctly, the following code must be run on the virtual machine host server, and it must be run with Administrator privileges.</span></span>

 


```CSharp
public static void CreateSnapshot(string vmName)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemSnapshotService");

    ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("CreateSnapshot");

    // Set the AffectedSystem property.
    ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
    if (null == vm)
    {
        throw new ArgumentException(string.Format("The virtual machine \"{0}\" could not be found.", vmName));
    }

    inParams["AffectedSystem"] = vm.Path.Path;

    // Set the SnapshotSettings property.
#if(true)
    inParams["SnapshotSettings"] = "";
#else
    ManagementObject snapshotSettings = Utility.GetServiceObject(scope, "CIM_SettingData"); 
    inParams["SnapshotSettings"] = snapshotSettings.ToString();
#endif       
    // Set the SnapshotType property.
    inParams["SnapshotType"] = 2; // Full snapshot.

    ManagementBaseObject outParams = virtualSystemService.InvokeMethod("CreateSnapshot", inParams, null);

    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("Snapshot was created successfully.");

            MiscClass.GetAffectedElement(outParams, scope);
        }
        else
        {
            Console.WriteLine("Failed to create snapshot VM");
        }
    }
    else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
    {
        Console.WriteLine("Snapshot was created successfully.");
    }
    else
    {
        Console.WriteLine("Create virtual system snapshot failed with error {0}", outParams["ReturnValue"]);
    }

    inParams.Dispose();
    outParams.Dispose();
    vm.Dispose();
    virtualSystemService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="7e1ff-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e1ff-142">Requirements</span></span>



| <span data-ttu-id="7e1ff-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e1ff-143">Requirement</span></span> | <span data-ttu-id="7e1ff-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e1ff-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e1ff-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e1ff-145">Minimum supported client</span></span><br/> | <span data-ttu-id="7e1ff-146">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e1ff-146">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7e1ff-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e1ff-147">Minimum supported server</span></span><br/> | <span data-ttu-id="7e1ff-148">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e1ff-148">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7e1ff-149">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7e1ff-149">Namespace</span></span><br/>                | <span data-ttu-id="7e1ff-150">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="7e1ff-150">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7e1ff-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="7e1ff-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e1ff-152"><dt>Dbdaoint. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e1ff-152"><dt>Dbdaoint.h</dt></span></span> </dl>                   |
| <span data-ttu-id="7e1ff-153">MOF</span><span class="sxs-lookup"><span data-stu-id="7e1ff-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e1ff-154"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7e1ff-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e1ff-155">DLL</span><span class="sxs-lookup"><span data-stu-id="7e1ff-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e1ff-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7e1ff-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7e1ff-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e1ff-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e1ff-158">**MSVM \_ VirtualSystemSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="7e1ff-158">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[<span data-ttu-id="7e1ff-159">**CreateVirtualSystemSnapshot (v1)**</span><span class="sxs-lookup"><span data-stu-id="7e1ff-159">**CreateVirtualSystemSnapshot (V1)**</span></span>](/previous-versions/windows/desktop/virtual/createvirtualsystemsnapshot-msvm-virtualsystemmanagementservice)
</dt> </dl>

 

