---
description: Optimise un fichier de définition de disque dur virtuel pour utiliser moins d’espace disque.
ms.assetid: 2d2f4531-5d2d-4334-bcc2-d3d3c15b1f46
title: Méthode OptimizeVHDSet de la classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.OptimizeVHDSet
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c360dcd8acf0a4721b8921cd2ca914c34002d078
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862934"
---
# <a name="optimizevhdset-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="4df0d-103">Méthode OptimizeVHDSet de la \_ classe ImageManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="4df0d-103">OptimizeVHDSet method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="4df0d-104">Optimise un fichier de définition de disque dur virtuel pour utiliser moins d’espace disque.</span><span class="sxs-lookup"><span data-stu-id="4df0d-104">Optimizes a VHD Set file to use less disk space.</span></span>

## <a name="syntax"></a><span data-ttu-id="4df0d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4df0d-105">Syntax</span></span>


```mof
uint32 OptimizeVHDSet(
  [in]  string              VHDSetPath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="4df0d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4df0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4df0d-107">*VHDSetPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4df0d-107">*VHDSetPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4df0d-108">Chemin d’accès qualifié complet qui spécifie l’emplacement du fichier de définition de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="4df0d-108">A fully-qualified path that specifies the location of the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="4df0d-109">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4df0d-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4df0d-110">Référence au travail (peut avoir la valeur null si la tâche est terminée).</span><span class="sxs-lookup"><span data-stu-id="4df0d-110">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4df0d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4df0d-111">Return value</span></span>

<span data-ttu-id="4df0d-112">La méthode retourne l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="4df0d-112">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="4df0d-113">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="4df0d-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4df0d-114">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="4df0d-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="4df0d-115">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="4df0d-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="4df0d-116">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="4df0d-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="4df0d-117">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="4df0d-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="4df0d-118">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="4df0d-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="4df0d-119">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="4df0d-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="4df0d-120">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="4df0d-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="4df0d-121">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="4df0d-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="4df0d-122">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="4df0d-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="4df0d-123">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="4df0d-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="4df0d-124">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="4df0d-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="4df0d-125">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="4df0d-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="4df0d-126">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="4df0d-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="4df0d-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4df0d-127">Requirements</span></span>



| <span data-ttu-id="4df0d-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4df0d-128">Requirement</span></span> | <span data-ttu-id="4df0d-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="4df0d-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4df0d-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4df0d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4df0d-131">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4df0d-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="4df0d-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4df0d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4df0d-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="4df0d-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="4df0d-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4df0d-134">Namespace</span></span><br/>                | <span data-ttu-id="4df0d-135">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="4df0d-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4df0d-136">MOF</span><span class="sxs-lookup"><span data-stu-id="4df0d-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4df0d-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4df0d-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4df0d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="4df0d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4df0d-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4df0d-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4df0d-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4df0d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4df0d-141">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="4df0d-141">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




