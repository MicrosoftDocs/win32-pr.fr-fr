---
description: Crée un point de référence d’un système virtuel.
ms.assetid: 9cc7665a-9562-4267-bcd0-3162e426fbad
title: Méthode CreateReferencePoint de la classe Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.CreateReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 08d28970288ba62346894d758ebac5ac156962ff
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106524773"
---
# <a name="createreferencepoint-method-of-the-msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="ebd36-103">Méthode CreateReferencePoint de la \_ classe VirtualSystemReferencePointService MSVM</span><span class="sxs-lookup"><span data-stu-id="ebd36-103">CreateReferencePoint method of the Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="ebd36-104">Crée un point de référence d’un système virtuel.</span><span class="sxs-lookup"><span data-stu-id="ebd36-104">Creates a reference point of a virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebd36-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ebd36-105">Syntax</span></span>


```mof
uint32 CreateReferencePoint(
  [in]      Msvm_ComputerSystem              REF AffectedSystem,
  [in]      string                               ReferencePointSettings,
  [in]      uint16                               ReferencePointType,
  [in, out] Msvm_VirtualSystemReferencePoint REF ResultingReferencePoint,
  [out]     CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ebd36-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ebd36-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebd36-107">*AffectedSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ebd36-107">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebd36-108">Un [**MSVM \_ ComputerSystem**](msvm-computersystem.md) qui fait référence au système virtuel affecté.</span><span class="sxs-lookup"><span data-stu-id="ebd36-108">A [**Msvm\_ComputerSystem**](msvm-computersystem.md) that references the affected virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="ebd36-109">*ReferencePointSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ebd36-109">*ReferencePointSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebd36-110">Contient les paramètres.</span><span class="sxs-lookup"><span data-stu-id="ebd36-110">Contains the parameter settings.</span></span>

</dd> <dt>

<span data-ttu-id="ebd36-111">*ReferencePointType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ebd36-111">*ReferencePointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebd36-112">Type de point de référence demandé :</span><span class="sxs-lookup"><span data-stu-id="ebd36-112">Requested reference point type:</span></span>

<dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span data-ttu-id="ebd36-113"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Basé sur le journal** (0)</span><span class="sxs-lookup"><span data-stu-id="ebd36-113"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Log based** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ebd36-114">Basé sur le suivi du journal de réplication Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="ebd36-114">Based on Hyper-V replica log tracking.</span></span>

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span data-ttu-id="ebd36-115"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**Basé sur RCT** (1)</span><span class="sxs-lookup"><span data-stu-id="ebd36-115"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT based** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ebd36-116">Basé sur une Change Tracking résiliente des disques virtuels.</span><span class="sxs-lookup"><span data-stu-id="ebd36-116">Based on Resilient Change Tracking of virtual disks.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ebd36-117">*ResultingReferencePoint* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ebd36-117">*ResultingReferencePoint* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ebd36-118">Point de référence du système virtuel résultant</span><span class="sxs-lookup"><span data-stu-id="ebd36-118">Resulting virtual system reference point</span></span>

</dd> <dt>

<span data-ttu-id="ebd36-119">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ebd36-119">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ebd36-120">Si l’opération est exécutée à long terme, vous pouvez éventuellement retourner un travail.</span><span class="sxs-lookup"><span data-stu-id="ebd36-120">If the operation is long running, then optionally a job may be returned.</span></span> <span data-ttu-id="ebd36-121">Dans ce cas, l’instance de la [**classe \_ MSVM VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) représentant le nouveau point de référence système virtuel est présentée via l’Association [**CIM \_ AffectedJobElement**](cim-affectedjobelement.md) avec la valeur de la propriété **AffectedElement** qui fait référence à la nouvelle instance de la classe MSVM **\_ VirtualSystemReferencePoint** représentant le point de référence système virtuel et la valeur de la **ElementEffects** définie à 5 (créer).</span><span class="sxs-lookup"><span data-stu-id="ebd36-121">In this case, the instance of the [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) class representing the new virtual system reference point is presented via the [**CIM\_AffectedJobElement**](cim-affectedjobelement.md) association with the value of the **AffectedElement** property referring to the new instance of the **Msvm\_VirtualSystemReferencePoint** class representing the virtual system reference point and the value of the **ElementEffects** set to 5 (Create).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebd36-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ebd36-122">Return value</span></span>

<span data-ttu-id="ebd36-123">En cas de réussite, retourne 0 ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="ebd36-123">On success, returns 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="ebd36-124">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="ebd36-124">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ebd36-125">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="ebd36-125">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ebd36-126">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="ebd36-126">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ebd36-127">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="ebd36-127">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ebd36-128">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="ebd36-128">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ebd36-129">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="ebd36-129">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ebd36-130">**Type non valide** (6)</span><span class="sxs-lookup"><span data-stu-id="ebd36-130">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="ebd36-131">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="ebd36-131">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ebd36-132">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="ebd36-132">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ebd36-133">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="ebd36-133">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="ebd36-134">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="ebd36-134">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ebd36-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebd36-135">Requirements</span></span>



| <span data-ttu-id="ebd36-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ebd36-136">Requirement</span></span> | <span data-ttu-id="ebd36-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebd36-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebd36-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebd36-138">Minimum supported client</span></span><br/> | <span data-ttu-id="ebd36-139">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ebd36-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="ebd36-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebd36-140">Minimum supported server</span></span><br/> | <span data-ttu-id="ebd36-141">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ebd36-141">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="ebd36-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ebd36-142">Namespace</span></span><br/>                | <span data-ttu-id="ebd36-143">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="ebd36-143">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ebd36-144">MOF</span><span class="sxs-lookup"><span data-stu-id="ebd36-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ebd36-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ebd36-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ebd36-146">DLL</span><span class="sxs-lookup"><span data-stu-id="ebd36-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebd36-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ebd36-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ebd36-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebd36-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebd36-149">**MSVM \_ VirtualSystemReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="ebd36-149">**Msvm\_VirtualSystemReferencePointService**</span></span>](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




