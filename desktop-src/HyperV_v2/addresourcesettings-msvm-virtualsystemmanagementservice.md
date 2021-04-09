---
description: Ajoute des ressources à une configuration d’ordinateur virtuel.
ms.assetid: e2878b60-dc8c-48fb-b163-29457a96d130
title: Méthode AddResourceSettings de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4b35379e0fe3925bbf0f7c4d753f77d1d207199b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865225"
---
# <a name="addresourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="cdf60-103">Méthode AddResourceSettings de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="cdf60-103">AddResourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="cdf60-104">Ajoute des ressources à une configuration d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="cdf60-104">Adds resources to a virtual machine configuration.</span></span> <span data-ttu-id="cdf60-105">En cas d’application à une configuration d’ordinateur virtuel « État », en tant qu’effet secondaire, les ressources sont ajoutées à la machine virtuelle active.</span><span class="sxs-lookup"><span data-stu-id="cdf60-105">When applied to a "state" virtual machine configuration, as a side effect, resources are added to the active virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdf60-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cdf60-106">Syntax</span></span>


```mof
uint32 AddResourceSettings(
  [in]  CIM_VirtualSystemSettingData      REF AffectedConfiguration,
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="cdf60-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cdf60-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdf60-108">*AffectedConfiguration* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cdf60-108">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdf60-109">Référence à un objet [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)) qui représente la configuration d’ordinateur virtuel affectée.</span><span class="sxs-lookup"><span data-stu-id="cdf60-109">A reference to a [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) object that represents the affected virtual machine configuration.</span></span>

</dd> <dt>

<span data-ttu-id="cdf60-110">*ResourceSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cdf60-110">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdf60-111">Tableau de chaînes qui contient une instance incorporée de la [**classe \_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) qui décrit les aspects virtuels d’une ressource virtuelle à ajouter à la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="cdf60-111">An array of strings that contain one embedded instance of the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class that describes the virtual aspects of a virtual resource to be added to the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="cdf60-112">*ResultingResourceSettings* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cdf60-112">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cdf60-113">Tableau de références aux instances de la classe [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) qui représente les aspects virtuels des ressources virtuelles ajoutées.</span><span class="sxs-lookup"><span data-stu-id="cdf60-113">An array of references to instances of the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class that represents virtual aspects of the added virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="cdf60-114">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cdf60-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cdf60-115">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cdf60-115">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdf60-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cdf60-116">Return value</span></span>

<span data-ttu-id="cdf60-117">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="cdf60-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="cdf60-118">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="cdf60-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cdf60-119">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="cdf60-119">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="cdf60-120">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="cdf60-120">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="cdf60-121">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="cdf60-121">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="cdf60-122">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="cdf60-122">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="cdf60-123">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="cdf60-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="cdf60-124">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="cdf60-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="cdf60-125">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="cdf60-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="cdf60-126">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="cdf60-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="cdf60-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cdf60-127">Requirements</span></span>



| <span data-ttu-id="cdf60-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cdf60-128">Requirement</span></span> | <span data-ttu-id="cdf60-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="cdf60-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdf60-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cdf60-130">Minimum supported client</span></span><br/> | <span data-ttu-id="cdf60-131">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cdf60-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="cdf60-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cdf60-132">Minimum supported server</span></span><br/> | <span data-ttu-id="cdf60-133">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cdf60-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cdf60-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cdf60-134">Namespace</span></span><br/>                | <span data-ttu-id="cdf60-135">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="cdf60-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="cdf60-136">MOF</span><span class="sxs-lookup"><span data-stu-id="cdf60-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cdf60-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cdf60-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cdf60-138">DLL</span><span class="sxs-lookup"><span data-stu-id="cdf60-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cdf60-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cdf60-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cdf60-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cdf60-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdf60-141">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="cdf60-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

