---
description: Modifie les données de paramètre de fusion de disque.
ms.assetid: 91775dc5-105a-4e38-a334-fb34dd4e59f8
title: Méthode ModifyDiskMergeSettings de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyDiskMergeSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fe737c084b4c1c76a411ce1d2eba513554b40f83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543119"
---
# <a name="modifydiskmergesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="1b8d8-103">Méthode ModifyDiskMergeSettings de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="1b8d8-103">ModifyDiskMergeSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="1b8d8-104">Modifie les données de paramètre de fusion de disque.</span><span class="sxs-lookup"><span data-stu-id="1b8d8-104">Modifies the disk merge setting data.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b8d8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1b8d8-105">Syntax</span></span>


```mof
uint32 ModifyDiskMergeSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="1b8d8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1b8d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b8d8-107">*SettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1b8d8-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b8d8-108">Une instance incorporée de la classe [**MSVM \_ DiskMergeSettingData**](msvm-diskmergesettingdata.md) qui contient les données de paramètre modifiées pour la fonction de fusion de disque.</span><span class="sxs-lookup"><span data-stu-id="1b8d8-108">An embedded instance of the [**Msvm\_DiskMergeSettingData**](msvm-diskmergesettingdata.md) class that contains modified setting data for the disk merge function.</span></span>

</dd> <dt>

<span data-ttu-id="1b8d8-109">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1b8d8-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b8d8-110">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1b8d8-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b8d8-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1b8d8-111">Return value</span></span>

<span data-ttu-id="1b8d8-112">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1b8d8-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="1b8d8-113">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="1b8d8-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1b8d8-114">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="1b8d8-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="1b8d8-115">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="1b8d8-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="1b8d8-116">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="1b8d8-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="1b8d8-117">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="1b8d8-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="1b8d8-118">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="1b8d8-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="1b8d8-119">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="1b8d8-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="1b8d8-120">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="1b8d8-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="1b8d8-121">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="1b8d8-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="1b8d8-122">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="1b8d8-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="1b8d8-123">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="1b8d8-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="1b8d8-124">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="1b8d8-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="1b8d8-125">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="1b8d8-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1b8d8-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b8d8-126">Requirements</span></span>



| <span data-ttu-id="1b8d8-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1b8d8-127">Requirement</span></span> | <span data-ttu-id="1b8d8-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b8d8-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b8d8-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b8d8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1b8d8-130">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b8d8-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1b8d8-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b8d8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1b8d8-132">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b8d8-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1b8d8-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1b8d8-133">Namespace</span></span><br/>                | <span data-ttu-id="1b8d8-134">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="1b8d8-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1b8d8-135">MOF</span><span class="sxs-lookup"><span data-stu-id="1b8d8-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1b8d8-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1b8d8-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1b8d8-137">DLL</span><span class="sxs-lookup"><span data-stu-id="1b8d8-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b8d8-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1b8d8-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1b8d8-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b8d8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b8d8-140">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="1b8d8-140">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

