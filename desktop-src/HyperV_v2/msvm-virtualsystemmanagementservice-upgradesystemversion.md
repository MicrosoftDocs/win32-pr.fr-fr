---
description: Met à niveau le système virtuel.
ms.assetid: 4b24aac9-b7b9-460f-9227-fd3c1e960191
title: Méthode UpgradeSystemVersion de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.UpgradeSystemVersion
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4c34b33da14d8718f2c2414de3aea3079672bbb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514579"
---
# <a name="upgradesystemversion-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="fd976-103">Méthode UpgradeSystemVersion de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="fd976-103">UpgradeSystemVersion method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="fd976-104">Met à niveau le système virtuel.</span><span class="sxs-lookup"><span data-stu-id="fd976-104">Upgrades the virtual system.</span></span>

<span data-ttu-id="fd976-105">En cas d’application aux paramètres système d’une configuration de système virtuel « en cours »</span><span class="sxs-lookup"><span data-stu-id="fd976-105">When applied to the system settings of a "current" virtual system configuration</span></span>

## <a name="syntax"></a><span data-ttu-id="fd976-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd976-106">Syntax</span></span>


```mof
uint32 UpgradeSystemVersion(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 UpgradeSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="fd976-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd976-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd976-108">*ComputerSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fd976-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd976-109">Référence à un [**\_ ComputerSystem CIM**](cim-computersystem.md) qui représente le système d’ordinateur virtuel à mettre à niveau.</span><span class="sxs-lookup"><span data-stu-id="fd976-109">A reference to a [**CIM\_ComputerSystem**](cim-computersystem.md) that represents the virtual computer system to be upgraded.</span></span>

</dd> <dt>

<span data-ttu-id="fd976-110">*UpgradeSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fd976-110">*UpgradeSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd976-111">Données du paramètre de mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="fd976-111">The upgrade setting data.</span></span>

</dd> <dt>

<span data-ttu-id="fd976-112">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fd976-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd976-113">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fd976-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd976-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fd976-114">Return value</span></span>

<span data-ttu-id="fd976-115">En cas de réussite, retourne 0 ou 4096 ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="fd976-115">On success, returns a 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="fd976-116">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="fd976-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fd976-117">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="fd976-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fd976-118">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="fd976-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fd976-119">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="fd976-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fd976-120">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="fd976-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fd976-121">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="fd976-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="fd976-122">**Paramètres incompatibles** (6)</span><span class="sxs-lookup"><span data-stu-id="fd976-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="fd976-123">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="fd976-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="fd976-124">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="fd976-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="fd976-125">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="fd976-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="fd976-126">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="fd976-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="fd976-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd976-127">Requirements</span></span>



| <span data-ttu-id="fd976-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd976-128">Requirement</span></span> | <span data-ttu-id="fd976-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd976-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd976-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd976-130">Minimum supported client</span></span><br/> | <span data-ttu-id="fd976-131">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd976-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="fd976-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd976-132">Minimum supported server</span></span><br/> | <span data-ttu-id="fd976-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="fd976-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="fd976-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fd976-134">Namespace</span></span><br/>                | <span data-ttu-id="fd976-135">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="fd976-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fd976-136">MOF</span><span class="sxs-lookup"><span data-stu-id="fd976-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd976-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd976-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd976-138">DLL</span><span class="sxs-lookup"><span data-stu-id="fd976-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd976-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fd976-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fd976-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd976-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd976-141">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="fd976-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

