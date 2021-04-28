---
description: La méthode ModifyResourceSettings de la classe Msvm_VirtualSystemManagementService-modifie les paramètres de ressource virtuelle.
ms.assetid: 3fb2a65f-9f40-4eb9-99e8-8fe1451427d9
title: Méthode ModifyResourceSettings de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 09ca0bb9fea02b6acc5599d9f907b1e60fdbd9ec
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119337"
---
# <a name="modifyresourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="86450-103">Méthode ModifyResourceSettings de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="86450-103">ModifyResourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="86450-104">Modifie les paramètres de ressource virtuelle.</span><span class="sxs-lookup"><span data-stu-id="86450-104">Modifies virtual resource settings.</span></span> <span data-ttu-id="86450-105">En cas d’application à des parties d’une configuration d’ordinateur virtuel active, en tant qu’effet secondaire, les ressources de la machine virtuelle active peuvent être modifiées.</span><span class="sxs-lookup"><span data-stu-id="86450-105">When applied to parts of a current virtual machine configuration, as a side effect, the resources of the active virtual machine may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="86450-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86450-106">Syntax</span></span>


```mof
uint32 ModifyResourceSettings(
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="86450-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="86450-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86450-108">*ResourceSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="86450-108">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86450-109">Tableau de chaînes qui contient une instance incorporée d’une classe dérivée de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), qui contient les aspects modifiés des ressources virtuelles existantes.</span><span class="sxs-lookup"><span data-stu-id="86450-109">An array of strings that contain an embedded instance of a class derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), that contain the modified aspects of existing virtual resources.</span></span> <span data-ttu-id="86450-110">La propriété **InstanceID** de chaque instance identifie le paramètre de ressource virtuelle à modifier.</span><span class="sxs-lookup"><span data-stu-id="86450-110">The **InstanceID** property of each instance identifies the virtual resource setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="86450-111">*ResultingResourceSettings* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="86450-111">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86450-112">Tableau de références aux instances d’objets dérivés de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) représentant les aspects virtuels des ressources virtuelles modifiées.</span><span class="sxs-lookup"><span data-stu-id="86450-112">An array of references to instances of objects derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) representing virtual aspects of the modified virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="86450-113">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="86450-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86450-114">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="86450-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86450-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="86450-115">Return value</span></span>

<span data-ttu-id="86450-116">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="86450-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="86450-117">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="86450-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="86450-118">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="86450-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="86450-119">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="86450-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="86450-120">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="86450-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="86450-121">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="86450-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="86450-122">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="86450-122">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="86450-123">**Paramètres incompatibles** (6)</span><span class="sxs-lookup"><span data-stu-id="86450-123">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="86450-124">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="86450-124">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="86450-125">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="86450-125">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="86450-126">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="86450-126">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="86450-127">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="86450-127">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="86450-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86450-128">Requirements</span></span>



| <span data-ttu-id="86450-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="86450-129">Requirement</span></span> | <span data-ttu-id="86450-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="86450-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86450-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86450-131">Minimum supported client</span></span><br/> | <span data-ttu-id="86450-132">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="86450-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="86450-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86450-133">Minimum supported server</span></span><br/> | <span data-ttu-id="86450-134">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="86450-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="86450-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="86450-135">Namespace</span></span><br/>                | <span data-ttu-id="86450-136">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="86450-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="86450-137">MOF</span><span class="sxs-lookup"><span data-stu-id="86450-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="86450-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="86450-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="86450-139">DLL</span><span class="sxs-lookup"><span data-stu-id="86450-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86450-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="86450-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="86450-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86450-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86450-142">**ModifyVirtualSystemResources (v1)**</span><span class="sxs-lookup"><span data-stu-id="86450-142">**ModifyVirtualSystemResources (V1)**</span></span>](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="86450-143">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="86450-143">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

