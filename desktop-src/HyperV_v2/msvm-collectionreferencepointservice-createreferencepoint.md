---
description: Crée un point de référence d’une collection de systèmes virtuels.
ms.assetid: 40ec5715-0dbc-43e3-a305-c8c31de60977
title: Méthode CreateReferencePoint de la classe Msvm_CollectionReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.CreateReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7681795ee18965e3e04b75c800e3e574d6627ea9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321102"
---
# <a name="createreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a><span data-ttu-id="e3284-103">Méthode CreateReferencePoint de la \_ classe CollectionReferencePointService MSVM</span><span class="sxs-lookup"><span data-stu-id="e3284-103">CreateReferencePoint method of the Msvm\_CollectionReferencePointService class</span></span>

<span data-ttu-id="e3284-104">Crée un point de référence d’une collection de systèmes virtuels.</span><span class="sxs-lookup"><span data-stu-id="e3284-104">Creates a reference point of a virtual system collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3284-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e3284-105">Syntax</span></span>


```mof
uint32 CreateReferencePoint(
  [in]      Msvm_VirtualSystemCollection REF Collection,
  [in]      string                           ReferencePointSettings,
  [in]      uint16                           ReferencePointType,
  [in, out] CIM_Collection               REF ResultingReferencePointCollection,
  [out]     CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="e3284-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e3284-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3284-107">*Collection* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e3284-107">*Collection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3284-108">Référence à la collection de systèmes virtuels affectés.</span><span class="sxs-lookup"><span data-stu-id="e3284-108">Reference to the affected virtual system collection.</span></span>

</dd> <dt>

<span data-ttu-id="e3284-109">*ReferencePointSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e3284-109">*ReferencePointSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3284-110">Paramètres.</span><span class="sxs-lookup"><span data-stu-id="e3284-110">Parameter settings.</span></span>

</dd> <dt>

<span data-ttu-id="e3284-111">*ReferencePointType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e3284-111">*ReferencePointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3284-112">Indique le type du point de référence.</span><span class="sxs-lookup"><span data-stu-id="e3284-112">Indicates the type of the reference point.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e3284-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="e3284-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span data-ttu-id="e3284-114"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Basé sur le journal** (1)</span><span class="sxs-lookup"><span data-stu-id="e3284-114"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Log based** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e3284-115">Suivi du journal de réplication Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="e3284-115">Hyper-V replica log tracking.</span></span>

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span data-ttu-id="e3284-116"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**Basé sur RCT** (2)</span><span class="sxs-lookup"><span data-stu-id="e3284-116"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT based** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e3284-117">Basé sur une Change Tracking résiliente des disques virtuels.</span><span class="sxs-lookup"><span data-stu-id="e3284-117">Based on Resilient Change Tracking of virtual disks.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e3284-118"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="e3284-118"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="e3284-119"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="e3284-119"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="e3284-120">*ResultingReferencePointCollection* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e3284-120">*ResultingReferencePointCollection* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3284-121">Point de référence résultant d’une collection de systèmes virtuels.</span><span class="sxs-lookup"><span data-stu-id="e3284-121">Resulting reference point of a virtual system collection.</span></span>

</dd> <dt>

<span data-ttu-id="e3284-122">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e3284-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3284-123">Si l’opération est exécutée à long terme, vous pouvez éventuellement retourner un travail.</span><span class="sxs-lookup"><span data-stu-id="e3284-123">If the operation is long running, then optionally a job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3284-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e3284-124">Return value</span></span>

<span data-ttu-id="e3284-125">En cas de réussite, retourne 0 (aucune erreur) ou 4096 (travail démarré); Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="e3284-125">If successful, returns either 0 (no error), or 4096 (job started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="e3284-126">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="e3284-126">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e3284-127">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="e3284-127">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e3284-128">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="e3284-128">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e3284-129">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="e3284-129">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e3284-130">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="e3284-130">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e3284-131">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="e3284-131">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e3284-132">**Type non valide** (6)</span><span class="sxs-lookup"><span data-stu-id="e3284-132">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="e3284-133">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="e3284-133">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e3284-134">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="e3284-134">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e3284-135">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="e3284-135">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="e3284-136">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="e3284-136">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e3284-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e3284-137">Requirements</span></span>



| <span data-ttu-id="e3284-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e3284-138">Requirement</span></span> | <span data-ttu-id="e3284-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3284-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3284-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3284-140">Minimum supported client</span></span><br/> | <span data-ttu-id="e3284-141">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e3284-141">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="e3284-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3284-142">Minimum supported server</span></span><br/> | <span data-ttu-id="e3284-143">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e3284-143">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e3284-144">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e3284-144">Namespace</span></span><br/>                | <span data-ttu-id="e3284-145">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="e3284-145">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e3284-146">MOF</span><span class="sxs-lookup"><span data-stu-id="e3284-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e3284-147"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e3284-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e3284-148">DLL</span><span class="sxs-lookup"><span data-stu-id="e3284-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3284-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e3284-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e3284-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3284-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3284-151">**MSVM \_ CollectionReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="e3284-151">**Msvm\_CollectionReferencePointService**</span></span>](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




