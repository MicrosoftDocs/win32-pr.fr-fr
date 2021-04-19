---
description: Convertit un disque dur virtuel existant dans un autre type ou format.
ms.assetid: D4F3A030-D860-4569-B6CD-31661BD40D54
title: Méthode ConvertVirtualHardDisk de la classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ConvertVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 766b117b69ecfebd13986d02ca21df3725981bb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536724"
---
# <a name="convertvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="98480-103">Méthode ConvertVirtualHardDisk de la \_ classe ImageManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="98480-103">ConvertVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="98480-104">Convertit un disque dur virtuel existant dans un autre type ou format.</span><span class="sxs-lookup"><span data-stu-id="98480-104">Converts an existing virtual hard disk to a different type or format.</span></span> <span data-ttu-id="98480-105">Cette méthode crée un nouveau disque dur virtuel et ne convertit pas le disque dur virtuel source en place.</span><span class="sxs-lookup"><span data-stu-id="98480-105">This method creates a new virtual hard disk and does not convert the source virtual hard disk in place.</span></span> <span data-ttu-id="98480-106">Consultez la section Notes pour connaître les restrictions d’utilisation de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="98480-106">See Remarks for usage restrictions for this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="98480-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="98480-107">Syntax</span></span>


```mof
uint32 ConvertVirtualHardDisk(
  [in]  string              SourcePath,
  [in]  string              VirtualDiskSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="98480-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="98480-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98480-109">*SourcePath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="98480-109">*SourcePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98480-110">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="98480-110">Type: **string**</span></span>

<span data-ttu-id="98480-111">Chemin d’accès complet du fichier de disque dur virtuel source à convertir.</span><span class="sxs-lookup"><span data-stu-id="98480-111">The fully qualified path of the source virtual hard disk file to convert.</span></span> <span data-ttu-id="98480-112">Ce fichier ne sera pas modifié à la suite de cette opération.</span><span class="sxs-lookup"><span data-stu-id="98480-112">This file will not be modified as a result of this operation.</span></span>

</dd> <dt>

<span data-ttu-id="98480-113">*VirtualDiskSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="98480-113">*VirtualDiskSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98480-114">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="98480-114">Type: **string**</span></span>

<span data-ttu-id="98480-115">Représentation sous forme de chaîne de la classe [**MSVM \_ VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) qui spécifie les attributs du nouveau disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="98480-115">A string representation of the [**Msvm\_VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) class that specifies the attributes of the new virtual hard disk.</span></span> <span data-ttu-id="98480-116">Les propriétés **path**, **type**, **format**, **ParentPath**, **BlockSize** et **LogicalSectorSize** doivent être définies.</span><span class="sxs-lookup"><span data-stu-id="98480-116">The **Path**, **Type**, **Format**, **ParentPath**, **BlockSize**, and **LogicalSectorSize** properties must be set.</span></span> <span data-ttu-id="98480-117">La propriété **ParentPath** peut avoir la **valeur null** si elle n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="98480-117">The **ParentPath** property can be **Null** if it is not needed.</span></span> <span data-ttu-id="98480-118">Définissez les propriétés **BlockSize** et **LogicalSectorSize** sur 0 pour utiliser les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="98480-118">Set the **BlockSize** and **LogicalSectorSize** properties to 0 to use the default values.</span></span>

<span data-ttu-id="98480-119">Pour spécifier le format (VHD ou VHDX) du nouveau disque dur virtuel, définissez l’extension du chemin d' **accès** à la valeur appropriée (« . vhd » ou « . VHDX »).</span><span class="sxs-lookup"><span data-stu-id="98480-119">To specify the format (VHD or VHDX) of the new virtual hard disk, set the extension of the **Path** to the appropriate value (".vhd" or ".vhdx").</span></span> <span data-ttu-id="98480-120">La propriété **format** doit correspondre à l’extension de nom de fichier dans le **chemin d’accès**.</span><span class="sxs-lookup"><span data-stu-id="98480-120">The **Format** property must match the file name extension in the **Path**.</span></span>

<span data-ttu-id="98480-121">La propriété **LogicalSectorSize** sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="98480-121">The **LogicalSectorSize** property will be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="98480-122">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="98480-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98480-123">Type : **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="98480-123">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="98480-124">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="98480-124">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98480-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="98480-125">Return value</span></span>

<span data-ttu-id="98480-126">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="98480-126">Type: **uint32**</span></span>

<span data-ttu-id="98480-127">Cette méthode peut retourner l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="98480-127">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="98480-128">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="98480-128">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="98480-129">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="98480-129">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="98480-130">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="98480-130">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="98480-131">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="98480-131">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="98480-132">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="98480-132">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="98480-133">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="98480-133">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="98480-134">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="98480-134">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="98480-135">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="98480-135">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="98480-136">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="98480-136">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="98480-137">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="98480-137">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="98480-138">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="98480-138">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="98480-139">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="98480-139">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="98480-140">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="98480-140">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="98480-141">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="98480-141">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="98480-142">Notes</span><span class="sxs-lookup"><span data-stu-id="98480-142">Remarks</span></span>

<span data-ttu-id="98480-143">Seuls les types de disques durs virtuels suivants peuvent être utilisés avec cette méthode :</span><span class="sxs-lookup"><span data-stu-id="98480-143">Only the following types of virtual hard disks can be used with this method:</span></span>

-   <span data-ttu-id="98480-144">VHD fixe</span><span class="sxs-lookup"><span data-stu-id="98480-144">Fixed VHD</span></span>
-   <span data-ttu-id="98480-145">VHDX fixe</span><span class="sxs-lookup"><span data-stu-id="98480-145">Fixed VHDX</span></span>
-   <span data-ttu-id="98480-146">Disque dur virtuel dynamique</span><span class="sxs-lookup"><span data-stu-id="98480-146">Dynamic VHD</span></span>
-   <span data-ttu-id="98480-147">VHDX dynamique</span><span class="sxs-lookup"><span data-stu-id="98480-147">Dynamic VHDX</span></span>
-   <span data-ttu-id="98480-148">Disque dur virtuel de différenciation</span><span class="sxs-lookup"><span data-stu-id="98480-148">Differencing VHD</span></span>
-   <span data-ttu-id="98480-149">VHDX de différenciation</span><span class="sxs-lookup"><span data-stu-id="98480-149">Differencing VHDX</span></span>

<span data-ttu-id="98480-150">L’accès à la classe [**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="98480-150">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="98480-151">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="98480-151">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="98480-152">Exemples</span><span class="sxs-lookup"><span data-stu-id="98480-152">Examples</span></span>

<span data-ttu-id="98480-153">L’exemple C# suivant convertit un disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="98480-153">The following C# example converts a virtual hard disk.</span></span> <span data-ttu-id="98480-154">Les utilitaires référencés se trouvent dans [les utilitaires courants pour les exemples de virtualisation (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="98480-154">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public enum VirtualHardDiskType
{
    Fixed = 2,
    Dynamic = 3,
    Differencing = 4
}

public enum VirtualHardDiskFormat
{
    Unknown = 0,
    Vhd = 2,
    Vhdx = 3
}

public static void ConvertVirtualHardDisk(string sourcePath, string destinationPath, VirtualHardDiskType diskType, VirtualHardDiskFormat diskFormat)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementPath path = new ManagementPath()
    {
        Server = null,
        NamespacePath = imageService.Path.Path,
        ClassName = "Msvm_VirtualHardDiskSettingData"
    };

    ManagementClass settingsClass = new ManagementClass(path);
    ManagementObject settingsInstance = settingsClass.CreateInstance();
    settingsInstance["Path"] = destinationPath;
    settingsInstance["Type"] = diskType;
    settingsInstance["Format"] = diskFormat;
    settingsInstance["ParentPath"] = null;
    settingsInstance["MaxInternalSize"] = 0;
    settingsInstance["BlockSize"] = 0;
    settingsInstance["LogicalSectorSize"] = 0;
    settingsInstance["PhysicalSectorSize"] = 0;

    ManagementBaseObject inParams = imageService.GetMethodParameters("ConvertVirtualHardDisk");

    inParams["SourcePath"] = sourcePath;
    inParams["VirtualDiskSettingData"] = settingsInstance.GetText(TextFormat.WmiDtd20);

    ManagementBaseObject outParams = imageService.InvokeMethod("ConvertVirtualHardDisk", inParams, null);
    UInt32 result = (UInt32)outParams["ReturnValue"];
    if (ReturnCode.Completed == result)
    {
        Console.WriteLine("{0} was converted successfully.", inParams["SourcePath"]);
    }
    else if (ReturnCode.Started == result)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was converted successfully.", inParams["SourcePath"]);
        }
        else
        {
            Console.WriteLine("Unable to convert {0}", inParams["SourcePath"]);
        }
    }
    else
    {
        // The method failed.
        Console.WriteLine("ConvertVirtualHardDisk failed with error code {0}.", result);
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="98480-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="98480-155">Requirements</span></span>



| <span data-ttu-id="98480-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98480-156">Requirement</span></span> | <span data-ttu-id="98480-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="98480-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98480-158">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98480-158">Minimum supported client</span></span><br/> | <span data-ttu-id="98480-159">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="98480-159">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="98480-160">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98480-160">Minimum supported server</span></span><br/> | <span data-ttu-id="98480-161">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="98480-161">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="98480-162">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="98480-162">Namespace</span></span><br/>                | <span data-ttu-id="98480-163">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="98480-163">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="98480-164">MOF</span><span class="sxs-lookup"><span data-stu-id="98480-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="98480-165"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="98480-165"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="98480-166">DLL</span><span class="sxs-lookup"><span data-stu-id="98480-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98480-167"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="98480-167"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="98480-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98480-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98480-169">**ConvertVirtualHardDisk (v1)**</span><span class="sxs-lookup"><span data-stu-id="98480-169">**ConvertVirtualHardDisk (V1)**</span></span>](/previous-versions/windows/desktop/virtual/convertvirtualharddisk-msvm-imagemanagementservice)
</dt> <dt>

<span data-ttu-id="98480-170">[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="98480-170">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="98480-171">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="98480-171">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

