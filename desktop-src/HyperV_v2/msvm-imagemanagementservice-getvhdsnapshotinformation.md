---
description: Récupère des informations sur une capture instantanée de disque dur virtuel dans un fichier de définition de VHD.
ms.assetid: 43745935-9bc3-4a87-8762-54693b2cdef6
title: Méthode GetVHDSnapshotInformation de la classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVHDSnapshotInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 85ea18e2be5329345ba49f4956307c4b29134ed6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514210"
---
# <a name="getvhdsnapshotinformation-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="c934a-103">Méthode GetVHDSnapshotInformation de la \_ classe ImageManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="c934a-103">GetVHDSnapshotInformation method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="c934a-104">Récupère des informations sur une capture instantanée de disque dur virtuel dans un fichier de définition de VHD.</span><span class="sxs-lookup"><span data-stu-id="c934a-104">Retrieves information about a VHD Snapshot within a VHD Set file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c934a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c934a-105">Syntax</span></span>


```mof
uint32 GetVHDSnapshotInformation(
  [in]  string              VHDSetPath,
  [in]  string              SnapshotIds[],
  [in]  uint32              AdditionalInformation[],
  [out] string              SnapshotInformation[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="c934a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c934a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c934a-107">*VHDSetPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c934a-107">*VHDSetPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c934a-108">Chemin d’accès qualifié complet qui spécifie l’emplacement du fichier de définition de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="c934a-108">A fully-qualified path that specifies the location of the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="c934a-109">*SnapshotIds* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c934a-109">*SnapshotIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c934a-110">Liste de GUID représentant les ID d’instantané de chaque capture instantanée pour laquelle les informations sont demandées.</span><span class="sxs-lookup"><span data-stu-id="c934a-110">A list of GUIDs representing the Snapshot Ids of each Snapshot for which information is being requested.</span></span> <span data-ttu-id="c934a-111">Si ce paramètre a la valeur NULL, les informations de tous les instantanés sont récupérées.</span><span class="sxs-lookup"><span data-stu-id="c934a-111">If this parameter is NULL, information for all Snapshots will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="c934a-112">*AdditionalInformation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c934a-112">*AdditionalInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c934a-113">Tableau spécifiant les informations supplémentaires à collecter sur chaque instantané de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="c934a-113">An array specifying what additional information should be gathered about each VHD Snapshot.</span></span> <span data-ttu-id="c934a-114">Chaque entrée du tableau est un type d’informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="c934a-114">Each entry in the array is a type of additional information.</span></span> <span data-ttu-id="c934a-115">Si ce paramètre a la valeur NULL, aucune information supplémentaire n’est récupérée.</span><span class="sxs-lookup"><span data-stu-id="c934a-115">If this parameter is NULL, no additional information will be retrieved.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c934a-116">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="c934a-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c934a-117">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="c934a-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Parent_Paths"></span><span id="parent_paths"></span><span id="PARENT_PATHS"></span>

<span data-ttu-id="c934a-118">**Chemins d’accès parents** (2)</span><span class="sxs-lookup"><span data-stu-id="c934a-118">**Parent Paths** (2)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="c934a-119">*SnapshotInformation* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c934a-119">*SnapshotInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c934a-120">En cas de réussite, un tableau d’informations sur chaque capture instantanée demandée.</span><span class="sxs-lookup"><span data-stu-id="c934a-120">If successful, an array of information about each requested snapshot.</span></span> <span data-ttu-id="c934a-121">Chaque élément est une instance incorporée de [**MSVM \_ VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md).</span><span class="sxs-lookup"><span data-stu-id="c934a-121">Each element is an embedded instance of [**Msvm\_VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="c934a-122">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c934a-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c934a-123">Référence au travail (peut avoir la valeur null si la tâche est terminée).</span><span class="sxs-lookup"><span data-stu-id="c934a-123">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c934a-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c934a-124">Return value</span></span>

<span data-ttu-id="c934a-125">La méthode retourne l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="c934a-125">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="c934a-126">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="c934a-126">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c934a-127">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="c934a-127">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c934a-128">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="c934a-128">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="c934a-129">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="c934a-129">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="c934a-130">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="c934a-130">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="c934a-131">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="c934a-131">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="c934a-132">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="c934a-132">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="c934a-133">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="c934a-133">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="c934a-134">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="c934a-134">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="c934a-135">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="c934a-135">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="c934a-136">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="c934a-136">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="c934a-137">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="c934a-137">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="c934a-138">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="c934a-138">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="c934a-139">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="c934a-139">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c934a-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c934a-140">Requirements</span></span>



| <span data-ttu-id="c934a-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c934a-141">Requirement</span></span> | <span data-ttu-id="c934a-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="c934a-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c934a-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c934a-143">Minimum supported client</span></span><br/> | <span data-ttu-id="c934a-144">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c934a-144">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="c934a-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c934a-145">Minimum supported server</span></span><br/> | <span data-ttu-id="c934a-146">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c934a-146">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="c934a-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c934a-147">Namespace</span></span><br/>                | <span data-ttu-id="c934a-148">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="c934a-148">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c934a-149">MOF</span><span class="sxs-lookup"><span data-stu-id="c934a-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c934a-150"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c934a-150"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c934a-151">DLL</span><span class="sxs-lookup"><span data-stu-id="c934a-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c934a-152"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c934a-152"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c934a-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c934a-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c934a-154">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="c934a-154">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




