---
description: Convertit un fichier de disque dur virtuel en créant un nouveau fichier de définition de disque dur virtuel en même temps que le disque dur virtuel existant.
ms.assetid: 04ae723e-e3c5-4640-a0e5-0e1b75bb2e6d
title: Méthode ConvertVirtualHardDiskToVHDSet de la classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ConvertVirtualHardDiskToVHDSet
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6113a14f321ff7319f8be15767621db3a7e833de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952964"
---
# <a name="convertvirtualharddisktovhdset-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="37154-103">Méthode ConvertVirtualHardDiskToVHDSet de la \_ classe ImageManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="37154-103">ConvertVirtualHardDiskToVHDSet method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="37154-104">Convertit un fichier de disque dur virtuel en créant un nouveau fichier de définition de disque dur virtuel en même temps que le disque dur virtuel existant.</span><span class="sxs-lookup"><span data-stu-id="37154-104">Converts a virtual hard disk file by creating a new VHD Set file alongside the existing virtual hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="37154-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37154-105">Syntax</span></span>


```mof
uint32 ConvertVirtualHardDiskToVHDSet(
  [in]  string              VirtualHardDiskPath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="37154-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="37154-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37154-107">*VirtualHardDiskPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="37154-107">*VirtualHardDiskPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37154-108">Chaîne contenant le chemin d’accès au fichier de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="37154-108">String containing the path to the virtual hard disk file.</span></span> <span data-ttu-id="37154-109">Le nouveau fichier de définition de disque dur virtuel aura le même nom de fichier, mais avec le. Extension de disques durs virtuels.</span><span class="sxs-lookup"><span data-stu-id="37154-109">The new VHD Set file will have the same filename but with the .VHDS extension.</span></span>

</dd> <dt>

<span data-ttu-id="37154-110">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="37154-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="37154-111">Référence au travail (peut avoir la valeur null si la tâche est terminée).</span><span class="sxs-lookup"><span data-stu-id="37154-111">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37154-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="37154-112">Return value</span></span>

<span data-ttu-id="37154-113">La méthode retourne l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="37154-113">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="37154-114">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="37154-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="37154-115">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="37154-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="37154-116">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="37154-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="37154-117">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="37154-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="37154-118">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="37154-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="37154-119">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="37154-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="37154-120">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="37154-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="37154-121">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="37154-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="37154-122">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="37154-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="37154-123">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="37154-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="37154-124">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="37154-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="37154-125">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="37154-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="37154-126">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="37154-126">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="37154-127">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="37154-127">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="37154-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37154-128">Requirements</span></span>



| <span data-ttu-id="37154-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37154-129">Requirement</span></span> | <span data-ttu-id="37154-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="37154-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37154-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37154-131">Minimum supported client</span></span><br/> | <span data-ttu-id="37154-132">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37154-132">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="37154-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37154-133">Minimum supported server</span></span><br/> | <span data-ttu-id="37154-134">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="37154-134">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="37154-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="37154-135">Namespace</span></span><br/>                | <span data-ttu-id="37154-136">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="37154-136">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="37154-137">MOF</span><span class="sxs-lookup"><span data-stu-id="37154-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37154-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="37154-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="37154-139">DLL</span><span class="sxs-lookup"><span data-stu-id="37154-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37154-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="37154-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="37154-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37154-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37154-142">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="37154-142">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




