---
description: Supprime les paramètres de ressources virtuelles d’une configuration d’ordinateur virtuel.
ms.assetid: 74d9a70a-5258-4e4b-8131-b25513d11a4b
title: Méthode RemoveResourceSettings de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 20a7c9fb10e4f7a6356e47f8c743266095de2042
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533745"
---
# <a name="removeresourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="e1e0f-103">Méthode RemoveResourceSettings de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="e1e0f-103">RemoveResourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="e1e0f-104">Supprime les paramètres de ressources virtuelles d’une configuration d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="e1e0f-104">Removes virtual resource settings from a virtual machine configuration.</span></span> <span data-ttu-id="e1e0f-105">En cas d’application à des parties d’une configuration d’ordinateur virtuel active, la machine virtuelle active peut être supprimée.</span><span class="sxs-lookup"><span data-stu-id="e1e0f-105">When applied to parts of a current virtual machine configuration, the active virtual machine may be removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1e0f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1e0f-106">Syntax</span></span>


```mof
uint32 RemoveResourceSettings(
  [in]  CIM_ResourceAllocationSettingData REF ResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="e1e0f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e1e0f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1e0f-108">*ResourceSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e1e0f-108">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1e0f-109">Tableau de références aux instances de la classe [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) , où chaque instance représente les paramètres d’une ressource virtuelle dans une configuration d’ordinateur virtuel qui doit être supprimée.</span><span class="sxs-lookup"><span data-stu-id="e1e0f-109">An array of references to instances of the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class, where each instance represents the settings of a virtual resource within a virtual machine configuration that are to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="e1e0f-110">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e1e0f-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1e0f-111">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e1e0f-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1e0f-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e1e0f-112">Return value</span></span>

<span data-ttu-id="e1e0f-113">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e1e0f-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e1e0f-114">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="e1e0f-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e1e0f-115">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="e1e0f-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e1e0f-116">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="e1e0f-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e1e0f-117">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="e1e0f-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e1e0f-118">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="e1e0f-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e1e0f-119">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="e1e0f-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e1e0f-120">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="e1e0f-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e1e0f-121">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="e1e0f-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e1e0f-122">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="e1e0f-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="e1e0f-123">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="e1e0f-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e1e0f-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1e0f-124">Requirements</span></span>



| <span data-ttu-id="e1e0f-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1e0f-125">Requirement</span></span> | <span data-ttu-id="e1e0f-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1e0f-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1e0f-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1e0f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e1e0f-128">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e1e0f-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e1e0f-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1e0f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e1e0f-130">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e1e0f-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e1e0f-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e1e0f-131">Namespace</span></span><br/>                | <span data-ttu-id="e1e0f-132">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="e1e0f-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e1e0f-133">MOF</span><span class="sxs-lookup"><span data-stu-id="e1e0f-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e1e0f-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0f-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e1e0f-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e1e0f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1e0f-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0f-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e1e0f-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1e0f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1e0f-138">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="e1e0f-138">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

