---
description: Récupère les informations d’état d’un fichier de disque dur virtuel.
ms.assetid: 398b098b-dc1a-45e0-abcb-37b4b0a32290
title: Méthode GetVirtualHardDiskState de la classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVirtualHardDiskState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e608078b88415eb683a95e3ba41d81b99014961d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519438"
---
# <a name="getvirtualharddiskstate-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="beb03-103">Méthode GetVirtualHardDiskState de la \_ classe ImageManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="beb03-103">GetVirtualHardDiskState method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="beb03-104">Récupère les informations d’état d’un fichier de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="beb03-104">Retrieves state information for a virtual hard disk file.</span></span>

## <a name="syntax"></a><span data-ttu-id="beb03-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="beb03-105">Syntax</span></span>


```mof
uint32 GetVirtualHardDiskState(
  [in]  string              Path,
  [out] string              State,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="beb03-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="beb03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="beb03-107">*Chemin d’accès* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="beb03-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beb03-108">Chemin d’accès complet du fichier image de disque.</span><span class="sxs-lookup"><span data-stu-id="beb03-108">The fully qualified path of the disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="beb03-109">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="beb03-109">*State* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="beb03-110">En cas de réussite, reçoit une instance incorporée de la classe [**MSVM \_ VirtualHardDiskState**](msvm-virtualharddiskstate.md) qui contient les informations d’État du disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="beb03-110">If successful, receives an embedded instance of the [**Msvm\_VirtualHardDiskState**](msvm-virtualharddiskstate.md) class that contains the state information for the virtual hard disk.</span></span>

</dd> <dt>

<span data-ttu-id="beb03-111">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="beb03-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="beb03-112">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="beb03-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="beb03-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="beb03-113">Return value</span></span>

<span data-ttu-id="beb03-114">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="beb03-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="beb03-115">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="beb03-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="beb03-116">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="beb03-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="beb03-117">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="beb03-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="beb03-118">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="beb03-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="beb03-119">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="beb03-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="beb03-120">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="beb03-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="beb03-121">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="beb03-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="beb03-122">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="beb03-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="beb03-123">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="beb03-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="beb03-124">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="beb03-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="beb03-125">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="beb03-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="beb03-126">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="beb03-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="beb03-127">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="beb03-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="beb03-128">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="beb03-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="beb03-129">Notes</span><span class="sxs-lookup"><span data-stu-id="beb03-129">Remarks</span></span>

<span data-ttu-id="beb03-130">L’accès à la classe [**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="beb03-130">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="beb03-131">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="beb03-131">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="beb03-132">Exemples</span><span class="sxs-lookup"><span data-stu-id="beb03-132">Examples</span></span>

<span data-ttu-id="beb03-133">L’exemple C# suivant montre comment appeler la méthode **GetVirtualHardDiskState** .</span><span class="sxs-lookup"><span data-stu-id="beb03-133">The following C# example shows how to call the **GetVirtualHardDiskState** method.</span></span> <span data-ttu-id="beb03-134">Les utilitaires référencés se trouvent dans [les utilitaires courants pour les exemples de virtualisation (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="beb03-134">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public static void GetVirtualHardDiskState(string vhdPath)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");
    ManagementBaseObject inParams = imageService.GetMethodParameters("GetVirtualHardDiskState");

    inParams["Path"] = vhdPath;
    
    ManagementBaseObject outParams = imageService.InvokeMethod("GetVirtualHardDiskState", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("GetVirtualHardDiskState was successful.");
        }
        else
        {
            Console.WriteLine("GetVirtualHardDiskState was not successful.");
        }
    }
    else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
    {
        string diskStateString = outParams["State"].ToString();
        Utility.PrintEmbeddedInstance(diskStateString);
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="beb03-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="beb03-135">Requirements</span></span>



| <span data-ttu-id="beb03-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="beb03-136">Requirement</span></span> | <span data-ttu-id="beb03-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="beb03-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="beb03-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="beb03-138">Minimum supported client</span></span><br/> | <span data-ttu-id="beb03-139">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="beb03-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="beb03-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="beb03-140">Minimum supported server</span></span><br/> | <span data-ttu-id="beb03-141">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="beb03-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="beb03-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="beb03-142">Namespace</span></span><br/>                | <span data-ttu-id="beb03-143">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="beb03-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="beb03-144">MOF</span><span class="sxs-lookup"><span data-stu-id="beb03-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="beb03-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="beb03-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="beb03-146">DLL</span><span class="sxs-lookup"><span data-stu-id="beb03-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="beb03-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="beb03-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="beb03-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="beb03-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beb03-149">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="beb03-149">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

