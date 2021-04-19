---
description: Compacte un fichier de disque dur virtuel.
ms.assetid: 1E64BD91-6FE6-4658-9EBF-615FC705B920
title: Méthode CompactVirtualHardDisk de la classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.CompactVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8e8c148e51105d8c78021b58366e2f2df3913f57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521263"
---
# <a name="compactvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="1a9e1-103">Méthode CompactVirtualHardDisk de la \_ classe ImageManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="1a9e1-103">CompactVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="1a9e1-104">Compacte un fichier de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="1a9e1-104">Compacts a virtual hard disk file.</span></span> <span data-ttu-id="1a9e1-105">Le compactage est le processus qui consiste à libérer des parties inutilisées du disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="1a9e1-105">Compacting is the process of freeing unused portions of the virtual hard disk.</span></span> <span data-ttu-id="1a9e1-106">Le disque dur virtuel n’est pas monté automatiquement.</span><span class="sxs-lookup"><span data-stu-id="1a9e1-106">The virtual hard disk is not automatically mounted.</span></span> <span data-ttu-id="1a9e1-107">Consultez la section Notes pour connaître les restrictions d’utilisation de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="1a9e1-107">See Remarks for usage restrictions for this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a9e1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1a9e1-108">Syntax</span></span>


```mof
uint32 CompactVirtualHardDisk(
  [in]  string              Path,
  [in]  uint16              Mode,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="1a9e1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a9e1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a9e1-110">*Chemin d’accès* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1a9e1-110">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a9e1-111">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1a9e1-111">Type: **string**</span></span>

<span data-ttu-id="1a9e1-112">Chemin qualifié complet qui spécifie l’emplacement du fichier de fusion.</span><span class="sxs-lookup"><span data-stu-id="1a9e1-112">A fully qualified path that specifies the location of the merging file.</span></span>

</dd> <dt>

<span data-ttu-id="1a9e1-113">*Mode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1a9e1-113">*Mode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a9e1-114">Type : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1a9e1-114">Type: **uint16**</span></span>

<span data-ttu-id="1a9e1-115">Spécifie le mode pour l’opération de compactage.</span><span class="sxs-lookup"><span data-stu-id="1a9e1-115">Specifies the mode for the compact operation.</span></span> <span data-ttu-id="1a9e1-116">Il doit s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1a9e1-116">This must be one of the following values.</span></span>

<dt>

<span id="Full"></span><span id="full"></span><span id="FULL"></span>

<span data-ttu-id="1a9e1-117">**Full** (0)</span><span class="sxs-lookup"><span data-stu-id="1a9e1-117">**Full** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Quick"></span><span id="quick"></span><span id="QUICK"></span>

<span data-ttu-id="1a9e1-118">**Rapide** (1)</span><span class="sxs-lookup"><span data-stu-id="1a9e1-118">**Quick** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Retrim"></span><span id="retrim"></span><span id="RETRIM"></span>

<span data-ttu-id="1a9e1-119">**Retrim** (2)</span><span class="sxs-lookup"><span data-stu-id="1a9e1-119">**Retrim** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Pretrimmed"></span><span id="pretrimmed"></span><span id="PRETRIMMED"></span>

<span data-ttu-id="1a9e1-120">**Préconformés** (3)</span><span class="sxs-lookup"><span data-stu-id="1a9e1-120">**Pretrimmed** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Prezeroed"></span><span id="prezeroed"></span><span id="PREZEROED"></span>

<span data-ttu-id="1a9e1-121">**Prezéros** (4)</span><span class="sxs-lookup"><span data-stu-id="1a9e1-121">**Prezeroed** (4)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="1a9e1-122">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1a9e1-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a9e1-123">Type : **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="1a9e1-123">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="1a9e1-124">Référence au travail (peut avoir la **valeur null** si la tâche est terminée).</span><span class="sxs-lookup"><span data-stu-id="1a9e1-124">A reference to the job (can be **Null** if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a9e1-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1a9e1-125">Return value</span></span>

<span data-ttu-id="1a9e1-126">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1a9e1-126">Type: **uint32**</span></span>

<span data-ttu-id="1a9e1-127">Cette méthode peut retourner l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1a9e1-127">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="1a9e1-128">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="1a9e1-128">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1a9e1-129">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="1a9e1-129">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="1a9e1-130">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="1a9e1-130">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="1a9e1-131">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="1a9e1-131">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="1a9e1-132">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="1a9e1-132">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="1a9e1-133">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="1a9e1-133">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="1a9e1-134">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="1a9e1-134">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="1a9e1-135">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="1a9e1-135">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="1a9e1-136">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="1a9e1-136">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="1a9e1-137">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="1a9e1-137">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="1a9e1-138">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="1a9e1-138">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="1a9e1-139">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="1a9e1-139">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="1a9e1-140">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="1a9e1-140">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="1a9e1-141">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="1a9e1-141">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="1a9e1-142">Notes</span><span class="sxs-lookup"><span data-stu-id="1a9e1-142">Remarks</span></span>

<span data-ttu-id="1a9e1-143">Seuls les types de disques durs virtuels suivants peuvent être utilisés avec cette méthode :</span><span class="sxs-lookup"><span data-stu-id="1a9e1-143">Only the following types of virtual hard disks can be used with this method:</span></span>

-   <span data-ttu-id="1a9e1-144">VHDX fixe</span><span class="sxs-lookup"><span data-stu-id="1a9e1-144">Fixed VHDX</span></span>
-   <span data-ttu-id="1a9e1-145">Disque dur virtuel dynamique</span><span class="sxs-lookup"><span data-stu-id="1a9e1-145">Dynamic VHD</span></span>
-   <span data-ttu-id="1a9e1-146">VHDX dynamique</span><span class="sxs-lookup"><span data-stu-id="1a9e1-146">Dynamic VHDX</span></span>
-   <span data-ttu-id="1a9e1-147">Disque dur virtuel de différenciation</span><span class="sxs-lookup"><span data-stu-id="1a9e1-147">Differencing VHD</span></span>
-   <span data-ttu-id="1a9e1-148">VHDX de différenciation</span><span class="sxs-lookup"><span data-stu-id="1a9e1-148">Differencing VHDX</span></span>

<span data-ttu-id="1a9e1-149">L’accès à la classe [**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="1a9e1-149">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="1a9e1-150">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="1a9e1-150">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="1a9e1-151">Exemples</span><span class="sxs-lookup"><span data-stu-id="1a9e1-151">Examples</span></span>

<span data-ttu-id="1a9e1-152">L’exemple C# suivant compacte un disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="1a9e1-152">The following C# example compacts a virtual hard disk.</span></span> <span data-ttu-id="1a9e1-153">Les utilitaires référencés se trouvent dans [les utilitaires courants pour les exemples de virtualisation (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="1a9e1-153">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public enum VirtualHardDiskCompactMode
{
    Full = 0,
    Quick = 1,
    Retrim = 2,
    Pretrimmed = 3,
    Prezeroed = 4
}

public static void CompactVirtualHardDisk(string vhdPath, VirtualHardDiskCompactMode compactMode)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("CompactVirtualHardDisk");
    inParams["Path"] = vhdPath;
    inParams["Mode"] = compactMode;
    ManagementBaseObject outParams = imageService.InvokeMethod("CompactVirtualHardDisk", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was compacted successfully.", inParams["Path"]);
        }
        else
        {
            Console.WriteLine("Unable to compact {0}", inParams["Path"]);
        }
    }
    else
    {
        Console.WriteLine("Compact {0} returned error {1}", inParams["Path"], outParams["ReturnValue"]);
    }

    inParams.Dispose();
    outParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="1a9e1-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1a9e1-154">Requirements</span></span>



| <span data-ttu-id="1a9e1-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1a9e1-155">Requirement</span></span> | <span data-ttu-id="1a9e1-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a9e1-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a9e1-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a9e1-157">Minimum supported client</span></span><br/> | <span data-ttu-id="1a9e1-158">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1a9e1-158">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1a9e1-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a9e1-159">Minimum supported server</span></span><br/> | <span data-ttu-id="1a9e1-160">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1a9e1-160">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1a9e1-161">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1a9e1-161">Namespace</span></span><br/>                | <span data-ttu-id="1a9e1-162">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="1a9e1-162">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1a9e1-163">MOF</span><span class="sxs-lookup"><span data-stu-id="1a9e1-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1a9e1-164"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1a9e1-164"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1a9e1-165">DLL</span><span class="sxs-lookup"><span data-stu-id="1a9e1-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a9e1-166"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1a9e1-166"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1a9e1-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a9e1-167">See also</span></span>

<dl> <dt>

<span data-ttu-id="1a9e1-168">[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1a9e1-168">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1a9e1-169">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="1a9e1-169">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

