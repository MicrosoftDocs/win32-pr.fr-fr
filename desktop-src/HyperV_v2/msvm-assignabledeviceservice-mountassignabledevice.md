---
description: Monte l’appareil PCI spécifié afin qu’il puisse être utilisé par le système de l’ordinateur hôte.
ms.assetid: 2a07174e-c221-4c04-81b8-5968aa67e235
title: Méthode MountAssignableDevice de la classe Msvm_AssignableDeviceService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceService.MountAssignableDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: df5f8a337fbf4baf47a4f695322944ed0b97e82e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541846"
---
# <a name="mountassignabledevice-method-of-the-msvm_assignabledeviceservice-class"></a><span data-ttu-id="f364b-103">Méthode MountAssignableDevice de la \_ classe AssignableDeviceService MSVM</span><span class="sxs-lookup"><span data-stu-id="f364b-103">MountAssignableDevice method of the Msvm\_AssignableDeviceService class</span></span>

<span data-ttu-id="f364b-104">Monte l’appareil PCI spécifié afin qu’il puisse être utilisé par le système de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="f364b-104">Mounts the specified PCI device so that it can be used by the host computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="f364b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f364b-105">Syntax</span></span>


```mof
uint32 MountAssignableDevice(
  [in]  string              DeviceInstancePath,
  [in]  string              DeviceLocationPath,
  [out] string              MountedDeviceInstancePath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f364b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f364b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f364b-107">*DeviceInstancePath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f364b-107">*DeviceInstancePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f364b-108">Chaîne contenant le chemin d’accès de l’instance d’appareil à un appareil.</span><span class="sxs-lookup"><span data-stu-id="f364b-108">String containing the device instance path to a device.</span></span>

</dd> <dt>

<span data-ttu-id="f364b-109">*DeviceLocationPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f364b-109">*DeviceLocationPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f364b-110">Chaîne contenant le chemin d’accès de l’emplacement de l’appareil à un appareil.</span><span class="sxs-lookup"><span data-stu-id="f364b-110">String containing the device location path to a device.</span></span>

</dd> <dt>

<span data-ttu-id="f364b-111">*MountedDeviceInstancePath* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f364b-111">*MountedDeviceInstancePath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f364b-112">Chaîne contenant le chemin d’accès à l’instance du périphérique monté.</span><span class="sxs-lookup"><span data-stu-id="f364b-112">String containing the device instance path to the mounted device.</span></span>

</dd> <dt>

<span data-ttu-id="f364b-113">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f364b-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f364b-114">Référence au travail (peut avoir la valeur null si la tâche est terminée).</span><span class="sxs-lookup"><span data-stu-id="f364b-114">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f364b-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f364b-115">Return value</span></span>

<span data-ttu-id="f364b-116">En cas de réussite, retourne 0 ou 4096 ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="f364b-116">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="f364b-117">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="f364b-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f364b-118">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="f364b-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f364b-119">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="f364b-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f364b-120">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="f364b-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f364b-121">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="f364b-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f364b-122">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="f364b-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f364b-123">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="f364b-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f364b-124">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="f364b-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f364b-125">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="f364b-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f364b-126">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="f364b-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f364b-127">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="f364b-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f364b-128">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="f364b-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f364b-129">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="f364b-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="f364b-130">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="f364b-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f364b-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f364b-131">Requirements</span></span>



| <span data-ttu-id="f364b-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f364b-132">Requirement</span></span> | <span data-ttu-id="f364b-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="f364b-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f364b-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f364b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f364b-135">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f364b-135">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f364b-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f364b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f364b-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f364b-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f364b-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f364b-138">Namespace</span></span><br/>                | <span data-ttu-id="f364b-139">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="f364b-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f364b-140">MOF</span><span class="sxs-lookup"><span data-stu-id="f364b-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f364b-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f364b-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f364b-142">DLL</span><span class="sxs-lookup"><span data-stu-id="f364b-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f364b-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f364b-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f364b-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f364b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f364b-145">**MSVM \_ AssignableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="f364b-145">**Msvm\_AssignableDeviceService**</span></span>](msvm-assignabledeviceservice.md)
</dt> </dl>

 

 




