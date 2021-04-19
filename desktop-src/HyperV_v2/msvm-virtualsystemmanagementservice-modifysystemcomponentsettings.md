---
description: Modifie les paramètres génériques des composants système.
ms.assetid: e745be32-c26a-4343-99c8-950788243adf
title: Méthode ModifySystemComponentSettings de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifySystemComponentSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e9495256d1b7610bebdac1fb2cc8b70960a63304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529106"
---
# <a name="modifysystemcomponentsettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="e025b-103">Méthode ModifySystemComponentSettings de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="e025b-103">ModifySystemComponentSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="e025b-104">Modifie les paramètres génériques des composants système.</span><span class="sxs-lookup"><span data-stu-id="e025b-104">Modifies generic system component settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="e025b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e025b-105">Syntax</span></span>


```mof
uint32 ModifySystemComponentSettings(
  [in]  string                              ComponentSettings[],
  [out] Msvm_SystemComponentSettingData REF ResultingComponentSettings[],
  [out] CIM_ConcreteJob                 REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="e025b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e025b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e025b-107">*ComponentSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e025b-107">*ComponentSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e025b-108">Tableau de paramètres de composant à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="e025b-108">An array of component settings to update.</span></span>

</dd> <dt>

<span data-ttu-id="e025b-109">*ResultingComponentSettings* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e025b-109">*ResultingComponentSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e025b-110">En cas de réussite, retourne un tableau de [**\_ SystemComponentSettingData MSVM**](msvm-systemcomponentsettingdata.md) qui référencent les paramètres de composant résultants.</span><span class="sxs-lookup"><span data-stu-id="e025b-110">On success, returns an array of [**Msvm\_SystemComponentSettingData**](msvm-systemcomponentsettingdata.md) that reference the resulting component settings.</span></span>

</dd> <dt>

<span data-ttu-id="e025b-111">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e025b-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e025b-112">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e025b-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e025b-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e025b-113">Return value</span></span>

<span data-ttu-id="e025b-114">En cas de réussite, retourne 0 ou 4096 ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="e025b-114">On success, returns a 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="e025b-115">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="e025b-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e025b-116">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="e025b-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e025b-117">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="e025b-117">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e025b-118">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="e025b-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e025b-119">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="e025b-119">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e025b-120">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="e025b-120">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e025b-121">**Paramètres incompatibles** (6)</span><span class="sxs-lookup"><span data-stu-id="e025b-121">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="e025b-122">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="e025b-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e025b-123">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="e025b-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e025b-124">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="e025b-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="e025b-125">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="e025b-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e025b-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e025b-126">Requirements</span></span>



| <span data-ttu-id="e025b-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e025b-127">Requirement</span></span> | <span data-ttu-id="e025b-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="e025b-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e025b-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e025b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e025b-130">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e025b-130">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e025b-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e025b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e025b-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e025b-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e025b-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e025b-133">Namespace</span></span><br/>                | <span data-ttu-id="e025b-134">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="e025b-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e025b-135">MOF</span><span class="sxs-lookup"><span data-stu-id="e025b-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e025b-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e025b-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e025b-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e025b-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e025b-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e025b-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e025b-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e025b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e025b-140">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="e025b-140">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

