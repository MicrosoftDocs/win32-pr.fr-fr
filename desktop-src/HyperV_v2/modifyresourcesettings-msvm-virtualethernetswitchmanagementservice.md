---
description: Modifie les paramètres de ressource pour un commutateur virtuel.
ms.assetid: 1ae2456f-921c-4ea6-b3fb-7065110063fb
title: Méthode ModifyResourceSettings de la classe Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.ModifyResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f40044b20389914281ad4f651019f3e8dc6b6148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534655"
---
# <a name="modifyresourcesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="61ae8-103">Méthode ModifyResourceSettings de la \_ classe VirtualEthernetSwitchManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="61ae8-103">ModifyResourceSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="61ae8-104">Modifie les paramètres de ressource pour un commutateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="61ae8-104">Modifies resource settings for a virtual switch.</span></span>

## <a name="syntax"></a><span data-ttu-id="61ae8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61ae8-105">Syntax</span></span>


```mof
uint32 ModifyResourceSettings(
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="61ae8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="61ae8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61ae8-107">*ResourceSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="61ae8-107">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61ae8-108">Tableau de chaînes qui contient une instance incorporée d’une classe dérivée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), qui contient les aspects modifiés des ressources virtuelles existantes.</span><span class="sxs-lookup"><span data-stu-id="61ae8-108">An array of strings that contain an embedded instance of a class derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), that contain the modified aspects of existing virtual resources.</span></span> <span data-ttu-id="61ae8-109">La propriété **InstanceID** de chaque instance identifie le paramètre de ressource virtuelle à modifier.</span><span class="sxs-lookup"><span data-stu-id="61ae8-109">The **InstanceID** property of each instance identifies the virtual resource setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="61ae8-110">*ResultingResourceSettings* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="61ae8-110">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61ae8-111">Tableau de références aux instances d’objets dérivés de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) représentant les aspects virtuels des ressources virtuelles modifiées.</span><span class="sxs-lookup"><span data-stu-id="61ae8-111">An array of references to instances of objects derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) representing virtual aspects of the modified virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="61ae8-112">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="61ae8-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61ae8-113">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="61ae8-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61ae8-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="61ae8-114">Return value</span></span>

<span data-ttu-id="61ae8-115">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="61ae8-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="61ae8-116">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="61ae8-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="61ae8-117">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="61ae8-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="61ae8-118">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="61ae8-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="61ae8-119">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="61ae8-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="61ae8-120">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="61ae8-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="61ae8-121">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="61ae8-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="61ae8-122">**Paramètres incompatibles** (6)</span><span class="sxs-lookup"><span data-stu-id="61ae8-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="61ae8-123">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="61ae8-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="61ae8-124">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="61ae8-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="61ae8-125">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="61ae8-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="61ae8-126">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="61ae8-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="61ae8-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="61ae8-127">Requirements</span></span>



| <span data-ttu-id="61ae8-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="61ae8-128">Requirement</span></span> | <span data-ttu-id="61ae8-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="61ae8-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61ae8-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61ae8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="61ae8-131">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="61ae8-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="61ae8-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61ae8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="61ae8-133">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="61ae8-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="61ae8-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="61ae8-134">Namespace</span></span><br/>                | <span data-ttu-id="61ae8-135">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="61ae8-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="61ae8-136">MOF</span><span class="sxs-lookup"><span data-stu-id="61ae8-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61ae8-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="61ae8-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="61ae8-138">DLL</span><span class="sxs-lookup"><span data-stu-id="61ae8-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61ae8-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="61ae8-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="61ae8-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61ae8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61ae8-141">**AddResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="61ae8-141">**AddResourceSettings**</span></span>](addresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="61ae8-142">**RemoveResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="61ae8-142">**RemoveResourceSettings**</span></span>](removeresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="61ae8-143">**MSVM \_ VirtualEthernetSwitchManagementService**</span><span class="sxs-lookup"><span data-stu-id="61ae8-143">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

