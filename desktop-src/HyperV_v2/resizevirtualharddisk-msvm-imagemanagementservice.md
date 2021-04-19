---
description: Redimensionne un disque dur virtuel existant.
ms.assetid: 54FDCA3B-E12B-4E68-B7EE-893C9CD97E1A
title: Méthode ResizeVirtualHardDisk de la classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ResizeVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5fcd88a9063dcbe4e19705245b36af33672dfc5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544235"
---
# <a name="resizevirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="0c2eb-103">Méthode ResizeVirtualHardDisk de la \_ classe ImageManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="0c2eb-103">ResizeVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="0c2eb-104">Redimensionne un disque dur virtuel existant.</span><span class="sxs-lookup"><span data-stu-id="0c2eb-104">Resizes an existing virtual hard disk.</span></span> <span data-ttu-id="0c2eb-105">Le disque dur virtuel doit être hors connexion.</span><span class="sxs-lookup"><span data-stu-id="0c2eb-105">The virtual hard disk must be offline.</span></span> <span data-ttu-id="0c2eb-106">Consultez la section Notes pour connaître les restrictions d’utilisation de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="0c2eb-106">See Remarks for usage restrictions for this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c2eb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c2eb-107">Syntax</span></span>


```mof
uint32 ResizeVirtualHardDisk(
  [in]  string              Path,
  [in]  uint64              MaxInternalSize,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="0c2eb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c2eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c2eb-109">*Chemin d’accès* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0c2eb-109">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c2eb-110">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0c2eb-110">Type: **string**</span></span>

<span data-ttu-id="0c2eb-111">Chemin d’accès complet du fichier de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="0c2eb-111">The fully qualified path of the virtual hard disk file.</span></span>

</dd> <dt>

<span data-ttu-id="0c2eb-112">*MaxInternalSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0c2eb-112">*MaxInternalSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c2eb-113">Type : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0c2eb-113">Type: **uint64**</span></span>

<span data-ttu-id="0c2eb-114">Taille maximale, en octets, du disque dur virtuel, tel qu’il est visible par l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="0c2eb-114">The maximum size of the virtual hard disk as viewable by the virtual machine, in bytes.</span></span> <span data-ttu-id="0c2eb-115">La valeur minimale de *MaxInternalSize* est « *disk* » + 512-(*diskze* mod 512).</span><span class="sxs-lookup"><span data-stu-id="0c2eb-115">*MaxInternalSize* minimum value is *DiskSize* + 512 - (*DiskSize* mod 512).</span></span> <span data-ttu-id="0c2eb-116">La *valeur de* cette valeur est la taille du fichier de disque dur virtuel, en octets.</span><span class="sxs-lookup"><span data-stu-id="0c2eb-116">*DiskSize* is the size of the virtual hard disk file, in bytes.</span></span> <span data-ttu-id="0c2eb-117">L’erreur InvalidParameter (32773) est retournée si la valeur *MaxInternalSize* spécifiée est inférieure à la valeur minimale.</span><span class="sxs-lookup"><span data-stu-id="0c2eb-117">The InvalidParameter error (32773) is returned if the *MaxInternalSize* value specified is less than the minimum value.</span></span>

</dd> <dt>

<span data-ttu-id="0c2eb-118">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0c2eb-118">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c2eb-119">Type : **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="0c2eb-119">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="0c2eb-120">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0c2eb-120">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c2eb-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0c2eb-121">Return value</span></span>

<span data-ttu-id="0c2eb-122">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0c2eb-122">Type: **uint32**</span></span>

<span data-ttu-id="0c2eb-123">Cette méthode peut retourner l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="0c2eb-123">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="0c2eb-124">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="0c2eb-124">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0c2eb-125">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="0c2eb-125">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="0c2eb-126">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="0c2eb-126">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="0c2eb-127">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="0c2eb-127">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="0c2eb-128">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="0c2eb-128">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="0c2eb-129">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="0c2eb-129">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="0c2eb-130">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="0c2eb-130">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="0c2eb-131">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="0c2eb-131">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="0c2eb-132">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="0c2eb-132">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="0c2eb-133">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="0c2eb-133">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="0c2eb-134">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="0c2eb-134">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="0c2eb-135">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="0c2eb-135">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="0c2eb-136">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="0c2eb-136">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="0c2eb-137">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="0c2eb-137">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="0c2eb-138">Notes</span><span class="sxs-lookup"><span data-stu-id="0c2eb-138">Remarks</span></span>

<span data-ttu-id="0c2eb-139">Seuls les types de disques durs virtuels suivants peuvent être utilisés avec cette méthode lorsque la taille du disque dur virtuel est augmentée :</span><span class="sxs-lookup"><span data-stu-id="0c2eb-139">Only the following types of virtual hard disks can be used with this method when the size of the virtual hard disk is being increased:</span></span>

-   <span data-ttu-id="0c2eb-140">VHD fixe</span><span class="sxs-lookup"><span data-stu-id="0c2eb-140">Fixed VHD</span></span>
-   <span data-ttu-id="0c2eb-141">VHDX fixe</span><span class="sxs-lookup"><span data-stu-id="0c2eb-141">Fixed VHDX</span></span>
-   <span data-ttu-id="0c2eb-142">Disque dur virtuel dynamique</span><span class="sxs-lookup"><span data-stu-id="0c2eb-142">Dynamic VHD</span></span>
-   <span data-ttu-id="0c2eb-143">VHDX dynamique</span><span class="sxs-lookup"><span data-stu-id="0c2eb-143">Dynamic VHDX</span></span>
-   <span data-ttu-id="0c2eb-144">VHDX de différenciation</span><span class="sxs-lookup"><span data-stu-id="0c2eb-144">Differencing VHDX</span></span>

<span data-ttu-id="0c2eb-145">Seuls les types de disques durs virtuels suivants peuvent être utilisés avec cette méthode lorsque la taille du disque dur virtuel est réduite :</span><span class="sxs-lookup"><span data-stu-id="0c2eb-145">Only the following types of virtual hard disks can be used with this method when the size of the virtual hard disk is being decreased:</span></span>

-   <span data-ttu-id="0c2eb-146">VHDX fixe</span><span class="sxs-lookup"><span data-stu-id="0c2eb-146">Fixed VHDX</span></span>
-   <span data-ttu-id="0c2eb-147">VHDX dynamique</span><span class="sxs-lookup"><span data-stu-id="0c2eb-147">Dynamic VHDX</span></span>
-   <span data-ttu-id="0c2eb-148">VHDX de différenciation</span><span class="sxs-lookup"><span data-stu-id="0c2eb-148">Differencing VHDX</span></span>

<span data-ttu-id="0c2eb-149">L’accès à la classe [**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="0c2eb-149">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="0c2eb-150">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="0c2eb-150">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="0c2eb-151">Exemples</span><span class="sxs-lookup"><span data-stu-id="0c2eb-151">Examples</span></span>

<span data-ttu-id="0c2eb-152">L’exemple C# suivant développe un fichier de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="0c2eb-152">The following C# example expands a virtual hard disk file.</span></span> <span data-ttu-id="0c2eb-153">Les utilitaires référencés se trouvent dans [les utilitaires courants pour les exemples de virtualisation (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="0c2eb-153">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
const UInt64 size1G = 0x40000000;

public static void ResizeVirtualHardDisk(string path, UInt64 maxInternalSize)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("ResizeVirtualHardDisk");
    inParams["Path"] = path;
    inParams["MaxInternalSize"] = maxInternalSize * size1G;
    ManagementBaseObject outParams = imageService.InvokeMethod("ResizeVirtualHardDisk", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was resized successfully.", inParams["Path"]);
        }
        else
        {
            Console.WriteLine("Unable to resize {0}", inParams["Path"]);
        }
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="0c2eb-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c2eb-154">Requirements</span></span>



| <span data-ttu-id="0c2eb-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c2eb-155">Requirement</span></span> | <span data-ttu-id="0c2eb-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c2eb-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c2eb-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c2eb-157">Minimum supported client</span></span><br/> | <span data-ttu-id="0c2eb-158">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0c2eb-158">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0c2eb-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c2eb-159">Minimum supported server</span></span><br/> | <span data-ttu-id="0c2eb-160">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0c2eb-160">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0c2eb-161">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0c2eb-161">Namespace</span></span><br/>                | <span data-ttu-id="0c2eb-162">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="0c2eb-162">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0c2eb-163">MOF</span><span class="sxs-lookup"><span data-stu-id="0c2eb-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0c2eb-164"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0c2eb-164"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0c2eb-165">DLL</span><span class="sxs-lookup"><span data-stu-id="0c2eb-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c2eb-166"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0c2eb-166"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0c2eb-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c2eb-167">See also</span></span>

<dl> <dt>

<span data-ttu-id="0c2eb-168">[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0c2eb-168">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0c2eb-169">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="0c2eb-169">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

