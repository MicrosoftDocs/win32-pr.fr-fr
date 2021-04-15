---
description: Définit un système virtuel planifié.
ms.assetid: f129554b-e43e-4c3a-8418-d5d810f4c4b5
title: Méthode DefinePlannedSystem de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DefinePlannedSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d5e9fa8a49e86850d044216a3d95e3d4dd756fc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525204"
---
# <a name="defineplannedsystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="a9425-103">Méthode DefinePlannedSystem de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="a9425-103">DefinePlannedSystem method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="a9425-104">Définit un système virtuel planifié.</span><span class="sxs-lookup"><span data-stu-id="a9425-104">Defines a planned virtual system.</span></span>

<span data-ttu-id="a9425-105">L’entrée qui n’est pas complètement spécifiée peut être remplie avec des valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="a9425-105">Input that is not completely specified may be filled out with default values.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9425-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a9425-106">Syntax</span></span>


```mof
uint32 DefinePlannedSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="a9425-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a9425-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9425-108">*SystemSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a9425-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9425-109">Paramètres système du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="a9425-109">The system settings for the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="a9425-110">*ResourceSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a9425-110">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9425-111">Paramètres de ressource pour le système virtuel.</span><span class="sxs-lookup"><span data-stu-id="a9425-111">The resource settings for the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="a9425-112">*ReferenceConfiguration* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a9425-112">*ReferenceConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9425-113">[**\_ VirtualSystemSettingData CIM**](cim-virtualsystemsettingdata.md) contenant la configuration de référence.</span><span class="sxs-lookup"><span data-stu-id="a9425-113">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) containing the reference configuration.</span></span>

</dd> <dt>

<span data-ttu-id="a9425-114">*ResultingSystem* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a9425-114">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9425-115">Un [**\_ ComputerSystem CIM**](cim-computersystem.md) contenant le système résultant.</span><span class="sxs-lookup"><span data-stu-id="a9425-115">A [**CIM\_ComputerSystem**](cim-computersystem.md) containing the resulting system.</span></span>

</dd> <dt>

<span data-ttu-id="a9425-116">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a9425-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9425-117">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a9425-117">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9425-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a9425-118">Return value</span></span>

<span data-ttu-id="a9425-119">En cas de réussite, retourne 0 ou 4096 ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="a9425-119">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="a9425-120">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="a9425-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a9425-121">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="a9425-121">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a9425-122">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="a9425-122">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a9425-123">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="a9425-123">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a9425-124">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="a9425-124">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a9425-125">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="a9425-125">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a9425-126">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="a9425-126">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a9425-127">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="a9425-127">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="a9425-128">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="a9425-128">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a9425-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a9425-129">Requirements</span></span>



| <span data-ttu-id="a9425-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a9425-130">Requirement</span></span> | <span data-ttu-id="a9425-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9425-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9425-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9425-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a9425-133">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a9425-133">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="a9425-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9425-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a9425-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a9425-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="a9425-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a9425-136">Namespace</span></span><br/>                | <span data-ttu-id="a9425-137">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="a9425-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a9425-138">MOF</span><span class="sxs-lookup"><span data-stu-id="a9425-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9425-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a9425-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a9425-140">DLL</span><span class="sxs-lookup"><span data-stu-id="a9425-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9425-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a9425-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a9425-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9425-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9425-143">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="a9425-143">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

