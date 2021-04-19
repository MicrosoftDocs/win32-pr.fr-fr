---
description: Ajoute les sous-réseaux du réseau de migration pour le service de migration de système virtuel.
ms.assetid: b0e0f187-beeb-4fdf-a91c-f6c5500f0f6d
title: Méthode AddNetworkSettings de la classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.AddNetworkSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 75d168b1a49d8ac44ab66ba9da13d1e598c647b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544869"
---
# <a name="addnetworksettings-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="cf09c-103">Méthode AddNetworkSettings de la \_ classe VirtualSystemMigrationService MSVM</span><span class="sxs-lookup"><span data-stu-id="cf09c-103">AddNetworkSettings method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="cf09c-104">Ajoute les sous-réseaux du réseau de migration pour le service de migration de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="cf09c-104">Adds migration network subnets for the virtual system migration service.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf09c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cf09c-105">Syntax</span></span>


```mof
uint32 AddNetworkSettings(
  [in]  string              NetworkSettings[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="cf09c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cf09c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf09c-107">*NetworkSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cf09c-107">*NetworkSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf09c-108">Tableau d’instances incorporées de la classe [**MSVM \_ VirtualSystemMigrationNetworkSettingData**](msvm-virtualsystemmigrationnetworksettingdata.md) qui contiennent les paramètres réseau de migration.</span><span class="sxs-lookup"><span data-stu-id="cf09c-108">An array of embedded instances of the [**Msvm\_VirtualSystemMigrationNetworkSettingData**](msvm-virtualsystemmigrationnetworksettingdata.md) class that contain the migration network settings.</span></span>

</dd> <dt>

<span data-ttu-id="cf09c-109">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cf09c-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf09c-110">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cf09c-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf09c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cf09c-111">Return value</span></span>

<span data-ttu-id="cf09c-112">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="cf09c-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="cf09c-113">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="cf09c-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cf09c-114">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="cf09c-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="cf09c-115">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="cf09c-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="cf09c-116">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="cf09c-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="cf09c-117">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="cf09c-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="cf09c-118">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="cf09c-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="cf09c-119">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="cf09c-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="cf09c-120">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="cf09c-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="cf09c-121">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="cf09c-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="cf09c-122">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="cf09c-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="cf09c-123">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="cf09c-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="cf09c-124">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="cf09c-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="cf09c-125">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="cf09c-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="cf09c-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cf09c-126">Requirements</span></span>



| <span data-ttu-id="cf09c-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cf09c-127">Requirement</span></span> | <span data-ttu-id="cf09c-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf09c-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf09c-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf09c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="cf09c-130">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cf09c-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="cf09c-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf09c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="cf09c-132">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cf09c-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cf09c-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cf09c-133">Namespace</span></span><br/>                | <span data-ttu-id="cf09c-134">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="cf09c-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="cf09c-135">MOF</span><span class="sxs-lookup"><span data-stu-id="cf09c-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cf09c-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cf09c-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cf09c-137">DLL</span><span class="sxs-lookup"><span data-stu-id="cf09c-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf09c-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cf09c-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cf09c-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf09c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf09c-140">**ModifyNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="cf09c-140">**ModifyNetworkSettings**</span></span>](modifynetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[<span data-ttu-id="cf09c-141">**RemoveNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="cf09c-141">**RemoveNetworkSettings**</span></span>](removenetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[<span data-ttu-id="cf09c-142">**MSVM \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="cf09c-142">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

