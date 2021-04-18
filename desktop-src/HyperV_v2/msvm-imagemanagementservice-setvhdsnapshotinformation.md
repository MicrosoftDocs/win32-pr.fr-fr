---
description: Modifie une entrée d’instantané de disque dur virtuel dans un fichier de définition de VHD. Si l’ID d’instantané en question existe déjà, l’entrée d’instantané existante sera remplacée par la nouvelle entrée. Dans le cas contraire, la nouvelle entrée sera ajoutée au fichier de définition de disque dur virtuel.
ms.assetid: dd14960d-3fb8-4d47-986f-fbbbb08eb37d
title: Méthode SetVHDSnapshotInformation de la classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.SetVHDSnapshotInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 54f5ac23cdf8f49532a05eee3fd23293715cd02a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519341"
---
# <a name="setvhdsnapshotinformation-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="82446-105">Méthode SetVHDSnapshotInformation de la \_ classe ImageManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="82446-105">SetVHDSnapshotInformation method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="82446-106">Modifie une entrée d’instantané de disque dur virtuel dans un fichier de définition de VHD.</span><span class="sxs-lookup"><span data-stu-id="82446-106">Edits a VHD Snapshot entry within a VHD Set file.</span></span> <span data-ttu-id="82446-107">Si l’ID d’instantané en question existe déjà, l’entrée d’instantané existante sera remplacée par la nouvelle entrée.</span><span class="sxs-lookup"><span data-stu-id="82446-107">If the Snapshot Id in question already exists, the existing Snapshot entry will be overwritten with the new entry.</span></span> <span data-ttu-id="82446-108">Dans le cas contraire, la nouvelle entrée sera ajoutée au fichier de définition de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="82446-108">Otherwise, the new entry will be added to the VHD Set file.</span></span>

## <a name="syntax"></a><span data-ttu-id="82446-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82446-109">Syntax</span></span>


```mof
uint32 SetVHDSnapshotInformation(
  [in]  string              Information,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="82446-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="82446-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82446-111">*Informations* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="82446-111">*Information* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82446-112">Informations sur les instantanés VHD à modifier ou à ajouter dans le fichier de définition de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="82446-112">VHD Snapshot Information to be changed or added in the VHD Set file.</span></span> <span data-ttu-id="82446-113">La chaîne est une instance incorporée de [**MSVM \_ VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md).</span><span class="sxs-lookup"><span data-stu-id="82446-113">The string is an embedded instance of [**Msvm\_VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="82446-114">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="82446-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82446-115">Référence au travail (peut avoir la valeur null si la tâche est terminée).</span><span class="sxs-lookup"><span data-stu-id="82446-115">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82446-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="82446-116">Return value</span></span>

<span data-ttu-id="82446-117">La méthode retourne l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="82446-117">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="82446-118">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="82446-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="82446-119">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="82446-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="82446-120">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="82446-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="82446-121">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="82446-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="82446-122">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="82446-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="82446-123">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="82446-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="82446-124">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="82446-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="82446-125">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="82446-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="82446-126">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="82446-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="82446-127">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="82446-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="82446-128">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="82446-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="82446-129">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="82446-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="82446-130">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="82446-130">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="82446-131">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="82446-131">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="82446-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="82446-132">Requirements</span></span>



| <span data-ttu-id="82446-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="82446-133">Requirement</span></span> | <span data-ttu-id="82446-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="82446-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82446-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="82446-135">Minimum supported client</span></span><br/> | <span data-ttu-id="82446-136">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="82446-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="82446-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="82446-137">Minimum supported server</span></span><br/> | <span data-ttu-id="82446-138">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="82446-138">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="82446-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="82446-139">Namespace</span></span><br/>                | <span data-ttu-id="82446-140">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="82446-140">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="82446-141">MOF</span><span class="sxs-lookup"><span data-stu-id="82446-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="82446-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="82446-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="82446-143">DLL</span><span class="sxs-lookup"><span data-stu-id="82446-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82446-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="82446-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="82446-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82446-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82446-146">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="82446-146">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




