---
description: Joint un fichier de disque dur virtuel en mode de bouclage.
ms.assetid: 54bd8e67-e309-4bf3-94bd-e29bc3300a3d
title: Méthode AttachVirtualHardDisk de la classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.AttachVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0f8a22ac377eb96fdc01fa54877cdc6c12619c41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865221"
---
# <a name="attachvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="77b42-103">Méthode AttachVirtualHardDisk de la \_ classe ImageManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="77b42-103">AttachVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="77b42-104">Joint un fichier de disque dur virtuel en mode de bouclage.</span><span class="sxs-lookup"><span data-stu-id="77b42-104">Attaches a virtual hard disk file in loopback mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="77b42-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77b42-105">Syntax</span></span>


```mof
uint32 AttachVirtualHardDisk(
  [in]  string              Path,
  [in]  boolean             AssignDriveLetter,
  [in]  boolean             ReadOnly,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="77b42-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="77b42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77b42-107">*Chemin d’accès* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="77b42-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77b42-108">Chemin qualifié complet qui spécifie l’emplacement du fichier de disque dur virtuel à attacher.</span><span class="sxs-lookup"><span data-stu-id="77b42-108">A fully qualified path that specifies the location of the virtual hard disk file to attach.</span></span>

</dd> <dt>

<span data-ttu-id="77b42-109">*AssignDriveLetter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="77b42-109">*AssignDriveLetter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77b42-110">Indique si des lettres de lecteur sont affectées aux volumes du disque.</span><span class="sxs-lookup"><span data-stu-id="77b42-110">Indicates if drive letters are assigned to the disk's volumes.</span></span>

</dd> <dt>

<span data-ttu-id="77b42-111">*Lecture seule* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="77b42-111">*ReadOnly* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77b42-112">Indique si le disque dur attaché doit être en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="77b42-112">Indicates if the attached hard disk should be read-only.</span></span>

</dd> <dt>

<span data-ttu-id="77b42-113">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="77b42-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77b42-114">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="77b42-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77b42-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="77b42-115">Return value</span></span>

<span data-ttu-id="77b42-116">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="77b42-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="77b42-117">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="77b42-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="77b42-118">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="77b42-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="77b42-119">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="77b42-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="77b42-120">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="77b42-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="77b42-121">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="77b42-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="77b42-122">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="77b42-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="77b42-123">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="77b42-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="77b42-124">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="77b42-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="77b42-125">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="77b42-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="77b42-126">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="77b42-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="77b42-127">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="77b42-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="77b42-128">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="77b42-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="77b42-129">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="77b42-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="77b42-130">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="77b42-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="77b42-131">Notes</span><span class="sxs-lookup"><span data-stu-id="77b42-131">Remarks</span></span>

<span data-ttu-id="77b42-132">Pour détacher le disque dur virtuel, utilisez la méthode [**MSVM \_ MountedStorageImage. DetachVirtualHardDisk**](detachvirtualharddisk-msvm-mountedstorageimage.md) .</span><span class="sxs-lookup"><span data-stu-id="77b42-132">To detach the virtual hard disk, use the [**Msvm\_MountedStorageImage.DetachVirtualHardDisk**](detachvirtualharddisk-msvm-mountedstorageimage.md) method.</span></span>

<span data-ttu-id="77b42-133">L’accès à la classe [**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="77b42-133">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="77b42-134">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="77b42-134">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="77b42-135">Exemples</span><span class="sxs-lookup"><span data-stu-id="77b42-135">Examples</span></span>

<span data-ttu-id="77b42-136">L’exemple C# suivant montre comment attacher un fichier de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="77b42-136">The following C# example shows how to attach a virtual hard disk file.</span></span> <span data-ttu-id="77b42-137">Les utilitaires référencés se trouvent dans [les utilitaires courants pour les exemples de virtualisation (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="77b42-137">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public static void AttachVirtualHardDisk(string path)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("AttachVirtualHardDisk");
    inParams["Path"] = path;
    inParams["AssignDriveLetter"] = true;
    inParams["ReadOnly"] = false;
    ManagementBaseObject outParams = imageService.InvokeMethod("AttachVirtualHardDisk", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was attached successfully.", inParams["Path"]);
        }
        else
        {
            Console.WriteLine("Unable to attach {0}", inParams["Path"]);
        }
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="77b42-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="77b42-138">Requirements</span></span>



| <span data-ttu-id="77b42-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="77b42-139">Requirement</span></span> | <span data-ttu-id="77b42-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="77b42-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77b42-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77b42-141">Minimum supported client</span></span><br/> | <span data-ttu-id="77b42-142">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="77b42-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="77b42-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77b42-143">Minimum supported server</span></span><br/> | <span data-ttu-id="77b42-144">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="77b42-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="77b42-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="77b42-145">Namespace</span></span><br/>                | <span data-ttu-id="77b42-146">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="77b42-146">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="77b42-147">MOF</span><span class="sxs-lookup"><span data-stu-id="77b42-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="77b42-148"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="77b42-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="77b42-149">DLL</span><span class="sxs-lookup"><span data-stu-id="77b42-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77b42-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="77b42-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="77b42-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77b42-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77b42-152">**MSVM \_ MountedStorageImage. DetachVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="77b42-152">**Msvm\_MountedStorageImage.DetachVirtualHardDisk**</span></span>](detachvirtualharddisk-msvm-mountedstorageimage.md)
</dt> <dt>

[<span data-ttu-id="77b42-153">**Mount (v1)**</span><span class="sxs-lookup"><span data-stu-id="77b42-153">**Mount (V1)**</span></span>](/previous-versions/windows/desktop/virtual/mount-msvm-imagemanagementservice)
</dt> <dt>

[<span data-ttu-id="77b42-154">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="77b42-154">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

