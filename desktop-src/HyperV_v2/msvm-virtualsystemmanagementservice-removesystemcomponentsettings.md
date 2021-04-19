---
description: Supprime les paramètres de composant génériques d’une configuration de système virtuel.
ms.assetid: 54ddb960-65b7-409d-ad80-f3685562a1a1
title: Méthode RemoveSystemComponentSettings de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveSystemComponentSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 93ef7b794b901212fad72a1fcdf6223d8344b8c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514789"
---
# <a name="removesystemcomponentsettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="d468a-103">Méthode RemoveSystemComponentSettings de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="d468a-103">RemoveSystemComponentSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="d468a-104">Supprime les paramètres de composant génériques d’une configuration de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="d468a-104">Removes generic component settings from a virtual system configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="d468a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d468a-105">Syntax</span></span>


```mof
uint32 RemoveSystemComponentSettings(
  [in]  Msvm_SystemComponentSettingData REF ComponentSettings[],
  [out] CIM_ConcreteJob                 REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d468a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d468a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d468a-107">*ComponentSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d468a-107">*ComponentSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d468a-108">Tableau de [**\_ SystemComponentSettingData MSVM**](msvm-systemcomponentsettingdata.md) qui référencent les paramètres de composant à supprimer.</span><span class="sxs-lookup"><span data-stu-id="d468a-108">Array of [**Msvm\_SystemComponentSettingData**](msvm-systemcomponentsettingdata.md) that reference the component settings to remove.</span></span>

</dd> <dt>

<span data-ttu-id="d468a-109">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d468a-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d468a-110">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d468a-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d468a-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d468a-111">Return value</span></span>

<span data-ttu-id="d468a-112">Retourne 0 ou 4096 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="d468a-112">Returns 0 or 4096 on a success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="d468a-113">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="d468a-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d468a-114">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="d468a-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d468a-115">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="d468a-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d468a-116">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="d468a-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d468a-117">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="d468a-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d468a-118">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="d468a-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d468a-119">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="d468a-119">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d468a-120">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="d468a-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d468a-121">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="d468a-121">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="d468a-122">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="d468a-122">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d468a-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d468a-123">Requirements</span></span>



| <span data-ttu-id="d468a-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d468a-124">Requirement</span></span> | <span data-ttu-id="d468a-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="d468a-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d468a-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d468a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d468a-127">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d468a-127">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d468a-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d468a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d468a-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d468a-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="d468a-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d468a-130">Namespace</span></span><br/>                | <span data-ttu-id="d468a-131">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="d468a-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d468a-132">MOF</span><span class="sxs-lookup"><span data-stu-id="d468a-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d468a-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d468a-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d468a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="d468a-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d468a-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d468a-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d468a-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d468a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d468a-137">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="d468a-137">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

