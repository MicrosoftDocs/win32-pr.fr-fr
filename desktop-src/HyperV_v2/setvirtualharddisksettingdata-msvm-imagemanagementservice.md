---
description: Met à jour les paramètres d’un disque dur virtuel.
ms.assetid: 10f80313-bc78-447e-bdf2-5635d7354e3c
title: Méthode SetVirtualHardDiskSettingData de la classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.SetVirtualHardDiskSettingData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 969e9019d05b49f2f171f2177e1e74f135e212da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320589"
---
# <a name="setvirtualharddisksettingdata-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="25fe4-103">Méthode SetVirtualHardDiskSettingData de la \_ classe ImageManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="25fe4-103">SetVirtualHardDiskSettingData method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="25fe4-104">Met à jour les paramètres d’un disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="25fe4-104">Updates the settings for a virtual hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="25fe4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25fe4-105">Syntax</span></span>


```mof
uint32 SetVirtualHardDiskSettingData(
  [in]  string              VirtualDiskSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="25fe4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="25fe4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25fe4-107">*VirtualDiskSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="25fe4-107">*VirtualDiskSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25fe4-108">Représentation sous forme de chaîne de la classe [**MSVM \_ VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) qui spécifie le disque dur virtuel à mettre à jour et qui contient les nouvelles données de paramètre.</span><span class="sxs-lookup"><span data-stu-id="25fe4-108">A string representation of the [**Msvm\_VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) class that specifies the virtual hard disk to update and that contains the new setting data.</span></span> <span data-ttu-id="25fe4-109">Seules les propriétés **ParentPath**, **PhysicalSectorSize** ou **VirtualDiskId** peuvent être mises à jour avec cette méthode.</span><span class="sxs-lookup"><span data-stu-id="25fe4-109">Only the **ParentPath**, **PhysicalSectorSize**, or **VirtualDiskId** properties can be updated with this method.</span></span> <span data-ttu-id="25fe4-110">Vous ne pouvez pas mettre à jour ces propriétés avec un appel de méthode.</span><span class="sxs-lookup"><span data-stu-id="25fe4-110">You can't update these properties with one method call.</span></span> <span data-ttu-id="25fe4-111">Vous pouvez uniquement mettre à jour l’une de ces propriétés à l’aide d’un seul appel de méthode.</span><span class="sxs-lookup"><span data-stu-id="25fe4-111">You can only update one of these properties with a single method call.</span></span>

</dd> <dt>

<span data-ttu-id="25fe4-112">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="25fe4-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25fe4-113">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="25fe4-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25fe4-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="25fe4-114">Return value</span></span>

<span data-ttu-id="25fe4-115">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="25fe4-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="25fe4-116">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="25fe4-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="25fe4-117">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="25fe4-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="25fe4-118">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="25fe4-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="25fe4-119">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="25fe4-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="25fe4-120">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="25fe4-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="25fe4-121">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="25fe4-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="25fe4-122">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="25fe4-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="25fe4-123">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="25fe4-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="25fe4-124">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="25fe4-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="25fe4-125">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="25fe4-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="25fe4-126">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="25fe4-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="25fe4-127">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="25fe4-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="25fe4-128">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="25fe4-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="25fe4-129">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="25fe4-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="25fe4-130">Notes</span><span class="sxs-lookup"><span data-stu-id="25fe4-130">Remarks</span></span>

<span data-ttu-id="25fe4-131">L’accès à la classe [**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="25fe4-131">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="25fe4-132">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="25fe4-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="25fe4-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25fe4-133">Requirements</span></span>



| <span data-ttu-id="25fe4-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25fe4-134">Requirement</span></span> | <span data-ttu-id="25fe4-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="25fe4-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25fe4-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25fe4-136">Minimum supported client</span></span><br/> | <span data-ttu-id="25fe4-137">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="25fe4-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="25fe4-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25fe4-138">Minimum supported server</span></span><br/> | <span data-ttu-id="25fe4-139">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="25fe4-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="25fe4-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="25fe4-140">Namespace</span></span><br/>                | <span data-ttu-id="25fe4-141">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="25fe4-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="25fe4-142">MOF</span><span class="sxs-lookup"><span data-stu-id="25fe4-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="25fe4-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="25fe4-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="25fe4-144">DLL</span><span class="sxs-lookup"><span data-stu-id="25fe4-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25fe4-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="25fe4-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="25fe4-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25fe4-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25fe4-147">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="25fe4-147">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

