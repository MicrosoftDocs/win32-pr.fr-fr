---
description: Ajoute des paramètres génériques à une configuration de système virtuel.
ms.assetid: ae04be39-0401-43e9-b19b-3539ca1786ec
title: Méthode AddSystemComponentSettings de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddSystemComponentSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 56ca8bed752bab52f6a82e18975dd5df72dbe12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515412"
---
# <a name="addsystemcomponentsettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="d11b2-103">Méthode AddSystemComponentSettings de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="d11b2-103">AddSystemComponentSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="d11b2-104">Ajoute des paramètres génériques à une configuration de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="d11b2-104">Adds generic settings to a virtual system configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="d11b2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d11b2-105">Syntax</span></span>


```mof
uint32 AddSystemComponentSettings(
  [in]  Msvm_VirtualSystemSettingData   REF AffectedConfiguration,
  [in]  string                              ComponentSettings[],
  [out] Msvm_SystemComponentSettingData REF ResultingComponentSettings[],
  [out] CIM_ConcreteJob                 REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d11b2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d11b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d11b2-107">*AffectedConfiguration* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d11b2-107">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="d11b2-108">*ComponentSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d11b2-108">*ComponentSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d11b2-109">Paramètres du composant à ajouter.</span><span class="sxs-lookup"><span data-stu-id="d11b2-109">The component settings to add.</span></span>

</dd> <dt>

<span data-ttu-id="d11b2-110">*ResultingComponentSettings* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d11b2-110">*ResultingComponentSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d11b2-111">En cas de réussite, fait référence à un [**MSVM \_ SystemComponentSettingData**](msvm-systemcomponentsettingdata.md) qui contient les paramètres de composant résultants.</span><span class="sxs-lookup"><span data-stu-id="d11b2-111">On success, references a [**Msvm\_SystemComponentSettingData**](msvm-systemcomponentsettingdata.md) that contains the resulting component settings.</span></span>

</dd> <dt>

<span data-ttu-id="d11b2-112">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d11b2-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d11b2-113">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d11b2-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d11b2-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d11b2-114">Return value</span></span>

<span data-ttu-id="d11b2-115">En cas de réussite, retourne 0 ou 4096 ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="d11b2-115">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="d11b2-116">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="d11b2-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d11b2-117">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="d11b2-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d11b2-118">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="d11b2-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d11b2-119">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="d11b2-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d11b2-120">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="d11b2-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d11b2-121">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="d11b2-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d11b2-122">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="d11b2-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d11b2-123">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="d11b2-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="d11b2-124">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="d11b2-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d11b2-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d11b2-125">Requirements</span></span>



| <span data-ttu-id="d11b2-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d11b2-126">Requirement</span></span> | <span data-ttu-id="d11b2-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="d11b2-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d11b2-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d11b2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d11b2-129">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d11b2-129">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d11b2-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d11b2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d11b2-131">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d11b2-131">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="d11b2-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d11b2-132">Namespace</span></span><br/>                | <span data-ttu-id="d11b2-133">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="d11b2-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d11b2-134">MOF</span><span class="sxs-lookup"><span data-stu-id="d11b2-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d11b2-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d11b2-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d11b2-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d11b2-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d11b2-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d11b2-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d11b2-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d11b2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d11b2-139">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="d11b2-139">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

