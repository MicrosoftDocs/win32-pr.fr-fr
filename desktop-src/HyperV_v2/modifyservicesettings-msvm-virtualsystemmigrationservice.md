---
description: Modifie les données de paramètre pour le service de migration.
ms.assetid: 5162fe88-dd39-4fe0-b8e9-e9b70c2b6a5c
title: Méthode ModifyServiceSettings de la classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e1e9dc96196752ec4408939adc418e7c43bc0c35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526176"
---
# <a name="modifyservicesettings-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="250bc-103">Méthode ModifyServiceSettings de la \_ classe VirtualSystemMigrationService MSVM</span><span class="sxs-lookup"><span data-stu-id="250bc-103">ModifyServiceSettings method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="250bc-104">Modifie les données de paramètre pour le service de migration.</span><span class="sxs-lookup"><span data-stu-id="250bc-104">Modifies the setting data for the migration service.</span></span>

## <a name="syntax"></a><span data-ttu-id="250bc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="250bc-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              ServiceSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="250bc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="250bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="250bc-107">*ServiceSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="250bc-107">*ServiceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="250bc-108">Une instance incorporée de la classe [**MSVM \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) qui contient les nouveaux paramètres de service.</span><span class="sxs-lookup"><span data-stu-id="250bc-108">An embedded instance of the [**Msvm\_VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) class that contains the new service settings.</span></span>

</dd> <dt>

<span data-ttu-id="250bc-109">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="250bc-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="250bc-110">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="250bc-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="250bc-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="250bc-111">Return value</span></span>

<span data-ttu-id="250bc-112">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="250bc-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="250bc-113">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="250bc-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="250bc-114">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="250bc-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="250bc-115">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="250bc-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="250bc-116">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="250bc-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="250bc-117">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="250bc-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="250bc-118">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="250bc-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="250bc-119">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="250bc-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="250bc-120">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="250bc-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="250bc-121">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="250bc-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="250bc-122">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="250bc-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="250bc-123">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="250bc-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="250bc-124">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="250bc-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="250bc-125">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="250bc-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="250bc-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="250bc-126">Requirements</span></span>



| <span data-ttu-id="250bc-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="250bc-127">Requirement</span></span> | <span data-ttu-id="250bc-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="250bc-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="250bc-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="250bc-129">Minimum supported client</span></span><br/> | <span data-ttu-id="250bc-130">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="250bc-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="250bc-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="250bc-131">Minimum supported server</span></span><br/> | <span data-ttu-id="250bc-132">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="250bc-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="250bc-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="250bc-133">Namespace</span></span><br/>                | <span data-ttu-id="250bc-134">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="250bc-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="250bc-135">MOF</span><span class="sxs-lookup"><span data-stu-id="250bc-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="250bc-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="250bc-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="250bc-137">DLL</span><span class="sxs-lookup"><span data-stu-id="250bc-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="250bc-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="250bc-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="250bc-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="250bc-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="250bc-140">**MSVM \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="250bc-140">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

