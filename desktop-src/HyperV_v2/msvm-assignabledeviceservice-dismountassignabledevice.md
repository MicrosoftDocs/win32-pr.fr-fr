---
description: Démonte l’appareil PCI spécifié afin qu’il puisse être attribué.
ms.assetid: 8ea3bc27-93ba-4db8-a4aa-cdfea225eaa9
title: Méthode DismountAssignableDevice de la classe Msvm_AssignableDeviceService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceService.DismountAssignableDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 53036cd09113430d1045c8e9eae7a8d782b35960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530601"
---
# <a name="dismountassignabledevice-method-of-the-msvm_assignabledeviceservice-class"></a><span data-ttu-id="d3f29-103">Méthode DismountAssignableDevice de la \_ classe AssignableDeviceService MSVM</span><span class="sxs-lookup"><span data-stu-id="d3f29-103">DismountAssignableDevice method of the Msvm\_AssignableDeviceService class</span></span>

<span data-ttu-id="d3f29-104">Démonte l’appareil PCI spécifié afin qu’il puisse être attribué.</span><span class="sxs-lookup"><span data-stu-id="d3f29-104">Dismounts the specified PCI device so that it can be assigned.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3f29-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d3f29-105">Syntax</span></span>


```mof
uint32 DismountAssignableDevice(
  [in]  string              DismountSettingData,
  [out] string              DismountedDeviceInstancePath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d3f29-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d3f29-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3f29-107">*DismountSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d3f29-107">*DismountSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3f29-108">Instance incorporée d’un objet de données de paramètre qui spécifie le périphérique PCI à démonter.</span><span class="sxs-lookup"><span data-stu-id="d3f29-108">Embedded instance of a setting data object that specifies the PCI device to dismount.</span></span>

</dd> <dt>

<span data-ttu-id="d3f29-109">*DismountedDeviceInstancePath* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d3f29-109">*DismountedDeviceInstancePath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3f29-110">Chaîne contenant le chemin d’accès de l’instance d’appareil à l’appareil démonté.</span><span class="sxs-lookup"><span data-stu-id="d3f29-110">String containing the device instance path to the dismounted device.</span></span>

</dd> <dt>

<span data-ttu-id="d3f29-111">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d3f29-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3f29-112">Référence au travail (peut avoir la valeur null si la tâche est terminée).</span><span class="sxs-lookup"><span data-stu-id="d3f29-112">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3f29-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d3f29-113">Return value</span></span>

<span data-ttu-id="d3f29-114">En cas de réussite, retourne 0 ou 4096 ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="d3f29-114">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="d3f29-115">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="d3f29-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d3f29-116">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="d3f29-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d3f29-117">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="d3f29-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="d3f29-118">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="d3f29-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="d3f29-119">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="d3f29-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="d3f29-120">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="d3f29-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="d3f29-121">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="d3f29-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="d3f29-122">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="d3f29-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="d3f29-123">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="d3f29-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="d3f29-124">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="d3f29-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="d3f29-125">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="d3f29-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="d3f29-126">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="d3f29-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="d3f29-127">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="d3f29-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="d3f29-128">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="d3f29-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d3f29-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d3f29-129">Requirements</span></span>



| <span data-ttu-id="d3f29-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d3f29-130">Requirement</span></span> | <span data-ttu-id="d3f29-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3f29-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3f29-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3f29-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d3f29-133">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d3f29-133">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d3f29-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3f29-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d3f29-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d3f29-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="d3f29-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d3f29-136">Namespace</span></span><br/>                | <span data-ttu-id="d3f29-137">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="d3f29-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d3f29-138">MOF</span><span class="sxs-lookup"><span data-stu-id="d3f29-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d3f29-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d3f29-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d3f29-140">DLL</span><span class="sxs-lookup"><span data-stu-id="d3f29-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3f29-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d3f29-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d3f29-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3f29-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3f29-143">**MSVM \_ AssignableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="d3f29-143">**Msvm\_AssignableDeviceService**</span></span>](msvm-assignabledeviceservice.md)
</dt> </dl>

 

 




