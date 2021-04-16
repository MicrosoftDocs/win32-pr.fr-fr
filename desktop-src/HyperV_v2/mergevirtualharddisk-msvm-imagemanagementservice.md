---
description: Fusionne un disque dur virtuel enfant dans une chaîne de différenciation avec un ou plusieurs disques durs virtuels parents dans la chaîne.
ms.assetid: 10633176-F0C3-4CA0-8E7B-2B11FF93B0EA
title: Méthode MergeVirtualHardDisk de la classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.MergeVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 347e11d55357a8b3366aeb09badc53c1afad9e01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529662"
---
# <a name="mergevirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="9f5f1-103">Méthode MergeVirtualHardDisk de la \_ classe ImageManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="9f5f1-103">MergeVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="9f5f1-104">Fusionne un disque dur virtuel enfant dans une chaîne de différenciation avec un ou plusieurs disques durs virtuels parents dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="9f5f1-104">Merges a child virtual hard disk in a differencing chain with one or more parent virtual hard disks in the chain.</span></span> <span data-ttu-id="9f5f1-105">Consultez la section Notes pour connaître les restrictions d’utilisation de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="9f5f1-105">See Remarks for usage restrictions for this method.</span></span>

<span data-ttu-id="9f5f1-106">Si l’utilisateur qui exécute cette fonction n’a pas l’autorisation de mettre à jour les ordinateurs virtuels, cette fonction échoue.</span><span class="sxs-lookup"><span data-stu-id="9f5f1-106">If the user executing this function does not have permission to update the virtual machines, then this function will fail.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f5f1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f5f1-107">Syntax</span></span>


```mof
uint32 MergeVirtualHardDisk(
  [in]  string              SourcePath,
  [in]  string              DestinationPath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="9f5f1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9f5f1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f5f1-109">*SourcePath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9f5f1-109">*SourcePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f5f1-110">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9f5f1-110">Type: **string**</span></span>

<span data-ttu-id="9f5f1-111">Chemin qualifié complet qui spécifie l’emplacement du fichier de disque dur virtuel à fusionner.</span><span class="sxs-lookup"><span data-stu-id="9f5f1-111">A fully qualified path that specifies the location of the virtual hard disk file to merge.</span></span>

</dd> <dt>

<span data-ttu-id="9f5f1-112">*DestinationPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9f5f1-112">*DestinationPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f5f1-113">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9f5f1-113">Type: **string**</span></span>

<span data-ttu-id="9f5f1-114">Chemin d’accès complet qui spécifie l’emplacement du fichier de disque dur virtuel parent dans lequel les données doivent être fusionnées.</span><span class="sxs-lookup"><span data-stu-id="9f5f1-114">A fully qualified path that specifies the location of the parent virtual hard disk file into which data is to be merged.</span></span> <span data-ttu-id="9f5f1-115">Il peut s’agir du disque dur virtuel parent immédiat du fichier de fusion ou de l’image de disque parent, à un niveau allant jusqu’à la chaîne de différenciation.</span><span class="sxs-lookup"><span data-stu-id="9f5f1-115">This could be the immediate parent virtual hard disk of the merging file or the parent disk image a few levels up the differencing chain.</span></span>

</dd> <dt>

<span data-ttu-id="9f5f1-116">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9f5f1-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f5f1-117">Type : **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="9f5f1-117">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="9f5f1-118">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9f5f1-118">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f5f1-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9f5f1-119">Return value</span></span>

<span data-ttu-id="9f5f1-120">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f5f1-120">Type: **uint32**</span></span>

<span data-ttu-id="9f5f1-121">Cette méthode peut retourner l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="9f5f1-121">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="9f5f1-122">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="9f5f1-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9f5f1-123">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="9f5f1-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="9f5f1-124">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="9f5f1-124">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="9f5f1-125">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="9f5f1-125">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="9f5f1-126">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="9f5f1-126">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="9f5f1-127">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="9f5f1-127">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="9f5f1-128">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="9f5f1-128">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="9f5f1-129">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="9f5f1-129">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="9f5f1-130">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="9f5f1-130">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="9f5f1-131">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="9f5f1-131">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="9f5f1-132">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="9f5f1-132">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="9f5f1-133">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="9f5f1-133">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="9f5f1-134">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="9f5f1-134">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="9f5f1-135">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="9f5f1-135">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="9f5f1-136">Notes</span><span class="sxs-lookup"><span data-stu-id="9f5f1-136">Remarks</span></span>

<span data-ttu-id="9f5f1-137">Le disque dur virtuel enfant doit être hors connexion.</span><span class="sxs-lookup"><span data-stu-id="9f5f1-137">The child virtual hard disk must be offline.</span></span>

<span data-ttu-id="9f5f1-138">Seuls les types de disques durs virtuels suivants peuvent être utilisés avec cette méthode :</span><span class="sxs-lookup"><span data-stu-id="9f5f1-138">Only the following types of virtual hard disks can be used with this method:</span></span>

-   <span data-ttu-id="9f5f1-139">Disque dur virtuel de différenciation</span><span class="sxs-lookup"><span data-stu-id="9f5f1-139">Differencing VHD</span></span>
-   <span data-ttu-id="9f5f1-140">VHDX de différenciation</span><span class="sxs-lookup"><span data-stu-id="9f5f1-140">Differencing VHDX</span></span>

<span data-ttu-id="9f5f1-141">L’accès à la classe [**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="9f5f1-141">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="9f5f1-142">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="9f5f1-142">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="9f5f1-143">Exemples</span><span class="sxs-lookup"><span data-stu-id="9f5f1-143">Examples</span></span>

<span data-ttu-id="9f5f1-144">L’exemple C# suivant développe un fichier de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="9f5f1-144">The following C# example expands a virtual hard disk file.</span></span> <span data-ttu-id="9f5f1-145">Les utilitaires référencés se trouvent dans [les utilitaires courants pour les exemples de virtualisation (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="9f5f1-145">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
// Merges a VHD into a parent VHD.
// ChildPath: The path to the VHD to merge.</param>
// ParentPath: The path to the parent into which to merge.</param>
public static void MergeVirtualHardDisk(string ChildPath, string ParentPath)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("MergeVirtualHardDisk");

    inParams["SourcePath"] = ChildPath;
    inParams["DestinationPath"] = ParentPath;

    ManagementBaseObject outParams = imageService.InvokeMethod("MergeVirtualHardDisk", inParams, null);

    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("MergeVirtualHardDisk succeeded.");
        }
        else
        {
            Console.WriteLine("MergeVirtualHardDisk failed.");
        }
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="9f5f1-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9f5f1-146">Requirements</span></span>



| <span data-ttu-id="9f5f1-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9f5f1-147">Requirement</span></span> | <span data-ttu-id="9f5f1-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f5f1-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f5f1-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f5f1-149">Minimum supported client</span></span><br/> | <span data-ttu-id="9f5f1-150">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9f5f1-150">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9f5f1-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f5f1-151">Minimum supported server</span></span><br/> | <span data-ttu-id="9f5f1-152">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9f5f1-152">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9f5f1-153">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9f5f1-153">Namespace</span></span><br/>                | <span data-ttu-id="9f5f1-154">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="9f5f1-154">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9f5f1-155">MOF</span><span class="sxs-lookup"><span data-stu-id="9f5f1-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f5f1-156"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9f5f1-156"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f5f1-157">DLL</span><span class="sxs-lookup"><span data-stu-id="9f5f1-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f5f1-158"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9f5f1-158"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9f5f1-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f5f1-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="9f5f1-160">[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9f5f1-160">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9f5f1-161">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="9f5f1-161">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

