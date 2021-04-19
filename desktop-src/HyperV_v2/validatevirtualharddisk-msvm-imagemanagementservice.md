---
description: Détermine si un fichier de disque dur virtuel est valide.
ms.assetid: 5F7C99DB-0C81-46D5-A965-B6D87647ABF6
title: Méthode ValidateVirtualHardDisk de la classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ValidateVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 50c00dc4336e3e85b7db8ffd334de8868054c997
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531740"
---
# <a name="validatevirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="fbaab-103">Méthode ValidateVirtualHardDisk de la \_ classe ImageManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="fbaab-103">ValidateVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="fbaab-104">Détermine si un fichier de disque dur virtuel est valide.</span><span class="sxs-lookup"><span data-stu-id="fbaab-104">Determines whether a virtual hard disk file is valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbaab-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fbaab-105">Syntax</span></span>


```mof
uint32 ValidateVirtualHardDisk(
  [in]  string              Path,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="fbaab-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fbaab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbaab-107">*Chemin d’accès* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fbaab-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbaab-108">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fbaab-108">Type: **string**</span></span>

<span data-ttu-id="fbaab-109">Chemin qualifié complet qui spécifie l’emplacement du fichier de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="fbaab-109">A fully qualified path that specifies the location of the virtual hard disk file.</span></span>

</dd> <dt>

<span data-ttu-id="fbaab-110">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fbaab-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fbaab-111">Type : **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="fbaab-111">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="fbaab-112">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fbaab-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbaab-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fbaab-113">Return value</span></span>

<span data-ttu-id="fbaab-114">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fbaab-114">Type: **uint32**</span></span>

<span data-ttu-id="fbaab-115">Cette méthode peut retourner l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="fbaab-115">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="fbaab-116">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="fbaab-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fbaab-117">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="fbaab-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="fbaab-118">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="fbaab-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="fbaab-119">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="fbaab-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="fbaab-120">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="fbaab-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="fbaab-121">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="fbaab-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="fbaab-122">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="fbaab-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="fbaab-123">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="fbaab-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="fbaab-124">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="fbaab-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="fbaab-125">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="fbaab-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="fbaab-126">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="fbaab-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="fbaab-127">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="fbaab-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="fbaab-128">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="fbaab-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="fbaab-129">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="fbaab-129">**File not found** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="fbaab-130">**Cycle de la chaîne de différenciation VHD détecté** (32787)</span><span class="sxs-lookup"><span data-stu-id="fbaab-130">**Vhd differencing chain cycle detected** (32787)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="fbaab-131">Notes</span><span class="sxs-lookup"><span data-stu-id="fbaab-131">Remarks</span></span>

<span data-ttu-id="fbaab-132">Si le disque dur virtuel est un disque de différenciation, la totalité de la chaîne de disques virtuelle est ouverte.</span><span class="sxs-lookup"><span data-stu-id="fbaab-132">If the virtual hard disk is a differencing disk, the entire virtual disk chain is opened.</span></span> <span data-ttu-id="fbaab-133">Si le lien est rompu dans la chaîne de disques, un objet de traitement est retourné avec l’erreur appropriée initialisée et les propriétés enfants et parentes sont initialisées à l’emplacement où le lien est rompu.</span><span class="sxs-lookup"><span data-stu-id="fbaab-133">If the link is broken in the disk chain, a job object is returned with the appropriate error initialized and the child and parent properties are initialized to the location where the link is broken.</span></span>

<span data-ttu-id="fbaab-134">L’accès à la classe [**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="fbaab-134">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="fbaab-135">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="fbaab-135">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="fbaab-136">Exemples</span><span class="sxs-lookup"><span data-stu-id="fbaab-136">Examples</span></span>

<span data-ttu-id="fbaab-137">L’exemple C# suivant valide une image de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="fbaab-137">The following C# example validates a virtual hard disk image.</span></span> <span data-ttu-id="fbaab-138">Les utilitaires référencés se trouvent dans [les utilitaires courants pour les exemples de virtualisation (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="fbaab-138">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public static void ValidateVirtualHardDisk(string vhdPath)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("ValidateVirtualHardDisk");
    inParams["Path"] = vhdPath;
    ManagementBaseObject outParams = imageService.InvokeMethod("ValidateVirtualHardDisk", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} is a valid virtual hard disk.", inParams["Path"]);
        }
        else
        {
            Console.WriteLine("Unable to validate {0}", inParams["Path"]);
        }
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="fbaab-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fbaab-139">Requirements</span></span>



| <span data-ttu-id="fbaab-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fbaab-140">Requirement</span></span> | <span data-ttu-id="fbaab-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="fbaab-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbaab-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fbaab-142">Minimum supported client</span></span><br/> | <span data-ttu-id="fbaab-143">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fbaab-143">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fbaab-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fbaab-144">Minimum supported server</span></span><br/> | <span data-ttu-id="fbaab-145">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fbaab-145">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fbaab-146">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fbaab-146">Namespace</span></span><br/>                | <span data-ttu-id="fbaab-147">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="fbaab-147">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fbaab-148">MOF</span><span class="sxs-lookup"><span data-stu-id="fbaab-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fbaab-149"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fbaab-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fbaab-150">DLL</span><span class="sxs-lookup"><span data-stu-id="fbaab-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbaab-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fbaab-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fbaab-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fbaab-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbaab-153">**ValidateVirtualHardDisk (v1)**</span><span class="sxs-lookup"><span data-stu-id="fbaab-153">**ValidateVirtualHardDisk (V1)**</span></span>](/previous-versions/windows/desktop/virtual/validatevirtualharddisk-msvm-imagemanagementservice)
</dt> <dt>

<span data-ttu-id="fbaab-154">[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fbaab-154">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="fbaab-155">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="fbaab-155">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

