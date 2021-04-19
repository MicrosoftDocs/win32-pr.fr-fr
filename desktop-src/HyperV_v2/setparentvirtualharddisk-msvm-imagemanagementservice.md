---
description: Met à jour le parent pour les fichiers de disque dur virtuel enfants et de feuille spécifiés.
ms.assetid: 5ad41218-bcfd-449a-a66e-2096a1d96bf5
title: Méthode SetParentVirtualHardDisk de la classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.SetParentVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f1d14d3b2ee19a9768e1ee9ed9333a452153cc9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517836"
---
# <a name="setparentvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="dc7ff-103">Méthode SetParentVirtualHardDisk de la \_ classe ImageManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="dc7ff-103">SetParentVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="dc7ff-104">Met à jour le parent pour les fichiers de disque dur virtuel enfants et de feuille spécifiés.</span><span class="sxs-lookup"><span data-stu-id="dc7ff-104">Updates the parent for the specified leaf and child virtual hard disk files.</span></span> <span data-ttu-id="dc7ff-105">Consultez la section Notes pour connaître les restrictions d’utilisation de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="dc7ff-105">See Remarks for usage restrictions for this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc7ff-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dc7ff-106">Syntax</span></span>


```mof
uint32 SetParentVirtualHardDisk(
  [in]  string              ChildPath,
  [in]  string              ParentPath,
  [in]  string              LeafPath,
  [in]  boolean             IgnoreIDMismatch,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="dc7ff-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dc7ff-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc7ff-108">*Childpath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dc7ff-108">*ChildPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc7ff-109">Chemin qualifié complet qui spécifie l’emplacement du fichier de disque dur virtuel enfant.</span><span class="sxs-lookup"><span data-stu-id="dc7ff-109">A fully qualified path that specifies the location of the child virtual hard disk file.</span></span>

</dd> <dt>

<span data-ttu-id="dc7ff-110">*ParentPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dc7ff-110">*ParentPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc7ff-111">Chemin qualifié complet qui spécifie l’emplacement du fichier de disque dur virtuel parent.</span><span class="sxs-lookup"><span data-stu-id="dc7ff-111">A fully qualified path that specifies the location of the parent virtual hard disk file.</span></span>

</dd> <dt>

<span data-ttu-id="dc7ff-112">*LeafPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dc7ff-112">*LeafPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc7ff-113">Chemin qualifié complet qui spécifie l’emplacement du fichier de disque dur virtuel feuille.</span><span class="sxs-lookup"><span data-stu-id="dc7ff-113">A fully qualified path that specifies the location of the leaf virtual hard disk file.</span></span> <span data-ttu-id="dc7ff-114">Le paramètre peut avoir la **valeur null** si le disque dur virtuel est hors connexion, mais doit être spécifié si le disque dur virtuel est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="dc7ff-114">The parameter can be **Null** if the virtual hard disk is offline, but must be specified if the virtual hard disk is in use.</span></span>

</dd> <dt>

<span data-ttu-id="dc7ff-115">*IgnoreIDMismatch* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dc7ff-115">*IgnoreIDMismatch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc7ff-116">Indique si le parent doit être défini de force lorsque les identificateurs de disque virtuel ne correspondent pas.</span><span class="sxs-lookup"><span data-stu-id="dc7ff-116">Indicates if the parent should be forcibly set when the virtual disk identifiers do not match.</span></span> <span data-ttu-id="dc7ff-117">Ce paramètre doit être utilisé avec précaution, car si le nouveau disque dur virtuel parent n’est pas identique au parent d’origine, des données peuvent être endommagées.</span><span class="sxs-lookup"><span data-stu-id="dc7ff-117">This parameter must be used with caution because if the new parent virtual hard disk is not identical to the original parent, data corruption can occur.</span></span>

</dd> <dt>

<span data-ttu-id="dc7ff-118">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="dc7ff-118">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc7ff-119">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dc7ff-119">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc7ff-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dc7ff-120">Return value</span></span>

<span data-ttu-id="dc7ff-121">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="dc7ff-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="dc7ff-122">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="dc7ff-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dc7ff-123">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="dc7ff-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="dc7ff-124">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="dc7ff-124">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="dc7ff-125">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="dc7ff-125">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="dc7ff-126">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="dc7ff-126">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="dc7ff-127">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="dc7ff-127">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="dc7ff-128">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="dc7ff-128">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="dc7ff-129">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="dc7ff-129">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="dc7ff-130">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="dc7ff-130">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="dc7ff-131">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="dc7ff-131">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="dc7ff-132">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="dc7ff-132">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="dc7ff-133">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="dc7ff-133">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="dc7ff-134">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="dc7ff-134">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="dc7ff-135">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="dc7ff-135">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="dc7ff-136">Notes</span><span class="sxs-lookup"><span data-stu-id="dc7ff-136">Remarks</span></span>

<span data-ttu-id="dc7ff-137">Seuls les types de disques durs virtuels suivants peuvent être utilisés avec cette méthode :</span><span class="sxs-lookup"><span data-stu-id="dc7ff-137">Only the following types of virtual hard disks can be used with this method:</span></span>

-   <span data-ttu-id="dc7ff-138">Disque dur virtuel de différenciation</span><span class="sxs-lookup"><span data-stu-id="dc7ff-138">Differencing VHD</span></span>
-   <span data-ttu-id="dc7ff-139">VHDX de différenciation</span><span class="sxs-lookup"><span data-stu-id="dc7ff-139">Differencing VHDX</span></span>

<span data-ttu-id="dc7ff-140">L’accès à la classe [**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="dc7ff-140">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="dc7ff-141">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="dc7ff-141">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="dc7ff-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dc7ff-142">Requirements</span></span>



| <span data-ttu-id="dc7ff-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dc7ff-143">Requirement</span></span> | <span data-ttu-id="dc7ff-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc7ff-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc7ff-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc7ff-145">Minimum supported client</span></span><br/> | <span data-ttu-id="dc7ff-146">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc7ff-146">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="dc7ff-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc7ff-147">Minimum supported server</span></span><br/> | <span data-ttu-id="dc7ff-148">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc7ff-148">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dc7ff-149">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="dc7ff-149">Namespace</span></span><br/>                | <span data-ttu-id="dc7ff-150">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="dc7ff-150">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="dc7ff-151">MOF</span><span class="sxs-lookup"><span data-stu-id="dc7ff-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc7ff-152"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dc7ff-152"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc7ff-153">DLL</span><span class="sxs-lookup"><span data-stu-id="dc7ff-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc7ff-154"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dc7ff-154"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dc7ff-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc7ff-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc7ff-156">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="dc7ff-156">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

