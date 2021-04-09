---
description: Ajoute des sources de démarrage à une configuration de système virtuel lorsqu’elle est appliquée à une &\# 0034 ; état&\# 0034 ; configuration du système virtuel.
ms.assetid: 2d091554-73d4-47c6-a0c2-97644fc9abe9
title: Méthode AddBootSourceSettings de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddBootSourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8e20a1184e11113ba25ac060ec19dab5d2391b84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112287"
---
# <a name="addbootsourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="80d37-103">Méthode AddBootSourceSettings de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="80d37-103">AddBootSourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="80d37-104">Ajoute des sources de démarrage à une configuration de système virtuel lorsqu’elle est appliquée à une configuration de système virtuel « État ».</span><span class="sxs-lookup"><span data-stu-id="80d37-104">Adds boot sources to a virtual system configuration when applied to a "state" virtual system configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="80d37-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80d37-105">Syntax</span></span>


```mof
uint32 AddBootSourceSettings(
  [in]  CIM_VirtualSystemSettingData REF AffectedConfiguration,
  [in]  string                           BootSourceSettings[],
  [out] CIM_SettingData              REF ResultingBootSourceSettings[],
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="80d37-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="80d37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80d37-107">*AffectedConfiguration* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="80d37-107">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80d37-108">[**\_ VirtualSystemSettingData CIM**](cim-virtualsystemsettingdata.md) contenant la configuration affectée.</span><span class="sxs-lookup"><span data-stu-id="80d37-108">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) containing the affected configuration.</span></span>

</dd> <dt>

<span data-ttu-id="80d37-109">*BootSourceSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="80d37-109">*BootSourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80d37-110">Tableau contenant les paramètres de la source de démarrage.</span><span class="sxs-lookup"><span data-stu-id="80d37-110">An array containing the boot source settings.</span></span>

</dd> <dt>

<span data-ttu-id="80d37-111">*ResultingBootSourceSettings* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="80d37-111">*ResultingBootSourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80d37-112">En cas de réussite, retourne un [**\_ SettingData CIM**](cim-settingdata.md) avec les paramètres de source de démarrage résultants.</span><span class="sxs-lookup"><span data-stu-id="80d37-112">On success, returns a [**CIM\_SettingData**](cim-settingdata.md) with the resulting boot source settings.</span></span>

</dd> <dt>

<span data-ttu-id="80d37-113">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="80d37-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80d37-114">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="80d37-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80d37-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="80d37-115">Return value</span></span>

<span data-ttu-id="80d37-116">En cas de réussite, retourne 0 ou 4096 ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="80d37-116">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="80d37-117">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="80d37-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="80d37-118">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="80d37-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="80d37-119">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="80d37-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="80d37-120">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="80d37-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="80d37-121">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="80d37-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="80d37-122">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="80d37-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="80d37-123">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="80d37-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="80d37-124">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="80d37-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="80d37-125">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="80d37-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="80d37-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80d37-126">Requirements</span></span>



| <span data-ttu-id="80d37-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80d37-127">Requirement</span></span> | <span data-ttu-id="80d37-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="80d37-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80d37-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80d37-129">Minimum supported client</span></span><br/> | <span data-ttu-id="80d37-130">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="80d37-130">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="80d37-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80d37-131">Minimum supported server</span></span><br/> | <span data-ttu-id="80d37-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="80d37-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="80d37-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="80d37-133">Namespace</span></span><br/>                | <span data-ttu-id="80d37-134">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="80d37-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="80d37-135">MOF</span><span class="sxs-lookup"><span data-stu-id="80d37-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80d37-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="80d37-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="80d37-137">DLL</span><span class="sxs-lookup"><span data-stu-id="80d37-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80d37-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="80d37-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="80d37-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80d37-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80d37-140">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="80d37-140">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

