---
description: Récupère des informations sur un fichier de définition de disque dur virtuel.
ms.assetid: efdfd4c6-b762-4369-add3-e152652c6802
title: Méthode GetVHDSetInformation de la classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVHDSetInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 16cdcf4a354e6d6b47b6a67c071daf8883905f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514047"
---
# <a name="getvhdsetinformation-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="1ab33-103">Méthode GetVHDSetInformation de la \_ classe ImageManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="1ab33-103">GetVHDSetInformation method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="1ab33-104">Récupère des informations sur un fichier de définition de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="1ab33-104">Retrieves information about a VHD Set file.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ab33-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ab33-105">Syntax</span></span>


```mof
uint32 GetVHDSetInformation(
  [in]  string              VHDSetPath,
  [in]  uint32              AdditionalInformation[],
  [out] string              Information,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="1ab33-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1ab33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ab33-107">*VHDSetPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1ab33-107">*VHDSetPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ab33-108">Chemin d’accès qualifié complet qui spécifie l’emplacement du fichier de définition de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="1ab33-108">A fully-qualified path that specifies the location of the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="1ab33-109">*AdditionalInformation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1ab33-109">*AdditionalInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ab33-110">Tableau spécifiant les informations supplémentaires qui doivent être collectées à propos du fichier de définition de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="1ab33-110">An array specifying what additional information should be gathered about the VHD Set file.</span></span> <span data-ttu-id="1ab33-111">Chaque entrée du tableau est un type d’informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="1ab33-111">Each entry in the array is a type of additional information.</span></span> <span data-ttu-id="1ab33-112">Si ce paramètre a la valeur NULL, aucune information supplémentaire n’est récupérée.</span><span class="sxs-lookup"><span data-stu-id="1ab33-112">If this parameter is NULL, no additional information will be retrieved.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1ab33-113">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="1ab33-113">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1ab33-114">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="1ab33-114">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Paths"></span><span id="paths"></span><span id="PATHS"></span>

<span data-ttu-id="1ab33-115">**Chemins d’accès** (2)</span><span class="sxs-lookup"><span data-stu-id="1ab33-115">**Paths** (2)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="1ab33-116">*Informations* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1ab33-116">*Information* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ab33-117">En cas de réussite, cet objet contient les informations relatives au fichier de définition de disque dur virtuel demandé.</span><span class="sxs-lookup"><span data-stu-id="1ab33-117">If successful, this object contains the information for the requested VHD Set file.</span></span> <span data-ttu-id="1ab33-118">Il s’agit d’une instance incorporée de [**MSVM \_ VHDSetInformation**](msvm-vhdsetinformation.md).</span><span class="sxs-lookup"><span data-stu-id="1ab33-118">This is an embedded instance of [**Msvm\_VHDSetInformation**](msvm-vhdsetinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ab33-119">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1ab33-119">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ab33-120">Référence au travail (peut avoir la valeur null si la tâche est terminée).</span><span class="sxs-lookup"><span data-stu-id="1ab33-120">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ab33-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1ab33-121">Return value</span></span>

<span data-ttu-id="1ab33-122">La méthode retourne l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="1ab33-122">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="1ab33-123">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="1ab33-123">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1ab33-124">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="1ab33-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="1ab33-125">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="1ab33-125">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="1ab33-126">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="1ab33-126">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="1ab33-127">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="1ab33-127">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="1ab33-128">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="1ab33-128">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="1ab33-129">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="1ab33-129">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="1ab33-130">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="1ab33-130">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="1ab33-131">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="1ab33-131">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="1ab33-132">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="1ab33-132">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="1ab33-133">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="1ab33-133">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="1ab33-134">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="1ab33-134">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="1ab33-135">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="1ab33-135">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="1ab33-136">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="1ab33-136">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1ab33-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ab33-137">Requirements</span></span>



| <span data-ttu-id="1ab33-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ab33-138">Requirement</span></span> | <span data-ttu-id="1ab33-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ab33-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ab33-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ab33-140">Minimum supported client</span></span><br/> | <span data-ttu-id="1ab33-141">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1ab33-141">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="1ab33-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ab33-142">Minimum supported server</span></span><br/> | <span data-ttu-id="1ab33-143">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="1ab33-143">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="1ab33-144">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1ab33-144">Namespace</span></span><br/>                | <span data-ttu-id="1ab33-145">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="1ab33-145">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1ab33-146">MOF</span><span class="sxs-lookup"><span data-stu-id="1ab33-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ab33-147"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1ab33-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ab33-148">DLL</span><span class="sxs-lookup"><span data-stu-id="1ab33-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ab33-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1ab33-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1ab33-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ab33-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ab33-151">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="1ab33-151">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




